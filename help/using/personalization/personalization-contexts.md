---
solution: Journey Optimizer
product: journey optimizer
title: 个性化上下文
description: 详细了解使消息的内容和显示个性化的方法。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式、编辑器、上下文、个性化
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 15%

---

# 个性化上下文{#personalization-areas}

[!DNL Journey Optimizer]投放的邮件的内容和显示可以通过几种不同的方式进行个性化。 在每个具有编辑器图标的字段中，您可以打开个性化编辑器（也称为个性化编辑器）并定义个性化。

![](assets/perso_icon.png)

## 使电子邮件个性化 {#personalize-emails}

创建电子邮件时，您可以在邮件的&#x200B;**[!UICONTROL 主题行]**&#x200B;字段中添加个性化设置。

![](assets/perso_subject.png)

在Email Designer中，您可以个性化内容：

* 在&#x200B;**消息**&#x200B;中：单击文本块内部，然后单击上下文工具栏中的&#x200B;**添加Personalization**&#x200B;图标。 有关电子邮件Designer界面的详细信息，请参阅此[部分](../email/get-started-email-design.md)。

  ![](assets/perso_insert.png)

* 对于&#x200B;**链接**：选择文本块中的某些文本或图像，单击上下文工具栏中的&#x200B;**插入链接**&#x200B;图标。 在窗口中，您可以通过单击&#x200B;**添加个性化**&#x200B;图标来添加个性化块。

  ![](assets/perso_link.png)

在这两种情况下，您都可以访问个性化编辑器。

![](assets/perso_ee.png)

## 个性化设置推送通知 {#personalize-push}

您还可以在以下字段中个性化设置&#x200B;**推送通知**：

* **标题**
* **正文**
* **自定义声音**
* **徽章**
* **自定义数据**

![](assets/perso_push.png)

在[本节](../push/push-gs.md)中了解有关推送通知配置的更多信息。

## 个性化您的优惠 {#personalize-offers}

在将文本类型内容添加到优惠的表示法时，您还可以访问个性化编辑器。

在[本节](../offers/offer-library/creating-personalized-offers.md#custom-text)中了解有关使用决策管理管理内容的更多信息。

## 创建个性化URL{#personalize-urls}

个性化 URL 可将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于用户档案属性。在Adobe Journey Optimizer中，您可以向消息内容中的URL添加个性化设置。 URL 个性化可应用于文本和图像，并使用用户档案数据或上下文数据。

了解如何在[本节](personalization-syntax.md#perso-urls)中插入个性化URL。

