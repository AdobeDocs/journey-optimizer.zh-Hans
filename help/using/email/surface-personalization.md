---
solution: Journey Optimizer
product: journey optimizer
title: 配置电子邮件动态子域
description: 了解如何在电子邮件渠道平面级别配置动态子域
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 设置，电子邮件，配置，子域
hide: true
hidefromtoc: true
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# 配置电子邮件动态子域 {#surface-personalization}

在创建电子邮件界面时，为了增强对电子邮件设置的灵活性和控制， [!DNL Journey Optimizer] 允许您定义子域、标头和URL跟踪参数的个性化值。

## 添加动态子域 {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="个性化不可用"
>abstract="此表面是在没有任何个性化属性的情况下创建的。 如需在需要个性化时解决问题的步骤，请参阅文档。"

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="启用动态子域"
>abstract="创建电子邮件表面时，您可以根据使用表达式编辑器定义的条件设置动态子域。 您最多可以添加50个动态子域。"

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="某些子域可能不可用"
>abstract="由于挂起的反馈循环注册，某些子域当前不可选择。 此过程最多可能需要10个工作日。 完成后，您可以从所有可用的子域中进行选择。"

创建电子邮件界面时，您可以根据特定条件设置动态子域。

例如，如果您在法律上限制每个国家/地区使用专用电子邮件地址发送消息，则可以使用动态子域。 这样，您就可以创建一个单独的表面，其中包含多个对应于不同国家/地区的发送子域，而不是为每个国家/地区创建多个表面。 然后，您可以将基于不同国家/地区的客户整合到一个营销活动中。

要定义动态子域，请执行以下步骤。

1. 创建渠道表面。 [了解如何操作](../configuration/channel-surfaces.md)

1. 选择 **[!UICONTROL 电子邮件]** 渠道。

1. 在 **子域** 部分，启用 **[!UICONTROL 动态子域]** 选项。

   ![](assets/surface-email-dynamic-subdomain.png)

1. 选择第一个页面旁边的编辑图标 **[!UICONTROL 条件]** 字段。

1. 此 [表达式编辑器](../personalization/personalization-build-expressions.md) 打开。 在此示例中，设置一个条件，如 `Country` 等于 `US`.

   ![](assets/surface-email-edit-condition.png)

1. 选择要与此条件关联的子域。 [了解有关子域的更多信息](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >由于挂起，某些子域当前无法选择 [反馈环](../reports/deliverability.md#feedback-loops) 注册。 此过程最多可能需要10个工作日。 完成后，您可以从所有可用的子域中进行选择。 <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   所有位于美国的收件人将收到使用该国家/地区的选定子域的消息，这意味着所有涉及的URL（如镜像页面、跟踪URL或取消订阅链接）都将基于该子域进行填充。

1. 根据需要设置其他动态子域。 您最多可以添加50个项目。

   ![](assets/surface-email-add-dynamic-subdomain.png)

1. 选择 [IP池](../configuration/ip-pools.md) 以与曲面相关联。 [了解详情](email-settings.md#subdomains-and-ip-pools)

将一个或多个动态子域添加到曲面后，将根据为此曲面解析的动态子域填充以下项目：

* 所有URL（资源URL、镜像页面URL和跟踪URL）

* 此 [取消订阅URL](email-settings.md#list-unsubscribe)

* 此 **发件人电子邮件** 和 **错误电子邮件** 后缀

## 个性化您的标题(#personalize-header)

您还可以对表面中定义的所有标题参数使用个性化。

例如，如果您有多个品牌，则可以创建一个表面，并将个性化的值用于电子邮件标题。 这样，您就可以确保从不同品牌发送的所有电子邮件发送到每位客户，并且提供正确的电子邮件地址和正确地址 **从** 姓名和电子邮件。 同样，当收件人点击 **回复** 按钮时，您希望 **回复** 名称和电子邮件对应于正确用户的正确品牌。

要为表面标题参数使用个性化变量，请执行以下步骤。

1. 像往常一样定义标题参数。 [了解如何操作](email-settings.md#email-header)

1. 对于每个字段，选择编辑图标。

   ![](assets/surface-email-personalize-header.png)

1. 此 [表达式编辑器](../personalization/personalization-build-expressions.md) 打开。 根据需要定义条件，然后保存更改。<!--In this example, set a condition such as -->

   >[!NOTE]
   >
   >您只能选择 **[!UICONTROL 配置文件属性]** 和 **[!UICONTROL 辅助函数]**.

1. 对要添加个性化的每个参数重复上述步骤。

   >[!NOTE]
   >
   >如果将一个或多个动态子域添加到曲面，则 **发件人电子邮件** 和 **错误电子邮件** 将根据解析的填充后缀 [动态子域](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->
