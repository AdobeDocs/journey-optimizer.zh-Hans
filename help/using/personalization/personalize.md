---
title: 在 Journey Optimizer 中个性化内容
description: 个性化入门
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 7be83409f7a594747963c5b125f3bf96c0b4f8b6
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 13%

---

# 个性化入门{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] 个性化功能，通过利用您拥有的有关邮件的数据和信息，使邮件适应每个特定收件人。 这可以是他们的名字、兴趣、住处、购买的东西等。

➡️ [了解如何在这些视频中个性化消息](#video-perso)

[!DNL Journey Optimizer] 使用 **内嵌** 基于Handlebars的简单个性化语法，允许您创建内容由双大括号括起的表达式 **{{}}**. 您可以在同一内容或字段中添加多个表达式，而不受限制。在 [个性化语法](personalization-syntax.md).

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。在 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

>[!CAUTION]
>的 **XDM个人配置文件** 架构是您唯一可以在 [!DNL Journey Optimizer].

**示例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

处理消息（电子邮件和推送）时，Journey Optimizer会将表达式替换为Experience Cloud平台数据库中包含的数据：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 变成了“你好，无名氏”。


## 个性化上下文{#personalization-areas}

投放的消息的内容和显示 [!DNL Journey Optimizer] 可通过多种不同方式进行个性化。

在每个带有编辑器图标的字段中，您可以打开个性化编辑器（也称为表达式编辑器）并定义个性化。

![](assets/perso_icon.png)

### 个性化电子邮件

创建电子邮件时，您可以在 **[!UICONTROL Subject line]** 字段。

![](assets/perso_subject.png)

在电子邮件设计器中，您可以个性化内容：

* 在 **消息**:在文本块内单击，然后单击 **个性化** 图标，然后选择 **插入个性化** 字段。 有关Email Designer界面的更多信息，请参阅此 [部分](../design-emails.md).

   ![](assets/perso_insert.png)

* 对于 **链接**:选择文本块中的某些文本或图像，单击 **插入链接** 图标。 在窗口中，您可以通过单击 **添加个性化** 图标。

   ![](assets/perso_link.png)

在这两种情况下，您都可以访问个性化编辑器。

![](assets/perso_ee.png)

### 个性化推送通知

您还可以将 **推送通知** 在以下字段中：

* **标题**
* **正文**
* **自定义声音**
* **徽章**
* **自定义数据**

![](assets/perso_push.png)

了解有关 [此部分](../push-gs.md).

### 个性化您的选件 {#personalize-offers}

在将文本类型内容添加到选件的表示时，您还可以访问个性化编辑器。

了解有关使用 [此部分](../offers/offer-library/creating-personalized-offers.md#custom-text).

## 使用表达式编辑器 {#use-expression-editor}

表达式编辑器是 [!DNL Journey Optimizer].

它在您需要定义个性化（如电子邮件、推送和选件）的每个上下文中均可用。

在表达式编辑器界面中，您将选择、排列、自定义和验证所有数据，以为您的内容创建自定义个性化。

![](assets/perso_ee1.png)

屏幕的左侧部分显示一个域选择器，用于选择个性化的源。

![](assets/perso_ee3.png)

可用源包括：

* **[!UICONTROL Profile attributes]** :列出与 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Segment memberships]** :列出在Adobe Experience Platform分段服务中创建的所有区段。 有关可用分段的更多信息 [此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Offer decisions]** :列出与特定版面关联的所有选件。 选择版面，然后在内容中插入选件。 有关如何管理选件的完整文档，请参阅 [此部分](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** :当 **消息** 在历程中使用，通过此菜单可使用上下文历程字段。 在 [此部分](personalization-use-case.md).
* **[!UICONTROL Helper functions]** :列出可用于对数据执行操作的所有帮助程序函数，例如计算、数据格式或转化、条件，并在个性化环境中处理这些函数。 在 [此部分](functions/functions.md).

选择后，将在编辑器中添加引用。

>[!NOTE]
>
>“+”图标旁边的信息图标将打开工具提示，其中提供了每个变量的更多详细信息。

在以下示例中，表达式编辑器允许您选择今天生日的用户档案，然后通过插入与当天对应的特定选件来完成自定义。

![](assets/perso_ee2.png)

## 操作方法视频{#video-perso}

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
