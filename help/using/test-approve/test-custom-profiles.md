---
solution: Journey Optimizer
product: journey optimizer
title: 使用样本配置文件测试内容
description: 了解如何使用示例用户档案预览电子邮件内容并发送校样。
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta 版"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 1%

---


# 使用样本配置文件测试内容 {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="使用样本轮廓进行模拟"
>abstract="在此屏幕中，您可以预览电子邮件内容并发送校样，同时模拟可从CSV文件上传或直接从该屏幕手动添加的示例配置文件。"


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>此功能目前仅作为测试版提供给选定用户。

通过历程优化器，您可以使用示例配置文件预览和测试电子邮件内容，这些配置文件可以从CSV文件上传，也可以在模拟内容时直接手动添加。 此功能允许您选择示例用户档案，以用于预览您的内容和发送校样。 系统会自动检测您的内容中用于个性化的所有配置文件属性，这些属性可用于您的测试。

要访问此体验，请单击“模拟内容”按钮&#x200B;****，然后选择“使用CSV(Beta)模拟”****。

![](assets/simulate-sample.png)


测试内容的主要步骤如下：

1. 通过上传CSV文件或手动逐个添加配置文件，添加最多30个示例配置文件。 [了解如何添加样本配置文件](#profiles)
1. 使用添加的用户档案查看内容的预览。 [了解如何预览您的内容](#preview)
1. 在模拟所需的示例配置文件时，向电子邮件地址发送最多10个验证。 [了解如何发送校样](#proofs)


## 护栏和限制 {#limitations}

开始使用示例配置文件测试内容之前，请考虑以下护栏和先决条件。

* 截至目前，使用样本用户档案进行测试仅适用于营销活动，也适用于电子邮件渠道。
* 当前体验中不提供以下功能：收件箱呈现、垃圾邮件报告、多语言内容和内容体验。 若要使用这些功能，请从内容中选择&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮以访问上一个用户界面。
* 当前仅支持配置文件属性。 如果在内容中使用上下文属性进行个性化，您将无法使用这些属性测试内容。
* 为样本配置文件输入数据时仅支持以下数据类型：数字（整数和小数）、字符串、布尔和日期类型。 任何其他数据类型将显示错误。

## 添加样本配置文件 {#profiles}

您最多可以添加30个示例配置文件以使用CSV文件或手动测试您的内容：

* 要从CSV文件上传配置文件，请单击&#x200B;**[!UICONTROL 下载模板]**&#x200B;链接以检索CSV文件模板。 此模板包含一列，其中包含您的内容中用于个性化的每个配置文件属性。

  填写CSV文件，然后单击&#x200B;**[!UICONTROL 上载示例配置文件]**&#x200B;以加载该文件以测试您的内容。

* 要手动添加配置文件，请单击&#x200B;**[!UICONTROL 创建示例配置文件]**&#x200B;按钮并填写配置文件的信息。 在您的内容中用于个性化的每个配置文件属性都显示一个字段。

  ![](assets/simulate-custom-add.png)

选择配置文件后，屏幕左侧会为每个配置文件显示一个框。 您可以使用这些配置文件预览您的内容并发送校样。

>[!NOTE]
>
>添加的示例配置文件仅用作当前内容的测试目的。 不会存储在Adobe Experience Platform中，而是会存储在您的用户浏览器会话中，这意味着在注销或从其他设备工作时，不会显示这些文件。

## 使用示例配置文件预览内容 {#preview}

要使用其中一个用户档案预览内容，请选择相关框以使用为此用户档案输入的信息更新右侧部分中的内容预览。

您可以使用右上角的省略号按钮并选择&#x200B;**[!UICONTROL 删除]**&#x200B;随时删除框。 要编辑用户档案的信息，请单击省略号按钮，然后选择&#x200B;**[!UICONTROL 编辑]**。

![](assets/simulate-custom-boxes.png)

## 发送校样 {#proofs}

Journey Optimizer允许您向电子邮件地址发送验证，同时模拟您在模拟屏幕中添加的一个或多个示例用户档案。 步骤如下：

1. 验证是否已添加样本配置文件以测试您的内容，然后单击&#x200B;**[!UICONTROL 发送校样]**&#x200B;按钮。

1. 在&#x200B;**[!UICONTROL 收件人]**&#x200B;字段中，输入要向其发送校样的电子邮件地址，然后单击&#x200B;**[!UICONTROL 添加]**。 重复操作以将验证发送到其他电子邮件地址。 您最多可以添加10个验证收件人。

1. 在屏幕的底部，选择要模拟到验证中的样本配置文件。 您可以选择多个用户档案，在这种情况下，电子邮件将包含与选定用户档案相同数量的校样。

   有关个人资料的详细信息，请选择&#x200B;**[!UICONTROL 查看个人资料详细信息]**&#x200B;链接。 这允许您显示在上一个屏幕中为不同的配置文件属性输入的信息。

   ![](assets/simulate-custom-proofs.png)

1. 单击&#x200B;**[!UICONTROL 发送校样]**&#x200B;按钮以开始发送校样。

您可以随时通过单击模拟内容屏幕中的&#x200B;**[!UICONTROL 查看校样]**&#x200B;按钮来跟踪发送。

![](assets/simulate-custom-sent-proofs.png)
