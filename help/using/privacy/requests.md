---
solution: Journey Optimizer
product: journey optimizer
title: 隐私请求
description: 了解有关隐私请求和 Privacy Service 的更多信息。
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: ht
source-wordcount: '491'
ht-degree: 100%

---

# 隐私请求 {#track-changes}

Adobe Experience Platform **Privacy Service** 提供 RESTful API 和用户界面，帮助您管理客户数据请求。借助 Privacy Service，您可以提交从 Adobe Experience Cloud 应用程序访问和删除个人客户数据的请求，从而促进自动遵守法律和组织隐私法规。

可从&#x200B;**[!UICONTROL 请求]**&#x200B;菜单创建和管理隐私请求。

![](assets/requests.png)

有关 Privacy Service 以及如何创建和管理隐私请求的更多信息，请参阅 [Adobe Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans){target="_blank"}。

<!--* [Privacy Service overview](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans)
* [Managing privacy jobs in the Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans)-->

## 管理可发送到 Adobe Journey Optimizer 的个人数据隐私请求 {#data-privacy-requests}

您可以通过两种方式提交个人请求以从 Adobe Journey Optimizer 访问和删除客户数据：

* 通过 **Privacy Service UI**。[了解详情](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans){target="_blank"}
* 通过 **Privacy Service API**。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/overview){target="_blank"}
  <!--More specific information on Privacy Service API [here](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank).-->

Privacy Service 支持两种类型的请求：**数据访问**&#x200B;和&#x200B;**数据删除**。

对于&#x200B;**访问请求**，请从 UI 中指定“**Adobe Journey Optimizer**”（或在 API 中将“**CJM**”指定为产品代码）。

对于&#x200B;**删除请求**，除了“**Adobe Journey Optimizer**”请求之外，您还必须向&#x200B;**三个上游服务**&#x200B;提交删除请求，以阻止 Journey Optimizer 重新注入已删除的数据。如果未指定这些上游服务，“Adobe Journey Optimizer”请求将保持为“正在处理”状态，直到上游服务的删除请求已创建。

三种上游服务包括：

* 用户档案（产品代码：“profileService”）
* AEP 数据湖（产品代码：“AdobeCloudPlatform”）
* 标识（产品代码：“identity”）

>[!NOTE]
>
>本指南仅介绍如何发出 [!UICONTROL Adobe Journey Optimizer] 隐私请求。
>
>* 如果您还计划向 Platform 数据湖发出隐私请求，请参阅此[指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/catalog/privacy)以及本教程。
>
>* 有关实时客户个人资料，请参阅此[指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/privacy)。
>* 有关标识服务，请参阅此[指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/privacy)。
>
>要删除和访问请求，您需要调用这些单独的系统，以确保每个系统都处理了这些请求。向 [!DNL Adobe Journey Optimizer] 发出隐私请求不会从所有这些系统中移除数据。

## 创建访问和删除请求

### 先决条件

要提出访问和删除 Adobe Journey Optimizer 数据的请求，您必须有：

* Adobe 组织 ID
* 要对其执行操作的人员的身份标识符以及对应的命名空间。有关 Adobe Journey Optimizer 和 Experience Platform 中的标识命名空间的更多信息，请参阅[标识命名空间概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces)。

>[!IMPORTANT]
>
>在提交隐私请求时，请确保将“[!DNL '**Adobe Journey Optimizer**]”指定为目标产品名称，并指定与需要访问或移除的配置文件数据关联的&#x200B;**所有标识命名空间**（例如“电子邮件”、“ECID”或“忠诚度 ID”）。特别是对于删除请求，如果您未明确包含产品名称和所有适用的命名空间，则不会从 [!DNL Adobe Journey Optimizer] 中移除数据。

### Journey Optimizer 中用于 API 请求的必填字段值

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your Adobe Organization ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### GDPR 访问请求示例：

通过 UI：

![](assets/accessrequest.png){width="60%" align="center"}

通过 API：

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### GDPR 删除请求示例：

通过 UI：

![](assets/deleterequest.png){width="60%" align="center"}

通过 API：

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
