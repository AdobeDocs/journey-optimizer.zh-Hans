---
title: 预览和测试内容
description: 了解如何预览和测试您的内容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: a5eacd7a746b2f17804062b23aee3146db0434c9
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 24%

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

## 关于预览和测试 {#about}

定义内容后，您可以在发送消息之前预览其内容。 这是确保准确且无内容错误和个性化设置错误的关键步骤。

您还可以将电子邮件的测试投放发送给特定收件人或订阅者，以进行测试和验证，并检查它们在常用桌面、移动和基于Web的客户端中的呈现方式。

>[!CAUTION]
>
>预览消息或发送校样时，仅显示用户档案个性化数据。 基于上下文数据（如事件信息）的Personalization只能在历程的上下文中测试。 了解如何在[此用例](../personalization/personalization-use-case.md)中测试个性化。

所有这些操作都可以使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮来执行，该按钮可从消息的编辑内容屏幕访问，或从电子邮件和Web渠道设计器访问。

![](../email/assets/email-preview-button.png)

请注意，您需要在&#x200B;**[!DNL Content Library Manager]**&#x200B;产品配置文件中包含&#x200B;**[!DNL Manage Simulate Content]**&#x200B;权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)。

## 使用测试用户档案或样本输入数据进行测试 {#methods}

您可以使用以下代码预览和测试内容：

* **测试用户档案**

  使用测试用户档案来预览内容，发送电子邮件校样并检查电子邮件渲染。 如果您添加了个性化字段，则可以使用测试用户档案数据检查这些字段的显示方式。 有关更多信息，请参阅以下章节：

  ➡️[选择测试配置文件](test-profiles.md)

  ➡️[使用测试配置文件预览您的内容](preview.md)

  ➡️[发送电子邮件校样](proofs.md)

  ➡️[检查电子邮件渲染](rendering.md)

  ➡️[预览和验证您的电子邮件（视频）](#video-preview)

* **示例输入数据**

  [!DNL Journey optimizer]允许您使用从CSV/JSON文件上传或手动添加的示例输入数据预览内容并发送校样，从而测试内容的不同变体。

  系统会自动检测内容中用于个性化的所有用户档案属性，可使用这些属性进行测试以创建多个变体。

  ➡️[了解如何使用示例输入数据测试内容](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >此功能目前仅作为电子邮件、短信和推送通知渠道的公共测试版向所有客户提供。

## 操作方法视频 {#video-preview}

了解如何使用测试用户档案测试收件箱中的电子邮件呈现，根据测试用户档案预览个性化电子邮件并发送校样。

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
