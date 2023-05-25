---
solution: Journey Optimizer
product: journey optimizer
title: PTR记录
description: 了解如何管理PTR记录
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子域， PTR，记录， DNS，域，邮件
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 9%

---

# PTR记录 {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="子域的 PTR 记录"
>abstract="指针记录 (PTR) 是一种 DNS 记录，它提供链接到 IP 地址的域名，帮助接收邮件服务器验证发件人的 IP 地址。您只有在与送达率专家进行讨论并充分考虑后，才能编辑 PTR 记录。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="子域的 PTR 记录"
>abstract="在 Journey Optimizer 中将子域委派给 Adobe 后，将自动创建 PTR 记录并将其与此子域相关联。"

## 关于PTR记录 {#about-ptr-records}

指针记录(PTR)是一种域名系统(DNS)记录，它提供链接到IP地址的域名。

利用PTR记录，接收邮件服务器可以通过识别其IP地址是否与服务器连接的名称对应来检查发送邮件服务器的真实性。

## 访问子域的PTR记录 {#access-ptr-records}

一次 [已委派子域](delegate-subdomain.md) 在Adobe Journey Optimizer中，会自动创建一个PTR记录并与此子域关联。 您可以从 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件配置]** > **[!UICONTROL PTR记录]** 菜单。

![](assets/ptr-records.png)

该列表显示了使用下列语法为每个委派的子域生成的PTR记录：

* 记录“r”，
* IP地址的最后两个数字是“xx”
* 子域名。

您可以从列表中打开PTR记录，以显示关联的子域名和IP地址。

## 编辑PTR记录 {#edit-ptr-record}

您可以修改PTR记录以编辑与IP地址关联的子域。

>[!CAUTION]
>
>PTR记录对所有环境都是通用的。 因此，对PTR记录的任何修改也将影响生产沙箱。
>
>编辑PTR记录时请格外小心。 如有任何疑问，请联系可投放性专家。

### 完全委派的子域 {#fully-delegated-subdomains}

要编辑包含子域的PTR记录，请执行以下操作 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 要Adobe，请执行以下步骤。

1. 从列表中，单击PTR记录名称以将其打开。

   ![](assets/ptr-record-select.png)

1. 选择子域 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 以从列表中Adobe。

   ![](assets/ptr-record-subdomain.png)

1. 单击 **[!UICONTROL 保存]** 以确认更改。

>[!NOTE]
>
>您无法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR记录]** 字段。

### 使用CNAME方法委派的子域 {#edit-ptr-subdomains-cname}

要编辑包含使用委派给Adobe的子域的PTR记录 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation)，请按照以下步骤操作。

1. 从列表中，单击PTR记录名称以将其打开。

   ![](assets/ptr-record-select-cname.png)

1. 使用以下方式选择委派给Adobe的子域 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation) 从名单上。

   ![](assets/ptr-record-subdomain-cname.png)

1. 您需要在托管平台上创建新的转发DNS记录。 为此，请复制Adobe生成的记录。 完成后，选中“I confirm...”框。

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >如果您收到此消息：“请先创建转发DNS，然后重试”，请执行以下步骤：
   >   * 如果成功创建了转发DNS记录，请检查DNS提供商。
   >   * DNS中的记录可能不会立即同步。 请等待几分钟，然后重试。


1. 单击 **[!UICONTROL 保存]** 以确认更改。

>[!NOTE]
>
>您无法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR记录]** 字段。

## 检查PTR记录更新详细信息 {#check-ptr-record-update}

确认PTR记录编辑后， **[!UICONTROL 正在处理]** 图标显示在列表中PTR记录的名称旁边。

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>此 [更新处理](#processing) 最多可能需要3小时。

要检查PTR记录更新详细信息，请单击其旁边的图标。 了解与中不同图标关联的状态的更多信息 [本节](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

您可以查看更新状态和请求的更改等信息。

![](assets/ptr-record-updates.png)

## PTR记录更新状态 {#ptr-record-update-statuses}

PTR记录更新可以具有以下状态：

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL 正在处理]**：PTR记录更新已提交，并正在验证过程中。
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL 成功]**：更新的PTR记录已通过验证，新子域现在已与IP地址关联。
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL 失败]**：在PTR记录更新验证期间，一项或多项检查失败。

### 处理时间 {#processing}

将执行多次可投放性检查，以验证要与IP地址关联的新子域是否有效。 这最多可能需要3小时。

>[!NOTE]
>
>在更新过程中，您无法修改PTR记录。 您仍然可以单击其名称，但是 **[!UICONTROL 子域]** 字段呈灰显状态。 更新成功后才会反映更改。

在验证过程中，旧子域仍与IP地址关联。

### 成功 {#success}

验证过程成功后，新子域将自动与IP地址关联。

### 失败 {#failes}

如果验证过程失败，则会显示较早的PTR记录。 以前与IP地址关联的有效子域保持不变。

可能的更新错误类型如下：
* 无法为PTR记录创建新的转发DNS
* 无法更新记录
* 无法重新载入相关性

更新失败时，PTR记录将再次变为可编辑。 您可以单击其名称并再次更新子域。
