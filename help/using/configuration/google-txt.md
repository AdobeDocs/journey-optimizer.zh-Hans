---
solution: Journey Optimizer
product: journey optimizer
title: 將Google TXT記錄新增至子網域
description: 瞭解如何將Google TXT記錄新增至子網域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子網域， google， txt，記錄， gmail，傳遞能力
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 24%

---

# 將Google TXT記錄新增至子網域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 记录"
>abstract="为确保将电子邮件成功发送到 Gmail 地址，您可以将专门的 Google 网站验证 TXT 记录添加到您的子域中，以确保该地址已通过验证。"

TXT記錄是一種DNS記錄，用於提供關於網域的文字資訊，可以由外部來源讀取。

為了確保最佳傳遞能力並成功傳遞電子郵件至Gmail地址， [!DNL Journey Optimizer] 可讓您新增特殊的Google網站驗證TXT記錄至您的子網域，以確保其經過驗證。

>[!CAUTION]
>
> 只有在子網域具有 **[!UICONTROL 成功]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

若要將Google TXT記錄新增至子網域，請遵循下列步驟：

1. 從開啟子網域 **[!UICONTROL 頻道]** / **[!UICONTROL 子網域]** 功能表。

1. 在 **[!UICONTROL Google txt記錄]** 區段，輸入產生的驗證碼 [Google工作區](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/subdomain-google-txt.png)

1. 添加 TXT 记录后，需要通过 Google 验证该记录。若要這麼做，請導覽至 [Google工作區](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後啟動驗證步驟。
