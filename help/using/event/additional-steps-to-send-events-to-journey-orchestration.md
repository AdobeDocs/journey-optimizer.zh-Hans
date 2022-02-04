---
title: 将事件发送到历程的其他步骤
description: 了解将事件发送到历程的其他步骤
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 7588a675319324e43bbc61a71b1fdfaab9cce93a
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 5%

---

# 用于发送事件的其他步骤 {#additional-steps-to-send-events}

配置要发送到的事件 **[!UICONTROL Streaming Ingestion APIs]** 和 [!DNL Journey Optimizer]，则需要执行以下步骤：

1. 从Adobe Experience Platform API获取入口URL。 在 [流摄取API概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target=&quot;_blank&quot;}。
1. 从 **[!UICONTROL Event]** 菜单。 请参阅[此页面](../event/about-creating.md#define-the-payload-fields)以了解详情。

然后，您需要配置数据系统，以使用您复制的有效负载将事件推送到流摄取API:

1. 设置对流摄取API URL的POSTAPI调用（称为入口）。
1. 使用您复制的有效负荷 [!DNL Journey Optimizer] 在对流摄取API的API调用的正文（“数据部分”）中。 请参阅下面的示例
1. 确定在何处获取有效负载中存在的所有变量。 示例：如果事件应传达地址，则粘贴的有效负载将显示“地址”：&quot;string&quot;。 “string”应被自动填充正确值（要向其发送消息的人员的电子邮件）的变量替换。 请注意，在有效负荷预览中， **[!UICONTROL Header]** 部分，我们会自动填充许多值，以便您的工作。
1. 选择“application/json”作为正文类型。
1. 在标题中使用键“x-gw-ims-org-id”传递您的IMS组织ID。 对于值，请使用您的IMS组织ID(&quot;XXX@AdobeOrg&quot;)。

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

为便于确定粘贴“数据”部件的位置，您可以使用JSON可视化工具，例如 [JSON格式化程序](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}。

要对流摄取API进行故障诊断，请参阅 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}。
