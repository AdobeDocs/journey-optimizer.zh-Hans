---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 发行说明 {#release-notes}

本页列出了 [!DNL Journey Optimizer]. 您还可以查阅 [最新文档更新](documentation-updates.md) 页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 本地构建 [!DNL Adobe Experience Platform] 并从其最新创新和改进中继承。 在 [Adobe Experience Platform发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}。

![新闻稿](../assets/do-not-localize/nl-icon.png) 注册 [Adobe Journey Optimizer季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}，并每季度接收最新产品更新、令人兴奋的故事、用例、提示等，并直接发送至您的收件箱。


## 2022年10月版 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### 改进 {#oct-2022-improvements}

**历程**

* 的 **重复时强制重入** 选项已添加到定期读取区段计划参数中。 利用此选项，可让历程中仍存在的所有用户档案在下次执行时自动退出该历程。 停用选项后，用户档案必须先完成历程，然后才能再次进入另一个实例。 [了解更多](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**管理**

* 在用户界面中添加了一条消息，警告所有沙箱都具有子域、登陆页子域、PTR记录和IP池配置，因此对这些配置中的任何修改也会影响生产沙箱。
* 修改了从用户界面将禁止显示列表上传为CSV文件的步骤。 [了解更多](../configuration/manage-suppression-list.md#download-suppression-list)

**促销活动**

* 您现在可以存档已完成和已停止的营销活动。 [了解更多](../campaigns/modify-stop-campaign.md#archive)
