---
title: 模板Personalization的示例
description: Journey Optimizer Personalization示例
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876eid: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 1%

---

# 健康计划处方电子邮件 {#plan-prescription}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;遵循个性化用例，通过嵌套配置文件数组反复使用条件规则来构建健康计划电子邮件，其中列出了可供收取或撤回的处方。

>[!ENDSHADEBOX]

个人资料包含健康计划，每个计划都包含处方。 处方具有各种状态，如“准备就绪”、“召回”或“已接受”。

在此使用案例中，我们希望向每个用户档案发送一封电子邮件，其中包括准备好接收或撤回的所有处方。 单击下面的每个选项卡，以了解有关用于实施此用例的语法的更多信息。

>[!BEGINTABS]

>[!TAB 已呈现消息]

<p>嗨，John，Doe</p>
<p>以下是已准备好取药或已被召回的处方：</p>

**健康计划A**

<ul>

<li>
      <strong>处方ID：</strong>首选项1<br>
      <strong>名称：</strong>药物A<br>
      <strong>状态：</strong>就绪
   </li>

<li>
      <strong>处方ID：</strong> pres2<br>
      <strong>名称：</strong>药物B<br>
      <strong>状态：</strong>撤消
   </li>

</ul>

**健康计划B**

<ul>

<li>
      <strong>处方ID：</strong> pres4<br>
      <strong>名称：</strong>药物D<br>
      <strong>状态：</strong>就绪
   </li>

</ul>

>[!TAB HTML模板]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB 配置文件数据]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]

## 快速参考 {#quick-reference}

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

>[!BEGINTABS]

>[!TAB 概述]

**TL；DR**

此页面演示了一个完整的个性化用例：使用条件筛选对嵌套配置文件数组（包含处方健康计划）进行迭代，以在电子邮件中仅显示处于“就绪”或“召回”状态的处方。

**意图**

* 查看个性化健康计划电子邮件的呈现输出示例
* 了解使用条件数组迭代的嵌套`{{#each}}`和`{%#if%}`块的HTML模板
* 了解所需的配置文件数据结构：一个`plans`数组，其中每个计划都包含一个具有`state`字段的`prescriptions`数组

>[!TAB 术语表]

* **嵌套迭代**：在其他`{{#each}}`循环中使用`{{#each}}`循环遍历配置文件数据（例如，计划→处方）中的多级数组结构。
* **处方状态**：每个处方对象上的字段，用于指示其在此用例中的生命周期状态 — 使用的值为“就绪”、“召回”和“已提取”。 *（用例特定）*
* **`{%#if%}`/`{%/if%}`**：消息模板中使用的条件块语法，用于在迭代期间筛选数组项（不同于双曲线`{{#if}}` Handlebars语法）。

>[!TAB 术语]

* **规范名称：**&#x200B;嵌套数组迭代 — 变体：嵌套循环，嵌套每个，多级迭代
* **请勿混淆：** `{{#each}}` / `{{/each}}` （Handlebars迭代语法，双大括号）≠ `{%#if%}` / `{%/if%}` （条件语法，% — 大括号） — 在此模板中同时使用它们
* **请勿混淆：**“就绪”（处方可供提取）≠“撤消”（处方已被撤消）≠“提取”（处方已被收集 — 条件筛选条件从输出中排除）

>[!TAB 常见问题解答]

**问：电子邮件输出中包含哪些处方状态？**

只显示状态为“就绪”或“召回”的处方。 `{%#if prescription.state = "ready" or prescription.state = "recall"%}`条件筛选器将排除状态为“picked”的处方。

**问：此用例需要什么配置文件数据结构？**

具有`plans`数组的配置文件，其中每个计划对象都包含一个`prescriptions`数组。 每个处方对象必须具有`prescription_id`、`name`和`state`字段。

**问：如何在模板中迭代计划和处方？**

外部`{{#each profile.plans as |plan|}}`循环循环循环循环遍历每个健康计划。 其中，`{{#each plan.prescriptions as |prescription|}}`遍历每个计划的处方，并且有条件地块过滤器仅选择“就绪”或“撤消”状态。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
