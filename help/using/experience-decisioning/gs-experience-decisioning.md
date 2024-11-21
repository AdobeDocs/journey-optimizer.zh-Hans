---
title: 开始使用Decisioning
description: 了解有关Decisioning的更多信息
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c179d81e664fea2b03bf734cafaf287709fa10a0
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 17%

---

# 开始使用Decisioning {#get-started-experience-decisioning}

## 什么是决策 {#about}

通过提供称为“决策项”的集中式营销优惠目录和复杂的决策引擎，决策简化了个性化流程。此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。

这些决策项目通过[新的基于代码的体验渠道](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based)无缝集成到广泛的集客界面中，该渠道现在可在Journey Optimizer营销活动中访问。 决策决策策略仅在基于代码的体验营销活动中可用。

## 护栏和限制 {#guardrails}

要确保优化使用决策，请牢记以下护栏和限制：

### 常规护栏 {#general}

* **优惠项目**：每个项目集合最多可包含500个优惠项目。
* **自定义属性**：决策项最多可包含100个自定义属性。
* **每个策略的选择策略和决策项**：决策策略支持最多10个合并的选择策略和决策项。

### 资格规则 {#eligibility}

* **嵌套级别**：嵌套深度限制为30个级别。 这是通过计数PQL字符串中的`)`个右括号来测量的。
* **规则字符串大小**：对于UTF-8编码字符，规则字符串的大小最多可达15KB。 这相当于15,000个ASCII字符（每个1字节），或3,750-7,500个非ASCII字符（每个2-4字节）。

### 排名公式 {#ranking}

* **嵌套级别**：嵌套深度限制为30个级别。 这是通过计数PQL字符串中的`)`个右括号来测量的。
* **公式字符串大小**：对于UTF-8编码字符，规则字符串的大小最多可达8KB。 这相当于8,000个ASCII字符（每个1字节），或2,000-4,000个非ASCII字符（每个2-4字节）。

## 决策关键步骤 {#steps}

使用Decisioning的主要步骤如下：

1. **分配适当的权限**。 决策仅适用于具有决策相关&#x200B;**[!UICONTROL 角色]**&#x200B;访问权限的用户，例如决策管理员。 如果您无法访问Decisioning，则必须扩展您的权限。

   +++了解如何分配决策管理者角色

   1. 要向[!DNL Permissions]产品中的用户分配角色，请导航到&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，然后选择决策管理器。

      ![](assets/decision_permission_1.png)

   1. 在&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加用户]**。

      ![](assets/decision_permission_2.png)

   1. 输入您的用户名或电子邮件地址，或从列表中选择用户并单击&#x200B;**[!UICONTROL 保存]**。

      如果之前没有创建用户，请参阅[有关添加用户的文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/ui/users)。

      ![](assets/decision_permission_3.png)

   随后，您的用户将收到一封重定向到您的实例的电子邮件。

+++

1. **配置自定义属性**：通过在目录架构中设置自定义属性，根据特定要求定制项目目录。

1. **创建决策项**&#x200B;以向您的目标受众显示。

1. **使用收藏集组织**：使用收藏集根据基于属性的规则对决策项进行分类。 将集合纳入您的选择策略，以确定应考虑的决策项目集合。

1. **创建决策规则**：决策项和/或选择策略中使用决策规则来确定可以将决策项显示给谁。

1. **实施排名方法**：创建排名方法并在决策策略中应用这些方法以确定选择决策项的优先级顺序。

1. **创建选择策略**：构建选择策略，该策略利用收藏集、决策规则和排名方法来识别适合显示到用户档案的决策项目。

1. **将决策策略嵌入到基于代码的营销活动中**：决策策略将多个选择策略相结合，以确定向目标受众显示的合格决策项。
