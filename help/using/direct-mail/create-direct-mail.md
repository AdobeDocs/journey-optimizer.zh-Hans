---
title: 创建直邮消息
description: 了解如何在 Journey Optimizer 中创建直邮消息
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 直邮、消息、营销活动
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 3fdfc98c0049f39d12b1cb2241fde892f449cdc1
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 15%

---

# 创建直邮消息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直邮创建"
>abstract="在计划的营销活动和历程中创建直邮消息，并设计直邮提供商向您的客户发送邮件所需的提取文件。"

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="结束活动"
>abstract="直邮是一种离线渠道，允许您生成第三方直邮服务提供商向客户发送邮件所需的提取文件并进行个性化设置。"

要创建直邮消息，请创建计划的活动或历程，并配置提取文件。 直邮提供商需要此文件向客户发送邮件。

>[!IMPORTANT]
>
>在创建直邮消息之前，请确保已配置：
>
>1. [文件路由配置](../direct-mail/direct-mail-configuration.md#file-routing-configuration)，它指定提取文件应上载和存储的服务器，
>1. 将引用文件路由配置的[直邮邮件配置](../direct-mail/direct-mail-configuration.md#direct-mail-surface)。

## 添加直邮消息 {#create-dm-campaign}

浏览以下选项卡，了解如何在营销活动或历程中添加直邮消息。

>[!BEGINTABS]

>[!TAB 向历程添加直邮邮件]

1. 打开您的历程，然后从调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分拖放&#x200B;**直邮**&#x200B;活动。

1. 提供有关消息的基本信息（标签、说明、类别），然后选择要使用的消息配置。 默认情况下，**[!UICONTROL 配置]**&#x200B;字段已预填充用户用于该渠道的最后一个配置。 有关如何配置历程的详细信息，请参阅[此页面](../building-journeys/journey-gs.md)。

1. 配置要发送给直邮提供商的提取文件。 为此，请单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮。

   ![](assets/direct-mail-add-journey.png)

1. 调整提取文件属性，如文件名或要显示的列。 有关如何配置提取文件属性的详细信息，请参阅以下部分：[创建直邮邮件](../direct-mail/create-direct-mail.md#extraction-file)。

   ![](assets/direct-mail-journey-content.png)

1. 定义提取文件的内容后，您可以使用测试用户档案进行预览。 如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

   为此，请单击&#x200B;**[!UICONTROL 模拟内容]**，然后添加测试配置文件以检查如何使用测试配置文件数据呈现提取文件。 有关如何选择测试用户档案和预览内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

提取文件准备就绪后，完成[历程](../building-journeys/journey-gs.md)的配置以发送该文件。

>[!TAB 向营销活动添加直邮消息]

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择&#x200B;**计划 — 营销**&#x200B;营销活动类型。

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;部分中，编辑营销活动的&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 要定义目标受众，请单击“选择受众”**[!UICONTROL 按钮]**，然后从可用的Adobe Experience Platform受众中进行选择。 [了解详情](../audience/about-audiences.md)。

   >[!IMPORTANT]
   >
   >目前，受众选择限制为300万个配置文件。 根据向Adobe代表提出的请求，可取消此限制。

1. 在&#x200B;**[!UICONTROL 身份命名空间]**&#x200B;字段中，选择适当的命名空间以识别所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 直邮]**。

1. 选择或创建要使用的&#x200B;**[!UICONTROL 直邮配置]**。 [了解如何创建直邮配置](direct-mail-configuration.md#direct-mail-surface)。

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

   >[!AVAILABILITY]
   >
   >直邮支持&#x200B;**保留**&#x200B;功能，但目前不支持&#x200B;**处理**。 [了解如何使用实验](../content-management/get-started-experiment.md)

1. 营销活动可以计划为特定日期，也可以设置为定期重复。 在&#x200B;**[!UICONTROL 本节]**&#x200B;中了解如何配置促销活动的[计划](../campaigns/campaign-schedule.md)。

您现在可以开始配置要发送给直邮提供商的提取文件。

>[!ENDTABS]

## 配置提取文件 {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="数据字段"
>abstract="添加并配置要在直邮提供商将电子邮件发送到您的客户时所需的提取文件中显示的列和信息。最多可以添加 50 个列。"

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="提取文件格式"
>abstract="对于每个字段，使用个性化编辑器指定一个标签和要显示的信息。<br/><br/>通过<b>排序方式</b>选项，可使用所选字段为提取文件的列排序。"

直邮提供商需要使用提取文件向客户发送邮件。 要定义提取文件配置，请执行以下步骤：

1. 在Campaign配置屏幕中，单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮以配置提取文件内容。

1. 调整提取文件属性：

   1. 在&#x200B;**[!UICONTROL 文件名]**&#x200B;字段中，指定提取文件的名称。

      >[!NOTE]
      >
      >默认情况下，该文件将写入服务器上的根目录中。 **[!UICONTROL Filename]**&#x200B;字段也接受格式“/your/path/here/Filename.csv”，其中指定的路径是所选服务器上的目标目录。<!--TBC if for SFTP and Azure only, or for all servers including S3-->

   1. 如果要向指定的文件名添加自动时间戳，请启用&#x200B;**[!UICONTROL 附加时间戳以导出文件名]**&#x200B;选项。

   1. 有时您可能需要在提取文件的开头或结尾添加信息。为此，请使用&#x200B;**[!UICONTROL 注释]**&#x200B;字段，然后指定是否要将该注释包含为页眉或页脚。

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. 配置要在提取文件中显示的列和信息：

   1. 单击&#x200B;**[!UICONTROL 添加]**&#x200B;按钮以创建新列。

   1. **[!UICONTROL 格式化]**&#x200B;窗格显示在右侧，允许您设置所选列。 为列指定&#x200B;**[!UICONTROL 标签]**。

   1. 在&#x200B;**[!UICONTROL 数据]**&#x200B;字段中，使用[个性化编辑器](../personalization/personalization-build-expressions.md)选择要显示的配置文件属性。

   1. 要使用列对提取文件排序，请选择该列并打开&#x200B;**[!UICONTROL 排序方式]**&#x200B;选项。 **[!UICONTROL 排序依据]**&#x200B;图标显示在&#x200B;**[!UICONTROL 数据字段]**&#x200B;部分中的列标签旁边。

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. 重复这些步骤以根据需要为提取文件添加任意数量的列。 请注意，最多可添加50列。

      要更改列的位置，请将其拖放到&#x200B;**[!UICONTROL 数据字段]**&#x200B;节中的所需位置。 要删除列，请选择该列，然后单击&#x200B;**[!UICONTROL 格式化]**&#x200B;窗格中的&#x200B;**[!UICONTROL 删除]**&#x200B;按钮。

您现在可以测试直邮消息并将其发送给受众。 [了解如何测试和发送直邮邮件](test-send-direct-mail.md)
