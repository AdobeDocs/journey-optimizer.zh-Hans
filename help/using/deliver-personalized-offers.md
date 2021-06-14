---
title: 添加个性化优惠
description: 了解如何向邮件中添加个性化优惠
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 添加个性化优惠 {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## 关于决策管理 {#about-offer-decisioning}

借助[!DNL Journey Optimizer]，您可以在电子邮件中插入决策（以前称为选件活动），以便利用选件决策引擎来选择要交付给客户的最佳选件。

例如，您可以添加一个决策，该决策会在电子邮件中显示一个特殊折扣选件，该选件将因收件人的忠诚度级别而异。

有关如何创建和管理选件的更多信息，请参阅[此部分](offers/get-started/starting-offer-decisioning.md)。

## 在电子邮件{#insert-offers}中插入决策

要在电子邮件中插入决策，请执行以下步骤：

1. 创建电子邮件，然后打开Email Designer以配置其内容。

1. 添加&#x200B;**[!UICONTROL Offer decision]**&#x200B;内容组件（请参阅[使用内容组件](content-components.md)）。

   ![](assets/deliver-offer-component.png)

1. 组件中会添加&#x200B;**[!UICONTROL Offer decision]**&#x200B;选项卡。 单击&#x200B;**[!UICONTROL Add personalization - Offer decision]**&#x200B;以添加选件活动。

   ![](assets/deliver-offer-tab.png)

1. 选择与要显示的选件对应的版面。

   版面是用于显示选件的容器。 在此示例中，我们将使用“电子邮件顶部图像”放置。 此位置已在选件库中创建，用于显示位于消息顶部的图像类型选件。

1. 选择要在内容组件中使用的选件活动，然后单击&#x200B;**[!UICONTROL Add]**。

   >[!NOTE]
   >
   >请注意，列表中仅显示与所选版面兼容的决策。 在此示例中，只有一个选件活动与“电子邮件顶部图像”版面相匹配。

   ![](assets/deliver-offer-placement.png)

1. 选件活动现已添加到组件中。 您可以使用&#x200B;**[!UICONTROL Offers]**&#x200B;部分或内容组件箭头预览决策中涉及的不同选件。

   ![](assets/deliver-offer-preview.png)
