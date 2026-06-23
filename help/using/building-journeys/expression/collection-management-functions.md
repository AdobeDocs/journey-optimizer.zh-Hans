---
solution: Journey Optimizer
product: journey optimizer
title: 集合管理函数
description: 了解集合管理函数中的数据类型
feature: Journeys
role: Developer
level: Experienced
keywords: 查询，集合，函数，有效负荷，历程
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sNFI7l-UMGmRV2wRcvYa56tILLoWFxXeG3N5txgrUiw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 1%

---

# 集合管理函数 {#collection-management-functions}


## 关于查询收集函数

表达式语言还引入了一组查询集合的函数。 这些职能说明如下。

在以下示例中，我们使用名为“LobbyBeacon”的事件，该事件包含推送通知令牌的集合。 此页面上的示例使用如下所示的事件有效负载结构：

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

>[!NOTE]
>
>在以下示例中，此有效负载是使用`@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}`引用的，其中“LobbyBeacon”是事件名称，并且路径的其余部分对应于上面显示的结构。

## all(`<condition>`)函数

**[!UICONTROL all]**&#x200B;函数使用布尔表达式在给定集合上启用过滤器的定义。

```json
<listExpression>.all(<condition>)
```

**概念示例：**&#x200B;在所有应用程序用户中，您可以使用IOS 13（布尔表达式“用于IOS 13==的应用程序”）获取这些用户。 此函数的结果是包含与布尔表达式匹配项目的过滤列表（例如：应用程序用户1、应用程序用户34、应用程序用户432）。

在数据Source条件活动中，您可以检查&#x200B;**[!UICONTROL all]**&#x200B;函数的结果是否为null。 您还可以将此&#x200B;**[!UICONTROL 所有]**&#x200B;函数与其他函数（如&#x200B;**[!UICONTROL count]**）组合。 有关详细信息，请参阅[数据Source条件活动](../conditions.md#data_source_condition)。

**使用LobbyBeacon有效负载的代码示例：**

以下示例使用本页顶部显示的事件有效负载。


>[!CAUTION]
>
>不支持在历程表达式/条件中使用体验事件。 如果您的用例需要使用体验事件，请考虑替代方法。 [了解详情](../exp-event-lookup.md)

### 示例 1

我们要检查用户是否已安装了应用程序的特定版本。 为此，我们将获得与版本为1.0的移动应用程序关联的所有推送通知令牌。 然后，我们使用&#x200B;**[!UICONTROL count]**&#x200B;函数执行一个条件，以检查返回的令牌列表是否至少包含一个元素。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

结果为true。

### 示例 2

此处，我们使用&#x200B;**[!UICONTROL count]**&#x200B;函数来检查集合中是否有推送通知令牌。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


结果为true。


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

表达式的结果为&#x200B;**3**。


>[!NOTE]
>
>* 当&#x200B;**all()**&#x200B;函数中的筛选条件为空时，筛选器将返回列表中的所有元素。 **但是，为了计算集合的元素数，不需要all函数。**
>
>* `currentEventField`仅在处理事件集合时可用，`currentDataPackField`在处理数据源集合时可用，`currentActionField`在处理自定义操作响应集合时可用。
>
>  处理具有`all`、`first`和`last`的集合时，我们会逐个循环该集合的每个元素。 `currentEventField`、`currentDataPackField`和`currentActionField`对应于正在循环的元素。


## 第一个(`<condition>`)和最后一个(`<condition>`)函数

**[!UICONTROL first]**&#x200B;和&#x200B;**[!UICONTROL last]**&#x200B;函数在返回满足筛选条件的列表的第一个/最后一个元素时，也启用集合上的筛选条件的定义。

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### 示例 1

此表达式返回与版本为1.0的移动应用程序关联的第一个推送通知令牌。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

结果为`token_1`。

### 示例 2

此表达式返回与版本为1.0的移动应用程序关联的最后一个推送通知令牌。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

结果为`token_2`。

## at(`<index>`)函数

**[!UICONTROL at]**函数允许您根据索引引用集合中的特定元素。
索引0是集合的第一个索引。

_`<listExpression>`.at(`<index>`)_

### 示例

此表达式返回列表的第二个推送通知令牌。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

结果为`token_2`。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;此页记录了历程高级表达式编辑器中使用的`all()`、`first()`、`last()`和`at()`集合管理函数，如推送通知令牌有效负载示例所示。

**意图：**

* 使用带有`all(<condition>)`的布尔条件筛选事件或数据源字段集合
* 使用`count()`与集合函数组合对已过滤或未过滤的集合元素进行计数
* 使用`first()`或`last()`检索集合的第一个或最后一个匹配元素
* 使用`at(<index>)`访问特定从零开始的索引处的集合元素
* 了解哪个循环变量(`currentEventField`、`currentDataPackField`、`currentActionField`)应用于每个集合上下文

**术语表：**

* **all(condition)**：筛选集合并返回与给定布尔表达式&#x200B;*（产品特定）*&#x200B;匹配的所有项
* **first(condition)**：返回集合中与条件&#x200B;*（产品特定）*&#x200B;匹配的第一个（体验事件的最近一个）元素
* **last(condition)**：返回集合中与条件&#x200B;*（产品特定）*&#x200B;匹配的最后一个（体验事件的最旧）元素
* **at(index)**：返回集合&#x200B;*（产品特定）*&#x200B;的指定从零开始的索引处的元素
* **currentEventField**：循环变量仅在迭代事件集合&#x200B;*（产品特定）*&#x200B;时可用
* **currentDataPackField**：循环变量仅在迭代数据源集合&#x200B;*（产品特定）*&#x200B;时可用
* **currentActionField**：循环变量仅在迭代自定义操作响应集合&#x200B;*（产品特定）*&#x200B;时可用

**护栏：**

* 不支持在历程表达式/条件中使用体验事件；请考虑替代方法，例如计算属性
* `currentEventField`、`currentDataPackField`和`currentActionField`仅在其各自的集合上下文中可用
* 不需要使用`all`函数来计算集合元素 — 可以直接将`count()`应用于字段路径
* 以空条件调用`all()`时，将返回集合中的所有元素

**术语：**

* 规范名称：集合管理函数 — 首字母缩略词：none — 变体：集合函数、查询集合函数
* 同义词： &quot;all()&quot; = &quot;collection filter function&quot;； &quot;at()&quot; = &quot;index accessor&quot;
* 请勿混淆： `first()` （最近体验事件）≠常规列表中第一个插入的元素

**常见问题解答：**

* **问：具有空条件的`all()`与具有条件的`all()`之间有何区别？**  — 空的`all()`返回每个元素；基于条件的`all()`仅返回与该布尔表达式匹配的元素。
* **问：如何在不使用`all()`的情况下计算推送通知令牌？**  — 直接在令牌字段路径中调用`count()`，例如`count(@event{LobbyBeacon...pushNotificationTokens.token})`。
* **问：当循环访问数据源集合时，我应使用哪个变量来引用当前元素？**  — 在数据源集合的`all()`、`first()`或`last()`中使用`currentDataPackField`。
* **问：如何获取收藏集中的第二个项目？**  — 使用`at(1)`，因为索引0是第一个元素。
* **问：为什么`last()`返回最早的体验事件？**  — 体验事件以逆时间顺序存储，因此集合中的最后一个位置对应于最早的事件。

+++
