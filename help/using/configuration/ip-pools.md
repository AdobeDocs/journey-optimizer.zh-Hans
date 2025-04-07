---
solution: Journey Optimizer
product: journey optimizer
title: 创建 IP 池
description: 了解如何管理IP池
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: IP、池、组、子域、可投放性
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 11%

---

# 创建 IP 池 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="设置 IP 池"
>abstract="IP 池收集您子域的 IP 地址以提高电子邮件的送达率。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="设置 IP 池"
>abstract="使用 Journey Optimizer，您可以创建 IP 池，将子域的 IP 地址分组在一起。这可以显著提高您的电子邮件送达率，因为这样做可以防止一个子域的声誉影响您的其他子域。"

## 关于IP池 {#about-ip-pools}

通过[!DNL Journey Optimizer]，您可以创建IP池以将子域的IP地址组合在一起。

强烈建议为电子邮件可投放性创建IP池。 这样，您可以防止子域的信誉影响您的其他子域。

例如，一个最佳实践是为营销消息设置一个IP池，为事务型消息设置另一个IP池。 这样一来，如果某条营销消息性能不佳并且被客户声明为垃圾邮件，则不会影响发送给该客户的事务型消息，这些客户仍会收到事务型消息（购买确认、密码恢复消息等）。

>[!CAUTION]
>
>IP池配置对所有环境都是通用的。 因此，任何IP池创建或编辑操作都将影响生产沙盒。

## 创建IP池 {#create-ip-pool}

要创建IP池，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL IP池]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建IP池]**。

   ![](assets/ip-pool-create.png)

1. 提供IP池的名称和描述（可选）。

   >[!NOTE]
   >
   >名称必须以字母(A - Z)开头，并且只包含字母数字字符或特殊字符( _， .， - )。

1. 从下拉列表中选择要包含在池中的IP地址，然后单击&#x200B;**[!UICONTROL 提交]**。

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >列表中提供了为您的实例配置的所有IP地址。

选择IP时，您可以从列表中看到与IP相关联的PTR记录。 这样，您可以在创建IP池时验证每个IP的品牌信息，例如，选择具有相同品牌信息的IP。 [了解有关PTR记录的更多信息](ptr-records.md)

![](assets/ip-pool-ptr-record.png)

>[!NOTE]
>
>如果没有为IP配置PTR记录，则无法选择该IP。 请联系您的Adobe代表以配置该IP的PTR记录。

创建IP池后，将鼠标悬停在IP池下拉列表下方显示的IP地址上时，会显示PTR信息。

![](assets/ip-pool-ptr-record-tooltip.png)

此时将创建IP池，并显示在列表中。 您可以选择它以访问其属性并显示关联的渠道配置（即消息预设）。 有关如何将通道配置与IP池关联的更多信息，请参阅[此部分](channel-surfaces.md)。

## 编辑IP池 {#edit-ip-pool}

要编辑IP池，请执行以下步骤。

1. 从列表中，单击IP池名称以将其打开。

1. 根据需要编辑其属性。 您可以修改说明，以及添加或删除IP地址。

   >[!NOTE]
   >
   >IP池名称不可编辑。 如果要修改它，您需要删除IP池，然后使用您选择的名称创建另一个池。

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >在考虑删除IP时，请格外谨慎，因为这将给其他IP带来额外负载，并且可能对您的可投放性产生严重影响。 如有任何疑问，请联系可投放性专家。

1. 保存更改。

更新会立即生效或异步生效，具体取决于与[通道配置](channel-surfaces.md)关联的IP池是否为：

* 如果IP池是&#x200B;**不是**&#x200B;与任何通道配置相关联，则更新是即时的（**[!UICONTROL 成功]**&#x200B;状态）。
* 如果IP池&#x200B;**与通道配置关联**，则更新最多可能需要3个小时（**[!UICONTROL 正在处理]**&#x200B;状态）。

>[!NOTE]
>
>在[创建通道配置](channel-surfaces.md#create-channel-surface)时，如果您选择的IP池处于编辑状态（**[!UICONTROL 正在处理]**&#x200B;状态）且从未与为该配置选择的子域关联，则无法继续创建配置。 [了解详情](channel-surfaces.md#subdomains-and-ip-pools)

要检查IP池更新状态，请单击&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 最近更新]**。

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池后，您可能必须等待：
>* 几分钟后才会被单一消息占用，
>* 直到下一次批处理时该IP池才能在批处理消息中生效。

您还可以使用&#x200B;**[!UICONTROL 删除]**&#x200B;按钮删除IP池。 请注意，您无法删除已与通道配置关联的IP池。

