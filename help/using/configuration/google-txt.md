---
title: 委派子域
description: 了解如何委派子域
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: 2d8b7bbaee7509d4cc33445c64b2382ed14a9678
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 24%

---


# 将Google TXT记录添加到子域

TXT 记录是一种 DNS 记录类型，用于提供有关域的文本信息，外部源可以读取该信息。

为确保电子邮件的良好传递性和成功投放到Gmail地址，客户历程管理允许您向子域添加特殊的Google网站验证TXT记录，以确保对其进行验证。

>[!NOTE]
>
> 只有在子域具有&#x200B;**[!UICONTROL Success]**&#x200B;状态时，才能执行此操作。 有关子域状态的更多信息，请参阅[此部分](access-subdomains.md)。

要将Google TXT记录添加到子域，请执行以下步骤：

1. 从&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**&#x200B;菜单中打开子域。

1. 在Google txt记录部分中，输入在[G Suite管理工具](https://support.google.com/a/answer/183895)中生成的验证代码，然后单击&#x200B;**[!UICONTROL Save]**。

   ![](../assets/subdomain-google-txt.png)

1. 添加 TXT 记录后，需要通过 Google 验证该记录。为此，请导航到G Suite管理员工具，然后启动验证步骤。
