---
solution: Journey Optimizer
product: journey optimizer
title: 集合管理函数
description: 了解集合管理函数中的数据类型
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 查询，集合，函数，有效负荷，历程
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
source-git-commit: 8e020f79e0f44e6fc804fcceb149146f9644c777
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 3%

---

# 集合管理函数 {#collection-management-functions}


## 关于查询收集函数

表达式语言还引入了一组查询集合的函数。 这些职能说明如下。

在以下示例中，我们使用包含集合的事件有效负载：

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

## all(`<condition>`)函数

**[!UICONTROL all]**&#x200B;函数使用布尔表达式在给定集合上启用过滤器的定义。

```json
<listExpression>.all(<condition>)
```

例如，在所有应用程序用户中，您可以使用IOS 13(布尔表达式“IOS 13==使用的应用程序”)获取这些用户。 此函数的结果是包含与布尔表达式匹配项目的过滤列表（例如：应用程序用户1、应用程序用户34、应用程序用户432）。

在数据Source条件活动中，您可以检查&#x200B;**[!UICONTROL all]**&#x200B;函数的结果是否为null。 您还可以将此&#x200B;**[!UICONTROL 所有]**&#x200B;函数与其他函数（如&#x200B;**[!UICONTROL count]**）组合。 有关详细信息，请参阅[数据Source条件活动](../condition-activity.md#data_source_condition)。


>[!CAUTION]
>
>不支持在历程表达式/条件中使用体验事件。 如果您的用例需要使用体验事件，请考虑替代方法。 [了解详情](../exp-event-lookup.md)

### 示例 1

我们要检查用户是否已安装了应用程序的特定版本。 为此，我们将获得与版本为1.0的移动应用程序关联的所有推送通知令牌。然后，我们使用&#x200B;**[!UICONTROL count]**&#x200B;函数执行一个条件，以检查返回的令牌列表是否至少包含一个元素。

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
>* 当&#x200B;**all()**&#x200B;函数中的筛选条件为空时，筛选器将返回列表中的所有元素。 **但是，要计算集合的元素数，不需要all函数。
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

**[!UICONTROL at]**&#x200B;函数允许您根据索引引用集合中的特定元素。
索引0是集合的第一个索引。

_`<listExpression>`.at(`<index>`)_

### 示例

此表达式返回列表的第二个推送通知令牌。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}`
```

结果为`token_2`。