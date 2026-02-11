---
solution: Journey Optimizer
product: journey optimizer
title: 访问和管理挑战和任务
description: 了解如何在Adobe Journey Optimizer中访问、管理和组织忠诚度挑战和任务。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: 8907c18e-4623-4743-a76b-333f34e13baf
source-git-commit: c5d7cbde6e0a9b4b835abac19d33b973f9f364e4
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# 访问和管理挑战和任务 {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md)
* **访问和管理挑战和任务** ◀}︎**您在这里**
* [创建挑战](create-challenges.md)
* [创建任务](create-tasks.md)
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges/){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 访问和管理挑战和任务

要访问忠诚度挑战，请导航到Journey Optimizer并选择&#x200B;**[!UICONTROL 历程管理]**&#x200B;部分下的&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**。 “忠诚度挑战”界面提供了一个集中化的位置来查看、管理和组织所有挑战和任务。

该界面提供对两个主要清单的访问：

* **挑战**：查看和管理所有忠诚度挑战，监视其状态，并执行快速操作，例如查看、编辑、复制或删除挑战
* **任务**：浏览可用于多个挑战的可重用任务，并独立管理任务定义

## 挑战清单 {#challenges-tab}

**[!UICONTROL 挑战]**&#x200B;选项卡按上次修改日期显示所有挑战，最近修改的挑战显示在最前。

![](assets/challenges-inventory.png)

显示的关键信息：

* **[!UICONTROL 状态]**：质询的当前状态（草稿或已发布）
* **[!UICONTROL 任务]**：挑战中配置的任务数
* **[!UICONTROL 历程]**：链接到与质询关联的自动生成历程
* **[!UICONTROL 状态]**：发送质询的自动生成历程的当前状态。
* **[!UICONTROL 开始/结束日期(UTC)]**：质询变为活动状态并过期的时间

在“挑战”选项卡中，您可以对挑战执行操作：

* **查看质询**：选择质询名称以打开其详细信息页面
* **复制挑战**：选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 复制]**。 创建的副本包含所有任务、内容和消息。
* **删除挑战**：选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 删除]**。

  >[!IMPORTANT]
  >
  >即使挑战已发布，您也可以将其删除。 在删除之前请考虑该影响。

* **编辑质询**：选择质询名称以打开其详细信息页面并进行所需的更改。

  当您打开已发布的挑战进行编辑时，您首先需要将其恢复为草稿状态。 直接对自动生成历程所做的任何自定义都将丢失。 进行更改后，再次保存并发布挑战，然后发布关联的历程。 [了解如何发起挑战](create-challenges.md#launch)

  >[!IMPORTANT]
  >
  >无法撤消将已发布的挑战还原为草稿。 在继续之前，请考虑对活动历程的影响。

## 任务清单 {#tasks-tab}

**[!UICONTROL 任务]**&#x200B;选项卡显示所有可用于多个挑战的可重用任务。 在创建或编辑任何挑战时，可以选择此处创建的任务。

![](assets/tasks-inventory.png)

显示的关键信息：

* **[!UICONTROL 描述]**：任务要求的简要描述
* **[!UICONTROL 任务活动]**：活动类型（购买、支出）
* **[!UICONTROL SKU]**：符合条件和/或排除的项目
* **[!UICONTROL 用于挑战]**：当前使用此任务的挑战数

在“任务”选项卡中，您可以对任务执行操作：

* **查看/编辑任务**：选择任务名称以查看完整配置并编辑任务
* **复制任务**：选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 复制]**
* **删除任务**：选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 删除]**。

  >[!IMPORTANT]
  >
  >即使任务用于一个或多个挑战，您也可以将其删除。 考虑删除前对引用任务的挑战的影响。
