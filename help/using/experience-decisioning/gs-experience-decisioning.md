---
title: 开始使用Decisioning
description: 了解有关Decisioning的更多信息
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

---

# 开始使用Decisioning {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>Decisioning当前仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。
>
>目前，此功能不适用于已购买Adobe **Healthcare Shield**&#x200B;和&#x200B;**Privacy and Security Shield**&#x200B;附加产品的客户。

## 什么是决策 {#about}

Decisioning通过提供称为“决策项目”的集中营销优惠目录和复杂的决策引擎，简化了个性化。 此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。

这些决策项目通过[新的基于代码的体验渠道](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based)无缝集成到广泛的集客界面中，该渠道现在可在Journey Optimizer营销活动中访问。 决策决策策略仅在基于代码的体验营销活动中可用。


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
