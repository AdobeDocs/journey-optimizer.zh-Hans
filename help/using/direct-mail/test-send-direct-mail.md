---
solution: Journey Optimizer
product: journey optimizer
title: 检查和发送直邮消息
description: 了解如何在Journey Optimizer中检查和发送直邮消息
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
TQID: https://experienceleague.adobe.com/4GZKFKOx-D-RT1mssiV5vpmZQSJGVbGMro8Q-suhtPE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 2f3a44b2366119c84e52861db09054f22d55623d
workflow-type: tm+mt
source-wordcount: 829
ht-degree: 11%

---

# 检查和发送直邮消息 {#direct-mail-test-send}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;预览提取文件，验证并激活您的营销活动或历程，以及管理邮政同意，以便您的直邮能够准确地送达正确的收件人。

>[!ENDSHADEBOX]

了解如何在Journey Optimizer中预览提取文件、验证和激活直邮营销活动或旅程，以及管理邮政邮件同意。

## 开始之前 {#before-you-start}

在测试和发送直邮邮件之前，[创建邮件并配置提取文件](create-direct-mail.md)。 确保您也已完成[直邮渠道配置](direct-mail-configuration.md)。

## 预览提取文件 {#preview-dm}

定义提取文件的内容后，使用任一模拟方法进行预览：

* 单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;以测试内容变体与样本输入数据或AI自动生成。 [了解如何模拟内容变体](../test-approve/simulate-sample-input.md)
* 单击&#x200B;**[!UICONTROL 模拟内容]**，然后从下拉列表中选择&#x200B;**[!UICONTROL 模拟内容（AEP配置文件）]**，并添加测试配置文件以检查提取文件呈现的方式。

有关如何预览和测试内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

![模拟直邮提取文件的内容预览](assets/direct-mail-simulate.png){width="800" align="center"}

文件内容准备好发送后，关闭模拟屏幕，然后单击&#x200B;**[!UICONTROL 查看以激活]**&#x200B;按钮。

## 验证并激活直邮营销活动 {#dm-validate}

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能发送直邮营销活动。 [了解详情](../test-approve/gs-approval.md)

在激活直邮营销活动之前，请确保正确配置了营销活动或历程以及提取文件。 要实现此目的，请检查编辑器上部分中的警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告**&#x200B;参考推荐和最佳实践。 例如，如果短信消息为空，则会显示警告消息。

* **错误**&#x200B;阻止您发布营销活动，前提是未解决这些错误。 例如，当主题行缺失时，会有一条错误消息警告您。

![查看并激活显示直邮营销活动验证警报的屏幕](assets/direct-mail-review.png){width="800" align="center"}

当直邮营销活动准备就绪时，请完成[历程](../building-journeys/journey-gs.md)或[营销活动](../campaigns/create-campaign.md)的配置以发送它。

>[!NOTE]
>
>默认情况下，导出的文件以换行结束。 这可确保与标准数据处理工具的兼容性。

发送后，您可以在报表中衡量直邮营销活动或旅程的影响。 有关直邮报告的更多信息，请参阅以下章节：
* [直邮营销活动报告](../reports/campaign-global-report-cja-direct.md)
* [直邮历程报告](../reports/journey-global-report-cja-direct.md)

## 了解导出时间和文件生成 {#dm-export-timing}

直邮导出在&#x200B;**02:01**、**06:01**、**10:01**、**14:01**、**18:01**&#x200B;和&#x200B;**22:01**&#x200B;处按固定4小时UTC周期运行。

用户档案到达直邮活动后，即包含在&#x200B;*下一个*&#x200B;导出周期中。 这意味着文件创建基于用户档案到达直邮节点的时间，而不是营销活动或历程首次激活的时间。

* **为什么一天内可以收到多个文件** — 如果配置文件在不同的四小时窗口中到达直邮活动，Journey Optimizer将为每个窗口生成单独的导出文件。 这是预期行为。

  例如：

   * 在&#x200B;**14:01**&#x200B;之前到达的用户档案将在&#x200B;**14:01**&#x200B;导出。
   * 从&#x200B;**14:02**&#x200B;到&#x200B;**18:01**&#x200B;的配置文件导出时间为&#x200B;**18:01**。

  这不会复制用户档案，而是按到达窗口对它们进行分批。

* **更新配置文件活动计时** — 在历程中，当配置文件到达历程运行时，**[!UICONTROL 更新配置文件]**&#x200B;活动会立即在历程运行时执行。 它不会等待直邮导出周期。

* **针对每天一个文件方案的建议** — 如果您每天需要一个文件，请考虑以下选项：

   * **24小时路由频率**：保证每天有一个文件，但会导致传递延迟。
   * **等待时间**：可以将配置文件调整到相同的导出窗口，但结果取决于历程计时。
   * **4小时路由频率**：提供最低的延迟，但每天可能会生成多个文件。

## 管理直邮的同意 {#dm-consent-management}

在 [!DNL Journey Optimizer] 中，同意由 Experience Platform [同意架构](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hans){target="_blank"}处理。 默认情况下，同意字段的值为空，并视为同意接收您的通信。

如果某个用户档案已选择不接收直邮，则在相应的Experience Platform用户档案属性中，`consents.marketing.postalMail.val`的值将为`n`，并且相应的用户档案将从后续投放中排除。

若要再次启用它，必须将配置文件属性更改回`consents.marketing.postalMail.val` ： `y`。

要管理配置文件的属性，请转到Experience Platform，并通过选择身份命名空间和相应的身份值访问配置文件。 在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}中了解更多信息。

在[本节](../privacy/opt-out.md)中了解有关在Journey Optimizer中管理选择退出的更多信息。

## 相关主题 {#related-topics}

* [直邮快速入门](get-started-direct-mail.md)
* [创建直邮消息](create-direct-mail.md)
* [配置直邮渠道](direct-mail-configuration.md)
* [预览和测试内容](../content-management/preview-test.md)

有关直邮的常见问题，请参阅[直邮入门](get-started-direct-mail.md)。
