---
solution: Journey Optimizer
product: journey optimizer
title: 创建 IP 池
description: 瞭解如何管理IP集區
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP、集區、群組、子網域、傳遞能力
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 10%

---

# 创建 IP 池 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="设置 IP 池"
>abstract="IP 池收集您子域的 IP 地址以提高电子邮件的送达率。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="设置 IP 池"
>abstract="使用 Journey Optimizer，您可以创建 IP 池，将子域的 IP 地址分组在一起。这可以显著提高您的电子邮件送达率，因为这样做可以防止一个子域的声誉影响您的其他子域。"

## 關於IP集區 {#about-ip-pools}

替換為 [!DNL Journey Optimizer]，您可以建立IP集區，將子網域的IP位址群組在一起。

強烈建議建立IP集區，以傳遞電子郵件。 如此，您就可以防止子網域的信譽影響您的其他子網域。

例如，一個最佳實務是讓一個IP集區用於行銷訊息，另一個集區用於交易式訊息。 如此一來，如果您的行銷訊息之一執行不佳且被客戶宣告為垃圾訊息，則不會影響傳送給該客戶的交易式訊息，該客戶仍會收到交易式訊息（購買確認、密碼恢複訊息等）。

>[!CAUTION]
>
>IP集區設定對所有環境都是通用的。 因此，任何IP集區的建立或編輯也將影響生產沙箱。

## 建立IP集區 {#create-ip-pool}

若要建立IP集區，請遵循下列步驟：

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL ip集區]** 功能表，然後按一下 **[!UICONTROL 建立IP集區]**.

   ![](assets/ip-pool-create.png)

1. 提供IP集區的名稱和說明（選擇性）。

   >[!NOTE]
   >
   >名稱必須以字母(A-Z)開頭，且僅包含英數字元或特殊字元( _、.、-)。

1. 從下拉式清單中選取要包含在集區中的IP位址，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >清單中提供您執行個體布建的所有IP位址。

選取IP時，您可以從清單中檢視與IP相關聯的PTR記錄。 這可讓您在建立IP集區時驗證每個IP的品牌資訊，並選取具有相同品牌資訊的IP。 [深入瞭解PTR記錄](ptr-records.md)

![](assets/ip-pool-ptr-record.png)

>[!NOTE]
>
>如果未為IP設定PTR記錄，則無法選取該IP。 請聯絡您的Adobe代表以設定該IP的PTR記錄。

建立IP集區後，當游標停留在IP集區下拉式清單下方顯示的IP位址上時，會顯示PTR資訊。

![](assets/ip-pool-ptr-record-tooltip.png)

IP集區現在已建立並顯示在清單中。 您可以選取它以存取其屬性並顯示相關頻道介面（即訊息預設集）。 有關如何將通道表面與IP集區關聯的詳細資訊，請參閱 [本節](channel-surfaces.md).

![](assets/ip-pool-created.png)

## 編輯IP集區 {#edit-ip-pool}

若要編輯IP集區，請遵循下列步驟。

1. 從清單中，按一下IP集區名稱以開啟。

   ![](assets/ip-pool-list.png)

1. 視需要編輯其屬性。 您可以修改說明，以及新增或移除IP位址。

   >[!NOTE]
   >
   >IP集區名稱不可編輯。 如果您想要修改它，您需要刪除IP集區，並以您選擇的名稱建立另一個集區。

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >在考慮刪除IP時請格外小心，因為這將對其他IP造成額外負載，並可能嚴重影響您的傳遞能力。 如有疑問，請聯絡傳遞能力專家。

1. 保存更改。

根據與關聯的IP集區，更新會立即或非同步生效。 [管道表面](channel-surfaces.md) 或不能：

* 如果IP集區是 **not** 與任何管道表面相關聯，更新是即時的(**[!UICONTROL 成功]** status)。
* 如果IP集區 **是** 和管道表面相關聯，更新最多可能需要3小時(**[!UICONTROL 處理中]** status)。

>[!NOTE]
>
>時間 [建立管道表面](channel-surfaces.md#create-channel-surface)，如果您選取正在編輯的IP集區(**[!UICONTROL 處理中]** 狀態)且從未與為該曲面選取的子域相關聯，則無法繼續建立曲面。 [了解详情](channel-surfaces.md#subdomains-and-ip-pools)

若要檢查IP集區更新狀態，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 最近更新]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP集區後，您可能必須等待：
>* 幾分鐘後，單一訊息便會使用，
>* 直到IP集區的下一個批次在批次訊息中生效。


您也可以使用 **[!UICONTROL 刪除]** 按鈕以刪除IP集區。 請注意，您無法刪除已關聯至管道表面的IP集區。

