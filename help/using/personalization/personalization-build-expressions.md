---
title: 关于表达式编辑器
description: 了解如何使用表达式编辑器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 5%

---

# 关于表达式编辑器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="关于表达式编辑器"
>abstract="表达式编辑器允许您选择、排列、自定义和验证所有数据，以便为您的内容创建自定义个性化。"

表达式编辑器是 [!DNL Journey Optimizer]. 它在您需要定义个性化（如电子邮件、推送和选件）的每个上下文中均可用。

在表达式编辑器界面中，您将选择、排列、自定义和验证所有数据，以为您的内容创建自定义个性化。

![](assets/perso_ee1.png)

屏幕的左侧部分显示一个域选择器，用于选择个性化的源。

![](assets/perso_ee3.png)

可用源包括：

* **[!UICONTROL Profile attributes]** :列出与 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。
* **[!UICONTROL Segment memberships]** :列出在Adobe Experience Platform分段服务中创建的所有区段。 有关可用分段的更多信息 [此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Offer decisions]** :列出与特定版面关联的所有选件。 选择版面，然后在内容中插入选件。 有关如何管理选件的完整文档，请参阅 [此部分](../messages/deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** :当 **消息** 在历程中使用，通过此菜单可使用上下文历程字段。 在 [此部分](personalization-use-case.md).
* **[!UICONTROL Helper functions]** :列出可用于对数据执行操作的所有帮助程序函数，例如计算、数据格式或转化、条件，并在个性化环境中处理这些函数。 在 [此部分](functions/functions.md).

单击+按钮以向编辑器中添加属性。

>[!NOTE]
>
>通过“+”图标旁边的椭圆菜单，您可以获取每个变量的更多详细信息，并将最常用的属性添加到 [收藏夹](personalization-favorites.md).

![](assets/attribute-details.png)

在以下示例中，表达式编辑器允许您选择今天生日的用户档案，然后通过插入与当天对应的特定选件来完成自定义。

![](assets/perso_ee2.png)

准备好个性化表达式后，您需要通过表达式编辑器验证该表达式。 在 [此部分](personalization-validation.md).
