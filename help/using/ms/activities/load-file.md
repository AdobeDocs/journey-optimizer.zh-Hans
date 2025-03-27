---
solution: Journey Optimizer
product: journey optimizer
title: 使用加载文件活动
description: 了解如何在多步营销活动中使用加载文件活动
hide: true
hidefromtoc: true
exl-id: ae0dc980-2361-4c3b-a68e-ae0bb5dc0a26
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 41%

---

# 加载文件 {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile"
>title="加载文件活动"
>abstract=" **加载文件**&#x200B;活动是一项&#x200B;**数据管理**&#x200B;活动。使用此活动可以处理存储在外部文件中的数据。轮廓和数据不会添加到数据库中，但输入文件中的所有字段均可用于个性化，或更新轮廓或任何其他表。 "

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition"
>title="拒绝管理出站过渡"
>abstract="拒绝管理出站过渡"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition_reject"
>title="针对拒绝的拒绝管理出站过渡"
>abstract="针对拒绝的拒绝管理出站过渡"


 **加载文件**&#x200B;活动是一项&#x200B;**数据管理**&#x200B;活动。使用此活动可使用存储在外部文件中的用户档案和数据。 轮廓和数据不会添加到数据库中，但输入文件中的所有字段均可用于个性化，或更新轮廓或任何其他表。

>[!NOTE]
>支持的文件格式有：文本 (TXT) 和逗号分隔值 (CSV)。您可以加载最大大小为50MB的文件。

此活动可与[协调](reconciliation.md)活动一起使用，以将未识别的数据链接到现有资源。 例如，如果将非标准数据导入数据库，则可以将&#x200B;**加载文件**&#x200B;活动放在&#x200B;**协调**&#x200B;活动之前。

## 配置加载文件活动 {#load-configuration}

**加载文件**&#x200B;活动配置包含两个步骤。 首先，您需要通过上传样例文件来定义预期的文件结构。完成此操作后，您可以指定要导入其数据的文件的来源。 请按照以下步骤配置活动。

![](../assets/workflow-load-file.png)

### 配置示例文件 {#sample}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_samplefile"
>title="示例文件"
>abstract="通过上传示例文件来选择预期的文件结构。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_formatting"
>title="加载文件活动的格式设置"
>abstract="在&#x200B;**格式化**&#x200B;部分，指定文件的格式化方式，以确保正确导入数据。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_valueremapping"
>title="加载文件活动的值重新映射"
>abstract="使用此选项可以将已加载文件中的特定值与新值进行映射。例如，如果列中包含 “True”/“False” 值，则可以通过添加映射来自动用 “0”/“1” 字符替换这些值。"

按照以下步骤配置用于定义预期文件结构的样例文件：

1. 将&#x200B;**加载文件**&#x200B;活动添加到您的多步骤营销活动中。

1. 选择用于定义预期文件结构的样例文件。 为此，请单击&#x200B;**[!UICONTROL 示例文件]**&#x200B;部分中的&#x200B;**选择文件**&#x200B;按钮，然后选择要使用的本地文件。

1. 此时将显示样例文件的预览，最多显示30行。

1. 在&#x200B;**[!UICONTROL 文件类型]**&#x200B;下拉列表中，指定文件使用的是分隔列还是固定宽度列。

   ![](../assets/workflow-load-file-sample.png)

1. 对于分隔列文件类型，请使用&#x200B;**列**&#x200B;部分来配置每个列的属性。

   +++文件列的可用选项

   * **[!UICONTROL 标签]**：为列显示的标签。
   * **[!UICONTROL 数据类型]**：列中包含的数据类型。
   * **[!UICONTROL 宽度]**（字符串数据类型）：列中可显示的最大字符数。
   * **[!UICONTROL 数据转换]**（字符串数据类型）：将转换应用于列中包含的值。
   * **[!UICONTROL 空格管理]** （字符串数据类型）：指定如何管理列中包含的空格。
   * **[!UICONTROL 分隔符]**（日期、时间、整数和数字数据类型）*：指定要用作分隔符的字符。
   * **[!UICONTROL 允许NULL]**：指定如何管理列中的空值。
   * **[!UICONTROL 处理]**&#x200B;时出错（字符串数据类型）：指定其中一行出错时的行为。
   * **[!UICONTROL 值重新映射]**：此选项允许您使用新值映射特定值。 例如，如果列中包含 “True”/“False” 值，则可以通过添加映射来自动用 “0”/“1” 字符替换这些值。

+++

1. 在&#x200B;**格式化**&#x200B;部分，指定文件的格式化方式，以确保正确导入数据。

### 定义要上传的目标文件 {#target}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetfile"
>title="加载文件活动的目标文件"
>abstract="在&#x200B;**[!UICONTROL 目标文件]**&#x200B;部分，指定如何检索要上传到服务器的文件。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_nameofthefile"
>title="文件名称"
>abstract="指定要上传到服务器的字段的名称。单击&#x200B;**[!UICONTROL 打开个性化对话框]**&#x200B;图标，利用表达式编辑器（包括事件变量）来计算文件名称。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetdb"
>title="目标数据库"
>abstract="如果您访问的是已设置的&#x200B;**[!UICONTROL 加载文件]**&#x200B;活动，并且已将该活动配置为将文件上传到外部数据库，则还会有额外的&#x200B;**[!UICONTROL 目标数据库]**&#x200B;部分可用。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_command"
>title="加载文件命令"
>abstract="允许使用任意命令进行预处理会带来安全问题，禁用安全选项 XtkSecurity_Disable_Preproc 可强制使用一系列预定义的命令。"

>[!CAUTION]
>
>在加载目标文件之前，请确保它遵守示例文件格式。 文件格式、列结构或列数的任何差异都可能导致多步骤营销活动执行期间出现错误。

要定义要上传的目标文件，请执行以下步骤：

1. 在&#x200B;**[!UICONTROL 目标文件]**&#x200B;部分中，指定检索要在服务器上上载的文件时要执行的操作。

   * **[!UICONTROL 从本地计算机上传文件]**：选择要从计算机上传的文件。

   * **[!UICONTROL 在过渡中指定]**：上传在集客过渡中指定的文件，该文件即将从以前的活动（如&#x200B;**[!UICONTROL 传输文件]**）上传。

   * **[!UICONTROL 预处理文件]**：上载在上一个转换中指定的文件并对其应用预处理命令，如&#x200B;**[!UICONTROL 解压缩]**&#x200B;或&#x200B;**[!UICONTROL 解密]**。

   * **[!UICONTROL 已计算]**：上载在&#x200B;**[!UICONTROL 文件名]**&#x200B;字段中指定名称的文件。 单击&#x200B;**[!UICONTROL 打开个性化对话框]**&#x200B;图标，利用表达式编辑器（包括事件变量）来计算文件名称。

   ![](../assets/workflow-load-file-config.png)

   >[!NOTE]
   >
   >如果您正在访问已设置的&#x200B;**[!UICONTROL 加载文件]**&#x200B;活动，如果您已将该活动配置为将文件上载到外部数据库，则会显示额外的&#x200B;**[!UICONTROL 目标数据库]**&#x200B;部分。 它允许您指定是将文件上传到Campaign服务器还是外部数据库。

### 其他选项 {#options}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_rejectmgt"
>title="加载文件活动的拒绝管理"
>abstract="在&#x200B;**拒绝管理**&#x200B;部分，指定在出现错误时该活动应如何表现。您可以定义允许的最大错误数，并切换&#x200B;**[!UICONTROL 将拒绝的内容保留在文件中]**&#x200B;选项，以在服务器上下载包含导入期间发生的错误的文件。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_delete"
>title="导入后删除文件"
>abstract="切换&#x200B;**导入后删除文件**，可在导入文件后从服务器中删除原始文件。"


1. 在&#x200B;**拒绝管理**&#x200B;部分中，指定活动在发生错误时的行为方式：

   * 在&#x200B;**[!UICONTROL 允许的错误数]**&#x200B;字段中，指定处理要加载的文件时授权的最大错误数。 例如，如果将该值设置为“20”，则当加载文件时出现20个以上的错误时，多步骤营销活动执行将失败。

   * 若要保留加载文件时发生的错误，请打开&#x200B;**[!UICONTROL Keep rejects in a file]**&#x200B;选项，并在&#x200B;**[!UICONTROL Rejection File]**&#x200B;字段中指定所需的文件名称。

     激活此选项后，在活动后会添加一个名为“补充”的其他输出过渡。 导入期间发生的任何错误都将存储在服务器上的指定文件中。

1. 要在执行多步骤活动后从服务器中删除已上传的文件，请切换&#x200B;**[!UICONTROL 导入后删除文件]**&#x200B;选项。

   ![](../assets/workflow-load-file-options.png)

1. 在确认设置正确后，单击&#x200B;**确认**。

## 示例 {#load-example}

[此部分](reconciliation.md#reconciliation-example)中提供了与&#x200B;**协调**&#x200B;活动一起使用的外部文件加载示例。
