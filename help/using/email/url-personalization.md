---
solution: Journey Optimizer
product: journey optimizer
title: 使电子邮件中的URL个性化
description: 了解动态生成URL并保持跟踪可靠的最佳实践和限制
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: url，链接，个性化，跟踪，编码，大括号
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# 使电子邮件中的URL个性化 {#url-personalization}

个性化URL可帮助您通过[!DNL Journey Optimizer]电子邮件提供情境式体验，例如生成特定于收件人的链接或附加动态参数。

用户档案会将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于用户档案属性。

## 个性化URL {#personalize-url}

要个性化URL，请执行以下步骤。

1. 在Email Designer中，在内容中选择一个元素，然后[使用上下文工具栏插入链接](message-tracking.md#insert-links)。

   >[!IMPORTANT]
   >
   >Personalization仅适用于&#x200B;**[!UICONTROL 外部链接]**、**[!UICONTROL 退订链接]**&#x200B;和&#x200B;**[!DNL Opt-Out]**。 确保选择适当的链接类型。

1. 选择个性化图标。

   ![](assets/message-tracking-insert-link-perso.png)

1. 使用个性化编辑器添加要个性化URL的用户档案属性。

1. 保存更改。

以下是一些个性化URL的示例：

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>在个性化编辑器中编辑个性化URL时，出于安全原因，将禁用帮助程序功能和受众成员资格。
>
>url内使用的个性化令牌不支持空格。

要获得可靠的渲染和跟踪，请遵循以下[最佳实践和防护](#best-practices)。

## 将完整/基本URL个性化 {#personalize-complete-base-url}

Journey Optimizer还支持个性化&#x200B;**整个** URL或URL的&#x200B;**基本域**，例如：

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>要启用完整或基本URL个性化，请与Adobe联系并提供您的接受域列表。 这是帮助防止不安全的重定向所必需的。

## 个性化URL跟踪参数 {#personalize-url-tracking-parameters}

[URL跟踪](url-tracking.md)在渠道配置级别进行管理，并应用于消息内容中包含的所有URL。 您还可以在Email Designer中为单个链接个性化URL跟踪参数。 这样，您可以将特定于收件人的参数附加到单个链接（例如，将标识符传递到网站分析工具）。

为此，请[插入链接](message-tracking.md#insert-links)，选择个性化图标，添加URL跟踪参数，并从[个性化编辑器](../personalization/personalization-build-expressions.md)中选择您选择的配置文件属性。

![](assets/message-tracking-perso-parameter.png)

对要将此跟踪参数添加到的每个链接重复上述步骤。

现在，在发送电子邮件时，此参数会自动附加到URL的末尾。 然后，您可以在网站分析工具或性能报表中捕获此参数。

>[!NOTE]
>
>要验证最终URL，您可以[发送校样](../content-management/proofs.md)，并在收到校样后单击电子邮件内容中的链接。 URL应显示跟踪参数。 例如：<https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## 最佳实践和防护 {#best-practices}

要使链接有效、可点击且可跟踪，请遵循以下最佳实践和防护。

### 动态URL的大括号 {#use-braces}

在插入包含个性化的URL时，请为URL的动态部分使用三个大括号(`{{{ ... }}}`)。 这可以防止转义更改特殊字符（例如`/`和`+`），并有助于避免URL损坏、重定向错误或跟踪问题。

示例如下：

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>使用原始输出(`{{{ ... }}}`)意味着按原样插入值。 请仅将其用于您信任且预计对URL安全的值（例如，您生成或验证上游的值）。

### 正确的URL跟踪 {#enable-url-tracking}

* 使用个性化生成URL时，请确保每个收件人的解析值以`http`/`https`开头。 否则，可能无法应用跟踪，并且链接可能无法按预期运行。

* 请勿在个性化编辑器的URL字段中直接使用动态逻辑，如`let`、`each`或`if`语句。 出于安全原因，已禁用这些功能。

* 如果您的场景涉及生成个性化URL的复杂逻辑，请避免将该逻辑直接放入个性化编辑器的URL字段中。 相反：
   * 在HTML内容中的URL字段上方或附近添加必要的逻辑和语句。
   * 单独生成和存储个性化属性，然后在电子邮件内容中引用它们。

### URL编码和长度 {#encoding}

* URI语法规则([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"})适用于电子邮件内容中的所有URL。 但是，个性化URL更有可能出现编码问题，因为收件人特定的值可能会引入保留字符（例如在查询参数中）。 因此，请确保您的动态值采用URL编码（尤其是空格、`&`、`#`、`%`和`+`），并避免使用`+`作为查询值。

* 浏览器、邮件客户端或下游系统可能会截断或拒绝过长的URL。 例如，在运行时个性化繁重时，镜像页面URL可能会显着增长。 使个性化负载保持小规模并避免将大型对象嵌入到URL中。

### 建议的验证步骤 {#validation}

在激活历程或营销策划之前，请遵循以下建议：

* 发送[验证](../content-management/proofs.md)并单击链接以确认解析的URL以`http`/`https`开头并保留预期结构。
* 如果附加了跟踪参数，请确认最终URL包含这些参数（通过配置级别的URL跟踪或每链接跟踪参数）。

