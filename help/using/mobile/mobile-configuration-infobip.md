---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Infobip 提供程序
description: 了解如何使用Journey Optimizer和Infobip配置您的环境以发送短信和彩信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
TQID: https://experienceleague.adobe.com/hkloRlDuOO-lNSezWvOcD3dtsHrhDqCJGo3cHq5pWog
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9a68782b0ca1a9a65db621209cf4f39ea5ce911d
workflow-type: tm+mt
source-wordcount: 769
ht-degree: 1%

---

# 配置 Infobip 提供程序 {#sms-configuration-infobip}

通过将Infobip与Adobe Journey Optimizer集成，您可以向个人资料发送短信，作为历程和营销活动的一部分。

要将Infobip配置为您的短信提供商，请执行以下步骤：

1. [创建API凭据](#api-credential)
1. [创建 Webhook](mobile-webhook.md)
1. [创建渠道配置](mobile-configuration-surface.md)
1. [通过短信渠道操作创建历程或营销活动](create-mobile-message.md)

## 配置短信的API凭据 {#api-credential}

要使用Journey Optimizer配置Infobip，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的SMS API凭据，如下所述：

   +++ 用于配置的短信凭据列表

   | 配置字段 | 描述 |
   |---|---|
   | SMS供应商 | Infobip |
   | 名称 | 选择API凭据的名称。 |
   | API基本URL和API密钥 | 访问您的Web界面主页或API密钥管理页面以查找您的凭据。 对于区域或备用域端点（例如`api-ny2.infobip.com`），请指定完整的基本URL并使用Infobip支持验证您的授权令牌。 </br>请参阅[Infobip文档](https://www.infobip.com/docs/api){target="_blank"}以了解详情 |
   | 主体实体ID | 输入分配的DLT主体实体ID。 |
   | 内容模板Id | 输入注册的DLT内容模板ID。 |
   | 有效期 | 输入以小时为单位的消息有效期。 如果在此时间范围内无法发送消息，系统将再次尝试重新发送消息。 默认有效期设置为48小时。 |
   | 回调数据 | 输入将在通知URL上发送的其他客户端数据。 |
   | 入站编号 | 添加您的独特入站编号。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号。 |

   +++

1. 启用&#x200B;**[!UICONTROL 模糊选择退出]**&#x200B;选项以检测类似于选择退出关键字的消息（如“CANCIL”），并在&#x200B;**[!UICONTROL 模糊自动回复]**&#x200B;字段中自定义确认回复。

   **[!UICONTROL Fuzzy Opt-out]**&#x200B;标识表示用户希望取消订阅的短信消息，即使该消息与定义的选择退出关键字不完全匹配。 它可以检测常见的选择退出短语和某些冒犯性术语，从而帮助确保您的营销活动尊重用户偏好并保持合规性。

1. 选择&#x200B;**[!UICONTROL 对入站]**&#x200B;使用自定义数据集，将此凭据的入站SMS路由到您从下拉列表选择的预创建的数据集。 [了解有关对入站关键字使用自定义数据集的更多信息](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >数据集架构必须是&#x200B;**[!UICONTROL XDM ExperienceEvent]**，并且至少包括以下字段组：
   >* Adobe CJM ExperienceEvent — 消息交互详细信息
   >* Adobe CJM ExperienceEvent — 消息执行详细信息
   >* Adobe CJM ExperienceEvent — 消息配置文件详细信息
   >
   >必须为配置文件启用架构和数据集。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

1. 单击现有API凭据中的&#x200B;**[!UICONTROL 验证SMS连接]**，通过向指定设备发送示例消息来测试和验证SMS API凭据。

1. 填写&#x200B;**数字**&#x200B;和&#x200B;**消息**&#x200B;字段，然后单击&#x200B;**[!UICONTROL 验证连接]**。

   >[!IMPORTANT]
   >
   >消息的结构必须与提供商的有效负荷格式保持一致。

   ![](assets/verify-connection.png)

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道配置。 [了解详情](mobile-configuration-surface.md)

## 为RCS配置API凭据

Adobe Journey Optimizer使用[自定义SMS提供程序](mobile-configuration-custom.md)功能，通过Infobip支持RCS消息传递。 这允许通过经验证的业务配置文件来交付丰富的交互式消息，并整合了诸如轮播、按钮和多媒体内容之类的元素。

➡️ [在Infobip文档中了解Infobip如何支持RCS](https://www.infobip.com/docs/api/channels/rcs)

要使用Infobip启用RCS消息传递，必须通过自定义SMS提供商配置新的API凭据。 现有Infobip SMS凭据不兼容，因为RCS需要不同的有效负载格式。

要使用Infobip配置RCS，请执行以下操作：

1. **通过Infobip注册您的RCS业务**

   首先在Infobip平台中完成RCS入门和注册流程。 这包括设置您的RCS发件人配置文件并确保您的帐户已启用RCS。 请参阅[Infobip文档](https://www.infobip.com/docs/rcs/get-started)以了解详情

1. **创建SMS Webhook**

   [在Journey Optimizer中配置自定义短信webhook](mobile-configuration-custom.md#webhook)。 此webhook将负责处理来自Infobip平台的投放接收、入站RCS消息和状态更新。

1. **使用自定义作为SMS供应商创建API凭据**

   [在Journey Optimizer中创建新的API凭据](mobile-configuration-custom.md#api-credential)，选择“自定义”作为SMS提供商。 使用适当的RCS端点身份验证方法、基本URL和标头。

创建和配置API凭据后，您现在需要创建[您的Webhook](mobile-webhook.md)和RCS消息的通道配置。 [了解详情](mobile-configuration-surface.md)
