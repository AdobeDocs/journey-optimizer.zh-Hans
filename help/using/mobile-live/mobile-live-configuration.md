---
solution: Journey Optimizer
product: journey optimizer
title: 配置实时活动渠道
description: 了解如何配置环境以使用Journey Optimizer发送实时活动
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 2%

---

# 实时活动配置入门 {#mobile-live-config}

>[!BEGINSHADEBOX]

* [实时活动入门](get-started-mobile-live.md)
* **[实时活动配置](mobile-live-configuration.md)**
* [实时活动与Adobe Experience Platform Mobile SDK集成](mobile-live-configuration-sdk.md)
* [创建实时活动](create-mobile-live.md)
* [常见问题解答](mobile-live-faq.md)
* [实时活动营销活动报告](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

在发送实时活动之前，必须配置Adobe Journey Optimizer环境。 要执行此操作，请执行以下操作：

## 步骤1：在Journey Optimizer中添加应用程序推送凭据（可选）{#push-credentials-launch}

需要移动设备应用程序推送凭据注册，才能授权Adobe代表您发送推送通知。

如果推送凭据已配置，则步骤1是可选的，因为这些凭据可为Live Activity渠道配置重复使用。 如果未定义凭据，则必须为应用程序创建新的推送凭据。 请参阅下面详述的步骤：

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 推送设置]** > **[!UICONTROL 推送凭据]**&#x200B;菜单。

1. 单击&#x200B;**[!UICONTROL 创建推送凭据]**。

   ![](assets/credential-1.png)

1. 从&#x200B;**[!UICONTROL 平台]**&#x200B;下拉列表中，选择操作系统：

1. 输入移动设备应用程序&#x200B;**[!UICONTROL 应用程序ID]**。

   ![](assets/credential-2.png)

1. 启用&#x200B;**[!UICONTROL 应用到所有沙盒]**&#x200B;选项以使这些推送凭据在所有沙盒中可用。 如果特定沙盒对于同一平台和应用程序ID对拥有自己的凭据，则这些特定于沙盒的凭据将优先。

1. 已打开&#x200B;**[!UICONTROL 手动输入推送凭据]**&#x200B;按钮以添加凭据。

1. 拖放您的.p8 Apple推送通知身份验证密钥文件。 此密钥可从&#x200B;**证书**、**标识符**&#x200B;和&#x200B;**配置文件**&#x200B;页面获取。

1. 提供&#x200B;**密钥ID**。 这是在创建p8身份验证密钥期间分配的10字符串。 可在&#x200B;**证书**、**标识符**&#x200B;和&#x200B;**配置文件**&#x200B;页面中的&#x200B;**密钥**&#x200B;选项卡下找到它。

1. 提供&#x200B;**团队ID**。 这是一个字符串值，可以在“成员资格”选项卡下找到。

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以创建您的应用程序配置。

## 第2步：创建您的实时活动配置 {#config-live-activity}

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**。 单击&#x200B;**[!UICONTROL 创建渠道配置]**&#x200B;按钮。

   ![](assets/config-1.png)

1. 输入配置的名称和描述（可选），然后选择WhatsApp渠道。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线 `_`、点 `.` 和连字符 `-` 符号。

1. 选择&#x200B;**[!DNL Live activity]**&#x200B;作为您的渠道。

   ![](assets/config-2.png)

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 了解详情

1. 选择iOS作为您的&#x200B;**[!UICONTROL 平台]**。

1. 从下拉列表中选择与上面配置的&#x200B;**[!UICONTROL 推送凭据]**&#x200B;相同的[应用程序ID](#push-credentials-launch)，或者选择现有的应用程序ID。

   ![](assets/config-3.png)

1. 配置所有参数后，单击&#x200B;**[!UICONTROL 提交]**&#x200B;以确认。 您还可以将渠道配置另存为草稿，并稍后恢复其配置。

1. 创建渠道配置后，它将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。

   >[!NOTE]
   >
   >如果检查不成功，请在[本节](../configuration/channel-surfaces.md)中进一步了解可能的失败原因。

1. 检查成功后，通道配置将获得&#x200B;**[!UICONTROL 活动]**&#x200B;状态。 它随时可用于投放消息。

您现在可以开始与Adobe Experience Platform Mobile SDK集成，以在锁屏界面和Dynamic Island上启用实时动态更新。

➡️ [了解有关Adobe Experience Platform Mobile SDK集成的更多信息](mobile-live-configuration-sdk.md)
