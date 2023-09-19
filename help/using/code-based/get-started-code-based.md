---
title: 开始使用基于代码的体验
description: 了解Journey Optimizer中基于代码的体验
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta 版"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 7%

---

# 基于代码的渠道入门 {#get-sarted-code-based}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* **[基于代码的渠道入门](get-started-code-based.md)**
* [基于代码的先决条件](code-based-prerequisites.md)
* [基于代码的实施示例](code-based-implementation-samples.md)
* [创建基于代码的体验](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>基于代码的体验渠道目前仅作为测试版向部分用户提供。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

[!DNL Journey Optimizer] 允许您在所有接触点（如Web应用程序、移动应用程序、桌面应用程序、视频控制台、电视连接设备、智能电视、信息亭、ATM、语音助手、物联网设备等）上个性化和测试要交付给客户的体验。

使用 **基于代码的体验** 功能，您可以使用简单直观的非可视化编辑器定义入站体验。 它允许您在应用程序或网页的单个和更细粒度的位置插入和编辑特定元素，而不管您拥有的应用程序类型如何 — 而不是将修改应用于整个内容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

当您 [创建活动](../campaigns/create-campaign.md#configure)，选择 **基于代码的体验（测试版）** 作为您的操作并定义基本设置。

>[!NOTE]
>
>如果您是首次创建 Web 体验，请确保遵循[此部分](code-based-prerequisites.md)中叙述的先决条件。

<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="潜在客户" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>工作原理</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="验证" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>先决条件</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="不频繁" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>创建基于代码的体验</strong></a>
</div>
<p></td>
<td>
<a href="create-code-based.md#edit-code">
<img alt="验证" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>编辑代码</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## 何时使用基于代码的渠道（相对于其他渠道） {#code-based-vs-other-channels}

### 基于代码的渠道与其他渠道的对比

何时使用基于代码的渠道，而不是使用其他渠道 [!DNL Journey Optimizer] 渠道？

* 当您的数字资产无法通过Web浏览器或移动应用程序进行访问时，您可以考虑随时使用基于代码的体验，在这些情况下，您可能可以更好地使用 [!DNL Journey Optimizer] [Web渠道](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} 渠道。

* 您可以使用基于代码的渠道作为的替代 [!DNL Journey Optimizer] Web渠道(如果您的网站无法加载到 [Web可视化编辑器](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} 支持Web渠道的可视化创作。

* 您还可以使用基于代码的渠道作为的替代 [!DNL Journey Optimizer] Web或应用程序内渠道，以防您具有基于API的、Headless或服务器端实施。

### 基于代码的与Web渠道的对比

要执行Web用例，您可以使用Web渠道或基于代码的体验，但根据您的上下文，一种体验可能比其他体验更合适。 下面列出了主要区别，以便您能够就何时使用内容做出明智的决策。

**Web**
* 使用编辑内容 [可视编辑器](../web/author-web.md){target="_blank"}.
* 您需要 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* 通过Web渠道，您可以修改页面上的所有内容，并且有一个预定义的可用于更改操作列表。 [了解详情](../web/author-web.md){target="_blank"}
* 它易于设置和快速进行。
* 注重营销人员角色。

**基于代码的体验**
* 使用编辑内容 [代码编辑器](create-code-based.md#edit-code).
* 基于代码的体验要求之前在实施中进行开发，以确保您的界面可以解释和交付在Edge上发布的内容，方法是 [!DNL Journey Optimizer] 用于这些曲面。 [了解详情](#surface-definition)
* 它需要更多的规划，而且只能更改开发人员指定的内容。 因此，必须识别组件（主页横幅、主页图像、菜单栏等） ，并与您的开发团队合作构建处理这些更改所需的实施。
* 它允许您使用JSON代码内容。
* 它是以开发人员角色为中心的。

## 工作原理 {#how-it-works}

>[!CAUTION]
>
>此功能适用于开发人员角色和/或经验丰富的用户。 具有某些代码编写技能的营销人员可以使用此功能，前提是开发团队处理表面实施和初始设置。

要使用，编辑您的内容 [!DNL Journey Optimizer] 基于代码的体验功能，因此需要检测您的页面或应用程序。 为此，您必须预先声明特定的单个位置(称为“[曲面](#surface-definition)“)要插入或替换内容的位置<!--HOW??-->.

>[!NOTE]
>
>当前，与表面关联的内容只能是HTML或JSON。 <!--WILL COME LATER: text, image or another format depending on the application-->

实施基于代码的营销活动的主要步骤如下。

1. 定义 [曲面](#surface-definition)，基本上是您要在其中添加基于代码的体验并创建营销活动的位置 [!DNL Journey Optimizer] 使用这个表面。 [了解如何操作](create-code-based.md#create-code-based-campaign)

1. 通过使用为所选表面指定内容来创作体验 [!DNL Journey Optimizer] 代码编辑器。 [了解如何操作](create-code-based.md#edit-code)

1. 您的应用程序实施团队会进行显式API或SDK调用，以获取命名表面的内容(例如“横幅文本”或“Recommendations任务栏1”)，或应用程序中与UI无关的决策点（例如“搜索算法参数”）。 在这种情况下，实施团队负责呈现或以其他方式解释并处理返回的内容。<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## 什么是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定义基于代码的体验表面"
>abstract="基于代码的界面是为用户或系统交互而设计的任何实体，由URI唯一标识。"

A **基于代码的体验表面** 是专为用户或系统交互而设计的任何实体<!--ask Robert to explain further-->，由唯一标识 **URI**.

换句话说，可以将表面视为具有实体（接触点）的任何层级层次结构中的容器。<!--good idea to illustrate how it can be seen, but to clarify-->

* 它可以是网页、移动设备应用程序、桌面应用程序，以及大型实体中的特定内容位置(例如 `div`)或非标准显示模式（例如，自助服务亭或桌面应用程序横幅）。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 它还可以扩展到特定片段的内容容器，用于非显示或抽象显示目的（例如，交付给服务的JSON Blob）。

* 它还可以是匹配各种客户端表面定义的通配符表面(例如，网站每个页面上的主页图像位置可以在表面URI中进行翻译，例如：web://mydomain.com/*#hero_image)。

表面URI基本上由多个部分组成：
1. **类型**：web、mobileapp、service、kiosk、tvcd等
1. **属性**：域或应用程序捆绑包
1. **路径**：页面/应用程序活动±页面/应用程序活动上的位置 <!--to clarify-->

下表列出了各种设备的一些表面URI定义示例。

| 类型 | URI | 描述 |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | 表示网站的单个路径和页面。 |
| Web | web://domain.com/path/page.html#element | 表示特定域的特定页面中的单个元素。 |
| Web | web://domain.com/*#element | 通配符表面 — 表示特定域下每个页面中的单个元素。 |
| 台式机 | desktop://com.vendor.bundle | 表示特定的桌面应用程序。 |
| 台式机 | desktop://com.vendor.bundle#element | 表示应用程序中的特定元素，如按钮、菜单、主页横幅等。 |
| iOS 应用程序 | ios://com.vendor.bundle | 表示适用于单个平台的特定移动应用程序 — 在本例中为iOS应用程序。 |
| iOS 应用程序 | ios://com.vendor.bundle/activity | 表示移动应用程序中的特定活动（视图）。 |
| iOS 应用程序 | ios://com.vendor.bundle/activity#element | 表示活动中的特定元素，如按钮或其他视图元素。 |
| Android应用程序 | android://com.vendor.bundle | 表示适用于单个平台的特定移动应用程序 — 在本例中为Android应用程序。 |
| tvOS应用程序 | tvos://com.vendor.bundle | 表示特定的tvOS应用程序。 |
| 电视应用程序 | tvcd://com.vendor.bundle | 表示特定的智能电视或电视连接设备应用程序 — 捆绑包ID。 |
| 服务 | service://servicename | 表示服务器端进程或其他手动实体。 |
| 自助服务亭 | kiosk://location/screen | 易于添加的潜在附加曲面类型示例。 |
| ATM | atm://location/screen | 易于添加的潜在附加曲面类型示例。 |