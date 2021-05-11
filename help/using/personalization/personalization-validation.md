---
title: 个性化验证
description: 了解有关个性化验证的更多信息以及如何解决问题
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 个性化验证{#personalization-validation}

![](../assets/do-not-localize/badge.png)

## 验证机制

在表达式编辑器屏幕中，**验证**&#x200B;按钮允许您验证您的个性化语法。

>[!NOTE]
> 单击&#x200B;**添加**&#x200B;以关闭编辑器窗口时会自动执行验证。


![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果个性化语法无效，则无法关闭表达式编辑器窗口。


## 常见错误

* **找不到路径&quot;XYZ&quot;**

尝试引用未在模式中定义的字段时。

在这种情况下，**firstName1**&#x200B;未在用户档案模式中定义为属性：

```
{{profile.person.name.firstName1}}
```

* **变量“XYZ”的类型不匹配。需要阵列。 找到字符串。**

尝试在字符串而不是数组上迭代时：

在这种情况下，**product**&#x200B;不是数组：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **handlebars语法无效。找到`‘[XYZ}}’`**

当使用无效的handlebars语法时。

Handlebars表达式被&#x200B;**{{表达式}}**&#x200B;包围

```
   {{[profile.person.name.firstName}}
```

* **区段定义无效**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### 与优惠相关的特定错误

与电子邮件或推送消息中的优惠集成相关的错误有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

验证是在消息发布期间或在表达式编辑器中的个性化内容验证期间执行的。

<table> 
 <thead> 
  <tr> 
   <th> 错误标题<br /> </th> 
   <th> 验证/解决方案<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>找不到ID placementID和类型为OfferPlacement的资源<br/>
找不到ID为activityID且类型为OfferActivity的资源<br/></td> 
   <td>检查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>无法验证资源。</td> 
   <td>“放置”中的componentType应与offerType优惠匹配</td> 
  </tr> 
   <tr> 
   <td>公共URL在优惠 offerId中不存在。</td> 
   <td>图像优惠（与决策和放置对关联的所有个性化和回退）应填充公共URL（deliveryURL不应为空）。</td> 
  </tr> 
  <tr> 
   <td>该决定(以前称为优惠活动)包含非用户档案属性。</td> 
   <td>优惠模型使用应仅包含用户档案属性。</td> 
  </tr> 
  <tr> 
   <td>获取决策使用情况时出错。</td> 
   <td>当API尝试获取优惠模型时，可能会发生此错误。</td> 
  </tr>
  <tr> 
   <td>优惠属性优惠属性无效。</td> 
   <td>检查在优惠 drp中引用的优惠属性是否有效。 以下是有效属性：<br/>
图像：deliveryURL， linkURL<br/>
文本：content<br/>
HTML:内容<br/></td> 
  </tr> 
 </tbody> 
</table>

