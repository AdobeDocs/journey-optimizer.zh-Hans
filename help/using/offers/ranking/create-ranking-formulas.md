---
title: 排名公式
description: 了解如何创建公式来对优惠进行排名
feature: Ranking, Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: baf76d3c571c62105c1f0a59e07ca70e61a83cc6
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 3%

---

# 排名公式 {#create-ranking-formulas}

## 关于排名公式 {#about-ranking-formulas}

**排名公式**&#x200B;允许您定义规则，这些规则将确定在给定投放位置应首先显示哪个优惠，而不是考虑优惠的优先级分数。

排名公式以&#x200B;**PQL语法**&#x200B;表示，可以利用配置文件属性、上下文数据和优惠属性。 有关如何使用PQL语法的更多信息，请参阅[专用文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hans)。

创建排名公式后，您可以将其分配给决策中的投放位置。 有关此内容的更多信息，请参阅[在决策中配置优惠选择](../offer-activities/configure-offer-selection.md)。

## 创建排名公式 {#create-ranking-formula}

要创建排名公式，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 组件]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 排名]**&#x200B;选项卡。 默认情况下已选中&#x200B;**[!UICONTROL 公式]**&#x200B;选项卡。 此时将显示之前创建的公式列表。

   ![](../assets/rankings-list.png)

1. 单击&#x200B;**[!UICONTROL 创建排名]**&#x200B;以创建新的排名公式。

   ![](../assets/ranking-create-formula.png)

1. 指定公式名称、说明和公式。

   在本例中，我们希望在实际天气炎热时提高所有具有“hot”属性的选件的优先级。 为此，在决策调用中传递了&#x200B;**contextData.weather=hot**。

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

### 根据上下文数据提升具有特定优惠属性的优惠

根据决策调用中传递的上下文数据提升某些选件。 例如，如果在决策调用中传递`contextData.weather=hot`，则必须提升所有带`attribute=hot`的优惠的优先级。

**排名公式：**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.get("weather")=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

请注意，使用决策API时，上下文数据将添加到请求正文中的配置文件元素，如下面的示例所示。

**请求正文中的代码片段：**

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

选件将包含&#x200B;*propensityType*&#x200B;的属性，该属性与得分中的类别匹配：

![](../assets/ranking-example-propensityType.png)

然后，您的排名公式可以将每个优惠的优先级设置为等于该&#x200B;*propensityType*&#x200B;的客户&#x200B;*propensityScore*。 如果未找到得分，请使用在选件中设置的静态优先级：

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.get("propensityType"), false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
