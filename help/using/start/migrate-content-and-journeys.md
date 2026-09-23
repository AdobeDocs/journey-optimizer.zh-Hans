---
solution: Journey Optimizer
product: journey optimizer
title: 迁移内容和历程
description: 了解如何迁移电子邮件内容模板以及从外部平台导入历程。
feature: Get Started
topic: Content Management
role: User
level: Intermediate
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
    internal-label: Journeys
subfeature_v2: []
source-git-commit: 57b04ad2f74c5a0a1d836bac9a45c9efd84ceb96
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 8%
---
# 迁移内容和历程 {#migrate-content-and-journeys}

>[!AVAILABILITY]
>
>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

如果您从另一个营销平台移动到[!DNL Journey Optimizer]，则不必从空白板开始。 Journey Optimizer包括一个专用工作区，用于导入您的现有电子邮件内容和历程。 它会将它们转换为[!DNL Journey Optimizer]内容模板和历程，因此您可以从停止的位置选择重建内容，而不是从头开始重建所有内容。

要将您的内容和历程迁移到Journey Optimizer，您需要以下权限：管理营销活动、管理历程、管理消息、管理区段、管理库项目、查看和管理沙盒以及管理AJO集成配置。 [了解有关角色和权限的更多信息](../administration/permissions.md)

您可以直接从[!DNL Journey Optimizer]主页访问此工作区。

![访问迁移工作区](assets/onboarding-hub-15.png)

## 设置连接 {#set-up-a-connection}

>[!CONTEXTUALHELP]
>id="ajo_migration_connection_name"
>title="连接名称"
>abstract="标识源系统的描述性名称（例如“Marketing-Automation-Prod”）。 必须以字母开头，并且只包含字母数字、下划线或连字符（4-50 个字符）。"


>[!CONTEXTUALHELP]
>id="ajo_migration_base_api_url"
>title="基本API URL"
>abstract="API 的根 URL，不含资源路径或查询字符串，例如 https://api.example.com。"

>[!CONTEXTUALHELP]
>id="ajo_migration_authentication_method"
>title="选择一个身份验证方式"
>abstract="API 密钥会随每个请求发送一个凭据，而 OAuth 2.0 则使用基于令牌的协议，这更适合企业和第三方 API。"

>[!CONTEXTUALHELP]
>id="ajo_migration_client_id"
>title="客户端 ID"
>abstract="您的应用程序的公共标识符，在您通过授权服务器注册时发布。"

>[!CONTEXTUALHELP]
>id="ajo_migration_client_secret"
>title="客户端密码"
>abstract="只有您的应用程序和授权服务器才知道的机密凭据。 切勿在客户端代码中将其公开。"


>[!CONTEXTUALHELP]
>id="ajo_migration_token_url"
>title="令牌 URL"
>abstract="发布客户端凭据流的访问令牌的授权服务器端点，通常以 /oauth/token 或 /token 结尾。"


>[!NOTE]
>
>如果您上传HTML文件或屏幕截图而不是通过API导入，则不需要连接。

要通过API导入内容或历程，请首先将[!DNL Journey Optimizer]连接到您的源平台：

1. 在工作区中选择&#x200B;**[!UICONTROL 管理连接]**。

   ![管理连接按钮](assets/onboarding-hub-14.png)

1. 单击&#x200B;**[!UICONTROL 新建连接]**。

   ![突出显示了“管理连接”按钮的连接窗口](assets/onboarding-hub-1.png)

1. 请填写以下详细信息：

   * **[!UICONTROL 连接名称]**：标识源系统的名称，如`Marketing-Automation-Prod`。 名称必须以字母开头，并且只能包含字母、数字、下划线或连字符，长度介于4到50个字符之间。
   * **[!UICONTROL 基本API URL]**：源系统API的根URL，不含任何资源路径或查询字符串，如`https://api.example.com`。
   * **[!UICONTROL 描述]**：可帮助您和其他用户识别此连接目的的可选上下文。
   * **[!UICONTROL 身份验证方法]**： [!DNL Journey Optimizer]如何对源系统进行身份验证。 选择&#x200B;**API密钥**&#x200B;以通过每个请求发送单个凭据。 选择&#x200B;**OAuth 2.0**&#x200B;以使用更适合企业和第三方API的基于令牌的协议。
   * **[!UICONTROL 客户端ID]**：向授权服务器注册应用程序时分配给该应用程序的公共标识符。 OAuth 2.0连接需要。
   * **[!UICONTROL 客户端密钥]**：与您的客户端ID关联的机密凭据。 保持私密性，因为只有您的应用程序和授权服务器才知道这一点。 OAuth 2.0连接需要。
   * **[!UICONTROL 令牌URL]**：为客户端凭据流颁发访问令牌的授权服务器终结点，通常以`/oauth/token`或`/token`结尾。 OAuth 2.0连接需要。

     ![新的连接表单，其中包含连接名称、基本API URL和身份验证详细信息的字段](assets/onboarding-hub-2.png)

1. 选择&#x200B;**[!UICONTROL 创建]**。

1. 设置连接后，使用高级菜单将其删除，或将其标记为默认值，以便在下次导入内容或历程时预先选择该连接。

   ![高级菜单，带有删除连接或将其标记为默认连接的选项](assets/onboarding-hub-3.png)

## 导入电子邮件内容 {#import-email-content}

当您拥有内容的源（HTML文件或与源平台的连接）后，请将其导入工作区以将其转换为[!DNL Journey Optimizer]内容模板。

1. 从&#x200B;**[!UICONTROL 电子邮件内容]**&#x200B;选项卡，选择导入电子邮件内容的方式：

   * **[!UICONTROL 上传HTML]**：从您的计算机中选择一个或多个HTML电子邮件文件。

   * **[!UICONTROL 从连接浏览]**：直接从连接的营销平台浏览和选择电子邮件，而无需手动导出和上传文件。

   ![包含上传HTML或从连接浏览选项的电子邮件内容选项卡](assets/onboarding-hub-6.png)

1. 要上传HTML，请浏览您的文件或将其拖放到上传区域。 完成后单击&#x200B;**[!UICONTROL 上传]**。

   文件必须采用`.html`或`.htm`格式，并且不能大于10 MB。

   电子邮件内容的![HTML文件上传区域](assets/onboarding-hub-7.png)

1. 对于从连接导入，请从“电子邮件”列表中选择，然后单击&#x200B;**[!UICONTROL 导入]**。

1. 访问导入的电子邮件并查看导入的HTML。

1. 添加您的&#x200B;**[!UICONTROL 主题行]**，并将每个个性化占位符映射到相应的配置文件属性。

   工作区会自动将源脚本语法转换为Handlebars语法。 有关支持的运算符列表，请参阅[运算符](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/personalization/functions/operators)。

   ![导入了主题行字段和个性化占位符映射的电子邮件编辑器](assets/onboarding-hub-8.png)

   >[!NOTE]
   >
   >某些源日期令牌会自动映射，不会显示为要映射的个性化占位符。 令牌发现和映射也已得到改进，以提高准确性。

1. 如果电子邮件引用任何内容块，请将其解析为片段。 请参阅[导入片段](#import-fragments)。

1. 选择一个文件夹以将电子邮件的图像上传到[!DNL Experience Manager Assets]，然后单击&#x200B;**[!UICONTROL 上传资产]**。

   ![用于将电子邮件图像上传到Experience Manager Assets的文件夹选择窗口](assets/onboarding-hub-9.png)

1. 电子邮件准备就绪后，选择&#x200B;**[!UICONTROL 迁移]**，然后选择&#x200B;**查看电子邮件**&#x200B;以打开新的内容模板。

   已完成电子邮件的![在Journey Optimizer中迁移按钮和查看选项](assets/onboarding-hub-10.png)

您的内容模板现在可在[!DNL Journey Optimizer]中使用，并可在您的历程中使用。

➡️ [了解有关内容模板的更多信息](../content-management/use-content-templates.md)

## 导入片段 {#import-fragments}

片段是电子邮件中可重用的构建基块，例如页眉、页脚或促销基块，您可以一次性构建这些基块，并在多个电子邮件中重复使用，以实现一致性和更快的创作。 当您迁移电子邮件时，[!DNL Journey Optimizer]会标识它引用的任何内容块，并将其显示为措施项，因此您可以随电子邮件迁移这些内容块。

1. 从&#x200B;**[!UICONTROL 片段]**&#x200B;选项卡中，选择您希望导入片段的方式：

   * **[!UICONTROL 上传HTML]**：从您的计算机中选择一个或多个HTML片段文件。

   * **[!UICONTROL 从连接浏览]**：直接从连接的营销平台浏览并选择片段，而无需手动导出和上传文件。

   ![包含上传HTML或从连接浏览选项的片段选项卡](assets/onboarding-fragment-1.png)

1. 您还可以在迁移电子邮件时导入片段。 在迁移电子邮件时，[!DNL Journey Optimizer]会扫描它，识别任何引用的内容块，并将其显示为电子邮件上的片段操作项，因此您可以在不离开电子邮件迁移流程的情况下解析它们。

   ![电子邮件上的片段操作项，显示检测到的等待解析的内容块](assets/onboarding-fragment-2.png)

1. 要从连接导入，请从“片段”列表中选择，然后单击&#x200B;**[!UICONTROL 导入]**。

1. 打开导入的片段并解析其剩余的操作项，例如，资产或相应的配置文件属性。

   ![已导入片段及其要解析的剩余操作项](assets/onboarding-fragment-3.png)

1. 片段准备就绪后，选择&#x200B;**[!UICONTROL 迁移]**，然后选择&#x200B;**查看片段**&#x200B;以将其打开。


## 导入历程 {#import-journeys}

通过导入历程流的屏幕快照或连接到源平台来重新创建历程。 历程准备为可编辑的草稿，您可以在可视化画布上查看这些草稿后进行迁移，这样您就能够获得首先需要您输入的所有内容的引导式核对清单，而不是盲目迁移。

1. 从&#x200B;**[!UICONTROL 历程]**&#x200B;选项卡中，选择您希望导入旅程的方式：

   * **[!UICONTROL 上传屏幕截图]**：从您的计算机中选择一个或多个历程屏幕截图。

   * **[!UICONTROL 从连接浏览]**：直接从连接的营销平台浏览并选择历程，而无需手动导出和上传屏幕截图。

   ![历程选项卡，可选择上传屏幕截图或从连接浏览](assets/onboarding-hub-11.png)

1. 要上传屏幕快照，请浏览您的文件或将其拖放到上传区域。 完成后单击&#x200B;**[!UICONTROL 上传]**。

   文件必须采用.png、.jpg、.gif、.webp格式且不得大于5 MB。

   ![历程图像的屏幕快照上传区域](assets/onboarding-hub-13.png)

1. 对于从连接导入，请从历程列表中选择，然后单击&#x200B;**[!UICONTROL 导入]**。

1. 打开历程以在交互式画布上预览它。 整个历程呈现为节点和边缘画布，并且需要关注的节点具有内联标记。

1. 从&#x200B;**[!UICONTROL 操作项]**&#x200B;面板中，解析每个项，然后再迁移。 面板标题显示已解析项目的实时计数（总数中的），选择措施项会突出显示画布上的匹配节点。 措施项包括：

   * **[!UICONTROL 历程名称]**：在迁移前设置历程名称。
   * **[!UICONTROL 内容模板]**：为需要内容模板的历程操作选择相应的内容模板。 在选择电子邮件模板时对其进行验证，所有验证问题均直接显示在措施项中。
   * **[!UICONTROL 渠道配置]**：为渠道（如电子邮件和短信）选择所需的配置。
   * **[!UICONTROL 受众区段]**：将源受众映射到相应的[!DNL Journey Optimizer]受众。

   ![具有已解析活动的措施项窗格和“应用更改”按钮](assets/onboarding-hub-12.png)

1. 解析每个操作项后，选择&#x200B;**[!UICONTROL 迁移]**。

   [!DNL Journey Optimizer]对历程运行最终检查，重新验证电子邮件模板并确认历程名称已设置。 任何缺失或无效的信息将阻止迁移，并内联显示在相关操作项中。 检查通过后，确认步骤会防止意外迁移，然后页面会反映处理状态。

1. 如果您不再需要历程迁移，请从历程列表或打开历程内的菜单中删除它。

   ![具有已解析活动的措施项窗格和“应用更改”按钮](assets/onboarding-hub-16.png)

您的历程现在位于[!DNL Journey Optimizer]中，您可以在其中查看画布、做出任何最终调整并在准备好上线时激活它。 选择&#x200B;**[!UICONTROL 查看历程]**&#x200B;以直接在[!DNL Journey Optimizer]中打开迁移的历程。 如果迁移完成，但无法应用某些操作项，则会告知您确切的数量，并指向[!DNL Journey Optimizer]以完成这些操作。

➡️ [了解有关历程创建的更多信息](../building-journeys/journey-gs.md)

## 跟踪迁移 {#track-migration-progress}

工作区概述可帮助您跟踪已导入的每封电子邮件或历程，并快速找到仍在等待操作的电子邮件或历程。 屏幕顶部的一组KPI为您提供了每种状态的项目一目了然计数：

* **总计**：导入到工作区中的项目总数。
* **进行中**：迁移之前仍在审核或映射的项。
* **已迁移**：已成功转换并且在[!DNL Journey Optimizer]中可用的项目。
* **失败**：无法迁移需要注意的项目。

![包含KPI的Workspace概述，适用于总计、进行中、已迁移和失败的项目](assets/onboarding-hub-4.png)

通过一组过滤器，您可以缩小导入内容列表的范围，以便能够专注于特定子集，而不是滚动浏览每个项目。 组合以下一个或多个筛选器以查找您要查找的内容：

* **[!UICONTROL 需要操作]**：该项具有未解析的操作项，需要您的输入才能迁移。
* **[!UICONTROL 正在处理]**：该项目当前正在迁移。
* **[!UICONTROL 已迁移]**：该项目已成功迁移，可在[!DNL Journey Optimizer]中使用。
* **[!UICONTROL 失败]**：迁移无法完成，需要注意。

![工作区中状态、创建日期和更新日期的筛选选项](assets/onboarding-hub-5.png)

{{$include /help/_includes/do-not-localize/start/ai-augmented-migrate-content-and-journeys.md}}
