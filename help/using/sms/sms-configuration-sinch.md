---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Sinch 提供程序
description: 了解如何使用Sinch配置您的环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 4%

---

# 配置 Sinch 提供程序 {#sms-configuration-sinch}

在将Sinch提供程序与Journey Optimizer结合使用时，您可以找到两个不同的选项：

* **短信配置**：设置您的Sinch API凭据以无缝发送SMS消息。

* **MMS配置**：对于多媒体消息(MMS)，请配置Sinch MMS API凭据。 请注意，跟踪和响应入站消息由短信配置处理。 MMS设置仅用于MMS消息的出站投放。

## Sinch API凭据{#create-api}

要配置您的Sinch提供商以使用Journey Optimizer发送短信消息和彩信，请执行以下步骤：

1. 在左边栏中，浏览 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 并选择 **[!UICONTROL API凭据]** 菜单。 单击 **[!UICONTROL 创建新的API凭据]** 按钮。

1. 配置您的SMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**：Sinch。

   * **[!UICONTROL 名称]**：选择API凭据的名称。

   * **[!UICONTROL 服务ID]** 和 **[!UICONTROL api令牌]**：访问API页面，您可以在SMS选项卡下找到凭据。 了解详情，请参阅 [Sinch文档](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL 选择加入关键词]**：输入将自动触发您的请求的默认或自定义关键词 **[!UICONTROL 选择加入消息]**. 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择加入消息]**：输入将作为您的自动发送的自定义响应 **[!UICONTROL 选择加入消息]**.

   * **[!UICONTROL 选择退出关键词]**：输入将自动触发您的请求的默认或自定义关键词 **[!UICONTROL 选择退出消息]**. 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择退出消息]**：输入将作为您的自动发送的自定义响应 **[!UICONTROL 选择退出消息]**.

   * **[!UICONTROL 帮助关键字]**：输入将自动触发您的请求的默认或自定义关键词 **帮助消息**. 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 帮助消息]**：输入将作为您的自动发送的自定义响应 **帮助消息**.

   * **[!UICONTROL 双重选择加入关键词]**：输入触发双重选择加入流程的关键字。 如果用户配置文件不存在，则会在确认成功时创建该配置文件。对于多个关键字，请使用逗号分隔的值。 [了解有关短信双重选择加入的更多信息](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL 双重选择加入消息]**：输入为响应双重选择加入确认而自动发送的自定义响应。

1. 单击 **[!UICONTROL 提交]** 完成API凭据配置时。

创建和配置API凭据后，现在需要为SMS消息创建渠道平面。 [了解详情](sms-configuration-surface.md)

## Sinch MMS API凭据 {#sinch-mms}

>[!IMPORTANT]
>
> 除了MMS设置之外，您还需要创建专门用于跟踪入站消息和管理同意请求的Sinch API凭据。

要配置Sinch MMS以使用Journey Optimizer发送MMS，请执行以下步骤：

1. 在左边栏中，浏览 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 并选择 **[!UICONTROL API凭据]** 菜单。 单击 **[!UICONTROL 创建新的API凭据]** 按钮。

1. 配置您的MMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**：Sinch MMS.

   * **[!UICONTROL 名称]**：选择API凭据的名称。

   * **[!UICONTROL 项目编号]**， **[!UICONTROL 应用程序ID]** 和 **[!UICONTROL api令牌]**：请按照以下步骤收集MMS API凭据。

      * 对象 **[!UICONTROL 项目编号]** 和 **[!UICONTROL 应用程序ID]**：访问 [对话API概述](https://dashboard.sinch.com/convapi/overview) Sinch项目的URL页面。
      * 对象 **[!UICONTROL api令牌]**：获取 [访问密钥](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) 为您的Sinch项目生成 **Base64 API令牌** 从您的Sinch项目中移除 **访问密钥**.

   * **[!UICONTROL 服务计划ID]** 和 **[!UICONTROL SMS API令牌]**：您的 **[!UICONTROL 服务计划ID]** 和 **[!UICONTROL SMS API令牌]** 位于API页面的SMS选项卡上。

1. 单击 **[!UICONTROL 提交]** 完成API凭据配置时。

创建和配置API凭据后，现在需要为MMS消息创建渠道平面。 [了解详情](sms-configuration-surface.md)
