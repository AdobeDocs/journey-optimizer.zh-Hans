---
solution: Journey Optimizer
product: journey optimizer
title: 测试内容模板
description: 了解如何测试某些电子邮件内容模板的呈现
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 6%

---

# 测试电子邮件内容模板 {#test-template}

您可以测试某些电子邮件模板的呈现，无论是从草稿还是从现有内容创建。 要实现此目的，请执行以下步骤。

1. 通过&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 内容模板]**&#x200B;菜单访问内容模板列表，然后选择任意电子邮件模板。

1. 从&#x200B;**[!UICONTROL 模板属性]**&#x200B;中单击&#x200B;**[!UICONTROL 编辑内容]**。

1. 单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;并选择测试配置文件以检查您的渲染。 [了解详情](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. 您可以发送校样以测试您的内容，并在将其用于历程或营销策划之前，先获得一些内部用户的批准。

   * 为此，请单击&#x200B;**[!UICONTROL 发送校样]**&#x200B;按钮，然后按照[此部分](../content-management/proofs.md)中描述的步骤操作。

   * 在发送校样之前，必须选择将用于测试内容的[电子邮件表面](../configuration/channel-surfaces.md)。

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>当前在测试电子邮件内容模板时不支持跟踪，这意味着跟踪事件、UTM参数和登陆页面链接将在从模板发送的验证中无效。 若要测试跟踪，[在电子邮件中使用内容模板](../email/use-email-templates.md)并[发送校样](../content-management/preview-test.md#send-proofs)。