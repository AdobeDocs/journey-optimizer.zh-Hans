---
solution: Journey Optimizer
product: journey optimizer
title: 个性化验证
description: 详细了解个性化验证以及如何进行故障排除。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器，验证，错误，个性化
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 155ae8ef14e5482d94e54b15962afa09aa6826fc
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 2%

---

# 个性化验证 {#personalization-validation}

## 验证机制 {#validation-mechanisms}

在&#x200B;**个性化编辑器**&#x200B;屏幕中，使用&#x200B;**验证**&#x200B;按钮检查您的个性化语法。

>[!NOTE]
> 单击&#x200B;**添加**&#x200B;按钮关闭编辑器窗口时，将自动执行验证。
>

![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果个性化语法无效，则无法关闭个性化编辑器窗口。
>

## 常见错误 {#common-errors}

* **找不到“XYZ”路径**

尝试引用架构中未定义的字段时。

在这种情况下，**firstName1**&#x200B;未定义为配置文件架构中的特性：

```
{{profile.person.name.firstName1}}
```

* **变量“XYZ”的类型不匹配。 应为数组。 找到字符串。**

当尝试对字符串而不是数组进行迭代时：

在这种情况下，**product**&#x200B;不是数组：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **无效的Handlebars语法。 找到`‘[XYZ}}’`**

当使用了无效的Handlebars语法时。

Handlebars表达式用&#x200B;**{{expression}}**&#x200B;括起来

```
   {{[profile.person.name.firstName}}
```

* **区段定义无效**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## 与优惠相关的特定错误 {#specific-errors}

与电子邮件或推送消息中的优惠集成相关的错误具有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

验证是在验证个性化编辑器中的个性化内容期间执行的。

<table> 
 <thead> 
  <tr> 
   <th> 错误标题<br /> </th> 
   <th> 验证/解析<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>未找到ID为placementID且类型为OfferPlacement的资源<br/>
未找到id为activityID且类型为OfferActivity的资源<br/></td> 
   <td>检查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>无法验证资源。</td> 
   <td>投放位置中的componentType应与offerType选件匹配</td> 
  </tr> 
   <tr> 
   <td>offerId中不存在公共URL。</td> 
   <td>图像选件（所有与决策和投放对关联的个性化和回退）应填充公共URL（deliveryURL不应为空）。</td> 
  </tr> 
  <tr> 
   <td>决策包含非配置文件属性。</td> 
   <td>选件模型用法应仅包含配置文件属性。</td> 
  </tr> 
  <tr> 
   <td>获取决策用法时出错。</td> 
   <td>当API尝试获取选件模型时，可能会发生此错误。</td> 
  </tr>
  <tr> 
   <td>选件属性offer-attribute无效。</td> 
   <td>检查选件drp中引用的选件属性是否有效。 以下是有效属性： <br/>
图像： deliveryURL， linkURL<br/>
文本： content<br/>
HTML：内容<br/></td> 
  </tr> 
 </tbody> 
</table>
