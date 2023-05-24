---
solution: Journey Optimizer
product: journey optimizer
title: 設定自訂動作
description: 瞭解如何設定自訂動作
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: 動作，協力廠商，自訂，歷程， API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 15%

---

# 設定自訂動作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自定义操作"
>abstract="如果您要使用第三方系统发送消息，或者如果希望历程将 API 调用发送到第三方系统，请使用自定义操作配置第三方系统与历程的连接。例如，可以通过自定义操作连接到以下系统：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com)、Firebase 等。"

如果您要使用第三方系统发送消息，或者如果希望历程将 API 调用发送到第三方系统，请使用自定义操作配置第三方系统与历程的连接。例如，您可以使用自訂動作連線到下列系統：Epsilon、Slack、 [Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等。

自定义操作是由技术用户定义并提供给营销人员的附加操作。設定後，其會顯示在您歷程的左側浮動視窗中，位於 **[!UICONTROL 動作]** 類別。 请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)以了解详情。

## 限制{#custom-actions-limitations}

自訂動作會附帶幾項限制，列於 [此頁面](../start/guardrails.md).

在自訂動作引數中，您可以傳遞簡單的集合以及物件集合。 進一步瞭解中的集合限制 [此頁面](../building-journeys/collections.md#limitations).

另請注意，自訂動作引數具有預期格式（例如：字串、小數等）。 您必須注意遵守這些預期的格式。 在本節瞭解更多 [使用案例](../building-journeys/collections.md).

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意原則套用至自訂動作，以防止特定欄位匯出至協力廠商系統，或排除未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action.md).
* [同意](../action/action.md).


## 配置步骤 {#configuration-steps}

以下是設定自訂動作所需的主要步驟：

1. 在「管理」選單區段中，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 動作]** 區段，按一下 **[!UICONTROL 管理]**. 按一下 **[!UICONTROL 建立動作]** 以建立新動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/custom2.png)

1. 輸入動作的名稱。

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 為動作新增說明。 此步骤是可选的。
1. 使用此動作的歷程次數會顯示在 **[!UICONTROL 使用位置]** 欄位。 您可以按一下 **[!UICONTROL 檢視歷程]** 按鈕來顯示使用此動作的歷程清單。
1. 定義不同的 **[!UICONTROL URL設定]** 引數。 请参阅[此页](../action/about-custom-action-configuration.md#url-configuration)。
1. 設定 **[!UICONTROL 驗證]** 區段。 此設定與資料來源的設定相同。  请参阅[此小节](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定義 **[!UICONTROL 動作引數]**. 请参阅[此页](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 单击&#x200B;**[!UICONTROL 保存]**。

   自訂動作現已設定完畢，且可供您在歷程中使用。 请参阅[此页](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在歷程中使用自訂動作時，大部分引數均為唯讀。 您只能修改 **[!UICONTROL 名稱]**， **[!UICONTROL 說明]**， **[!UICONTROL URL]** 欄位和 **[!UICONTROL 驗證]** 區段。

## URL 配置 {#url-configuration}

設定自訂動作時，您需要定義下列專案 **[!UICONTROL URL設定]** 引數：

![](assets/journeyurlconfiguration.png)

1. 在 **[!UICONTROL URL]** 欄位中，指定外部服務的URL：

   * 如果URL是靜態的，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，請只輸入URL的靜態部分，即配置、主機、連線埠，以及（選擇性）路徑的靜態部分。

      示例：`https://xxx.yyy.com/somethingstatic/`

      將自訂動作新增至歷程時，您將指定URL的動態路徑。 [了解详情](../building-journeys/using-custom-actions.md)。
   >[!NOTE]
   >
   >基於安全考量，強烈建議您針對URL使用HTTPS配置。 我們不允許使用非公開的Adobe位址和IP位址。
   >
   >定義自訂動作時只允許預設連線埠：80代表http，443代表https。

1. 選取通話 **[!UICONTROL 方法]**：它可以是以下任一值 **[!UICONTROL POST]** 或 **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > 此 **DELETE** 方法不受支援。 如果您需要更新現有資源，請選取 **PUT** 方法。

1. 定義標題和查詢引數：

   * 在 **[!UICONTROL 標頭]** 區段，按一下 **[!UICONTROL 新增標題欄位]** 定義要傳送至外部服務之要求訊息的HTTP標頭。 此 **[!UICONTROL Content-Type]** 和 **[!UICONTROL 字元集]** 標頭欄位預設為設定。 您無法修改或刪除這些欄位。

   * 在 **[!UICONTROL 查詢引數]** 區段，按一下 **[!UICONTROL 新增查詢引數欄位]** 以定義您要新增至URL的引數。

   ![](assets/journeyurlconfiguration2bis.png)

1. 輸入欄位的標籤或名稱。

1. 選取型別： **[!UICONTROL 常數]** 或 **[!UICONTROL 變數]**. 如果您已選取 **[!UICONTROL 常數]**，然後在「 」中輸入常數值 **[!UICONTROL 值]** 欄位。 如果您已選取 **[!UICONTROL 變數]**，則會在將自訂動作新增至歷程時指定此變數。 [了解详情](../building-journeys/using-custom-actions.md)。

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >將自訂動作新增到歷程後，如果歷程處於草稿狀態，您仍然可以新增標題或查詢引數欄位。 如果您不想讓歷程受設定變更影響，請複製自訂動作，並將欄位新增到新的自訂動作。
   >
   >標頭會根據欄位剖析規則進行驗證。 進一步瞭解 [本檔案](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}。

## 定義動作引數 {#define-the-message-parameters}

在 **[!UICONTROL 動作引數]** 區段，貼上要傳送至外部服務的JSON裝載範例。

![](assets/messageparameterssection.png)

>[!NOTE]
>
>裝載範例不能包含null值。 承載中的欄位名稱不能包含「。」 字符. 開頭不能為「$」字元。

您將能夠定義引數型別（例如：字串、整數等）。

您也可以選擇指定引數是常數還是變數：

* **常數** 表示引數的值是由技術角色在動作設定窗格中定義。 各個歷程中的值一律相同。 這不會改變，且行銷人員在歷程中使用自訂動作時不會看到。 例如，它可能是協力廠商系統期望的ID。 在這種情況下，切換常數/變數右側的欄位是傳遞的值。
* **變數** 表示引數的值會有所不同。 在歷程中使用此自訂動作的行銷人員，可以自由傳遞他們想要的值，或指定從何處擷取此引數的值(例如從事件、Adobe Experience Platform等)。 在這種情況下，切換常數/變數右側的欄位是行銷人員將在歷程中看到的標籤，以命名此引數。

![](assets/customactionpayloadmessage2.png)
