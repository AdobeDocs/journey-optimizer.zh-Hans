---
title: 使用Edge Decisioning API提供优惠
description: Adobe Experience Platform Web SDK允许您检索和渲染使用API或选件库创建的个性化选件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: b02981f2c0cf74c8dba657570157709bc422d94c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 3%

---


# 使用Edge Decisioning API提供优惠 {#edge-decisioning-api}

## 入门指南和先决条件 {#aep-web-sdk-overview-and-prerequisites}

的 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是一个客户端JavaScript库，它允许Adobe Experience Cloud客户通过Experience Platform边缘网络与Experience Cloud中的各种服务进行交互。

Experience PlatformWeb SDK支持在Adobe中查询个性化解决方案（包括决策管理），从而允许您检索和渲染使用API或选件库创建的个性化选件。 有关更多详细说明，请参阅 [创建优惠](../../get-started/starting-offer-decisioning.md).

可使用以下两种方法来实施Offer decisioning: [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). 一种方法是面向开发人员，需要了解网站和编程知识。 另一种方法是使用Adobe Experience Platform用户界面设置选件，该选件只需在HTML页面的标题中引用一个小脚本即可。

请参阅 [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) 有关如何使用Platform Web SDK提供个性化优惠的更多信息。

>[!NOTE]
>
>目前，在Adobe Experience Platform Web SDK中，决策管理的使用方式可供选定用户抢先体验。 并非所有IMS组织都能使用此功能。

## Adobe Experience Platform Web SDK  {#aep-web-sdk-overview-and-prerequisites}

Platform Web SDK取代了以下SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK未合并这些库，而是从头开始的一项新实施。 要使用它，您必须首先执行以下步骤：

1. 确保贵组织具有使用SDK的适当权限，并且您已正确配置了这些权限。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [配置数据流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) (位于您帐户的Adobe Experience Cloud中的数据收集选项卡中)。

1. 安装SDK。 可以使用多种方法来执行此操作，详情请参阅 [安装SDK页面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). 本页将继续介绍每种不同的实施方法。

要使用SDK，您必须具有 [模式](../../../start/get-started-schemas.md) 和 [数据流](../../../start/get-started-datasets.md) 定义。

<!-- ****TODO - Configure schema**** -->

要个性化选件，您必须单独配置个性化/配置文件。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

要配置SDK以进行Offer decisioning，请执行以下两个步骤之一：

## 选项1 — 使用Launch安装标记扩展和实施

对于编码体验可能较少的用户而言，此选项更易于使用。

1. [创建标记属性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [添加嵌入代码](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. 使用您通过从“Datastream”下拉菜单中选择配置而创建的数据流，安装和配置Platform Web SDK扩展。 请参阅 [扩展](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![配置扩展](../../assets/configure-sdk-extension.png)

1. 创建必需的 [数据元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). 您至少必须创建Platform Web SDK身份映射和Platform Web SDK XDM对象数据元素。

   ![标识映射](../../assets/sdk-identity-map.png)

   ![XDM 对象](../../assets/xdm-object.png)

1. 创建 [规则](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   添加Platform Web SDK发送事件操作，并将相关决策作用域添加到该操作的配置中

   ![渲染选件](../../assets/rule-render-offer.png)

   ![请求选件](../../assets/rule-request-offer.png)

1. [创建和发布](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) 包含您配置的所有相关规则、数据元素和扩展的库。

## 选项2 — 使用预建的独立版本手动实施

以下是使用Web SDK预建的独立安装使用Offer decisioning所需的步骤。 本指南假定这是您首次实施SDK，因此所有步骤可能不适用于您。 本指南还假定具有一些开发经验。

在选项2中包含以下JavaScript代码片段：上预建的独立版本 [本页](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 在 `<head>` HTML页面的部分。


## 限制

移动设备体验边缘工作流程当前不支持某些选件约束，例如上限。 上限字段值指定选件在所有用户中可显示的次数。 有关更多详细信息，请参阅 [向选件添加约束](../../offer-library/add-constraints.md#capping).
