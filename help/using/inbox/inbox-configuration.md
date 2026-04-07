---
title: 收件箱配置
description: 收件箱渠道配置
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 4%

---

# 配置收件箱 {#inbox-configuration}

您必须先在&#x200B;**渠道配置**&#x200B;中定义&#x200B;**[!UICONTROL 收件箱]**&#x200B;渠道配置，然后才能通过收件箱投放内容卡体验。 该配置会将界面与同意、可选访问标签以及体验在Web上或您的iOS或Android应用程序中出现的位置关联起来。 请按照以下步骤创建配置：

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。

   ![](assets/inbox-configuration-1.png)

1. 输入配置的名称和说明（可选）。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线 `_`、点 `.` 和连字符 `-` 符号。

1. 要为配置分配自定义或核心数据使用标签，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)。

1. 选择&#x200B;**[!UICONTROL 收件箱]**&#x200B;频道。

   ![](assets/inbox-configuration-2.png)

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 [了解详情](../action/consent.md#surface-marketing-actions)

1. 选择要应用收件箱体验的平台。

   ![](assets/inbox-configuration-3.png)

1. 对于Web：

   * 在&#x200B;**[!UICONTROL 页面URL]**&#x200B;中，输入或选择收件箱应出现的页面的URL。 当体验限制为一个页面时，可使用此选项。

   * 在&#x200B;**[!UICONTROL 页面]**&#x200B;上的位置中，定义页面内投放位置，例如，网站用于收件箱表面的区域或标识符。 [了解详情](../web/web-configuration.md)

     ![](assets/inbox-configuration-4.png)

1. 对于iOS和Android：

   * 在&#x200B;**[!UICONTROL 应用程序ID]**&#x200B;中，输入或选择应用程序的标识符，以便该配置适用于正确的iOS或Android内部版本。

   * 在应用程序&#x200B;**[!UICONTROL 内的]**&#x200B;位置或路径中，指定用户应打开收件箱的屏幕、路由或容器。

1. 提交更改。

现在，您可以在创建收件箱体验时选择配置。

➡️ [按照此页面中详述的步骤操作](inbox-create.md)
