---
title: Customized DataCap Plugin for Kotlin Running Successfully
date: 2023-09-26 17:32:15
categories:
  - development tool
tags:
  - development tool
  - datacap
  - springboot
  - java
  - program
  
description: DataCap is a full-platform data management tool based on SpringBoot development，DataCap supports custom plug-ins, users can write their own plug-ins integrated into the system, this article focuses on how to quickly integrate a plug-in to the DataCap system.

cover: https://s2.loli.net/2023/09/26/ph8EYRSntKf9xrO.jpg

---

**DataCap** is a full-platform data management tool based on SpringBoot development, with complete features, recommended to download and use. *You can get the tool at github.com/EdurtIO/datacap, which currently supports more than 40+ data sources*. In addition, DataCap is the first project in China to apply ChatGPT to data management system.

*DataCap* supports custom plug-ins, users can write their own plug-ins to integrate into the system. This document mainly explains how to quickly integrate a plugin into the *DataCap* system.

```

This article demonstrates the integration of the StarRocks data storage system based on the JDBC protocol.

```

## pom.xml dependencies

```xml

<dependency>
    <groupId>io.edurt.datacap</groupId>
    <artifactId>datacap-spi</artifactId>
    <scope>provided</scope>
</dependency>
<dependency>
    <groupId>io.edurt.datacap</groupId>
    <artifactId>datacap-common</artifactId>
</dependency>
<dependency>
    <groupId>commons-beanutils</groupId>
    <artifactId>commons-beanutils</artifactId>
</dependency>
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
</dependency>
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-simple</artifactId>
    <scope>test</scope>
</dependency>
<dependency>
    <groupId>org.testcontainers</groupId>
    <artifactId>testcontainers</artifactId>
    <scope>test</scope>
</dependency>

```

The above configuration adds the `datacap-spi` and `datacap-common` modules, and the rest are auxiliary dependencies.


```

Note that you need to specify the version number of each dependency if you are opening the project separately.

```

## plug-in loader


```kotlin

class StarRocksPluginModule : AbstractPluginModule(), PluginModule {
    override fun getName(): String {
        return "StarRocks"
    }

    override fun getType(): PluginType {
        return PluginType.JDBC
    }

    override fun get(): AbstractPluginModule {
        return this
    }

    override fun configure() {
        val module = Multibinder.newSetBinder(binder(), String::class.java)
        module.addBinding().toInstance(this.javaClass.simpleName)
        val plugin: Multibinder<Plugin> = Multibinder.newSetBinder(binder(), Plugin::class.java)
        plugin.addBinding().to(StarRocksPlugin::class.java)
    }
}

```

The loader needs to inherit the `AbstractPluginModule` class and implement the `PluginModule` interface so that the system will automatically load the plugin into the system at startup.


```

Note that you need to override the configure() method in the parent class and bind the plugin to the system.

```

## Plug-in actuators

```kotlin

class StarRocksPlugin : Plugin {
    private val log = getLogger(StarRocksPlugin::class.java)

    private var jdbcConfigure: JdbcConfigure? = null
    private var jdbcConnection: JdbcConnection? = null
    private var jdbcResponse: Response? = null

    override fun name(): String {
        return "StarRocks"
    }

    override fun description(): String {
        return "Integrate StarRocks data sources"
    }

    override fun type(): PluginType {
        return PluginType.JDBC
    }

    override fun connect(configure: Configure?) {
        try {
            log.info("Connecting to StarRocks")
            jdbcResponse = Response()
            jdbcConfigure = JdbcConfigure()
            BeanUtils.copyProperties(jdbcConfigure, configure)
            jdbcConfigure!!.jdbcDriver = "com.mysql.cj.jdbc.Driver"
            jdbcConfigure!!.jdbcType = "mysql"
            jdbcConnection = object : JdbcConnection(jdbcConfigure, jdbcResponse) {}
        } catch (ex: Exception) {
            jdbcResponse!!.isConnected = false
            jdbcResponse!!.message = ex.message
        }
    }

    override fun execute(content: String?): Response {
        if (ObjectUtils.isNotEmpty(jdbcConnection)) {
            log.info("Execute starrocks plugin logic started")
            jdbcResponse = jdbcConnection?.response
            val processor = JdbcAdapter(jdbcConnection)
            jdbcResponse = processor.handlerExecute(content)
            log.info("Execute starrocks plugin logic end")
        }
        destroy()
        return jdbcResponse!!
    }

    override fun destroy() {
        if (ObjectUtils.isNotEmpty(jdbcConnection)) {
            jdbcConnection?.destroy()
            jdbcConnection = null
        }
    }
}

```

The executor needs to implement the Plugin interface, which provides the following methods

- `name()`: the plugin has a unique name, the plugin with the same name will only take effect when it is loaded for the first time.

- `description()`: the description of the plugin.

- `type()`: type of the plugin

- `connect(Configure configure)`: the plugin needs to connect information in advance, such as the current plugin plugin, is the plugin's connection stage (the system preset HTTP connection method used directly).

- `execute(String content)`: the specific execution of the operation logic

- `destroy()`: the final destruction of the plugin, note that the destruction needs to include the information in the connection.

## Plugin converter

The plugin converter is used to transform the result of the current plugin execution into logic that can be used in DataCap. It is mainly used to encapsulate the `Response` return result.

This article is based on the JDBC plug-in so directly inherit `JdbcAdapter` parent class to achieve some of the functions.

## SPI Loader

Add `META-INF` and `services` directories to the `resources` source directory.

```

Services are required in the resources directory.

```

Create the `io.edurt.datacap.spi.PluginModule` file with the following contents

```java

io.edurt.datacap.plugin.jdbc.starrocks.StarRocksPluginModule

```

The contents of this file is our defined plugin loader module.

```

Unit testing of the plugin can be done by referring to the published plugin

```


