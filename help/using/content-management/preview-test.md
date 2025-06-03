---
title: 预览和测试内容
description: 了解如何预览和测试内容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: ht
source-wordcount: '500'
ht-degree: 100%

---

# 预览和测试内容 {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="检查您的内容的渲染方式"
>abstract="定义内容后可使用测试轮廓预览它，并根据所使用的渠道检查渲染是否正确。"

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="检查您的内容的渲染方式"
>abstract="定义内容后可预览它，并根据所使用的渠道检查渲染是否正确。"

定义内容后，您可以在发送消息之前预览其内容。这是确保内容和个性化设置准确无误的关键步骤。

您还可以将电子邮件消息的测试投放发送给特定收件人或订阅者，以进行测试和验证，并查看它们在常用桌面设备、移动设备和 Web 客户端中的渲染情况。

可以使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮来执行所有这些操作，您可以从消息的编辑内容屏幕访问该按钮，或从电子邮件和 Web 渠道的电子邮件和 Web 设计器访问该按钮。

![](../email/assets/email-preview-button.png)

## 使用测试轮廓数据或样本输入数据进行测试 {#methods}

Journey Optimizer 提供两种测试内容的方法：

* **使用测试轮廓数据测试内容**

  您可以使用测试轮廓来预览内容，发送电子邮件校样并检查电子邮件呈现情况。如果您添加了个性化字段，则可以使用测试轮廓数据检查它们的显示方式。有关详细信息，请参阅以下部分：

  ➡️ [选择测试轮廓](test-profiles.md)
➡️ [使用测试轮廓预览](preview.md)
➡️ [发送电子邮件校样](proofs.md)
➡️ [检查电子邮件呈现情况](rendering.md)
➡️ [预览和验证电子邮件（视频）](#video-preview)

* **使用样本输入数据测试内容变体**

  [!DNL Journey optimizer] 可以让您使用从 CSV 或 JSON 文件上传或手动添加的示例输入数据针对内容的不同变体预览和发送校样。

  系统会自动检测内容中用于个性化的所有轮廓属性，可使用这些属性进行测试以创建多个变体。

  ➡️ [模拟内容变体](../test-approve/simulate-sample-input.md)

## 必读

* **需要的权限** - 您需要在 **[!DNL Content Library Manager]** 产品配置文件中授予 **[!DNL Manage Simulate Content]** 权限。[了解详情](../administration/ootb-product-profiles.md#content-library-manager)。

  要发送校样，您必须对与电子邮件关联的特定资源（营销活动或历程）具有&#x200B;**批准和发布**&#x200B;权限。此外，要在历程中发送校样，还需要有&#x200B;**发布历程**&#x200B;的权限。[了解有关权限的更多信息](../administration/ootb-permissions.md)。

* **使用上下文数据的个性化** - 预览消息或发送校样时，仅显示轮廓个性化数据。只能在历程上下文中测试基于上下文数据（如事件信息）的个性化。在[此用例](../personalization/personalization-use-case.md)中了解更多信息。

* **预览具有多个条件变量的内容** - 模拟或呈现包含多个条件变量的电子邮件校样时，Journey Optimizer 可能需要更长的处理时间。如果出现超时或错误消息，请考虑减少变体的总数或简化条件规则。在[此页面](../personalization/dynamic-content.md)中详细了解条件内容。

## 操作方法视频 {#video-preview}

了解如何使用测试用户档案测试不同收件箱中的电子邮件渲染情况，根据测试用户档案预览个性化电子邮件并发送验证。

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
