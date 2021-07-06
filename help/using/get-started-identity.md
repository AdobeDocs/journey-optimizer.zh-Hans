---
title: 在Journey Optimizer中开始使用身份
description: 了解如何在Adobe Journey Optimizer中管理身份
feature: 配置文件
role: User
level: Beginner
source-git-commit: e51be6bf18f2e3dfec11e80d34bf63a8ce8b1012
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 6%

---

# 身份入门 {#identities-gs}

身份是实体（通常是个人）特有的数据。 登录ID、ECID或忠诚度ID等身份称为已知身份。

个人身份信息(PII)（如电子邮件地址和电话号码）用于直接识别客户。 因此，PII用于跨系统匹配客户的多个身份。

在[!DNL Adobe Journey Optimizer]、**Identities**&#x200B;中，将跨设备和渠道的用户链接到一起，结果为[标识图](#id-graph)。 链接的身份图用于根据您所有业务接触点之间的交互对体验进行个性化。

![](assets/identities-home.png)

在[本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}中了解有关&#x200B;**Identity Service**&#x200B;的更多信息。

## 身份命名空间

****&#x200B;身份命名空间是 Identity Service 的组件，充当与身份相关的上下文指示器。例如，它们将值`name@email.com`区分为电子邮件地址，或将值`443522`区分为数字CRM ID。 使用身份命名空间需要了解所涉及的各种Adobe Experience Platform服务。 开始使用命名空间之前，请查阅以下服务的文档：

在[本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}中了解有关&#x200B;**身份命名空间**&#x200B;的更多信息。

## 身份图{#id-graph}

**身份图**&#x200B;是特定客户不同身份之间关系的映射，可直观地展示客户如何跨不同渠道与您的品牌进行交互。 所有客户身份图表都由Adobe Experience Platform Identity Service近乎实时地进行集体管理和更新，以响应客户活动。

通过[!DNL Adobe Journey Optimizer]用户界面中的身份图查看器，您可以直观地了解哪些客户身份拼合在一起，以及以哪些方式拼合。 查看器允许您拖动图形的不同部分并与之交互，从而允许您检查复杂的身份关系、更高效地进行调试，并从信息的使用方式提高透明度中受益。

在[本文档](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}中了解有关&#x200B;**标识图**&#x200B;的更多信息。

