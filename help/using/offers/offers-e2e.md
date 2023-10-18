---
title: 在电子邮件中使用个性化优惠
description: 探索一个端到端示例，其中显示配置选件和在电子邮件中使用它们所需的所有步骤。
feature: Decision Management, Email
topic: Integrations
role: User
level: Intermediate
exl-id: 851d988a-2582-4c30-80f3-b881d90771be
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 6%

---

# 用例：配置个性化优惠并将其添加到电子邮件中 {#configure-add-personalized-offers-email}

本节将提供一个端到端示例，说明如何根据您之前创建的决策配置优惠并在电子邮件中使用它们。

## 主要步骤 {#main-steps}

下面列出了配置优惠（在决策中包括优惠）并在电子邮件中利用此决策的关键步骤：

1. 在创建选件之前， [定义组件](#define-components)

   * 创建投放位置
   * 创建决策规则
   * 创建收藏集限定符 （以前称为“标记”）
   * 创建排名（可选）

1. [配置优惠](#configure-offers)

   * 创建优惠
   * 对于每个选件：

      * 创建表示，并为每个表示选择版面和资产
      * 为每个选件添加规则
      * 定义每个优惠的优先级

1. [创建后备优惠](#create-fallback)

1. [创建收藏集](#create-collection) 以包含您创建的个性化优惠

1. [配置决策](#configure-decision)

   * 创建决策
   * 选择您创建的版面
   * 对于每个投放位置，选择收藏集
   * 对于每个投放位置，选择一个排名（可选）
   * 选择后备

1. [在电子邮件中插入决策](#insert-decision-in-email)

   * 选择与要显示的选件匹配的版面
   * 从与所选投放位置兼容的项目中选择决策
   * 预览优惠

在电子邮件中使用选件的整体决策管理过程可描述如下：

![](assets/offers-e2e-process.png)

## 定义组件 {#define-components}

在开始创建选件之前，必须定义将在选件中使用的多个组件。

您将在以下位置找到它们： **[!UICONTROL 决策管理]** > **[!UICONTROL “组件”菜单]**.

1. 首先创建 **投放位置** 您的选件。

   您将使用这些投放位置来定义在定义优惠决策时生成的优惠的显示位置。

   在此示例中，使用以下渠道和内容类型创建三个投放位置：

   * *Web — 图像*
   * *电子邮件 — 图像*
   * *非数字 — 文本*

   ![](assets/offers-e2e-placements.png)

   有关创建版面的详细步骤，请参见 [本节](../../using/offers/offer-library/creating-placements.md).

1. 创建 **决策规则**.

   决策规则将为Adobe Experience Platform中的配置文件提供最佳优惠。

   使用配置两个简单规则 **[!UICONTROL XDM个人资料>人员>性别]** 属性：

   * *女性客户*
   * *男性客户*

   ![](assets/offers-e2e-rules.png)

   有关创建规则的详细步骤，请参见 [本节](../../using/offers/offer-library/creating-decision-rules.md).

1. 您还可以创建 **集合限定符**.

   然后，您可以将其与优惠相关联，并使用此收藏集限定符将优惠分组到一个收藏集中。

   在此示例中，创建 *瑜伽* 集合限定符。

   ![](assets/offers-e2e-tag.png)

   有关创建集合限定符的详细步骤，请参阅 [本节](../../using/offers/offer-library/creating-tags.md).

1. 如果要定义规则以确定在给定投放位置应首先显示哪个优惠（而不是考虑优惠的优先级评分），则可以创建 **排名公式**.

   有关创建排名公式的详细步骤，请参见 [本节](../../using/offers/ranking/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >在本例中，我们将仅使用优先级分数。 详细了解 [合格规则和约束](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## 配置优惠 {#configure-offers}

您现在可以创建并配置选件。 在此示例中，您将创建四个要根据每个特定配置文件显示的选件。

1. 创建选件. 有关详细信息，请参阅[此部分](../../using/offers/offer-library/creating-personalized-offers.md#create-offer)。

1. 在此优惠中，创建三个呈现。 每个表示都必须是您之前创建的版面和资源的组合：

   * 一个对应于 *Web — 图像* 投放
   * 一个对应于 *电子邮件 — 图像* 投放
   * 一个对应于 *非数字 — 文本* 投放

   >[!NOTE]
   >
   >选件可以显示在消息中的不同位置，从而创造更多机会在不同的投放位置上下文中使用选件。

   了解中表示法的更多信息 [本节](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. 为前两个投放位置选择适当的图像。 输入自定义文本 *非数字 — 文本* 投放位置。

   ![](assets/offers-e2e-representations.png)

1. 在 **[!UICONTROL 优惠资格]** 部分，选择 **[!UICONTROL 按定义的决策规则]** 拖放您选择的规则。

   ![](assets/offers-e2e-eligibility.png)

1. 填写 **[!UICONTROL 优先级]**. 在此示例中，添加 *25*.

1. 查看选件，然后单击 **[!UICONTROL 保存并批准]**.

   ![](assets/offers-e2e-review.png)

1. 在本例中，再创建三个具有相同表示但资源不同的选件。 为他们分配不同的规则和优先级，例如：

   * 第一个优惠 — 决策规则： *女性客户*，优先级： *25*
   * 第二个优惠 — 决策规则： *女性客户*，优先级： *15*
   * 第三个优惠 — 决策规则： *男性客户*，优先级： *25*
   * 第四个优惠 — 决策规则： *男性客户*，优先级： *15*

   ![](assets/offers-e2e-offers-created.png)

有关创建和配置优惠的详细步骤，请参见 [本节](../../using/offers/offer-library/creating-personalized-offers.md).

## 创建后备优惠 {#create-fallback}

1. 创建后备优惠.

1. 定义与优惠相同的呈现方式，并赋予相应的资产（这些资产应与优惠中使用的资产不同）。

   每个表示都必须是您之前创建的版面和资源的组合：

   * 一个对应于 *Web — 图像* 投放
   * 一个对应于 *电子邮件 — 图像* 投放
   * 一个对应于 *非数字 — 文本* 投放

   ![](assets/offers-e2e-fallback-representations.png)

1. 查看您的后备优惠，然后单击 **[!UICONTROL 保存并批准]**.

![](assets/offers-e2e-fallback.png)

您的后备优惠现已准备就绪，可用于决策。

有关创建和配置后备优惠的详细步骤，请参见 [本节](../../using/offers/offer-library/creating-fallback-offers.md).

## 创建收藏集 {#create-collection}

配置决策时，您需要将个性化优惠添加为收藏集的一部分。

1. 要加快决策过程，请创建动态收藏集。

1. 使用 *瑜伽* 收藏集限定符，用于选择您之前创建的四个个性化优惠。

   ![](assets/offers-e2e-collection-using-tag.png)

有关创建收藏集的详细步骤，请参见 [本节](../../using/offers/offer-library/creating-collections.md).

## 配置决策 {#configure-decision}

现在，您必须创建一个决策，以将投放位置与您刚刚创建的个性化优惠和备用优惠相结合。

决策引擎将使用此组合来查找特定用户档案的最佳优惠：在本例中，最佳优惠将基于您分配给每个优惠的优先级和决策规则。

要创建和配置优惠决策，请执行以下步骤：

1. 创建决策. 有关详细信息，请参阅[此部分](../../using/offers/offer-activities/create-offer-activities.md#create-activity)。

1. 选择 *Web — 图像*， *电子邮件 — 图像* 和 *非数字 — 文本* 投放位置。

   ![](assets/offers-e2e-decision-placements.png)

1. 对于每个投放位置，添加您创建的收藏集。

   ![](assets/offers-e2e-decision-collection.png)

1. 如果您在以下情况下定义排名： [构建组件](#define-components)，您可以将其分配给决策中的投放位置。 如果多个优惠符合在此投放位置中显示的条件，决策将使用此公式计算首先投放哪个优惠。

   有关将排名公式分配给投放位置的详细步骤，请参见 [本节](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. 选择您创建的后备优惠。 该选件将显示为三个选定投放位置的可用后备选件。

   ![](assets/offers-e2e-decision-fallback.png)

1. 查看您的决策，然后单击 **[!UICONTROL 保存并批准]**.

   ![](assets/offers-e2e-review-decision.png)

您的决策现已准备就绪，可用于提供优化和个性化的优惠。

有关创建和配置决策的详细步骤，请参见 [本节](../../using/offers/offer-activities/create-offer-activities.md).

## 在电子邮件中插入决策 {#insert-decision-in-email}

现在，您的决策已上线，您可以将其插入到电子邮件中。 为此，请按照中详述的步骤操作 [此页面](../../using/email/add-offers-email.md).

![](assets/offers-e2e-offers-displayed.png)
