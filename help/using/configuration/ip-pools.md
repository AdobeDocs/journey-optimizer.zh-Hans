---
solution: Journey Optimizer
product: journey optimizer
title: 创建 IP 池
description: 了解如何管理IP池
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 1%

---

# 创建 IP 池 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="设置IP池"
>abstract="您可以创建IP池以将子域的IP地址分组在一起，以改进电子邮件投放能力。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="设置IP池"
>abstract="使用Journey Optimizer，您可以创建IP池以将子域的IP地址分组在一起。 这可能会显着提高您的电子邮件投放能力，因为这样做可以防止子域的声誉影响您的其他子域。"

## 关于IP池 {#about-ip-pools}

使用 [!DNL Journey Optimizer]，则可以创建IP池以将子域的IP地址分组到一起。

强烈建议创建IP池，以便电子邮件可投放。 这样，您就可以防止子域的声誉影响您的其他子域。

例如，一个最佳实践是为营销消息提供一个IP池，为事务型消息设置一个IP池。 这样，如果您的其中一条营销消息性能不佳，且客户声明为垃圾邮件，则不会影响发送给该客户的事务型消息，该客户仍将接收事务型消息（购买确认、密码恢复消息等）。

## 创建IP池 {#create-ip-pool}

要创建IP池，请执行以下步骤：

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP池]** 菜单，然后单击 **[!UICONTROL 创建IP池]**.

   ![](assets/ip-pool-create.png)

1. 为IP池提供名称和描述（可选）。

   >[!NOTE]
   >
   >名称必须以字母(A-Z)开头，且只包含字母数字字符或特殊字符(_、 ., -)。

1. 从下拉列表中选择要包含在池中的IP地址，然后单击 **[!UICONTROL 提交]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >随您的实例配置的所有IP地址都可在列表中找到。

IP池现已创建并显示在列表中。 您可以选择它以访问其属性并显示关联的渠道表面（即消息预设）。 有关如何将通道表面与IP池关联的详细信息，请参阅 [此部分](channel-surfaces.md).

![](assets/ip-pool-created.png)

## 编辑IP池 {#edit-ip-pool}

要编辑IP池，请执行以下操作：

1. 在列表中，单击IP池名称以将其打开。

   ![](assets/ip-pool-list.png)

1. 根据需要编辑其属性。 您可以修改描述，并添加或删除IP地址。

   >[!NOTE]
   >
   >IP池名称不可编辑。 如果要修改IP池，您需要删除该IP池，然后使用您选择的名称创建另一个IP池。

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >考虑删除IP时请格外小心，因为这会给其他IP带来额外负载，并且可能会对您的投放能力造成严重影响。 如有疑问，请联系可投放性专家。

1. 保存更改。

根据与关联的IP池，更新可立即或异步生效 [通道表面](channel-surfaces.md) 或否：

* 如果IP池为 **not** 与任何通道表面相关联，更新是瞬时(**[!UICONTROL 成功]** 状态)。
* 如果IP池 **is** 与通道表面相关，更新最长可能需要3小时(**[!UICONTROL 处理]** 状态)。

>[!NOTE]
>
>When [创建通道曲面](channel-surfaces.md#create-channel-surface)，如果您选择的IP池位于版本(**[!UICONTROL 处理]** 状态)且从未与为该曲面选择的子域关联，则无法继续创建曲面。 [了解详情](channel-surfaces.md#subdomains-and-ip-pools)

要检查IP池更新状态，请单击 **[!UICONTROL 更多操作]** 按钮，选择 **[!UICONTROL 近期更新]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池后，您可能需要等待：
>* 在被单一报文使用前几分钟，
>* 直到IP池的下一个批处理消息生效。


您还可以使用 **[!UICONTROL 删除]** 按钮以删除IP池。 请注意，您无法删除已与通道表面关联的IP池。

