---
title: 使用Adobe Stock图像
description: 开始使用Adobe Stock
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 0715f65f-04bd-4dc2-a152-98111f4c42e6
source-git-commit: fb56b69a74aa8c727bf75f1c7988ece845f43b5f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 1%

---

# 使用 [!DNL Adobe Stock] 图像 {#stock}

## 开始使用 [!DNL Adobe Stock] {#get-started-stock}

的 [!DNL Adobe Stock] 和 [!DNL Adobe Journey Optimizer] Email Designer集成插件为客户提供了一种导航、许可和保存图像以用于消息创作的简便方法。

[Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target=&quot;_blank&quot;}提供对数百万张高品质、精选且免版税的照片、视频、插图和矢量图形的访问。 您可以选择购买信用包以授权资产，或仅为所需资产购买一个Standard或Extended许可证。 Adobe Stock还提供免费的资产集合。

使用 [!DNL Adobe Journey Optimizer]，则您可以从 [!DNL Adobe Stock] ，然后将其添加到您的Assets文件夹中。 的 **[!UICONTROL Find Similar Image]** 选项可帮助您查找与投放中所用资产的内容、颜色和组成相匹配的图像。

## 权限{#stock-permissions}

的 **[!UICONTROL Find Adobe Stock photos]** 具有AEM Assets Essentials产品配置文件访问权限的用户可以使用选项。

有关更多信息，请参阅 [资产基本文档](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-users-to-essentials){target=&quot;_blank&quot;}。

## 插入图像 [!DNL Adobe Stock] {#add-stock-image}

从添加图像 [!DNL Adobe Stock] 对于您的内容，请执行以下步骤：

1. 从 **[!UICONTROL Content components]** ，拖放 **图像**.

1. 单击 **[!UICONTROL Find Adobe Stock photos]** 按钮。

   ![](assets/stock-find-photos.png)

1. 浏览库或在搜索字段中输入术语。

   ![](assets/stock-select-from-lib.png)

1. 选择所选图像并单击 **[!UICONTROL Save]**.

   如果您选择的图像未获得许可，则必须 [获得许可证](#license-stock-image).


## 从获取许可证 [!DNL Adobe Stock] {#license-stock-image}

如果您的图像已获得许可，则会由 ![](assets/stock_10.png) 图标。 如果没有，您必须获得许可。

要授权并下载您的图像，请执行以下步骤：

1. 选择它并单击 **[!UICONTROL License Adobe Stock image]** 图标。

   ![](assets/stock-license-icon.png)

   然后，系统会将您重定向到 [!DNL Adobe Stock] 网站，但许可证。

   ![](assets/stock-license-photo.png)

1. 从 [!DNL Adobe Stock] 网站，您需要购买资产才能下载图像并删除水印。

   此购买取决于您的Adobe Stock计划或订阅。 请注意，如果您有多个Adobe Stock帐户，则会被重定向到上次使用的股票ID。 在这种情况下，请确保您在获得资产许可之前已登录到正确的帐户。

   有关Adobe Stock计划和价格的更多信息，请参阅 [Adobe Stock文档](https://stock.adobe.com/plans){target=&quot;_blank&quot;}。

   >[!WARNING]
   > 如果发送了包含未授权图像的电子邮件，则图像会保留其未授权的表单，并带有水印。

1. 完成购买后，您现在可以返回至 [!DNL Adobe Journey Optimizer] 选择 **[!UICONTROL Import stock image]** 将授权图像导入资产。

   ![](assets/stock_6.png)

1. 选择存储资产的文件夹。 有关 [!DNL Assets Essentials]，请参见 [页面](assets-essentials.md#get-started-assets-essentials).

## 查找类似照片 {#similar-stock-image}

您可以通过 [!DNL Adobe Stock]. 请注意，此选项适用于所有图像：Assets文件夹中的Stock图像和图像获得许可/未获得许可。

要浏览类似照片，请执行以下步骤：

1. 选择要替换的图像。
1. 单击 **[!UICONTROL Find similar Stock photos]** 按钮在中显示资产 [!DNL Adobe Stock] 与图像的内容、颜色和构成匹配。

   ![](assets/stock-similar.png)

1. 选择所选图像并单击 **[!UICONTROL Save]**.

   ![](assets/stock-similar-results.png)

   如果您选择的图像未获得许可，则必须 [获得许可证](#license-stock-image).

1. 根据需要，使用 **[!UICONTROL Components settings]** 菜单。 [了解有关组件设置的更多信息](content-components.md)

创建并个性化消息后，您可以将其发布以供执行。 [了解详情](../messages/publish-manage-message.md)


### 相关主题{#stock-related-topics}

* [Journey Optimizer中的电子邮件设计](design-emails.md)
* [电子邮件设计的组件设置](content-components.md)
* [Adobe Stock快速入门](https://helpx.adobe.com/stock/get-started.html){target=&quot;_blank&quot;}。

