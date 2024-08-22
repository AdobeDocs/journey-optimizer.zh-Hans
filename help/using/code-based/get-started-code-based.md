---
title: 开始使用基于代码的体验
description: 了解 Journey Optimizer 中基于代码的体验
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 82%

---

# 基于代码的渠道快速入门 {#get-sarted-code-based}

[!DNL Journey Optimizer]允许您在所有接触点（如 Web 应用程序、移动应用程序、桌面应用程序、视频控制台、电视连接设备、智能电视、信息亭、ATM、语音助手、IoT 设备等）上个性化和测试要交付给客户的体验。

使用&#x200B;**基于代码的体验**&#x200B;功能，您可以使用简单直观的非可视化编辑器定义入站体验。 它允许您在应用程序或网页的单个位置和更精细的位置插入和编辑特定元素（不管您拥有的应用程序类型如何 ），而不是将修改应用于全部内容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>要详细了解有关基于代码的体验的特定护栏和建议，请参阅[此页面](code-based-prerequisites.md)。


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
<a href="code-based-prerequisites.md"><strong>护栏和先决条件</strong></a>
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
<a href="code-based-implementation-samples.md">
<img alt="验证" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>实施示例</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## 何时使用基于代码的渠道或其他渠道 {#code-based-vs-other-channels}

### 基于代码的渠道与其他渠道对比

何时使用基于代码的渠道，而不是使用其他 [!DNL Journey Optimizer] 渠道？

* 当您的数字资产无法通过 Web 浏览器或移动应用程序进行访问时，您可以考虑随时使用基于代码的体验，在这些情况下，您最好使用 [!DNL Journey Optimizer] [Web 渠道](../web/get-started-web.md){target="_blank"}或 [!DNL Journey Optimizer] [应用程序内消息传递](../in-app/get-started-in-app.md){target="_blank"}渠道。

* 如果您的网站无法加载到 [Web 设计器](../web/edit-web-content.md#work-with-web-designer){target="_blank"}可视化编辑器中，或者您无法使用[浏览器扩展](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"}进行 Web 渠道的可视化创作，则可以使用基于代码的渠道作为 [!DNL Journey Optimizer] Web 渠道的替代方案。

* 如果您具有基于 API 的无头或服务器端实施，还可以使用基于代码的渠道来替代 [!DNL Journey Optimizer] Web 或应用程序内渠道。

### 基于代码的渠道与 Web 渠道对比

要执行 Web 用例，您可以使用 Web 渠道或基于代码的体验，但其中一种体验可能比其他体验更合适，具体取决于您的环境。 下面列出了主要区别，以便您能够就使用哪种渠道做出明智的决策。

**Web**

* 使用 [Web 设计器](../web/edit-web-content.md#work-with-web-designer){target="_blank"}可视编辑器编辑您的内容。
* 您需要在 Web 浏览器上安装 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} 实施和 [Adobe Experience Cloud 可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}扩展。[了解详情](../web/web-prerequisites.md){target="_blank"}
* 通过 Web 渠道，您可以修改页面上的所有内容，并且有一个预定义列表，可用于进行更改。 [了解详情](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* 它易于设置，快捷方便。
* 它是以营销人员为中心的。

**基于代码的体验**

* 使用[个性化编辑器](create-code-based.md#edit-code)编辑内容。
* 基于代码的体验需要以前在实施中的开发工作，以确保您的应用程序可以解释和交付[!DNL Journey Optimizer]在这些位置发布的边缘内容。 [了解详情](code-based-configuration.md#surface-definition)
* 它需要更多的规划，而且只能更改开发人员指定的内容。 因此，必须确定表面上需要修改，然后与开发团队合作构建处理这些更改所需的实施。
* 它允许您使用 JSON 代码内容。
* 它是以开发人员为中心的。

## 工作原理 {#how-it-works}

>[!CAUTION]
>
>此功能适合开发人员和/或经验丰富的用户。具有一定代码编写技能的营销人员可以使用此功能，前提是开发团队处理表面实施和初始设置。

要使用 [!DNL Journey Optimizer] 基于代码的体验功能编辑您的内容，需要检测您的页面或应用程序。为此，您必须在要插入或替换内容的位置预先声明特定的单个位置（称为“[表面](code-based-configuration.md#surface-definition)”）<!--HOW??-->。

>[!NOTE]
>
>当前，与配置关联的内容只能是HTML或JSON。<!--WILL COME LATER: text, image or another format depending on the application-->

实施基于代码的营销活动的主要步骤如下：

1. 在应用程序实施中定义一个[表面](code-based-configuration.md#surface-definition)，这基本上是您要添加基于代码的体验的位置，然后创建引用该位置的基于代码的体验渠道配置，然后使用此配置在[!DNL Journey Optimizer]中创建营销活动。 [了解如何操作](create-code-based.md#create-code-based-campaign)

1. 通过使用[!DNL Journey Optimizer]个性化编辑器为所选配置指定内容来撰写体验。 [了解如何操作](create-code-based.md#edit-code)

1. 您的应用程序实施团队会进行显式 API 或 SDK 调用，以获取命名表面的内容（例如“横幅文本”或“推荐托盘 1”），或应用程序中与 UI 无关的决策点（例如“搜索算法参数”）。在这种情况下，实施团队负责呈现或解释并处理返回的内容。<!--TBC with Robert - should link to a new section with API/SDK call samples-->
