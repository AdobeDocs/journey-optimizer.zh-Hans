---
title: 在 Journey Optimizer 中个性化内容
description: 个性化入门
feature: 个性化
topic: 个性化
role: Data Engineer
level: Beginner
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 9%

---

# 个性化入门{#add-personalization}

探索[!DNL Adobe Journey Optimizer]个性化功能，通过利用您拥有的关于他/她的数据和信息，使您的消息适应每个特定收件人。 这可以是他的名字、兴趣、居住地、购买的东西等。

➡️ [了解如何对这些视频中的消息进行个性化](#video-perso)

[!DNL Journey Optimizer] 使用基 **** 于Handlebars的inlinesimple个性化语法，该语法允许您创建内容由双大括号包&#x200B;**围的表达式{{}}**。您可以在同一内容或字段中添加多个表达式，而不受限制。请参阅[个性化语法](personalization-syntax.md)，以了解更多信息。

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。在[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}中了解更多信息。

>[!CAUTION]
>**XDM个人配置文件**&#x200B;架构是您唯一可用于在[!DNL Journey Optimizer]中个性化内容的架构。

**示例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

处理消息（电子邮件和推送）时，Journey Optimizer会将表达式替换为Experience Cloud平台数据库中包含的数据： `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`变为“Hello John Doe”。


## 个性化上下文{#personalization-areas}

[!DNL Journey Optimizer]投放的消息的内容和显示可通过多种不同方式进行个性化。

在每个带有编辑器图标的字段中，您可以打开个性化编辑器（也称为表达式编辑器）并定义个性化。

![](assets/perso_icon.png)

### 个性化电子邮件

创建电子邮件时，可以在邮件的&#x200B;**Email subject**&#x200B;字段中添加个性化。

![](assets/perso_subject.png)

在电子邮件设计器中，您可以个性化内容：

* 在&#x200B;**message**&#x200B;中：在文本块内单击，单击上下文工具栏中的&#x200B;**Personalize**&#x200B;图标，然后选择&#x200B;**插入个性化**&#x200B;字段。 有关Email Designer界面的更多信息，请参阅此[部分](../design-emails.md)。

   ![](assets/perso_insert.png)

* 对于&#x200B;**链接**:选择文本块中的某些文本或图像，单击上下文工具栏中的&#x200B;**插入链接**&#x200B;图标。 在窗口中，您可以通过单击&#x200B;**添加个性化**&#x200B;图标来添加个性化块。

   ![](assets/perso_link.png)

在这两种情况下，您都可以访问个性化编辑器。

![](assets/perso_ee.png)


### 个性化推送通知

您还可以在以下字段中个性化您的&#x200B;**推送通知**:

* **标题**
* **正文**
* **自定义声音**
* **徽章**
* **自定义数据**

![](assets/perso_push.png)

详细了解[此部分](../push-gs.md)中的推送通知配置。

## 使用表达式编辑器

表达式编辑器是[!DNL Journey Optimizer]中个性化的核心。

它在您需要定义个性化（如电子邮件、推送和选件）的每个上下文中均可用。

在表达式编辑器界面中，您将选择、排列、自定义和验证所有数据，以为您的内容创建自定义个性化。

![](assets/perso_ee1.png)

屏幕的左侧部分显示一个域选择器，用于选择个性化的源。 可用源包括：

* **用户档案** :列出与 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}中所述的配置文件架构关联的所有引用。
* **区段成员资格** :列出在Adobe Experience Platform分段服务中创建的所有区段。有关可用分段的更多信息，请参见[此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en){target=&quot;_blank&quot;}。
* **选件** :列出与特定版面关联的所有选件。选择版面，然后在内容中插入选件。 有关如何管理选件的完整文档，请参阅[此部分](../deliver-personalized-offers.md)。
* **上下文** :在历程 **** 中使用消息活动时，此菜单中提供了上下文历程字段。在[此部分](personalization-use-case.md)中了解详情。
* **帮助程序函数** :列出可用于对数据执行操作的所有帮助程序函数，例如计算、数据格式或转化、条件，并在个性化环境中处理这些函数。在[此部分](functions/functions.md)中了解详情。

选择后，将在编辑器中添加引用。

>[!NOTE]
>
>“+”图标旁边的信息图标将打开工具提示，其中提供了每个变量的更多详细信息。

在以下示例中，表达式编辑器允许您选择今天生日的用户档案，然后通过插入与当天对应的特定选件来完成自定义。

![](assets/perso_ee2.png)

## 操作方法视频{#video-perso}

了解如何使用历程中的情境事件信息来个性化消息。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何使用历程中的情境事件信息来个性化消息。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
