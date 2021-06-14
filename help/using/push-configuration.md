---
title: 推送通知配置
description: 了解如何配置环境以通过Journey Optimizer发送推送通知
hide: true
hidefromtoc: true
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 1%

---

# 配置推送通知渠道{#push-notification-configuration}

![](assets/do-not-localize/badge.png)

开始使用[!DNL Journey Optimizer]发送推送通知之前，您需要在[!DNL Adobe Experience Platform]和[!DNL Adobe Experience Platform Launch]中定义设置。

## Adobe Experience Platform设置{#platform-settings}

要在[!DNL Adobe Experience Platform Launch]中设置移动设备应用程序，请执行以下步骤：

1. [分配资产和公司权限](#push-rights)
1. [在Platform launch中添加移动应用程序的推送凭据](#push-credentials-launch)。
1. [创建边缘](#edge-configuration) 配置，以供扩展用 **[!UICONTROL Edge]** 于将自定义数据从移动设备发送到 [!DNL Adobe Experience Platform]。
1. [设置Platform launch属性](#launch-property)。
1. [发布资产](#publish-property)。
1. [配置ProfileDataSource](#configure-profiledatasource)。

### 步骤1:分配资产和公司权限{#push-rights}

在创建移动应用程序之前，您首先需要确保您拥有或分配了正确的用户权限。

有关[!DNL Adobe Experience Platform Launch]用户管理的更多信息，请参阅[Platform launch文档](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions)。

要分配资产和公司权限，请执行以下操作：

1. 访问[!DNL Admin Console]。

1. 从&#x200B;**[!UICONTROL Products]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

   ![](assets/push_product_1.png)

1. 选择现有的&#x200B;**[!UICONTROL Product Profile]**，或使用&#x200B;**[!UICONTROL New profile]**&#x200B;按钮创建新的。 有关如何创建新&#x200B;**[!UICONTROL New profile]**&#x200B;的更多信息，请参阅[管理控制台文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui)。

1. 从&#x200B;**[!UICONTROL Permissions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Property rights]**。

   ![](assets/push_product_2.png)

1. 单击 **[!UICONTROL Add all]**。这会将以下权限添加到您的产品用户档案：
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. 然后，在左侧菜单中选择&#x200B;**[!UICONTROL Company rights]**。

   ![](assets/push_product_4.png)

1. 添加以下权限：

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. 单击 **[!UICONTROL Save]**。

要将此&#x200B;**[!UICONTROL Product profile]**&#x200B;分配给用户，请执行以下操作：

1. 在[!DNL Admin Console]的&#x200B;**[!UICONTROL Products]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

1. 选择您之前配置的&#x200B;**[!UICONTROL Product profile]**。

1. 在选项卡 **[!UICONTROL Users]** 中，单击 **[!UICONTROL Add user]**。

   ![](assets/push_product_6.png)

1. 键入您的用户名或电子邮件地址，然后选择用户。 然后，单击&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >如果用户之前未在Admin Console中创建，请参阅[添加用户文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)。

   ![](assets/push_product_7.png)


现在，您拥有在[!DNL Adobe Experience Platform Launch]中创建和配置移动应用程序的正确用户权限。

### 步骤2:在{#push-credentials-launch}Platform launch中添加移动应用程序推送凭据

授予正确的用户权限后，您现在需要在[!DNL Adobe Experience Platform Launch]中添加移动应用程序推送凭据。

有关如何添加移动应用程序推送凭据的更多详细信息和过程，请参阅[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/beta/adobe-journey-optimizer#configure-the-journey-optimizer-extension-in-launch)中详细的步骤。

<!--
Note that to add push credentials in [!DNL Adobe Experience Platform Launch], the owner of the mobile app should fetch them from APNs/FCM.
1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. Select the **[!UICONTROL App Configurations]** tab in the left-hand panel and click **[!UICONTROL App Configuration]** to create a new configuration.

1. Enter a **[!UICONTROL Name]** for the configuration.

1. From the **[!UICONTROL Messaging Service Type]** drop-down menu, select the **[!UICONTROL Messaging service type]** to be used for these credentials. Here, we selected **[!UICONTROL Apple Push Notification Service]** since we are working with iOS.

1. Enter the mobile app **[!UICONTROL Bundle Id]** in the **[!UICONTROL App ID (iOS Bundle ID)]** field if you are using Apple push notification service or in the **[!UICONTROL App ID (Android package name)]** field if you are using Firebase Cloud Messaging.

    ![](assets/push_launch_app_configuration.png)

1. Drag and drop the .p8 key file or the .json private key file to the **[!UICONTROL Push Credentials]** field.

1. Enter the **[!UICONTROL Key Id]** and **[!UICONTROL Team Id]** if you are using Apple push notification service.

1. Click **[!UICONTROL Save]** to create your app configuration.
-->

### 步骤3:创建边缘配置{#edge-configuration}

**[!UICONTROL Edge configuration]** 扩展使用来 **[!UICONTROL Edge]** 将自定义数据从移动设备发送到 [!DNL Adobe Experience Platform]。要配置[!DNL Adobe Experience Platform]，必须提供&#x200B;**[!UICONTROL Sandbox]**&#x200B;名称和&#x200B;**[!UICONTROL Event Dataset]**。

有关如何创建&#x200B;**[!UICONTROL Edge configuration]**&#x200B;的更多详细信息和过程，请参阅[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams)中详细的步骤。


<!--
1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)
-->

### 步骤4:设置Platform launch属性{#launch-property}

通过设置[!DNL Adobe Experience Platform Launch]属性，移动设备应用程序开发人员或营销人员可以配置移动SDK属性，如会话超时、要定向的[!DNL Adobe Experience Platform]沙盒以及要用于将数据发送到的移动SDK的&#x200B;**[!UICONTROL Adobe Experience Platform Datasets]**。

有关如何设置&#x200B;**[!UICONTROL Platform Launch property]**&#x200B;的更多详细信息和步骤，请参阅[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property)中详细描述的步骤。

要获取推送通知工作所需的SDK，您需要以下SDK扩展（适用于Android和iOS）：

* **[!UICONTROL Mobile Core]** （自动安装）
* **[!UICONTROL Profile]** （自动安装）
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**，可选，但建议调试移动设备实施。

要了解有关[!DNL Adobe Experience Platform Launch]扩展的更多信息，请参阅[Platform launch文档](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html)。

<!--

1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

### 步骤5:发布属性{#publish-property}

您现在需要发布资产以集成配置并在移动设备应用程序中使用。

要发布您的资产，请参阅[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)中详细的步骤

### 步骤6:配置ProfileDataSource {#configure-profiledatasource}

要配置`ProfileDataSource`，请使用[!DNL Adobe Experience Platform]设置中的`ProfileDCInletURL`，并在移动设备应用程序中添加以下内容：

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->

### 步骤7:创建消息预设{#message-preset}

在[!DNL Adobe Experience Platform Launch]中设置移动应用程序后，您需要创建消息预设，才能从&#x200B;**[!DNL Journey Optimizer]**&#x200B;发送推送通知。

了解如何在[此部分](configuration/message-presets.md)中创建和配置消息预设。