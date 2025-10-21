---
solution: Journey Optimizer
product: journey optimizer
title: 管理客户的首选项
description: 了解如何通过使用同意政策来管理用户的偏好设置
feature: Journeys, Privacy, Consent Management, Landing Pages
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 策略、治理、平台、同意、医疗保健防护
hide: true
hidefromtoc: true
source-git-commit: 0aa29a163e337359ea4455edee57bc49fd06a020
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 4%

---

# 管理客户的首选项 {#preference-center}

>[!AVAILABILITY]
>
>此功能当前仅适用于已购买Adobe **Healthcare Shield**&#x200B;或&#x200B;**Privacy and Security Shield**&#x200B;附加产品的组织。

在现代营销自动化生态系统中，品牌厂商通过各种接触点与客户互动，面临不相关或过度通信的风险，从而导致脱离、垃圾邮件投诉和合规风险。 因此，他们需要管理客户的偏好，以便获得对受众的实时洞察并提供个性化、尊重的沟通。

通过[!DNL Adobe Journey Optimizer]，通过使用[同意政策](consent.md)，您可以尊重客户的偏好<!-- in terms of **channels** and **topics**-->。 这可确保[!DNL Journey Optimizer]仅根据客户的选择<!-- their preferred channels and on the subscription topics-->定位客户，同时尊重他们的同意。

要使用[!DNL Journey Optimizer]管理用户的首选项，您可以：

* 检索客户是否同意选择加入/退出任何本机出站频道。 例如，在[!DNL Experience Platform]中创建同意策略以排除尚未同意接收给定渠道的通信的客户。 然后，使用电子邮件渠道配置在[!DNL Journey Optimizer]中应用此同意策略。 [了解如何操作](consent.md#surface-marketing-actions)

  >[!NOTE]
  >
  >支持的渠道包括电子邮件、推送、短信和应用程序内消息。<!--To check-->

* 询问您的客户他们愿意订阅哪些主题（例如他们同意接收或不同意接收的通信类型）。 [了解如何操作](#manage-preferences)

>[!IMPORTANT]
>
>同意优先于偏好设置。 例如，您的客户之一指出其首选渠道是电子邮件，并且同意接收新闻稿<!-- they are interested in yoga-->；但是，如果他们选择不接收来自您的任何通信，则您发送的电子邮件新闻稿无法定位他们<!-- on yoga-->。

## 记录和执行首选项 {#manage-preferences}

使用[!DNL Journey Optimizer]中的同意策略，您可以集中管理客户的首选项。 这样，您就可以确保仅根据客户选择的主题来定位客户，同时尊重他们的同意选择。 为此，请执行以下步骤。

假设您想通过历程和促销活动，根据客户在多个订阅主题（*新闻稿*、*优惠*&#x200B;和&#x200B;*新产品发布*）中的通信偏好设置来定位客户。

1. 在配置文件级别<!--how??-->使用布尔运算符定义首选项属性。 例如，您可以指定：

   * Newsletter_Email — 布尔值(True/False)
   * 选件 — 布尔值(True/False)
   * 新产品启动次数 — 布尔值(True/False)

   这些属性是在启用配置文件的[数据集](../data/get-started-datasets.md)的架构中捕获的，并映射到[统一客户配置文件](../audience/get-started-profiles.md)。

   >[!NOTE]
   >
   >客户同意和联系人偏好设置是复杂的主题。 要了解如何在[!DNL Experience Platform]中收集、处理和筛选同意和上下文首选项，建议您阅读以下文档：
   >
   >* 要了解收集同意数据所需的架构字段组，请参阅[此页面](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview){target="_blank"}。 它详细介绍了如何处理您从客户那里收集的同意数据，并将其集成到您存储的客户配置文件中。
   >* 要了解有关“同意和首选项”字段组的详细信息，请参阅[此页面](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents#ingest){target="_blank"}。
   >* 若要向架构添加自定义首选项字段，请按照[此部分](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/dataset#custom-consent){target="_blank"}中的步骤操作。

1. 创建一个页面以捕获客户的首选项。 使用以下任一方法：

   * 使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home){target="_blank"}创建网页以记录客户的首选项。

   * 使用包含表单的[!DNL Journey Optimizer] [登陆页面](../landing-pages/create-lp.md)通过配置文件数据捕获客户的首选项。  [了解有关表单的更多信息](../landing-pages/lp-forms.md) <!--Forms not released/announced yet - TBC-->

     >[!NOTE]
     >
     >确保使用的登陆页面的域属于上层品牌而不是子品牌。 这是为了确保最终用户之间的信任。<!--Please clarify-->

1. 在此页面上，客户可以通过选中或取消选中复选框来更新其偏好设置，例如基于主题的订阅。

   每个操作都会触发一个同意事件，该事件针对相应的配置文件属性（`True`表示选择加入，`False`表示选择退出）进行保存，方法是将数据摄取到启用配置文件的数据集架构<!-- that contains the corresponding preference fields-->。

   <!--Record your users' preferences through the web page or landing page that you created. The data is saved against the corresponding profile, meaning that the preference data is ingested into a Profile-enabled dataset whose schema contains consent/preference fields.-->

   例如，电子邮件地址为john.black@lumamail.com的用户同意接收优惠，但不希望接收新闻稿。

   相应的用户档案数据集已更新，如下所示：

   | 属性=电子邮件ID | 属性=选件 | 属性=新闻稿 |
   |---------|----------|---------|
   | john.black@lumamail.com | Y | N |

   >[!NOTE]
   >
   >传入的同意事件将输入到客户个人资料中，确保实时更新。 每个用户档案都会反映其最近跨订阅首选项所做的选择。

1. 在 Adobe Experience Platform 中，创建自定义策略（从&#x200B;**[!UICONTROL 隐私]** > **[!UICONTROL 策略]**&#x200B;菜单）。[了解如何操作](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=zh-Hans#create-policy){target="_blank"}

   >[!AVAILABILITY]
   >
   >同意策略当前仅适用于已购买Adobe **Healthcare Shield**&#x200B;或&#x200B;**Privacy and Security Shield**&#x200B;附加产品的组织。 [了解有关同意政策的更多信息](consent.md)

   要使用同意策略，配置文件数据中必须存在首选项属性。 这就是为什么您必须在用户档案级别定义这些属性（如步骤1中所述）。

1. 选择&#x200B;**[!UICONTROL 同意政策]**，按以下方式键入并配置条件。[了解如何配置同意政策](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=zh-Hans#consent-policy){target="_blank"}

<!--Consent policies are comprised of two logical components:

* **If**: The condition that will trigger the policy check, based on a certain marketing action (email, SMS, push, custom action, etc.) being performed, the presence of certain data usage labels, or a combination of the two.

* **Then**: The consent attribute must be present for a profile to be included in the action that triggered the policy. More than one field can also be selected.-->

    例如，要仅向未选择不接收电子邮件新闻稿的客户发送通信，请创建自定义策略并定义以下条件：
    
    *如果&#x200B;**[!UICONTROL 营销操作]**&#x200B;等于&#x200B;**[!UICONTROL 电子邮件]**
    
    *则&#x200B;**[!UICONTROL 新闻稿_电子邮件]**&#x200B;不存在&#x200B;**[!UICONTROL false]**&#x200B;或&#x200B;**[!UICONTROL 新闻稿_电子邮件]**&#x200B;不等于&#x200B;**[!UICONTROL false]**
    
    ！[&#128279;](assets/consent-policy-email-newsletter.png){width=100%}
    
    >[！TIP]
    >
    >启用配置文件的数据集必须包含配置文件属性&#x200B;**[!UICONTROL Newsletter_Email]**，其值设置为“true”（如步骤1中所述）

1. 创建同意策略后，在[!DNL Journey Optimizer]中使用[渠道配置](consent.md#surface-marketing-actions)或[历程自定义操作](consent.md#journey-custom-actions)来利用它。

1. 现在，您可以在历程和营销策划中使用这些渠道配置或自定义操作，以确保您的<!--targeted-->客户的偏好设置得到遵守。
