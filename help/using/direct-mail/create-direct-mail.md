---
title: 创建直邮消息
description: 了解如何在Journey Optimizer中创建直邮消息
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 直邮、消息、营销活动
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 6bcfbc835a61aa326d4ee548722a6ad6e2942ea2
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 18%

---

# 创建直邮消息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直邮创建"
>abstract="在计划的营销活动中创建直邮，并设计直邮提供商向您的客户发送邮件所需的提取文件。"

要创建直邮消息，请创建计划的营销活动，并配置提取文件。 直邮提供商需要此文件向客户发送邮件。

>[!IMPORTANT]
>
>在创建直邮消息之前，请确保已配置：
>
>1. [文件路由配置](../direct-mail/direct-mail-configuration.md#file-routing-configuration)，它指定提取文件应上载和存储的服务器，
>1. 将引用文件路由配置的[直邮邮件配置](../direct-mail/direct-mail-configuration.md#direct-mail-surface)。


## 创建直邮营销活动{#create-dm-campaign}

要创建直邮营销活动，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择要执行的营销活动类型

   * **已计划 — 营销**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送营销消息。 它们从用户界面配置和执行。

   * **API触发 — 营销/事务性**：使用API调用执行营销活动。 API触发的营销活动旨在发送营销或事务型消息，即，在个人执行操作（密码重置、购物车购买等）之后发送的消息。

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;部分中，编辑营销活动的&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 要定义目标受众，请单击“选择受众”**[!UICONTROL 按钮]**，然后从可用的Adobe Experience Platform受众中进行选择。 [了解详情](../audience/about-audiences.md)。

   >[!IMPORTANT]
   >
   >目前，受众选择限制为300万个配置文件。 根据向Adobe代表提出的请求，可取消此限制。

1. 在&#x200B;**[!UICONTROL 身份命名空间]**&#x200B;字段中，选择适当的命名空间以识别所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 直邮]**。

1. 选择或新建要使用的&#x200B;**[!UICONTROL 直邮配置]**&#x200B;的配置。 [了解如何创建直邮配置](direct-mail-configuration.md#direct-mail-surface)。

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. 营销活动可以计划为特定日期，也可以设置为定期重复。 在[本节](../campaigns/create-campaign.md#schedule)中了解如何配置促销活动的&#x200B;**[!UICONTROL 计划]**。

您现在可以开始配置要发送给直邮提供商的提取文件。

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

