---
solution: Journey Optimizer
product: journey optimizer
title: 组件列表
description: 瞭解如何使用全域報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a41e82db-1fa4-478d-a5a2-324d1df1f8ee
source-git-commit: 26456f7c2d879843eb533209377b83fc0ccb5617
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 5%

---

# 组件列表 {#list-of-components-global}

下表提供報表中使用的量度清單，以及量度定義（視傳送型別而定）。

## 歷程量度 {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>動作已成功執行<br/> </td> 
   <td> 成功執行歷程的動作總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 輸入的設定檔<br/> </td> 
   <td> 到達歷程進入事件的個人總數。<br/> </td> 
</tr>
  <tr> 
   <td> 動作中發生錯誤<br/> </td> 
   <td>動作發生的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已退出的設定檔<br/> </td> 
   <td> 退出歷程的個人總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 失敗的個人歷程<br/> </td> 
   <td> 未成功執行的個別歷程總數。<br/> </td> 
</tr> 
 </tbody> 
</table>

## 電子郵件和簡訊維度和量度 {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> 退信数<br/> </td> 
   <td> 傳遞和自動傳回處理期間累計的錯誤總數（與已傳送訊息總數相關）。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與已傳送電子郵件相比跳出的電子郵件百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 单击次数<br/> </td> 
   <td> 在電子郵件中點按內容的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已送达 <br/> </td> 
   <td> 成功傳送的訊息數（相對於已傳送的訊息總數）。<br/></td> 
</tr> 
  <tr> 
   <td> 傳遞率<br/> </td> 
   <td> 成功傳送的訊息百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 傳遞期間發生且無法傳送至設定檔的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與已傳送的電子郵件相較之下，在傳送期間發生且無法傳送的錯誤百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。<br/> </td> 
</tr>
  <tr> 
   <td> 硬跳出<br/> </td> 
   <td> 永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 暫時性的總數，例如「不在辦公室」，或是技術錯誤，例如，如果寄件者型別是郵遞員。<br/> </td> 
</tr>
   <tr> 
   <td>優惠點按率<br/> </td> 
   <td>與優惠方案互動的使用者百分比。<br/> </td> 
</tr>
   <tr> 
   <td>優惠曝光率<br/> </td> 
   <td>已開啟優惠方案與已傳送優惠方案數的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>选件名称<br/> </td> 
   <td> 在傳遞中新增的優惠方案名稱。 如需位置的詳細資訊，請參閱此 <a href="../offers/offer-library/creating-personalized-offers.md">頁面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已傳送的優惠<br/> </td> 
   <td>優惠方案的傳送總數。<br/> </td> 
</tr> 
  <tr>
   <td>打开次数<br/> </td> 
   <td> 訊息開啟的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 開啟率<br/> </td> 
   <td> 與已傳遞電子郵件數量相比較的已開啟電子郵件總數。<br/> </td> 
</tr>
  <tr> 
   <td>位置名稱<br/> </td> 
   <td> 用來顯示優惠方案的位置名稱。 如需位置的詳細資訊，請參閱此 <a href="../offers/offer-library/creating-placements.md">頁面</a>. </td> 
</tr> 
  <tr> 
   <td> 重试<br/> </td> 
   <td> 重試佇列中的電子郵件數目。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 傳遞的傳送總數。<br/> </td> 
</tr>
  <tr> 
   <td> 軟退信<br/> </td> 
   <td> 臨時錯誤總數，例如完整收件匣。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾邮件投诉次数<br/> </td> 
   <td> 將郵件宣告為垃圾郵件或垃圾郵件的次數。<br/> </td> 
</tr>
  <tr> 
   <td> 已定位<br/> </td> 
   <td> 傳遞分析期間處理的訊息總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 唯一点击次数<br/> </td> 
   <td> 點按電子郵件中內容的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td>不重複點按率<br/> </td> 
   <td> 與傳遞互動的使用者百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 唯一打开次数<br/> </td> 
   <td>開啟傳遞的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消订阅<br/> </td> 
   <td> 對取消訂閱連結的點按次數。<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

## 應用程式內量度 {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>单击次数<br/> </td> 
   <td>與應用程式內訊息所含按鈕互動的收件者總數。<br/> </td> 
</tr>
  <tr> 
   <td>點按率<br/> </td> 
   <td>與已看到訊息的使用者相比，與應用程式內訊息中所包含按鈕互動的使用者百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>解除率<br/> </td> 
   <td> 收件者已解除的應用程式內訊息的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>展示次数<br/> </td> 
   <td> 傳送給所有使用者的應用程式內訊息總數。<br/> </td>
</tr>
  <tr> 
   <td>不重複曝光次數<br/> </td> 
   <td>應用程式內訊息傳遞至的不重複使用者人數。<br/> </td>
</tr>
 </tbody> 
</table>

## 推播通知量度

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>操作<br/> </td> 
   <td> 推播通知已傳遞的動作總數，例如按鈕點選或解除。<br/> </td> 
</tr>
  <tr> 
   <td>退信数<br/> </td> 
   <td> 傳遞和自動傳回處理期間累計的錯誤總數（與已傳送訊息總數相關）。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與已傳送的推播通知相比，已跳出的推播通知的百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已送达<br/> </td> 
   <td> 成功傳送的訊息數（相對於已傳送的訊息總數）。<br/> </td> 
</tr> 
  <tr> 
   <td> 傳遞率<br/> </td> 
   <td> 成功傳送的推播通知百分比。<br/> </td> 
</tr>
  <tr> 
   <td>參與<br/> </td> 
   <td> 此推播通知的開啟和動作總數，亦即設定檔是否已開啟推播，或按鈕是否已點按。<br/> </td> 
</tr> 
  <tr> 
   <td> 參與率<br/> </td> 
   <td> 此推播通知的開啟和動作百分比，亦即設定檔是否已開啟推播，或按鈕是否已點按。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 傳遞期間發生且無法傳送至設定檔的錯誤總數。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與已傳送的推播通知相比，在傳送期間發生且無法傳送的錯誤百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。<br/> </td> 
</tr>
  <tr> 
   <td> 打开次数<br/> </td> 
   <td> 傳送至裝置並由使用者點按以開啟應用程式的推播通知總數。 這類似於「推送點按」，但如果通知已關閉，則不會觸發「推送開啟」。<br/> </td> 
</tr> 
  <tr> 
   <td> 開啟率<br/> </td> 
   <td> 已開啟推播通知的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 傳遞的傳送總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已定位<br/> </td> 
   <td> 傳遞分析期間處理的推送訊息總數。<br/> </td> 
</tr>  
 </tbody> 
</table>

### 登陸頁面量度 {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>退信数<br/> </td> 
   <td>未與登入頁面互動且未完成訂閱動作的人數。<br/> </td> 
</tr>
 <tr> 
   <td>跳出率<br/> </td> 
   <td>未與登入頁面互動且未完成訂閱動作的人數（相對於造訪總數）。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>单击次数<br/> </td> 
   <td>內容在登入頁面中的點按次數。<br/> </td> 
</tr>
 <tr> 
   <td>點按率<br/> </td> 
   <td>登陸頁面中的點按百分比。<br/> </td>
</tr>
<tr>
<td>转化<br/> </td> 
   <td>與登入頁面互動（例如訂閱表單）的人數。<br/> </td> 
</tr>
<tr>
   <td>转化率<br/> </td> 
   <td>與登入頁面互動的人數（例如訂閱了表單），與造訪總數相關。<br/> </td> 
</tr>
 <tr> 
   <td>歷程<br/> </td> 
   <td>來自歷程的登陸頁面造訪次數。<br/> </td> 
</tr>
 <tr> 
   <td>其他來源<br/> </td> 
   <td>來自外部來源而非歷程的登陸頁面瀏覽次數。<br/> </td> 
</tr>
 <tr> 
   <td>造訪總數<br/> </td> 
   <td> 來自歷程和外部來源的登陸頁面造訪總數，包括一位收件者的多次造訪。<br/> </td> 
</tr>
 <tr> 
   <td>独特访客<br/> </td> 
   <td>造訪您登陸頁面的使用者人數，不會將一位收件者的多次造訪納入考量。<br/> </td> 
</tr>
 <tr> 
   <td>访问次数<br/> </td> 
   <td>登陸頁面的瀏覽次數，包括一位收件者的多次瀏覽。<br/> </td> 
</tr>
 </tbody> 
</table>
