---
solution: Journey Optimizer
product: journey optimizer
title: 设计电子邮件
description: 了解如何设计电子邮件
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 电子邮件、设计、库存、资源
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 89%

---

# 电子邮件设计入门 {#get-started-content-design}

您可以在 [!DNL Journey Optimizer] 中导入现有内容或利用内容设计功能：

* 使用[!DNL Journey Optimizer]**电子邮件设计功能**，设计或导入响应式电子邮件。[了解详情](content-from-scratch.md)

* 利用 **Adobe Experience Manager Assets Essentials** 来丰富您的电子邮件，构建和管理自己的资源数据库。[了解详情](../integrations/assets.md)

* 查找 **Adobe Stock 照片**&#x200B;以构建内容并改进电子邮件设计。[了解详情](../integrations/stock.md)

* 根据客户的轮廓属性创建个性化的动态消息以增强客户体验。详细了解[个性化](../personalization/personalize.md)和[动态内容](../personalization/get-started-dynamic-content.md)。

➡️ [通过观看视频了解此功能](#video)

## 电子邮件设计最佳实践 {#best-practices}

在发送电子邮件时，请务必考虑到收件人可能会转发它们，而这有时会导致电子邮件的呈现出现问题。当使用电子邮件提供商可能不支持用于转发的CSS类时，尤其是当使用“is-desktop-hidden”CSS类隐藏移动设备上的图像时，更是如此。

为了最大限度地减少这些呈现问题，我们建议尽可能简化电子邮件设计结构。请尝试使用适用于桌面和移动设备的单个设计，并避免使用复杂的 CSS 类或其他设计元素，可能并非所有电子邮件客户端都完全支持这些元素。遵循这些最佳实践有助于您确保电子邮件均能始终如一地正确呈现，无论收件人如何查看或转发电子邮件。

有关电子邮件设计的最佳实践，请参阅下表：

| 推荐 | 谨慎使用 | 不推荐 |
|-|-|-|
| <ul><li>用于结构的<b>基于表的静态布局</b></li> <li>用于保持布局一致性的 <b>HTML 表和嵌套表</b></li> <li>介于 600px 和 800px 之间的<b>模板宽度</b> </li> <li>用于设置样式的<b>简单内联 CSS</b> </li> <li>用于实现通用兼容性的 <b>Web 安全字体</b></li> | <ul><li>某些电子邮件平台可能不显示<b>背景图像</b>。</li><li><b>自定义 Web 字体</b>缺少通用支持。</li><li><b>宽布局</b>在较小的屏幕上显示效果不佳。</li><li><b>图像映射</b>提供有限的功能。</li><li><b>嵌入式 CSS</b> 在电子邮件投放期间有时会被删除。</li> | <ul><li>电子邮件环境中通常不支持 <b>JavaScript</b>。</li> <li> 大多数平台会阻止 <b>`<iframe>`</b> 标记。 </li> <li><b>Flash</b> 已过期，不再受支持。</li> <li><b>嵌入式音频</b>经常无法播放。</li> <li><b>嵌入式视频</b>与许多电子邮件平台不兼容。</li> <li> <b>表单</b>无法在电子邮件中运行。</li> <li> `<div>` 分层可能会导致渲染问题。</li> |

## 创建电子邮件内容的关键步骤 {#key-steps}

将[电子邮件添加](create-email.md)到历程或营销活动后，您便可以开始创建电子邮件内容。

1. 在历程或营销活动配置屏幕中，浏览&#x200B;**[!UICONTROL 编辑内容]**&#x200B;屏幕，访问“电子邮件设计器”。[了解详情](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. 在“电子邮件设计器”主页上，从以下选项中选择设计电子邮件的方式：

   * **通过Email Designer的界面从头开始设计电子邮件**，并利用[Adobe Experience Manager Assets](../integrations/assets.md)中的图像。 要了解如何设计电子邮件内容，请参阅[此部分](content-from-scratch.md)。

   * **直接在Email Designer中编码或粘贴原始HTML**。 要了解如何编码自己的内容，请参阅[此部分](code-content.md)。

     >[!NOTE]
     >
     >在营销活动中，您还可以选择&#x200B;**[!UICONTROL 编辑内容]**&#x200B;屏幕中的&#x200B;**[!UICONTROL 代码编辑器]**&#x200B;按钮。[了解详情](create-email.md#define-email-content)

   * 从文件或 .zip 文件夹&#x200B;**导入现有 HTML 内容**。要了解如何导入电子邮件内容，请参阅[此部分](existing-content.md)。

   * 从内置或自定义模板列表中&#x200B;**选择现有内容**。要了解如何使用电子邮件模板，请参阅[此部分](../email/use-email-templates.md)。

   ![](assets/email_designer_create_options.png)

1. 定义并个性化电子邮件内容后，即可导出内容以供验证或稍后使用。单击&#x200B;**[!UICONTROL 导出 HTML]** 在计算机上保存一个 zip 文件，其中将包含您的 HTML 和资源。

   ![](assets/email_designer_export.png)

## 操作说明视频 {#video}

了解如何使用消息编辑器创建电子邮件内容。

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)

了解如何配置内容试验以进行 A/B 测试，并探索电子邮件内容以最有效地推动业务目标的实现。

>[!VIDEO](https://video.tv.adobe.com/v/3419893)
