---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的营销活动中使用事件变量
description: 了解如何在编排的活动中使用事件变量
hide: true
hidefromtoc: true
exl-id: f86dd262-0209-42f6-a180-736f1de98d78
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---

# 使用事件变量 {#event-variables}

某些编排的营销活动允许您在表达式编辑器中编辑脚本以执行特定操作，例如检索来自先前活动的数据、构建条件或根据事件变量计算文件名。

## 什么是事件变量 {#scripting}

在编排的营销活动上下文中执行的脚本访问一系列其他全局&#x200B;**对象**，例如正在执行的编排的营销活动本身(`ìnstance`)、其各种任务(`task`)或激活给定任务的事件(`event`)。

**对象**&#x200B;的每个类型都与&#x200B;**变量**&#x200B;的类别相关联，在诸如&#x200B;**[!UICONTROL JavaScript代码]**&#x200B;或&#x200B;**[!UICONTROL Test]**&#x200B;之类的活动中编辑脚本时，可在表达式编辑器中利用该类别。

* **实例变量** (`instance.vars.xxx`)与全局变量类似。 所有活动都共享它们。
* **任务变量** (`task.vars.xxx`)可与局部变量比较。 它们仅由当前任务使用。 这些变量由永久性活动用来保留数据，有时也用于在同一活动的不同脚本之间交换数据。
* **事件变量** (`vars.xxx`)允许在编排的营销活动进程的基本任务之间交换数据。 这些变量由激活正在进行的任务的任务传递。 然后，它们会被传递到以下活动。 **事件变量**&#x200B;是最常使用的变量，应优先使用它们而不是实例变量。

## 在表达式编辑器中利用事件变量 {#expression-editor}

预定义事件变量可用于表达式编辑器左侧窗格。 您也可以通过在代码中初始化新变量来创建新变量。

![](assets/event-variables.png)

除了这些事件变量之外，您还可以利用左窗格中的&#x200B;**[!UICONTROL 条件]**&#x200B;菜单来构建条件，利用&#x200B;**[!UICONTROL 添加当前日期]**&#x200B;菜单来使用与日期格式相关的函数。
