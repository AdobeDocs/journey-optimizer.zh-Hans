---
title: PTR记录
description: 了解如何管理PTR记录
audience: administrators
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 3f83ef8074fd52ab611117282015f60e2e57b61d
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# PTR记录

## 关于PTR记录

指针记录(PTR)是一种域名系统(DNS)记录类型，它提供链接到IP地址的域名。

使用PTR记录，接收邮件服务器可以通过确定其IP地址是否与服务器所连接的名称对应来检查邮件服务器发送的真实性。

## 访问子域的PTR记录

在Adobe Journey Optimizer中委派子域后，将自动创建PTR记录并与此子域关联。 您可以从 **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** 菜单。

![](../assets/ptr-records.png)

该列表使用以下语法显示为每个委派的子域生成的PTR记录：

* “r”表示记录，
* “xx”表示IP地址的最后两个数字，
* 子域名。

您可以从列表中打开PTR记录以显示关联的子域名和IP地址。

## 编辑PTR记录 {#edit-ptr-record}

您可以修改PTR记录以编辑与IP地址关联的子域。

1. 在列表中，单击PTR记录名称以将其打开。

   ![](../assets/ptr-record-select.png)

1. 根据需要编辑子域。

   ![](../assets/ptr-record-subdomain.png)

   >[!NOTE]
   >
   >您无法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR record]** 字段。

1. 单击 **[!UICONTROL Save]** 确认更改。

安 **[!UICONTROL Updating]** 图标会显示在列表中PTR记录名称的旁边。

![](../assets/ptr-record-updating.png)

要检查PTR记录更新详细信息，请单击 **[!UICONTROL Updating]** 或 **[!UICONTROL Recent updates]** 图标。

![](../assets/ptr-record-recent-update.png)

您可以看到更新状态和请求的更改等信息。

![](../assets/ptr-record-updates.png)

## 更新状态

PTR记录更新可以具有以下状态：

* **[!UICONTROL Processing]**:PTR记录更新已提交，正在进行验证过程。
* **[!UICONTROL Success]**:已验证更新的PTR记录，并且新子域现在与IP地址关联。
* **[!UICONTROL Failed]**:在PTR记录更新验证期间，一个或多个检查失败。

### 处理时间

将执行多项可投放性检查，以验证要与IP地址关联的新子域是否有效。 <!--The processing time is around **48h-72h**, and can take up to **7-10 days**. Learn more on the checks performed during the validation cycle in [this section](#create-message-preset).-->

>[!NOTE]
>
>在更新过程中，无法修改PTR记录。 您仍可以单击其名称，但 **[!UICONTROL Subdomain]** 字段灰显。 更新成功后，才会反映更改。

在验证过程中，旧子域仍与IP地址关联。

### 成功

验证过程成功后，新子域将自动与IP地址关联。

### 失败

如果验证过程失败，则显示较旧的PTR记录。 之前与IP地址关联的有效子域将保持不变。

可能的更新错误类型如下：
* 无法为PTR记录创建新的转发DNS
* 更新记录失败
* 重新载入任务相关性失败

更新失败后，PTR记录将再次变得可编辑。 您可以单击其名称，然后再次更新子域。
