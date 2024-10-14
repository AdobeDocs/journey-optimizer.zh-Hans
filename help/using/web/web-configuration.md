---
title: Web渠道配置
description: 创建网页渠道配置
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 2161baf0-38b7-4397-bffe-083929e8033a
source-git-commit: e3c597f66436e8e0e22d06f1905fc7ca9a9dd570
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 10%

---

# 配置Web体验 {#web-configuration}

## 创建Web渠道配置 {#create-web-configuration}

Web配置是由要交付内容的URL标识的Web属性。 它可以匹配单个页面URL或多个页面，从而允许您跨一个或多个网页进行修改。

要创建Web渠道配置，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。

   ![](assets/web_config_1.png)

1. 输入配置的名称和说明（可选）。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`字符。

1. 要为配置分配自定义或核心数据使用标签，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

1. 选择&#x200B;**Web**&#x200B;渠道。

   ![](assets/web_config_2.png)

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 [了解详情](../action/consent.md#surface-marketing-actions)

1. 在&#x200B;**[!UICONTROL Web设置]**&#x200B;部分中，选择以下选项之一：

   * **[!UICONTROL 单页]** — 如果要将更改仅应用于单个页面，请输入&#x200B;**[!UICONTROL 页面URL]**。

   * **[!UICONTROL 页面匹配规则]** — 若要定位多个匹配同一规则的URL，请构建一个页面匹配规则，并输入&#x200B;**[!UICONTROL 默认创作和预览URL]**。 [了解详情](#web-page-matching-rule)

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以保存更改。

当在营销活动或历程中使用Web渠道时，您现在可以选择此配置。

## 构建页面匹配规则 {#web-page-matching-rule}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="构建页面匹配规则"
>abstract="为了有效管理和定位一组具有相同标准的 URL，请创建一个页面匹配规则。通过使用此规则，您可以将多个 URL 合并到一条准则下，从而简化在这些页面上应用一致的设置和操作的流程。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="为内容创作和预览定义URL"
>abstract="该字段可确保该规则生成或匹配的页面具有指定的 URL，这对于有效地创建和预览内容至关重要。"

创建Web或[基于代码的体验](../code-based/get-started-code-based.md)配置时，您可以生成与规则&#x200B;]**匹配的**[!UICONTROL &#x200B;页面，以定位多个与同一规则匹配的URL。 因此，您可以一次性将相同的内容更改应用于多个页面。

例如，您可能希望将更改应用于整个网站的主页横幅，或添加一个显示在网站所有产品页面上的顶部图像。

1. 配置[Web](#web-configuration)或[基于代码的体验](../code-based/code-based-configuration.md)时，请选择&#x200B;**[!UICONTROL 页面匹配规则]**。

1. 为&#x200B;**[!UICONTROL 域]**&#x200B;和&#x200B;**[!UICONTROL 页面]**&#x200B;字段定义您的条件。 检查[此节](#available-operators)中可用的运算符。

   例如，如果您要编辑显示在Luma网站的所有女性产品页面上的元素，请选择&#x200B;**[!UICONTROL 域]** > **[!UICONTROL 开头为]** > `luma`和&#x200B;**[!UICONTROL 页面]** > **[!UICONTROL 包含]** > `women`。

   ![](assets/web_config_3.png)

1. 如果您的用例无法使用一条规则建模，则可以选择添加多条规则。 单击&#x200B;**[!UICONTROL 添加其他页面规则]**&#x200B;并重复上述步骤。

   >[!NOTE]
   >
   >您最多可以添加10个规则。

1. 在不同的规则之间可以使用&#x200B;**[!UICONTROL Or]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**&#x200B;运算符。

   当与定义的规则匹配的某个页面不应被定位时，**[!UICONTROL 排除]**&#x200B;非常有用。 例如，您可以定位包含`product`的所有`luma.com`页面，但以下页面除外： `https://luma.com/blogs/productinfo`。

   ![](assets/web_config_4.png)

1. 输入&#x200B;**[!UICONTROL 默认创作和预览URL]**。 此步骤可确保规则生成或匹配的页面具有用于内容创建和预览的指定URL。

### 用于构建页面匹配规则的可用运算符 {#available-operators}

在创建与多个页面](#web-page-matching-rule)匹配的[规则时，您可以在&#x200B;**[!UICONTROL 域]**&#x200B;和&#x200B;**[!UICONTROL 路径]**&#x200B;部分中使用不同的运算符来构建所需的规则。 下面列出了可用的运算符。

* **域**

  | 运算符  | 描述  | 示例  |
  |---|---|---|
  | 等于  | 域的完全匹配。  |
  | 开头为  | 匹配以输入的字符串开头的所有域（包括子域）。  | 例如：“Starts with： dev” ->匹配所有以“dev”开头的域和子域，如：dev.example.com、dev.products.example.com、developer.example.com  |
  | 结束于  | 匹配以输入字符串结尾的所有域（包括子域）。  | 例如：“Ends with： example.com” ->匹配所有以“example.com”结尾的域和子域，如：stage.example.com、prod.example.com、myexample.com  |
  | 通配符匹配  | “通配符匹配”运算符允许用户在字符串中间定义通配符匹配，如“dev”。*.example.com”。 验证规则是当运算符为“通配符匹配”时，值必须包含且只能包含一个通配符（星号）。  | 例如：“通配符匹配：dev.*.example.com” ->匹配域，如：dev.products.example.com、dev.mytest.products.example.com、dev.blog.example.com  |
  | 任何  | 匹配所有域 — 在跨域测试特定路径时很有用  |


* **路径**

<table>
    <thead>
    <tr>
        <th><strong>操作员</th>
        <th><strong>描述</th>
        <th><strong>示例</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>等于</td>
        <td>路径完全匹配。 </td>
        <td></td>
    </tr>
    <tr>
        <td>开始于</td>
        <td>匹配以输入的字符串开头的所有路径（包括子路径）。</td>
        <td></td>
    </tr>
    <tr>
        <td>结束于</td>
        <td>匹配以输入的字符串结尾的所有路径（包括子路径）。</td>
        <td></td>
    </tr>
    <tr>
        <td>任何</td>
        <td>匹配所有路径 — 在定位一个或多个域下的所有路径时很有用。</td>
        <td></td>
    </tr>
    <tr>
        <td>通配符匹配</td>
        <td>“通配符匹配”运算符允许用户在路径中定义内部通配符，如“/products/*/detail”。  路径**组件中的通配符*匹配任意字符序列，直到遇到第一个/字符。  /*/匹配任意字符序列（包括子路径）</td>
        <td>例如：“通配符匹配：/products/*/detail”，匹配所有路径，如： <ul><li>example.com/products/yoga/detail</li><li>example.com/products/surf/detail</li><li>example.com/products/tennis/detail</li><li>example.com/products/yoga/pants/detail</li></ul>例如：“Matches： /prod*/detail， matches all paths like： <ul><li>example.com/products/detail</li><li>example.com/production/detail</li></ul>不匹配以下路径： <ul><li>example.com/products/yoga/detail</li></ul></td>
    </tr>
    <tr>
        <td>Contains</td>
        <td>“contains”将转换为通配符（如“mystring”），并匹配包含此字符序列的所有路径。</td>
        <td>例如：“Contains： product”，匹配包含字符串product的所有路径，如： <ul><li>example.com/products</li><li>example.com/yoga/perfproduct</li><li>example.com/surf/productdescription</li><li>example.com/home/product/page</li></ul></td>
    </tr>
    </tbody>
</table>
