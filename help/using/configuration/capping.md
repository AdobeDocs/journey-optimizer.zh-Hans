---
solution: Journey Optimizer
product: journey optimizer
title: API 上限
description: 了解如何使用上限API
feature: Journeys, API
role: User
level: Beginner
keywords: 外部， API，优化器，上限
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: ecb479f0875cfe1865a60667da6e2f84fad5044a
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 6%

---

# 使用上限API {#work}

上限API可帮助您创建、配置和监控上限配置。

本节提供有关如何使用API的全球信息。 [Adobe Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/)中提供了详细的API描述。

## API描述和Postman收藏集上限 {#description}

下表列出了用于上限API的可用命令。 [Adobe Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)中提供了请求示例、参数和响应格式的详细信息。

| 方法 | 路径 | 描述 |
|---|---|---|
| [!DNL POST] | list/endpointConfig | 获取端点上限配置的列表 |
| [!DNL POST] | /endpointConfigs | 创建端点上限配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | 部署端点上限配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | 取消部署端点上限配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | 检查是否可以部署端点上限配置 |
| [!DNL PUT] | /endpointConfigs/`{uid}` | 更新端点上限配置 |
| [!DNL GET] | /endpointConfigs/`{uid}` | 检索端点上限配置 |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | 删除端点封顶配置 |

创建或更新配置时，将自动执行检查以确保语法和有效负载的完整性。
如果发生某些问题，该操作将返回警告或错误，以帮助您更正配置。

此外，[此处](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json)还提供了一个Postman收藏集，帮助您进行测试配置。

此集合已设置为共享通过&#x200B;__[Postman控制台的集成](https://console.adobe.io/integrations) >尝试使用>下载Adobe I/O生成的Postman变量集合__，这将生成一个具有选定集成值的Postman环境文件。

下载并上传到 Postman 后，您需要添加三个变量：`{JO_HOST}`、`{BASE_PATH}` 和 `{SANDBOX_NAME}`。
* `{JO_HOST}` ： [!DNL Journey Optimizer]网关URL。
* `{BASE_PATH}` ： API的入口点。
* `{SANDBOX_NAME}`：标头 **x-sandbox-name**（例如，“prod”），对应将执行 API 操作的沙盒名称。有关更多信息，请参阅[沙盒概述](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hans)。

## 端点配置

以下是端点配置的基本结构：

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>**maxHttpConnections**&#x200B;参数是可选的。 它允许您限制Journey Optimizer将打开到外部系统的连接数。
>
>可以设置的最大值为400。 如果未指定任何内容，则系统可能会打开数千个连接，具体取决于系统的动态缩放情况。
>
>在部署上限配置时，如果未提供“maxHttpConnection”值，则会在部署的配置中添加默认的“maxHttpConnection = -1”，这意味着Journey Optimizer将使用默认的系统值。

示例：

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

## 警告和错误

调用&#x200B;**canDeploy**&#x200B;方法时，进程将验证配置并返回由其唯一ID标识的验证状态：

```
"ok" or "error"
```

潜在的错误包括：

* **ERR_ENDPOINTCONFIG_100**：配置上限：缺少URL或无效的URL
* **ERR_ENDPOINTCONFIG_101**：上限配置：错误的url
* **ERR_ENDPOINTCONFIG_102**：上限配置：格式错误的url：主机：端口中不允许使用url中的通配符
* **ERR_ENDPOINTCONFIG_103**：上限配置：缺少HTTP方法
* **ERR_ENDPOINTCONFIG_104**：上限配置：未定义调用等级
* **ERR_ENDPOINTCONFIG_107**：上限配置：无效的最大调用计数(maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**：上限配置：无效的最大调用计数(periodInMs)
* **ERR_ENDPOINTCONFIG_111**：上限配置：无法创建终结点配置：有效负载无效
* **ERR_ENDPOINTCONFIG_112**：上限配置：无法创建终结点配置：应为JSON负载
* **ERR_AUTHORING_ENDPOINTCONFIG_1**：无效的服务名称`<!--<given value>-->`：必须为“dataSource”或“action”

潜在的警告是：

**ERR_ENDPOINTCONFIG_106**：上限配置：未定义最大HTTP连接：默认情况下无限制

## 用例

本节列出了在[!DNL Journey Optimizer]中管理上限配置的关键用例，以及实施用例所需的相关API命令。

有关每个API命令的详细信息，请参见[API描述和Postman集合](#description)。

+++创建和部署新的上限配置

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`create`** — 创建新配置。
1. **`candeploy`** — 检查配置是否可以部署。
1. **`deploy`** — 部署配置。

+++

+++更新和部署上限配置（尚未部署）

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`get`** — 获取特定配置的详细信息。
1. **`update`** — 修改配置。
1. **`candeploy`** — 检查部署资格。
1. **`deploy`** — 部署配置。

+++

+++取消部署和删除已部署的上限配置

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`undeploy`** — 取消部署配置。
1. **`delete`** — 删除配置。

+++

+++只需一步即可删除已部署的上限配置

在仅一个API调用中，您可以使用`forceDelete`参数取消部署和删除配置。

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`delete`（带`forceDelete`参数）** — 强制在单个步骤中删除已部署的配置。

+++

+++更新已部署的上限配置

>[!NOTE]
>
>更新已部署的配置后需要进行重新部署。

要使用的API调用：
1. **`list`** — 检索现有配置。
1. **`get`** — 获取特定配置的详细信息。
1. **`update`** — 修改配置。
1. **`undeploy`** — 在应用更改之前取消部署配置。
1. **`candeploy`** — 检查部署资格。
1. **`deploy`** — 部署更新的配置。

+++
