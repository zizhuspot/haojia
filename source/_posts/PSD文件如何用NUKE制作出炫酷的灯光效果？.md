---
title: PSD文件如何用NUKE制作出炫酷的灯光效果？
date: 2023-07-25 17:39:22
categories:
  -  特效制作
tags:
  -  NUKE
  -  灯光环境
  -  搭建灯光
description: PSD文件使用NUKE制作出逼真的灯光效果，大大提高工作效率
cover: https://s2.loli.net/2023/07/26/qWuQtOEC73rUJ1e.png
---

大家都知道，NUKE可以导入模型，abc、fbx、obj、.....的文件类型，但如果没有模型……，只用美术提供的psd图，如何实现三维灯光模拟效果？
## 1.搭建环境

### STEP 1

搭建nuke三维空间基础节点“Camera、Scene、ScanlineRender”

![](https://s2.loli.net/2023/07/26/qWuQtOEC73rUJ1e.png)

### STEP 2

新建球体模型“Sphere”将psd贴入球体上，中间再增加Project3D，链接到场景；为了方便后续灯光调整，需要在球体模型下方增加“TransformGeo”，调整球体空间位置，使得推远一点。

![](https://s2.loli.net/2023/07/26/duoOfXEqlW6iTDL.png)

![](https://s2.loli.net/2023/07/26/buMDwp6jXZ73YSO.png)

效果如图，这样出来的图与原本psd的图就一致了，可以进行第二步增加灯光动画

![](https://s2.loli.net/2023/07/26/ZVYo1aUABc2OMTq.png)

## 2.增加灯光动画

### STEP 1

把灯光“Light”添加到“scene”场景中；如图：

![](https://s2.loli.net/2023/07/26/CTHVB4gDRU1EiLc.png)

![](https://s2.loli.net/2023/07/26/p1Gn89UtmqLOV6u.png)

### STEP 2

调整灯光动画，调整到自己觉得合适的位置；这里做了两个灯，分别为主灯、副灯；然后根据画面要求设定主次。
![](https://s2.loli.net/2023/07/26/yRSjNmuqrpLEsQB.png)

![](https://s2.loli.net/2023/07/26/bKcreYowjq93OdS.png)


## 3. 最后的补充工作

### STEP 1

赋予模型红绿蓝三通道，使用“HueShift”节点中的“hue rotation”调节红绿蓝通道变化。如图：

![](https://s2.loli.net/2023/07/26/fRlNoQbuE268qZO.png)

![](https://s2.loli.net/2023/07/26/w8p3LuFGYTbzgtX.png)

### STEP 2

优化通道；调整“Grade”、“keyer”、“blur”，使得“Alpha通道”达到需求效果；

![](https://s2.loli.net/2023/07/26/Po3CEKNUJXxg7yq.png)

### STEP 3

调色，使用“grade”节点提亮；

![](https://s2.loli.net/2023/07/26/5ZDjO7cWbFuQ2n3.png)

## **总结**：

本次使用NUKE制作炫酷的灯光效果，主要是要利用颜色通道的调节来达到，这里面需要基本功要踏实，大家要在日常工作使用当中多做总结，这样才能在特效师这个职业上走得更快更远。

## -*拓展资料*

### *使用NUKE的优势*

NUKE以其巨大的技术和精湛的特技，在许多影视节目中得到了广泛的应用。从核综合训练的角度来看，其视觉效果主要表现在以下几个方面。

1：在制作复杂的合成图像时，关键是配置合适的工具，以便应用这些工具并掌握其性能的特殊要求。否则，您将被迫剪切剪辑以获得所需的效果。在这样做的时候，冒着破坏你的生产任务和声誉的风险。

2：这些强大的工具配备了一整套类似NUKE的性能丰富的工具，足以应对工作中的任何挑战，包括NUKE视觉效果和合成系统。这是整个工作中最具挑战性的任务之一：为这些站点进行场景扩展并将它们合成到自己的场景中。

3：使用NUKE的版本来控制电影的合成工作。NUKE是一种功能强大的合成器，可以方便地控制大量的处理工作。核能的优势在于它能在多个处理器上运行。

***tips***:在CG和真实拍摄的结合中，一个用三维软件渲染的小东西可以分成几十层，一个镜头可能有几百层甚至几百层。在AE中处理这种复杂的合成并不特别方便。NUKE的运行流程图非常清晰。

### *NUKE与AE的对比*

1、软件的操作方式：AE是基于“图层”的操作，像PS一样；而Nuke是节点式的操作方式，这和传统的软件有所区别，它通过各个节点去传递功能属性。

2、软件的定位：Nuke本身定位在高端影视制作上；AE则比较难以定位，低、中、高端它都能做，但遇到复杂文件则会捉襟见肘。

3、对于素材的整合能力：ae对于多种格式的素材都是比较包容和接纳的；而nuke在格式支持上目前只支持图片序列和mov的格式，nuke基于通道的合成软件，用作单镜头画面的超高级vfx特效合成， 最多可支持1023条通道信息的合成。

各自优点：

1、AE的优点：素材整合能力很强 psd ai swf gif wav 格式等等都可以当做素材文件，适合处理大小各异的多镜头整体合成。

2、nuke的优点：nuke处理三维vfx合成的能力更佳，且处理视频最高分辨率支持4k以上。









