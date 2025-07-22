---
solution: Journey Optimizer
product: journey optimizer
title: 使用来自外部端点的数据个性化内容
description: 了解如何从外部端点动态获取数据以个性化入站内容。
badge: label="有限发布版" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---


# 使用来自外部端点的数据个性化内容 {#data-endpoint}

>[!AVAILABILITY]
>
>此功能仅适用于一组组织（限量发布）。

Journey Optimizer允许您利用外部端点的数据，对入站渠道（如基于代码的体验、Web和应用程序内消息渠道）中的内容进行个性化。

为此，个性化编辑器中提供了专用辅助函数`externalDataLookup`。 要使用帮助程序，必须首先定义一个[!DNL Journey Optimizer] **操作**，您可以在其中配置有关外部端点的详细信息。

## 必读

### 运行时执行

当入站操作包含externalDataLookup帮助程序时，将会在[!DNL Adobe Experience Platform] Edge Network收到并处理个性化请求时动态调用端点。 这意味着外部端点需要能够处理的并发负载和吞吐量至少与客户端为给定表面向AEP Edge Network发送的并发负载和吞吐量相同。

### 身份验证

externalDataLookup帮助程序当前不支持操作配置中的身份验证选项。
同时，对于基于API密钥的身份验证或其他纯文本授权密钥，您可以在操作配置中将它们指定为标头字段。
仅适用于Adobe内部端点：联系AJO工程部门以启用端点的基于服务令牌的身份验证。

### 护栏和限制

另请参阅AJO入站渠道营销活动和历程中#GuardrailsandGuidelines自定义操作。

默认情况下，AJO在调用外部端点时使用300毫秒的超时。 请联系AJO工程部门以增加端点的此超时。
在Personalization编辑器中，当您插入表达式时，AJO不允许您浏览端点响应的架构，并且不会验证表达式中使用的响应对JSON属性的引用。
要通过externalDataLookup帮助程序替换的有效负载变量参数支持的数据类型是String、Integer、Decimal、Boolean、listString、listInt、listInteger、listDecimal
对操作配置所做的更改不会反映在实时营销活动和历程中的相应externalDataLookup调用中。 为了反映更改，您需要复制或修改任何在externalDataLookup帮助程序中使用操作的实时活动或历程。
尚不支持在外部数据查找帮助程序参数中使用变量。
当前不支持动态URL路径。   — 入站自定义操作增强#DynamicPathSegments

## 创建操作

创建操作以配置查找的端点。 每个端点只需执行一次此操作，应由技术用户执行。 请参阅此页面。

在&#x200B;**[!UICONTROL 自定义操作]**&#x200B;活动中和`externalDataLookup`帮助程序函数中，可以使用相同的操作获取历程中的内容，在历程或营销活动中的入站操作中获取数据。

浏览到&#x200B;**[!UICONTROL 管理]** / **[!UICONTROL 配置]**&#x200B;菜单。

记下操作ID并复制它以在步骤6中使用。


## 使用获取的数据个性化您的内容

### 将辅助函数添加到您的内容

1. 创建入站营销活动或历程操作并编辑其内容。

1. 找到您要在其中使用从外部端点获取的数据的内容并访问个性化编辑器。

1. 选择辅助函数菜单，然后找到`externalDataLookup`辅助函数。

1. 选择将关联的语法插入到您的代码中，并按如下方式替换`actionId`和`result`参数值：

   * `actionId` ：粘贴创建操作时复制的action nID。
   * `result`：将此参数设置为您选择的名称。 您将使用此结果变量来访问获取的内容。

1. 添加任何要在端点调用中传递的变量参数值。 例如，下面是如何传递语言参数和max items参数的。

### 使用获取的数据进行个性化

要访问从外部端点查找调用获取的数据，您可以使用个性化表达式和帮助程序函数引用操作定义中响应有效载荷中定义的字段。

使用`result`变量访问获取的数据并将其插入到集客操作的内容中。 例如，下面显示了如何返回从端点获取的项目的JSON数组。

让我们举个以下示例，其中操作中的响应有效负载已进行如下配置：

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Personalization示例1 — 在基于代码的Experience HTML操作中显示第一个视频的描述：

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Personalization示例2 — 在基于代码的Experience JSON操作中返回项数组：

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## 超时和错误处理

AJO在调用外部端点时使用严格的超时，以保持AEP Edge Network的低延迟、高吞吐量的性能特征。

如果端点超时或存在任何其他类型的错误到达端点，则结果变量将为空。 在这种情况下，对结果变量中属性的任何引用也将为空。 如果您只是在内容中显示属性，则会显示为空白。 如果尝试循环遍历结果中的数组属性，则不会返回任何项。

如果您希望通过显示回退内容来更正常地处理超时或错误，则可以检查查找结果是否为空，并在该情况下显示回退内容。

例如，您可以为单个属性显示一个回退值，如下所示：

第一个视频描述： {%=result.videos[0].description ？： &quot;none found&quot; %}


或者，您可以有条件地呈现整个内容块，如下所示：

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if result%}
...对结果执行操作……
{%else%}
...返回后备内容……
{%/if%}
调试
为帮助进行调试，外部数据查找的超时和错误详细信息包含在AEP Assurance的Edge Delivery视图中。 如果在入站操作中未看到externalDataLookup帮助程序的预期结果，则可启动Assurance会话，从Web或移动设备实施启动AJO调用，并使用Edge Delivery视图检查超时或错误详细信息。

例如：

在执行详细信息中，在保障跟踪的Edge Delivery部分下添加了新的customActions块，

请求和响应详细信息类似于以下内容。 如果在执行自定义操作时出现任何问题，则错误部分将有助于进行调试

## 常见问题

+++如何将上下文属性作为参数从请求传递到外部数据查找？

使用上下文属性>数据流>事件菜单浏览您所使用的体验事件架构，并将相关属性作为参数值插入，如下所示：

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++AJO是否执行任何外部端点响应缓存？

当前不是。 此功能将在将来受支持。

+++









语法
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



传递参数
调用外部端点时，将使用Action配置中给定的值发送在Action中定义的所有常量标头值、查询参数和请求有效负载值。

对于任何变量标头值、查询/路径参数或请求有效负载值，您可以使用参数将值动态传递到externalDataLookup帮助程序。

参数名称：

标题参数：标题。&lt;parameter-name>
查询参数：查询。&lt;parameter-name>
有效负载参数：有效负载。&lt;parameter-name>
路径参数：dynamic_path。&lt;parameter-name>
例如：

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
参数值可以是固定值，也可以通过引用配置文件字段或其他上下文属性对其进行个性化，例如：

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
可以使用点表示法提供有效负荷参数以引用嵌套的JSON属性，例如：

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}