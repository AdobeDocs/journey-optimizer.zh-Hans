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
source-git-commit: f9fbf3d0dd49c98d3e4d88fc97ff26f44835769c
workflow-type: tm+mt
source-wordcount: '402'
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

<!--
## Best practices and guardrails {#best-practices}

To keep links valid, clickable, and trackable, follow the best practices and guardrails below.

### Braces for dynamic URLs {#use-braces}

When inserting a URL that contains personalization, use three curly braces (`{{{ ... }}}`) for the dynamic portion of the URL. This prevents escaping from altering special characters (for example `/` and `+`) and helps avoid broken URLs, incorrect redirects, or tracking issues.

Here is an example:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>Using raw output (`{{{ ... }}}`) means the value is inserted as-is. Only use it with values you trust and that are intended to be URL-safe (for example, values you generate or validate upstream).

### Correct URL tracking {#enable-url-tracking}

* When using personalization to generate the URL, ensure the resolved value starts with `http`/`https` for every recipient. Otherwise, tracking may not be applied and the link may not behave as expected.

* Do not use dynamic logic such as `let`, `each`, or `if` statements directly in the personalization editor's URL field. These are disabled for security reasons.

* If your scenario involves complex logic to generate personalized URLs, avoid placing that logic directly in the personalization editor's URL field. Instead:
    * Add the necessary logic and statements in the HTML content above or near the URL field.
    * Generate and store personalized attributes separately, then reference them in your email content.

### URL encoding and length {#encoding}

* URI syntax rules ([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) apply to all URLs in your email content. However, personalized URLs are more likely to surface encoding issues because recipient-specific values can introduce reserved characters (for example in query parameters). Therefore, ensure your dynamic values are URL-encoded (especially spaces, `&`, `#`, `%`, and `+`) and avoid using `+` for query values.

* Very long URLs can be truncated or rejected by browsers, mail clients, or downstream systems. For example, mirror page URLs can grow significantly when runtime personalization is heavy. Keep personalized payloads small and avoid embedding large objects into URLs.

### Recommended validation steps {#validation}

Before activating a journey or campaign, follow the recommendations below:

* Send a [proof](../content-management/proofs.md) and click links to confirm the resolved URL starts with `http`/`https` and keeps the expected structure.
* If tracking parameters are appended, confirm the final URL includes them (either via configuration-level URL tracking or per-link tracking parameters).
-->
