---
solution: Journey Optimizer
product: journey optimizer
title: 将Google TXT记录添加到子域
description: 了解如何将Google TXT记录添加到子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 将Google TXT记录添加到子域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT记录"
>abstract="为确保将电子邮件成功发送到Gmail地址，您可以向子域添加特殊的Google网站验证TXT记录，以确保对其进行验证。"

TXT记录是一种DNS记录类型，用于提供域的文本信息，外部源可读取该信息。

为确保电子邮件的最佳投放能力和成功投放到Gmail地址， [!DNL Journey Optimizer] 允许您向子域添加特殊的Google网站验证TXT记录，以确保对其进行验证。

>[!CAUTION]
>
> 仅当子域具有 **[!UICONTROL Success]** 状态。 有关子域状态的更多信息，请参阅 [此部分](about-subdomain-delegation.md#access-delegated-subdomains).

要将Google TXT记录添加到子域，请执行以下步骤：

1. 从 **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 菜单。

1. 在 **[!UICONTROL Google txt record]** ，输入从 [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->，然后单击 **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. 添加TXT记录后，需要通过Google验证该记录。 为此，请导航至 [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->，然后启动验证步骤。
