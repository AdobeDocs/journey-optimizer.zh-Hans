---
title: 基于代码的配置
description: 创建基于代码的配置
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: b057d198d3c5b12121ee50d7a97ff4b33b8209b4
workflow-type: tm+mt
source-wordcount: '1558'
ht-degree: 40%

---

# 配置基于代码的体验 {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定义基于代码的体验配置"
>abstract="基于代码的配置定义了应用程序内部的路径和位置，由应用程序实施中的 URI 唯一标识，而内容则会在该路径和位置传送和使用。"

在[构建体验](create-code-based.md)之前，您需要创建基于代码的体验配置，在其中定义内容在应用程序中的交付和使用位置。

基于代码的体验配置必须引用表面，它基本上是您要呈现更改的位置。 根据所选平台，您需要输入位置/路径或完整表面URI。 [了解详情](#surface-definition)

## 创建一个基于代码的体验配置 {#create-code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="指明页面或应用程序里的具体位置"
>abstract="此字段指定了您希望用户访问的页面或应用程序内的确切目标。它可以是网页内的特定部分，也可以是应用程序导航结构深处的页面。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="定义内容创建和预览的 URL"
>abstract="该字段可确保该规则生成或匹配的页面具有指定的 URL，这对于有效地创建和预览内容至关重要。"

要创建基于代码的体验渠道配置，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。

   ![](assets/code_config_1.png)

1. 输入配置的名称和说明（可选）。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`字符。

1. 要为配置分配自定义或核心数据使用标签，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 [了解详情](../action/consent.md#surface-marketing-actions)

1. 选择&#x200B;**基于代码的体验**&#x200B;渠道。

   ![](assets/code_config_2.png)

1. 选择要应用代码库体验的平台：

   * [Web](#web)
   * [iOS和/或Android](#mobile)
   * [其他](#other)

   >[!NOTE]
   >
   >您可以选择多个平台。 当选择多个平台时，内容将交付到所有选定的页面或应用程序。

1. 为此特定位置选择应用程序所需的格式。 在营销活动和历程中创作基于代码的体验时，将使用此功能。

   ![](assets/code_config_4.png)

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以保存更改。

当在营销活动和历程中[创建基于代码的体验](create-code-based.md)时，您现在可以选择此配置。

>[!NOTE]
>
>您的应用程序实施团队负责发出显式API或SDK调用，以获取选定基于代码的体验配置中定义的界面的内容。 在[本节](code-based-implementation-samples.md)中了解关于不同客户实施的更多信息。

### 网络平台 {#web}

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="定义内容创作和预览的 URL"
>abstract="该字段可确保该规则生成或匹配的页面具有指定的 URL，这对于有效地创建和预览内容至关重要。"

要为Web平台定义基于代码的体验配置设置，请执行以下步骤。

1. 选择以下选项之一：

   * **[!UICONTROL 单页]** — 如果要将更改仅应用于单个页面，请输入&#x200B;**[!UICONTROL 页面URL]**。

     ![](assets/code_config_single_page.png)

   * **[!UICONTROL 页面匹配规则]** — 若要定位多个匹配同一规则的URL，请构建一个或多个规则。 [了解详情](../web/web-configuration.md#web-page-matching-rule)

     <!--This could be used to apply changes universally across a website, such as updating a hero banner across all pages or adding a top image to display on every product page.-->

     例如，如果您要编辑显示在Luma网站的所有女性产品页面上的元素，请选择&#x200B;**[!UICONTROL 域]** > **[!UICONTROL 开头为]** > `luma`和&#x200B;**[!UICONTROL 页面]** > **[!UICONTROL 包含]** > `women`。

     ![](assets/code_config_matching_rules.png)

1. 以下内容适用于预览URL：

   * 如果输入了单页URL，则该URL将用于预览 — 无需输入其他URL。
   * 如果选择了与规则](../web/web-configuration.md#web-page-matching-rule)匹配的[页面，则必须输入用于预览浏览器体验的&#x200B;**[!UICONTROL 默认创作和预览URL]**。 [了解详情](../code-based/create-code-based.md#preview-on-device)

     ![](assets/code_config_matching_rules_preview.png)

1. **[!UICONTROL 页面]**&#x200B;上的位置字段指定了您希望用户访问的页面内的确切目标。 它可以是网站导航结构中的某个页面上的特定部分，例如“hero-banner”或“product-rail”。

   ![](assets/code_config_location_on_page.png)

### 移动设备平台（iOS 和 Android） {#mobile}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="提供你的应用程序 ID"
>abstract="输入应用程序 ID，以便在应用程序的运行环境中进行准确识别和配置，确保无缝集成和功能。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="输入预览内容的 URL"
>abstract="此字段对于在您的应用程序中直接在设备上启用内容的模拟和预览至关重要。"

要为移动平台定义基于代码的体验配置设置，请执行以下步骤。

1. 输入您的&#x200B;**[!UICONTROL 应用程序ID]**。 这允许在应用程序的操作环境中进行准确的识别和配置，并确保无缝集成和功能。

1. 提供应用程序&#x200B;]**中的**[!UICONTROL &#x200B;位置或路径。 此字段指定您希望用户访问的应用程序内的确切目标。 它可以是应用程序导航结构深处的特定部分或页面，例如“hero-banner”或“product-rail”。

   ![](assets/code_config_3.png)

1. 填写&#x200B;**[!UICONTROL 预览URL]**&#x200B;字段以启用设备上预览。 此URL通知预览服务在设备上触发预览时要使用的特定URL。 [了解详情](../code-based/create-code-based.md#preview-on-device)

   预览URL是由应用程序开发人员在您的应用程序中配置的深层链接。 这可确保在应用程序中（而不是在移动Web浏览器中）打开任何与深层链接方案匹配的URL。 请联系您的应用程序开发人员，以获取为您的应用程序配置的深层链接方案。

+++  以下资源可帮助您为应用程序实施配置深层链接

   * 对于Android：

      * [创建与应用程序上下文的深层链接](https://developer.android.com/training/app-links/deep-linking)

   * 对于iOS：

      * [为您的应用程序定义自定义 URL 方案](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

      * [在您的应用程序中支持通用链接](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >如果您在预览体验时遇到问题，请参阅[本文档](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link)。

### 其他平台 {#other}

要为其他平台（如视频控制台、电视连接设备、智能电视、网亭、ATM、语音助手、物联网设备等）定义基于代码的体验配置设置，请执行以下步骤。

1. 如果您的实现不适用于Web、iOS或Android，或者需要定位特定的URI，请选择&#x200B;**[!UICONTROL Other]**&#x200B;作为平台。

1. 输入&#x200B;**[!UICONTROL 表面URI]**。 表面URI是一个唯一标识符，对应于您要交付体验的实体。 [了解详情](#surface-definition)

   ![](assets/code_config_5.png)

   >[!CAUTION]
   >
   >确保输入的表面URI与您自己的实施中使用的表面URI相匹配。 否则，将无法交付更改。

1. **[!UICONTROL 如果需要，添加其他表面URI]**。 您最多可以添加10个URI。

   >[!NOTE]
   >
   >添加多个URI时，内容将传递到列出的所有组件。

## 什么是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="为你的组件添加表面 URI"
>abstract="如果您的实施不是针对 Web、iOS 或 Android，或者您需要定位特定的 URI，请输入表面 URI，它是指向您想要提供体验的实体的唯一标识符。确保输入的表面 URI 与您自己的实现中使用的 URI 相匹配。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/code-based-experience/code-based-configuration#other" text="为其他平台创建基于代码的体验配置"

基于代码的体验&#x200B;**surface**&#x200B;是为用户或系统交互而设计的任何实体，它由&#x200B;**URI**&#x200B;唯一标识。 曲面在应用程序实施中指定，必须与基于代码的体验渠道配置中引用的曲面匹配。

在任何层级的容器中，表面都可以被视为存在实体（接触点）的容器。

* 可以是网页、移动设备应用程序、桌面应用程序，以及大型实体中的特定内容位置（例如 `div`）或非标准显示模式（例如，自助服务终端或桌面应用程序横幅）。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 还可以扩展到用于非显示或抽象显示目的的特定内容容器（例如，传递给服务的 JSON Blob）。

* 它还可以是匹配各种客户端表面定义的通配符表面（例如，网站每个页面上的主图像位置可以在表面 URI 中进行转译，例如：web://mydomain.com/*#hero_image）。

创建基于代码的体验渠道配置时，您有两种方式可根据所选平台指定表面：

* 对于&#x200B;**[!UICONTROL Web]**、**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!UICONTROL Android]**&#x200B;平台，您需要输入&#x200B;**位置或路径**&#x200B;来构成表面。

* 如果平台是&#x200B;**[!UICONTROL Other]**，则需要输入完整的&#x200B;**表面URI**，如下面的示例所示。

表面URI用作指向应用程序内不同的用户界面元素或组件的精确标识符。 表面URI基本上由多个部分组成：

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
