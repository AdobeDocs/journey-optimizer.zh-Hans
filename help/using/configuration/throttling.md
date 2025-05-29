---
solution: Journey Optimizer
product: journey optimizer
title: API 限制
description: 了解如何使用限制API
feature: Journeys, API
role: User
level: Beginner
keywords: 外部， API，优化器，上限
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: 60cb5e1ba2b5c8cfd0a306a589c85761be1cf657
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 48%

---

# 使用 API 限制

节流API可帮助您创建、配置和监视节流配置，以限制每秒发送的事件数。

本节提供有关如何使用API的全球信息。 [Adobe Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/)中提供了详细的API描述。

## 必读

* **每个组织一个配置：**&#x200B;当前每个组织只允许一个配置。 必须在生产沙盒上定义配置（通过标头中的`x-sandbox-name`提供）。
* **组织级别的应用程序：**&#x200B;在组织级别应用了配置。
* **API限制处理：**&#x200B;当达到API中设置的限制时，其他事件将排队等候最多6小时。 无法修改此值。
* **`maxHttpConnections`参数：**“maxHttpConnections”参数是可选参数，在Capping API中可用，仅允许您限制Journey Optimizer将打开到外部系统的连接数。 [了解如何使用上限API](../configuration/capping.md)

  如果要限制连接数，但同时限制这些外部调用，则可以在同一端点上配置两个配置，一个限制和一个限制。 两个配置可以针对一个端点共存。 要为节流端点设置“maxHttpConnections”，请使用节流API设置节流阈值，并使用上限API设置“maxHttpConnections”。 在调用上限API时，您可以将上限阈值设置为高于限制阈值的值，以便该上限规则实际上永远不会起作用。

## 限制API描述和Postman收藏集 {#description}

下表列出了用于限制API的可用命令。 [Adobe Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)中提供了请求示例、参数和响应格式的详细信息。

| 方法 | 路径 | 描述 |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | 获取限制配置列表 |
| [!DNL POST] | /throttlingConfigs | 创建限制配置 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | 部署限制配置 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | 取消部署限制配置 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | 检查是否可以部署限制配置 |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | 更新限制配置 |
| [!DNL GET] | /throttlingConfigs/`{uid}` | 检索限制配置 |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | 删除限制配置 |

此外，[此处](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json)还提供了一个Postman收藏集，帮助您进行测试配置。

此集合已设置为共享通过&#x200B;__[Postman控制台的集成](https://console.adobe.io/integrations) >尝试使用>下载Adobe I/O生成的Postman变量集合__，这将生成一个具有选定集成值的Postman环境文件。

下载并上传到 Postman 后，您需要添加三个变量：`{JO_HOST}`、`{BASE_PATH}` 和 `{SANDBOX_NAME}`。
* `{JO_HOST}` ： [!DNL Journey Optimizer]网关URL。
* `{BASE_PATH}` ： API的入口点。
* `{SANDBOX_NAME}`：标头 **x-sandbox-name**（例如，“prod”），对应将执行 API 操作的沙盒名称。有关更多信息，请参阅[沙盒概述](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hans)。

## 限制配置{#configuration}

以下是限制配置的结构。**name** 和 **description** 属性是可选项。

```
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

示例：

```
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

>[!IMPORTANT]
>
>只有在调用&#x200B;**部署**&#x200B;终结点后，配置才会处于活动状态。

## 错误

创建或更新配置时，该流程会验证给定配置并返回由其“唯一 ID”标识的验证状态，这可以是：

```
"ok" or "error"
```

>[!IMPORTANT]
>
>属性 **maxThroughput**、**urlPattern** 和 **methods** 是必填项。
>
>**maxThroughput** 的值必须在 200-5000 范围内。

创建、删除或部署限制配置时，可能会出现以下错误：

* **ERR_THROTTLING_CONFIG_100**：限制配置：`<mandatory attribute>`必需
* **ERR_THROTTLING_CONFIG_101**：限制配置：maxThroughput 是必填项，且必须大于或等于 200 且小于或等于 5,000
* **ERR_THROTTLING_CONFIG_104**：限制配置：格式错误的 URL 模式
* **ERR_THROTTLING_CONFIG_105**：限制配置：URL 模式的主机部分不允许使用通配符
* **ERR_THROTTLING_CONFIG_106**：限制配置：无效负载
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**，“无法删除已部署的限制配置。请在删除之前取消部署”
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**，“无法删除限制配置：发生意外错误”
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**，“无法部署限制配置：发生意外错误”
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**，“无法取消部署限制配置：发生意外错误”
* **THROTTLING_CONFIG_GET_ERROR: 1460**，“无法获取限制配置：发生意外错误”
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**，“无法更新限制配置：运行时版本处于不活动状态”
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**，“无法更新限制配置：发生意外错误”
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**，“禁止对限制配置执行操作：非生产沙盒”
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**，“无法创建限制配置：发生意外错误”
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**，“无法创建限制配置：仅允许为每个组织使用一个配置”
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466**，“无法部署限制配置：已部署”
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467**，“找不到限制配置”
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468**，“无法取消部署限制配置：尚未部署”

**错误示例**

尝试在非生产沙盒上创建配置时：

```
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

如果给定的沙盒不存在：

```
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

尝试创建其他配置时：

```
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## 运行时级别的配置生命周期 {#config}

取消部署配置后，该配置在运行时级别被标记为不活动，并且在 24 小时内将继续处理待处理事件。然后，会在运行时服务中删除它。

取消部署配置后，可以更新和重新部署配置。这将创建新的运行时配置，在即将执行的操作中将使用该配置。

更新已部署的配置时，会立即使用新值。底层系统资源将自动调整。与取消部署然后重新部署配置相比，这是最佳选择。

## 响应示例 {#responses}

**创建 - POST**

```
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**更新 - PUT**

```
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**读取（更新后）- GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**读取（部署后）- GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## 用例 {#uc}

本节列出了在[!DNL Journey Optimizer]中管理限制配置的关键用例，以及实施用例所需的相关API命令。

有关每个API命令的详细信息，请参见[API描述和Postman集合](#description)。

+++创建和部署新限制配置

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`create`** — 创建新配置。
1. **`candeploy`** — 检查配置是否可以部署。
1. **`deploy`** — 部署配置。

+++

+++更新和部署限制配置（尚未部署）

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`get`** — 获取特定配置的详细信息。
1. **`update`** — 修改配置。
1. **`candeploy`** — 检查部署资格。
1. **`deploy`** — 部署配置。

+++

+++取消部署和删除已部署的限制配置

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`undeploy`** — 取消部署配置。
1. **`delete`** — 删除配置。

+++

+++删除已部署的限制配置

在仅一个API调用中，您可以使用`forceDelete`参数取消部署和删除配置。

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`delete`（带`forceDelete`参数）** — 强制在单个步骤中删除已部署的配置。

+++

+++更新已部署的限制配置

>[!NOTE]
>
>在更新之前，无需取消部署配置

要使用的API调用：

1. **`list`** — 检索现有配置。
1. **`get`** — 获取特定配置的详细信息。
1. **`update`** — 修改配置。

+++
