---
title: 开始使用 Experience Decisioning
description: 了解有关Experience Decisioning的更多信息
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 19%

---

# 开始使用 Experience Decisioning {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>目前，体验决策功能仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。
>
>目前，已购买Adobe的客户无法使用该功能 **Health Shield** 和 **隐私和安全防护板** 附加产品。

## 什么是Experience决策 {#about}

通过提供称为“决策项”的集中式营销优惠目录和复杂的决策引擎，体验决策简化了个性化操作。此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。

这些决策项目通过新的基于代码的体验渠道(现在可在Journey Optimizer促销活动中访问)无缝集成到广泛的集客界面中。 Experience Decisioning决策策略仅适用于基于代码的体验营销活动。

## Experience Decisioning关键步骤 {#steps}

使用Experience Decisioning的主要步骤如下：

1. **分配适当的权限**. Experience Decisioning仅适用于有权访问相关Experience Decisioning的用户 **[!UICONTROL 角色]** 例如“决策管理器”。 如果您无法访问Experience Decisioning，则必须扩展您的权限。

   +++了解如何分配决策管理者角色

   1. 在中为用户分配角色 [!DNL Permissions] 产品，导航到 **[!UICONTROL 角色]** 选项卡并选择决策管理器。

      ![](assets/decision_permission_1.png)

   1. 从 **[!UICONTROL 用户]** 选项卡，单击 **[!UICONTROL 添加用户]**.

      ![](assets/decision_permission_2.png)

   1. 键入用户名或电子邮件地址，或从列表中选择用户并单击 **[!UICONTROL 保存]**.

      如果之前未创建用户，请参阅 [添加用户文档](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   随后，您的用户将收到一封重定向到您的实例的电子邮件。

+++

1. **配置自定义属性**：通过在目录架构中设置自定义属性，根据特定要求定制项目目录。

1. **创建决策项目** 以向您的目标受众显示。

1. **使用收藏集组织**：使用收藏集根据基于属性的规则对决策项进行分类。 将集合纳入您的选择策略，以确定应考虑的决策项目集合。

1. **创建决策规则**：决策规则用在决策项目和/或选择策略中，以确定可以向谁显示决策项目。

1. **实施排名方法**：创建排名方法并在决策策略中应用它们以确定选择决策项目的优先级顺序。

1. **创建选择策略**：构建选择策略，这些策略利用收藏集、决策规则和排名方法来确定适合显示到用户档案的决策项目。

1. **将决策策略嵌入到基于代码的营销活动中**：决策策略将多个选择策略相结合，以确定向目标受众显示的合格决策项目。
