---
title: 检查并发送直邮消息
description: 了解如何在Journey Optimizer中检查和发送直邮消息
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 2%

---

# 检查并发送直邮消息 {#direct-mail-test-send}

## 预览提取文件 {#preview-dm}

定义提取文件的内容后，您可以使用测试用户档案进行预览。 如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

为此，请单击&#x200B;**[!UICONTROL 模拟内容]**，然后添加测试配置文件以检查如何使用测试配置文件数据呈现提取文件。

![](assets/direct-mail-simulate.png){width="800" align="center"}

有关如何选择测试用户档案和预览内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

文件内容准备好发送后，关闭模拟屏幕，然后单击&#x200B;**[!UICONTROL 查看以激活]**&#x200B;按钮。

## 验证并激活直邮营销活动 {#dm-validate}

在激活直邮营销活动之前，请确保正确配置了营销活动和提取文件。 要实现此目的，请检查编辑器上部分中的警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告**&#x200B;参考推荐和最佳实践。 例如，如果短信消息为空，则会显示警告消息。

* **错误**&#x200B;阻止您发布营销活动，前提是未解决这些错误。 例如，当主题行缺失时，会有一条错误消息警告您。

![](assets/direct-mail-review.png){width="800" align="center"}

当直邮营销活动就绪时，单击&#x200B;**[!UICONTROL 激活]**&#x200B;按钮。 活动启动时，将自动生成提取文件并将其导出到[文件路由配置](../direct-mail/direct-mail-configuration.md)中指定的服务器。

发送后，您可以在营销活动报表中衡量直邮营销活动的影响。 有关报告的更多信息，请参阅此章节。

## 管理直邮的同意 {#dm-consent-management}

在 [!DNL Journey Optimizer] 中，同意由 Experience Platform [同意架构](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hans){target="_blank"}处理。默认情况下，“同意”字段的值为空，并视为同意接收您的通信。

如果某个用户档案已选择不接收直邮，则在相应的Experience Platform用户档案属性中，`consents.marketing.postalMail.val`的值将为`n`，并且相应的用户档案将从后续投放中排除。

若要再次启用它，必须将配置文件属性更改回`consents.marketing.postalMail.val` ： `y`。

要管理配置文件的属性，请转到Experience Platform，然后通过选择身份命名空间和相应的身份值来访问配置文件。 请参阅[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}以了解详情。

在[本节](../privacy/opt-out.md)中了解有关在Journey Optimizer中管理选择退出的更多信息。
