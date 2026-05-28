---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Manager内容片段注意事项和疑难解答
description: Journey Optimizer中AEM内容片段的注意事项和常见问题。
topic: Content Management
role: User
level: Beginner
exl-id: de4f441e-c3a3-4759-a634-bc9029328ebb
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 764
ht-degree: 1%

---

# 注意事项和疑难解答 {#aem-fragments-limitations}

## 关键注意事项 {#considerations}

在[!DNL Journey Optimizer]中使用[!DNL Adobe Experience Manager]中的内容片段时，请记住以下事项：

* **内容片段类型**
   * 支持简单内容片段、嵌套内容片段和&#x200B;**内容片段变量**。 在[!DNL Journey Optimizer]中插入片段时选择变量。 如果不选择变量，则使用&#x200B;**Main**&#x200B;变量（片段在[!DNL Adobe Experience Manager]中的主要内容）。

* **多语言内容**
   * 必须在[!DNL Adobe Experience Manager]中创作、标记和发布每个变量。 在[!DNL Journey Optimizer]中，选择与每种消息语言或区域设置匹配的片段变体。
   * 变体之间没有自动语言解析或回退功能。

* **存储库访问权限**
   * [!DNL Journey Optimizer]仅与[!DNL Adobe Experience Manager] **发布**&#x200B;层（站点、内容片段）集成。 内容片段可通过未经过身份验证的公共端点使用。
   * 作者存储库可能显示在存储库选择器中，但只有发布到&#x200B;**发布**&#x200B;的片段才能在[!DNL Journey Optimizer]中使用。

* **内容片段状态**
   * 片段可以显示&#x200B;**[!UICONTROL 已发布]**&#x200B;或&#x200B;**[!UICONTROL 已修改]**&#x200B;状态；[!DNL Journey Optimizer]始终使用&#x200B;**最新发布的版本**。
   * 在[!DNL Adobe Experience Manager]中重新发布片段之前，发布后所做的更改不会反映在[!DNL Journey Optimizer]中。 这两种产品之间没有自动版本协调。

* **个性化**
   * 支持：配置文件属性、上下文属性、静态字符串和预声明的变量。
   * 不支持：派生或计算属性。

* **更新和版本控制**
   * 更新需要从[!DNL Adobe Experience Manager]手动重新发布。 没有自动版本协调。
   * 在[!DNL Adobe Experience Manager]中发布或重新发布内容片段时，[!DNL Journey Optimizer]将更新该片段并刷新&#x200B;**在活动营销活动或历程中引用该片段的所有变体**。
   * [!DNL Adobe Experience Manager] [发布操作](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-publication)可能延迟。 完成后，[!DNL Journey Optimizer]接收事件并刷新内容。
   * 成功更新后，对于单一历程，更改通常会在约&#x200B;**5分钟**&#x200B;内可用，对于批次用例，更改通常会在约&#x200B;**下一个批次**&#x200B;内可用。

* **缓存和校对**
   * 首次将片段添加到营销活动或历程时，[!DNL Journey Optimizer]将缓存该片段。 如果您选择的片段已通过&#x200B;**[!UICONTROL 打开AEM内容审查程序]**&#x200B;在其他地方使用，则会从[!DNL Journey Optimizer]缓存加载该片段。
   * 在[!DNL Adobe Experience Manager]中重新发布修改的片段后，[!DNL Journey Optimizer]将侦听该事件并更新缓存。
   * 验证始终反映&#x200B;**最近发布的**&#x200B;版本；您无法锁定历史版本以进行验证。

## 疑难解答 {#troubleshooting}

如果您在Journey Optimizer中使用Adobe Experience Manager内容片段时遇到问题，请参阅以下常见问题和解决方案：

| 问题 | 原因 | 解决方法 |
|-|-|-|
| **标记未找到**&#x200B;或&#x200B;**内容片段在选择器中不可见** | Adobe Experience Manager标记语法与必需的格式`ajo-enabled:{OrgId}/{SandboxName}`不匹配 | 验证标记ID是否使用正确的&#x200B;**组织ID**&#x200B;和&#x200B;**沙盒名称**。 确保没有空格或分隔符不正确。 更正标记后重新发布内容片段。 |
| **内容片段未出现在列表**&#x200B;中 | 内容片段处于草稿状态或未发布 | Journey Optimizer选择器中仅显示已批准和已发布的内容片段。 在Adobe Experience Manager中发布内容片段，并确保其处于已发布状态。 |
| **变量未定义错误** | 未在片段帮助程序标记中声明Personalization占位符 | 在片段帮助程序标记中添加所有必需的参数。 内容片段中使用的每个占位符必须使用其映射进行显式声明。 |
| **校对显示意外内容** | 校对使用Adobe Experience Manager中最新发布的版本 | 验证始终反映Adobe Experience Manager中内容片段的最新发布。 如果您最近在Adobe Experience Manager中进行了更改，请重新发布片段并刷新验证。 |
| **访问被拒绝(CPES)错误** | 用户角色无权访问某些属性 | 请联系您的系统管理员，以验证您的角色是否对个性化中使用的配置文件或上下文属性具有适当的权限。 |
| **片段显示空白或缺少内容** | 缺少所需的个性化参数或回退值 | 请确保提供了所有必需的参数，并考虑为可选属性添加回退值。 |
| **图像未呈现或显示为已损坏** | 内容片段中的图像URL是相对路径或无法从渠道访问 | 对图像字段使用&#x200B;**绝对** URL (`https://...`)。 不支持来自Adobe Experience Manager的相对路径。 在浏览器或消息预览中确认URL。 |
| **Experience League AEM链接返回404** | 过时的书签、预览内部版本或未发布的AEM帮助页面 | 打开实时Adobe Journey Optimizer文档中的[包含Experience Manager的内容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}主题，并从页面上的目录中导航，或搜索分区名称（例如&#x200B;**Dispatcher配置**）。 |

如果问题仍然存在，请与Adobe代表联系，告知有关内容片段ID、营销活动或历程ID的详细信息，以及显示的任何错误消息。
