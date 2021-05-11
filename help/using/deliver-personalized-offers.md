---
title: 添加个性化优惠
description: 了解如何在消息中添加个性化优惠
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 添加个性化优惠{#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## 关于决策管理{#about-offer-decisioning}

通过[!DNL Journey Optimizer]，您可以在电子邮件决策(以前称为优惠活动)中插入，这些决策将利用优惠决策引擎来选择最适合向客户交付的优惠。

例如，您可以添加一项将在电子邮件中显示特殊折扣优惠的决定，该折扣视收件人的忠诚度级别而异。

有关如何创建和管理优惠的详细信息，请参阅[本节](offers/get-started/starting-offer-decisioning.md)。

## 在电子邮件{#insert-offers}中插入决定

要在电子邮件中插入决定，请执行以下步骤：

1. 创建您的电子邮件，然后打开电子邮件设计器以配置其内容。

1. 添加&#x200B;**[!UICONTROL Offer decision]**&#x200B;内容组件（请参阅[使用内容组件](content-components.md)）。

   ![](assets/deliver-offer-component.png)

1. **[!UICONTROL Offer decision]**&#x200B;选项卡会添加到组件中。 单击&#x200B;**[!UICONTROL Add personalization - Offer decision]**&#x200B;添加优惠活动。

   ![](assets/deliver-offer-tab.png)

1. 选择与要显示的优惠对应的位置。

   版面是用于展示您的容器的优惠。 在此示例中，我们将使用“通过电子邮件发送最佳图像”的位置。 此位置已在优惠库中创建，用于显示位于消息顶部的图像类型优惠。

1. 选择要在内容组件中使用的优惠活动，然后单击&#x200B;**[!UICONTROL Add]**。

   >[!NOTE]
   >
   >请注意，只有与所选位置兼容的决策才会显示在列表中。 在此示例中，只有一个优惠活动与“电子邮件至上图像”位置匹配。

   ![](assets/deliver-offer-placement.png)

1. 优惠活动现已添加到组件中。 您可以使用&#x200B;**[!UICONTROL Offers]**&#x200B;部分或内容组件箭头预览作为决策一部分的不同优惠。

   ![](assets/deliver-offer-preview.png)
