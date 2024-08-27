---
title: 基于代码的配置
description: 创建基于代码的配置
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 55%

---

# 配置基于代码的体验 {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="应用程序 ID"
>abstract="提供应用程序 ID，以便在应用程序的运行环境中进行准确识别和配置，确保能够无缝集成并使用相关功能。"

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="页面上的位置"
>abstract="应用程序字段内的位置或路径指定了您希望用户访问的应用程序内的确切目标。这可能是应用程序导航结构深处的特定部分或页面。"

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI 表面"
>abstract="表面 URI 可作为指向应用程序内不同用户界面元素或组件的精确标识符。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="默认创作和预览 URL"
>abstract="该字段可确保该规则生成或匹配的页面具有指定的 URL，这对于有效地创建和预览内容至关重要。"

## 创建渠道配置 {#reatte-code-based-configuration}

要创建渠道配置，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。

   ![](assets/code_config_1.png)

1. 输入配置的名称和说明（可选）。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`字符。

1. 要为配置分配自定义或核心数据使用标签，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)。

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 [了解详情](../action/consent.md#surface-marketing-actions)

1. 选择&#x200B;**基于代码的体验**&#x200B;渠道。

   ![](assets/code_config_2.png)

1. 选择要应用代码库体验的平台。

1. 对于Web：

   * 指定&#x200B;**[!UICONTROL 页面URL]**&#x200B;以独占地应用对单个页面的更改。

   * 或者，创建与规则&#x200B;]**匹配的**[!UICONTROL &#x200B;页面，以定位多个与指定规则匹配的URL。 例如，这可用于在网站中通用应用更改，例如在所有页面中更新主页横幅，或添加要在每个产品页面上显示的顶部图像。 [了解详情](../web/web-configuration.md)

1. 对于iOS和Android：

   * 输入您的&#x200B;**[!UICONTROL 应用程序ID]**&#x200B;和应用程序&#x200B;]**中的位置或路径**[!UICONTROL 。

1. 如果您的实施不适用于Web、iOS或Android，或者您需要定位特定URI，请选择“其他”作为平台。 当选择多个平台或添加多个URI时，内容将交付到所有选定的页面或应用程序。

   * 输入&#x200B;**[!UICONTROL 表面URI]**。

   >[!CAUTION]
   >
   >确保在基于代码的营销活动中使用的表面URI与您自己的实施中使用的表面URI相匹配。 否则，将不会交付更改。

1. 选择该特定位置的应用程序所需的格式。 在营销活动和历程中创作基于代码的体验时，将使用此功能。

1. 提交更改。

在创建基于代码的体验时，您现在可以选择配置。


## 什么是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定义基于代码的体验配置"
>abstract="基于代码的配置定义了应用程序内部的路径和位置，由应用程序实施中的 URI 唯一标识，而内容则会在该路径和位置传送和使用。"

**基于代码的体验表面**&#x200B;是为用户或系统交互而设计的任何实体，它由URI唯一标识。 该界面在应用程序实施中指定，它应该对应于基于代码的体验渠道配置中构成的一个界面。

创建基于代码的体验渠道配置时 — 对于Web、iOS和Android平台，您需要输入路径和位置来构成表面，而如果平台是“其他”，则需要输入完整的URI，如下例所示。

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

