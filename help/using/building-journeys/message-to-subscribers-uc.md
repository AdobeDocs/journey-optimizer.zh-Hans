---
solution: Journey Optimizer
product: journey optimizer
title: 向订阅者发送消息
description: 了解如何构建历程以向列表的订阅者发送消息
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: 历程，用例，消息，订阅者，列表，读取
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# 用例：向列表的订阅者发送消息{#send-a-message-to-the-subscribers-of-a-list}

此用例的目的在于创建历程，以向列表的订阅者发送消息。

在此示例中， **[!UICONTROL 同意和偏好设置详细信息]** 字段组来源 [!DNL Adobe Experience Platform] 已使用。 要查找此字段组，请从 **[!UICONTROL 数据管理]** 菜单，选择 **[!UICONTROL 架构]**. 在 **[!UICONTROL 字段组]** 选项卡，在搜索字段中输入字段组的名称。

![此字段组包括subscriptions元素](assets/consent-and-preference-details-field-group.png)

要配置此历程，请执行以下步骤：

1. 创建以开始的历程 **[!UICONTROL 读取]** 活动。 [了解更多信息](journey-gs.md)。
1. 添加 **[!UICONTROL 电子邮件]** 历程的操作活动。 [了解更多信息](journeys-message.md)。
1. 在 **[!UICONTROL 电子邮件参数]** 的部分 **[!UICONTROL 电子邮件]** 活动设置，替换默认电子邮件地址(`PersonalEmail.adress`)的电子邮件中指定订阅者的电子邮件地址：

   1. 单击 **[!UICONTROL 启用参数覆盖]** 图标（位于右侧） **[!UICONTROL 地址]** 字段，然后单击 **[!UICONTROL 编辑]** 图标。

      ![](assets/message-to-subscribers-uc-1.png)

   1. 在表达式编辑器中，输入用于检索订阅者电子邮件地址的表达式。 [了解更多信息](expression/expressionadvanced.md)。

      此示例显示一个包含映射字段引用的表达式：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在此示例中，使用以下函数：

      | 函数 | 描述 | 示例 |
      | --- | --- | --- |
      | `entry` | 根据选定的命名空间引用映射元素 | 请参阅特定订阅列表 |
      | `firstEntryKey` | 检索映射的第一个条目键 | 检索订阅者的第一个电子邮件地址 |

      在此示例中，将命名订阅列表 `daily-email`. 电子邮件地址在中定义为键 `subscribers` 映射，链接到订阅列表映射。

      详细了解 [对字段的引用](expression/field-references.md) 在表达式中。

      ![](assets/message-to-subscribers-uc-2.png)

   1. 在 **[!UICONTROL 添加表达式]** 对话框中，单击 **[!UICONTROL 确定]**.

>[!CAUTION]
>
>仅应针对特定用例使用电子邮件地址覆盖。大多数情况下，无需更改电子邮件地址，应使用&#x200B;**[!UICONTROL 执行字段]**&#x200B;中定义为主地址的值。[了解详情](../configuration/primary-email-addresses.md)
