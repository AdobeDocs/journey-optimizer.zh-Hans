---
title: 决策策略入门
description: 了解如何使用决策策略来投放优惠。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: 6cfea1a34cb004d4028f190be92d8365f90de6b2
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 27%

---

# 决策策略快速入门 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="决策是什么？"
>abstract="决策策略包含决策引擎挑选最佳内容的所有选择逻辑。决策政策是针对特定活动的。他们的目标是为每个轮廓选择最佳的报价，而活动创作允许您指示如何呈现所选的决策项目，包括应在消息中包含哪些项目属性。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="关于决策"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="定义决策策略"
>abstract="决策策略允许您从决策引擎中挑选最佳项目，并将其推送给合适的受众。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="关于决策"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="决策策略"
>abstract="决策策略允许您从决策引擎中挑选最合适的项目并交付给每个受众。"

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="投放"
>abstract="放置环境决定了决策引擎返回的项目在消息中出现的位置。您可以在报告中跟踪其在不同放置环境的性能。"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="从目录中选择决策属性"
>abstract="决策属性存储在目录的架构中。从所选目录中选择要在此使用的属性。"

决策策略是优惠的容器，它们利用决策引擎动态返回为每个受众成员提供的最佳内容。 其目标是为每个用户档案选择最佳优惠，而营销活动/历程创作允许您指示应如何显示选定的决策项目，包括要包含在消息中的项目属性。

➡️ [通过观看视频了解此功能](#video)

## 护栏和限制

* **支持的渠道** — 决策策略适用于这些渠道：基于代码的体验、电子邮件和推送通知。
* **推送通知SDK要求** — 具有推送通知的Experience Decisioning需要特定版本的Mobile SDK。 在实施此功能之前，请查看[发行说明](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}以确定所需的版本，并确保您已相应地升级。 您还可以在[此部分](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}中查看您的平台的所有可用SDK版本。
* **电子邮件镜像页面** — 目前，决策项不在电子邮件镜像页面中呈现。
* **跟踪和链接类型** — 要跟踪通过决策生成的链接，请在架构中将其定义为“决策Assets”。 基于属性的链接不可跟踪。
* **在电子邮件中嵌套决策策略** — 无法在已具有关联决策策略的父电子邮件组件中嵌套多个决策策略。
* **包含决策的重复历程/营销活动** — 如果您重复了包含决策策略的历程或营销活动，则复制的版本会引用原始电子邮件或基于代码的体验，从而导致出现错误。 复制后，请始终重新配置决策策略。
* **同意政策** — 对同意政策的更新最多需要48小时才能生效。 如果决策策略引用与最近更新的同意策略关联的属性，则不会立即应用更改。

  同样，如果将受同意策略约束的新配置文件属性添加到决策策略，则这些属性将可用，但只有在延迟过去后，才会实施与其关联的同意策略。

  同意策略仅适用于具有Adobe Healthcare Shield或Privacy and Security Shield加载项的组织。

* **AI排名** — 目前，使用决策的历程中的电子邮件渠道不支持AI排名。

* **内容模板** — 在内容中配置的任何决策策略都不会保存在模板中。 如果将模板应用于其他操作，则需要重新配置策略。

## 关键步骤 {#key}

在消息中利用决策策略的主要步骤如下：

1. **创建决策策略**

   在消息中添加决策策略，并配置要返回的项目数、选择策略和回退选项。

   ➡️ [了解如何创建决策策略](../experience-decisioning/create-decision-policy.md)

1. **在您的内容中使用决策策略**

   通过插入要在消息中显示的决策项中的属性，使用决策策略输出个性化您的内容

   ➡️ [了解如何在邮件中使用决策策略](../experience-decisioning/create-decision-policy.md)

## 操作说明视频 {#video}

了解如何使用Decisioning为受众个性化电子邮件。

>[!VIDEO](https://video.tv.adobe.com/v/3479199?quality=12)

了解如何使用Decisioning为受众个性化推送通知。

>[!VIDEO](https://video.tv.adobe.com/v/3479199?quality=12)
