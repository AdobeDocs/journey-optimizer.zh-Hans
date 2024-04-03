---
title: 开始使用基于代码的体验
description: 了解 Journey Optimizer 中基于代码的体验
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: d741a34a0418dc88db730d0b953cb5c7db8dc103
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 100%

---

# 基于代码的渠道快速入门 {#get-sarted-code-based}

[!DNL Journey Optimizer]允许您在所有接触点（如 Web 应用程序、移动应用程序、桌面应用程序、视频控制台、电视连接设备、智能电视、信息亭、ATM、语音助手、IoT 设备等）上个性化和测试要交付给客户的体验。

使用&#x200B;**基于代码的体验**&#x200B;功能，您可以使用简单直观的非可视化编辑器定义入站体验。 它允许您在应用程序或网页的单个位置和更精细的位置插入和编辑特定元素（不管您拥有的应用程序类型如何 ），而不是将修改应用于全部内容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

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

* 当您的数字资产无法通过 Web 浏览器或移动应用程序进行访问时，您可以考虑随时使用基于代码的体验，在这些情况下，您最好使用 [!DNL Journey Optimizer] [Web 渠道](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"}。

* 如果您的网站无法加载到 [Web 设计器](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"}进行 Web 渠道的可视化创作，您可以使用基于代码的渠道来替代 [!DNL Journey Optimizer] Web 渠道。

* 如果您具有基于 API 的无头或服务器端实施，还可以使用基于代码的渠道来替代 [!DNL Journey Optimizer] Web 或应用程序内渠道。

### 基于代码的渠道与 Web 渠道对比

要执行 Web 用例，您可以使用 Web 渠道或基于代码的体验，但其中一种体验可能比其他体验更合适，具体取决于您的环境。 下面列出了主要区别，以便您能够就使用哪种渠道做出明智的决策。

**Web**
* 使用 [Web 设计器](../web/edit-web-content.md#work-with-web-designer){target="_blank"}可视编辑器编辑您的内容。
* 您需要 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* 通过 Web 渠道，您可以修改页面上的所有内容，并且有一个预定义列表，可用于进行更改。 [了解详情](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* 它易于设置，快捷方便。
* 它是以营销人员为中心的。

**基于代码的体验**
* 使用[表达式编辑器](create-code-based.md#edit-code)编辑内容。
* 要使用基于代码的体验，需要对您的实现进行预先开发，以确保您的表面能够解释和交付由 [!DNL Journey Optimizer] 在边缘上为这些表面发布的内容。[了解详情](#surface-definition)
* 它需要更多的规划，而且只能更改开发人员指定的内容。 因此，必须确定表面上需要修改以进行个性化或测试的组件（主页横幅、主页图像、菜单栏等），并与开发团队合作构建处理这些更改所需的实现。
* 它允许您使用 JSON 代码内容。
* 它是以开发人员为中心的。

## 工作原理 {#how-it-works}

>[!CAUTION]
>
>此功能适合开发人员和/或经验丰富的用户。具有一定代码编写技能的营销人员可以使用此功能，前提是开发团队处理表面实施和初始设置。

要使用 [!DNL Journey Optimizer] 基于代码的体验功能编辑您的内容，需要检测您的页面或应用程序。为此，您必须在要插入或替换内容的位置预先声明特定的单个位置（称为“[表面](#surface-definition)”）<!--HOW??-->。

>[!NOTE]
>
>当前，与表面关联的内容只能是 HTML 或 JSON。<!--WILL COME LATER: text, image or another format depending on the application-->

实施基于代码的营销活动的主要步骤如下：

1. 定义[表面](#surface-definition)，基本上是您要使用该表面在其中添加基于代码的体验并创建营销活动的位置[!DNL Journey Optimizer]。[了解如何操作](create-code-based.md#create-code-based-campaign)

1. 通过使用 [!DNL Journey Optimizer] 表达式编辑器为选定表面指定内容来编写体验。[了解如何操作](create-code-based.md#edit-code)

1. 您的应用程序实施团队会进行显式 API 或 SDK 调用，以获取命名表面的内容（例如“横幅文本”或“推荐托盘 1”），或应用程序中与 UI 无关的决策点（例如“搜索算法参数”）。在这种情况下，实施团队负责呈现或解释并处理返回的内容。<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## 什么是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定义基于代码的体验表面"
>abstract="基于代码的表面是任何专为用户或系统交互设计的实体，用 URI 唯一地标识它。"

**基于代码的体验表面**&#x200B;是为用户或系统交互设计的任何实体<!--ask Robert to explain further-->，由一个 **URI** 进行唯一标识。

换句话说，可以将表面视为具有实体（接触点）的任何层级层次结构中的容器。<!--good idea to illustrate how it can be seen, but to clarify-->

* 可以是网页、移动设备应用程序、桌面应用程序，以及大型实体中的特定内容位置（例如 `div`）或非标准显示模式（例如，自助服务终端或桌面应用程序横幅）。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 还可以扩展到用于非显示或抽象显示目的的特定内容容器（例如，传递给服务的 JSON Blob）。

* 它还可以是匹配各种客户端表面定义的通配符表面（例如，网站每个页面上的主图像位置可以在表面 URI 中进行转译，例如：web://mydomain.com/*#hero_image）。

表面 URI 基本上由多个部分组成：
1. **类型**：web、mobileapp、atm、kiosk、tvcd、service 等。
1. **属性**：页面 URL 或应用程序捆绑包
1. **容器**：页面/应用程序活动上的位置

下表列出了各种设备的一些表面 URI 定义示例。

**Web 和移动**

| 类型 | URI | 描述 |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | 表示特定域的特定页面中的单个元素，其中元素可以是标签，如以下示例中的标签：hero_banner、top_nav、menu、footer 等。 |
| iOS 应用程序 | `mobileapp://com.vendor.bundle/activity#element` | 表示原生应用程序活动中的特定元素，如按钮或其他视图元素。 |
| Android 应用程序 | `mobileapp://com.vendor.bundle/#element` | 表示原生应用程序中的特定元素。 |

**其他设备类型**

| 类型 | URI | 描述 |
| --------- | ----------- | ------- | 
| 桌面 | `desktop://com.vendor.bundle/#element` | 表示应用程序中的特定元素，如按钮、菜单、主横幅等。 |
| TV 应用程序 | `tvcd://com.vendor.bundle/#element` | 表示智能电视或电视连接设备应用程序中的特定元素 - 捆绑 ID。 |
| 服务 | `service://servicename/#element` | 表示服务器端进程或其他手动实体。 |
| 自助服务终端 | `kiosk://location/screen#element` | 易于添加的其他潜在表面类型示例。 |
| ATM | `atm://location/screen#element` | 易于添加的其他潜在表面类型示例。 |

**通配符表面**

| 类型 | URI | 描述 |
| --------- | ----------- | ------- | 
| 通配符 Web | `wildcard:web://domain.com/*#element` | 通配符表面 - 表示特定域下每个页面中的单个元素。 |
| 通配符 Web | `wildcard:web://*domain.com/*#element` | 通配符表面 - 表示以“domain.com”结尾的所有域下每个页面中的单个元素。 |
