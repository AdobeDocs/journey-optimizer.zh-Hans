---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Infobip 提供程序
description: 了解如何使用Journey Optimizer和Infobip配置您的环境以发送短信和彩信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 604af3a0ac9febb62f2e2b1705e2751b2c476e04
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 3%

---

# 配置 Infobip 提供程序 {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

如果未提供选择加入或选择退出关键词，则使用标准同意消息尊重用户隐私。 添加自定义关键字会自动覆盖默认值。

**默认关键字：**

* **选择加入**：订阅，是，不停止，开始，继续，继续，开始
* **选择退出**：停止、退出、取消、结束、取消订阅、否
* **帮助**：帮助

>[!ENDSHADEBOX]

## 配置短信的API凭据

要使用Journey Optimizer配置Infobip，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的SMS API凭据，如下所述：

+++ 用于配置的短信凭据列表

   | 配置字段 | 描述 |
   |---|---|    
   | SMS供应商 | Infobip |
   | 名称 | 选择API凭据的名称。 |
   | API基本URL和API密钥 | 访问您的Web界面主页或API密钥管理页面以查找您的凭据。 请参阅[Infobip文档](https://www.infobip.com/docs/api){target="_blank"}以了解详情 |
   | 选择加入关键词 | 输入将自动触发选择加入消息的默认或自定义关键词。 对于多个关键字，请使用逗号分隔的值。 |
   | 选择加入消息 | 输入作为选择加入消息自动发送的自定义响应。 |
   | 选择退出关键词 | 输入将自动触发选择退出消息的默认或自定义关键词。 对于多个关键字，请使用逗号分隔的值。 |
   | 选择退出消息 | 输入作为选择退出消息自动发送的自定义响应。 |
   | 帮助关键字 | 输入将自动触发&#x200B;**帮助消息**&#x200B;的默认关键字或自定义关键字。 对于多个关键字，请使用逗号分隔的值。 |
   | 帮助消息 | 输入作为&#x200B;**帮助消息**&#x200B;自动发送的自定义响应。 |
   | 双重选择加入关键词 | 输入触发双重选择加入流程的关键字。 如果用户轮廓不存在，则会在确认成功时创建该轮廓。对于多个关键字，请使用逗号分隔的值。 [了解有关短信双重选择加入的更多信息](https://video.tv.adobe.com/v/3427129/?learn=on)。 |
   | 双重选择加入消息 | 输入为响应双重选择加入确认而自动发送的自定义响应。 |
   | 主体实体ID | 输入分配的DLT主体实体ID。 |
   | 内容模板Id | 输入注册的DLT内容模板ID。 |
   | 有效期 | 输入以小时为单位的消息有效期。 如果在此时间范围内无法发送消息，系统将再次尝试重新发送消息。 默认有效期设置为48小时。 |
   | 回调数据 | 输入将在通知URL上发送的其他客户端数据。 |
   | 入站编号 | 添加您的独特入站编号。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号。 |
   | 自定义入站关键词 | 为特定操作定义唯一的关键字，例如DISCOUNT、OFFERS、ENROLL。 这些关键字将作为属性捕获并存储在配置文件中，使您能够触发历程中的流区段鉴别并提供自定义响应或操作。 |
   | 默认入站回复消息 | 输入在最终用户发送与定义的任何关键字都不匹配的入站SMS时发送的默认回复。 |

+++

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)

## 为RCS配置API凭据

Adobe Journey Optimizer使用[自定义SMS提供程序](sms-configuration-custom.md)功能，通过Infobip支持RCS消息传递。 这允许通过经验证的业务配置文件来交付丰富的交互式消息，并整合了诸如轮播、按钮和多媒体内容之类的元素。

➡️ [在Infobip文档中了解Infobip如何支持RCS](https://www.infobip.com/docs/api/channels/rcs)

要使用Infobip启用RCS消息传递，必须通过自定义SMS提供商配置新的API凭据。 现有Infobip SMS凭据不兼容，因为RCS需要不同的有效负载格式。

要使用Infobip配置RCS，请执行以下操作：

1. **通过Infobip注册您的RCS业务**

   首先在Infobip平台中完成RCS入门和注册流程。 这包括设置您的RCS发件人配置文件并确保您的帐户已启用RCS。 请参阅[Infobip文档](https://www.infobip.com/docs/rcs/get-started)以了解详情

1. **创建SMS Webhook**

   [在Journey Optimizer中配置自定义短信webhook](sms-configuration-custom.md#webhook)。 此webhook将负责处理来自Infobip平台的投放接收、入站RCS消息和状态更新。

1. **使用自定义作为SMS供应商创建API凭据**

   [在Journey Optimizer中创建新的API凭据](sms-configuration-custom.md#api-credential)，选择“自定义”作为SMS提供商。 使用适当的RCS端点身份验证方法、基本URL和标头。

创建和配置API凭据后，现在需要为RCS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)
