---
solution: Journey Optimizer
product: journey optimizer
title: IP预热计划入门
description: 了解如何实施IP预热计划
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、池、组、子域、可投放性
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 7%

---

# IP预热计划入门 {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* **[IP预热入门](ip-warmup-gs.md)**
* [创建IP预热活动](ip-warmup-campaign.md)
* [创建IP预热计划](ip-warmup-plan.md)
* [运行IP预热计划](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>IP预热功能目前仅作为测试版提供给部分用户。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

替换为 [!DNL Journey Optimizer]，您可以按照最佳可投放性实践以标准化且高效的方式直接从用户界面执行IP预热工作流。

>[!CAUTION]
>
>此功能仅适用于电子邮件渠道。

使用新平台发送电子邮件时，Internet服务提供商(ISP)会怀疑无法识别的IP地址。 如果突然发送大量电子邮件，ISP通常会将其标记为垃圾邮件。

要避免被标记为垃圾邮件，您可以使用IP预热计划功能逐步增加发送量。 中的新选项 **[!UICONTROL 管理]** 菜单可让您更顺利地执行操作，而不是创建复杂的每日历程。 这应该可以确保启动阶段的顺利发展，并帮助您降低地址无效的总比率。

>[!NOTE]
>
>在中了解更多有关利用IP预热提高您的电子邮件声誉的信息 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

实施IP预热计划的关键步骤如下：

1. 您首先需要在启用IP预热选项的情况下创建一个或多个营销活动。 [了解详情](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. 在中创建IP预热计划 [!DNL Journey Optimizer] 并上传之前填充IP预热数据的Excel工作表。 [了解详情](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. 为计划的每个阶段选择一个营销活动并激活相应的运行。 [了解详情](ip-warmup-running.md)
