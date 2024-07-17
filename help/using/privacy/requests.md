---
solution: Journey Optimizer
product: journey optimizer
title: 隐私请求
description: 了解有关隐私请求和 Privacy Service 的更多信息。
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 100%

---

# 隐私请求 {#track-changes}

Adobe Experience Platform **Privacy Service** 提供 RESTful API 和用户界面，帮助您管理客户数据请求。借助 Privacy Service，您可以提交从 Adobe Experience Cloud 应用程序访问和删除个人客户数据的请求，从而促进自动遵守法律和组织隐私法规。

可从&#x200B;**[!UICONTROL 请求]**&#x200B;菜单创建和管理隐私请求。

![](assets/requests.png)

有关 Privacy Service 以及如何创建和管理隐私请求的更多信息，请参阅 Adobe Experience Platform 文档：

* [Privacy Service 概述](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans)
* [在 Privacy Service UI 中管理隐私作业](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans)



## 管理可发送到 Adobe Journey Optimizer 的个人数据隐私请求 {#data-privacy-requests}

您可以通过两种方式提交个人请求以从 Adobe Journey Optimizer 访问和删除客户数据：

* 通过 **Privacy Service UI**。请参阅[此处](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/ui/user-guide#_blank)的文档。
* 通过 **Privacy Service API**。请参阅[此处](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank)的文档和[此处](https://developer.adobe.com/experience-platform-apis/#_blank)的 API 信息。

Privacy Service 支持两种类型的请求：**数据访问**&#x200B;和&#x200B;**数据删除**。

>[!NOTE]
>
>本指南仅介绍如何发出 Adobe Journey Optimizer 隐私请求。如果您还计划向 Platform 数据湖发出隐私请求，请参阅此[指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/catalog/privacy)以及本教程。对于实时客户档案，请参阅此[指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/privacy)；对于标识服务，请参阅此[指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/privacy)。要删除和访问请求，您需要调用这些单独的系统，以确保每个系统都处理了这些请求。向 Adobe Journey Optimizer 发出隐私请求不会从所有这些系统中移除数据。

对于&#x200B;**访问请求**，请从 UI 中指定“Adobe Journey Optimizer”（或在 API 中将“CJM”指定为产品代码）。

对于&#x200B;**删除请求**，除了“Adobe Journey Optimizer”请求之外，您还必须向三个上游服务提交删除请求，以阻止 Journey Optimizer 重新注入已删除的数据。如果未指定这些上游服务，“Adobe Journey Optimizer”请求将保持为“正在处理”状态，直到上游服务的删除请求已创建。

三种上游服务包括：

* 用户档案（产品代码：“profileService”）
* AEP 数据湖（产品代码：“AdobeCloudPlatform”）
* 标识（产品代码：“identity”）

## 如何创建访问和删除请求

### 先决条件

要提出访问和删除 Adobe Journey Optimizer 数据的请求，您必须有：

* IMS 组织 ID
* 要对其执行操作的人员的身份标识符以及对应的命名空间。有关 Adobe Journey Optimizer 和 Experience Platform 中的标识命名空间的更多信息，请参阅[标识命名空间概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces)。

### Adobe Journey Optimizer 中用于 API 请求的必填字段值

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

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

![](assets/accessrequest.png)

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

![](assets/deleterequest.png)

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
