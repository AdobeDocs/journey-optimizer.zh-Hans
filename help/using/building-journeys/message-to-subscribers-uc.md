---
title: 向订阅者发送消息
description: 了解如何构建旅程以向列表的订阅者发送消息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 59ee283f50850e160e7a6506c1f0deab1976f20c
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# 向列表的订阅者发送消息

此用例的用途是创建旅程，以向列表的订阅者发送消息。

在本例中， **[!UICONTROL Consent and Preference Details]** 字段组自 [!DNL Adobe Experience Platform] 中，将使用。 要查找此字段组，请从 **[!UICONTROL Data Management]** 菜单，选择 **[!UICONTROL Schemas]**. 在 **[!UICONTROL Field groups]** 选项卡，在搜索字段中输入字段组的名称。

![此字段组包含订阅元素](../assets/consent-and-preference-details-field-group.png)

要配置此历程，请执行以下步骤：

1. 创建以 **[!UICONTROL Read]** 活动。 [了解更多信息](journey-gs.md)。
1. 添加 **[!UICONTROL Message]** 活动，通过电子邮件发送到历程。 [了解更多信息](journeys-message.md)。
1. 在 **[!UICONTROL Email parameters]** 部分 **[!UICONTROL Message]** 活动设置，替换默认的电子邮件地址(`PersonalEmail.adress`)，其电子邮件地址为列表订阅者：

   1. 单击 **[!UICONTROL Enable parameter override]** 图标 **[!UICONTROL Address]** 字段，然后单击 **[!UICONTROL Edit]** 图标。

      ![](../assets/message-to-subscribers-uc-1.png)

      要修改电子邮件地址，您必须先已发布了该消息。

   1. 在表达式编辑器中，输入用于检索订阅者电子邮件地址的表达式。 [了解更多](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=zh-Hans){target=&quot;_blank&quot;}。

      此示例显示的表达式包含对映射字段的引用：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在本例中，使用了以下函数：

      | 函数 | 描述 | 示例 |
      | --- | --- | --- |
      | `entry` | 根据所选命名空间引用映射元素 | 请参阅特定订阅列表 |
      | `firstEntryKey` | 检索映射的第一个条目键 | 检索订阅者的第一个电子邮件地址 |

      在本例中，订阅列表名为 `daily-email`. 电子邮件地址在 `subscribers` 映射，链接到订阅列表映射。

      有关更多信息 [对字段的引用](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/field-references.html) 中。

      ![](../assets/message-to-subscribers-uc-2.png)

   1. 在 **[!UICONTROL Add an expression]** 对话框，单击 **[!UICONTROL Ok]**.

   ![](../assets/message-to-subscribers-uc-3.png)

1. 通过 **[!UICONTROL End]** 活动。




