---
solution: Journey Optimizer
product: journey optimizer
title: 将事件发送到历程的其他步骤
description: 了解将事件发送到历程的其他步骤
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 步骤，配置，历程，事件，流， API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---

# 用于发送事件的其他步骤 {#additional-steps-to-send-events}

要配置发送到&#x200B;**[!UICONTROL 流式引入API]**&#x200B;并在[!DNL Journey Optimizer]中使用的事件，您需要执行以下步骤：

1. 从Adobe Experience Platform API获取入口URL。 在[流式引入API概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target="_blank"}中了解更多信息。
1. 从&#x200B;**[!UICONTROL Event]**&#x200B;菜单中的有效负载预览复制有效负载。 在[此页面](../event/about-creating.md#define-the-payload-fields)上了解详情。

然后，您需要配置数据系统，以使用您复制的有效负载将事件推送到流式引入API：

1. 对流式引入API URL（称为入口）设置POST API调用。
1. 在流摄取API调用主体（“数据部分”）中使用您从[!DNL Journey Optimizer]复制的有效负载。 有关示例，请参阅下文
1. 确定从何处获取有效负载中存在的所有变量。 示例：如果事件应传递地址，则粘贴的有效负载将显示“address”：“string”。 “string”应替换为自动填充正确值的变量，即向其发送消息的人员的电子邮件。 请注意，在有效负载预览的&#x200B;**[!UICONTROL 标头]**&#x200B;部分，我们会自动填充许多预期有助于您完成工作的值。
1. 选择“application/json”作为主体类型。
1. 使用键“x-gw-ims-org-id”在标头中传递您的组织ID。 对于值，请使用您的组织ID (&quot;XXX@AdobeOrg&quot;)。

以下是流摄取API事件的示例：

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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

为了便于识别粘贴“数据”部分的位置，您可以使用JSON可视化工具，如[JSON格式器](https://jsonformatter.curiousconcept.com){target="_blank"}。

要排查流式引入API问题，请参阅[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=zh-Hans){target="_blank"}。
