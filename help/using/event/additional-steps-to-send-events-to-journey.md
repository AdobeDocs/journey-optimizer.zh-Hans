---
solution: Journey Optimizer
product: journey optimizer
title: 將事件傳送至歷程的其他步驟
description: 瞭解將事件傳送至歷程的其他步驟
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: 步驟，設定，歷程，事件，串流， API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 5%

---

# 用于发送事件的其他步骤 {#additional-steps-to-send-events}

若要設定要傳送至的事件 **[!UICONTROL 串流擷取API]** 並將用於 [!DNL Journey Optimizer]，您必須遵循下列步驟：

1. 從Adobe Experience Platform API取得入口URL。 進一步瞭解 [串流擷取API概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target="_blank"}.
1. 從中的裝載預覽複製裝載 **[!UICONTROL 事件]** 功能表。 请参阅[此页面](../event/about-creating.md#define-the-payload-fields)以了解详情。

然後，您需要設定資料系統，使用您複製的裝載將事件推送至串流獲取API：

1. 設定串流獲取API URL的POSTAPI呼叫（稱為入口）。
1. 使用您複製自的裝載 [!DNL Journey Optimizer] 串流獲取API之API呼叫的內文（「資料區段」）中。 如需範例，請參閱下文
1. 決定從何處取得裝載中出現的所有變數。 範例：如果事件應該要傳達位址，貼上的裝載會顯示「address」：「string」。 「string」應取代為會自動填入正確值的變數，也就是傳送訊息的收件者電子郵件。 請注意，在裝載預覽中，在 **[!UICONTROL 頁首]** 章節，我們會自動填入許多值，以利您順利完成工作。
1. 選取「application/json」作為內文型別。
1. 使用索引鍵「x-gw-ims-org-id」在標題中傳遞您的組織ID。 對於該值，請使用您的組織ID (&quot;XXX@AdobeOrg&quot;)。

以下是串流擷取API事件的範例：

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

為方便您識別「資料」部分的貼上位置，您可以使用JSON視覺化工具，例如 [JSON格式化程式](https://jsonformatter.curiousconcept.com){target="_blank"}.

若要疑難排解串流獲取API，請參閱 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}.
