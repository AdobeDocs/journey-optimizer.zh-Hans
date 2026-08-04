---
solution: Journey Optimizer
product: journey optimizer
title: 向订阅者发送消息
description: 了解如何构建历程以向列表的订阅者发送消息
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 历程，用例，消息，订阅者，列表，读取
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sDhncesYlIjsj2zjB-QmjWqP--0KDyp-5x5-UGLSjRc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 924
ht-degree: 5%

---

# 向列表的订阅者发送消息 {#send-a-message-to-the-subscribers-of-a-list}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用“同意和偏好设置详细信息”字段组构建历程，以向列表的订阅者发送消息。

>[!ENDSHADEBOX]

此用例的目的在于创建历程，以向列表的订阅者发送消息。

在此示例中，使用了[!DNL Adobe Experience Platform]中的&#x200B;**[!UICONTROL 同意和偏好设置详细信息]**&#x200B;字段组。 若要查找此字段组，请从&#x200B;**[!UICONTROL 数据管理]**&#x200B;菜单中选择&#x200B;**[!UICONTROL 架构]**。 在&#x200B;**[!UICONTROL 字段组]**&#x200B;选项卡上，在搜索字段中输入字段组的名称。

![此字段组包含订阅元素](assets/consent-and-preference-details-field-group.png)

要配置此历程，请执行以下步骤：

1. 创建以&#x200B;**[!UICONTROL 读取]**&#x200B;活动开始的历程。 在[创建您的第一个历程](journey-gs.md)中了解详情。
1. 向历程添加&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作活动。 了解如何[使用渠道操作](journey-action.md)。
1. 在&#x200B;**[!UICONTROL 电子邮件]**&#x200B;活动设置的&#x200B;**[!UICONTROL 电子邮件参数]**&#x200B;部分中，将默认电子邮件地址(`PersonalEmail.adress`)替换为列表订阅者的电子邮件地址：

   1. 单击&#x200B;**[!UICONTROL 地址]**&#x200B;字段右侧的&#x200B;**[!UICONTROL 启用参数覆盖]**&#x200B;图标，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;图标。

      ![历程流，带有针对订阅者列表定向的读取受众](assets/message-to-subscribers-uc-1.png)

   1. 在表达式编辑器中，输入用于检索订阅者电子邮件地址的表达式。 [了解详情](expression/expressionadvanced.md)。

      此示例显示一个包含映射字段引用的表达式：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在此示例中，使用以下函数：

      | 函数 | 描述 | 示例 |
      | --- | --- | --- |
      | `entry` | 根据选定的命名空间引用映射元素 | 请参阅特定订阅列表 |
      | `firstEntryKey` | 检索映射的第一个条目键 | 检索订阅者的第一个电子邮件地址 |

      在此示例中，订阅列表名为`daily-email`。 电子邮件地址在`subscribers`映射中定义为键，该映射链接到订阅列表映射。

      阅读有关表达式中[对字段](expression/field-references.md)的引用的更多信息。

      ![为订阅者发送包含个性化内容的电子邮件配置](assets/message-to-subscribers-uc-2.png)

   1. 在&#x200B;**[!UICONTROL 添加表达式]**&#x200B;对话框中，单击&#x200B;**[!UICONTROL 确定]**。

>[!CAUTION]
>
>仅应针对特定用例使用电子邮件地址覆盖。 大多数情况下，无需更改电子邮件地址，应使用&#x200B;**[!UICONTROL 执行字段]**&#x200B;中定义为主地址的值。 [了解详情](../configuration/primary-email-addresses.md)

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;此页显示如何通过使用从同意映射字段读取订阅者地址的表达式来覆盖默认电子邮件地址参数，从而构建向列表订阅者发送电子邮件的历程。

**意图：**

* 使用读取受众活动构建定位特定列表订阅者的历程
* 使用表达式编辑器覆盖电子邮件操作活动中的默认电子邮件地址
* 使用`entry`和`firstEntryKey`函数从同意映射中检索订阅者电子邮件地址
* 引用同意和偏好设置详细信息字段组以访问订阅列表数据

**术语表：**

* **电子邮件地址覆盖（参数覆盖）**：历程电子邮件活动设置将默认用户档案电子邮件地址替换为自定义表达式，用于特殊情况，如订阅列表定位。 *（产品特定）*
* **同意和偏好设置详细信息字段组**： Adobe Experience Platform架构字段组，包含订阅和同意数据，包括用于存储订阅者电子邮件地址的`subscriptions`映射。 *（产品特定）*
* **`entry`函数**：表达式函数，它通过命名空间键引用映射元素 — 此处用于引用特定的订阅列表（例如，`daily-email`）。 *（产品特定）*
* **`firstEntryKey`函数**：检索映射的第一个键的表达式函数 — 在此用于从订阅列表的订阅者映射中检索第一个电子邮件地址。 *（产品特定）*

**护栏：**

* 电子邮件地址覆盖仅应用于特定用例，例如订阅列表定位；在大多数情况下，应使用执行字段中定义的主地址
* 要使该用例正常工作，架构中必须存在同意和偏好设置详细信息字段组
* 表达式中使用的订阅列表名称（例如`daily-email`）必须与数据中配置的名称完全匹配

**术语：**

* 规范名称：电子邮件地址覆盖 — 缩写：无 — 变体：参数覆盖，电子邮件参数覆盖
* 同义词： &quot;subscription list&quot; = &quot;subscriber list&quot;
* 请勿混淆：“电子邮件地址覆盖”≠“主电子邮件地址” — 主电子邮件地址是所有历程中使用的默认地址；覆盖是仅用于订阅列表发送等特殊情况的每个活动的表达式

**常见问题解答：**

* **问：如何将电子邮件发送给订阅列表的订阅者，而不是个人资料电子邮件地址？**  — 在电子邮件活动的Address字段上启用参数覆盖，并使用`entry`和`firstEntryKey`函数输入表达式，以从目标订阅列表的订阅者映射中检索地址。
* **问：此用例需要哪个字段组？** — Adobe Experience Platform中的“同意和偏好设置详细信息”字段组，其中包含用于存储订阅者电子邮件地址的`subscriptions`映射结构。
* **问：定位订阅者时是否应始终使用电子邮件地址覆盖？**  — 否；电子邮件地址覆盖仅适用于特定用例。 在大多数历程中，应使用执行字段中定义的主地址。
* **问：`firstEntryKey`函数在此上下文中做什么？**  — 从与特定订阅列表关联的`subscribers`映射中检索第一个电子邮件地址密钥，使历程能够寻址单个订阅者。

+++
