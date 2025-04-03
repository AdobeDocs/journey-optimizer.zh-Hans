---
title: 测试基于代码的体验
description: 了解如何在Journey Optimizer中测试基于代码的体验
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 9a1c148c-a6c3-406b-8f2e-1cf8b8239e75
source-git-commit: effc706cfa56eca21cde0f26fe7b6332d3728b74
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 24%

---

# 测试基于代码的体验 {#test-code-based}

## 预览基于代码的体验 {#preview-code-based}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="预览基于代码的体验"
>abstract="模拟基于代码的体验将看起来是什么样。"

要显示已修改的基于代码的体验的预览，请执行以下步骤。

>[!CAUTION]
>
>您必须具有可用的测试用户档案，以模拟将向他们投放哪些优惠。 了解如何[创建测试配置文件](../audience/creating-test-profiles.md)。

1. 在历程或营销策划中，从个性化编辑器或编辑内容屏幕中选择&#x200B;**[!UICONTROL 模拟内容]**。

   ![](assets/code-based-campaign-simulate.png)

1. 单击&#x200B;**[!UICONTROL 管理测试配置文件]**&#x200B;以选择一个或多个测试配置文件。

1. 此时将显示已修改的基于代码的体验预览。

有关如何选择测试用户档案和预览内容的详细信息，请参阅[此部分](../content-management/preview.md)。

>[!NOTE]
>
>目前，无法使用[Decisioning](../experience-decisioning/gs-experience-decisioning.md)从基于代码的体验营销活动或历程的用户界面模拟内容。 [此部分](../experience-decisioning/create-decision.md#test-and-publish)中提供了解决方法。


## 在设备上预览 {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="在真实设备上预览基于代码的体验"
>abstract="在您的浏览器或移动设备上预览您的个性化体验，看看它们在真实设备上的显示效果。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="在设备上预览基于代码的 Web 体验"
>abstract="扫描二维码或复制链接以在设备上预览。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="在移动设备上预览基于代码的体验"
>abstract="扫描二维码或复制链接以在设备上预览。连接后，在设备上输入 PIN 码。每次更新预览链接时，您可能需要重新启动应用程序才能看到更改。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="刷新预览链接以反映当前视图"
>abstract="设备上的预览将显示您创建或刷新预览链接时的内容。如果您修改了内容或选择了不同的测试轮廓或处理，请刷新预览以使其反映当前视图。"

为网页或移动应用程序构建基于代码的体验时，您可以直接在浏览器或移动设备上预览个性化体验，以了解这些体验在实际设备上的外观。

>[!WARNING]
>
>使用[决策策略](../experience-decisioning/create-decision.md)或[个性化](../personalization/personalization-build-expressions.md)上下文属性时，设备上预览不可用。

1. 在&#x200B;**[!UICONTROL 模拟]**&#x200B;屏幕中，单击&#x200B;**[!UICONTROL 打开预览选项]**&#x200B;按钮。 预览选项取决于[基于代码的配置](code-based-configuration.md#create-code-based-configuration)中选择的平台。

1. 如果您在基于代码的配置中使用[Web平台](code-based-configuration.md#web)，则会使用为当前渠道配置输入的URL预填充&#x200B;**[!UICONTROL 设备预览URL]**&#x200B;只读字段。

   ![](assets/preview-on-device-web.png)

   您可以：

   * 选择&#x200B;**[!UICONTROL 复制链接]**&#x200B;按钮并将链接粘贴到浏览器选项卡中。 您还可以与团队和利益相关者共享链接，利益相关者可以在更改生效之前在任何浏览器中预览新体验。

   * 单击&#x200B;**[!UICONTROL 在新标签页中打开]**&#x200B;以在当前浏览器中打开链接。

   * 使用移动设备扫描二维码以在移动设备浏览器中打开预览链接。

1. 如果您在基于代码的配置中使用[Mobile Platforms](code-based-configuration.md#mobile) (iOS / Android)，则&#x200B;**[!UICONTROL Deeplink]**&#x200B;只读字段会使用在所选平台的渠道配置中输入的&#x200B;**[!UICONTROL 预览URL]**&#x200B;值预填充。

   在&#x200B;**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!DNL Android]**&#x200B;选项卡之间切换以预览您所选平台的体验。

   ![](assets/preview-on-device-mobile.png)

   您可以：

   * 选择&#x200B;**[!UICONTROL 复制链接]**&#x200B;按钮并与您的团队和利益相关者共享该链接，这些利益相关者可以在更改生效之前在任何移动设备浏览器中预览新体验。

   * 使用移动设备扫描二维码以直接在移动设备应用程序中打开预览链接。 您必须在设备上输入PIN才能建立[Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"}会话。

     >[!NOTE]
     >
     >**Adobe Experience Platform Assurance**&#x200B;是Adobe Experience Cloud的一个产品，可帮助您检查、校对、模拟和验证在移动应用程序中收集数据或提供体验的方式。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/home){target="_blank"}

1. 如果您在基于代码的配置中使用任何[其他平台](code-based-configuration.md#other)，请从下拉列表中选择要预览的[表面URI](code-based-surface.md#surface-uri)。

   ![](assets/preview-on-device-other.png)

   * 选择&#x200B;**[!UICONTROL 复制链接]**&#x200B;按钮以将链接粘贴到浏览器选项卡中，或与您的团队和利益相关者共享该链接。

   * 如果您在配置中添加了多个URI（最多10个），则可以选择任意一个URI进行预览。

1. 为选定的测试配置文件生成预览链接，如果您在历程或营销活动中使用[内容试验](../content-management/content-experiment.md)，则为选定的处理生成预览链接。

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   更新内容或选择其他测试用户档案或治疗时，预览链接会自动刷新。 您可以将链接复制到不同的浏览器选项卡中，并比较体验。
