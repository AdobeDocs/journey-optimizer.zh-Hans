---
solution: Journey Optimizer
product: journey optimizer
title: 配置Infobip提供程序
description: 了解如何使用Journey Optimizer和Infobip配置您的环境以发送短信和彩信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 4%

---

# 配置Infobip提供程序 {#sms-configuration-infobip}

要使用Journey Optimizer配置Infobip，请执行以下步骤：

1. 在左边栏中，浏览 **[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]** 并选择 **[!UICONTROL API凭据]** 菜单。 单击 **[!UICONTROL 创建新的API凭据]** 按钮。

   ![](assets/sms_6.png)

1. 配置API凭据，如下所述。

   * **[!UICONTROL 名称]**：选择API凭据的名称。

   * **[!UICONTROL API基本URL]** 和 **[!UICONTROL API密钥]**：访问您的Web界面主页或API密钥管理页面以查找您的凭据。 了解详情，请参阅 [Infobip文档](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL 选择加入关键词]**：输入将自动触发您的请求的默认或自定义关键词 **[!UICONTROL 选择加入消息]**. 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择加入消息]**：输入将作为您的自动发送的自定义响应 **[!UICONTROL 选择加入消息]**.

   * **[!UICONTROL 选择退出关键词]**：输入默认或自动触发的关键字 **[!UICONTROL 选择退出消息]**. 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择退出消息]**：输入将作为您的自动发送的自定义响应 **[!UICONTROL 选择退出消息]**.

   * **[!UICONTROL 帮助关键字]**：输入将自动触发您的请求的默认或自定义关键词 **帮助消息**. 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 帮助消息]**：输入将作为您的自动发送的自定义响应 **帮助消息**.

   * **[!UICONTROL 双重选择加入关键词]**：输入触发双重选择加入流程的关键字。 如果用户配置文件不存在，则会在确认成功时创建该配置文件。对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 双重选择加入消息]**：输入为响应双重选择加入确认而自动发送的自定义响应。

   * **[!UICONTROL 主体实体ID]**：输入分配的DLT主体实体ID。

   * **[!UICONTROL 内容模板Id]**：输入注册的DLT内容模板ID。

   * **[!UICONTROL 有效期]**：输入以小时为单位的消息有效期。 如果在此时间范围内无法发送消息，系统将再次尝试重新发送消息。 默认有效期设置为48小时。

   * **[!UICONTROL 回调数据]**：输入将在通知URL上发送的其他客户端数据。

1. 单击 **[!UICONTROL 提交]** 完成API凭据配置时。

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道平面。 [了解详情](sms-configuration-surface.md)
