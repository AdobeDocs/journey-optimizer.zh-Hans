---
title: 开始使用Journey Optimizer中的身份
description: 了解如何在Adobe Journey Optimizer中管理身份
feature: Profiles
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 9%

---

# 身份入门 {#identities-gs}

身份是实体（通常是个人）特有的数据。 登录ID、ECID或忠诚度ID等身份称为已知身份。

个人身份信息(PII)（如电子邮件地址和电话号码）用于直接识别客户。 因此，PII用于跨系统匹配客户的多个身份。

在 [!DNL Adobe Journey Optimizer], **标识** 链接跨设备和渠道的用户，结果是 [身份图](#id-graph). 链接的身份图用于根据您所有业务接触点之间的交互对体验进行个性化。

![](assets/identities-home.png)

详细了解 **Identity Service** in [本文档](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

## 身份命名空间 {#identity-namespaces}

****&#x200B;身份命名空间是 Identity Service 的组件，充当与身份相关的上下文指示器。例如，它们会将 `name@email.com` 作为电子邮件地址或 `443522` 作为数字CRM ID。 使用身份命名空间需要了解所涉及的各种Adobe Experience Platform服务。 开始使用命名空间之前，请查阅以下服务的文档：

详细了解 **身份命名空间** in [本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hans){target=&quot;_blank&quot;}。

## 身份图{#id-graph}

的 **身份图** 是特定客户不同身份之间关系的映射，可直观地展示客户如何跨不同渠道与您的品牌进行交互。 所有客户身份图表都由Adobe Experience Platform Identity Service近乎实时地进行集体管理和更新，以响应客户活动。

中的身份图查看器 [!DNL Adobe Journey Optimizer] 通过用户界面，您可以可视化并更好地了解将哪些客户身份拼合在一起，以及通过哪些方式拼合在一起。 查看器允许您拖动图形的不同部分并与之交互，从而允许您检查复杂的身份关系、更高效地进行调试，并从信息的使用方式提高透明度中受益。

详细了解 **身份图** in [本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}。
