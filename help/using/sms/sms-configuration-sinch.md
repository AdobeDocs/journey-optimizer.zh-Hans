---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Sinch 提供程序
description: 了解如何使用Sinch配置您的环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 2%

---

# 配置 Sinch 提供程序 {#sms-configuration-sinch}

在将Sinch提供程序与Journey Optimizer结合使用时，您可以找到三个不同的选项：

* **SMS配置**：设置您的Sinch API凭据以无缝发送SMS消息。

* **MMS配置**：对于多媒体消息(MMS)，请配置Sinch MMS API凭据。 请注意，跟踪和响应入站消息由短信配置处理。 MMS设置仅用于MMS消息的出站投放。

* **RCS配置**：设置您的Sinch API凭据以无缝发送RCS消息。

## 配置短信的API凭据{#create-api}

>[!BEGINSHADEBOX]

如果未提供选择加入或选择退出关键词，则使用标准同意消息尊重用户隐私。 添加自定义关键字会自动覆盖默认值。

**默认关键字：**

* **选择加入**：订阅，是，不停止，开始，继续，继续，开始
* **选择退出**：停止、退出、取消、结束、取消订阅、否
* **帮助**：帮助

>[!ENDSHADEBOX]

要配置您的Sinch提供商以使用Journey Optimizer发送短信消息和彩信，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** `>` **[!UICONTROL SMS设置]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的SMS API凭据，如下所述：

+++ 用于配置的短信凭据列表

   | 配置字段 | 描述 |
   |---|---|    
   | SMS供应商 | Sinch |
   | 名称 | 选择API凭据的名称。 |
   | 服务ID和API令牌 | 访问API页面，您可以在SMS选项卡下找到凭据。 请参阅[Sinch文档](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}以了解详情。 |
   | 选择加入关键词 | 输入将自动触发选择加入消息的默认或自定义关键词。 对于多个关键字，请使用逗号分隔的值。 |
   | 选择加入消息 | 输入作为选择加入消息自动发送的自定义响应。 |
   | 选择退出关键词 | 输入将自动触发选择退出消息的默认或自定义关键词。 对于多个关键字，请使用逗号分隔的值。 |
   | 选择退出消息 | 输入作为选择退出消息自动发送的自定义响应。 |
   | 帮助关键字 | 输入将自动触发&#x200B;**帮助消息**&#x200B;的默认关键字或自定义关键字。 对于多个关键字，请使用逗号分隔的值。 |
   | 帮助消息 | 输入作为&#x200B;**帮助消息**&#x200B;自动发送的自定义响应。 |
   | 双重选择加入关键词 | 输入触发双重选择加入流程的关键字。 如果用户轮廓不存在，则会在确认成功时创建该轮廓。对于多个关键字，请使用逗号分隔的值。 [了解有关短信双重选择加入的更多信息](https://video.tv.adobe.com/v/3427129/?learn=on)。 |
   | 双重选择加入消息 | 输入为响应双重选择加入确认而自动发送的自定义响应。 |
   | 入站编号 | 添加唯一的入站编号或短代码。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号或短代码。 |
   | 自定义入站关键词 | 为特定操作定义唯一的关键字，例如DISCOUNT、OFFERS、ENROLL。 这些关键字将作为属性捕获并存储在配置文件中，使您能够触发历程中的流区段鉴别并提供自定义响应或操作。 |
   | 默认入站回复消息 | 输入在最终用户发送与定义的任何关键字都不匹配的入站SMS时发送的默认回复。 |
   | 覆盖URL | 输入您的自定义URL以替换SMS投放报告、反馈数据、入站消息或事件通知的默认端点。 Sinch会将所有相关更新发送到此URL，而不是预定义的更新。 |

+++

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

创建和配置API凭据后，现在需要为SMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)

## 为MMS配置API凭据{#sinch-mms}

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

## 为RCS配置API凭据

<!--![](assets/do-not-localize/rcs-sms.png)-->

Journey Optimizer通过Sinch支持RCS（富通信服务）消息传递，允许使用经过验证的企业个人资料以及品牌元素（如徽标和发件人名称）发送基本消息。

请注意，当用户档案的设备不支持RCS或暂时无法通过RCS访问时，消息会自动回退到短信。

使用Sinch配置RCS：

1. **设置您的品牌RCS代理**

   请联系您的Adobe代表以设置品牌RCS代理。 [了解有关品牌RCS代理的更多信息](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **设置您的[Sinch API凭据](#create-api)**

   RCS代理获得批准后，您需要设置Sinch API凭据，其中包括访问密钥、密钥和服务计划ID。 Journey Optimizer将使用这些凭据通过Sinch的平台进行身份验证并发送消息。

1. **为您的RCS消息创建[通道配置](sms-configuration-surface.md)**

   通过链接您的Sinch凭据并定义消息传递参数，在Journey Optimizer中配置渠道平面。 此设置允许您从Journey Optimizer撰写和发送RCS消息。

