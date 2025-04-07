---
solution: Journey Optimizer
product: journey optimizer
title: 排除项列表
description: 了解有关发送期间发生排除的更多信息
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 排除原因 {#exclusion-list}

| 排除原因 | 错误代码 | 渠道 | 说明 |
|-|-|-|-|
| RuntimeDispatchError | 050301 | 所有渠道 | 任何运行时调度错误的通用排除事件。 |
| RuntimeRenderingError | 050302 | 所有渠道 | 任何运行时渲染错误的通用排除事件。 |
| NamespaceErrorForExperimentation | 050017 | 所有渠道 | 当试验中的命名空间与配置文件的命名空间不同时，会生成排除事件。 |
| ExperimentationHoldoutExclusion | 050018 | 所有渠道 | 当试验的合格处理为“维持”时，将生成此排除事件。 |
| ExcludedForControlRules | 050002 | 所有渠道 | 当投放当前消息导致违反控制规则（例如，一个月内允许的电子邮件数量）时，生成此排除事件。 |
| DirectMailNoVariantDefined | 050062 | 直邮 | 未定义直邮变体时，会生成排除事件。 |
| DirectMailNoMessageFoundForTreatment | 050061 | 直邮 | 为消息启用试验且未找到符合条件的处理消息时，会生成排除事件。 |
| EmailNoConsent | 050101 | 电子邮件 | 当用户选择不接收营销电子邮件时，会生成排除事件。 |
| 已禁止 | 050107 | 电子邮件 | 由于某个禁止显示原因而排除。 |
| 电子邮件已禁止 | 050102 | 电子邮件 | 禁止显示目标电子邮件时会生成排除事件。 |
| 域已禁止 | 050105 | 电子邮件 | 当目标电子邮件的域被禁止时，会生成排除事件。 |
| 不允许 | 050108 | 电子邮件 | 启用允许列表并将目标电子邮件从允许列表中排除时，会生成排除事件。 |
| EmailNotAllowed | 050103 | 电子邮件 | 启用允许列表并将目标电子邮件从允许列表中排除时，会生成排除事件。 |
| DomainNotAllowed | 050106 | 电子邮件 | 启用允许列表并将目标电子邮件的域从允许列表中排除时，会生成排除事件。 |
| EmailNoSubscriberIdFoundInProfile | 050025 | 电子邮件 | 在订阅电子邮件的配置文件中找不到subscriberId时，会生成排除事件。 |
| EmailNoAddressFoundInProfile | 050020 | 电子邮件 | 在执行地址中找不到电子邮件地址时，会生成排除事件。 |
| EmailNoAddressDefinedInPreset | 050021 | 电子邮件 | 如果未在配置中定义执行地址，则会生成排除事件。 |
| EmailNoVariantDefined | 050026 | 电子邮件 | 当电子邮件中未定义变体时，会生成排除事件。 |
| EmailNoMessageFoundForTreatment | 050027 | 电子邮件 | 为消息启用试验且未找到符合条件的处理消息时，会生成排除事件。 |
| EmailFormatAddress | 050024 | 电子邮件 | 当电子邮件包含格式错误的地址时，会生成排除事件。 |
| InAppNoVariantDefined | 050041 | 应用程序内 | 如果没有为InApp消息定义变体，则会生成排除事件。 |
| InAppNoMessageFoundForTreatment | 050042 | 应用程序内 | 为消息启用试验且未找到符合条件的处理消息时，会生成排除事件。 |
| PushNoTokenFoundInProfile | 050030 | 推送 | 当配置文件没有推送令牌时，会生成排除事件。 |
| PushNoValidTokenFoundForApps | 050031 | 推送 | 当在配置中未找到目标应用程序的有效令牌时，会生成排除事件。 |
| PushFormatProfile | 050034 | 推送 | 当配置文件中的pushNotificationDetails格式不正确时，会生成排除事件。 |
| PushNoConsent | 050111 | 推送 | 当用户选择退出营销推送通知时，将生成排除事件。 |
| PushNoApplicationDefinedInPreset | 050033 | 推送 | 当配置不包含任何要定位的应用程序时，会生成排除事件。 |
| PushNoVariantDefined | 050035 | 推送 | 未定义变体时，会生成排除事件。 |
| PushNoMessageFoundForTreatment | 050036 | 推送 | 为消息启用试验且未找到符合条件的处理消息时，会生成排除事件。 |
| SMSNoConsent | 050104 | 短信 | 当用户选择退出营销短信时，会生成排除事件。 |
| SMSFromNumberNotDefinedInPreset | 050152 | 短信 | 配置中未定义“FromNumber”时，将生成排除事件。 |
| SMSNoToNumberDefinedInProfile | 050153 | 短信 | 配置中未定义“ToNumber”时，将生成排除事件。 |
| SMSNoVariantDefined | 050154 | 短信 | 未定义变体时，会生成排除事件。 |
| SMSNoMessageFoundForTreatment | 050155 | 短信 | 为消息启用试验且未找到符合条件的处理消息时，会生成排除事件。 |
| WebNoVariantDefined | 050041 | Web | 如果没有为Web消息定义变体，则会生成排除事件。 |
| WebNoMessageFoundForTreatment | 050042 | Web | 为消息启用试验且未找到符合条件的处理消息时，会生成排除事件。 |
