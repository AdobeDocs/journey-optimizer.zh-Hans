---
solution: Journey Optimizer
product: journey optimizer
title: 设置移动和Web
description: 了解如何配置和监测移动和Web渠道
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 通道，表面，技术，参数，优化器
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
TQID: https://experienceleague.adobe.com/wZkMADPKflUPDtBaSa0eEdHESX-0X0MQCqmk98fZn9k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 858
ht-degree: 0%

---

# 引导式渠道设置入门 {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="移动和Web配置名称"
>abstract="输入移动或Web配置的名称。 此名称将用于通过引导式渠道设置自动创建的每个资源。"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="使用Assurance进行验证"
>abstract="Adobe Experience Platform Assurance将嵌入到此工作流中，以帮助您检查SDK实施，并模拟和验证应用程序事件。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance概述"

**引导式渠道设置**&#x200B;是Adobe Journey Optimizer中简化的工作流，可帮助您快速配置移动和Web营销渠道。 它位于&#x200B;**管理** > **渠道** > **渠道配置**&#x200B;下，可跨Adobe Experience Platform、Journey Optimizer和数据收集自动创建基本资源，如标记属性、数据流和渠道配置。 您无需手动配置每个组件，而是按照引导式流程为您设置所有内容，这样营销团队就可以立即开始创建应用程序内消息、推送通知和Web体验。

引导式渠道设置支持以下平台和渠道。

>[!BEGINTABS]

>[!TAB iOS]

**SDK：** Apple的Swift

**渠道：**&#x200B;移动应用程序内消息、移动推送消息

>[!TAB Android]

**SDK：** Kotlin

**渠道：**&#x200B;移动应用程序内消息、移动推送消息

>[!TAB Web]

**SDK：** Javascript

**渠道：** Web基本

>[!ENDTABS]

请注意，对于要设置的每个平台，都需要创建单独的配置。 这是因为每个应用程序都需要唯一的渠道配置，这样可以灵活地决定您想要用于每个平台的渠道。

## 先决条件 {#prereq}

* 为有效实施这一目标，至关重要的是，组织内有权力和技术能力修改网站或移动代码的成员应监督设置。

  以下是运行引导式渠道设置所需的权限。

  +++ 所需权限

  <table>
    <thead>
      <tr>
        <th><strong>解决方案</strong></th>
        <th><strong>权限</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>数据收集</p>
        </td>
        <td>
          <ul>
            <li>公司权限&gt;资产</li>
            <li>资产权限：开发、发布、管理扩展和环境</li>
            <li>应用程序表面：管理应用程序配置</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>数据收集：管理数据流</li>
           <li>沙盒：授予对沙盒的访问权限</li>
            <li>管理区段：读取、创建、编辑和删除区段定义</li>
            <li>管理配置文件：读取、创建、编辑和删除配置文件</li>
            <li>读取数据集：对数据集的只读访问权限</li>
            <li>读取架构：对架构的只读访问权限</li>
            <li>读取身份命名空间：对身份命名空间的只读访问</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>活动：管理和发布活动</p>
        </td>
      </tr>
    </tbody>
  </table>

  +++

* 如果您使用的是现有配置选项，请确保您使用的是以下Adobe Experience Platform Mobile SDK扩展版本。 有关SDK设置的更多详细信息，包括所需的依赖项和初始化代码，请参阅[以下文档](https://experienceleague.adobe.com/zh-hans/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks)。

>[!BEGINTABS]

>[!TAB 用于iOS的] 

* Mobile Core v5.2.0或更高版本
* Adobe Journey Optimizer v5.1.1或更高版本


>[!TAB 用于Android的] 

* Mobile Core v3.1.0或更高版本
* Adobe Journey Optimizer v3.1.0或更高版本


>[!ENDTABS]


## 自动创建的资源 {#auto-create-resources}

引导式渠道设置简化了营销渠道的快速配置，使所有基本资源都可以在Experience Platform、Journey Optimizer和数据收集应用程序中随时使用。 这允许您的营销团队快速开始创建活动和历程。 以下是作为引导式渠道设置的一部分自动生成和配置的资源列表。

浏览以下选项卡以访问自动生成的所有资源的完整列表：

>[!BEGINTABS]

>[!TAB iOS]

对于&#x200B;**初始配置**，以下是单击&#x200B;**自动创建资源**&#x200B;时在&#x200B;**配置详细信息**&#x200B;屏幕上创建的所有资源的完整列表。

<table>
  <thead>
  <tr>
  <th><strong>解决方案</strong></th>
  <th><strong>自动创建的资源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>标记</p>
  </td>
  <td>
  <ul>
  <li>移动标记属性</li>
  <li>规则</li>
  <li>数据元素</li>
  <li>库</li>
  <li>环境（暂存、生产、开发）</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>标记扩展</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>同意（已启用默认同意策略）</li>
  <li>标识（使用默认ECID，使用默认拼接规则）</li>
  <li>移动核心</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance会话</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>数据流</p>
  </td>
  <td>
  <p>使用服务的数据流</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>数据集</li>
  <li>架构</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

对于&#x200B;**渠道设置**，下面是在&#x200B;**添加渠道**&#x200B;屏幕上创建的所有资源的完整列表。

<table>
  <thead>
  <tr>
  <th><strong>解决方案</strong></th>
  <th><strong>自动创建的资源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>渠道配置</li>
  <li>上传推送凭据（仅限移动设备推送消息）</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

对于&#x200B;**初始配置**，以下是单击&#x200B;**自动创建资源**&#x200B;时在&#x200B;**配置详细信息**&#x200B;屏幕上创建的所有资源的完整列表。

<table>
  <thead>
  <tr>
  <th><strong>解决方案</strong></th>
  <th><strong>自动创建的资源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>标记</p>
  </td>
  <td>
  <ul>
  <li>移动标记属性</li>
  <li>规则</li>
  <li>数据元素</li>
  <li>库</li>
  <li>环境（暂存、生产、开发）</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>标记扩展</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>同意（已启用默认同意策略）</li>
  <li>标识（使用默认ECID，使用默认拼接规则）</li>
  <li>移动核心</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance会话</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>数据流</p>
  </td>
  <td>
  <p>使用服务的数据流</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>数据集</li>
  <li>架构</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

对于&#x200B;**渠道设置**，下面是在&#x200B;**添加渠道**&#x200B;屏幕上创建的所有资源的完整列表。

<table>
  <thead>
  <tr>
  <th><strong>解决方案</strong></th>
  <th><strong>自动创建的资源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>渠道配置</li>
  <li>上传推送凭据（仅限移动设备推送消息）</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

对于&#x200B;**初始配置**，以下是单击&#x200B;**自动创建资源**&#x200B;时在&#x200B;**配置详细信息**&#x200B;屏幕上创建的所有资源的完整列表。

<table>
  <thead>
  <tr>
  <th><strong>解决方案</strong></th>
  <th><strong>自动创建的资源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>标记</p>
  </td>
  <td>
  <ul>
  <li>移动标记属性</li>
  <li>规则</li>
  <li>数据元素</li>
  <li>库</li>
  <li>环境（暂存、生产、开发）</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>标记扩展</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>同意（已启用默认同意策略）</li>
  <li>标识（使用默认ECID，使用默认拼接规则）</li>
  <li>移动核心</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance会话</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>数据流</p>
  </td>
  <td>
  <p>使用服务的数据流</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>数据集</li>
  <li>架构</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

