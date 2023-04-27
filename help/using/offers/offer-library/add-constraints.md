---
title: 向选件添加约束
description: 了解如何定义要显示的选件的条件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 17%

---

# 向选件添加约束 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="关于优惠约束"
>abstract="通过约束，您可以指定与其他优惠相比，该优惠如何确定优先级并呈现给用户。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="关于优惠约束"
>abstract="通过约束，您可以指定与其他优惠相比，该优惠如何确定优先级并呈现给用户。"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="关于优惠优先级"
>abstract="在此字段中，您可以指定优惠的优先级设置。优先级是一个数字，用于对满足所有约束（例如资格、日期和上限）的优惠进行排名。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="设置优先级"
>abstract="如果用户有资格获得多个优惠，则优先级有助于定义该优惠相对于其他优惠的优先级。优惠的优先级越高，与其他优惠相比其优先级就越高。"

利用约束，可定义显示选件的条件。

1. 配置 **[!UICONTROL 选件资格]**. [了解详情](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定义 **[!UICONTROL 优先级]** 选件（如果用户符合多个选件的条件）。 优惠的优先级越高，与其他优惠相比其优先级就越高。

   ![](../assets/offer-priority.png)

1. 指定选件的 **[!UICONTROL 上限]**，即显示选件的次数。 [了解详情](#capping)

   ![](../assets/offer-capping.png)

1. 单击 **[!UICONTROL 下一个]** 以确认您定义的所有约束。

例如，如果设置以下约束：

![](../assets/offer-constraints-example.png)

* 仅对与“金牌忠诚度客户”决策规则匹配的用户考虑选件。
* 选件的优先级设置为“50”，这意味着选件将在优先级为1到49的选件之前和优先级为至少51的选件之后显示。
* 该选件将在所有版面中每月仅向每位用户显示一次。

## 资格 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定义资格"
>abstract="默认情况下，任何配置文件都有资格获得优惠，但您可以使用区段或决策规则将优惠限制为特定的配置文件。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="关于优惠资格"
>abstract="在此部分中，您可以使用决策规则来确定哪些用户有资格享受优惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="观看演示视频"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="对配置文件的总体估计"
>abstract="当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。"

的 **[!UICONTROL 选件资格]** 部分允许您将选件限制为使用区段或决策规则定义的特定用户档案。

>[!NOTE]
>
>了解有关使用的更多信息 **区段** 与 **决策规则** in [此部分](#segments-vs-decision-rules).

* 默认情况下， **[!UICONTROL 所有访客]** 选项，这意味着任何用户档案都有资格获得该选件。

   ![](../assets/offer-eligibility-default.png)

* 您还可以将选件的呈现方式限制为一个或多个选件的成员 [Adobe Experience Platform区段](../../segment/about-segments.md).

   为此，请激活 **[!UICONTROL 属于一个或多个区段的访客]** 选项，然后从左侧窗格添加一个或多个区段，并使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 逻辑运算符。

   ![](../assets/offer-eligibility-segment.png)

* 如果要关联特定 [决策规则](../offer-library/creating-decision-rules.md) 在选件中，选择 **[!UICONTROL 按定义的决策规则]**，然后将所需的规则从左侧窗格拖入 **[!UICONTROL 决策规则]** 的上界。

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >中当前不支持基于事件的选件 [!DNL Journey Optimizer]. 如果您根据 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}，则无法在选件中利用它。

当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。单击 **[!UICONTROL 刷新]** 更新数据。

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>如果规则参数包含不在配置文件中的数据（如上下文数据），则配置文件估计不可用。 例如，要求当前天气为≥80度的资格规则。

### 使用区段和决策规则 {#segments-vs-decision-rules}

要应用约束，您可以将选件的选择限制为一个或多个选件的成员 **Adobe Experience Platform区段**，或者您可以使用 **决策规则**，两个解决方案对应于不同的使用情况。

基本上，区段的输出是用户档案列表，而决策规则是在决策过程中针对单个用户档案按需执行的函数。 下面详述了这两种用法之间的差异。

* **区段**

   一方面，区段是一组Adobe Experience Platform用户档案，这些用户档案根据用户档案属性和体验事件与特定逻辑进行匹配。 但是，选件管理不会重新计算区段，在显示选件时，该区段可能不是最新的。

   了解有关 [此部分](../../segment/about-segments.md).

* **决策规则**

   另一方面，决策规则基于Adobe Experience Platform中可用的数据，并确定可向谁显示选件。 在选件中选择或为给定版面做出决策后，每次做出决策时都会执行规则，以确保每个用户档案都获得最新和最佳选件。

   了解有关 [此部分](creating-decision-rules.md).

## 上限 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="关于优惠上限"
>abstract="在此字段中，可指定可呈现优惠的次数。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用上限"
>abstract="为避免过度招揽客户，请使用上限定义可呈现优惠的最大次数。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html#capping-change-date" text="更改日期可能会影响上限"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="设置上限频率"
>abstract="您可以选择每天、每周或每月重置优惠上限计数器。请注意，保存优惠后，您将无法更改所选频率。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="印象"
>abstract="仅入站频道可将印象用作上限事件。"

上限用作约束，以定义选件可显示的最大次数。

通过限制用户获得特定选件的次数，您可以避免过度取悦客户，从而使用最佳选件优化每个接触点。

要设置上限，请执行以下主要步骤。

1. 确保 **[!UICONTROL 包含上限]** 切换按钮。 默认情况下包含上限。

   >[!CAUTION]
   >
   >无法启用或禁用之前创建选件的频率上限。 为此，您需要复制选件或创建一个新选件。

1. 定义 **[!UICONTROL 上限事件]** 将考虑增加计数器。 [了解详情](#capping-event)

1. 设置选件可以显示的次数。 [了解详情](#capping-count)

1. 选择是要将上限应用于所有用户还是仅应用于一个用户档案。 [了解详情](#capping-type)

1. 设置 **[!UICONTROL 频率]** 定义重置上限计数的频率。 [了解详情](#frequency-capping)

1. 如果您定义了 [表示](add-representations.md) 为选件指定是否要应用上限 **[!UICONTROL 跨所有版面]** 或 **[!UICONTROL 对于每个版面]**. [了解详情](#placements)

1. 保存并批准后，如果向选件显示您根据标准和您定义的时间范围在此字段中指定的次数，则其交付将停止。

在准备电子邮件时计算建议使用选件的次数。 例如，如果您准备发送一封包含大量选件的电子邮件，则无论是否发送了这封电子邮件，这些数量都将计入您的最大上限。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>当选件过期或选件开始日期后2年（以先到者为准）时，上限计数器将重置。 了解如何在 [此部分](creating-personalized-offers.md#create-offer).

### 上限事件 {#capping-event}

的 **[!UICONTROL 上限事件]** 字段，用于定义 **[!UICONTROL 上限事件]** 将考虑以增加计数器：

![](../assets/offer-capping-event.png)

* **[!UICONTROL 决策事件]** （默认值）：显示选件的最大次数。
* **[!UICONTROL 展示]**:向用户显示选件的最大次数。

   >[!NOTE]
   >
   >可以使用展示次数作为上限事件 **入站频道** 仅。

* **[!UICONTROL 点击次数]**:用户可点击选件的最大次数。
* **[!UICONTROL 自定义事件]**:您可以定义一个自定义事件，用于限制已发送的选件数量。 例如，您可以限制赎回次数，直到它们等于10000或给定用户档案已赎回1次为止。 为此，请使用 [Adobe Experience Platform XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"} 构建自定义事件规则的架构。

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

   在以下示例中，您需要限制结帐次数。

   1. 选择 **[!UICONTROL 自定义事件]** 并使用 **[!UICONTROL 添加自定义事件]** 按钮。

      ![](../assets/offer-capping-custom-event-add.png)

   1. 使用 **[!UICONTROL 创建自定义事件规则]** 生成器来选择相关事件。 您可以选择要为选件设置上限的任何用户操作。

      在此处选择 **[!UICONTROL 商务]** > **[!UICONTROL 结账]** > **[!UICONTROL 值]** 选择 **[!UICONTROL 存在]** 从下拉列表中。

      ![](../assets/offer-capping-custom-event.png)

   1. 创建规则后，该规则会显示在 **[!UICONTROL 自定义事件查询]** 字段。

      ![](../assets/offer-capping-custom-event-query.png)

>[!CAUTION]
>
>对于除决策事件之外的所有上限事件，可能不会自动收集决策管理反馈，这可能会导致上限计数器无法正确递增。 [了解详情](../data-collection/data-collection.md)
>
>要确保在上限计数器中跟踪每个上限事件并对其进行计数，请确保用于收集体验事件的架构包含该事件的正确字段组。 [了解详情](../data-collection/schema-requirement.md)

### 上限计数 {#capping-count}

的 **[!UICONTROL 上限计数]** 字段，可指定选件的显示次数。

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>数字必须是大于0的整数。

例如，您定义了自定义上限事件，如结账次数。 如果您在 **[!UICONTROL 上限计数]** 字段，则在10次结帐后将不再发送任何选件。

### 上限类型 {#capping-type}

您还可以指定希望在所有用户中还是将上限应用于一个特定配置文件：

![](../assets/offer-capping-total.png)

* 选择 **[!UICONTROL 合计]** 定义在组合目标受众中可建议选件多少次，即在所有用户中。

   例如，如果您是一家电子产品零售商，并且有一项“电视门卫交易”，则您希望在所有用户档案中仅返回选件200次。

* 选择 **[!UICONTROL 每个用户档案]** 定义向同一用户建议选件的次数。

   例如，如果您是拥有“白金信用卡”选件的银行，则您不希望此选件在每个用户档案中显示超过5次。 事实上，您认为如果用户查看了选件5次而未对其执行操作，则他们更有机会对下一个最佳选件执行操作。

### 频次上限 {#frequency-capping}

的 **[!UICONTROL 频率]** 部分允许您定义重置上限计数的频率。 为此，请定义计数的时间段（每日、每周或每月），并输入您选择的天/周/月数。

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>重置在您定义的日期(UTC)早上12点进行，或在一周/月的第一天（如果适用）进行。 周的开始日是星期日。 您选择的任何持续时间都不能超过2年（即相应的月、周或天数）。

例如，如果希望每两周重置一次上限计数，请选择 **[!UICONTROL 每周]** 从 **[!UICONTROL 重复]** 下拉列表和类型 **2** 中。 重置将每隔一个星期日（世界协调时）中午12点进行。

>[!CAUTION]
>
>保存选件后，您将无法更改为该频率选择的时间段（每月、每周或每天）。

### 上限和版面 {#placements}

如果您定义了 [表示](add-representations.md) 为选件指定是否要应用上限 **[!UICONTROL 跨所有版面]** 或 **[!UICONTROL 对于每个版面]**.

![](../assets/offer-capping-placement.png)

* **[!UICONTROL 跨所有版面]**:上限计数将总计与选件关联的版面中的所有决策。

   例如，如果选件具有 **电子邮件** 版面和 **Web** 的上限，并在 **所有版面中的每个用户档案2个**，则无论使用何种版面组合，每个用户档案总共可收到选件2次。

* **[!UICONTROL 对于每个版面]**:上限计数将单独对每个版面应用决策计数。

   例如，如果选件具有 **电子邮件** 版面和 **Web** 的上限，并在 **每次投放的每个用户档案2个**，则每个用户档案最多可收到选件2次（用于电子邮件投放），另外2次（用于Web投放）。

### 更改日期对上限的影响 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="更改日期可能会影响上限"
>abstract="如果此优惠具有上限，则在更改开始或结束日期时可能会影响该上限。"

更改选件日期时，您必须继续小心，因为如果满足以下条件，这可能会对上限产生影响：

* 该选件是 [已批准](#review).
* [上限](#capping) 已应用于选件。
* 按用户档案定义上限。

>[!NOTE]
>
>了解如何在 [此部分](creating-personalized-offers.md#create-offer).

每个配置文件的上限存储每个配置文件的上限计数。 当您更改已批准选件的开始和结束日期时，某些配置文件的上限计数可能会根据下面描述的不同方案而受到影响。

![](../assets/offer-capping-change-date.png)

以下是 **更改选件开始日期**:

| 方案：<br>如果…… | 会发生什么情况：<br>那么…… | 对上限计数的可能影响 |
|--- |--- |--- |
| ...在原始选件开始日期开始之前更新选件开始日期， | ...上限计数将从新开始日期开始。 | 否 |
| ...新的开始日期在当前结束日期之前， | ...上限将继续保留新的开始日期，并且每个用户档案的上一个上限计数将继续。 | 否 |
| ...新开始日期晚于当前结束日期， | ...当前上限将过期，并且新上限计数将从新开始日期所有用户档案的0开始。 | 是 |

以下是 **延长优惠结束日期**:

| 方案：<br>如果…… | 会发生什么情况：<br>那么…… | 对上限计数的可能影响 |
|--- |--- |--- |
| ...在原始选件结束日期之前，发生决策请求， | ...将更新上限计数，并且每个用户档案的上一个上限计数将结转。 | 否 |
| ...在原始结束日期之前，不会发出决策请求， | ...上限计数将在每个用户档案的原始结束日期重置。 随后，对于将在原始结束日期之后发生的任何新决策请求，新的上限计数将从0重新开始。 | 是 |

**示例**

假设您有一个选件，且原始开始日期设置为 **1月1日**，过期 **1月31日**.

1. 将显示用户档案X、Y和Z。
1. 开 **1月10日**，则选件的结束日期将更改为 **2月15日**.
1. **从1月11日至1月31日**，则仅会显示选件Z。

   * 因为决策请求在原始结束日期之前发生 **对于配置文件Z**，则选件的结束日期可延长到 **2月15日**.
   * 但是，由于在的原始结束日期之前未发生任何活动 **用户档案X和Y**，其计数器将过期，其上限计数将在 **1月31日**.

![](../assets/offer-capping-change-date-ex.png)
