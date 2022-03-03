---
title: 创建登陆页面
description: 了解如何在Journey Optimizer中配置和发布登陆页面
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: c988f0baa8b3c622dfb4f1ff060001a3462ed31e
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 3%

---

# Create and publish landing pages {#create-lp}

>[!CAUTION]
>
>登陆页面目前仅供选定用户抢先使用。 如果要利用此功能，请联系您的Adobe客户经理。

## 访问登陆页面 {#access-landing-pages}

要访问登陆页面列表，请选择 **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** 菜单中。

![](assets/lp_access-list.png)

的 **[!UICONTROL Landing Pages]** 列表会显示所有已创建的项目。 您可以根据用户的状态或修改日期进行筛选。

![](assets/lp_access-list-filter.png)

## 创建登陆页面 {#create-landing-page}

创建登陆页面的步骤如下所示。

1. 在登陆页面列表中，单击 **[!UICONTROL Create landing page]**.

   ![](assets/lp_create-lp.png)

1. Add a title. 您可以根据需要添加描述。

   ![](assets/lp_create-lp-details.png)

1. 选择预设。

   ![](assets/lp_create-lp-presets.png)

   >[!NOTE]
   >
   >To define landing page presets, contact your Adobe account representative or the [Adobe Customer Care Support Team](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

1. 单击 **[!UICONTROL Create]**。

1. 将显示主页面及其属性。 了解如何配置主页面设置 [此处](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. 单击+图标以添加子页面。 了解如何配置子页面设置 [此处](#configure-subpages).

   ![](assets/lp_add-subpage.png)

配置和设计 [主页](#configure-primary-page)和 [子页面](#configure-subpages) 如果有，您可以 [测试](#test-landing-page) 和 [发布](#publish-landing-page) 登陆页面。

## 配置主页面 {#configure-primary-page}

主页面是用户在单击登陆页面的链接后立即向其显示的页面，例如来自电子邮件或网站的页面。

要定义主页面设置，请执行以下步骤。

1. 您可以更改页面名称，即 **[!UICONTROL Primary page]** 默认情况下。

1. 使用内容设计器编辑页面内容。 了解如何定义登陆页面内容 [此处](design-lp.md).

   ![](assets/lp_open-designer.png)

1. 定义登陆页面URL。 The first part of the URL requires the domain delegation to be performed. It is pre-filled and cannot be edited through the user interface. To set it up, contact your Adobe account representative or the [Adobe Customer Care Support Team](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

   >[!CAUTION]
   >
   >The landing page URL must be unique.

   ![](assets/lp_access-url.png)

1. 您可以为页面定义到期日期。 In that case, you must select an action upon page expiry:

   * **[!UICONTROL Redirect URL]**:输入用户将在页面过期时被重定向到的页面的URL。
   * **[!UICONTROL Custom page]**: [配置子页面](#configure-subpages) ，然后从显示的下拉列表中选择它。
   * **[!UICONTROL Browser error]**: Type the error text that will be displayed instead of the page.

   ![](assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. 如果您在 [设计主页面](design-lp.md)，则它们会显示在 **[!UICONTROL Subscription list]** 中。

   ![](assets/lp_subscription-list.png)

1. 从登陆页面，您可以直接 [创建旅程](../building-journeys/journey-gs.md#jo-build) 用户在提交表单时将向用户发送确认消息。 了解如何在此结束时构建此类历程 [用例](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   单击 **[!UICONTROL Create journey]** 被重定向到 **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** 列表。

## Configure subpages {#configure-subpages}

You can add up to 2 subpages. For example, you can create a &#39;thank you&#39; page that will display once the users submit the form, and you can define an error page that will be called if a problem occurs with the landing page.

To define the subpage settings, follow the steps below.

1. You can change the page name, which is **[!UICONTROL Subpage 1]** by default.

1. 使用内容设计器编辑页面内容。 Learn how to define landing page content [here](design-lp.md).

1. 定义登陆页面URL。 URL的第一部分要求执行域委派。 已预填充，无法通过用户界面进行编辑。 To set it up, contact your Adobe account representative or the [Adobe Customer Care Support Team](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。

![](assets/lp_subpage-settings.png)

## 测试登陆页面 {#test-landing-page}

定义登陆页面设置和内容后，即可使用测试用户档案进行预览。 如果插入 [个性化内容](../personalization/personalize.md)，您将能够利用测试用户档案数据检查此内容在登陆页面中的显示方式。

>[!CAUTION]
>
>您需要提供测试用户档案才能预览消息和发送校样。 了解如何 [创建测试用户档案](../building-journeys/creating-test-profiles.md).

1. 在登陆页面界面中，单击 **[!UICONTROL Preview & test]** 按钮以访问测试用户档案选择。

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >The **[!UICONTROL Preview]** button is also accessible from the content designer.

1. 从 **[!UICONTROL Preview & test]** ，选择一个或多个测试用户档案。

   ![](assets/lp_test-profiles.png)

   选择测试用户档案的步骤与测试消息时相同。 详见 [此部分](../messages/preview.md#select-test-profiles).

1. Select the **[!UICONTROL Preview]** tab and click **[!UICONTROL Open preview]** to test your landing page.

   ![](assets/lp_open-preview.png)

1. The preview of your landing page opens in a new tab. 个性化元素会被替换为选定的测试用户档案数据。

   ![](assets/lp_preview.png)

1. Select other test profiles to preview the rendering for each variant of your landing page.

## 检查警报 {#check-alerts}

While you are creating your landing page, alerts warn you when you need to take important actions before publishing.

警报显示在屏幕的右上方，如下所示：

![](assets/lp_alerts.png)

>[!NOTE]
>
>If you do not see this button, no alert has been detected.

Two types of alerts can happen:

* **警告** 请参阅建议和最佳实践。 <!--For example, a message will display if -->

* **错误** 阻止您发布消息，但前提是这些消息未得到解析。 例如，如果主页面URL缺失，您将收到一则警告。

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> 您需要解决所有 **错误** 发布前警报。

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you need to resolve all **error** alerts.
-->

## 发布登陆页面 {#publish-landing-page}

Once your landing page is ready, you can publish it to make it available for use in a message.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Before publishing, check and resolve alerts. [了解详情](#check-alerts)

发布登陆页面后，该页面会添加到登陆页面列表，其中包含 **[!UICONTROL Published]** 状态。

它现已上线，可在 [!DNL Journey Optimizer] [消息](../messages/create-message.md) 将通过 [历程](../building-journeys/journey.md).

>[!NOTE]
>
>您可以通过特定报表监控登陆页面的影响。 [了解详情](lp-report.md)

