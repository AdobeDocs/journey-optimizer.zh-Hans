---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 中的身份入门
description: 了解如何在 Adobe Journey Optimizer 中管理身份
feature: Profiles, Identities
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: ht
source-wordcount: '342'
ht-degree: 100%

---

# 身份入门 {#identities-gs}

身份是指实体（通常是个人）的独特数据。登录 ID、ECID 或忠诚度 ID 等身份称为已知身份。

电子邮件地址和电话号码等个人身份信息 (PII) 用于直接识别客户。因此，PII 用于跨系统匹配客户的多个身份。

在[!DNL Adobe Journey Optimizer]中，跨设备和渠道的&#x200B;**身份**&#x200B;与用户相关联，从而会生成一个[身份图](#id-graph)。关联的身份图用于根据您所有业务接触点之间的交互对体验进行个性化。

![](assets/identities-home.png)

要了解&#x200B;**身份服务**&#x200B;的更多信息，请参阅[本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hans){target="_blank"}。

## 身份命名空间 {#identity-namespaces}

**身份命名空间**&#x200B;是“身份服务”的组件，充当与身份相关的上下文指示器。例如，它们会将`name@email.com`的值区别于电子邮件地址或将`443522`区别于数字 CRM ID。使用身份命名空间需要了解所涉及的多个 Adobe Experience Platform 服务。开始使用命名空间之前，请参阅以下服务的文档：

要了解&#x200B;**身份命名空间**&#x200B;的更多信息，请参阅[本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hans){target="_blank"}。

## 身份图{#id-graph}

**身份图**&#x200B;是特定客户不同身份之间关系的映射，可直观地展示客户如何跨不同渠道与您的品牌进行交互。Adobe Experience Platform 身份服务几乎可以实时地集体管理和更新所有客户身份图，以响应客户活动。

通过[!DNL Adobe Journey Optimizer]用户界面中的身份图查看器，您可以查看并更好地了解将哪些客户身份拼合在一起，以及如何拼合在一起。查看器允许您拖动图形的不同部分并与之交互，从而检查复杂的身份关系、更高效地进行调试，了解信息的利用方式从而增强透明度并从中受益。

要了解&#x200B;**身份图**&#x200B;的更多信息，请参阅[本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html?lang=zh-Hans){target="_blank"}。
