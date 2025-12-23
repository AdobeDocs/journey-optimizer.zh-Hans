---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 利用自定义上传受众进行决策
description: 了解如何利用自定义上传受众进行决策。
badge: label="旧版" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: bd950410-691b-49d8-8851-8c6c448c00fd
version: Journey Orchestration
source-git-commit: 62b244990611006e5eced7a5d35dbd0373aa23f7
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 5%

---

# 利用自定义上传受众进行决策 {#custom-upload-decisioning}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！[了解详情](../experience-decisioning/gs-experience-decisioning.md)

通过[!DNL Journey Optimizer]，您可以将使用自定义上传（CSV文件）创建的受众中的数据用到[!DNL Adobe Experience Platform]中。 此数据支持您的决策管理工作流。 当配置文件上不需要数据，但在决策中仍然必须提供数据时，此功能尤为有用。

可以在决策管理中利用来自自定义上传受众的数据：

1. 优惠和决策中的资格标准。
2. 个性化优惠呈现中的内容。

有关自定义上传受众的更多信息，请参阅以下章节：

* [受众和Journey Optimizer入门](../audience/about-audiences.md)
* [在Adobe Experience Platform中导入受众](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## 必读 {#must-read}

* **仅决策管理** — 仅在决策管理中支持此功能，而不在Decisioning（以前称为“Experience Decisioning”）中支持。
* 仅&#x200B;**决策API（中心）** — 仅通过Decisioning API（中心）请求提供，Edge Decisioning API或批量决策不支持该功能。
* **扩充数据所需的API旗标** — 使用自定义上传(CSV)受众时，如果您想在优惠决策响应中检索扩充数据，则必须在您的API请求有效负载中包含`"xdm:enrichedAudience": true`。 如果没有此标志，将不会返回CSV上传受众中的扩充属性。 [了解有关Decisioning API的更多信息](api-reference/offer-delivery-api/decisioning-api.md)

## 使用自定义上传受众作为资格标准 {#eligibilty}

您可以将自定义上传受众用作优惠或决策级别的资格标准。 添加后，这些标准可以从资格中排除优惠或优惠集合。 以下是您可以利用自定义上传受众来优化优惠和决策资格的各种位置：

* 使用自定义上传受众创建决策规则：

   1. 在创作规则时，访问&#x200B;**受众**&#x200B;选项卡并在列表中搜索CSV受众。 将受众拖放到规则画布中。
   1. 使用&#x200B;**属性**&#x200B;选项卡并导航到链接到所选受众的扩充架构。 这允许您访问CSV文件中的所有数据，并在规则中使用这些数据。 [了解如何创建决策规则](../offers/offer-library/creating-decision-rules.md)
   1. 保存规则。 创建规则后，即可在优惠和决策级别使用它来优化其资格。

  决策规则画布中的![CSV受众](assets/csv-rule.png)

* 使用自定义上传受众作为选件限制。 [了解如何向优惠添加约束](../offers/offer-library/add-constraints.md)

  在创作选件时，在&#x200B;**添加约束**&#x200B;步骤，您可以：

   * 使用自定义上传受众来定义选件资格，
   * 利用自定义上传受众应用规则。

  ![自定义上载受众限制选项](assets/csv-offer.png)

* 在决策级别使用自定义上传受众。

  设置决策时，在&#x200B;**添加决策范围**&#x200B;步骤中，您可以使用自定义上传受众作为优惠集合的评估标准。 [了解如何定义决策范围](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![决策级别的自定义上传受众](assets/csv-decision.png)

## 使用自定义上传受众使优惠呈现个性化

自定义上传受众也可用于通过引用CSV文件中的数据来个性化优惠呈现的内容。 [了解如何向优惠添加呈现](../offers/offer-library/add-representations.md)

要利用自定义上传受众的属性进行个性化，您首先需要添加自定义受众作为限制。 为此，在创作选件时，请在&#x200B;**添加约束**&#x200B;步骤中将受众添加为约束或选择利用自定义上传受众的规则。

![自定义上载受众限制选项](assets/csv-offer.png)

将受众添加为限制后，您可以使用其属性来个性化呈现内容。 为此，请访问&#x200B;**配置文件属性**&#x200B;选项卡并搜索自定义上传受众。 从受众中选择相关属性以个性化选件内容。

![配置文件属性个性化界面](assets/csv-perso.png)
