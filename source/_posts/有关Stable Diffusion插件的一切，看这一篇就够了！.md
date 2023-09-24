---
title: Everything you need to know about the Stable Diffusion plugin, just read this one!
date: 2023-05-16 18:19:25

categories:
  - Ai Tools
tags: 
  - Stable Diffusion
  - Ai Drawing
  - Stable Diffusion Model
  - Stable Diffusion in action
  - Creative Art
  - Creative Art
  - Ai Tools
  - Artistic Creation
  - Artificial Intelligence
  - Art & Design

description: This article describes the installation/update/uninstallation of the Stable Diffusion plugin in detail, so that practitioners with no basic knowledge of the tool can also be updated and used with ease.

cover: https://s2.loli.net/2023/09/24/7qINDJk3n9greSU.jpg

---

![](https://s2.loli.net/2023/07/27/IRDMANqGWBtxHiv.png)

## I. Plug-in basics

Stable Diffusion WebUI, this open source user interface crafted by the great god Automatic1111, closely around the Stable Diffusion model, in order to let our ordinary users can also be free and easy to experience the charm of the Vincennes technology! Just install it locally and you can enjoy this technological feast right away. It must be mentioned that, since the emergence of WebUI, attracted a large wave of AI painting enthusiasts based on it to develop a variety of plug-ins, constantly optimizing and expanding the functionality of the WebUI, it is simply to push our experience to a climax!

The popular plug-in Controlnet is one of them. These plug-ins are free and open source, their programs and code are generally hosted on the [Github](https://github.com/) platform for the public to access for free, which is why we download WebUI plug-ins are not bypassed Github.

That's why we can't download WebUI plugins without Github. [](https://s2.loli.net/2023/07/27/d6gXeJBoSq4D8vy.jpg)

The Github homepage of the well-known Controlnet plugin, [https://github.com/Mikubill/sd-webui-controlnet](https://github.com/Mikubill/sd-webui-controlnet).

On Github, we can see the detailed information of the plugin, including the plugin overview, functionality, installation/usage, installation requirements, precautions, etc. Plugin installation and download are also used in the resources here, we should carefully read the contents of the Github page before installing a plugin. 

![](https://s2.loli.net/2023/07/27/oP3IlvZkY4c8NB2.jpg)

After the plugin is installed, it will be automatically displayed in the WebUI interface. In "**Extensions-Installed**", you can view all successfully installed plugins and update them; the corresponding source files of the plugins are stored in the "*Extensions*" folder in the root directory of the SD WebUI, which is one of the most important ways for us to manage plugins.

This folder is also one of the important ways for us to manage the plugins. [](https://s2.loli.net/2023/07/27/qPWRTOmY1diN7AS.jpg)

![](https://s2.loli.net/2023/07/27/tgKHF6kDclwdPmL.jpg)

* Take Prompt All-in-One plugin as an example, we will introduce the installation method one by one, and follow the instructions on one of the Github pages. *

- Prompt All-in-One plugin interface: [https://github.com/physton/sd-webui-prompt-all-in-one](https://github.com/physton/sd-webui-prompt-all-in-one)

- Tip All-in-One plugin installation overview: documentation ([physton.github.io](https://physton.github.io/sd-webui-prompt-all-in-one-assets/#/zh-cn/Installation))

## II.Plugin update

There are 2 ways to update the plugin, one is to open SD WebUI, go to "*Extension-Installed*", click "**Check for Updates**" button, wait for the progress to be completed, then click "**Apply and restart the UI**", the plugin update will be completed.

![](https://s2.loli.net/2023/07/27/XJPv5SZtNnL1z8q.jpg)

If you are lucky enough to be using the integration pack personally handled by @Akiba aaaki bigwig from B station, then before launching WebUI, you just need to click on "**Version Management-Expansion**" on the launcher, and you will be able to see the update status of all the plugins that have been successfully installed. Just click "**One Click Update**" in the upper right corner and everything is done! This method is much faster than doing updates inside WebUI, saving time and effort. And you can also uninstall the plugin here. For your information, the two plugins in the picture that say "*Not Git Installed*" are installed by downloading a zip archive, so you can't update them directly from here. But don't worry, that doesn't stop you from enjoying the convenience and fun of other plugins!

![](https://s2.loli.net/2023/07/27/srEJNjObVR2opt4.jpg)

## III. Plugin deactivation/uninstallation

### - Deactivate the plugin

Open WebUI interface, go to "*Extensions-Installed*", find the plugin you want to deactivate in the list, uncheck the checkbox in front of its name, and then click "**Apply and restart the UI**", then you can't see the plugin after re-entering. This way the plugin won't be shown in the WebUI interface, but the file will still be saved in the "*Extensions*" folder in the root directory; uncheck the checkbox and restart the UI, and you can see the plugin again.

![](https://s2.loli.net/2023/07/27/SCjx8uv2QNUlfDV.jpg)

### - Uninstalling a plugin

If you don't want to use a plugin anymore, you can open the "*Extensions*" folder in the root directory, select the corresponding plugin folder, and right-click to delete it. Then restart SD WebUI and the plugin will no longer exist. If you are using the integration pack from @Akihaaaaki, you can also uninstall the corresponding plugin in the "Version Management - Extensions" section of the launcher. Above is how to install, update and uninstall Stable Diffusion WebUI plugin. When installing the plugin, if WebUI shows that the plugin is already installed, you should remove it from the extension. First, a folder in the root directory. Specify the correct file and reinstall.

![](https://s2.loli.net/2023/07/27/QfpCkLsb2qOGH79.jpg)

### About stable diffusion, my experience with it:

Stable Diffusion's ControlNet plugin is a powerful tool that is so powerful that it makes the star of Stable Diffusion shine even brighter. The purpose of this plugin is to enhance the expressiveness of the algorithms, increase stability, and give the user ultra-fine control over the algorithms to meet the needs of application scenarios of all shapes and sizes. Below, I will take you to explore my experience of using Oh!

Installing and configuring the ControlNet plugin is like solving a puzzle game, take it one step at a time and everything will fall into place. First, you need to download and install the Stable Diffusion algorithm library, which is like finding a magic book. Then, you need to use the source code of ControlNet plugin as Lego blocks and link it with the algorithm library to build it. During the configuration process, you need to unravel the mystery of the algorithm and specify some parameters, such as time step, space step, and diffusion coefficient. These parameters are like magic incantations, which can be recited and adjusted according to the actual needs to inspire the best performance and stability.

After completing the installation and configuration, it's like getting a key to open the treasure box, and you can start playing with ControlNet plug-in! It supports a variety of application scenarios, such as machine learning and automation. In the field of machine learning, ControlNet plugin is like a mysterious mage, which can ally with common machine learning frameworks such as TensorFlow, PyTorch, etc., and work together to cast the magic of stability and efficient training.

In the field of automation, the ControlNet plugin is like a control master, which can create fine-grained control strategies to control system behavior at will.

In practice, I have discovered several advantages of the ControlNet plug-in:

Its stability is simply unbelievable! ControlNet plug-in utilizes advanced stability theory to enhance the stability of the algorithm, thus effectively reducing the demand for computing resources.
It is bursting with performance! With optimized algorithms and parallel computing, the ControlNet plug-in can easily handle large-scale datasets with blazing fast computation speeds!
How about it? Isn't it tantalizing? Come together to experience this powerful magic world!



