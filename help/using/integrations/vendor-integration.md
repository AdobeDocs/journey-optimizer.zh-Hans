---
solution: Journey Optimizer
product: journey optimizer
title: 供应商集成
description: 将Adobe Journey Optimizer与任何公开有效API的外部平台以及经过工程测试的供应商模式集成，以便在您设计设置时提高信心。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 集成，供应商，第三方
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 10185
ht-degree: 5%

---

# 示例供应商配置 {#vendor-integration}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何将Adobe Journey Optimizer集成与任何公开兼容API的外部平台结合使用，以及操作护栏和说明性供应商模式来指导您的设置。

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

客户有责任确保其使用AJO集成功能及任何关联的第三方供应商或集成符合所有适用法律和法规，例如HIPAA。

>[!ENDSHADEBOX]

## 快速导航 {#quick-navigation}

使用这些分组链接快速跳转到相关的供应商模式：

* **内容管理系统：** [内容](#contentful)，[Sitecore](#sitecore)，[Salsify](#salsify)，[内容栈栈](#contentstack)，[Akeneo](#akeneo)，[Magnolia](#magnolia)
* **忠诚度和奖励：** [Voucherify](#voucherify)，[Talon.One](#talon-one)，[Antavo](#antavo)，[Salesforce忠诚度](#salesforce-loyalty)，[毛细管](#capillary)
* **模板、个性化和推荐：** [Stensul](#stensul)，[Marigold](#marigold)，[Adobe Target推荐](#adobe-target-recommendations)
* **数据、天气和操作：** [AccuWeather](#accuweather)，[ShipStation](#shipstation)，[RevenueCat](#revenuecat)，[数据库](#databricks)
* **评论、同意和社交：** [Bynder](#bynder)，[Trustpilot](#trustpilot)，[Bazaarvoice](#bazaarvoice)，[OneTrust](#onetrust)，[Meta](#meta)，[Aprimo](#aprimo)，[Epsilon (Epsilon3)](#epsilon)

## 内容和CMS {#content-and-cms}

### 有内容 {#contentful}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由Contentfied维护或正式支持的。 使用有内容的文档确认当前API详细信息。

>[!BEGINSHADEBOX]

“内容”是指用于通过REST或GraphQL进行的结构化条目和资产的Headless CMS，因此Journey Optimizer可以在发送或打开时提取内容。

典型用例包括电子邮件中本地化的主页块、替换文本和CTA，以及动态模块中的产品或促销条目。 另一种常见模式是按ID检索特定条目，以进行个性化消息传递。

>[!ENDSHADEBOX]

+++ 了解关于内容先决条件和限制的更多信息。

以下先决条件适用：

* 具有投放API访问和面向读取的API密钥的充满内容的空间。
* 清除内容类型和字段ID；可在Journey Optimizer中拥有管理员访问权限以创建集成。

以下限制和排除项适用：

* 广泛列出或分页的内容性API不适合此模式；首选针对特定条目或资产的检索调用。
* 回写同步或双向同步超出了此示例的范围。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用内容交付API和您的交付令牌配置&#x200B;**GET**，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用内容投放API (CDA) URL配置端点： `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. 选择HTTP方法： **GET**。

1. 添加身份验证。 将&#x200B;**`access_token`** **查询**&#x200B;参数设置为您的内容交付API令牌，如下面的&#x200B;**示例集成字段**&#x200B;所示。 内容还接受`Authorization: Bearer`标头中的相同令牌；使用您的集成字段支持的令牌。

1. 根据需要添加路径变量（例如，条目ID、区域设置）。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择个性化所需的字段。

1. 根据需要配置超时和缓存。

1. 测试连接并激活。

下表列出了此集成请求的示例值。

+++ 集成字段示例

集成字段示例（与共享空间和环境的[内容交付API](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"}一致）：

| 字段 | 值 |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/environments/{{environment_id}}/entries/{{entry_id}}` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |
| **HTTP方法** | `GET` |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |
| `entry_id` | `entry_id` | `<YOUR_ENTRY_ID>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | `access_token` | `<YOUR_API_KEY>` | 查询参数 |

+++

### Sitecore {#sitecore}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Sitecore维护或正式支持。 使用Sitecore文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Sitecore Content Hub和相关云API支持DAM样式的下载和元数据流；以下示例模式以ID下载订单为中心。

典型用例包括电子邮件内容中的资产或下载元数据，以及与Sitecore中管理的DAM工作流保持一致。

>[!ENDSHADEBOX]

+++ 详细了解Sitecore的先决条件和限制。

以下先决条件适用：

* 租户URL和凭据（每个API表面的持有者或令牌）。
* Journey Optimizer中的管理员访问权限以创建集成。

以下限制和排除项适用：

* 主机名和路径因Sitecore产品而异。 仅使用租户公开的端点。
* OAuth访问令牌、刷新和生命周期必须遵循Sitecore安全策略。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 在下载订单路径上配置&#x200B;**GET**，为每个Sitecore设置授权标头，从上下文映射`id`，粘贴示例JSON，映射字段，以及针对资源延迟调整超时。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Content Hub API配置端点（示例：按ID下载订单）。 示例URL模式：

   `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

在Journey Optimizer中配置此示例调用时，请使用以下字段。 在[Sitecore文档](https://doc.sitecore.com/){target="_blank"}中确认您的产品（Content Hub、XM Cloud等）的主机名和API版本。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |
| Authorization | Authorization | 常量 | 持有人`<token>` | 是（开） |
| If-Modified-Since | If-Modified-Since | Variable | 2019-08-24T14:15:22Z | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | X-Auth-Token | `<token>` | Header |

+++

### Salsify {#salsify}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Salsify维护或正式支持。 使用Salsify文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Salsify是一个PIM，具有用于产品、渠道和数字资产的API。

典型用例包括电子邮件中的产品属性或媒体URL，以及与联合目录数据一致的消息传送。

>[!ENDSHADEBOX]

+++ 详细了解Salsify的先决条件和限制。

以下先决条件适用：

* API令牌和组织上下文；可从配置文件或上下文解析的产品ID。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 非常大的目录：如果集成需要按实体进行检索，请避免使用批量列表端点。
* Salsify角色权限可限制属性可见性。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 与批量目录调用、设置持有者身份验证、粘贴示例JSON、映射字段、测试、激活相比，偏好使用单产品检索。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Salsify Product API配置端点。 示例URL模式：

   `https://api.salsify.com/v1/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

一些较旧的引用为Salsify重复使用了下载顺序样式路径；您的租户可能使用`https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}`或类似路径。 在[Salsify开发人员](https://developers.salsify.com/){target="_blank"}中确认。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认参数） | Content-Type | 常量 | application/json | 是（开） |
| Authorization | Authorization | 常量 | `Bearer <YOUR_TOKEN_HERE>` | 是（开） |
| If-Modified-Since | If-Modified-Since | Variable | 2019-08-24T14:15:22Z | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | `apiKey` | `<your_api_key>` | Header |

+++

### Contentstack {#contentstack}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Contentstack维护或正式支持。 使用Contentstack文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Contentstack是Headless CMS；REST投放是Journey Optimizer中JSON字段映射的典型方法。

典型用例是将横幅或促销的条目与包括区域设置的参数结合使用。

>[!ENDSHADEBOX]

+++ 详细了解Contentstack的先决条件和限制。

以下先决条件适用：

* 栈栈API密钥、投放令牌、环境名称和内容类型UID。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 此模式使用REST JSON进行字段映射；GraphQL交付遵循不同的集成路径。
* 使用适合生产的投放令牌；预览和发布的流不可互换。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 按Contentstack的要求添加`api_key`和`access_token`标头，包括`environment`查询参数，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用内容投放API配置端点。 示例URL模式：

   `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

集成字段示例。 请参阅[Contentstack内容交付API](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |
| 标头 | 无需额外的标头。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `content_type_uid` | 内容类型UID | `<your_content_type_uid>` |
| `entry_uid` | 登录UID | `<your_entry_uid>` |

**身份验证**

| 键名称 | 键值 | 添加至 |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

Contentstack需要&#x200B;**两个**&#x200B;密钥作为投放请求的标头。

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `environment` | 环境名称 | Variable | `<your_environment_name>` | 是（开） |

+++

### 阿赫尼奥 {#akeneo}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Akeneo维护或正式支持。 使用Akeneo文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Akeneo PIM会为产品、属性和媒体公开REST API。

典型用例包括电子邮件模块中受管理的产品数据和历程中给定渠道的属性。

>[!ENDSHADEBOX]

+++ 详细了解Akeneo的先决条件和限制。

以下先决条件适用：

* PIM基本URL和OAuth客户端；产品UUID或标识符策略。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* PIM响应可能会很大。 仅映射个性化所需的属性。
* 写操作不在典型的只读个性化示例的范围之内。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用带有持有者令牌的&#x200B;**GET**，在查询标记中仅请求所需的属性选项，粘贴示例JSON，映射最小属性集，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Akeneo REST API配置端点。 示例URL模式：

   `https://{pim-host}/api/rest/v1/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例模式：带有`Accept: application/json`的`https://{pim-host}/api/rest/v1/products-uuid/{uuid}`。 查看[Akeneo API](https://api.akeneo.com/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Authorization | Authorization | 常量 | `Bearer <YOUR_TOKEN>` | 是（开） |
| 接受 | 接受 | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | 包括属性选项 | Variable | 假 | 否（关闭） |
| `with_quality_scores` | 包括质量分数 | Variable | 假 | 否（关闭） |
| `with_completenesses` | 包括完整性 | Variable | 假 | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | Authorization | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### 木兰花 {#magnolia}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由木兰维护或正式支持的。 使用Magnolia文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Magnolia根据部署提供Headless和REST投放端点。

典型用例是为营销模块交付内容节点或片段。

>[!ENDSHADEBOX]

+++ 详细了解Magnolia的先决条件和限制。

以下先决条件适用：

* 实例URL和令牌或基本身份验证；用于投放的工作区和路径。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* REST投放URL取决于安装的Magnolia模块和配置。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用模块公开的公共投放URL模式，根据Magnolia指南进行身份验证（匿名投放与受保护内容的令牌），粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Magnolia REST（投放）配置端点。 示例URL模式：

   `https://{author-or-public}/.rest/delivery/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例模式： `https://{domain}/magnoliaAuthor/.rest/delivery/...`或公共投放导览样式的URL。 您的路径取决于已安装的模块。 请参阅[木兰文档](https://docs.magnolia-cms.com/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | 常量 | application/json | 是（开） |
| 接受 | 接受 | 常量 | application/json | 是（开） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | Authorization | `<bearer_token>` | Header |

注意：投放API对不需要登录的内容使用rest-anonymous角色。 要安全地访问受保护的数据，最好使用更可靠的方法，如API令牌或OAuth 2.0。

+++


## 忠诚度和奖励 {#loyalty-and-rewards}

### 武谢里菲 {#voucherify}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不受Voucherify维护或正式支持。 使用Voucherify文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Voucherify提供促销和忠诚度REST API（营销活动、优惠券、忠诚度计划）。

典型用例包括读取内容中选件的忠诚度或促销状态，以及在适当时显示层或平衡。

>[!ENDSHADEBOX]

+++ 详细了解Voucherify的先决条件和限制。

以下先决条件适用：

* 应用程序ID和密码（按区域/群集）；明确您呼叫的忠诚度或营销活动端点。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 避免在面向客户的错误或消息内容中暴露内部促销活动或营销活动标识符。
* 应用级别的速率限制适用。 根据验证指南配置重试和缓存。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 为群集设置基本URL，添加必需的标头(`X-APP-ID`， `X-APP-TOKEN`)，使用过滤器或ID约束列表端点，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用忠诚度/REST API配置端点。 根据[Voucherify](https://docs.voucherify.io/){target="_blank"}，为您的区域设置&#x200B;**群集**&#x200B;主机和路径。 示例URL模式：

   `https://{cluster}.voucherify.io/`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

集成字段示例。 完整引用： [Voucherify API](https://docs.voucherify.io/reference/introduction){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |
| X-APP-ID | X-APP-ID | 常量 | `<YOUR-APP-ID>` | 是（开） |
| X-Voucherify通道 | X-Voucherify通道 | 常量 | Voucherify文档 | 否（关闭） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | Variable | 10 | 否（关闭） |
| `page` | `page` | Variable | 1 | 否（关闭） |
| `customer` | `customer` | Variable | `<customer_identifier>` | 否（关闭） |
| `created_at` | `created_at` | Variable | `<iso8601_date>` | 否（关闭） |
| `updated_at` | `updated_at` | Variable | `<iso8601_date>` | 否（关闭） |
| `order` | `order` | Variable | `<sort_field>` | 否（关闭） |
| `code` | `code` | Variable | `<loyalty_card_code>` | 否（关闭） |
| `ids` | `ids` | Variable | `<array_of_ids>` | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### 爪子.One {#talon-one}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Talon.One维护或正式支持。 使用Talon.One文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Talon.One是一个促销和忠诚度规则引擎，带有REST API用于会话、效果和配置文件。

典型用例包括个性化内容中的购物车或个人资料级别的促销以及忠诚度进度或奖励显示。

>[!ENDSHADEBOX]

+++ 详细了解Talon.One的先决条件和限制。

以下先决条件适用：

* API密钥和特定于部署的基本URL；应用程序或营销活动范围的标识符。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 会话密集型流可能需要仔细映射到集成请求模型。
* 请遵守Talon.One速率限制和幂等指南。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 在所需的配置文件或成就路径上使用&#x200B;**GET**，按文档说明设置`Authorization: ApiKey-v1 <key>`，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Talon.One集成API配置端点。 示例URL模式：

   `https://{your-domain}.talon.one/v1/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **HTTP方法** | `GET` |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | Variable | 进行中/已完成/已过期 | 否（关闭） |
| `startDate` | `startDate` | Variable | 2024-05-29T15:04:05+07:00 | 否（关闭） |
| `endDate` | `endDate` | Variable | 2024-05-29T15:04:05+07:00 | 否（关闭） |
| `pageSize` | `pageSize` | Variable | `<default_page_size>` | 否（关闭） |
| `skip` | `skip` | Variable | `<items_to_skip>` | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | Authorization | ApiKey-v1 `<YOUR_API_KEY>` | Header |

+++

### 安塔沃 {#antavo}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由Antavo维护或正式支持的。 使用Antavo文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Antavo是一个企业忠诚度平台，具有用于成员、奖励和事件的REST API。

典型用例包括电子邮件或推送中的点数、层级或奖励，以及由忠诚度状态驱动的优惠。

>[!ENDSHADEBOX]

+++ 详细了解Antavo的先决条件和限制。

以下先决条件适用：

* 栈叠URL和API凭据；根据需要栈叠URL和API凭据；程序或商店标识符。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 客户PII必须根据Antavo协议和您的隐私政策进行处理。
* 使用Antavo为您的环境确认API版本和稳定的端点。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用供应商的身份验证（例如查询中的API密钥）配置&#x200B;**GET**，避免针对策略公开PII，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Antavo Enterprise API配置端点。

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例集成字段使用&#x200B;**暂存**&#x200B;主机；生产使用您的Antavo栈栈主机名。 请参阅[Antavo文档](https://antavo.com/docs/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |
| 接受 | 接受 | 常量 | application/json | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | `api_key` | `<YOUR_API_KEY>` | 查询参数 |

+++

### Salesforce忠诚度 {#salesforce-loyalty}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不受Salesforce维护或正式支持。 通过Salesforce文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Salesforce忠诚度管理在Salesforce平台上为成员、项目和交易公开REST API。

典型用例包括在历程中显示层、点或好处，以及根据CRM和忠诚度数据调整消息传递。

>[!ENDSHADEBOX]

+++ 了解有关Salesforce忠诚度的先决条件和限制的更多信息。

以下先决条件适用：

* Salesforce实例、连接的应用程序或集成用户，以及适用于您组织的OAuth。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 必须在集成中设计Salesforce API限制和OAuth令牌刷新。
* 字段级安全和共享规则可管理API响应中显示的字段。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用您的团队批准的忠诚度集成端点，完成Salesforce OAuth，粘贴示例JSON，映射字段，遵守复合API限制，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Salesforce忠诚度管理REST配置端点。 示例URL模式：

   `https://{instance}.salesforce.com/services/data/vXX.X/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

使用针对贵组织API版本记录的忠诚度管理&#x200B;**成员配置文件** GET操作；路径包括程序和成员标识符。 查看[Salesforce开发人员](https://developer.salesforce.com/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |
| 接受 | 接受 | 常量 | application/json | 否（关闭） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | Variable | `<membership_number>` | 否（关闭） * |
| `membershipId` | `membershipId` | Variable | `<membership_id>` | 否（关闭） * |
| `posMemId` | `posMemId` | Variable | `<pos_mem_id>` | 否（关闭） * |

\*至少需要三个中的一个。

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | Authorization | `<access_token>` | Header |

+++

### 毛细管 {#capillary}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不受毛细管的维护或正式支持。 使用毛细管文档确认当前API详细信息。

>[!BEGINSHADEBOX]

毛细血管提供零售栈栈中常见的忠诚度和参与API。

典型用例包括个性化历程中的点数、层或优惠。

>[!ENDSHADEBOX]

+++ 了解关于毛细管的先决条件和限制的更多信息。

以下先决条件适用：

* API主机和身份验证（通常为已签名的请求；遵循毛细管文档）。
* 端点的程序标识符。

以下限制和排除项适用：

* 身份验证方案和区域主机因部署而异。 用毛细管确认你的烟囱。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 根据需要配置标头，如`CAP-API-ACCESS-TOKEN`，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用毛细管API配置端点。

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例： `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}`（主机因地区而异）。 使用[毛细管](https://capillarytech.com/){target="_blank"}验证主机和身份验证方案。


| 字段 | 值 |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `reward_id` | 奖励ID | `<your_reward_id>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | 常量 | application/json | 是（开） |
| CAP-API-ACCESS-TOKEN | 访问令牌 | 常量 | `<YOUR_ACCESS_TOKEN>` | 是（开） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## 模板和消息传递 {#templates-and-messaging}

### 模板 {#stensul}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Stensul维护或正式支持。 使用Stensul文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Stensul是用于已批准模板的电子邮件创建平台；Journey Optimizer可以通过其API使用模板元数据和结构化区域。

典型用例包括导入已批准的模板并将区域映射到用户档案属性，以及为可伸缩的活动内部版本重用受管理的块。

>[!ENDSHADEBOX]

+++ 详细了解Stensul的先决条件和限制。

以下先决条件适用：

* 具有API访问权限的模板帐户，以及使用定义的令牌发布的模板。
* Journey Optimizer中的管理员访问权限以创建集成。

以下限制和排除项适用：

* 此处不介绍如何在Journey Optimizer中就地编辑模具模板的WYSIWYG。
* 模板有效负载中的大型或复杂HTML可能需要安全审查和整理。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入集成名称。

1. 使用模板模板API URL配置端点。 示例URL模式：

   `https://api.stensul.com/v1/templates/{template_id}`

1. 配置身份验证（根据模板API文档提供API密钥或OAuth）。

1. 定义路径变量，例如模板ID。

1. 粘贴用于字段检测的示例JSON响应。

1. 将所需的模板字段映射到Journey Optimizer个性化字段。

1. 测试连接并激活。

### 马里戈尔德 {#marigold}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Marigold维护或正式支持。 使用Marigold文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Marigold会公开忠诚度和参与度API；主机因地理位置而异（欧盟主机名与美国模块主机名）。

一个典型用例是使用Marigold项目的忠诚度或偏好数据扩充消息。

>[!ENDSHADEBOX]

+++ 详细了解Marigold的先决条件和限制。

以下先决条件适用：

* 合同中的基本URL和凭据；可能时，提供权限最低的API用户。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 端点因Marigold产品而异。 验证您的部署是否支持Marigold。
* 响应中的个人数据必须符合您的DPA和保留策略。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 指向您所在地区的Marigold主机，设置身份验证（下面的示例使用带有密钥和密码的`X-Api-Key`），粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Marigold REST API配置端点。

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

1. Marigold根据客户实例所在的地理区域使用2个端点：

   * 欧洲： `https://{{customername}}.module.slgnt.eu`
   * 美国： `https://{{customername}}.module.slgnt.us`

下表列出了此集成请求的示例值。

+++ 集成字段示例

基础主机依赖于区域（例如`https://{{customername}}.module.slgnt.eu`或`https://{{customername}}.module.slgnt.us`）。 使用Marigold为您的部署确认路径。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | X-Api-Key | `<apiKey>:<apiSecret>` | Header |

+++

### Adobe Target Recommendations {#adobe-target-recommendations}

>[!IMPORTANT]
>
>此配置是Adobe Journey Optimizer团队测试的说明性模式。 Adobe Target Recommendations是一个单独的Adobe产品，具有自身的发行周期和API版本控制。 在生产环境中部署之前，请始终通过[Adobe Target开发人员文档](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview)确认当前API详细信息。

>[!BEGINSHADEBOX]

Adobe Target包括适用于服务器端或集成体验的推荐和交付API，具体取决于权利。

典型用例包括将推荐注入您在Journey Optimizer中创作的体验，并将键与配置文件或Experience Platform上下文保持一致。

>[!ENDSHADEBOX]

+++ 详细了解Adobe Target推荐的先决条件和限制。

以下先决条件适用：

* 具有推荐的Target；IMS组织和支持的身份验证。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 推荐和投放API需要特定参数（例如mbox或产品标识符）。 请按照Adobe Target文档中的说明进行操作。
* 调整发送卷和用例的延迟和缓存。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 传递调用通常为带有JSON正文的&#x200B;**POST**。 按[目标身份验证](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication){target="_blank"}配置OAuth，粘贴示例响应，映射字段，在预期卷下测试。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Target推荐/交付API配置端点。

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| 策略 | 根据需要配置策略级别详细信息。 |
| **HTTP方法** | `POST` |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| 客户端 | 客户端 | Variable | `<customer_client_code>` | 是（开） |
| sessionId | sessionId | Variable | ` <session_identifier>` | 是（开） |

**身份验证**

请参阅[Target身份验证配置](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication)并将JSON添加到有效负载。

**请求有效负载**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## 数据、天气和操作 {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由AccuWeather维护或正式支持。 使用AccuWeather文档确认当前API详细信息。

>[!BEGINSHADEBOX]

AccuWeather会公开预测和位置REST API，以便消息可以包含天气感知代码片段。

典型用例包括电子邮件或推送中的简短预测，以及使用与用户档案或上下文关联的预测值定制内容。

>[!ENDSHADEBOX]

+++ 详细了解AccuWeather的先决条件和限制。

以下先决条件适用：

* API订阅和密钥；位置密钥或城市搜索流。
* Journey Optimizer中的管理员访问权限以创建集成。

以下限制和排除项适用：

* 确认AccuWeather订阅层的JSON响应形状；集成映射JSON响应中的字段。
* 观察AccuWeather速率限制和建议的缓存。
* 在预测调用之前，解决`locationKey`通常需要单独的地理位置或城市搜索请求。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 除非您的订阅另有要求，否则请使用&#x200B;**GET**，附加`apiKey`查询参数，映射`locationKey`和其他来自配置文件/上下文的变量，粘贴示例JSON，映射字段，然后进行测试。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用每日预测API配置端点。 示例URL模式：

   `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++集成字段示例

集成字段示例。 [AccuWeather API](https://developer.accuweather.com/apis){target="_blank"}中介绍了详细信息和层。 您通常通过单独的位置搜索调用（例如`.../locations/v1/cities/search?q={{cityName}}`）解析`locationKey`。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `format` | `format` | Variable | json | 否（关闭） |
| `language` | `language` | Variable | en-US | 否（关闭） |
| `details` | `details` | Variable | False | 否（关闭） |
| `metric` | `metric` | Variable | False | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | `apiKey` | `<YOUR_API_KEY>` | 查询参数 |

+++

### 船站 {#shipstation}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由ShipStation维护或正式支持的。 通过ShipStation文档确认当前API详细信息。

>[!BEGINSHADEBOX]

ShipStation为承运人、标签和跟踪提供配送和订单API。

典型用例包括事务型消息中的订单状态、跟踪链接或投放ETA。

>[!ENDSHADEBOX]

+++ 详细了解ShipStation的先决条件和限制。

以下先决条件适用：

* API密钥和密钥（按ShipStation文档的基本身份验证）。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 不要在消息内容中公开ShipStation API密钥；仅在集成配置中保留凭据。
* 分页列表端点可能不太适合集成；如果可能，首选单资源GET。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 定位您需要的资源（订单与装运），根据[ShipStation API](https://www.shipstation.com/docs/api/){target="_blank"}进行身份验证，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用ShipStation REST API配置端点。 示例URL模式：

   `https://ssapi.shipstation.com/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

以下&#x200B;**获取计时器**&#x200B;示例演示了一个ShipStation自动化计时调用。 在Journey Optimizer中重现时，请使用ShipStation集成指南中的确切路径和身份验证。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **HTTP方法** | `POST` |
| **策略** | 根据需要配置策略级别详细信息。 |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | apiKey | `<your_api_key>` | Header |

**请求有效负载**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### RevenueCat {#revenuecat}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由RevenueCat维护或正式支持。 通过RevenueCat文档确认当前API详细信息。

>[!BEGINSHADEBOX]

RevenueCat为应用程序提供订阅状态和授权API。

在策略允许的生命周期营销活动中，典型的用例是反映订阅状态。

>[!ENDSHADEBOX]

+++ 详细了解RevenueCat的先决条件和限制。

以下先决条件适用：

* 密钥API密钥和应用程序标识符；配置文件与RevenueCat客户ID之间的稳定映射。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 保护机密API密钥并遵循您的轮换策略。
* 订阅和授权数据是敏感的。 满足隐私和同意要求。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 调用下面建模的REST **GET**，使用密钥标头进行身份验证，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用RevenueCat REST API配置端点。 示例URL模式：

   `https://api.revenuecat.com/v1/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例模式：将RevenueCat的&#x200B;**从[RevenueCat文档](https://docs.revenuecat.com/){target="_blank"}获取产品** （或等效产品/权利GET）与项目的基本URL和版本一起使用。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | 否（关闭） |
| `locale` | `locale` | Variable | `<locale_code>` | 否（关闭） |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | Authorization | `Bearer <token>` | Header |

+++

### 数据块 {#databricks}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由Databricks维护或正式支持的。 使用数据库文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Databricks通过lakehouse数据提供SQL和REST API；较早的草案将语句执行指导与&#x200B;**jobs/get**&#x200B;示例相结合。

典型用例是使用受管表中的非规范化小属性，以便以严格的最低权限进行个性化。

>[!ENDSHADEBOX]

+++ 了解有关数据库先决条件和限制的更多信息。

以下先决条件适用：

* 每个组织策略的Workspace主机、令牌或OAuth；具有最小范围的服务主体。
* Journey Optimizer中的管理员访问权限。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 首选较窄的读取路径；如果您使用&#x200B;**POST**&#x200B;语句执行，请包括API所需的JSON主体，粘贴映射成功响应示例，仔细测试延迟，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Databricks SQL语句执行API配置端点。 示例URL模式：

   `https://{workspace-host}/api/2.0/sql/statements/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++集成字段示例

下面的&#x200B;**GET**&#x200B;作业示例具有说明性；对于SQL驱动的个性化，首选您的工作区支持的[语句执行API](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"}模式。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |
| 身份验证 | OAuth |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | Variable | `12` | 是 |

+++

## 审核、同意和社交 {#reviews-consent-and-social}

### Bynder {#bynder}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由Bynder维护或者正式支持的。 使用Bynder文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Bynder是一个具有REST API的DAM；集成通常使用OAuth 2.0作为只读元数据或资源URL。

典型用例包括将资产元数据或投放URL提取到消息中，以及使Bynder中的创意审批与历程保持一致。

>[!ENDSHADEBOX]

+++ 详细了解Bynder的先决条件和限制。

以下先决条件适用：

* 门户域和OAuth客户端（或批准的令牌方法）。
* 只读访问权限的范围；Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 分页和OAuth令牌刷新必须遵循Bynder的API规则。
* 大型分页响应：仅映射个性化所需的字段。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 在所选终结点上配置&#x200B;**GET**（一个常见模式是用户列表），按[Bynder](https://developer.bynder.com/){target="_blank"}完成OAuth，避免提取不必要的数据页面，映射字段，测试，然后激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Bynder API v4配置端点。 示例URL模式：

   `https://{your-bynder-domain}/api/v4/users/`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

集成字段示例。 有关OAuth 2.0有效负载的详细信息，请参阅[Bynder API文档](https://developer.bynder.com/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |
| Authorization | Authorization | 常量 | 持有人`<token>` | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | Variable | False | 否（关闭） |
| `limit` | `limit` | Variable | 100 | 否（关闭） |
| `page` | `page` | Variable | 1 | 否（关闭） |

**身份验证**

| 类型 | 负载 |
| --- | --- |
| OAuth 2.0 | OAuth 2.0有效负载（请参阅Bynder文档） |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Trustpilot维护或正式支持。 使用Trustpilot文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Trustpilot在您的用例和合同允许的情况下，为业务和审查摘要数据提供API。

一个典型用例是显示符合Trustpilot条款的营销内容中的审核计数或评级。

>[!ENDSHADEBOX]

+++ 详细了解Trustpilot的先决条件和限制。

以下先决条件适用：

* API密钥和批准的使用案例；用于查询的业务标识符。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 使用Trustpilot数据必须符合Trustpilot品牌和数据使用政策。
* 速率限制适用于审核摘要和相关端点。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用所需的查询身份验证配置&#x200B;**GET**，从配置文件或上下文映射标识符，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Trustpilot API配置端点。 示例URL模式：

   `https://api.trustpilot.com/v1/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

将[Trustpilot开发人员](https://developers.trustpilot.com/){target="_blank"}的类别列表操作用于您的集成模式；参数因资源而异。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | 否（关闭） |
| `locale` | `locale` | Variable | `<locale_code>` | 否（关闭） |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | apiKey | `<your_api_key>` | Header |

+++

### Bazaarvoice {#bazaarvoice}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Bazaarvoice维护或正式支持。 通过Bazaarvoice文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Bazaarvoice提供评级、评论和UGC API。

典型用例是在策略允许的情况下在电子邮件中显示审核摘要或评级。

>[!ENDSHADEBOX]

+++ 详细了解Bazaarvoice的先决条件和限制。

以下先决条件适用：

* 合同中的API密钥和客户端标识符。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 评级和评论的显示必须遵循Bazaarvoice内容策略。
* 速率限制和缓存规则适用于每个API密钥。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用带有`passkey`的&#x200B;**GET**&#x200B;作为对话API上的查询参数，设置`Accept: application/json`，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Bazaarvoice对话API配置端点。 示例URL模式：

   `https://api.bazaarvoice.com/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例入口点： `https://api.bazaarvoice.com/data/products.json`具有版本和筛选查询参数。 查看[Bazaarvoice开发人员](https://developer.bazaarvoice.com/){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常量 | application/json | 是（开） |

**身份验证**

| 类型 | 键值 | 位置 |
| --- | --- | --- |
| 密钥 | `<YOUR_ACCESS_TOKEN>` | 查询参数 |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | 常量 | 5.4 | 是（开） |
| `filter` | `filter` | Variable | Id:47950830 | 否（关闭） |
| `stats` | `stats` | Variable | 所有 | 否（关闭） |

+++

### OneTrust {#onetrust}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由OneTrust维护或正式支持。 使用OneTrust文档确认当前API详细信息。

>[!BEGINSHADEBOX]

OneTrust会公开隐私和同意API（产品特定的URL和架构）。

典型用例是在架构和法律审查允许的情况下读取条件内容的同意或偏好设置信号。

>[!ENDSHADEBOX]

+++ 了解有关OneTrust先决条件和限制的更多信息。

以下先决条件适用：

* API凭据和区域基本URL；对消息传递中使用的字段进行法律批准。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 同意和偏好设置数据受到严格监管。 与隐私和法律团队协调。
* API路径和负载因OneTrust产品而异。 使用订阅文档。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 使用发布的架构或首选项中心路径访问您的订阅文档，根据需要完成OAuth，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用OneTrust API配置端点。 你的租户、产品和路径来自你的订阅的[OneTrust](https://developer.onetrust.com/){target="_blank"}文档。 示例URL模式：

   `https://{tenant}.my.onetrust.com/api/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

| 字段 | 值 |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| **身份验证** | OAuth |

**路径参数**

| 参数 | 名称 | 值 |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `state` | `state` | 常量 | 已发布 | 是 |

+++

#### 首选项中心架构（已发布）

示例模式（片段）： `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`。 在[OneTrust Developer](https://developer.onetrust.com/){target="_blank"}中确认确切的路径。

### Meta {#meta}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不受Meta维护或正式支持。 通过Meta文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Meta图形和营销API为授权的业务集成公开目录和营销活动对象。

典型的用例是使用令牌和策略允许的Meta属性丰富内容。

>[!ENDSHADEBOX]

+++ 详细了解Meta的先决条件和限制。

以下先决条件适用：

* 具有正确权限的系统用户或应用程序令牌；Business Manager一致性。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 短期访问令牌需要适合服务器端集成的续订或长期策略。
* 遵守Meta平台条款；请勿在消息负载中记录令牌或其他密钥。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 图形调用通常是带有版本化路径的&#x200B;**GET**；处理令牌过期、粘贴示例JSON、映射字段、测试、激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Meta Graph API配置端点。 示例URL模式：

   `https://graph.facebook.com/vXX.X/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

集成字段示例。 有关版本控制和访问令牌，请参阅[Graph API](https://developers.facebook.com/docs/graph-api){target="_blank"}。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **HTTP方法** | `GET` |
| 响应有效负载 | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |
| 策略 | 根据需要配置策略级别详细信息。 |
| 身份验证 | OAuth |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | Variable | ID | 否 |
| `filter` | `filter` | Variable | — | 否 |

+++

### Aprimo {#aprimo}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不由Aprimo维护或正式支持。 通过Aprimo文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Aprimo将营销操作与用于记录、资源和元数据的DAM API整合在一起。

典型用例包括动态内容中已批准的记录或资产字段，以及受管控行业中已管理的DAM工作流。

>[!ENDSHADEBOX]

+++ 详细了解Aprimo的先决条件和限制。

以下先决条件适用：

* 租户URL和凭据（根据您的设置，为OAuth或API密钥）。
* Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* Aprimo字段级安全性必须与您在Journey Optimizer中映射的属性保持一致。
* 大型HAL或JSON负载：将映射字段限制为所需的最小值集。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 在所需的记录路径上使用&#x200B;**GET**，发送所需的标头（如`API-VERSION`），粘贴示例JSON（返回的HAL或JSON），映射最小字段集，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Aprimo DAM /记录API配置端点。 使用&#x200B;**租户**&#x200B;的API基本URL和记录路径（每个Aprimo）。 示例URL模式：

   `https://{tenant}.dam.aprimo.com/`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

| 字段 | 值 |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **HTTP方法** | `GET` |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |
| API版本 | API版本 | 常量 | 1 | 是（开） |
| 接受 | 接受 | 常量 | application/hal+json OR application/json | 否（关闭） |
| select-record | select-record | Variable | `<selection_type>` | 否（关闭） |
| select-record-field | select-record-field | Variable | `<field_list>` | 否（关闭） |
| 选择字段 | 选择字段 | Variable | `<field_selection>` | 否（关闭） |

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | Authorization | 持有人`<token>` | Header |

+++

### Epsilon (Epsilon3) {#epsilon}

>[!IMPORTANT]
>
>此配置示例由Adobe作为示例模式独立测试。 它不是由Epsilon维护或正式支持的。 通过Epsilon文档确认当前API详细信息。

>[!BEGINSHADEBOX]

Epsilon会根据企业协议公开API；基本URL和身份验证来自您的帐户团队（下面的“事件API”示例具有说明性）。

典型用例是通过支持的JSON API公开忠诚度或优惠属性。

>[!ENDSHADEBOX]

+++ 详细了解Epsilon (Epsilon3)的先决条件和限制。

以下先决条件适用：

* 来自Epsilon的凭据和端点；Journey Optimizer中的管理员访问权限。

以下限制和排除项适用：

* 端点和主机特定于客户。 如果没有来自Epsilon帐户团队的文档，请勿部署。

+++

使用以下过程可在Journey Optimizer中配置此集成。 查看&#x200B;**集成字段示例**&#x200B;以取得请求详细信息，并通过供应商文档确认这些值。

1. 关注[使用集成](integrations.md)。 不要猜测公共URL。 使用Epsilon中的规范，粘贴示例JSON，映射字段，测试，激活。

1. 在Journey Optimizer中，转到&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

1. 输入不带空格的集成名称。

1. 使用Epsilon API配置端点（根据集成规范）。 基本URL和资源路径由Epsilon帐户团队提供。 示例URL模式：

   `https://{your-instance}.epsilon3.io/api/...`

1. 选择配置表中显示的HTTP方法，通常为GET，除非另有说明。

1. 完全按照表和供应商文档中的指定配置身份验证（标头、查询参数或OAuth）。

1. 定义路径、查询和标头参数，并根据需要将变量映射到配置文件或上下文数据。

1. 粘贴示例JSON响应，以便可以检测和映射字段。

1. 选择在响应有效负载映射中进行个性化所需的字段。

1. 根据预期卷配置超时、重试和缓存策略。

1. 测试连接，然后激活集成。

下表列出了此集成请求的示例值。

+++ 集成字段示例

示例模式：带有`start`和`end`查询参数以及基于标头的API密钥的`https://{your-instance}.epsilon3.io/api/v1/planning/events`。 在生产之前使用Epsilon确认。

| 字段 | 值 |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **HTTP方法** | `GET` |
| **策略** | 根据需要配置策略级别详细信息。 |
| **响应有效负载** | 根据API响应，选择并配置要在创作期间使用的所需响应字段。 |

**路径参数**

| Path参数 | 名称 | 默认值 |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**标头**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| Content-Type（默认） | Content-Type | 常量 | application/json | 是（开） |

**查询参数**

| 参数 | 名称 | 类型 | 值 | 必需 |
| --- | --- | --- | --- | --- |
| `start` | `start` | Variable | 2019-08-24T14:15:22Z | 是（开） * |
| `end` | `end` | Variable | 2019-08-24T14:15:22Z | 是（开） * |
| `eventType` | `eventType` | Variable | 已计划/未计划 | 否（关闭） |
| `exclude_recurrences` | `exclude_recurrences` | Variable | true / false | 否（关闭） |

\*对于`eventType` = `unscheduled`是可选的，对于`exclude_recurrences` = `true`是可选的。

**身份验证**

| 类型 | API密钥名称 | API密钥值 | 位置 |
| --- | --- | --- | --- |
| API密钥 | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

