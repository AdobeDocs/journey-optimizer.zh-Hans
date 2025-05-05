---
title: 内容卡配置
description: 内容卡渠道配置
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: 50e47e83-4b9e-4088-aa09-dea76393c035
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 49%

---

# 配置内容卡片 {#content-card-configuration}

## 什么是配置？ {#surface-definition}

**内容卡体验配置**&#x200B;是为用户或系统交互而设计的任何实体，它由&#x200B;**URI**&#x200B;唯一标识。

换句话说，可以将表面视为具有实体（接触点）的任何层级层次结构中的容器。

* 它可以是网页、移动设备应用程序、桌面应用程序、大型实体中的特定内容位置（例如`div`）或非标准显示模式（例如，自助服务亭或桌面应用程序横幅）。

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

## 创建内容卡配置 {#create-config}

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 品牌]** > **[!UICONTROL 渠道配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。

   ![](assets/content_card_config_1.png)

1. 输入配置的名称和说明（可选）。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线 `_`、点 `.` 和连字符 `-` 符号。

1. 要为配置分配自定义或核心数据使用标签，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)。

1. 选择&#x200B;**[!UICONTROL 内容卡]**&#x200B;渠道。

   ![](assets/content_card_config_2.png)

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 [了解详情](../action/consent.md#surface-marketing-actions)

1. 选择要应用内容卡体验的平台。

   ![](assets/content_card_config_3.png)

1. 对于Web：

   * 指定&#x200B;**[!UICONTROL 页面URL]**&#x200B;以独占地应用对单个页面的更改。

   * 或者，创建与规则&#x200B;**匹配的**&#x200B;页面，以定位多个与指定规则匹配的URL。 例如，这可用于在网站中通用应用更改，例如在所有页面中更新主页横幅，或添加要在每个产品页面上显示的顶部图像。 [了解详情](../web/web-configuration.md)

1. 对于iOS和Android：

   * 输入或选择您的&#x200B;**[!UICONTROL 应用程序ID]**、**[!UICONTROL 应用程序内的位置或路径]**&#x200B;和&#x200B;**[!UICONTROL 预览URL]**。

1. 提交更改。

现在，您可以在创建内容卡体验时选择配置。
