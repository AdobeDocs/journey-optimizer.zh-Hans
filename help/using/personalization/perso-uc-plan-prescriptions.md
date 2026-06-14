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
source-git-commit: 378c98d4dc9552de3eed68eda59d9917c2b56347
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

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
      <strong>处方ID：</strong> pres1<br>
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
