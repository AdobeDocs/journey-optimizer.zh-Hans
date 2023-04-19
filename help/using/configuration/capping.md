---
solution: Journey Optimizer
product: journey optimizer
title: API 上限
description: 了解如何使用上限API
role: User
level: Beginner
keywords: 外部， API，优化器，上限
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 30%

---

# 使用上限API {#work}

上限API可帮助您创建、配置和监控上限配置。

本节提供有关如何使用API的全局信息。 有关API的详细描述，请参阅 [Adobe Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/).

## API描述上限

| 方法 | 路径 | 描述 |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | 获取端点上限配置的列表 |
| [!DNL POST] | /endpointConfigs | 创建端点上限配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | 部署端点上限配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | 取消部署端点上限配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | 检查是否可以部署端点上限配置 |
| [!DNL PUT] | /endpointConfigs/`{uid}` | 更新端点上限配置 |
| [!DNL GET] | /endpointConfigs/`{uid}` | 检索端点上限配置 |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | 删除入点上限配置 |

创建或更新配置后，将自动执行检查以保证有效负载的语法和完整性。
如果出现某些问题，操作会返回警告或错误，以帮助您更正配置。

## 端点配置

以下是端点配置的基本结构：

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

### 示例：

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "maxHttpConnections": 30000,
      "rating": {
        "maxCallsCount": 5000,
        "periodInMs": 1000
      }
    }
  },
  "orgId": "<IMS Org Id>"
}
```

## 警告和错误

当 **canDeploy** 方法调用时，该过程将验证配置并返回由其唯一ID标识的验证状态，其中任一ID:

```
"ok" or "error"
```

潜在错误包括：

* **ERR_ENDPOINTCONFIG_100**:上限配置：缺少或无效的url
* **ERR_ENDPOINTCONFIG_101**:上限配置：格式错误的url
* **ERR_ENDPOINTCONFIG_102**:上限配置：url格式错误：host:port中不允许在url中使用通配符
* **ERR_ENDPOINTCONFIG_103**:上限配置：缺少HTTP方法
* **ERR_ENDPOINTCONFIG_104**:上限配置：未定义呼叫评级
* **ERR_ENDPOINTCONFIG_107**:上限配置：最大调用计数无效(maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**:上限配置：最大调用计数无效(periodInMs)
* **ERR_ENDPOINTCONFIG_111**:上限配置：无法创建端点配置：无效负载
* **ERR_ENDPOINTCONFIG_112**:上限配置：无法创建端点配置：应为JSON有效负载
* **ERR_AUTHORING_ENDPOINTCONFIG_1**:无效的服务名称 `<!--<given value>-->`:必须是“dataSource”或“action”

潜在的警告是：

**ERR_ENDPOINTCONFIG_106**:上限配置：未定义的最大HTTP连接数：默认情况下不限制

## 用例

在此部分中，您将找到在中管理上限配置可执行的五个主要用例 [!DNL Journey Optimizer].

为帮助您进行测试和配置，可点击[此处](https://raw.githubusercontent.com/AdobeDocs/JourneyAPI/master/postman-collections/Journey-Orchestration_Capping-API_postman-collection.json)获取 Postman 集合。

此“Postman 集合”已设置为通过 __[Adobe I/O 控制台的集成](https://console.adobe.io/integrations) > 试用 > 为 Postman 下载__&#x200B;共享 Postman 变量集合，它会使用选定的集成值生成 Postman 环境文件。

下载并上传到 Postman 后，您需要添加三个变量：`{JO_HOST}`、`{BASE_PATH}` 和 `{SANDBOX_NAME}`。
* `{JO_HOST}`：[!DNL Journey Optimizer]网关 URL
* `{BASE_PATH}`：API 的入口点。
* `{SANDBOX_NAME}`：标头 **x-sandbox-name**（例如，“prod”），对应将执行 API 操作的沙盒名称。有关更多信息，请参阅[沙盒概述](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hans)。

在以下部分中，您将找到用于执行用例的 Rest API 调用排序列表。

用例n°1: **创建和部署新的上限配置**

1. list
1. create
1. candeploy
1. deploy

用例n°2: **更新和部署尚未部署的上限配置**

1. list
1. get
1. update
1. candeploy
1. deploy

用例n°3: **取消部署和删除已部署的上限配置**

1. list
1. undeploy
1. delete

用例n°4: **删除已部署的上限配置。**

在仅一个 API 调用中，您可以使用 forceDelete 参数取消部署和删除配置。
1. list
1. 删除，使用 forceDelete 参数

用例n°5: **更新已部署的上限配置**

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
