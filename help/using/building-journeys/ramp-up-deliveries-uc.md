---
solution: Journey Optimizer
product: journey optimizer
title: 加快傳遞速度
description: 瞭解如何加快傳遞速度
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 可遞送性、歷程、使用案例、電子郵件、聲譽
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 3%

---

# 使用案例：加快傳遞速度{#use-case-ramp-up-your-deliveries}

如果您最近移至其他電子郵件服務提供者、IP位址或電子郵件網域或子網域，您必須建立您作為寄件者的信譽。 否則，您的傳遞可能會被封鎖或移至收件者信箱的垃圾郵件資料夾。 瞭解如何透過IP暖身提高您的電子郵件聲譽 [傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target="_blank"}.

若要讓IP暖和，您可以逐步增加傳送數量。 深入瞭解 [在Journey Optimizer中最佳化傳遞能力](../reports/deliverability.md).

此使用案例的目的是建立歷程，以加快電子郵件傳送速度。 若要設定此歷程，請遵循下列步驟：

1. 创建历程. [了解更多信息](journey-gs.md)。

1. 新增 **[!UICONTROL 條件]** 活動至歷程。 [了解更多信息](condition-activity.md)。

1. 在 **[!UICONTROL 條件]** 活動設定，設定您傳送的收件者數目上限：

   1. 在 **[!UICONTROL 條件]** 活動設定，設定 **[!UICONTROL 型別]** 欄位至 **[!UICONTROL 設定檔上限]**. [了解更多信息](condition-activity.md#profile_cap)。

   1. 設定 **[!UICONTROL 限制]** 此傳遞的收件者數目上限的欄位。

   ![](assets/profile-cap-condition.png)

   您可以逐步提高此上限，直到您的訂閱者總數為止。

1. 新增 **[!UICONTROL 電子郵件]** 動作活動到命名路徑之後 **[!UICONTROL 條件]** 活動。

   ![](assets/ramp-up-deliveries-message.png)

   歷程執行時，訊息會傳送到輸入的設定檔，最多為您指定的設定檔數量上限。 當達到此限制時，輸入的設定檔會採用替代路徑。

1. 使用您選擇的活動完成歷程。

在IP預熱後，您可以移除此條件。
