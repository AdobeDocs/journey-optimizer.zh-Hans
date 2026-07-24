---
title: 创建自定义渠道
description: 了解如何使用渠道生成器在Adobe Journey Optimizer中创建和配置自定义渠道。
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="有限发布版" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '1538'
ht-degree: 15%

---


# 设置一个自定义渠道 {#create-custom-channel}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_settings"
>title="关于自定义渠道"
>abstract="自定义渠道允许 Adobe Journey Optimizer 通过您自己的 API 端点向外部系统发送个性化消息。 定义常规属性、端点、身份验证和负载，然后测试和激活您新的自定义渠道。 完成后，您就可以使用它来创建渠道配置，使营销人员可以在历程和营销活动中使用它。"
>additional-url="" text="开始使用自定义渠道"

<!--Contextual help final location TBC (here or in Settings subsection-->

要在营销活动和历程中使用自定义渠道，管理员必须首先创建渠道。 这涉及定义端点、身份验证、限制策略和消息有效负载结构。

**渠道生成器**&#x200B;部分是定义新自定义渠道的中心界面。 <!--It is accessible to users with the **[!UICONTROL Administrator]** role. -->它使您能够创建和配置自定义渠道，还可以管理API凭据和委派子域。

>[!IMPORTANT]
>
>要访问Channel Builder、创建和管理自定义渠道，您必须具有&#x200B;**查看自定义渠道**&#x200B;和&#x200B;**管理自定义渠道**&#x200B;权限。<!--[Learn more](../administration/high-low-permissions.md)--> 在[本节](../administration/permissions.md)中了解如何管理权限。

## 访问和管理自定义渠道 {#access-channel-builder}

要访问&#x200B;**渠道生成器**&#x200B;并管理您的自定义渠道，请执行以下步骤。

1. 在左侧导航边栏中转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。

1. 在&#x200B;**[!UICONTROL 渠道生成器]**&#x200B;部分中选择&#x200B;**[!UICONTROL 自定义渠道]**。

   ![自定义渠道清单](assets/custom_channels_inventory.png){width="70%"}

1. 清单列出沙盒中的所有自定义渠道，包括其当前状态和用于连接到外部端点的身份验证类型。

1. 您可以按创建自定义渠道的状态（**草稿**、**活动**&#x200B;或&#x200B;**已存档**）筛选自定义渠道，并按名称搜索。

1. 要编辑渠道，请在清单中单击渠道名称，进行更改并保存。 对于活动渠道，您只能编辑某些字段 — [了解更多](#test-activate)。

   >[!CAUTION]
   >
   >修改活动渠道上的限制或重试设置会立即对所有正在进行的和未来的执行生效。

1. 若要存档渠道，请从清单中打开它，然后单击&#x200B;**[!UICONTROL 存档]**。

   存档活动渠道会将其从所有选择下拉列表（营销活动操作选择器、历程操作调色板、编排的营销活动渠道列表、渠道配置和内容模板）中删除。 已使用该渠道的现有历程和营销活动继续正常运行。

## 创建自定义渠道 {#create-channel}

要创建新的自定义渠道，请执行以下步骤。

1. 单击&#x200B;**[!UICONTROL 创建自定义渠道]**&#x200B;按钮以打开渠道创建表单。 首先定义自定义渠道的常规设置。

   ![常规设置](assets/custom_channel_properties.png){width="70%"}

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;部分中，为您的自定义渠道输入&#x200B;**[!UICONTROL 名称]**。 此名称将显示在历程画布、营销活动操作选择器和编排的营销活动渠道列表中。

   >[!NOTE]
   >
   >名称必须是唯一的，以字母(A-Z)开头，仅包含字母数字字符或特殊字符( _， .， -)，并且应大于1个字符。

1. 您可以从默认图标库中选择图标，或从计算机中选择SVG文件。

   >[!NOTE]
   >
   >文件不能大于150KB。

   此图标将显示在历程画布中的渠道名称旁边。 如果未上传图标，则使用默认图标。

1. 输入可选的&#x200B;**[!UICONTROL 描述]**。

<!--
1. Optionally, assign **[!UICONTROL Access labels]** to restrict access to this channel based on data usage policies. Learn more
-->

## 设置端点配置 {#endpoint-configuration}

您必须配置端点，它是外部消息传递系统的HTTP URL。 当某个用户档案在营销活动或历程中符合条件时，[!DNL Journey Optimizer]使用个性化有效负载向此端点发送POST请求。

![终结点配置](assets/custom_channel_endpoint_configuration.png){width="70%"}

1. 在&#x200B;**[!UICONTROL 终结点配置]**&#x200B;部分中，输入外部消息传递系统的主机&#x200B;**[!UICONTROL URL]**。

   <!--The HTTP method to is currently set to **POST**.-->

   >[!IMPORTANT]
   >您的外部消息传递系统必须公开[!DNL Journey Optimizer]可以通过HTTP POST调用的HTTPS端点。 端点必须：
   >
   >* 接受您的渠道定义的有效负载格式(JSON)。
   >* 支持Channel Builder中提供的身份验证方法之一。 [了解详情](#authentication-settings)
   >* 返回HTTP 2xx响应以确认成功收到请求。

1. 根据需要添加&#x200B;**[!UICONTROL 标头]**。 标头是在HTTP请求级别传输的键值对。 它们与发送到端点的每个请求一起发送，通常用于身份验证令牌、内容类型规范或外部系统所需的任何其他元数据。

   <!--At minimum, `Content-Type` and `Charset` are available as default headers.-->

   ![标头配置](assets/custom_channel_endpoint_headers.png)

   对于每个标头，您可以定义其值是否为：

   * **[!UICONTROL 常量]** — 一个静态值，设置一次并包含在每个请求中。 例如，您可以定义值为`application/json`的`Content-Type`参数或值为`UTF-8`的`Charset`参数。
   * **[!UICONTROL 变量]** — 如果在此处输入了默认值，则除非在渠道配置中覆盖该默认值，否则将使用该默认值。 例如，您可以为在运行时解析的用户ID定义一个变量。 [了解详情](custom-channel-configuration.md) <!--From Custom actions section: For these parameters, you can define where to get this information (example: events, data sources), pass values manually or use the advanced expression editor for advanced use cases. Advanced uses cases can be data manipulation and other function usage. Refer to this [page](expression/expressionadvanced.md).-->

1. （可选）使用相同的常量/变量模式添加&#x200B;**[!UICONTROL 查询参数]**。 查询参数在投放时附加到端点URL。 常量参数始终使用相同的值添加；变量参数在发送时解析，例如，从用户档案传递用户标识符。

   ![查询参数](assets/custom_channel_endpoint_query_param.png){width="70%"}

1. 在&#x200B;**[!UICONTROL 策略配置]**&#x200B;部分中，定义[!DNL Journey Optimizer]如何处理请求吞吐量和失败。 这对于确保外部系统能够处理大量请求并避免其过多非常重要。

   ![策略配置](assets/custom_channel_endpoint_policy_config.png)

   * **[!UICONTROL 启用节流]** — 默认情况下处于禁用状态。 设置每秒的最大请求数（默认值： **5,000c**）。 一旦达到限制，请求就会排队并尽快发送。
   * **[!UICONTROL 启用重试]** — 默认启用。 为失败的请求设置最大重试计数（默认值： **3**，可配置的范围： 0-10）。 这有助于避免在瞬态失败期间使端点不堪重负。
   * **[!UICONTROL 超时]** — 默认值： **5,000毫秒**。设置考虑请求失败之前等待端点响应的最长时间。
     <!--* **[!UICONTROL Enable cache]** – Disabled by default. Set the caching duration (default TTL: **600 seconds**). After the TTL (Time To Live) expires, the next request is sent to the endpoint. Caching is useful for endpoints that return the same response for identical requests, reducing load and improving performance.-->

## 身份验证设置 {#authentication-settings}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_authentication"
>title="定义身份验证类型"
>abstract="身份验证可确保只有经过授权的请求才能发送给您的外部消息传递系统。 您可以从多种身份验证方法中进行选择，包括 API 密钥、基本身份验证和 OAuth 2.0。 激活后，Adobe Journey Optimizer 会自动为渠道生成一组初始 API 凭据，在 API 凭据库存中可以管理这些凭据。 但是，即使您可以稍后更改凭据，也必须在此处提供身份验证详细信息，以测试与您的端点的连接，然后才能激活渠道。"
>additional-url="" text="了解有关 API 凭据的更多信息"

选择您需要用于此渠道的&#x200B;**[!UICONTROL 身份验证类型]**。 可用的选项取决于外部消息传递系统支持的身份验证方法。

![身份验证类型](assets/custom_channel_authentication_type.png){width="70%"}

提供端点所需的身份验证详细信息。

* **[!UICONTROL 无]** — 发送请求时没有凭据。
* **[!UICONTROL API密钥]** — 提供密钥名称、值和位置（查询参数或标头）。
* **[!UICONTROL 基本身份验证]** — 提供用户名和密码。
* **[!UICONTROL OAuth 2.0]** — 为OAuth 2.0身份验证配置有效负载。
  <!--* **[!UICONTROL Custom]** – Define the authentication configuration using a JSON payload.-->

当身份验证类型不是&#x200B;**None**&#x200B;时，[!DNL Journey Optimizer]会在激活此渠道时自动为其生成初始API凭据集。 您可以在API凭据清单中更改这些凭据并创建新凭据。 [了解详情](custom-channel-api-credentials.md) <!--TBC-->

但是，在激活渠道之前，需要此处提供身份验证详细信息以测试与端点的连接。 **[!UICONTROL 测试连接]**&#x200B;按钮可用于验证身份验证设置。 [了解详情](#test-activate)

## 负载配置 {#payload-configuration}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_payload_config"
>title="启用渠道配置的字段"
>abstract="启用以后，此列中的字段将显示在渠道配置中，允许管理员为每个配置设置不同的值（例如，为每个品牌或区域设置不同的发件人 ID）。 这对于那些可能因营销活动或历程的上下文而不同的字段非常有用，例如发件人信息或消息模板。"
>additional-url="" text="在自定义渠道配置中配置动态参数"

<!--Create a page on Custom channel config to explain how to use the payload in a channel configuration.-->

当配置文件在营销活动或历程中符合条件时，有效负载会被发送到端点。

在有效负载配置中，定义消息有效负载的结构以及营销人员可以创作和个性化的字段。

1. 单击&#x200B;**[!UICONTROL 定义有效负载]**，然后选择如何定义有效负载：

   * **[!UICONTROL 粘贴示例JSON有效负载]** — 粘贴一个具有代表性的JSON对象，然后[!DNL Journey Optimizer]自动推断该对象中的架构。
   * **[!UICONTROL 导入JSON架构]**（即将推出） — 上传完整的JSON架构文件。

     >[!AVAILABILITY]
     >
     >此功能尚不可用。 它将在未来版本中添加。

1. 生成架构后，[!DNL Journey Optimizer]在表单视图中显示所有检测到的字段。

   ![](assets/custom_channel_payload_configuration.png)

1. 对于每个字段，请配置以下设置：

   | 设置 | 描述 |
   | --- | --- |
   | **[!UICONTROL 默认值]** | 可选。 如果在创作时未提供个性化值，则使用。 |
   | **[!UICONTROL 类型]** | 只读，从有效负载派生。 支持的类型： `string`、`integer`、`decimal`、`boolean`、`dateTime`、`dateTimeOnly`、`dateOnly`、`listObject`、`listString`、`listInteger`、`listDecimal`、`listBoolean`、`listDateTime`、`listDateTimeOnly`、`listDateOnly`。 |
   | **[!UICONTROL 必需]** | 如果启用，则在营销活动或历程中使用渠道时，字段必须具有值。 缺少必填字段会触发阻止激活的验证错误。 |
   | **[!UICONTROL 频道配置]** | 如果启用，该字段将显示在渠道配置中，允许管理员为每个配置设置不同的值（例如，为每个品牌或区域设置不同的发件人ID）。 [了解如何操作](custom-channel-configuration.md) |

   嵌套字段使用点表示法表示（例如，`image.id`）。<!--TBC-->

## 测试和激活 {#test-activate}

当渠道处于&#x200B;**[!UICONTROL 草稿]**&#x200B;状态时，使用屏幕顶部的&#x200B;**[!UICONTROL 测试连接]**&#x200B;按钮向您的端点发送测试请求并验证端到端连接。

![测试连接按钮](assets/custom_channel_test_connection.png){width="70%"}

检查外部系统的日志，确认已收到具有预期身份验证和有效负载的请求。

测试成功后，您可以保存或激活渠道。

* 单击&#x200B;**[!UICONTROL 另存为草稿]**&#x200B;以保存您的进度，而不使该渠道可用。
* 单击&#x200B;**[!UICONTROL 激活]**&#x200B;使该渠道可用于渠道配置、营销活动和历程。

>[!IMPORTANT]
>
>激活渠道后，只有以下字段保持可编辑状态：名称、描述、图标、限制和重试配置。 终结点URL、标头、查询参数、身份验证和有效负载结构已锁定。<!--TBC-->

<!--TBC: An activated channel can be **archived** (hidden from all selection drop-downs while existing journeys and campaigns continue to function), but it cannot be **deleted**. Deletion is only possible while the channel is in **[!UICONTROL Draft]** status.TBC-->

## 后续步骤 {#next-steps}

您的自定义渠道现已创建。 按照以下剩余步骤完成配置：

* [设置API凭据](custom-channel-api-credentials.md)（如果渠道使用身份验证）
* [委派子域](custom-channel-subdomains.md)（可选 — 链接跟踪必需）
* [创建渠道配置](custom-channel-configuration.md)
