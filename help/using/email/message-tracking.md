---
solution: Journey Optimizer
product: journey optimizer
title: 跟踪您的邮件
description: 了解如何添加链接和跟踪已发送邮件
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 連結，追蹤，監視，電子郵件
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 9592e9c1b0e9c8a1c606a9a187501542e496eddb
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 38%

---

# 添加链接和跟踪消息 {#tracking}

使用 [!DNL Journey Optimizer] 新增內容連結及追蹤傳送的訊息，以監控收件者的行為。

## 啟用追蹤 {#enable-tracking}

您可以在電子郵件層級啟用追蹤，方法是檢查 **[!UICONTROL 電子郵件開啟次數]** 和/或 **[!UICONTROL 按一下電子郵件]** 在歷程或行銷活動中建立訊息時的選項。

>[!BEGINTABS]

>[!TAB 在歷程中啟用追蹤]

![](assets/message-tracking-journey.png)

>[!TAB 在行銷活動中啟用追蹤]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>預設會啟用這兩個選項。

這可讓您透過以下方式追蹤收件者的行為：

* **[!UICONTROL 電子郵件開啟次數]**：已開啟的訊息。
* **[!UICONTROL 按一下電子郵件]**：按一下電子郵件中的連結。

## 插入链接 {#insert-links}

设计邮件时，可以添加指向内容的链接。

>[!NOTE]
>
>時間 [已啟用追蹤](#enable-tracking)，則會追蹤訊息內容中包含的所有連結。

要在电子邮件内容中插入链接，请执行以下步骤：

1. 选择一个元素，并单击上下文工具栏中的&#x200B;**[!UICONTROL 插入链接]**。

   ![](assets/message-tracking-insert-link.png)

1. 選擇您要建立的連結型別：

   * **[!UICONTROL 外部連結]**：插入外部URL的連結。

   * **[!UICONTROL 登陸頁面]**：插入登陸頁面的連結。 [在本节](../landing-pages/get-started-lp.md)中了解详情

   * **[!UICONTROL 一鍵選擇退出]**：插入連結以讓使用者快速取消訂閱您的通訊，而不需要確認選擇退出。 有关详细信息，请参阅[此部分](../privacy/opt-out.md#one-click-opt-out)。

   * **[!UICONTROL 外部選擇加入/訂閱]**：插入連結以接受來自您品牌的通訊。

   * **[!UICONTROL 外部選擇退出/取消訂閱]**：插入連結以取消訂閱接收來自您品牌的通訊。 在[此部分中](../privacy/opt-out.md#opt-out-management)中了解有关选择退出管理的更多信息。

   * **[!UICONTROL 映象頁面]**：插入在網頁瀏覽器中顯示電子郵件內容的連結。 有关详细信息，请参阅[此部分](#mirror-page)。

1. 您可以个性化自己的链接。在[本节](../personalization/personalization-syntax.md#perso-urls)中了解更多关于个性化 URL 的信息。

1. 保存更改。

1. 创建链接后，仍可以从右侧的&#x200B;**[!UICONTROL 组件设置]**&#x200B;窗格修改它。

   * 您可以編輯連結並變更其型別。
   * 可以通过选中相应的选项来选择是否为链接加下划线。

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>行銷型別的電子郵件訊息必須包含 [退出連結](../privacy/opt-out.md#opt-out-management)，這是異動訊息不需要的。 訊息類別(**[!UICONTROL 行銷]** 或 **[!UICONTROL 異動]**)在中定義 [管道表面](../configuration/channel-surfaces.md#email-type) 建立訊息時。

## 映象頁面的連結 {#mirror-page}

镜像页面是可通过 Web 浏览器在线访问的 HTML 页面。其內容與您的電子郵件內容相同。

若要在電子郵件中新增映象頁面的連結， [插入連結](#insert-links) 並選取 **[!UICONTROL 映象頁面]** 作為連結型別。

![](assets/message-tracking-mirror-page.png)

镜像页面是自动创建的。

>[!IMPORTANT]
>
>镜像页面链接是自动生成的，并且无法编辑。它们包含渲染原始电子邮件所需的所有加密的个性化数据。因此，使用具有较大值的个性化属性可能会生成冗长的镜像页面 URL，从而导致无法在具有最大 URL 长度限制的 Web 浏览器中访问链接。

发送电子邮件后，当收件人单击镜像页面链接时，电子邮件的内容将显示在他们的默认 Web 浏览器中。

>[!NOTE]
>
>在 [證明](preview.md#send-proofs) 傳送至測試設定檔，則映象頁面的連結未啟用。 它仅在最终邮件中激活。

映象頁面的保留期為60天。 經過此延遲後，將無法再使用映象頁面。

## 管理跟踪 {#manage-tracking}

[电子邮件设计器](content-from-scratch.md)允许您管理跟踪的 URL，例如编辑每个链接的跟踪类型。

1. 按一下 **[!UICONTROL 連結]** 圖示來顯示您要追蹤之內容的所有URL清單。

   此列表提供一个集中式视图，让您能够找到电子邮件内容中的每个 URL。

1. 要编辑链接，请单击相应的铅笔图标。

1. 如果需要，可以修改&#x200B;**[!UICONTROL 跟踪类型]**：

   ![](assets/message-tracking-edit-a-link.png)

   对于每个跟踪的 URL，可以将跟踪模式设置为下列值之一：

   * **[!UICONTROL 已跟踪]**：激活对此 URL 的跟踪。
   * **[!UICONTROL 选择禁用]**：将此 URL 视为选择退出或退订 URL。
   * **[!UICONTROL 镜像页面]**：将此 URL 视为镜像页面 URL。
   * **[!UICONTROL 从不]**：从不激活对此 URL 的跟踪。<!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

有關開啟次數和點按次數的報表，請參閱 [即時報告](../reports/live-report.md) 和 [全域報告](../reports/global-report.md).

## URL追蹤 {#url-tracking}

通常 [URL追蹤](email-settings.md#url-tracking) 在曲面層級進行管理，但不支援設定檔屬性。 目前唯一的方法是 [個人化URL](../personalization/personalization-syntax.md#perso-urls) 在電子郵件設計工具中。

若要將個人化URL追蹤引數新增至您的連結，請遵循下列步驟。

1. 選取連結並按一下 **[!UICONTROL 插入連結]** 從內容工具列。

1. 選取個人化圖示。 它僅適用於下列型別的連結： **外部連結**， **取消訂閱連結** 和 **選擇退出**.

   ![](assets/message-tracking-insert-link-perso.png)

1. 新增URL追蹤引數，並從運算式編輯器中選取您選擇的設定檔屬性。

   ![](assets/message-tracking-perso-parameter.png)

1. 保存更改。

1. 針對您要新增此追蹤引數的每個連結，重複上述步驟。

現在，當電子郵件寄出時，此引數會自動附加至URL的結尾。 然後，您可以在網站分析工具或效能報表中擷取此引數。

>[!NOTE]
>
>若要驗證最終URL，您可以 [傳送證明](preview.md#send-proofs) 和收到校樣後，按一下電子郵件內容中的連結。 URL應顯示追蹤引數。 在上述範例中，最終URL將為：https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number
