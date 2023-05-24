---
solution: Journey Optimizer
product: journey optimizer
title: 外部数据源
description: 了解如何配置外部数据源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: 外部，來源，資料，設定，連線，第三方
exl-id: f3cdc01a-9f1c-498b-b330-1feb1ba358af
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 71%

---

# 外部数据源 {#external-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_custom"
>title="外部数据源"
>abstract="外部数据源允许您定义与第三方系统的连接，例如，如果您使用酒店预订系统来检查人员是否已注册了房间。与内置 Adobe Experience Platform 数据源相反，您可以根据需要创建尽可能多的外部数据源。"

外部数据源允许您定义与第三方系统的连接，例如，如果您使用酒店预订系统来检查人员是否已注册了房间。与内置 Adobe Experience Platform 数据源相反，您可以根据需要创建尽可能多的外部数据源。

>[!NOTE]
>
>使用外部系統時的護欄列於 [此頁面](../configuration/external-systems.md).

支持使用 POST 或 GET 的 REST API 和返回 JSON。支持 API 密钥、基本和自定义身份验证模式。

让我们举一个天气 API 服务的例子，我想借助该服务根据实时天气数据定制我的历程的行为。

以下是两个 API 调用示例：

* _https://api.adobeweather.org/weather?city=London,uk&amp;appid=1234_
* _https://api.adobeweather.org/weather?lat=35&amp;lon=139&amp;appid=1234_

该调用由一个主 URL (_https://api.adobeweather.org/weather_)、两个参数集（“city”表示城市，“lat/long”表示纬度和经度）和 API 密钥 (appid) 组成。

以下是创建和配置新外部数据源的主要步骤：

1. 從資料來源清單中，按一下 **[!UICONTROL 建立資料來源]** 以建立新的外部資料來源。

   ![](assets/journey25.png)

   这将打开屏幕右侧的数据源配置窗格。

   ![](assets/journey26.png)

1. 输入数据源的名称。

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 向数据源添加描述。此步骤是可选的。
1. 添加外部服务的 URL。在我们的示例中：_https://api.adobeweather.org/weather_。

   >[!CAUTION]
   >
   >出于安全原因，我们强烈建议使用 HTTPS。另请注意，我们不允许使用非公开的 Adobe 地址和 IP 地址。

   ![](assets/journey27.png)

1. 根據外部服務組態設定驗證： **[!UICONTROL 無驗證]**， **[!UICONTROL 基本]**， **[!UICONTROL 自訂]** 或 **[!UICONTROL API金鑰]**. 有关自定义身份验证模式的更多信息，请参阅[此部分](../datasource/external-data-sources.md#custom-authentication-mode)。在我们的示例中，我们选择：

   * **[!UICONTROL 型別]**：「API金鑰」
   * **[!UICONTROL 名稱]**：「appid」（這是API金鑰引數名稱）
   * **[!UICONTROL 值]**：「1234」（這是我們API金鑰的值）
   * **[!UICONTROL 位置]**：「查詢引數」（API金鑰位於URL）

   ![](assets/journey28.png)

1. 按一下以為每個API引數集新增欄位群組 **[!UICONTROL 新增欄位群組]**. 请勿在字段组名称中使用空格或特殊字符。在我们的示例中，我们需要创建两个字段组，每个参数集（“city”和“long/lat”）各一个。

对于“long/lat”参数集，我们创建一个包含以下信息的字段组：

* **[!UICONTROL 使用位置]**：顯示使用欄位群組的歷程次數。 您可以按一下 **[!UICONTROL 檢視歷程]** 圖示以顯示使用此欄位群組的歷程清單。
* **[!UICONTROL 方法]**：選取POST或GET方法。 在我们的示例中，我们选择 GET 方法。
* **[!UICONTROL 動態值]**：在本例中，輸入以逗號分隔的不同引數，即&quot;long，lat&quot;。 由于参数值取决于执行上下文，因此将在历程中进行定义。[了解详情](../building-journeys/expression/expressionadvanced.md)
* **[!UICONTROL 回應裝載]**：按一下 **[!UICONTROL 裝載]** 欄位並貼上呼叫傳回之裝載的範例。 例如，我们使用了在天气 API 网站上找到的有效负载。验证字段类型是否正确。每次调用 API 时，系统将检索有效负载示例中包含的所有字段。請注意，您可以按一下 **[!UICONTROL 貼上新裝載]** 如果您想要變更目前已傳遞的裝載。

   >[!NOTE]
   >
   >回應裝載定義中不支援純量陣列。

* **[!UICONTROL 已傳送裝載]**：此欄位不會出現在我們的範例中。 仅当选择 POST 方法时才可用。粘贴将发送到第三方系统的有效负载。

若是GET呼叫所需的引數，請在 **[!UICONTROL 動態值]** 欄位，它們就會在呼叫結束時自動新增。 如果是 POST 调用，您需要：

* 在中列出呼叫時要傳遞的引數 **[!UICONTROL 動態值]** 欄位（在以下範例中：「identifier」）。
* 在发送的有效负载主体中使用完全相同的语法指定它们。为此，您需要添加“param”：“您的参数名称”（在以下示例中为“identifier”）。请遵循以下语法：

   ```
   {"id":{"param":"identifier"}}
   ```

![](assets/journey29.png)

单击&#x200B;**[!UICONTROL 保存]**。

数据源现已配置完毕，可随时用于您的历程，例如在您的条件下或个性化电子邮件时。如果温度高于 30°C，您可以决定发送特定通信。

## 自定义身份验证模式{#custom-authentication-mode}

>[!CONTEXTUALHELP]
>id="jo_authentication_payload"
>title="关于自定义身份验证"
>abstract="自定义身份验证模式用于复杂身份验证，以调用 OAuth2 等 API 封装协议。操作执行分为两步。首先，执行对端点的调用以生成访问令牌。然后，访问令牌将插入操作的 HTTP 请求中。"

此身份验证模式用于复杂的身份验证，通常用于调用 OAuth2 等 API 封装协议，以检索要插入到操作的实际 HTTP 请求中的访问令牌。

配置自定义身份验证时，可以单击以下按钮检查自定义身份验证有效负载是否正确配置。

![](assets/journey29-bis.png)

如果测试成功，按钮将变为绿色。

![](assets/journey29-ter.png)

通过此身份验证，操作执行分为两步：

1. 调用端点以生成访问令牌。
1. 通过以正确的方式插入访问令牌以调用 REST API。

此身份验证分为两部分。

要调用以生成访问令牌端点的定义：

* 端点：用于生成端点的 URL
* 端点上 HTTP 请求的方法（GET 或 POST）
* 標頭：在此呼叫中插入做為標頭的機碼值組（如有需要）
* 主体：描述在方法为 POST 时调用的主体。我們支援有限的主體結構，在bodyParams （索引鍵值配對）中定義。 bodyType 描述调用中主体的格式和编码：
   * &#39;form&#39;：表示內容型別將會是application/x-www-form-urlencoded （字元集UTF-8），而金鑰 — 值配對將會序列化為：key1=value1&amp;key2=value2&amp;...
   * &#39;json&#39;：表示內容型別將會是application/json （字元集UTF-8），而機碼值組將會序列化為json物件，如下所示： _{ &quot;key1&quot;： &quot;value1&quot;， &quot;key2&quot;： &quot;value2&quot;， ...}_

在操作的 HTTP 请求中必须插入访问令牌方式的定义：

* authorizationType：定义如何在操作的 HTTP 调用中插入生成的访问令牌。可能的值包括：

   * 载体：指示必须在授权标头中插入的访问令牌，如：_授权：载体&lt;access token>_
   * 标头：指示必须将访问令牌作为标头插入，即由 tokenTarget 属性定义的标头名。例如，如果 tokenTarget 是 myHeader，则访问令牌将作为标头插入：_myHeader：&lt;access token>_
   * queryParam：指示访问令牌必须作为 queryParam 插入，即由属性 tokenTarget 定义的查询参数名称。例如，如果 tokenTarget 是 myQueryParam，则操作调用的 URL 将为：_&lt;url>?myQueryParam=&lt;access token>_

* tokenInResponse：指示如何从身份验证调用中提取访问令牌。此属性可以是：
   * “response”：指示 HTTP 响应是访问令牌
   * json 中的选择器（假定响应是 json，我们不支持 XML 等其他格式）。此选择器的格式为 _json://&lt;path to the access token property>_。例如，如果调用的响应为 _{ &quot;access_token&quot;: &quot;theToken&quot;、&quot;timestamp&quot;: 12323445656 }_，则 tokenInResponse 将为 _json: //access_token_

此身份验证的格式为：

```
{
    "type": "customAuthorization",
    "authorizationType": "<value in 'bearer', 'header' or 'queryParam'>",
    (optional, mandatory if authorizationType is 'header' or 'queryParam') "tokenTarget": "<name of the header or queryParam if the authorizationType is 'header' or 'queryParam'>",
    "endpoint": "<URL of the authentication endpoint>",
    "method": "<HTTP method to call the authentication endpoint, in 'GET' or 'POST'>",
    (optional) "headers": {
        "<header name>": "<header value>",
        ...
    },
    (optional, mandatory if method is 'POST') "body": {
        "bodyType": "<'form'or 'json'>,
        "bodyParams": {
            "param1": value1,
            ...

        }
    },
    "tokenInResponse": "<'response' or json selector in format 'json://<field path to access token>'"
}
```

您可以更改自定义身份验证数据源的令牌的缓存时间。以下是自定义身份验证有效负载的示例。缓存时间在“cacheDuration”参数中定义。它指定缓存中生成的令牌的保留持续时间。单位可以是毫秒、秒、分钟、小时、天、月、年。

以下是持有人驗證型別的範例：

```
{
  "authentication": {
    "type": "customAuthorization",
    "authorizationType": "Bearer",
    "endpoint": "http://localhost:${port}/epsilon/oauth2/access_token",
    "method": "POST",
    "headers": {
      "Authorization": "Basic EncodeBase64(<epsilon Client Id>:<epsilon Client Secret>)"
    },
    "body": {
      "bodyType": "form",
      "bodyParams": {
        "scope": "cn mail givenname uid employeeNumber",
        "grant_type": "password",
        "username": "<epsilon User Name>",
        "password": "<epsilon User Password>"
      }
    },
    "tokenInResponse": "json://access_token",
    "cacheDuration": {
      "duration": 5,
      "timeUnit": "minutes"
    }
  }
}
```

>[!NOTE]
>
>快取持續時間有助於避免過多呼叫驗證端點。 驗證權杖保留在服務中會快取，沒有持續性。 如果重新啟動服務，它會從乾淨的快取開始。 快取持續時間預設為1小時。 在自訂驗證裝載中，可透過指定另一個保留期間來調整它。

以下是標頭驗證型別的範例：

```
{
  "type": "customAuthorization",
  "authorizationType": "header",
  "tokenTarget": "x-auth-token",
  "endpoint": "https://myapidomain.com/v2/user/login",
  "method": "POST",
  "headers": {
    "x-retailer": "any value"
  },
  "body": {
    "bodyType": "form",
    "bodyParams": {
      "secret": "any value",
      "username": "any value"
    }
  },
  "tokenInResponse": "json://token"
} 
```

以下是登入API呼叫的回應範例：

```
{
  "token": "xDIUssuYE9beucIE_TFOmpdheTqwzzISNKeysjeODSHUibdzN87S"
}
```
