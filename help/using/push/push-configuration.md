---
solution: Journey Optimizer
product: journey optimizer
title: 推送通知配置
description: 瞭解如何使用Journey Optimizer設定您的環境以傳送推播通知
role: Admin
level: Intermediate
exl-id: 7099d44e-5d5d-4eef-9477-f68f4eaa1983
source-git-commit: 014cc551cb125ba6dc20a4f572e6cd7024d9fab5
workflow-type: tm+mt
source-wordcount: '1587'
ht-degree: 4%

---

# 配置推送通知渠道 {#push-notification-configuration}

[!DNL Journey Optimizer] 可讓您建立歷程並傳送訊息給目標對象。 開始使用傳送推播通知之前 [!DNL Journey Optimizer]，您必須確保行動應用程式上和Adobe Experience Platform中的標籤的設定和整合已就緒。 若要瞭解中的推播通知資料流程 [!DNL Adobe Journey Optimizer] 請參閱 [此頁面](push-gs.md).

>[!AVAILABILITY]
>
>新 **行動入門快速入門工作流程** 現已推出。 使用此新產品功能快速設定Mobile SDK，以開始收集和驗證行動事件資料，並傳送行動推播通知。 作为公开测试版，此功能可通过数据收集主页访问。[了解详情](mobile-onboarding-wf.md)


## 开始前 {#before-starting}

<!--
### Check provisioning

Your Adobe Experience Platform account must be provisioned to contain following schemas and datasets for push notification data flow to function correctly:

| Schema <br>Dataset                                                                       | Group of fields                                                                                                                                                                         | Operation                                                |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM Push Profile Schema <br>CJM Push Profile Dataset                                     | Push Notification Details<br>Adobe CJM ExperienceEvent - Message Profile Details<br>Adobe CJM ExperienceEvent - Message Execution Details<br>Application Details<br>Environment Details | Register Push Token                                      |
| CJM Push Tracking Experience Event Schema<br>CJM Push Tracking Experience Event Dataset | Push Notification Tracking                                                                                                                                                              | Track interactions and provide data for the reporting UI |
-->

### 設定許可權 {#setup-permissions}

在建立行動應用程式之前，您必須先確定您擁有或指派正確的Adobe Experience Platform標籤使用者許可權。 進一步瞭解 [標籤檔案](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

>[!CAUTION]
>
>推播設定必須由專家使用者執行。 根據您的實作模型和此實作中涉及的角色，您可能需要將完整許可權集指派給單一產品設定檔，或在應用程式開發人員和 **Adobe Journey Optimizer** 管理員。 進一步瞭解 **標籤** 中的許可權 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

要指派 **屬性** 和 **公司** 許可權，請遵循下列步驟：

1. 存取 **[!DNL Admin Console]**.

1. 從 **[!UICONTROL 產品]** 索引標籤中，選取 **[!UICONTROL Adobe Experience Platform資料彙集]** 卡片。

   ![](assets/push_product_1.png)

1. 選取現有 **[!UICONTROL 產品設定檔]** 或建立新的，使用 **[!UICONTROL 新設定檔]** 按鈕。 瞭解如何建立新的 **[!UICONTROL 新設定檔]** 在 [Admin Console檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target="_blank"}.

1. 從 **[!UICONTROL 許可權]** 索引標籤，選取 **[!UICONTROL 屬性權利]**.

   ![](assets/push_product_2.png)

1. 按一下 **[!UICONTROL 全部新增]**. 這會將以下許可權新增至您的產品設定檔：
   * **[!UICONTROL 批准]**
   * **[!UICONTROL 开发]**
   * **[!UICONTROL 管理環境]**
   * **[!UICONTROL 管理擴充功能]**
   * **[!UICONTROL 发布]**

   在Adobe Experience Platform Mobile SDK中安裝和發佈Adobe Journey Optimizer擴充功能及發佈應用程式屬性時，需要這些許可權。

1. 然後，選取 **[!UICONTROL 公司權利]** 在左側功能表中。

   ![](assets/push_product_4.png)

1. 新增下列許可權：

   * **[!UICONTROL 管理應用程式設定]**
   * **[!UICONTROL 管理资产]**

   行動應用程式開發人員需要這些許可權，才能在中設定推送認證 **Adobe Experience Platform資料彙集** 並在中定義推播通知頻道介面（即訊息預設集） **Adobe Journey Optimizer**.

   ![](assets/push_product_5.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

若要指派此專案 **[!UICONTROL 產品設定檔]** 對於使用者，請遵循下列步驟：

1. 存取 **[!DNL Admin Console]**.

1. 從 **[!UICONTROL 產品]** 索引標籤中，選取 **[!UICONTROL Adobe Experience Platform資料彙集]** 卡片。

1. 選取您先前設定的 **[!UICONTROL 產品設定檔]**.

1. 從 **[!UICONTROL 使用者]** 標籤，按一下 **[!UICONTROL 新增使用者]**.

   ![](assets/push_product_6.png)

1. 輸入使用者的名稱或電子郵件地址，然後選取使用者。 然後，按一下 **[!UICONTROL 儲存]**.

   >[!NOTE]
   >
   >如果先前未在Admin Console中建立使用者，請參閱 [新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)

### 設定您的應用程式 {#configure-app}

技術設定涉及應用程式開發人員與企業管理員之間的緊密合作。 開始使用傳送推播通知之前 [!DNL Journey Optimizer]，您必須在以下位置定義設定： [!DNL Adobe Experience Platform Data Collection] 並將您的行動應用程式與Adobe Experience Platform Mobile SDK整合。

請依照以下連結中詳述的實作步驟操作：

* 對象 **Apple iOS**：瞭解如何在中使用APN註冊您的應用程式 [Apple檔案](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}
* 對象 **Google Android**：瞭解如何在中設定Firebase Cloud Messaging使用者端應用程式 [Google檔案](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}

### 將行動應用程式與Adobe Experience Platform SDK整合 {#integrate-mobile-app}

Adobe Experience Platform Mobile SDK透過與Android和iOS相容的SDK，為您的行動裝置提供使用者端整合API。 追隨 [Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/getting-started/overview){target="_blank"} 以於應用程式中設定Adobe Experience Platform Mobile SDK。

到最後，您也應該已在以下位置建立並設定行動屬性： [!DNL Adobe Experience Platform Data Collection]. 您通常會為想要管理的每個行動應用程式建立行動屬性。 瞭解如何在中建立和設定行動屬性 [Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property){target="_blank"}.


## 步驟1：在Adobe Experience Platform Data Collection中新增應用程式推送認證 {#push-credentials-launch}

在授與正確的使用者許可權後，您現在需要在中新增行動應用程式推送認證 [!DNL Adobe Experience Platform Data Collection].

行動應用程式推送認證註冊為必填，才能授權Adobe代表您傳送推送通知。 請參閱以下詳細步驟：

1. 從 [!DNL Adobe Experience Platform Data Collection]，選取 **[!UICONTROL 應用程式表面]** 標籤。

1. 按一下 **[!UICONTROL 建立應用程式表面]** 以建立新組態。

   ![](assets/add-app-config.png)

1. 輸入 **[!UICONTROL 名稱]** 用於設定。

1. 從 **[!UICONTROL 行動應用程式設定]**，選取作業系統：

   * **適用於iOS**

      ![](assets/add-app-config-ios.png)

      1. 輸入行動應用程式 **套件組合ID** 在 **[!UICONTROL 應用程式ID (iOS套件組合ID)]** 欄位。 應用程式套件組合ID可在以下網址找到： **一般** 中主要目標的索引標籤 **XCode**.

      1. 已開啟 **[!UICONTROL 推送認證]** 按鈕以新增您的認證。

      1. 拖放您的.p8 Apple推播通知驗證金鑰檔案。 此金鑰可以從 **憑證**， **識別碼** 和 **設定檔** 頁面。

      1. 提供 **金鑰ID**. 這是在建立p8驗證金鑰期間指派的10字元字串。 此路徑位於 **金鑰** 定位於 **憑證**， **識別碼** 和 **設定檔** 頁面。

      1. 提供 **團隊ID**. 此字串值可在「成員資格」標籤下找到。
   * **適用於Android**

      ![](assets/add-app-config-android.png)

      1. 提供 **[!UICONTROL 應用程式ID （Android套件名稱）]**：套件名稱通常是中的應用程式id，位於 `build.gradle` 檔案。

      1. 已開啟 **[!UICONTROL 推送認證]** 按鈕以新增您的認證。

      1. 拖放FCM推送認證。 如需有關如何取得推送認證的詳細資訊，請參閱 [Google檔案](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"}.



1. 按一下 **[!UICONTROL 儲存]** 以建立您的應用程式設定。

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

## 步驟2：在行動屬性中設定Adobe Journey Optimizer擴充功能 {#configure-journey-optimizer-extension}

此 **Adobe Journey Optimizer擴充功能** 適用於Adobe Experience Platform的Mobile SDK可支援行動應用程式的推播通知，並協助您收集使用者推播權杖，並管理與Adobe Experience Platform服務的互動測量。

瞭解如何在中設定Journey Optimizer擴充功能 [Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer){target="_blank"}.


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

## 步驟3：使用事件測試您的行動應用程式 {#mobile-app-test}

在Adobe Experience Platform和中設定您的行動應用程式後 [!DNL Adobe Experience Platform Data Collection]，您現在可以在將推播通知傳送至設定檔之前先測試它。 在此使用案例中，我們會建立歷程來鎖定行動應用程式，並設定觸發推播通知的事件。

<!--
You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).
-->

為了讓此歷程正常運作，您需要建立XDM結構描述。 如需詳細資訊，請參閱 [XDM檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schemas-and-data-ingestion){target="_blank"}.

1. 在左側功能表中，瀏覽至 **[!UICONTROL 結構描述]**.

1. 按一下 **[!UICONTROL 建立結構描述]** 然後選取 **[!UICONTROL XDM ExperienceEvent]**.

   ![](assets/test_push_2.png)

1. 選取 **[!UICONTROL 建立新的欄位群組]**.

1. 輸入 **[!UICONTROL 顯示名稱]** 和 **[!UICONTROL 說明]**. 按一下 **[!UICONTROL 新增欄位群組]** 完成時。 有關如何建立欄位群組的詳細資訊，請參閱 [XDM系統檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hans){target="_blank"}.


   ![](assets/test_push_4.png)

1. 在左側，選取結構描述。 在右窗格中，輸入結構描述的名稱和說明。 為以下專案啟用此結構描述 **[!UICONTROL 設定檔]**.

   ![](assets/test_push_4b.png)


1. 在左側，選取欄位群組，然後按一下+圖示以建立新欄位。 在 **[!UICONTROL 欄位群組屬性]**，在右側輸入 **[!UICONTROL 欄位名稱]**， **[!UICONTROL 顯示名稱]** 並選取 **[!UICONTROL 字串]** 作為 **[!UICONTROL 型別]**.

   ![](assets/test_push_5.png)

1. Check **[!UICONTROL 必填]** 並按一下 **[!UICONTROL 套用]**.

1. 单击 **[!UICONTROL Save]**。您的結構描述現在已建立，並可用於事件中。

然後，您需要設定事件。

1. 從首頁的左側功能表的「管理」下方，選取 **[!UICONTROL 設定]**. 按一下 **[!UICONTROL 管理]** 在 **[!UICONTROL 事件]** 區段來建立您的新事件。

1. 按一下 **[!UICONTROL 建立事件]**，事件設定窗格就會在畫面右側開啟。

   ![](assets/test_push_6.png)

1. 輸入事件的名稱。 您也可以新增說明。

1. 在 **[!UICONTROL 事件ID型別]** 欄位，選取 **[!UICONTROL 基於規則]**.

1. 在 **[!UICONTROL 引數]**，選取您先前建立的結構描述。

   ![](assets/test_push_7.png)

1. 在欄位清單中，檢查是否選取了在結構描述欄位群組中建立的欄位。

   ![](assets/test_push_7b.png)

1. 按一下 **[!UICONTROL 編輯]** 在 **[!UICONTROL 事件ID條件]** 欄位。 拖放您先前新增的欄位，以定義系統用來識別觸發歷程之事件的條件。

   ![](assets/test_push_8.png)

1. 在此範例中，輸入您在測試應用程式中觸發推播通知所需使用的語法 **訂單確認**.

   ![](assets/test_push_9.png)

1. 選取 **[!UICONTROL ECID]** 作為您的 **[!UICONTROL 名稱空間]**.

1. 按一下 **[!UICONTROL 確定]** 則 **[!UICONTROL 儲存]**.

您的事件現在已建立，並可用於歷程中。

1. 在左側功能表中，按一下 **[!UICONTROL 歷程]**.

1. 按一下 **[!UICONTROL 建立歷程]** 以建立新歷程。

1. 编辑右侧显示的配置窗格中的历程属性。在本節瞭解更多 [區段](../building-journeys/journey-gs.md#change-properties).

1. 首先，從以下位置拖放上一個步驟中建立的事件： **[!UICONTROL 事件]** 下拉式清單。

   ![](assets/test_push_11.png)

1. 從 **[!UICONTROL 動作]** 下拉式清單，拖放 **[!UICONTROL 推播]** 活動至您的歷程。

1. 設定推播通知。 有關如何建立推播通知的詳細資訊，請參閱此 [頁面](create-push.md).

1. 按一下 **[!UICONTROL 測試]** 切換以開始測試推播通知，然後按一下 **[!UICONTROL 觸發事件]**.

   ![](assets/test_push_12.png)

1. 在中輸入您的ECID **[!UICONTROL 金鑰]** 欄位然後輸入 **訂單確認** 在第二個欄位中。

   ![](assets/test_push_13.png)

1. 按一下 **[!UICONTROL 傳送]**.

系統會觸發您的事件，而且您會收到傳送至行動應用程式的推播通知。

## 步驟4：建立推送的管道表面{#message-preset}

一旦您的行動應用程式在中設定完成 [!DNL Adobe Experience Platform Data Collection]，您需要建立介面才能從傳送推播通知 **[!DNL Journey Optimizer]**.

瞭解如何在中建立和設定管道表面 [本節](../configuration/channel-surfaces.md).

您現在可以使用Journey Optimizer傳送推播通知了。

* 瞭解如何在中建立推送訊息 [此頁面](create-push.md).
* 瞭解如何在中新增訊息至歷程 [本節](../building-journeys/journeys-message.md).
