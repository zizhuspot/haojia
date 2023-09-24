---
title: How can I quickly and easily configure the Rust toolchain?
date: 2023-09-20 14:12:05
categories:
  - development tool

tags:
  - development tool
  - Rustup
  - Linux
  
description: This article introduces Rustup, a useful management tool that simplifies the process of installing and updating the Rust toolchain. With Rustup installed, you can seamlessly switch between stable, beta, and nightly versions of Rust.

cover: https://s2.loli.net/2023/09/24/HFDJ3Sf1ZXx8pWj.jpg

---

You may be annoyed by different versions of the toolchain, even for Rust. This article introduces Rustup, a useful management tool that simplifies the process of installing and updating the Rust toolchain. With Rustup installed, you can seamlessly switch between stable, beta, and nightly versions of Rust.

![17.png](https://s2.loli.net/2023/09/23/3pnQxHhke6wWyK7.png)

At the time of this writing, the Rust programming language has grown in popularity with many developers and organizations, and one of the reasons for Rust's popularity is that it provides developer-friendly tools that make development more enjoyable.

Rustup, the official tool for managing the Rust toolchain, not only installs Rust and keeps it up to date, but also lets you seamlessly switch between different versions of the Rust compiler and tools. Here's a quick overview of Rustup and some of the commands you'll need to use it.

## Default Installation

If you want to install Rust on Linux, you can use a package manager. On Ubuntu, you can use apt as the package manager.

```ardunio

$ sudo apt-get install rustc cargo

```

This installation is a stable version of the Rust toolchain, ideal for Rust beginners and those who want to try their hand at compiling and running simple programs. Rustc is the rust compiler and cargo is the rust package manager.

However, Rust is a relatively new programming language, and it changes rapidly and is updated frequently, with many new features and specializations being released. These features and functionality are placed in nightly and updated versions of the Rust toolchain.

If you want to try out a new feature without affecting the stable version already installed on your system, you will need to install a newer version of the toolchain. Unfortunately, the package managers in most distributions can't help you do this.

So what can you do? Here's what to do!

## Using rustup


In order to install rustup, you need to download the script from the official website and use the common curl command

```shell

$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs > sh.rustup.rs

```

Before running the installation download script sh.rustup.rs, you can choose to change the installation source to one of the domestic mirrors to speed things up.

```ardunio

export RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static

```

Then start the sh.rustup.rs script to download and install rust.

```shell

$ ./sh.rustup.rs
info: downloading installer

...

```

The script sh.rustup.rs will download the necessary files first, so wait a moment and select option 1 when prompted:

```csharp

1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
> 1

```
After installing, enter the command to view the toolchain version directly, you will find that the terminal prompt still cannot find the corresponding command

```javascript

$ rustc -V
-bash: /usr/bin/rustc: No such file or directory
$ cargo -V
-bash: /usr/bin/rustc: No such file or directory

```

At this point, you need to restart the command terminal in order to reload the environment variables and the bin directory containing cargo.

But I'm lazy, so I'll just manually configure the environment variables to include cargo's bin directory

```shell

$ source $HOME/.cargo/env

```

This will allow you to start using the rust toolchain

```ruby

$ rustc -V
rustc 1.72.0 (5680fa18f 2023-08-23)
$ cargo -V
cargo 1.72.0 (103a7ff2e 2023-08-15)

```

## View installed and active versions

With rustup it is said that you can manage multiple versions of the rust toolchain, so which version of the toolchain is currently in effect?

Use the following commands to find out

```

$ rustup show
Default host: x86_64-unknown-linux-gnu
rustup home:  /home/user/.rustup

stable-x86_64-unknown-linux-gnu (default)
rustc 1.72.0 (5680fa18f 2023-08-23)

```

## Switching between versions

After installing rustup, you can change the toolchain that rust is currently using as needed. If you are currently using the stable version of the toolchain and would like to try out the newly introduced features available in the nightly version, you can easily switch to the nightly version

```arduino

$ rustup default
$ rustup default nightly

```

Correspondingly, if you need to see the exact paths to the Rust compiler and package manager after switching between versions, you can

```bash

$ rustup which rustc
/home/user/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/bin/rustc
$ rustup which cargo
/home/user/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/bin/cargo

```

## Checking and updating

A simple check to see if a new Rust toolchain is available in the release feed:

```ruby

$ rustup check

```

When you get a message that a new version of Rust has been released with some nice features or functionality, how do you get the latest version of Rust? Use the update subcommand.

```ruby

$ rustup update

```

## Update

The commands described above are sufficient for daily use, but there is always something missing. rustup has a lot of commands that can be tapped into, so we suggest you refer to the help section for more detailed information.

```shell

$ rustup --help

```

Maybe you're wondering if you have to search online to find detailed guide information?

![](https://s2.loli.net/2023/09/23/W5UkgeGP8pmdYIR.png)

The good news is that all the Rust documentation has been installed by rustup on your local system and is available offline. You can access the local documentation, which includes books, standard libraries, and more:

```ruby

$ rustup doc
$ rustup doc --book
$ rustup doc --std
$ rustup doc --cargo

```

Of course, Rustup has a full book on GitHub that you can use as a reference.


