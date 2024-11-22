---
title: 基于代码的表面
description: 了解什么是基于代码的体验表面
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 52%

---

# 基于代码的体验平面 {#code-based-surface}

## 什么是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="为您的组件添加表面 URI"
>abstract="如果您的实施不是针对 Web、iOS 或 Android，或者您需要定位特定的 URI，请输入表面 URI，它是指向您想要提供体验的实体的唯一标识符。确保输入的表面 URI 与您自己的实现中使用的 URI 相匹配。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/channels/code-based-experience/code-based-configuration#other" text="为其他平台创建基于代码的体验配置"

基于代码的体验&#x200B;**surface**&#x200B;是为用户或系统交互而设计的任何实体，由[URI](#surface-uri)唯一标识。 该表面在[应用程序实现](code-based-prerequisites.md#implementation-prerequisites)中指定，并且必须匹配在基于[代码的体验渠道配置](code-based-configuration.md)中引用的表面。

在任何层级的容器中，表面都可以被视为存在实体（接触点）的容器。

* 可以是网页、移动设备应用程序、桌面应用程序，以及大型实体中的特定内容位置（例如 `div`）或非标准显示模式（例如，自助服务终端或桌面应用程序横幅）。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 还可以扩展到用于非显示或抽象显示目的的特定内容容器（例如，传递给服务的 JSON Blob）。

* 它还可以是匹配各种客户端表面定义的通配符表面（例如，网站每个页面上的主图像位置可以在表面 URI 中进行转译，例如：web://mydomain.com/*#hero_image）。

## 表面标识符 {#surface-uri}

**表面URI**&#x200B;用作指向应用程序中不同用户界面元素或组件的精确标识符。 表面URI基本上由多个部分组成：

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

## URI合成 {#uri-composition}

在[!DNL Journey Optimizer]中，基于代码的体验渠道支持两种类型的客户实施：

* 基于您网站的[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}，或基于您移动应用程序的[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"}；
* 使用[AEPEdge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"}的服务器端或混合服务器。

>[!NOTE]
>
>在[本节](code-based-prerequisites.md#implementation-prerequisites)中了解关于实施先决条件的更多信息。

使用基于代码的体验，您可以修改粒度位置<!--(such as a specific location on a page, or inside a mobile native app)-->上的内容，这些位置由[!DNL Journey Optimizer]使用[表面URI](#surface-uri)唯一标识。

这些表面URI的构成和处理取决于实施方法：

* **Web/Mobile SDK**：您的Web/Mobile开发人员需要将这些粒度位置定义为简单字符串，因为Web/Mobile SDK能够基于当前URL/应用程序ID和位置字符串自动撰写表面URI。

* **Edge NetworkAPI**：应用程序/页面开发人员必须定义包含完整路径和使用内容的位置的完整表面URI，因为此类型的实现需要完整URI。

这就是为什么在创建基于[代码的体验渠道配置](code-based-configuration.md)时，您有两种方式可根据所选平台指定表面：

* 对于&#x200B;**[!UICONTROL Web]**、**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!UICONTROL Android]**&#x200B;平台，您需要输入&#x200B;**URL/应用程序ID**&#x200B;和&#x200B;**位置或路径**&#x200B;来构成表面。 了解有关为[Web](code-based-configuration.md#web)和[移动设备](code-based-configuration.md#mobile)平台配置基于代码的体验的更多信息

* 如果平台是&#x200B;**[!UICONTROL Other]**，则需要输入完整的&#x200B;**表面URI**，如上面的示例[所示](#surface-uri)。 了解有关为[其他](code-based-configuration.md#other)平台配置基于代码的体验的更多信息
