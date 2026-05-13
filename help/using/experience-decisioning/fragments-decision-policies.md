---
title: 在决策策略中利用片段
description: 了解如何在决策策略中利用片段
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
TQID: https://experienceleague.adobe.com/5Vpngi03UnC9YPlB5tdTRcd0NoT7iglH2pRDkmeZKOg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2225d3c796e777f459bebc35a5c33ce1a0635f42
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# 在决策策略中利用片段 {#fragments}

如果您的决策策略包含决策项目，包括片段，则您可以在决策策略中创作消息时利用这些片段。 [了解有关片段的更多信息](../content-management/fragments.md)

>[!AVAILABILITY]
>
>此功能适用于&#x200B;**基于代码的体验**&#x200B;和&#x200B;**电子邮件**&#x200B;渠道。

例如，假设您要为多个移动设备型号显示不同的内容。 将指定的片段（每个片段属于不同的电话型号）添加到您在决策策略中使用的决策项目中。 [了解如何操作](items.md#attributes)。

决策项的![片段部分，显示片段引用和放置键。](assets/item-fragments.png){width=70%}

完成后，您可以使用以下任一方法：

>[!BEGINTABS]

>[!TAB 直接插入代码]

只需将下面的代码块复制并粘贴到决策策略代码中。 将`variable`替换为片段ID，将`placement`替换为片段引用键：

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB 按照详细步骤操作]

1. 导航到&#x200B;**[!UICONTROL 帮助程序函数]**&#x200B;并将&#x200B;**Let**&#x200B;函数`{% let variable = expression %} {{variable}}`添加到代码窗格，您可以在代码窗格中声明片段的变量。

   ![决策策略代码编辑器，显示添加到代码窗格的Let帮助程序功能。](assets/decision-let-function.png)

1. 使用&#x200B;**Map** > **Get**&#x200B;函数`{%= get(map, string) %}`构建表达式。 映射是决策项中引用的片段。 该字符串可以是您在决策项中输入的设备模型，作为&#x200B;**[!UICONTROL 片段引用键]**。

   ![用于引用片段映射和片段引用键的Map和Get函数。](assets/decision-map-function.png)

1. 您还可以使用上下文属性，该属性将包含此设备型号ID。

   ![为设备模型标识符选择的上下文属性。](assets/decision-contextual-attribute.png)

1. 添加您为片段选择的变量作为片段ID。

   从决策策略代码中的决策项设置的![片段ID变量。](assets/decision-fragment-id.png)

>[!ENDTABS]

将从决策项的&#x200B;**[!UICONTROL 片段]**&#x200B;部分中选择片段ID和引用键。

>[!WARNING]
>
>如果片段键不正确或片段内容无效，渲染可能会失败并在Edge调用中导致错误。
>
>为了避免在片段暂时不可用时失败，使用了`required=false`标志，因此跳过了片段。 [了解详情](#temporary-unavailable-fragments)

## 使用和护栏 {#fragments-guardrails}

### 在电子邮件中模拟内容和表达式片段 {#simulate-content-expression-fragments}

对于&#x200B;**电子邮件**&#x200B;渠道，当您&#x200B;**[!UICONTROL 发送验证]**&#x200B;或激活营销活动时，与决策项关联的表达式片段正确显示。 但是，**[!UICONTROL 模拟内容]**&#x200B;不显示决策项中的表达式片段。

### 电子邮件中的可视化片段和决策项 {#visual-fragments-decision-items}

您无法将&#x200B;**[!UICONTROL 可视化片段]**&#x200B;分配给决策项，此上下文中仅支持&#x200B;**表达式片段**。

### 决策项和上下文属性 {#decision-item-context-attributes}

默认情况下，[!DNL Journey Optimizer]片段不支持决策项属性和上下文属性。 但是，您可以改用全局变量，如下所述。

假设您要在片段中使用&#x200B;*sport*&#x200B;变量。

1. 在片段中引用此变量，例如：

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. 在决策策略块中使用&#x200B;**Let**&#x200B;函数定义变量。 在以下示例中，*sport*&#x200B;是使用决策项属性定义的：

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

### 决策项片段内容验证 {#fragment-content-validation}

* 由于这些片段的动态性质，在营销活动中使用时，会为决策项目中引用的片段跳过在营销活动内容创建期间的消息验证。

* 片段内容的验证仅在片段创建和发布期间进行。

* 对于JSON类型的表达式片段，在保存片段时会语法验证内容。 验证错误显示为警报。

在运行时，将验证营销活动内容（包括决策项中的片段内容）。 如果验证失败，则不会呈现营销活动。

### 暂时不可用的片段被跳过 {#temporary-unavailable-fragments}

当历程或营销活动引用附加到决策项的片段时，在更新的片段在Edge上可用之前可能会有短暂的同步延迟。

为避免在片段暂时不可用时失败，片段现在默认将`required`标志设置为`false`，以便跳过这些片段，而不是导致历程或营销活动失败。

这意味着如果片段在Edge上暂时不可用，则忽略该片段即可。 如果片段可用，它将正常呈现。

**示例**

如果您的决策策略符合两个优惠的条件，并且每个优惠都有片段，例如“20%优惠”和“30%优惠”，但第二个片段暂时不可用，因为`required=false`，系统将呈现可用优惠（20%优惠）并跳过另一个片段（30%优惠），而不是导致历程或营销活动失败。 这提高了内容仍在同步时的可靠性。

>[!NOTE]
>
>您仍然可以通过将`required`标志设置为`true`来将片段标记为必需。 但是，如果片段暂时缺失，可能会导致历程或营销活动渲染失败。
