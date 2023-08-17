---
solution: Journey Optimizer
product: journey optimizer
title: 将Google TXT记录添加到子域
description: 了解如何将Google TXT记录添加到子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子域， google， txt，记录， gmail，可投放性
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 24%

---

# 将Google TXT记录添加到子域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 记录"
>abstract="为确保将电子邮件成功发送到 Gmail 地址，您可以将专门的 Google 网站验证 TXT 记录添加到您的子域中，以确保该地址已通过验证。"

TXT记录是一种DNS记录，用于提供有关域的文本信息，外部源可以读取该信息。

为了确保最佳可投放性并成功将电子邮件投放到Gmail地址， [!DNL Journey Optimizer] 允许您向子域添加特殊的Google网站验证TXT记录，以确保其经过验证。

>[!CAUTION]
>
> 仅当子域具有 **[!UICONTROL 成功]** 状态。 有关子域状态的更多信息，请参阅 [本节](about-subdomain-delegation.md#access-delegated-subdomains).

要将Google TXT记录添加到子域，请执行以下步骤：

1. 从打开子域 **[!UICONTROL 渠道]** / **[!UICONTROL 子域]** 菜单。

1. 在 **[!UICONTROL Google txt记录]** 部分，输入生成的验证码 [Google工作区](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然后单击 **[!UICONTROL 保存]**.

   ![](assets/subdomain-google-txt.png)

1. 添加 TXT 记录后，需要通过 Google 验证该记录。为此，请导航至 [Google工作区](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然后启动验证步骤。
