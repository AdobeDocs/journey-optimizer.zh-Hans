---
solution: Journey Optimizer
product: journey optimizer
title: 使用自訂動作
description: 瞭解如何使用自訂動作
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 動作，自訂， API，歷程，設定，服務
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 25%

---

# 使用自訂動作 {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自定义操作"
>abstract="通过自定义操作，您可以配置第三方系统的连接以发送消息或 API 调用。可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。"

通过自定义操作，您可以配置第三方系统的连接以发送消息或 API 调用。可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意原則套用至自訂動作，以防止特定欄位匯出至協力廠商系統，或排除未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action-privacy.md).
* [同意](../action/consent.md).

## URL 配置

的設定窗格 **自訂動作** 活動會顯示針對自訂動作設定的URL設定引數和驗證引數。 您無法在歷程中設定URL的靜態部分，但可在自訂動作的全域設定中設定。 [了解详情](../action/about-custom-action-configuration.md)。

### 動態路徑

如果URL包含動態路徑，請在 **[!UICONTROL 路徑]** 欄位。

若要串連欄位和純文字字串，請使用字串函式或進階運算式編輯器中的加號(+)。 以單引號(&#39;)或雙引號(&#39;&#39;)括住純文字字串。 [了解详情](expression/expressionadvanced.md)。

此表格顯示組態範例：

| 字段 | 值 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 路径 | `The id of marketingCampaign + '/messages'` |

串連URL的格式如下：

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### 標頭與查詢引數 {#headers}

此 **[!UICONTROL URL設定]** 區段顯示動態標頭與查詢引數欄位，但不顯示常數欄位。 動態標題和查詢引數欄位在動作設定畫面中定義為變數。 [了解详情](../action/about-custom-action-configuration.md#url-configuration)

若要指定動態標題和查詢引數欄位的值，請在欄位內或鉛筆圖示上按一下，然後選取所需欄位。

![](assets/journey-dynamicheaderfield.png)

## 動作引數

在 **[!UICONTROL 動作引數]** 區段，您會看到訊息引數定義為 _&quot;Variable&quot;_. 對於這些引數，您可以定義從何處取得此資訊（例如：事件、資料來源）、手動傳遞值或使用進階運算式編輯器進行進階使用案例。 進階使用案例可以是資料操控和其他函式用途。 請參閱此 [頁面](expression/expressionadvanced.md).

**相关主题**

[配置操作](../action/about-custom-action-configuration.md)
