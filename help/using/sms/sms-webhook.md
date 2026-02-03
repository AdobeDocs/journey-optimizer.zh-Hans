---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信Webhook
description: 了解如何配置Webhook以捕获入站响应，用于管理选择启用和选择禁用同意
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 0%

---

# 创建 Webhook {#webhook}

>[!BEGINSHADEBOX]

如果未提供选择加入或选择退出关键词，则使用标准同意消息尊重用户隐私。 添加自定义关键字会自动覆盖默认值。

**默认关键字：**

* **选择加入**：订阅，是，不停止，开始，继续，继续，开始
* **选择退出**：停止、退出、取消、结束、取消订阅、否
* **帮助**：帮助

>[!ENDSHADEBOX]

成功创建API凭据后，您现在可以配置Webhook以捕获入站响应，用于管理选择加入和选择退出同意，并接收投放报表，包括可用的读取回执。

在设置webhook时，您可以根据要捕获的数据类型定义其用途：

* **[!UICONTROL 入站]**：如果要捕获同意响应（如选择加入或选择退出），并收集用户首选项，请使用此选项。

* **[!UICONTROL 反馈]**：选择此选项可跟踪投放和参与事件（包括读取回执和用户交互），以支持报告和分析。

根据您的短信提供商浏览以下选项卡：

>[!BEGINTABS]

>[!TAB 自定义]

1. 在左边栏中，导航到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**，选择&#x200B;**[!UICONTROL 短信设置]**&#x200B;下的&#x200B;**[!UICONTROL 短信Webhook]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建Webhook]**&#x200B;按钮。

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 配置Webhook设置，如下所述：

   * **[!UICONTROL 名称]**：输入Webhook的名称。

   * **[!UICONTROL 选择SMS供应商]**：自定义。

   * **[!UICONTROL 类型]**：入站。

   * **[!UICONTROL API凭据]**：从下拉列表中选择[之前配置的API凭据](sms-configuration-custom.md#api-credential)。

   * **[!UICONTROL 发件人电话号码&#x200B;]**：输入&#x200B;要用于通信的发件人电话号码。

     ![](assets/webhook-inbound.png){zoomable="yes"}

1. 单击![](assets/do-not-localize/Smock_Add_18_N.svg)以添加您的关键字类别，然后根据短信提供商进行配置：

   * **[!UICONTROL 入站关键词类别]**：选择您的关键词类别&#x200B;**[!UICONTROL 选择加入]**、**[!UICONTROL 选择退出]**、**[!UICONTROL 双重选择加入]**、**[!UICONTROL 帮助]**&#x200B;或&#x200B;**[!UICONTROL 自定义]**。

   * **[!UICONTROL 输入关键字]**：输入将自动触发消息的默认或自定义关键字。 单击![](assets/do-not-localize/Smock_Add_18_N.svg)可添加多个关键字。

     对于&#x200B;**[!UICONTROL 自定义关键字]**，请使用与同意无关的关键字在历程中执行基于批次的操作。

   * **[!UICONTROL 回复消息]**：从下拉列表中选择自动发送的自定义响应。

   * **[!UICONTROL 模糊选择退出]**：启用此选项，以便在检测到接近匹配的选择退出关键字时发送自动回复。

   ![](assets/sms_byo_6.png){zoomable="yes"}

1. 输入当入站消息与任何配置的关键字或类别不匹配时自动发送的&#x200B;**[!UICONTROL 默认回复消息]**。

1. 单击&#x200B;**[!UICONTROL 查看有效负载编辑器]**&#x200B;以验证和自定义您的请求有效负载。

   您可以使用配置文件属性动态个性化有效负载，并通过内置帮助程序功能确保发送准确的数据用于处理和生成响应。

1. 完成Webhook配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 要创建&#x200B;**[!UICONTROL 反馈]** webhook，请执行与上述步骤相同的步骤，选择&#x200B;**[!UICONTROL 反馈]**&#x200B;作为您的webhook **[!UICONTROL 类型]**。

1. 从&#x200B;**[!UICONTROL Webhooks]**&#x200B;菜单中，可以编辑或删除现有Webhook，或访问和复制&#x200B;**[!UICONTROL Webhook URL]**&#x200B;以便与您的SMS提供商集成。

   ![](assets/sms_byo_7.png){zoomable="yes"}

在创建和配置Webhook的设置后，您现在需要为短信消息创建[渠道配置](sms-configuration-surface.md)。

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。

>[!TAB Infobip]

1. 在左边栏中，导航到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**，选择&#x200B;**[!UICONTROL 短信设置]**&#x200B;下的&#x200B;**[!UICONTROL 短信Webhook]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建Webhook]**&#x200B;按钮。

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 配置Webhook设置，如下所述：

   * **[!UICONTROL 名称]**：输入Webhook的名称。

   * **[!UICONTROL 选择SMS供应商]**： Infobip。

   * **[!UICONTROL 类型]**：入站。

   * **[!UICONTROL API凭据]**：从下拉列表中选择[之前配置的API凭据](sms-configuration-infobip.md#api-credential)。

   * **[!UICONTROL 发件人电话号码&#x200B;]**：输入&#x200B;要用于通信的发件人电话号码。

     ![](assets/webhook-infobip-1.png){zoomable="yes"}

1. 单击![](assets/do-not-localize/Smock_Add_18_N.svg)以添加您的关键字类别，然后根据短信提供商进行配置：

   * **[!UICONTROL 入站关键词类别]**：选择您的关键词类别&#x200B;**[!UICONTROL 选择加入]**、**[!UICONTROL 选择退出]**、**[!UICONTROL 双重选择加入]**、**[!UICONTROL 帮助]**&#x200B;或&#x200B;**[!UICONTROL 自定义]**。

   * **[!UICONTROL 输入关键字]**：输入将自动触发消息的默认或自定义关键字。 单击![](assets/do-not-localize/Smock_Add_18_N.svg)可添加多个关键字。

     对于&#x200B;**[!UICONTROL 自定义关键字]**，请使用与同意无关的关键字在历程中执行基于批次的操作。

   * **[!UICONTROL 回复消息]**：从下拉列表中选择自动发送的自定义响应。

   * **[!UICONTROL 模糊选择退出]**：启用此选项，以便在检测到接近匹配的选择退出关键字时发送自动回复。

   ![](assets/webhook-infobip-2.png){zoomable="yes"}

1. 输入当入站消息与任何配置的关键字或类别不匹配时自动发送的&#x200B;**[!UICONTROL 默认回复消息]**。

1. 完成Webhook配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 要创建&#x200B;**[!UICONTROL 反馈]** webhook，请执行与上述步骤相同的步骤，选择&#x200B;**[!UICONTROL 反馈]**&#x200B;作为您的webhook **[!UICONTROL 类型]**。

1. 从&#x200B;**[!UICONTROL Webhooks]**&#x200B;菜单中，可以编辑或删除现有Webhook，或访问和复制&#x200B;**[!UICONTROL Webhook URL]**&#x200B;以便与您的SMS提供商集成。

   ![](assets/sms_byo_7.png){zoomable="yes"}

在为Webhook创建和配置入站设置后，您现在需要为短信创建[渠道配置](sms-configuration-surface.md)。

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。

>[!TAB Sinch]

1. 在左边栏中，导航到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**，选择&#x200B;**[!UICONTROL 短信设置]**&#x200B;下的&#x200B;**[!UICONTROL 短信Webhook]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建Webhook]**&#x200B;按钮。

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 配置Webhook设置，如下所述：

   * **[!UICONTROL 名称]**：输入Webhook的名称。

   * **[!UICONTROL 选择SMS供应商]**： Sinch。

   * **[!UICONTROL 类型]**：入站。

   * **[!UICONTROL API凭据]**：从下拉列表中选择[之前配置的API凭据](sms-configuration-sinch.md#create-api)。

   * **[!UICONTROL 发件人电话号码&#x200B;]**：输入&#x200B;要用于通信的发件人电话号码。

     ![](assets/webhook-sinch-1.png){zoomable="yes"}

1. 单击![](assets/do-not-localize/Smock_Add_18_N.svg)以添加您的关键字类别，然后根据短信提供商进行配置：

   * **[!UICONTROL 入站关键词类别]**：选择您的关键词类别&#x200B;**[!UICONTROL 选择加入]**、**[!UICONTROL 选择退出]**、**[!UICONTROL 双重选择加入]**、**[!UICONTROL 帮助]**&#x200B;或&#x200B;**[!UICONTROL 自定义]**。

   * **[!UICONTROL 输入关键字]**：输入将自动触发消息的默认或自定义关键字。 单击![](assets/do-not-localize/Smock_Add_18_N.svg)可添加多个关键字。

     对于&#x200B;**[!UICONTROL 自定义关键字]**，请使用与同意无关的关键字在历程中执行基于批次的操作。

   * **[!UICONTROL 回复消息]**：从下拉列表中选择自动发送的自定义响应。

   * **[!UICONTROL 模糊选择退出]**：启用此选项，以便在检测到接近匹配的选择退出关键字时发送自动回复。

   ![](assets/webhook-sinch-2.png){zoomable="yes"}

1. 输入当入站消息与任何配置的关键字或类别不匹配时自动发送的&#x200B;**[!UICONTROL 默认回复消息]**。

1. 完成Webhook配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL Webhooks]**&#x200B;菜单中，单击![bin图标](assets/do-not-localize/Smock_Delete_18_N.svg)以删除您的Webhook。

1. 要修改现有配置，请找到所需的Webhook，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要的更改。

1. 从您以前提交的&#x200B;**[!UICONTROL Webhook]**&#x200B;访问和复制新的&#x200B;**[!UICONTROL Webhook URL]**。

   ![](assets/sms_byo_7.png){zoomable="yes"}

在为Webhook创建和配置入站设置后，您现在需要为短信创建[渠道配置](sms-configuration-surface.md)。

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。

>[!TAB Twilio]

1. 在左边栏中，导航到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**，选择&#x200B;**[!UICONTROL 短信设置]**&#x200B;下的&#x200B;**[!UICONTROL 短信Webhook]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建Webhook]**&#x200B;按钮。

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 配置Webhook设置，如下所述：

   * **[!UICONTROL 名称]**：输入Webhook的名称。

   * **[!UICONTROL 选择SMS供应商]**： Twilio。

   * **[!UICONTROL 类型]**：入站。

   * **[!UICONTROL API凭据]**：从下拉列表中选择[之前配置的API凭据](sms-configuration-twilio.md#create-api)。

   * **[!UICONTROL 发件人电话号码&#x200B;]**：输入&#x200B;要用于通信的发件人电话号码。

1. 单击![](assets/do-not-localize/Smock_Add_18_N.svg)以添加您的关键字类别，然后根据短信提供商进行配置：

   * **[!UICONTROL 入站关键词类别]**：选择您的关键词类别&#x200B;**[!UICONTROL 选择加入]**、**[!UICONTROL 选择退出]**、**[!UICONTROL 双重选择加入]**、**[!UICONTROL 帮助]**&#x200B;或&#x200B;**[!UICONTROL 自定义]**。

   * **[!UICONTROL 输入关键字]**：输入将自动触发消息的默认或自定义关键字。 单击![](assets/do-not-localize/Smock_Add_18_N.svg)可添加多个关键字。

     对于&#x200B;**[!UICONTROL 自定义关键字]**，请使用与同意无关的关键字在历程中执行基于批次的操作。

   * **[!UICONTROL 回复消息]**：从下拉列表中选择自动发送的自定义响应。

   * **[!UICONTROL 模糊选择退出]**：启用此选项，以便在检测到接近匹配的选择退出关键字时发送自动回复。

1. 输入当入站消息与任何配置的关键字或类别不匹配时自动发送的&#x200B;**[!UICONTROL 默认回复消息]**。

1. 完成Webhook配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL Webhooks]**&#x200B;菜单中，单击![bin图标](assets/do-not-localize/Smock_Delete_18_N.svg)以删除您的Webhook。

1. 要修改现有配置，请找到所需的Webhook，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要的更改。

1. 从您以前提交的&#x200B;**[!UICONTROL Webhook]**&#x200B;访问和复制新的&#x200B;**[!UICONTROL Webhook URL]**。

在为Webhook创建和配置入站设置后，您现在需要为短信创建[渠道配置](sms-configuration-surface.md)。

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。


>[!ENDTABS]


## 操作说明视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

