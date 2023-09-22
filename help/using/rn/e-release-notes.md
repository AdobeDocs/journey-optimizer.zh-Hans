---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
hide: true
hidefromtoc: true
source-git-commit: c9be63086b63fb5f4d6094d8bc7690464cf6b768
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 21%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。链接、屏幕和更新文档，会在发行之日发布于[发行说明](release-notes.md)中。

## 2023年9月早期发行说明 {#sept-rn-2023}

**发行日期**： 2023年9月26日至27日

### 新功能{#sept-2023-features}

此版本引入了下方列出的新功能。


<table>
<thead>
<tr>
<th><strong>合并的渠道报表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>渠道报表功能为分析师和营销人员提供了渠道级别的流量和参与量度的全面概述。 要访问“报告”菜单，您必须具有“查看渠道报告”权限。</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>数据集导出目标(GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可以将Journey Optimizer数据集导出到云存储目标。 通过此功能，您可以与云存储位置建立实时连接，以导出数据集的内容。</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>每个沙盒移动应用程序凭据存储</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>这项新功能允许您轻松管理推送凭据，并将其与应用程序表面中的专用沙盒关联。</p>
<p>有关更多信息，请参阅<a href="../in-app/inapp-configuration.md">详细文档</a>。</p>
</tr>
</tbody>
</table>

### 改进 {#sept-2023-improvements}

此版本包含下方列出的改进。

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**个性化**

* 除了可视片段之外，现在还可以通过表达式编辑器从Journey Optimizer界面创建、保存和重用表达式片段。 表达式片段替换以前保存的表达式。
* 您现在可以在Journey Optimizer中使用Adobe Experience Platform计算属性进行个性化。 计算属性是根据引入到Adobe Experience Platform中的支持配置文件的体验事件数据集计算的聚合值。

**警报**

* 引入了两种新型的系统报警。 现在，您可以在自定义操作或读取区段失败时收到通知。

**Web 渠道**

* 单页应用程序(SPA)现在可以在Web可视编辑器中创作。 您现在可以选择要将网页修改应用到哪些特定视图。 视图可定义为整个网站或网站上的一组可视化元素，例如主页、整个产品网站或所有结账页面上的投放首选项框架。 在Adobe Experience Platform Web SDK实施中定义视图需要一次性开发人员设置，这使得营销人员能够在SPA上创建并运行Adobe Journey Optimizer Web营销活动。

* 使用Web设计器编辑页面时，您现在可以直接从“修改”窗格向内容添加新更改，而无需从设计器界面中选择组件并进行编辑。
* 在设置Web子域时，除了使用已委派给Adobe的子域之外，您现在可以选择添加自己的子域。

**历程**

* 现在，自定义操作响应功能已正式推出。 这允许您在自定义操作中利用API调用响应，并根据这些响应编排您的历程。 此外，还新增了护栏，以将所有海关操作限制为每个端点5000次调用/秒。
* 复制历程时，您现在可以定义历程副本的名称。
* 现在，您可以在等待活动中定义的最长持续时间为29天，而不是30天。

**电子邮件渠道**

利用电子邮件平面配置中的新选项，可选择向用户档案发送事务型消息，即使其电子邮件地址在Adobe Journey Optimizer禁止列表上也是如此。

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->