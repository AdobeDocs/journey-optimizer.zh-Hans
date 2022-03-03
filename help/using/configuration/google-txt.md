---
title: 将Google TXT记录添加到子域
description: 了解如何将Google TXT记录添加到子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 7c9f04b8d3faa171444bfa0adc537b5faabde37e
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 26%

---

# 将Google TXT记录添加到子域 {#google-txt-record}

TXT 记录是一种 DNS 记录类型，用于提供有关域的文本信息，外部源可以读取该信息。

为确保电子邮件的良好投放能力和成功投放到Gmail地址， [!DNL Journey Optimizer] 允许您向子域添加特殊的Google站点验证TXT记录，以确保对其进行验证。

>[!CAUTION]
>
> 仅当子域具有 **[!UICONTROL Success]** 状态。 有关子域状态的更多信息，请参阅 [此部分](access-subdomains.md).

要将Google TXT记录添加到子域，请执行以下步骤：

1. 从 **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 菜单。

1. 在 **[!UICONTROL Google txt record]** ，输入从 [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->，然后单击 **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. 添加 TXT 记录后，需要通过 Google 验证该记录。为此，请导航至 [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->，然后启动验证步骤。
