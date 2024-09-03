---
solution: Journey Optimizer
product: journey optimizer
title: 设置移动和Web
description: 了解如何配置和监测移动和Web渠道
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 通道，表面，技术，参数，优化器
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 0144809646e9e3b57089820290723ed7f9ed0acc
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 17%

---

# 开始使用引导式频道设置 {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="移动和 Web 配置名称"
>abstract="输入您的移动或网络配置的名称。此名称将用于通过引导频道设置自动创建的每个资源。"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="使用保证功能进行验证"
>abstract="Adobe Experience Platform保障将嵌入到此工作流中，以帮助您检查SDK实施，并模拟和验证应用程序事件。"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance 概述"

这种设置便于快速配置营销渠道，确保所有所需资源在 Experience Platform、Journey Optimizer 和数据收集中随时可用。这使您的营销团队能够开始创建营销活动和历程。

引导式渠道设置支持以下平台和渠道。

* 平台和SDK：

   * Apple的SWIFT解决方案，iOS

   * Android州科特林

   * Javascript， Web

* 渠道：

   * 移动应用程序内

   * 移动推送消息

   * Web基本

请注意，对于要设置的每个平台，都需要创建单独的配置。 这是因为每个应用程序都需要唯一的渠道配置，这样可以灵活地决定您想要用于每个平台的渠道。

## 先决条件 {#prereq}

* 为有效实施这一目标，至关重要的是，组织内有权力和技术能力修改网站或移动代码的成员应监督设置。

  以下是运行引导式渠道设置所需的权限。

+++ 所需的权限

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

* 如果您使用的是现有配置选项，请确保您使用的是以下Adobe Experience Platform Mobile SDK扩展版本。 有关SDK设置的更多详细信息，包括所需的依赖项和初始化代码，请参阅[以下文档](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en)。

  适用于Android的

   * Mobile Core v3.1.0或更高版本
   * Adobe Journey Optimizer v3.1.0或更高版本

  适用于iOS的

   * Mobile Core v5.2.0或更高版本
   * Adobe Journey Optimizer v5.1.1或更高版本

## 自动创建的资源 {#auto-create-resources}

引导式渠道设置简化了营销渠道的快速配置，使所有基本资源都可以在Experience Platform、Journey Optimizer和数据收集应用程序中随时使用。 这允许您的营销团队快速开始创建活动和历程。 以下是作为引导式渠道设置的一部分自动生成和配置的资源列表。

浏览以下选项卡，访问自动生成的所有资源的完整列表：

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
  <li>Adobe Experience PlatformEdge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP保证</li>
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
  <p>保证会话</p>
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
  <li>Adobe Experience PlatformEdge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP保证</li>
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
  <p>保证会话</p>
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
  <li>Adobe Experience PlatformEdge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP保证</li>
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
  <p>保证会话</p>
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

