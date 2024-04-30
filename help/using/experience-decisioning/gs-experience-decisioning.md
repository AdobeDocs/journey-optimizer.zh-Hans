---
title: 开始使用 Experience Decisioning
description: 了解有关Experience Decisioning的更多信息
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: f71795c99157ce43f5250aaf10eb0b97f235b454
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 23%

---

# 开始使用 Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX “您将在本文档指南中找到什么”]

* **[Experience Decisioning入门](gs-experience-decisioning.md)**
* 管理您的决策项目： [配置物料目录](catalogs.md) - [创建决策项目](items.md) - [管理物料集合](collections.md)
* 配置项目的选择： [创建决策规则](rules.md) - [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)

>[!ENDSHADEBOX]

## 什么是Experience决策 {#about}

>[!AVAILABILITY]
>
>experience decisioning功能目前仅作为测试版向部分用户提供。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。
>
>决策策略仅适用于基于代码的体验营销活动。

通过提供称为“决策项”的集中式营销优惠目录和复杂的决策引擎，体验决策简化了个性化操作。此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。

这些决策项通过新的基于代码的体验渠道无缝集成到广泛的入站表面中，现在可以在 Journey Optimizer 营销活动中访问。

## Experience Decisioning关键步骤 {#steps}

使用Experience Decisioning的主要步骤如下：

1. **分配适当的权限**. 决策仅适用于有权访问Experience Decisioning相关项目的用户 **[!UICONTROL 角色]** 例如“决策管理器”。 如果您无法访问决策，则必须扩展您的权限。

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

1. **配置自定义属性**：通过在目录架构中设置自定义属性，根据特定要求定制决策项目的目录。

1. **创建决策项目** 以向您的目标受众显示。

1. **使用收藏集组织**：使用收藏集根据基于属性的规则对决策项进行分类。 将集合纳入您的选择策略，以确定应考虑的决策项目集合。

1. **创建决策规则**：决策规则用在决策项目和/或选择策略中，以确定可以向谁显示决策项目。

1. **实施排名方法**：创建排名方法并在决策策略中应用它们以确定选择决策项目的优先级顺序。

1. **创建选择策略**：构建选择策略，这些策略利用收藏集、决策规则和排名方法来确定适合显示到用户档案的决策项目。

1. **将决策策略嵌入到基于代码的营销活动中**：决策策略将多个选择策略相结合，以确定向目标受众显示的合格决策项目。
