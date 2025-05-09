---
solution: Journey Optimizer
product: journey optimizer
title: 用例战术手册
description: 了解如何将 Adobe Experience Platform 用例战术手册与 Adobe Journeys Optimizer 结合使用。
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2214ec90-580e-469e-9b14-d8cb2d4bb050
source-git-commit: 7bb46f33d877d0a1976e8d74b88a5cccb81c1d4e
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 69%

---

# 用例战术手册 {#playbooks}

## 什么是用例行动手册 {#gs}

用例战术手册是预定义的工作流程，用于处理您可以使用 Adobe Experience Platform 和 Journey Optimizer 执行的常见用例。

![显示用例战术手册的动画图像](../rn/assets/do-not-localize/playbooks.gif){width="85%"}

每个战术手册都提供了全面的概述，包括实施战术手册的意图、目标、目标角色和所需的资源。此外，每个战术手册中都有思维导图，用于直观地表示与战术手册关联的真实客户接触点。

![发现战术手册视图中的放弃购物车战术手册](assets/playbooks-detail.png){width="85%"}

## 先决条件 {#prerequisites}

在使用用例战术手册之前，需要执行以下配置步骤。有关每个步骤的详细信息，请参阅用例行动手册文档[入门](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/get-started.html?lang=zh-Hans){target="_blank"}页。

* 创建沙盒
* 配置用户权限
* 为电子邮件、推送和短信通知配置 Journey Optimizer 渠道配置

## 访问和启用行动手册 {#access}

要访问手册，请导航到位于左侧导航边栏的&#x200B;**[!UICONTROL 战术手册]**&#x200B;菜单。该库包含多个使用 Adobe Journey Optimizer 实施的战术手册。为了轻松访问战术手册，请使用搜索栏旁边的筛选器。[用例行动手册文档](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/playbooks-list.html?lang=zh-Hans){target="_blank"}中提供了Journey Optimizer行动手册的完整列表。

![打开了带有筛选器窗格的战术手册列表](assets/playbooks-filter.png){width="85%"}

选择最符合您需求的战术手册后，就可以启用该战术手册。这将创建一个战术手册实例，并自动生成支持特定用例所需的资源。资源包括 Journey Optimizer 资产（如历程、消息）以及 Adobe Experience Platform 资产（如架构或区段）。

>[!NOTE]
>
>这些对象旨在帮助您了解实施特定用例所需的所有资源。它们不包含任何数据，并且将在开发沙盒上创建它们。

要实施用例，您可以导航到每个对象并根据需求进行调整。您还可以在团队之间共享战术手册实例页面 URL，以便协作实施用例。

此外，您可以将战术手册资产导入其他沙盒中。假如您已设置自己的架构、字段和字段组，这样做可以使生成的资产与现有资产保持一致，并确保其与数据兼容。用例行动手册文档中详细介绍了这些步骤：[将行动手册生成的资源发布到其他沙盒](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/data-awareness.html?lang=zh-Hans){target="_blank"}。

## 创建您自己的行动手册(Beta) {#create}

>[!AVAILABILITY]
>
>用例行动手册创建目前作为公共测试版提供给所有客户。

除了利用预定义的行动手册之外，您还可以在Adobe Experience Platform中创建并共享您自己的行动手册。

您可以使用AI帮助或手动输入定义元数据，关联技术资产（如架构、区段），并在不同IMS组织之间共享行动手册。

有关如何创建和共享行动手册的更多信息，请参阅用例行动手册文档： [使用AI助手创作和共享您自己的行动手册](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/author.html?lang=zh-Hans#sharing-playbooks-sandboxes){target="_blank"}。
