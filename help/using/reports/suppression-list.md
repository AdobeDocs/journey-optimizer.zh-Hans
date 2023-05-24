---
solution: Journey Optimizer
product: journey optimizer
title: 禁止列表
description: 瞭解如何使用隱藏清單
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 8%

---

# 禁止列表 {#suppression-list}

隱藏清單包含您要從傳送中排除的地址和網域，因為傳送給這些聯絡人可能會損害您的傳送信譽和傳送率。

此 [!DNL Journey Optimizer] 隱藏清單是在您自己的環境層級（即對於指定的沙箱）進行管理。

它會收集單一使用者端環境中所有郵件中隱藏的電子郵件地址和網域，這表示會特定於與沙箱ID關聯的組織ID。

>[!NOTE]
>
>Adobe會保留已知不良地址的更新清單（這些地址已被證明對參與和郵寄信譽有害），並確保不會將電子郵件傳送給他們。 在所有 Adobe 客户共有的一个全局禁止列表中管理此列表。全局禁止列表中包含的地址和域名被隐藏起来。在投递报告中仅指示被排除的收件人数量。

## 為何隱藏清單？ {#why-suppression-list}

為了控制收件匣擁有者收到的電子郵件訊息，並確保他們僅收到想要的訊息，網際網路服務提供者(ISP)和商業垃圾郵件篩選器擁有其專屬的演演算法，可根據其使用的IP位址和傳送網域來追蹤電子郵件寄件者的整體信譽。

如果您不接受他們的意見（例如垃圾郵件投訴、退回等）， 他們會考量到您的聲譽。 隱藏清單可協助您接受ISP的意見回饋。

系統會自動從郵件傳遞中排除其電子郵件地址已被抑制的收件者。 这样可加快投放速度，因为错误率对投放速度有显著的影响。

## 隱藏清單上有什麼？ {#what-s-on-suppression-list}

地址會新增到隱藏清單中，如下所示：

* 全部 **硬跳出** 和 **垃圾郵件投訴** 在單一發生次數後，自動將對應位址傳送至隱藏清單。

* **軟退信** 不要立即傳送位址至隱藏清單，但會增加錯誤計數器。 數個 [重試](../configuration/retries.md) 然後執行，而當錯誤計數器達到臨界值時，該地址就會新增到隱藏清單中。

* 您也可以 [**手動** 新增地址或網域](../configuration/manage-suppression-list.md#add-addresses-and-domains) 至隱藏清單。

進一步瞭解中的硬跳出和軟跳出 [本節](#delivery-failures).

>[!NOTE]
>
>取消訂閱的使用者地址無法傳送到隱藏清單，因為他們沒有接收電子郵件 [!DNL Journey Optimizer]. 他們的選擇在Experience Platform層級處理。 進一步瞭解 [選擇退出](../privacy/opt-out.md).

針對每個地址，隱藏的基本原因和隱藏類別（軟式、硬式等） 會顯示在隱藏清單中。 進一步瞭解如何存取和管理隱藏清單 [本節](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>設定檔具有 **[!UICONTROL 已隱藏]** 在訊息傳送過程中會排除狀態。 因此，當 **歷程報告** 會將這些設定檔顯示為已移動通過歷程([讀取區段](../building-journeys/read-segment.md) 和 [訊息活動](../building-journeys/journeys-message.md))， **以電子郵件傳送報告** 不會將其納入 **[!UICONTROL 已傳送]** 量度，因為這些量度在傳送電子郵件前會被篩選掉。
>
>進一步瞭解 [即時報告](../reports/live-report.md) 和 [全域報告](../reports/global-report.md). 若要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### 投放失败 {#delivery-failures}

傳送失敗時，有兩種型別的錯誤：

* **硬跳出**. 硬跳出表示電子郵件地址無效（即不存在電子郵件地址）。 這涉及來自接收電子郵件伺服器的退回訊息，明確指出地址無效。
* **軟退信**. 這是有效的電子郵件地址發生的暫時電子郵件彈回。

A **硬跳出** 自動將電子郵件地址新增至隱藏清單。

A **軟退信** <!--or an **ignored** error--> 發生次數太多也會在多次重試後將電子郵件地址傳送至隱藏清單。 [進一步瞭解重試](../configuration/retries.md)

如果您繼續傳送至這些地址，可能會影響您的傳送率，因為它會告知ISP您可能未遵循電子郵件地址清單維護最佳實務，因此可能不是值得信賴的寄件者。

### 垃圾邮件投诉次数 {#spam-complaints}

隱藏清單會收集將您的訊息標示為垃圾訊息的電子郵件地址。 例如，如果有人寫信給客戶服務，要求永不再收到您的郵件，該人的電子郵件地址將在您的執行個體中隱藏，您將無法再傳送給該地址。

在收件者提交垃圾郵件投訴後將其傳送給他們，可能會對您的傳送信譽產生巨大影響，因為它會通知ISP您可能會傳送不需要的電子郵件，並且可能不會監聽您的收件者。

這可能會造成您的IP位址或傳送網域遭到封鎖，若將這些位址列入隱藏清單可避免發生這種情況。
