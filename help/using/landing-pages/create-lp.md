---
title: 创建登陆页面
description: 了解如何在Journey Optimizer中配置和发布登陆页面
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 2%

---

# 创建和发布登陆页面 {#create-lp}

## 访问登陆页面 {#access-landing-pages}

要访问登陆页面列表，请选择 **[!UICONTROL 历程管理]** > **[!UICONTROL 登陆页面]** 菜单中。

![](assets/lp_access-list.png)

的 **[!UICONTROL 登陆页面]** 列表会显示所有已创建的项目。 您可以根据用户的状态或修改日期进行筛选。

![](assets/lp_access-list-filter.png)

在此列表中，您可以访问 [登陆页面实时报表](../reports/lp-report-live.md) 或 [登陆页面全局报表](../reports/lp-report-global.md) ，以查看已发布的项目。

您还可以删除、复制和取消发布登陆页面。

>[!CAUTION]
>
>如果取消发布消息中引用的登陆页面，则指向登陆页面的链接将断开，并显示错误页面。

单击登陆页面旁边的三个圆点，以选择所需的操作。

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>您无法删除 [发布](#publish-landing-page) 登陆页面。 要删除它，必须先取消发布它。

## 创建登陆页面 {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="定义和配置登陆页面"
>abstract="要创建登陆页面，您需要选择一个预设，然后配置主页面和子页面，最后在发布之前对您的页面进行测试。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/create-lp.html#publish-landing-page" text="发布登陆页面"

创建登陆页面的步骤如下所示。

1. 在登陆页面列表中，单击 **[!UICONTROL 创建登陆页面]**.

   ![](assets/lp_create-lp.png)

1. 添加标题。 您可以根据需要添加描述。

   ![](assets/lp_create-lp-details.png)

1. 要为登陆页面分配自定义或核心数据使用标签，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级别访问控制(OLAC)的更多信息](../administration/object-based-access.md)

   <!--You can add a tag. See AEP documentation?-->

1. 选择预设。 了解如何在 [此部分](../configuration/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 将显示主页面及其属性。 了解如何配置主页面设置 [此处](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. 单击+图标以添加子页面。 了解如何配置子页面设置 [此处](#configure-subpages).

   ![](assets/lp_add-subpage.png)

配置和设计 [主页](#configure-primary-page)和 [子页面](#configure-subpages) 如果有，您可以 [测试](#test-landing-page) 和 [发布](#publish-landing-page) 登陆页面。

## 配置主页面 {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="定义主页面设置"
>abstract="用户在单击指向登陆页面的链接后（例如从电子邮件或网站），会立即向用户显示主页面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="设计登陆页面内容"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="定义登陆页面URL"
>abstract="在此部分中，定义一个唯一的登陆页面URL。 URL的第一部分要求您之前在所选预设中设置登陆页面子域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-subdomains.html" text="配置登陆页面子域"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"

主页面是用户在单击登陆页面的链接后立即向其显示的页面，例如来自电子邮件或网站的页面。

要定义主页面设置，请执行以下步骤。

1. 您可以更改页面名称，即 **[!UICONTROL 主页面]** 默认情况下。

1. 使用内容设计器编辑页面内容。 了解如何定义登陆页面内容 [此处](design-lp.md).

   ![](assets/lp_open-designer.png)

1. 定义登陆页面URL。 URL的第一部分要求您之前在 [预设](../configuration/lp-presets.md#lp-create-preset) 已选择。 [了解详情](../configuration/lp-subdomains.md)

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。

   ![](assets/lp_access-url.png)

   >[!NOTE]
   >
   >即使发布了URL，您也无法通过将此URL复制粘贴到Web浏览器来访问登陆页面。 您而是可以使用预览函数(如 [此部分](#test-landing-page).

1. 如果希望登陆页面预载已可用的表单数据，请选择 **[!UICONTROL 使用用户档案信息预填表单字段]**.

   ![](assets/lp_prefill-form-fields.png)

   启用此选项后，如果用户档案已选择启用/禁用或已添加到订阅列表，则在显示登陆页面时，将反映其选择。

   例如，如果某个用户档案选择接收有关未来事件的通信，则在下次向该用户档案显示登陆页面时，将已选中相应的复选框。

   ![](assets/lp_prefill-form-ex.png)

1. 您可以为页面定义到期日期。 在这种情况下，您必须在页面到期时选择一项操作：

   * **[!UICONTROL 重定向URL]**:输入用户将在页面过期时被重定向到的页面的URL。
   * **[!UICONTROL 自定义页面]**: [配置子页面](#configure-subpages) ，然后从显示的下拉列表中选择它。
   * **[!UICONTROL 浏览器错误]**:键入将显示的错误文本，而不是页面。

   ![](assets/lp_expiry-date.png)

1. 在 **[!UICONTROL 其他数据]** 定义一个或多个键及其相应的参数值。 您将能够在主页面和子页面的内容中使用 [表达式编辑器](../personalization/personalization-build-expressions.md). 有关详细信息，请参阅[此部分](lp-content.md#use-form-component#use-additional-data)。

   ![](assets/lp_create-lp-additional-data.png)

1. 如果您在 [设计主页面](design-lp.md)，则它们会显示在 **[!UICONTROL 订阅列表]** 中。

   ![](assets/lp_subscription-list.png)

1. 从登陆页面，您可以直接 [创建旅程](../building-journeys/journey-gs.md#jo-build) 用户在提交表单时将向用户发送确认消息。 了解如何在此结束时构建此类历程 [用例](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   单击 **[!UICONTROL 创建历程]** 被重定向到 **[!UICONTROL 历程管理]** > **[!UICONTROL 历程]** 列表。

## 配置子页面 {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="定义子页面设置"
>abstract="最多可以添加2个子页面。 例如，您可以创建一个“感谢”页面，在用户提交表单后，该页面将显示；您可以定义一个错误页面，在登陆页面出现问题时，将调用该错误页面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="设计登陆页面内容"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="定义登陆页面URL"
>abstract="在此部分中，定义一个唯一的登陆页面URL。 URL的第一部分要求您之前在所选预设中设置登陆页面子域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-subdomains.html" text="配置登陆页面子域"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"

最多可以添加2个子页面。 例如，您可以创建一个“感谢”页面，在用户提交表单后，该页面将显示；您可以定义一个错误页面，在登陆页面出现问题时，将调用该错误页面。

要定义子页面设置，请执行以下步骤。

1. 您可以更改页面名称，即 **[!UICONTROL 子页面1]** 默认情况下。

1. 使用内容设计器编辑页面内容。 了解如何定义登陆页面内容 [此处](design-lp.md).

   >[!NOTE]
   >
   >您可以从同一登陆页面的任何子页面插入指向主页面的链接。 例如，要重定向出错并希望再次订阅的用户，您可以从确认子页面添加一个链接至订阅主页面。 了解如何在 [此部分](../design/message-tracking.md#insert-links).

1. 定义登陆页面URL。 URL的第一部分要求您先前设置登陆页面子域。 [了解详情](../configuration/lp-subdomains.md)

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。

![](assets/lp_subpage-settings.png)

## 测试登陆页面 {#test-landing-page}

定义登陆页面设置和内容后，即可使用测试用户档案进行预览。 如果插入 [个性化内容](../personalization/personalize.md)，您将能够利用测试用户档案数据检查此内容在登陆页面中的显示方式。

>[!CAUTION]
>
>您必须具有测试用户档案才能预览消息和发送校样。 了解如何 [创建测试用户档案](../segment/creating-test-profiles.md).

1. 在登陆页面界面中，单击 **[!UICONTROL 预览和测试]** 按钮以访问测试用户档案选择。

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL 预览]** 按钮。

1. 从 **[!UICONTROL 预览和测试]** ，选择一个或多个测试用户档案。

   ![](assets/lp_test-profiles.png)

   选择测试用户档案的步骤与测试消息时相同。 详见 [此部分](../design/preview.md#select-test-profiles).

1. 选择 **[!UICONTROL 预览]** 选项卡，单击 **[!UICONTROL 打开预览]** 来测试登陆页面。

   ![](assets/lp_open-preview.png)

1. 登陆页面的预览将在新选项卡中打开。 个性化元素会被替换为选定的测试用户档案数据。

   ![](assets/lp_preview.png)

1. 选择其他测试用户档案以预览登陆页面每个变体的呈现。

## 检查警报 {#check-alerts}

创建登陆页面时，当您在发布之前必须执行重要操作时，会发出警告。

警报显示在屏幕的右上方，如下所示：

![](assets/lp_alerts.png)

>[!NOTE]
>
>如果看不到此按钮，则未检测到任何警报。

可以发生两种类型的警报：

* **警告** 请参阅建议和最佳实践。 <!--For example, a message will display if -->

* **错误** 阻止您发布登陆页面，但前提是这些页面未得到解决。 例如，如果主页面URL缺失，您将收到一则警告。

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> 您必须解决所有 **错误** 发布前警报。

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

登陆页面准备就绪后，您可以发布该页面以将其用于消息。

![](assets/lp_publish.png)

>[!CAUTION]
>
>在发布之前，请检查并解析警报。 [了解详情](#check-alerts)

发布登陆页面后，该页面会添加到登陆页面列表，其中包含 **[!UICONTROL 已发布]** 状态。

它现已上线，可在 [!DNL Journey Optimizer] [消息](../messages/get-started-content.md) 将通过 [历程](../building-journeys/journey.md).

>[!NOTE]
>
>您可以通过特定报表监控登陆页面的影响。 [了解详情](../reports/lp-report-live.md)

