---
title: 个性化验证
description: 了解有关个性化验证以及如何进行故障诊断的更多信息
feature: 个性化
topic: 个性化
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---


# 个性化验证 {#personalization-validation}

![](../assets/do-not-localize/badge.png)

## 验证机制

在表达式编辑器屏幕中， **Validate**&#x200B;按钮允许您验证个性化语法。

>[!NOTE]
> 单击&#x200B;**Add**&#x200B;以关闭编辑器窗口时，将自动执行验证。


![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果个性化语法无效，则无法关闭表达式编辑器窗口。


## 常见错误

* **找不到路径“XYZ”**

尝试引用架构中未定义的字段时。

在此例中，**firstName1**&#x200B;未在配置文件架构中定义为属性：

```
{{profile.person.name.firstName1}}
```

* **变量“XYZ”的类型不匹配。预期阵列。 找到字符串。**

尝试在字符串而不是数组上迭代时：

在这种情况下， **product**&#x200B;不是数组：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **句柄语法无效。找到`‘[XYZ}}’`**

使用无效的handlebars语法时。

Handlebars表达式被&#x200B;**{{expression}}**&#x200B;包围

```
   {{[profile.person.name.firstName}}
```

* **区段定义无效**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### 与选件相关的特定错误

与电子邮件或推送消息中的选件集成相关的错误具有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

验证在消息发布期间或在表达式编辑器中的个性化内容验证期间执行。

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
未找到ID为activityID且类型为OfferActivity的资源<br/></td> 
   <td>检查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>无法验证资源。</td> 
   <td>版面中的componentType应与offerType选件匹配</td> 
  </tr> 
   <tr> 
   <td>offerId中不存在公共URL。</td> 
   <td>图像选件（与决策和放置对关联的所有个性化和回退）应填充公共URL（deliveryURL不应为空）。</td> 
  </tr> 
  <tr> 
   <td>决策（以前称为选件活动）包含非用户档案属性。</td> 
   <td>选件模型的使用应仅包含配置文件属性。</td> 
  </tr> 
  <tr> 
   <td>获取决策使用情况时出错。</td> 
   <td>当API尝试获取选件模型时，可能会发生此错误。</td> 
  </tr>
  <tr> 
   <td>选件属性offer-attribute无效。</td> 
   <td>检查选件drp中引用的选件属性是否有效。 以下是有效属性：<br/>
图像：deliveryURL， linkURL<br/>
文本：content<br/>
HTML:内容<br/></td> 
  </tr> 
 </tbody> 
</table>

