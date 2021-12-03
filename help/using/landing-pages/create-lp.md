---
title: 创建登陆页面
description: 了解如何在Journey Optimizer中配置和发布登陆页面
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 3%

---

# 创建和发布登陆页面 {#create-lp}

>[!CAUTION]
>
>登陆页面目前仅供选定用户抢先使用。 如果要利用此功能，请联系您的Adobe客户经理。

## 访问登陆页面

要访问登陆页面列表，请选择 **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** 菜单中。

![](../assets/lp_access-list.png)

的 **[!UICONTROL Landing Pages]** 列表会显示所有已创建的项目。 您可以根据用户的状态或修改日期进行筛选。

![](../assets/lp_access-list-filter.png)

## 创建登陆页面

创建登陆页面的步骤如下所示。

1. 在登陆页面列表中，单击 **[!UICONTROL Create landing page]**.

   ![](../assets/lp_create-lp.png)

1. 添加标题。 您可以根据需要添加描述。

   ![](../assets/lp_create-lp-details.png)

1. 单击 **[!UICONTROL Create]**。

1. 将显示主页面及其属性。 了解如何配置页面设置 [此处](#configure-primary-page).

   ![](../assets/lp_primary-page.png)

1. 单击+图标以添加子页面。 了解如何配置其设置 [此处](#configure-subpages).

   ![](../assets/lp_add-subpage.png)

配置和设计 [主页](#configure-primary-page) 和 [子页面](#configure-subpages) 如果有，您可以 [测试](#test) 和 [发布](#publish) 登陆页面。

## 配置主页面 {#configure-primary-page}

主页面是用户在单击登陆页面的链接时立即向其显示的页面，例如来自电子邮件或网站的页面。

要定义主页面设置，请执行以下步骤。

1. 您可以更改页面名称，即 **[!UICONTROL Primary page]** 默认情况下。

1. 使用内容设计器编辑页面内容。 了解如何设计登陆页面内容 [此处](design-lp.md).

   ![](../assets/lp_open-designer.png)

1. 定义登陆页面URL。

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。

   ![](../assets/lp_access-url.png)

   URL的第一部分已预填充，无法通过用户界面进行编辑。 要进行设置，请联系您的Adobe客户代表或 [Adobe客户关怀支持团队](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。

1. 您可以为页面定义到期日期。 在这种情况下，您必须在页面到期时选择一项操作：

   * **[!UICONTROL Redirect URL]**:输入用户将在页面过期时被重定向到的页面的URL。
   * **[!UICONTROL Custom page]**: [配置子页面](#configure-subpages) ，然后从显示的下拉列表中选择它。
   * **[!UICONTROL Browser error]**:键入将显示的错误文本，而不是页面。

   ![](../assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. 如果您为主页面选择了一个或多个订阅列表，则这些订阅列表会显示在 **[!UICONTROL Subscription list]** 中。

   ![](../assets/lp_subscription-list.png)

1. 从登陆页面，您可以直接创建一个旅程，在用户提交表单时向其发送确认消息。

   ![](../assets/lp_create-journey.png)

   单击 **[!UICONTROL Create journey]** 开始 [配置此历程](../building-journeys/journey-gs.md#jo-build). 您将被重定向到 **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** 列表。

## 配置子页面 {#configure-subpages}

您可以根据需要添加任意数量的子页面。 例如，您可以创建一个感谢页面，该页面将在用户提交表单后显示。 您还可以定义在登陆页面发生错误时将调用的错误页面。

要定义子页面设置，请执行以下步骤。

1. 您可以更改页面名称，即 **[!UICONTROL Subpage 1]** 默认情况下。

1. 使用内容设计器编辑页面内容。 了解如何设计登陆页面内容 [此处](design-lp.md).

1. 定义登陆页面URL。

   URL的第一部分已预填充，无法通过用户界面进行编辑。 要进行设置，请联系您的Adobe客户代表或 [Adobe客户关怀支持团队](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。

   >[!CAUTION]
   >
   >登陆页面URL必须是唯一的。

![](../assets/lp_subpage-settings.png)

## 测试登陆页面 {#test}

定义登陆页面设置和内容后，即可使用测试用户档案进行预览。 如果插入 [个性化内容](../personalization/personalize.md)，您将能够利用测试用户档案数据检查此内容在登陆页面中的显示方式。

>[!CAUTION]
>
>您需要提供测试用户档案才能预览消息和发送校样。 了解如何在 [本页](../building-journeys/creating-test-profiles.md).

1. 在登陆页面界面或内容设计器中，单击 **[!UICONTROL Preview & test]** 按钮以访问测试用户档案选择。

   ![](../assets/lp_preview-button.png)

1. 选择一个或多个测试用户档案。

   ![](../assets/lp_test-profiles.png)

   选择测试用户档案的步骤与测试消息时相同。 详见 [此部分](../preview.md#select-test-profiles).

1. 单击 **[!UICONTROL Preview]** 选项卡来测试登陆页面。

   <!--![](../assets/lp_preview.png)-->

1. 个性化元素会被替换为选定的测试用户档案数据。 选择其他测试用户档案以预览登陆页面每个变体的呈现。

## 检查警报 {#alerts}

创建登陆页面时，当您需要在发布之前执行重要操作时，会发出警告。

警报显示在屏幕的右上方，如下所示：

![](../assets/lp_alerts.png)

>[!NOTE]
>
>如果看不到此按钮，则未检测到任何警报。

可以发生两种类型的警报：

* **警告** 请参阅建议和最佳实践。 <!--For example, a message will display if -->

* **错误** 阻止您发布消息，但前提是这些消息未得到解析。 例如，将显示一条消息，警告您主页面URL缺失。

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

## 发布登陆页面 {#publish}

登陆页面准备就绪后，您可以发布该页面以将其用于消息或网站上。

![](../assets/lp_publish.png)

>[!CAUTION]
>
>在发布之前，请检查并解析警报。 [了解详情](#alerts)

发布登陆页面后，该页面会添加到登陆页面列表，其中包含 **[!UICONTROL Published]** 状态。

它现已上线，指向它的链接已准备就绪，可在 [消息](../create-message.md) 通过 [历程](../building-journeys/journey.md).
