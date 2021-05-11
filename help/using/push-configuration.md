---
title: 推送通知配置
description: 了解如何配置环境以通过Journey Optimizer发送推送通知
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# 推送通知配置{#push-notification-configuration}

![](assets/do-not-localize/badge.png)

## 推送配置{#gs-push}快速入门

在开始使用[!DNL Journey Optimizer]发送推送通知之前，您需要在[!DNL Adobe Experience Platform]和[!DNL Adobe Experience Platform Launch]中定义设置。

## Adobe Experience Platform设置{#platform-settings}

要在[!DNL Adobe Experience Platform Launch]中设置您的移动应用程序，请执行以下步骤：

1. [分配属性和公司权限](#push-rights)
1. [在Platform launch中添加移动应用程序的推送凭据](#push-credentials-launch)。
1. [创建Edge](#edge-configuration) 配置，以便扩展 **[!UICONTROL Edge]** 将自定义数据从移动设备发送到 [!DNL Adobe Experience Platform]。
1. [设置Platform launch属性](#launch-property)。
1. [发布属性](#publish-property)。
1. [配置ProfileDataSource](#configure-profiledatasource)。

### 第1步：分配属性和公司权限{#push-rights}

在创建移动应用程序之前，您首先需要确保您拥有或分配了正确的用户权限。

有关[!DNL Adobe Experience Platform Launch]用户管理的详细信息，请参阅[Platform launch文档](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions)。

要分配“属性”和“公司”权限，请执行以下操作：

1. 访问[!DNL Admin Console]。

1. 从&#x200B;**[!UICONTROL Products]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

   ![](assets/push_product_1.png)

1. 选择现有的&#x200B;**[!UICONTROL Product Profile]**&#x200B;或使用&#x200B;**[!UICONTROL New profile]**&#x200B;按钮新建一个。 有关如何创建新&#x200B;**[!UICONTROL New profile]**&#x200B;的详细信息，请参阅[管理控制台文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui)。

1. 从&#x200B;**[!UICONTROL Permissions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Property rights]**。

   ![](assets/push_product_2.png)

1. 单击 **[!UICONTROL Add all]**。这将为您的产品用户档案添加以下权限：
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

1. 键入用户的姓名或电子邮件地址，然后选择用户。 然后，单击&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >如果用户之前未在管理控制台中创建，请参阅[添加用户文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)。

   ![](assets/push_product_7.png)


您现在拥有在[!DNL Adobe Experience Platform Launch]中创建和配置移动应用程序的正确用户权限。

### 第2步：在Platform launch {#push-credentials-launch}中添加您的移动应用程序推送凭据

>[!NOTE]
>
> 要在[!DNL Adobe Experience Platform Launch]中添加推送凭据，移动应用程序的所有者应从APNs/FCM中获取这些凭据。

1. 从[!DNL Adobe Experience Platform Launch]中，确保在下拉菜单中选择了&#x200B;**[!UICONTROL Client Side]**。

1. 在左侧面板中选择&#x200B;**[!UICONTROL App Configurations]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL App Configuration]**&#x200B;以创建新配置。

1. 输入&#x200B;**[!UICONTROL Name]**&#x200B;作为配置。

1. 从&#x200B;**[!UICONTROL Messaging Service Type]**&#x200B;下拉菜单中，选择要用于这些凭据的&#x200B;**[!UICONTROL Messaging service type]**。 在此，我们选择了&#x200B;**[!UICONTROL Apple Push Notification Service]**，因为我们正在使用iOS。

1. 如果您使用Apple推送通知服务，请在&#x200B;**[!UICONTROL App ID (iOS Bundle ID)]**&#x200B;字段中输入移动应用程序&#x200B;**[!UICONTROL Bundle Id]**；如果您使用Firebase Cloud Messaging，则在&#x200B;**[!UICONTROL App ID (Android package name)]**&#x200B;字段中输入。

   ![](assets/push_launch_app_configuration.png)

1. 将.p8密钥文件或.json私钥文件拖放到&#x200B;**[!UICONTROL Push Credentials]**&#x200B;字段。

1. 如果您使用Apple推送通知服务，请输入&#x200B;**[!UICONTROL Key Id]**&#x200B;和&#x200B;**[!UICONTROL Team Id]**。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;以创建您的应用程序配置。

### 第3步：创建边缘配置{#edge-configuration}

**[!UICONTROL Edge configuration]** 扩展使 **[!UICONTROL Edge]** 用，将自定义数据从移动设备发送到 [!DNL Adobe Experience Platform]。要配置[!DNL Adobe Experience Platform]，必须提供&#x200B;**[!UICONTROL Sandbox]**&#x200B;名称和&#x200B;**[!UICONTROL Event Dataset]**。

1. 从[!DNL Adobe Experience Platform Launch]中，选择&#x200B;**[!UICONTROL Edge Configurations]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL Edge Configurations]**。

1. 选择&#x200B;**[!UICONTROL New Edge Configuration]**&#x200B;以添加新&#x200B;**[!UICONTROL Edge Configuration]**。
1. 输入&#x200B;**[!UICONTROL Name]**&#x200B;并单击&#x200B;**[!UICONTROL Save]**

1. 单击&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;切换键以启用它。

1. 填写&#x200B;**[!UICONTROL Sandbox]**、**[!UICONTROL Event dataset]**&#x200B;和&#x200B;**[!UICONTROL Profile Dataset]**&#x200B;字段。 然后，单击&#x200B;**[!UICONTROL Save]**。

   ![](assets/push-config-4.png)

### 第4步：设置Platform launch属性{#launch-property}

通过设置[!DNL Adobe Experience Platform Launch]属性，移动应用程序开发人员或营销人员可以配置移动SDK属性，如会话超时、要定位的[!DNL Adobe Experience Platform]沙箱以及要用于向其发送数据的&#x200B;**[!UICONTROL Adobe Experience Platform Datasets]**。

1. 从[!DNL Adobe Experience Platform Launch]中，确保在下拉菜单中选择了&#x200B;**[!UICONTROL Client Side]**。

1. 选择&#x200B;**[!UICONTROL Properties]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL New Property]**。

   ![](assets/push-config-6.png)

1. 为新属性输入&#x200B;**[!UICONTROL Name]**。

1. 选择&#x200B;**[!UICONTROL Mobile]**&#x200B;作为&#x200B;**[!UICONTROL Platform]**。

   ![](assets/push-config-7.png)

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;以创建新属性。

要获取推送通知所需的SDK，您需要以下SDK扩展（适用于Android和iOS）：

* **[!UICONTROL Mobile Core]** （自动安装）
* **[!UICONTROL Profile]** （自动安装）
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**，可选，但建议调试移动设备实施。

要了解有关[!DNL Adobe Experience Platform Launch]扩展的更多信息，请参阅[Platform launch文档](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html)。

配置&#x200B;**[!UICONTROL Adobe Experience Platform Edge Extension]**&#x200B;以将自定义数据从移动设备发送到[!DNL Adobe Experience Platform]。

1. 选择您之前创建的属性，然后选择&#x200B;**[!UICONTROL Extensions]**&#x200B;选项卡以视图此属性的扩展。

   ![](assets/push-config-8.png)

1. 单击&#x200B;**[!UICONTROL Adobe Experience Platform Edge]**&#x200B;网络扩展下的&#x200B;**[!UICONTROL Configure]**。

1. 从&#x200B;**[!UICONTROL Edge Configuration]**&#x200B;下拉列表中，选择在上一步中创建的&#x200B;**[!UICONTROL Edge Configuration]**。 有关&#x200B;**[!UICONTROL Edge Configuration]**&#x200B;的详细信息，请参阅此[部分](#edge-configuration)。

1. 单击 **[!UICONTROL Save]**。

要配置&#x200B;**[!UICONTROL Adobe Experience Platform Messaging]**&#x200B;扩展以发送推送用户档案并将交互推送到正确的数据集，请执行与上述步骤相同的步骤。 使用在[Adobe Experience Platform设置](#edge-configuration)中创建的&#x200B;**[!UICONTROL Sandbox]**、**[!UICONTROL Event dataset]**&#x200B;和&#x200B;**[!UICONTROL  Profile Dataset]**。

### 第5步：发布属性{#publish-property}

您现在需要发布属性以集成配置并在移动应用程序中使用它。
要发布您的属性，请参阅[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)中详细介绍的步骤

### 第6步：配置ProfileDataSource {#configure-profiledatasource}

要配置`ProfileDataSource`，请使用[!DNL Adobe Experience Platform]设置中的`ProfileDCInletURL`，并在移动应用程序中添加以下内容：

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
