---
solution: Journey Optimizer
product: journey optimizer
title: 关于表达式编辑器
description: 了解如何使用表达式编辑器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器，关于，开始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 10%

---

# 开始使用表达式编辑器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="关于表达式编辑器"
>abstract="表达式编辑器让您可以选择、排列、自定义和验证所有数据，为自己的内容创建定制的个性化。"

表达式编辑器是中个性化的核心 [!DNL Journey Optimizer]. 它可在您需要定义个性化的每个上下文中使用，例如电子邮件、推送和选件。

在表达式编辑器界面中，您将选择、排列、自定义和验证所有数据，以创建内容的自定义个性化设置。

![](assets/perso_ee1.png)

## 可用的个性化源 {#sources}

屏幕左侧显示一个域选择器，允许您选择个性化的源。 可用源包括：

* **[!UICONTROL 配置文件属性]** ：列出与中所述的配置文件架构关联的所有引用 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}.
* **[!UICONTROL 受众]** ：列出在Adobe Experience Platform分段服务中创建的所有受众。 有关分段的更多信息，请访问 [此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}.
* **[!UICONTROL 优惠决策]** ：列出与特定投放位置关联的所有选件。 选择投放位置，然后在您的内容中插入选件。 有关如何管理优惠的完整文档，请参阅 [本节](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL 上下文属性]** ：当在历程或营销策划中使用渠道操作活动（电子邮件、推送、短信）时，与事件和属性相关的上下文属性可用于个性化。 有关利用上下文属性的个性化示例，请参见 [本节](personalization-use-case.md).
* **[!UICONTROL 辅助函数]** ：列出可用于对数据执行操作（例如计算、数据格式或转换、条件）的所有辅助函数，并在个性化上下文中处理这些函数。 有关详细信息，请参阅[此部分](functions/functions.md)。

## 添加个性化属性 {#add}

单击+按钮可向个性化表达式添加属性。

通过“+”图标旁边的省略号菜单，可获取每个变量的更多详细信息并将最常用的属性添加到收藏夹。 [了解如何将属性添加到收藏夹](personalization-favorites.md)

>[!NOTE]
>
>如果您要定位具有使用构成工作流或自定义上传（CSV文件）生成的扩充属性的受众，则可以利用这些扩充属性个性化您的消息。 [了解如何使用受众扩充属性](../audience/about-audiences.md#enrichment)

此外，您可以定义在字符串类型配置文件属性为空时显示的默认回退文本。 为此，请单击属性旁边的省略号按钮，然后选择 **[!UICONTROL 插入后备文本]**. 编写在配置文件的属性值为空时默认显示的文本，然后单击 **[!UICONTROL 添加]**.

![](assets/attribute-details.png)

在以下示例中，表达式编辑器允许您选择今天生日的用户档案，然后插入对应于今天的特定选件以完成自定义。

![](assets/perso_ee2.png)

个性化表达式准备就绪后，需要由表达式编辑器验证该表达式。 有关详细信息，请参阅[此部分](personalization-validation.md)。
