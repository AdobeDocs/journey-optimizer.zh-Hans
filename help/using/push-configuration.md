---
title: 推送通知配置
description: 了解如何配置环境以通过Journey Optimizer发送推送通知
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: 12623f6f8a9571673b2b498a02da39608344ef1e
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 3%

---

# 配置推送通知渠道{#push-notification-configuration}

[!DNL Journey Optimizer] 允许您创建历程并向目标受众发送消息。在开始使用[!DNL Journey Optimizer]发送推送通知之前，您需要确保在移动设备应用程序上以及在[!DNL Adobe Experience Platform]和[!DNL Adobe Experience Platform Launch]中配置和集成就位。 要了解Adobe历程优化程序中的推送通知数据流，请参阅[此页面](push-gs.md)。

## 开始前

<!--
### Check provisioning

Your Adobe Experience Platform account must be provisioned to contain following schemas and datasets for push notification data flow to function correctly:

| Schema <br>Dataset                                                                       | Group of fields                                                                                                                                                                         | Operation                                                |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM Push Profile Schema <br>CJM Push Profile Dataset                                     | Push Notification Details<br>Adobe CJM ExperienceEvent - Message Profile Details<br>Adobe CJM ExperienceEvent - Message Execution Details<br>Application Details<br>Environment Details | Register Push Token                                      |
| CJM Push Tracking Experience Event Schema<br>CJM Push Tracking Experience Event Dataset | Push Notification Tracking                                                                                                                                                              | Track interactions and provide data for the reporting UI |
-->

### 设置权限

在创建移动应用程序之前，您首先需要确保在&#x200B;**Adobe Experience Platform Launch**&#x200B;中拥有或分配正确的用户权限。 请参阅[Adobe Experience Platform Launch文档](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html)，以了解更多信息。

>[!CAUTION]
>
>推送配置必须由专家用户执行。 根据您的实施模型和此实施中涉及的角色，您可能需要将整套权限分配给单个产品配置文件或在应用程序开发人员与&#x200B;**Adobe Journey Optimizer**&#x200B;管理员之间共享权限。 进一步了解[本文档](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html?lang=en#platform-launch-permissions)中的&#x200B;**Adobe Experience Platform Launch**&#x200B;权限

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

要分配&#x200B;**Property**&#x200B;和&#x200B;**Company**&#x200B;权限，请执行以下步骤：

1. 访问&#x200B;**[!DNL Admin Console]**。

1. 从&#x200B;**[!UICONTROL Products]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

   ![](assets/push_product_1.png)

1. 选择现有的&#x200B;**[!UICONTROL Product Profile]**，或使用&#x200B;**[!UICONTROL New profile]**&#x200B;按钮创建新的。 了解如何在[管理控制台文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui)中创建新的&#x200B;**[!UICONTROL New profile]**。

1. 从&#x200B;**[!UICONTROL Permissions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Property rights]**。

   ![](assets/push_product_2.png)

1. 单击 **[!UICONTROL Add all]**。这会将以下权限添加到您的产品用户档案：
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   在Adobe Experience Platform Mobile SDK中安装和发布Adobe Journey Optimizer扩展以及发布应用程序资产时，需要这些权限。

1. 然后，在左侧菜单中选择&#x200B;**[!UICONTROL Company rights]**。

   ![](assets/push_product_4.png)

1. 添加以下权限：

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   移动设备应用程序开发人员需要这些权限，才能在&#x200B;**Adobe Experience Launch**&#x200B;中设置推送凭据，并在&#x200B;**Adobe Journey Optimizer**&#x200B;中定义推送通知预设。

   ![](assets/push_product_5.png)

1. 单击 **[!UICONTROL Save]**。

要将此&#x200B;**[!UICONTROL Product profile]**&#x200B;分配给用户，请执行以下步骤：

1. 访问&#x200B;**[!DNL Admin Console]**。

1. 从&#x200B;**[!UICONTROL Products]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

1. 选择您之前配置的&#x200B;**[!UICONTROL Product profile]**。

1. 在选项卡 **[!UICONTROL Users]** 中，单击 **[!UICONTROL Add user]**。

   ![](assets/push_product_6.png)

1. 键入您的用户名或电子邮件地址，然后选择用户。 然后，单击&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >如果用户之前未在Admin Console中创建，请参阅[添加用户文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)。

   ![](assets/push_product_7.png)

### 配置您的应用程序

技术设置涉及应用程序开发人员与业务管理员之间的密切协作。 在开始使用[!DNL Journey Optimizer]发送推送通知之前，您需要在Adobe Experience Platform Launch中定义设置，并将移动应用程序与Adobe Experience Platform Mobile SDK集成。

按照以下链接中详细描述的实施步骤操作：

* 对于&#x200B;**Apple iOS**:了解如何在[Apple Documentation](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns)中向APNs注册应用程序
* 对于&#x200B;**Google Android**:了解如何在[Google Documentation](https://firebase.google.com/docs/cloud-messaging/android/client)中在Android上设置Firebase Cloud Messaging客户端应用程序

### 将您的移动设备应用程序与Adobe Experience Platform SDK集成

Adobe Experience Platform Mobile SDK通过Android和iOS兼容SDK为您的手机提供客户端集成API。 请按照[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/getting-started/overview)，在您的应用程序中使用Adobe Experience Platform Mobile SDK进行设置。

在此步骤结束时，您还应该在Adobe Experience Platform Launch中创建并配置移动资产。 通常，您会为要管理的每个移动应用程序创建一个移动资产。 了解如何在[Adobe Experience Platform Launch文档](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)中创建和配置移动资产。


## 步骤1:在Adobe Experience Platform Launch {#push-credentials-launch}中添加应用程序推送凭据

授予正确的用户权限后，您现在需要在[!DNL Adobe Experience Platform Launch]中添加移动应用程序推送凭据。

要授权Adobe代表您发送推送通知，需要注册移动设备应用程序推送凭据。 请参阅下面详述的步骤：

1. 从[!DNL Adobe Experience Platform Launch]中，确保在下拉菜单中选择&#x200B;**[!UICONTROL Client Side]**。

1. 选择左侧面板中的&#x200B;**[!UICONTROL App Configurations]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL App Configuration]**&#x200B;以创建新配置。

1. 输入&#x200B;**[!UICONTROL Name]**&#x200B;作为配置。

1. 从&#x200B;**[!UICONTROL Messaging Service Type]**&#x200B;下拉菜单中，选择要用于这些凭据的&#x200B;**[!UICONTROL Messaging service type]**。

   * **对于Android**

      ![](assets/add-app-config-android.png)

      1. 提供&#x200B;**[!UICONTROL App ID (Android package name)]**:通常，包名称是`build.gradle`文件中的应用程序id。

      1. 拖放FCM推送凭据。 有关如何获取推送凭据的更多详细信息，请参阅[Google文档](https://firebase.google.com/docs/admin/setup#initialize-sdk)。
   * **对于iOS**

      ![](assets/add-app-config-ios.png)

      1. 在&#x200B;**[!UICONTROL App ID (iOS Bundle ID)]**&#x200B;字段中输入移动设备应用程序&#x200B;**包ID**。 应用程序包ID可在&#x200B;**XCode**&#x200B;中主目标的&#x200B;**General**&#x200B;选项卡中找到。

      1. 拖放Apple开发人员帐户的&#x200B;**Apple推送通知身份验证密钥**。 此密钥可从&#x200B;**Certificates**、**Identifiers**&#x200B;和&#x200B;**Profiles**&#x200B;页中获取。

      1. 提供&#x200B;**键ID**。 这是在创建p8身份验证密钥期间分配的10个字符串。 它位于&#x200B;**Certificates**、**Identifiers**&#x200B;和&#x200B;**Profiles**&#x200B;页面的&#x200B;**Keys**&#x200B;选项卡下。

      1. 提供&#x200B;**团队ID**。 这是一个字符串值，可在成员资格选项卡下找到。


1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;以创建应用程序配置。

<!--
## Step 2: Set up a mobile property in Adobe Experience Platform Launch {#launch-property}

Setting up a mobile property allows the mobile app developer or marketer to configure the mobile SDKs attributes such as Session Timeouts, the [!DNL Adobe Experience Platform] sandbox to be targeted and the **[!UICONTROL Adobe Experience Platform Datasets]** to be used for mobile SDK to send data to.

For further details and procedures on how to set up a **[!UICONTROL Platform Launch property]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).


To get the SDKs needed for push notification to work you will need the following SDK extensions, for both Android and iOS:

* **[!UICONTROL Mobile Core]** (installed automatically)
* **[!UICONTROL Profile]** (installed automatically)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, optional but recommended to debug the mobile implementation.

Learn more about [!DNL Adobe Experience Platform Launch] extensions in [Adobe Experience Platform Launch documentation](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).
-->

## 步骤2:在移动资产中配置Adobe Journey Optimizer扩展

适用于Adobe Experience Platform Mobile SDK的&#x200B;**Adobe Journey Optimizer扩展**&#x200B;可为移动应用程序的推送通知提供支持，并帮助您收集用户推送令牌并管理与Adobe Experience Platform服务的交互测量。

了解如何在[Adobe Experience Platform Mobile SDK文档](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer)中设置Journey Optimizer扩展。


<!-- 
**[!UICONTROL Edge configuration]** is used by **[!UICONTROL Edge]** extension to send custom data from mobile device to [!DNL Adobe Experience Platform]. 
To configure [!DNL Adobe Experience Platform], you must provide the **[!UICONTROL Sandbox]** name and **[!UICONTROL Event Dataset]**.

For further details and procedures on how to create **[!UICONTROL Edge configuration]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)



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

<!--
## Step 4: Publish the Property {#publish-property}

You now need to publish the property to integrate your configuration and to use it in the mobile app. 

To publish your property, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

## Step 5: Configure the ProfileDataSource {#configure-profiledatasource}

To configure the `ProfileDataSource`, use the `ProfileDCInletURL` from [!DNL Adobe Experience Platform] setup and add the following in the mobile app:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

-->

## 步骤3:使用事件{#mobile-app-test}测试移动设备应用程序

现在，在Adobe Experience Platform和Launch中配置移动设备应用程序后，您可以在向用户档案发送推送通知之前对其进行测试。 在此用例中，我们将创建一个旅程以定位我们的移动设备应用程序，并设置一个触发推送通知的事件。

<!--
You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).
-->

要使此历程正常工作，您需要创建XDM模式。 有关更多信息，请参阅[XDM文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion)。

1. 在左侧菜单中，浏览到&#x200B;**[!UICONTROL Schemas]**。

1. 单击&#x200B;**[!UICONTROL Create schema]**，然后选择&#x200B;**[!UICONTROL XDM ExperienceEvent]**。

   ![](assets/test_push_2.png)

1. 选择 **[!UICONTROL Create a new field group]**。

1. 输入&#x200B;**[!UICONTROL Display Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**。 完成后，单击&#x200B;**[!UICONTROL Add field groups]**。 有关如何创建字段组的更多信息，请参阅[XDM系统文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hans)。


   ![](assets/test_push_4.png)

1. 在左侧，选择架构。 在右侧窗格中，输入架构的名称和说明。 为&#x200B;**[!UICONTROL Profile]**&#x200B;启用此架构。

   ![](assets/test_push_4b.png)


1. 在左侧，选择字段组，然后单击+图标以创建新字段。 在右侧的&#x200B;**[!UICONTROL Field groups properties]**&#x200B;中，键入&#x200B;**[!UICONTROL Field name]**、**[!UICONTROL Display name]**&#x200B;并选择&#x200B;**[!UICONTROL String]**&#x200B;作为&#x200B;**[!UICONTROL Type]**。

   ![](assets/test_push_5.png)

1. 选中&#x200B;**[!UICONTROL Required]**&#x200B;并单击&#x200B;**[!UICONTROL Apply]**。

1. 单击 **[!UICONTROL Save]**。您的架构现已创建完成，可在事件中使用。

然后，您需要设置事件。

1. 从主页的左侧菜单的“管理”下，选择&#x200B;**[!UICONTROL Configurations]**。 单击&#x200B;**[!UICONTROL Events]**&#x200B;部分中的&#x200B;**[!UICONTROL Manage]**&#x200B;以创建新事件。

1. 单击&#x200B;**[!UICONTROL Create Event]**，将在屏幕右侧打开事件配置窗格。

   ![](assets/test_push_6.png)

1. 输入事件的名称。 您还可以添加描述。

1. 在 **[!UICONTROL Event ID type]** 字段中，选择 **[!UICONTROL Rule Based]**。

1. 在&#x200B;**[!UICONTROL Parameters]**&#x200B;中，选择您之前创建的架构。

   ![](assets/test_push_7.png)

1. 在字段列表中，检查是否已选择在架构字段组中创建的字段。

   ![](assets/test_push_7b.png)

1. 在&#x200B;**[!UICONTROL Event ID condition]**&#x200B;字段中单击&#x200B;**[!UICONTROL Edit]**。 拖放您之前添加的字段以定义系统将用于识别将触发历程的事件的条件。

   ![](assets/test_push_8.png)

1. 在此示例中，键入在测试应用程序中触发推送通知时需要使用的语法，即&#x200B;**订单确认**。

   ![](assets/test_push_9.png)

1. 选择&#x200B;**[!UICONTROL ECID]**&#x200B;作为&#x200B;**[!UICONTROL Namespace]**。

1. 单击 **[!UICONTROL Ok]**，然后单击 **[!UICONTROL Save]**。

您的事件现已创建完成，现在可用于历程。

1. 在左侧菜单中，单击&#x200B;**[!UICONTROL Journeys]**。

1. 单击&#x200B;**[!UICONTROL Create Journey]**&#x200B;以创建新历程。

1. 编辑右侧显示的配置窗格中的历程属性。在此[部分](building-journeys/journey-gs.md#change-properties)中了解详情。

1. 首先，从&#x200B;**[!UICONTROL Events]**&#x200B;下拉菜单中拖放在上一步中创建的事件。

   ![](assets/test_push_11.png)

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;下拉列表中，将&#x200B;**[!UICONTROL Message]**&#x200B;活动拖放到您的历程中。

1. 选择之前创建的消息。 有关如何创建推送通知的更多信息，请参阅此[页面](create-message.md)。

1. 将&#x200B;**[!UICONTROL End]**&#x200B;活动拖放到历程中。

1. 单击&#x200B;**[!UICONTROL Test]**&#x200B;切换开关以开始测试推送通知，然后单击&#x200B;**[!UICONTROL Trigger an event]**。

   ![](assets/test_push_12.png)

1. 在&#x200B;**[!UICONTROL Key]**&#x200B;字段中输入ECID，然后在第二个字段中键入&#x200B;**订单确认**。

   ![](assets/test_push_13.png)

1. 单击 **[!UICONTROL Send]**。

您的事件将被触发，并且您将收到到移动设备应用程序的推送通知。

## 步骤4:为推送创建消息预设{#message-preset}

在[!DNL Adobe Experience Platform Launch]中设置移动应用程序后，您需要创建消息预设，才能从&#x200B;**[!DNL Journey Optimizer]**&#x200B;发送推送通知。

了解如何在[此部分](configuration/message-presets.md)中创建和配置消息预设。

现在，您可以随时随地使用Journey Optimizer发送推送通知。

* 了解如何在[此页面](create-push.md)中创建推送消息。
* 了解如何在[此部分](building-journeys/journeys-message.md)的历程中发送添加消息。
