---
solution: Journey Optimizer
product: journey optimizer
title: 创建登陆页面
description: 了解如何在Journey Optimizer中配置和发布登陆页面
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登录，登陆页面，创建，发布
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 53d2d09342979d8f277d1be9f2f72da067dc1763
workflow-type: tm+mt
source-wordcount: '1783'
ht-degree: 24%

---

# 创建和发布登陆页面 {#create-lp}

>[!CAUTION]
>
>要测试和发布登陆页面，您必须拥有 **[!UICONTROL 发布消息]** 许可。

要将您的客户引导至要在他们单击特定链接时显示的已定义网页，请在中创建登陆页面 [!DNL Journey Optimizer]，配置主页面和任何子页面，测试并发布它。

>[!CAUTION]
>
>您无法将以下情况下定义的URL复制粘贴到Web浏览器中，从而无法访问登陆页面： [创建页面](#create-landing-page)，即使已发布。 相反，您可以使用预览功能对其进行测试，如中所述 [本节](#test-landing-page).

## 访问登陆页面 {#access-landing-pages}

要访问登陆页面列表，请选择 **[!UICONTROL 历程管理]** > **[!UICONTROL 登陆页面]** 从左侧菜单。

![](assets/lp_access-list.png)

此 **[!UICONTROL 登陆页面]** 列表会显示所有已创建的项目。 您可以根据它们的状态或修改日期筛选它们。

![](assets/lp_access-list-filter.png)

从该列表中，您可以访问 [登陆页面实时报告](../reports/lp-report-live.md) 或 [登陆页面全局报告](../reports/lp-report-global.md) （已发布项目）。

您还可以删除、复制和取消发布登陆页面。

>[!CAUTION]
>
>如果取消发布消息中引用的登陆页面，则将断开指向登陆页面的链接，并显示错误页面。

单击登陆页面旁边的三个圆点，以选择所需的操作。

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>您无法删除 [已发布](#publish-landing-page) 登陆页面。 要删除它，必须先取消发布它。

## 创建登陆页面 {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="定义和配置您的登陆页面"
>abstract="要创建登陆页面，您需要选择一个预设，然后配置主页面和子页面，最后在发布之前测试您的页面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=zh-Hans#lp-create-preset" text="创建登陆页面预设"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/create-lp.html?lang=zh-Hans#publish-landing-page" text="发布登陆页面"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="向您的登陆页面分配标签"
>abstract="为了保护敏感的数字资产，您可以使用标签来定义授权，用于管理对登陆页面的数据访问。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html?lang=zh-Hans" text="对象级访问控制"

创建登陆页面的主要步骤如下：

![](assets/lp-creation-process.png)

1. 从登陆页面列表中，单击 **[!UICONTROL 创建登陆页面]**.

   ![](assets/lp_create-lp.png)

1. 添加标题。 您可以根据需要添加描述。

   ![](assets/lp_create-lp-details.png)

1. 要将自定义或核心数据使用标签分配给登陆页面，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

1. 从中选择或创建Adobe Experience Platform标记 **[!UICONTROL 标记]** 用于对登陆页面进行分类以改进搜索的字段。 [了解详情](../start/search-filter-categorize.md#tags)

1. 选择预设。 了解如何在中创建登陆页面预设 [本节](../landing-pages/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 此时将显示主页面及其属性。 了解如何配置主页面设置 [此处](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. 单击+图标可添加子页面。 了解如何配置子页面设置 [此处](#configure-subpages).

   ![](assets/lp_add-subpage.png)

配置和设计 [主页面](#configure-primary-page)，和 [子页面](#configure-subpages) 如果有，您可以 [测试](#test-landing-page) 和 [发布](#publish-landing-page) 您的登陆页面。

>[!CAUTION]
>
>即使已发布，您也无法仅通过复制粘贴已定义的URL到Web浏览器中来访问登陆页面。 相反，您可以使用预览功能对其进行测试，如中所述 [本节](#test-landing-page).

## 配置主页面 {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="定义主页面设置"
>abstract="用户单击您的登陆页面链接（例如在电子邮件或网站中）时，主页面会立即显示给用户。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=zh-Hans" text="设计登陆页面内容"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="定义登陆页面 URL"
>abstract="在此部分中，定义一个唯一的登陆页面 URL。URL 的第一部分需要您以前设置的登陆页面子域，这应该包括在您选择的预设中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html?lang=zh-Hans" text="配置登陆页面子域"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=zh-Hans#lp-create-preset" text="创建登陆页面预设"

主页面是在用户单击指向登陆页面的链接后立即向用户显示的页面，例如通过电子邮件或网站。

要定义主页面设置，请执行以下步骤。

1. 您可以更改页面名称，它是 **[!UICONTROL 主页面]** 默认情况下。

1. 使用内容设计器编辑页面的内容。 了解如何定义登陆页面内容 [此处](design-lp.md).

   ![](assets/lp_open-designer.png)

1. 定义登陆页面 URL. URL的第一部分要求您之前将登陆页面子域设置为 [预设](../landing-pages/lp-presets.md#lp-create-preset) 您已选择。 [了解详情](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。
   >
   >您仅需将此URL复制粘贴到Web浏览器中（即使已发布），就无法访问登陆页面。 相反，您可以使用预览功能对其进行测试，如中所述 [本节](#test-landing-page).

   ![](assets/lp_access-url.png)

1. 如果您希望登陆页面预载已可用的表单数据，请选择 **[!UICONTROL 使用用户档案信息预填表单字段]**.

   ![](assets/lp_prefill-form-fields.png)

   启用此选项后，如果配置文件已选择加入/退出或已经添加到订阅列表，则显示登陆页面时会反映配置文件的选择。

   例如，如果某个用户档案已选择接收有关未来事件的通信，则下次向该用户档案显示登陆页面时，将会选中相应的复选框。

   ![](assets/lp_prefill-form-ex.png)

1. 您可以为页面定义到期日期。 在这种情况下，您必须在页面到期时选择操作：

   * **[!UICONTROL 重定向URL]**：输入页面过期时用户将被重定向到的页面的URL。
   * **[!UICONTROL 自定义页面]**： [配置子页面](#configure-subpages) 并从显示的下拉列表中选择它。
   * **[!UICONTROL 浏览器错误]**：键入将显示的错误文本而不是页面。

   ![](assets/lp_expiry-date.png)

1. 在 **[!UICONTROL 其他数据]** 部分，定义一个或多个键及其相应的参数值。 您将能够使用以下工具在主页面和子页面的内容中利用这些键 [表达式编辑器](../personalization/personalization-build-expressions.md). 有关详细信息，请参阅[此部分](lp-content.md#use-form-component#use-additional-data)。

   ![](assets/lp_create-lp-additional-data.png)

1. 如果您在以下情况下选择了一个或多个订阅列表： [设计主页面](design-lp.md)，它们显示在中 **[!UICONTROL 订阅列表]** 部分。

   ![](assets/lp_subscription-list.png)

1. 从登陆页面，您可以直接 [创建旅程](../building-journeys/journey-gs.md#jo-build) 会在用户提交表单时向其发送确认消息。 在本课程结束时了解如何构建此类历程 [用例](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   单击 **[!UICONTROL 创建历程]** 将被重定向到 **[!UICONTROL 历程管理]** > **[!UICONTROL 历程]** 列表。

## 配置子页面 {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="定义子页面设置"
>abstract="您最多可以添加 2 个子页。例如，您可以创建一个“谢谢”页面，该页面在用户提交表单后显示，您还可以定义一个错误页面，在登陆页面出现问题时调用该页面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=zh-Hans" text="设计登陆页面内容"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="定义登陆页面 URL"
>abstract="在此部分中，定义一个唯一的登陆页面 URL。URL 的第一部分需要您以前设置的登陆页面子域，这应该包括在您选择的预设中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html?lang=zh-Hans" text="配置登陆页面子域"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=zh-Hans#lp-create-preset" text="创建登陆页面预设"

您最多可以添加 2 个子页。例如，您可以创建一个“谢谢”页面，该页面在用户提交表单后显示，您还可以定义一个错误页面，在登陆页面出现问题时调用该页面。

要定义子页面设置，请执行以下步骤。

1. 您可以更改页面名称，它是 **[!UICONTROL 子页面1]** 默认情况下。

1. 使用内容设计器编辑页面的内容。 了解如何定义登陆页面内容 [此处](design-lp.md).

   >[!NOTE]
   >
   >您可以从同一登陆页面的任何子页面插入指向主页面的链接。 例如，要重定向发生错误并想要再次订阅的用户，您可以从确认子页面添加一个链接至订阅主页面。 了解如何在中插入链接 [本节](../email/message-tracking.md#insert-links).

1. 定义登陆页面 URL. URL的第一部分要求您之前设置登陆页面子域。 [了解详情](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。
   >
   >即使已发布，您也无法仅通过复制此URL并将其粘贴到Web浏览器中来访问子页面。 相反，您可以使用预览功能对其进行测试，如中所述 [本节](#test-landing-page).

![](assets/lp_subpage-settings.png)

## 测试登陆页面 {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ac_preview_lp_profiles"
>title="预览和测试登陆页面"
>abstract="定义了登陆页面设置和内容之后，您可使用测试配置文件对其进行预览。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles.html" text="选择测试配置文件"

定义登陆页面设置和内容后，您可以使用测试配置文件进行预览。 如果您已插入 [个性化内容](../personalization/personalize.md)，您将能够使用测试用户档案数据检查此内容在登陆页面中的显示方式。

>[!CAUTION]
>
>要能够测试登陆页面，您必须拥有 **[!UICONTROL 发布消息]** 许可。
>
>您必须具有可用的测试用户档案，才能预览消息并发送校样。 了解如何 [创建测试用户档案](../audience/creating-test-profiles.md).

1. 在登陆页面界面中，单击 **[!UICONTROL 模拟内容]** 按钮以访问选择的测试用户档案。

   ![](assets/lp_simulate-button.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 模拟内容]** 按钮也可以从内容设计器访问。

1. 从 **[!UICONTROL 模拟]** 屏幕中，选择一个或多个测试用户档案。

   ![](assets/lp_test-profiles.png)

   选择测试用户档案的步骤与测试消息时的步骤相同。 有关详情，请参阅 [本节](../email/preview.md#select-test-profiles).

1. 选择 **[!UICONTROL 打开预览]** 以测试您的登陆页面。

   ![](assets/lp_open-preview.png)

1. 登陆页面的预览将在新选项卡中打开。 个性化的元素将由选定的测试配置文件数据替换。

   <!--![](assets/lp_preview.png)-->

1. 选择其他测试用户档案以预览登陆页面每个变体的渲染。

## 检查警报 {#check-alerts}

在创建登陆页面时，如果必须在发布之前执行重要操作，则会收到警报。

警报显示在屏幕的右上方，如下所示：

![](assets/lp_alerts.png)

>[!NOTE]
>
>如果未看到此按钮，则表示未检测到警报。

可能会发生两种类型的警报：

* **警告** 请参阅建议和最佳实践。 <!--For example, a message will display if -->

* **错误** 阻止发布登陆页面，前提是这些页面未解析。 例如，如果缺少主页面URL，您将收到警告。

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> 您必须解决所有 **错误** 发布前的警报。

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you must resolve all **error** alerts.
-->

## 发布登陆页面 {#publish-landing-page}

>[!CAUTION]
>
>要发布登陆页面，您必须拥有 **[!UICONTROL 发布消息]** 许可。

准备登陆页面后，即可发布该页面，以供在消息中使用。

![](assets/lp_publish.png)

>[!CAUTION]
>
>发布之前，请检查并解决警报。 [了解详情](#check-alerts)

发布登陆页面后，该页面将添加到登陆页面列表，其中包含 **[!UICONTROL 已发布]** 状态。

它现在已上线并准备好用于 [!DNL Journey Optimizer] 将通过 [历程](../building-journeys/journey.md).

>[!NOTE]
>
>您无法将以下情况下定义的URL复制粘贴到Web浏览器中，从而无法访问登陆页面： [创建页面](#create-landing-page)，即使已发布。 相反，您可以使用预览功能对其进行测试，如中所述 [本节](#test-landing-page).

您可以通过特定报告监控登陆页面影响。 [了解详情](../reports/lp-report-live.md)
