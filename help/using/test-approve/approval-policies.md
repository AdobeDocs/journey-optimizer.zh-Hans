---
title: 创建和管理审批策略
description: 了解如何创建和管理审批策略。
role: User
level: Beginner
feature: Approval
exl-id: e518cb3c-f361-43a4-b9a5-ec070c612e75
source-git-commit: 4ce83c9cd3f70462c977db6e872a7ac51ea0e006
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 10%

---

# 创建和管理审批策略 {#approval-policies}

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_approval"
>title="请求审批"
>abstract="请求审批"

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_change"
>title="请求更改"
>abstract="请求更改"

>[!NOTE]
>
>要创建批准策略，您必须在Adobe Experience Platform中拥有系统管理员或产品管理员权限。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/home)

批准策略允许管理员为历程和营销活动建立验证流程。 此系统概述了特定条件，这些条件决定了历程或活动是否需要批准。 这些策略在复杂性上可能有所不同。 它们只需要求所有营销活动都由特定用户或团队进行审核，或根据营销活动的创建者建立标准。

您可以使用灵活的标准（如标记、营销活动/历程名称、渠道类型或请求者信息）来定位审批策略。 例如，您可以要求批准所有标记为“高风险”的对象，或批准任何符合特定命名模式的营销活动。

## 创建审批策略 {#create-policies}

>[!CONTEXTUALHELP]
>id="ajo_permissions_approval_policy"
>title="新的审批策略"
>abstract="在此屏幕中，输入名称并选择审批策略的上下文，然后生成条件，确定谁可以启动审批请求，以及谁可以验证审批请求。"

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_self_approval"
>title="阻止自我审批"
>abstract="启用此选项可阻止用户批准自己的批准请求，即使它们属于已指定为审阅者的用户组或角色也是如此。"

要创建批准策略，请执行以下步骤：

1. 从&#x200B;**[!UICONTROL 中的]**&#x200B;管理[!DNL Journey Optimizer]菜单中，依次访问&#x200B;**[!UICONTROL 权限]**&#x200B;和&#x200B;**[!UICONTROL 策略]**。

   ![“权限”菜单中的“创建审批策略”按钮](assets/policy_create_1.png)

1. 在&#x200B;**[!UICONTROL 审批策略]**&#x200B;选项卡中单击&#x200B;**[!UICONTROL 创建]**，选择&#x200B;**[!UICONTROL 审批策略]**，然后单击&#x200B;**[!UICONTROL 确认]**。

1. 输入策略的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 选择策略将应用于&#x200B;**[!UICONTROL 历程]**&#x200B;还是&#x200B;**[!UICONTROL 营销活动]**。

1. 启用&#x200B;**[!UICONTROL 块自批准]**&#x200B;以阻止历程/营销活动创建者批准自己的对象。

   ![](assets/policy_create_2.png)

您现在可以优化条件以指定谁可以启动审批请求以及谁可以验证审批请求。

## 设置审批策略的条件 {#conditions}

审批策略提供了灵活的定位选项，以满足您的治理需求。 您可以根据各种条件创建批准策略，包括：

* **促销活动/历程名称**：按名称定位特定对象
* **标记**：将策略应用于具有特定标记的所有营销活动或历程
* **渠道类型**：特定操作（电子邮件、短信、推送等）需要审批
* **营销活动类型**：为[操作与API触发的营销活动设置不同的规则](../campaigns/get-started-with-campaigns.md#campaign-types)
* **请求者**：根据创建活动或历程的人员定义策略

要定义与审批策略关联的条件，请执行以下步骤：

1. 访问您的&#x200B;**[!UICONTROL 审批策略]**。

1. 在&#x200B;**[!UICONTROL If]**&#x200B;菜单下，单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;以定义将触发审批请求的对象或用户。

1. 选择适当的&#x200B;**[!UICONTROL 类别]**、**[!UICONTROL 匹配规则]**&#x200B;和&#x200B;**[!UICONTROL 选项]**。

   例如，“如果操作与任何直邮匹配”或“如果请求者用户名与John Doe匹配”。

   ![审批策略条件生成器界面](assets/policy_condition_1.png)

   +++ 了解有关可用类别和选项的更多信息
   <table>
    <tr>
      <th>类别</th>
      <th>选项</th>
    </tr>
    <tr>
      <td rowspan="3">营销活动类型</td>
      <td>已计划（营销）</td>
    </tr>
    <tr>
    <td>API 触发（营销）</td>
    </tr>
    <tr>
    <td>API 触发（事务性）</td>
    </tr>
    <tr>
    <td rowspan="8">操作</td>
    <td>应用程序内</td>
    </tr>
    <tr>
    <td>推送通知</td>
   </tr>
    <tr>
    <td>短信</td>
    </tr>
    <tr>
    <td>电子邮件</td>
    </tr>
    <tr>
    <td>直邮</td>
    </tr>
    <tr>
    <td>Web</td>
    </tr>
    <tr>
    <td>基于代码</td>
    </tr>
    <tr>
    <td>内容卡片</td>
    </tr>
    <tr>
    <td>标记</td>
    <td>用于组织受众的标记的名称。 </td>
    </tr>
    <tr>
    <td>对象名称</td>
    <td>对象的名称。</td>
    </tr>
    <tr>
    <td>请求者用户名</td>
    <td>指定请求者的姓名和电子邮件地址</td>
    </tr>
    <tr>
    <td>请求者用户组</td>
    <td>指定请求者的用户组的名称</td>
    </tr>
    </table>

1. 若要添加更多条件，请单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;以定义其他规则，并选择&#x200B;**[!UICONTROL And]**&#x200B;或&#x200B;**[!UICONTROL Or]**&#x200B;以指定连接条件的方式。

1. 在&#x200B;**[!UICONTROL Then，将审批请求发送到]**&#x200B;菜单下，单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;以定义哪个用户可以接受审批请求。

1. 从&#x200B;**[!UICONTROL 类别]**&#x200B;下拉列表中，选择要选择用户组还是单个用户。

1. 然后，从&#x200B;**[!UICONTROL 选项]**&#x200B;下拉列表中，选择特定用户组或用户。

   选定的用户或用户组将负责验证审批请求。

   ![审批请求收件人选择界面](assets/policy_condition_2.png)

1. 若要添加更多条件，请单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;以定义其他规则，并选择&#x200B;**[!UICONTROL And]**&#x200B;或&#x200B;**[!UICONTROL Or]**&#x200B;以指定连接条件的方式。

1. 完全配置策略后，单击&#x200B;**[!UICONTROL 保存]**。

您现在可以激活审批策略以应用它。

## 激活和管理审批策略 {#activate-policies}

要应用审批策略，您必须激活它。 要执行此操作，请执行以下步骤：

1. 访问您的&#x200B;**[!UICONTROL 审批策略]**。

1. 然后，单击&#x200B;**[!UICONTROL 激活]**&#x200B;以将配置的条件应用到您的环境。

   >[!NOTE]
   >
   >激活策略后，便无法对其进行编辑。 要修改条件，请先取消激活策略。

   ![激活审批策略按钮](assets/policy_activate_1.png)

1. 从&#x200B;**[!UICONTROL 策略]**&#x200B;菜单中，打开高级选项，以根据需要编辑&#x200B;**[!UICONTROL 3&rbrace;、]**&#x200B;停用&#x200B;**[!UICONTROL 或]**&#x200B;复制&#x200B;**[!UICONTROL 策略。]**

   ![审批策略管理选项菜单](assets/policy_activate_2.png)
