---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Infobip 提供程序
description: 了解如何使用Journey Optimizer和Infobip配置您的环境以发送短信和彩信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 4%

---

# 配置 Infobip 提供程序 {#sms-configuration-infobip}

要使用Journey Optimizer配置Infobip，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置API凭据，如下所述。

   * **[!UICONTROL SMS供应商]**： Infobip。

   * **[!UICONTROL 名称]**：为您的API凭据选择一个名称。

   * **[!UICONTROL API基本URL]**&#x200B;和&#x200B;**[!UICONTROL API密钥]**：访问Web界面主页或API密钥管理页以查找您的凭据。 请参阅[Infobip文档](https://www.infobip.com/docs/api){target="_blank"}以了解详情。

   * **[!UICONTROL 选择加入关键字]**：输入将自动触发您的&#x200B;**[!UICONTROL 选择加入消息]**&#x200B;的默认或自定义关键字。 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择加入消息]**：输入作为&#x200B;**[!UICONTROL 选择加入消息]**&#x200B;自动发送的自定义响应。

   * **[!UICONTROL 选择退出关键字]**：输入将自动触发您的&#x200B;**[!UICONTROL 选择退出消息]**&#x200B;的默认关键字或关键字。 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 选择退出消息]**：输入作为&#x200B;**[!UICONTROL 选择退出消息]**&#x200B;自动发送的自定义响应。

   * **[!UICONTROL 帮助关键字]**：输入将自动触发您的&#x200B;**帮助消息**&#x200B;的默认或自定义关键字。 对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 帮助消息]**：输入作为&#x200B;**帮助消息**&#x200B;自动发送的自定义响应。

   * **[!UICONTROL 双重选择加入关键字]**：输入触发双重选择加入流程的关键字。 如果用户配置文件不存在，则会在确认成功时创建该配置文件。对于多个关键字，请使用逗号分隔的值。

   * **[!UICONTROL 双重选择加入消息]**：输入为响应双重选择加入确认而自动发送的自定义响应。

   * **[!UICONTROL 主体实体ID]**：输入分配的DLT主体实体ID。

   * **[!UICONTROL 内容模板ID]**：输入已注册的DLT内容模板ID。

   * **[!UICONTROL 有效期]**：输入以小时为单位的消息有效期。 如果在此时间范围内无法发送消息，系统将再次尝试重新发送消息。 默认有效期设置为48小时。

   * **[!UICONTROL 回调数据]**：输入将在通知URL上发送的其他客户端数据。

   * **[!UICONTROL 入站编号]**：添加您的独特入站编号。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号。

   * **[!UICONTROL 自定义入站关键字]**：为特定操作（例如，折扣、优惠、注册）定义唯一关键字。 这些关键字将作为属性捕获并存储在配置文件中，使您能够触发历程中的流区段鉴别并提供自定义响应或操作。

   * **[!UICONTROL 默认入站回复消息]**：输入在最终用户发送与定义的任何关键字都不匹配的入站SMS时发送的默认回复。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)
