---
title: 排名公式
description: 了解如何创建公式来对优惠进行排名
feature: Ranking, Decision Management
topic: Integrations
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 2%

---

# 排名公式 {#create-ranking-formulas}

## 关于排名公式 {#about-ranking-formulas}

**排名公式**&#x200B;允许您定义规则，这些规则将确定在给定投放位置应首先显示哪个优惠，而不是考虑优惠的优先级分数。

排名公式以&#x200B;**PQL语法**&#x200B;表示，可以利用配置文件属性、上下文数据和优惠属性。 有关如何使用PQL语法的更多信息，请参阅[专用文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hans)。

创建排名公式后，您可以将其分配给决策中的投放位置。 有关此内容的更多信息，请参阅[在决策中配置产品建议选择](../offer-activities/configure-offer-selection.md)。

## 创建排名公式 {#create-ranking-formula}

要创建排名公式，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 组件]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 排名]**&#x200B;选项卡。 默认情况下已选中&#x200B;**[!UICONTROL 公式]**&#x200B;选项卡。 此时将显示之前创建的公式列表。

   ![](../assets/rankings-list.png)

1. 单击&#x200B;**[!UICONTROL 创建排名]**&#x200B;以创建新的排名公式。

   ![](../assets/ranking-create-formula.png)

1. 指定公式名称、说明和公式。

   在本例中，我们希望在实际天气炎热时提高所有具有“hot”属性的选件的优先级。 为此，在决策调用中传递了&#x200B;**contextData.weather=hot**。 [了解如何使用上下文数据](../context-data.md)

   ![](../assets/ranking-syntax.png)

   >[!IMPORTANT]
   >
   >创建排名公式时，不支持回顾以前的时间段。 例如，如果您将上个月之内发生的体验事件指定为公式的一个组成部分。 在公式创建期间任何包含回顾期间的尝试将在保存公式时触发错误。

1. 单击 **[!UICONTROL Save]**。已创建排名公式，您可以从列表中选择该公式以获取详细信息并编辑或删除它。

   它现在可用于决策中，为投放位置排名符合条件的优惠（请参阅[在决策中配置优惠选择](../offer-activities/configure-offer-selection.md)）。

   ![](../assets/ranking-formula-created.png)

## 排名公式示例 {#ranking-formula-examples}

您可以根据需要创建许多不同的排名公式。 以下是一些示例。

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's audience membership

Boost the priority of offers based on whether the user is a member of a priority audience, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.get("prioritySegmentId")).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### 根据配置文件属性，提升具有特定优惠属性的优惠

如果配置文件住在选件对应的城市，则将该城市中所有选件的优先级加倍。

**排名公式：**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### 结束日期距现在不到24小时的Boost优惠

**排名公式：**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### 根据客户购买所提供产品的倾向提升优惠内容

您可以根据客户倾向得分提高选件的得分。

在此示例中，实例租户是&#x200B;*_salesvelocity*，并且配置文件架构包含存储在数组中的分数范围：

![](../assets/ranking-example-schema.png)

因此，对于用户档案，例如：

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

### 根据上下文数据提升优惠 {#context-data}

[!DNL Journey Optimizer]允许您根据调用中传递的上下文数据提升某些选件。 例如，如果传递了`contextData.weather=hot`，则必须提升所有带`attribute=hot`的选件的优先级。 有关如何使用&#x200B;**Edge Decisioning**&#x200B;和&#x200B;**Decisioning** API传递上下文数据的详细信息，请参阅[此部分](../context-data.md)

请注意，在使用&#x200B;**Decisioning** API时，上下文数据将添加到请求正文中的配置文件元素，如下面的示例所示。

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
    
}],
```

以下示例说明了如何在排名公式中使用上下文数据来提高优惠的优先级。 展开每个部分以获取有关排名公式语法的详细信息。

>[!NOTE]
>
>在Edge Decisioning API示例中，将`<OrgID>`替换为您的组织租户ID。

+++如果上下文数据中的渠道与客户首选的渠道匹配，则将优惠优先级提高10

>[!BEGINTABS]

>[!TAB 决策API]

`if (@{_xdm.context.additionalParameters;version=1}.channel.isNotNull() and @{_xdm.context.additionalParameters;version=1}.channel.equals(_abcMobile.preferredChannel), offer.rank.priority + 10, offer.rank.priority)`

>[!TAB Edge Decisioning API]

`if (xEvent.<OrgID>.channel.isNotNull() and xEvent.<OrgID>.channel.equals(_abcMobile.preferredChannel), offer.rank.priority + 10, offer.rank.priority)`

>[!ENDTABS]

+++

+++如果在调用中传递“contextData.weather=hot”，则提升具有“attribute=hot”的所有选件的优先级。

>[!BEGINTABS]

>[!TAB 决策API]

`if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull() and offer.characteristics.get("weather")=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)`

>[!TAB Edge Decisioning API]

`if (xEvent.<OrgID>.weather.isNotNull() and offer.characteristics.get("weather")=xEvent.<OrgID>.weather, offer.rank.priority + 5, offer.rank.priority)`

>[!ENDTABS]

+++

+++Content Origin Boost

>[!BEGINTABS]

>[!TAB 决策API]

`if (@{_xdm.context.additionalParameters;version=1}.contentorigin.isNotNull() and offer.characteristics.contentorigin=@{_xdm.context.additionalParameters;version=1}.contentorigin, offer.rank.priority * 100, offer.rank.priority)`

>[!TAB Edge Decisioning API]

`if (xEvent.<OrgID>.contentorigin.isNotNull() and offer.characteristics.contentorigin=xEvent.<OrgID>.contentorigin, offer.rank.priority * 100, offer.rank.priority)`

>[!ENDTABS]

+++

+++天气提速

>[!BEGINTABS]

>[!TAB 决策API]

`if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull() and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority * offer.characteristics.scoringBoost, offer.rank.priority)`

>[!TAB Edge Decisioning API]

`if (xEvent.<OrgID>.weather.isNotNull() and offer.characteristics.weather=xEvent.<OrgID>.weather, offer.rank.priority * offer.characteristics.scoringBoost, offer.rank.priority)`

>[!ENDTABS]

+++
