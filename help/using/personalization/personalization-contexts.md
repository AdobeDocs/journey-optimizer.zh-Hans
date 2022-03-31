---
title: 个性化上下文
description: '进一步了解个性化内容和显示消息的方式。 '
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 15%

---

# 个性化上下文{#personalization-areas}

投放的消息的内容和显示 [!DNL Journey Optimizer] 可通过多种不同方式进行个性化。

在每个带有编辑器图标的字段中，您可以打开个性化编辑器（也称为表达式编辑器）并定义个性化。

![](assets/perso_icon.png)

## 个性化电子邮件 {#personalize-emails}

创建电子邮件时，您可以在 **[!UICONTROL Subject line]** 字段。

![](assets/perso_subject.png)

在电子邮件设计器中，您可以个性化内容：

* 在 **消息**:在文本块内单击，然后单击 **个性化** 图标，然后选择 **插入个性化** 字段。 有关Email Designer界面的更多信息，请参阅此 [部分](../design/design-emails.md).

   ![](assets/perso_insert.png)

* 对于 **链接**:选择文本块中的某些文本或图像，单击 **插入链接** 图标。 在窗口中，您可以通过单击 **添加个性化** 图标。

   ![](assets/perso_link.png)

在这两种情况下，您都可以访问个性化编辑器。

![](assets/perso_ee.png)

## 个性化推送通知 {#personalize-push}

您还可以将 **推送通知** 在以下字段中：

* **标题**
* **正文**
* **自定义声音**
* **徽章**
* **自定义数据**

![](assets/perso_push.png)

了解有关 [此部分](../configuration/push-gs.md).

## 个性化您的选件 {#personalize-offers}

在将文本类型内容添加到选件的表示时，您还可以访问个性化编辑器。

了解有关使用 [此部分](../offers/offer-library/creating-personalized-offers.md#custom-text).

## 创建个性化URL{#personalize-urls}

个性化 URL 可将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于用户档案属性。在Adobe Journey Optimizer中，您可以向消息内容中的URL添加个性化。 URL 个性化可应用于文本和图像，并使用用户档案数据或上下文数据。

了解如何在 [此部分](personalization-syntax.md#perso-urls).

