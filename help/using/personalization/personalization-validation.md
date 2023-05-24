---
solution: Journey Optimizer
product: journey optimizer
title: 个性化验证
description: 進一步瞭解個人化驗證及疑難排解。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，驗證，錯誤，個人化
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# 个性化验证 {#personalization-validation}

## 驗證機制 {#validation-mechanisms}

在 **運算式編輯器** 畫面，使用 **驗證** 按鈕以檢查您的個人化語法。

>[!NOTE]
> 當您按一下 **新增** 按鈕以關閉編輯器視窗。

![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果個人化語法無效，則無法關閉運算式編輯器視窗。

## 常见错误 {#common-errors}

* **找不到路徑「XYZ」**

嘗試參照結構描述中未定義的欄位時。

在此案例中 **名字1** 未在設定檔結構描述中定義為屬性：

```
{{profile.person.name.firstName1}}
```

* **變數&quot;XYZ&quot;的型別不相符。 必須是陣列。 找到字串。**

嘗試對字串而非陣列進行反複運算時：

在此案例中 **product** 不是陣列：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **無效的Handlebars語法。 已找到`‘[XYZ}}’`**

使用無效的Handlebars語法時。

Handlebars運算式周圍有 **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **區段定義無效**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## 與優惠方案相關的特定錯誤 {#specific-errors}

與電子郵件或推播訊息中的優惠方案整合相關的錯誤具有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

驗證會在運算式編輯器中執行個人化內容驗證。

<table> 
 <thead> 
  <tr> 
   <th> 錯誤標題<br /> </th> 
   <th> 驗證/解析 <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>找不到id placementID和型別OfferPlacement的資源 <br/>
找不到id activityID和型別OfferActivity的資源<br/></td> 
   <td>檢查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>無法驗證資源。</td> 
   <td>Placement中的componentType應符合offerType選件</td> 
  </tr> 
   <tr> 
   <td>offerId中不存在公開URL。</td> 
   <td>影像選件（與決定和位置配對相關的所有個人化和遞補內容）應填入公開URL （deliveryURL不應空白）。</td> 
  </tr> 
  <tr> 
   <td>決定包含非設定檔屬性。</td> 
   <td>優惠方案模型使用方式應僅包含設定檔屬性。</td> 
  </tr> 
  <tr> 
   <td>擷取決定使用方式時發生錯誤。</td> 
   <td>當API嘗試擷取選件模型時，可能會發生此錯誤。</td> 
  </tr>
  <tr> 
   <td>優惠屬性優惠屬性無效。</td> 
   <td>檢查優惠方案drp中參照的優惠方案屬性是否有效。 以下是有效的屬性： <br/>
影像： deliveryURL， linkURL<br/>
文字：內容<br/>
HTML：內容<br/></td> 
  </tr> 
 </tbody> 
</table>
