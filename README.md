# 实现 360 全景的 N 种方案

360 全景是一种虚拟现实技术，是对诸如图片、视频等传统媒体的升级。虚拟现实技术为屏幕前的看客带来身临其境的体验，相较于传统媒介具有不可比拟的优势，广泛应用于房产、家居、旅游等领域。可以确定的是，以 360 全景为代表的虚拟现实技术将会越来越普及，广泛应用于各行各业。

360 全景技术一般包括以下流程：数据采集（拍摄）、图片裁剪拼接等处理、应用制作展示。本文主要针对 Web 前端开发者，简单介绍一下制作全景网页的几种方案。

## CSS3

利用 CSS 中的变换、旋转等属性就可以实现一个360全景。实现的基本思路如下：

- 利用 CSS3 做出一个 3D 立方体；
- 在立方体的6个面设置目标图片（利用全景工具导出的图片，一共有6张）；
- 使用perspective、translateZ、transform-style: preserve-3d 等属性改变视图的大小；
- 添加触摸事件改变translateX、translateY的角度数即可实现一个基本的全景图效果；

## three.js

官方示例：
- [webgl_panorama_cube](https://threejs.org/examples/?q=panorama#webgl_panorama_cube)
- [webgl_panorama_equirectangular](https://threejs.org/examples/?q=panorama#webgl_panorama_equirectangular)
- [webgl_video_panorama_equirectangular](https://threejs.org/examples/?q=panorama#webgl_video_panorama_equirectangular)

## pannellum

[pannellum](https://pannellum.org/) 是一个轻量级、免费、开源的基于 webGL 的全景播放器。支持多种投影方式、支持热点、支持漫游、视频等，且文档清晰明了、简单易用、API 比较丰富，易于功能扩展。


## krpano

krpano 是一款专业的全景引擎平台。目前市场中较大的全景平台大部分都用了 krpano (例如：720云)。它用法较复杂，有一定的学习成本，需要掌握其使用的 XML 的各种配置、功能较多较重且是收费的。

## A-FREAM

[A-FREAM](https://aframe.io/) 是一个用来构建虚拟现实（VR）应用的网页开发框架。由WebVR的发起人[Mozilla VR](https://mixedreality.mozilla.org/) 团队所开发，是当下用来开发WebVR内容主流技术方案。

A-Frame 基于HTML，容易上手。但是A-Frame不仅仅是一个3D场景渲染引擎或者一个标记语言。其核心思想是基于Three.js来提供一个声明式、可扩展以及组件化的编程方式，来实现虚拟现实应用。

A-Frame 遵循[WebXR 标准规范](https://immersive-web.github.io/webxr/) ，更侧重于虚拟现实（VR）或者增强现实（AR），360 全景只是其基本功能。

如果只是为了实现全景功能，不建议使用该框架。

## 其他

根据个人了解到的，目前国内 360 全景技术做的比较好的有：

- 百度地图全景（WebGL）
- 贝壳如视（WebGL）
- 酷家乐（krpano、CSS）
- 720 云（krpano、CSS）

## 参考

- [three.js](https://threejs.org/)
- [pannellum](https://pannellum.org/)
- [krpano](https://krpano.com/home/)
- [krpano中文网](http://www.krpano360.com/)
- [A-FREAM](https://aframe.io/)
- [踏得网 A-Frame 中文教程](https://www.techbrood.com/aframe)
- [【CSS进阶】试试酷炫的 3D 视角](https://www.cnblogs.com/coco1s/p/5847080.html)
- [webVR全景图多种方案实现](https://www.cnblogs.com/ifannie/p/9917490.html)
- [实现一个360全景的N种方案](https://mp.weixin.qq.com/s/FRLnaC0wWyLylibufmxERg)
- [VR 资源导航](https://hao.chinavr.net/index.php/)
