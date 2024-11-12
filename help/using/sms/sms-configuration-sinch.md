---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Sinch 提供程序
description: 了解如何使用Sinch配置您的环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: a196a27fd22a03915838ab4a9bb6139f85242f6b
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 3%

---

# 配置 Sinch 提供程序 {#sms-configuration-sinch}

在将Sinch提供程序与Journey Optimizer结合使用时，您可以找到两个不同的选项：

* **SMS配置**：设置您的Sinch API凭据以无缝发送SMS消息。

* **MMS配置**：对于多媒体消息(MMS)，请配置Sinch MMS API凭据。 请注意，跟踪和响应入站消息由短信配置处理。 MMS设置仅用于MMS消息的出站投放。

## Sinch API凭据{#create-api}

要配置您的Sinch提供商以使用Journey Optimizer发送短信消息和彩信，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** `>` **[!UICONTROL SMS设置]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的SMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**： Sinch。

   * **[!UICONTROL 名称]**：为您的API凭据选择一个名称。

   * **[!UICONTROL 服务ID]**&#x200B;和&#x200B;**[!UICONTROL API令牌]**：访问API页面，您可以在SMS选项卡下找到您的凭据。 请参阅[Sinch文档](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}以了解详情。

   * **[!UICONTROL 选择加入关键字]**：输入将自动触发您的&#x200B;**[!UICONTROL 选择加入消息]**&#x200B;的默认或自定义关键字。 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择加入消息]**：输入作为&#x200B;**[!UICONTROL 选择加入消息]**&#x200B;自动发送的自定义响应。

   * **[!UICONTROL 选择退出关键字]**：输入将自动触发您的&#x200B;**[!UICONTROL 选择退出消息]**&#x200B;的默认或自定义关键字。 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择退出消息]**：输入作为&#x200B;**[!UICONTROL 选择退出消息]**&#x200B;自动发送的自定义响应。

   * **[!UICONTROL 帮助关键字]**：输入将自动触发您的&#x200B;**帮助消息**&#x200B;的默认或自定义关键字。 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 帮助消息]**：输入作为&#x200B;**帮助消息**&#x200B;自动发送的自定义响应。

   * **[!UICONTROL 双重选择加入关键字]**：输入触发双重选择加入流程的关键字。 如果用户配置文件不存在，则会在确认成功时创建该配置文件。对于多个关键字，请使用逗号分隔的值。 [了解有关短信双重选择加入的更多信息](https://video.tv.adobe.com/v/3427129/?learn=on)。

   * **[!UICONTROL 双重选择加入消息]**：输入为响应双重选择加入确认而自动发送的自定义响应。

   * **[!UICONTROL 入站号码]**：添加您的唯一入站号码或短代码。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号或短代码。

   * **[!UICONTROL 自定义入站关键字]**：为特定操作（例如，折扣、优惠、注册）定义唯一关键字。 这些关键字将作为属性捕获并存储在配置文件中，使您能够触发历程中的流区段鉴别并提供自定义响应或操作。

   * **[!UICONTROL 默认入站回复消息]**：输入在最终用户发送与定义的任何关键字都不匹配的入站SMS时发送的默认回复。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

创建和配置API凭据后，现在需要为SMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)

## Sinch MMS API凭据 {#sinch-mms}

>[!IMPORTANT]
>
> 除了MMS设置之外，您还需要创建专门用于跟踪入站消息和管理同意请求的Sinch API凭据。

要配置Sinch MMS以使用Journey Optimizer发送MMS，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** `>` **[!UICONTROL SMS设置]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的MMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**： Sinch MMS。

   * **[!UICONTROL 名称]**：为您的API凭据选择一个名称。

   * **[!UICONTROL 项目ID]**、**[!UICONTROL 应用程序ID]**&#x200B;和&#x200B;**[!UICONTROL API令牌]**：请按照以下步骤收集您的MMS API凭据。

      * 对于&#x200B;**[!UICONTROL 项目ID]**&#x200B;和&#x200B;**[!UICONTROL 应用程序ID]**：访问Sinch仪表板上Sinch项目的[对话API概述](https://dashboard.sinch.com/convapi/overview)页面。
      * 对于&#x200B;**[!UICONTROL API令牌]**：获取Sinch项目的[访问密钥](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638)，并生成Sinch项目&#x200B;**访问密钥**&#x200B;中的&#x200B;**Base64 API令牌**。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

创建和配置API凭据后，现在需要为MMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)
