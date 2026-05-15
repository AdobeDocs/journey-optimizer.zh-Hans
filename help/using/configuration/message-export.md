---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer中的消息导出
description: 了解如何导出消息
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 导出，消息， HIPAA，电子邮件，短信，配置
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
TQID: https://experienceleague.adobe.com/4i6dFByqNizhrMeQrr32twEPVrg4Jz8J-rgA-sR70Ho
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cc84ad59f4233967c484c99651edb0558518c58c
workflow-type: tm+mt
source-wordcount: 1398
ht-degree: 6%

---

# 导出消息内容 {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="保留和导出您发送的内容"
>abstract="选择此选项可将按照该配置发送的电子邮件或短信内容写入 [!DNL Experience Platform] 数据集。 记录自摄取之日起保留 7 个自然日，在此期间您可以将其导出到自己的存储位置。"

>[!AVAILABILITY]
>
>此功能适用于已购买消息导出附加组件产品的组织，且仅限于电子邮件和短信渠道。 有关更多信息，请与您的 Adobe 代表联系。

**消息导出**&#x200B;允许您通过[[!DNL Adobe Experience Platform] 目标](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/home){target="_blank"}将已发送的电子邮件和短信消息内容从[!DNL Journey Optimizer]传输到您自己的存储空间，这样您就可以将数据从[!DNL Experience Platform]传输到外部端点。

使用此功能，通过[!DNL Journey Optimizer]发送的已标记为导出的电子邮件和短信消息的内容将写入[!DNL Experience Platform] [AJO消息导出数据集](message-export-schema.md)。

然后，记录会在数据集中保留七个日历天（从摄取开始），在此期间，您可以将它们导出到您选择的外部系统。

➡️有关常见问题和答案，请参阅[邮件导出常见问题解答](#message-export-faq)。

## 护栏

* 此功能仅支持&#x200B;**电子邮件**&#x200B;和&#x200B;**短信**&#x200B;渠道。
* AJO消息导出数据集中的记录从引入起保留&#x200B;**7个日历日**。
* 在启用邮件导出之前发送的邮件不支持回填，如下所述。

## 启用邮件导出 {#enable-message-export}

报文导出功能的载入流程包括两个步骤：

1. [在[!DNL Experience Platform]中设置导出数据流](#set-up-export-dataflow)；
1. 在[!DNL Journey Optimizer]中的通道配置上[启用消息导出](#config-message-export)。

>[!WARNING]
>
>只有启用导出和发送消息后才会显示新记录。 不支持在设置导出流程和启用导出消息选项之前回填内容。

### 设置导出数据流 {#set-up-export-dataflow}

在能够导出数据之前，请先通过定义[!DNL Experience Platform]目标和数据集导出流来设置导出流程。

有关详细步骤、支持的云目标、所需权限以及更多信息，请参阅[此部分](../data/export-datasets.md#export-datasets)。

>[!NOTE]
>
>必须为每个沙盒配置此设置。

1. 选择Experience Platform [目标类型](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/destination-types){target="_blank"}。 [此页面](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/catalog/overview){target="_blank"}上提供了准备好接收数据的可用目标平台列表。

1. 在[!DNL Experience Platform]中，通过定义凭据、存储桶/容器、路径前缀和安全选项来配置您的目标。 [了解如何操作](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. 使用以下数据创建数据集导出流：

   * Source数据集：选择&#x200B;**AJO消息导出数据集**。
   * 文件格式：选择JSON或Parquet（根据下游工具选择一种格式）。
   * 计划：确保在7天保留期内运行。

### 在渠道配置中启用消息导出 {#config-message-export}

要将消息导出应用于营销活动和历程，必须在渠道配置级别启用专用选项。 请按照以下步骤操作。

1. 在[!DNL Journey Optimizer]中，编辑或创建所需的电子邮件或短信[渠道配置](channel-surfaces.md#create-channel-surface)。

1. 选择&#x200B;**[!UICONTROL 启用消息导出]**&#x200B;选项。

   ![](assets/config-message-export.png)

1. 保存更改并提交渠道配置。

使用此渠道配置通过营销活动或历程发送消息后，电子邮件和短信消息将写入&#x200B;**AJO消息导出数据集**。 然后，您可以[访问数据集中的记录](#access-exported-data)，并根据您定义的导出数据流将它们导出到您选定的存储目标。

>[!NOTE]
>
>禁用&#x200B;**[!UICONTROL 启用消息导出]**&#x200B;切换可阻止将此渠道配置的新记录引入数据集。 现有记录会一直保留，直到保留期到期。

## 访问导出的报文数据 {#access-exported-data}

使用启用了消息导出的渠道配置发送消息后，您可以在&#x200B;**AJO消息导出数据集**&#x200B;中访问和查看导出的数据。

要查看导出的消息数据，请执行以下操作：

1. 在[!DNL Journey Optimizer]中，在左侧导航中导航到&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 数据集]**。 [了解有关数据集的更多信息](../data/get-started-datasets.md)

1. 确保显示的是系统生成的数据集。

1. 从列表中选择&#x200B;**AJO消息导出数据集**。

   ![](assets/datasets-list.png)

1. 在数据集详细信息页面上，单击&#x200B;**[!UICONTROL 预览数据集]**&#x200B;以查看最新记录。

   ![](assets/ajo-message-export-dataset.png)

该数据集包含通过启用了消息导出功能的渠道配置发送的每封消息的全面信息，包括：主题行、消息正文、收件人电子邮件地址或电话号码、发件人地址或电话号码、发送日期和时间、个性化数据等。

➡️有关数据集结构和所有可用字段的完整视图，请参阅[AJO消息导出架构](message-export-schema.md)。

数据集中的所有记录都将保留&#x200B;**七个日历天**。 在此保留期内，您可以访问数据以进行合规性审核、法律查询，或通过配置的Experience Platform目标将其导出到您自己的存储系统。

## 示例导出JSON {#sample-exported-json}

以下示例显示了写入AJO短信和电子邮件消息导出数据集的记录的整体形状。 标识符、架构引用、时间戳和内容等值具有说明性；您的导出反映您的沙盒、架构和已发送消息。

展开每个部分以查看完整的JSON示例。

+++ 短信导出示例

```json
{
  "header": {
    "msgId": "f06d2a6d-65c3-472b-9ca7-cc4224af2df4",
    "xactionId": "9ccd6e76-9ee5-4a12-bff3-fea240228121",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "906E3A095DC834230A495FD6@AdobeOrg",
    "sandboxId": "db3adc95-dcf6-49c3-badc-95dcf639c345",
    "sandboxName": "ajo-e2e",
    "createdAt": 1773591102107,
    "datasetId": "689653509dd3432b92f6323f",
    "schemaRef": {
      "id": "https://ns.adobe.com/aemonacpprodcampaign/schemas/64cb5d9d26c2aae6b08bdc9b7882deb90202439ec53836e7",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1773591102107,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "CSM-09561055",
            "messageID": "15fe77c8-ab73-49e4-abbb-c25b859162ff-0",
            "messageType": "marketing",
            "campaignID": "5638ce57-5264-4a96-995f-5ae34eddafd7",
            "campaignVersionID": "f9019155-3d6a-44a1-9b6f-5f9cd49e7cf5",
            "campaignActionID": "dfa7f59f-477c-42ec-9db2-831d294b5779",
            "batchInstanceID": "5e23a286fb72411f1cdf1443a81ad2eb",
            "messagePublicationID": "15fe77c8-ab73-49e4-abbb-c25b859162ff",
            "audience": {
              "id": "4c339f63-b66e-4e72-8d56-db624b5277f2",
              "type": "targeted"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/sms",
              "_type": "https://ns.adobe.com/xdm/channel-types/sms"
            },
            "messageProfileID": "7ff5aefb-7583-38c4-8c32-b63cced94aa7",
            "variant": "5c1092da-5ba2-4bcc-b591-713ee7999f7d"
          },
          "messageRenderedContent": {
            "smsContent": {
              "message": "AJO Campaigns - Prod - E2E Test Text VA7"
            }
          },
          "messageDeliveryMetadata": {
            "smsMetadata": {
              "recipient": {
                "number": "+19256260201"
              },
              "sender": {
                "numbers": [
                  "12345678"
                ]
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "rlyajoqa+messageExport1@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "b0001846-cafa-379a-be96-1d8ee973e047",
      "timestamp": "2026-03-15T16:11:42.184Z"
    }
  }
}
```

+++

+++ 电子邮件导出示例

```json
{
  "header": {
    "msgId": "1e64d2c4-7887-4f80-8b28-5c20d3da8baf",
    "xactionId": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "745F37C35E4B776E0A49421B@AdobeOrg",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "sandboxName": "prod",
    "createdAt": 1754489661211,
    "datasetId": "68912b8881572a2b267380c1",
    "schemaRef": {
      "id": "https://ns.adobe.com/cjmstage/schemas/1684477c0160376b8bb6975a80b5e5bd384696329faa1c42",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1754489659000,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "HUMA-62208933",
            "messageID": "d0d02f68-afea-42fc-b898-6819cee643e6-0",
            "messageType": "transactional",
            "campaignID": "ce2331c2-c259-47ff-a1dd-f6d1eae08801",
            "campaignVersionID": "4272bb9f-e154-44e9-89f1-6548c77d1455",
            "batchInstanceID": "03587190-72cf-11f0-938b-31e7c9f96d89",
            "messagePublicationID": "d0d02f68-afea-42fc-b898-6819cee643e6",
            "audience": {
              "type": "all"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/email",
              "_type": "https://ns.adobe.com/xdm/channel-types/email"
            },
            "messageProfileID": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
            "variant": "11cc5796-8017-4738-aa66-ca5db967dfcc"
          },
          "messageRenderedContent": {
            "emailContent": {
              "subject": "test",
              "html": "xxx"
            }
          },
          "messageDeliveryMetadata": {
            "emailMetadata": {
              "recipient": {
                "email": "himanshig@adobe.com"
              },
              "sender": {
                "email": "cjm-team@e2e-personalisation.test.cjmadobe.com",
                "name": "CJM team",
                "replyToEmail": "replyto@marketing.adobecjm.com",
                "replyToName": "replyto",
                "errorEmail": "replyto@e2e-personalisation.test.cjmadobe.com"
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "chijain@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "ea48ce1b-80c9-3c6a-b05f-d1c998989e02",
      "timestamp": "2025-08-06T14:14:22.814Z"
    }
  }
}
```

+++

## 邮件导出常见问题解答 {#message-export-faq}

+++ 什么是消息导出？

通过消息导出，客户可以导出发送给最终用户的完全呈现的消息（电子邮件和短信）。 导出的数据可使用标准[!DNL Adobe Experience Platform] (AEP)导出功能传送到外部目标，并用于存档、合规性审查、分析或下游集成。

+++

+++ 支持哪些渠道？

消息导出支持：

* 电子邮件
* 短信

+++

+++ 报文导出会生成哪些数据？

消息导出在[!DNL Adobe Experience Platform]中创建一个系统生成的数据集，其中包含发送时消息的快照。 然后，可将此数据集导出到支持的目标（例如，云存储或第三方系统）。

Message Export是一种使客户能够将报文数据移出Adobe系统的支持机制，客户负责在其自己的存档或法规遵从性解决方案中转换、存储和管理数据。

+++

+++ 消息导出是否会捕获完全个性化的消息？

可以。 消息导出会捕获已发送给每个收件人的完全呈现的消息，包括在发送时呈现的个性化和动态内容。

+++

+++ Message Export是否可用于重现原始邮件？

可以。 导出的HTML可用于在浏览器中重现已发送的原始消息。

但是，复制取决于外部托管的资产（如图像）的可用性。 消息导出不会直接在导出中嵌入媒体文件。

+++

+++ 导出中是否包含图像和媒体？

“消息导出”包含的HTML内容包含对图像和其他媒体的引用(URL)。 媒体资产未嵌入到导出中。

如果图像或资源URL在发送后变得无效、受限制或未发布，则消息导出无法恢复该资源。

+++

+++ 在“消息导出”中如何处理链接？

导出的邮件包含加密的跟踪链接，与发送时处理链接的方式一致。 这些加密的链接将保留在导出中，并可按平台设计的那样进行解析。

+++

+++ 如何处理PII和个性化数据？

数据存储与呈现的消息中显示的完全相同：

* 呈现到消息中的Personalization值（例如，名字）将显示为文本。
* 加密的元素（如跟踪的链接）仍保持加密状态。
* 报文导出不会自动对渲染的报文内容进行匿名化或密文。

+++

+++ 邮件导出数据的保留期是多久？

邮件导出数据遵循[!DNL Adobe Experience Platform]内的7天保留期限。

客户应在此期限内导出数据，并在需要更长的保留期时将其存储在自己的系统中。

+++

+++ 客户能否在购买前测试报文导出？

消息导出没有试用或“先试后买”选项。

客户可以使用示例导出文件验证其下游系统，因为消息导出依赖于标准AEP数据集和目标功能。

+++

+++ 购买前消息导出架构是否可用？

不是。 只有在购买并启用消息导出加载项后，消息导出数据集和架构才在产品中可用。

+++

+++ Message Export是完整存档还是法规遵从性解决方案？

不是。 Message Export是一个支持工具，而不是完整存档或合规性产品。

客户应：

* 从Adobe导出消息数据
* 根据需要进行转换或扩充
* 将数据存储并管理到他们自己的存档或法规遵从性系统中

+++

+++ 常见用例有哪些？

客户通常使用消息导出执行以下操作：

* 法规或合规性审查
* 报文存档
* 与第三方系统集成
* 内部审计或支持工作流程
* Analytics beyond Adobe应用程序

+++

+++ 消息导出不具备的功能

消息导出不会：

* 嵌入外部图像或媒体资产
* 在Adobe系统中提供无限期或长期数据保留
* 提供试用环境
* 自动将邮件存档到Adobe之外

+++

