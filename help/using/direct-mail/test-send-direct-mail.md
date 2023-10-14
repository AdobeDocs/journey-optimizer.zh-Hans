---
title: 测试并发送直邮消息
description: 了解如何在Journey Optimizer中测试和发送直邮消息
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 12%

---

# 测试并发送直邮消息 {#direct-mail-test-send}

## 预览提取文件 {#preview-dm}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_preview"
>title="提取文件预览"
>abstract="在此窗格中，您可以预览在左窗格中选择的每个测试配置文件的提取文件显示方式。 如果您已插入个性化内容，则可以使用测试配置文件数据检查此内容的显示方式。"

定义提取文件的内容后，您可以使用测试用户档案进行预览。 如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

1. 在提取文件内容配置屏幕中，单击 **[!UICONTROL 模拟内容]**.

   ![](assets/direct-mail-simulate-button.png){width="800" align="center"}

1. 单击 **[!UICONTROL 管理测试用户档案]** 以添加测试用户档案。

1. 使用查找您的测试用户档案 **[!UICONTROL 身份命名空间]** 和 **[!UICONTROL 标识值]** 字段。 然后，单击 **[!UICONTROL 添加配置文件]**.

   ![](assets/direct-mail-test-profile.png){width="800" align="center"}

1. 选择测试用户档案后，您可以关闭 **[!UICONTROL 添加测试配置文件]** 窗口。

1. 从 **预览和测试** 窗口中，测试配置文件数据会添加到提取文件内容，以便您预览文件的呈现方式。

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

一旦文件内容准备好发送，请关闭模拟屏幕，然后单击 **[!UICONTROL 审查以激活]** 按钮。

## 验证并激活直邮营销活动 {#dm-validate}

在激活直邮营销活动之前，请确保正确配置了营销活动和提取文件。 要实现此目的，请检查编辑器上部分中的警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告** 请参阅建议和最佳实践。 例如，如果短信消息为空，则会显示警告消息。

* **错误** 阻止发布营销活动，前提是未解决营销活动。 例如，当主题行缺失时，会有一条错误消息警告您。

![](assets/direct-mail-review.png){width="800" align="center"}

当直邮营销活动就绪时，单击 **[!UICONTROL 激活]** 按钮。 活动启动时，将自动生成提取文件并将其导出到中指定的服务器。 [文件路由配置](../direct-mail/direct-mail-configuration.md).

发送后，您可以在营销活动报表中衡量直邮营销活动的影响。 有关报告的更多信息，请参考此章节。

## 管理直邮的同意 {#dm-consent-management}

在 [!DNL Journey Optimizer] 中，同意由 Experience Platform [同意模式](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hans){target="_blank"}处理。默认情况下，同意字段的值为空，并视为同意接收您的通信。

如果配置文件已选择不接收直邮，则在相应的Experience Platform配置文件属性中，值 `consents.marketing.postalMail.val` 将为 `n` 并且相应的用户档案将从后续投放中排除。

要再次启用它，必须将配置文件属性更改回 `consents.marketing.postalMail.val` ： `y`.

要管理配置文件的属性，请转到Experience Platform，然后通过选择身份命名空间和相应的身份值来访问配置文件。 在中了解详情 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}.

在中了解有关管理Journey Optimizer中的选择退出的更多信息 [本节](../privacy/opt-out.md).
