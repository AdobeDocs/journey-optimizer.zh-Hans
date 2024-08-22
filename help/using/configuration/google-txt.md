---
solution: Journey Optimizer
product: journey optimizer
title: 将 Google TXT 记录添加到子域
description: 了解如何将Google TXT记录添加到子域
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子域， google， txt，记录， gmail，可投放性
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 30%

---

# 将 Google TXT 记录添加到子域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 记录"
>abstract="为确保将电子邮件成功发送到 Gmail 地址，您可以将专门的 Google 网站验证 TXT 记录添加到您的子域中，以确保该地址已通过验证。"

TXT记录是一种DNS记录，用于提供有关域的文本信息，外部源可以读取该信息。

为了确保电子邮件的最佳传递性并成功投放到Gmail地址，[!DNL Journey Optimizer]允许您向子域添加特殊的Google网站验证TXT记录，以确保对其进行验证。

>[!CAUTION]
>
> 仅当子域处于&#x200B;**[!UICONTROL 成功]**&#x200B;状态时，才能执行此操作。 有关子域状态的详细信息，请参阅[此部分](about-subdomain-delegation.md#access-delegated-subdomains)。

要将Google TXT记录添加到子域，请执行以下步骤：

1. 从&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 子域]**&#x200B;菜单打开子域。

1. 在&#x200B;**[!UICONTROL Google txt记录]**&#x200B;部分中，输入从[Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->生成的验证代码，然后单击&#x200B;**[!UICONTROL 保存]**。

   ![](assets/subdomain-google-txt.png)

1. 添加 TXT 记录后，需要通过 Google 验证该记录。为此，请导航到[Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然后启动验证步骤。
