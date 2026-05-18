---
solution: Journey Optimizer
product: journey optimizer
title: 在电子邮件和短信消息中使用和配置深层链接
description: 了解如何向电子邮件和短信内容添加深层链接，以及如何在iOS和Android应用程序中实施深层链接处理。
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 深层链接，深层链接，通用链接，应用程序链接，电子邮件，短信
source-git-commit: d189ba524cdccaf0a220608680425d0a275c3ed9
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 1%

---


# 在电子邮件和短信中使用和配置深层链接 {#deeplinks}

深层链接可帮助您将电子邮件或短信消息的收件人引导至移动应用程序中的特定屏幕或内容片段。 它有助于将用户直接引导至所需的应用程序内体验，而无需通过Web浏览器或应用商店路由他们，因此该历程始终相关且符合品牌要求。

当您的收件人单击深层链接时，他们会直接转到所需的应用程序内内容 — **前提是您已完成**：

* Journey Optimizer中的[配置步骤](#configuration)；

* iOS和Android在移动应用程序中的[移动应用程序实施](#mobile-implementation)步骤。

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer]支持使用跟踪的URL (`/ee/v1/mclick/*`)对iOS和Android进行深层链接，以确保兼容性和点击跟踪。

## 创作深层链接 {#authoring}

### 电子邮件 {#authoring-email}

对于电子邮件，有两个选项可插入深层链接：

* **向Designer发送电子邮件**：确保启用[链接跟踪](message-tracking.md#enable-tracking)。 选择要链接的元素（文本、按钮或图像），在上下文工具栏中单击&#x200B;**[!UICONTROL 插入链接]**，然后选择&#x200B;**[!UICONTROL 深层链接]**&#x200B;以输入深层链接URL。 [了解有关插入链接的更多信息](message-tracking.md#insert-links)

* **Personalization编辑器（代码）**：使用以下代码片段将深层链接直接插入HTML：

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  将`<<deeplink_url>>`替换为实际的深层链接URL，并为每个块使用唯一的`id`以避免冲突。

### 短信 {#authoring-sms}

对于短信，深层链接是使用个性化编辑器中的&#x200B;**Url**&#x200B;帮助程序功能创作的。 在[本节](../sms/create-sms.md#sms-content)中了解更多有关添加指向短信内容的链接的信息。

要在短信内容中插入深层链接，请使用以下语法：

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

将`<<url>>`替换为您的实际深层链接URL。

## Journey Optimizer中的配置 {#configuration}

要在移动应用程序的电子邮件和短信中使用深层链接，请完成以下配置步骤。

>[!NOTE]
>
>此部分适用于您使用&#x200B;**通用链接(iOS)**&#x200B;和&#x200B;**应用程序链接(Android)**（基于HTTPS的深层链接）的情况。

1. 在Journey Optimizer中，委派启用了深层链接的子域。 [了解详情](../configuration/delegate-subdomain.md)

1. 在您的子域中托管iOS的AASA文件和Android的assetLinks.json文件。 请联系[Adobe客户关怀](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"}或您的Adobe代表，并提供以下详细信息：

   * 对于iOS (AASA)**&#x200B;**：
      * 已委派的子域
      * 应用程序捆绑包ID
   * 对于Android (assetLinks.json)**&#x200B;**：
      * 已委派的子域
      * 应用程序捆绑包ID
      * SHA-256证书指纹

>[!IMPORTANT]
>
>当为消息启用链接跟踪时 — 在[电子邮件跟踪设置](message-tracking.md#enable-tracking)中或在短信营销活动的&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分中 — 通过Adobe基础架构进行深层链接适用。 跟踪的深层链接点击使用`/ee/v1/mclick/*`下的URL，Adobe会托管这些URL并对其进行解析。
>
>对于&#x200B;**非跟踪**&#x200B;链接，不会通过Adobe系统重写URL。 您必须在自己的域和托管上配置通用链接或应用程序链接，以便这些链接能够按预期打开您的应用程序。

## 移动应用程序实施 {#mobile-implementation}

本节介绍如何使用[!DNL Adobe Journey Optimizer]实施移动深层链接，以便在典型的&#x200B;**HTTPS**&#x200B;设置中（通用链接和应用程序链接），单个URL可以：

* 安装移动应用程序后，在移动应用程序中打开一个特定的屏幕，或者
* 在未安装应用程序时作为回退打开您的网站。

为您的消息启用链接跟踪后，[!DNL Journey Optimizer]将继续跟踪这些点击，将它们包含在报表中，并且如果您对消息运行它们，则可以在[内容实验](../content-management/content-experiment.md)中使用它们。

本节提供了深层链接的常见实施模式。 确切的设置取决于您的应用程序架构和路由框架。

### iOS（通用链接） {#ios-implementation}

1. 在Xcode中，通过&#x200B;**[!UICONTROL 签名和功能]** > **[!UICONTROL +功能]** > **[!UICONTROL 关联的域]**&#x200B;选择您的目标。
1. 为委派的子域添加条目，例如：

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. 在应用程序中处理通用链接，并从响应标头中获取原始链接。

   +++ 示例：包含场景的iOS 13+

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>应用必须在`mclick` URL上执行&#x200B;**GET**&#x200B;并读取&#x200B;**`Location`**&#x200B;标头，然后基于&#x200B;**最终** URL进行路由。
>
>不要只是在Safari中打开`mclick` URL；这会破坏深层链接的目的。

### Android（应用程序链接） {#android-implementation}

1. 在您的Android应用程序中添加应用程序链接意图筛选器。

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. 实施深层链接处理程序。

   +++ 在Kotlin：

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>与iOS一样，应用程序必须调用`mclick` URL并使用&#x200B;**`Location`**&#x200B;标头确定最终目标。
>
>使用`followRedirects(false)`，以便您控制重定向处理并根据需要准确记录分析。
>
>路由逻辑特定于应用程序；定义从URL到屏幕的清晰映射。

## 建议的做法 {#deeplink-best-practices}

* **使用稳定路径**：首选对应用程序UI更改具有弹性的路由（例如`/account/orders`而不是`/tab/3/view/2`）。
* **考虑跟踪的路径**：启用链接跟踪时，点击的链接可能使用跟踪的路径模式（例如`/ee/v1/mclick/`）。 确保您的路由器在解析跟踪链接后可以解析最终URL。
* **保持参数可预测**：定义一致的参数方案（例如`?orderId=12345`）。
* **避免URL中的敏感数据**：不要将机密或个人数据直接放入深层链接URL中。
* **测试您的深层链接**：发送校样并单击已安装应用程序的设备上的深层链接。
* **在真实设备上验证**：在物理设备上验证通用链接和跟踪链接解析行为比在模拟器中验证更可靠。
* **验证应用端路由**：如果深层链接未打开预期的屏幕，则验证应用端路由和URL格式（主机/路径/查询和URL编码）。
* **请牢记应用初始化**：应用链接/通用链接行为在安装并打开应用至少一次后最为可靠。

## 疑难解答和常见问题 {#troubleshooting-faq}

+++ 我点按深层链接时，应用程序未打开。

* 验证URL是否与注册应用程序以处理的主机模式和路径模式匹配，包括在启用链接跟踪时跟踪的点击路径（例如`/ee/v1/mclick/`下的路径）。
* 对于iOS通用链接和Android应用程序链接，请确认域关联(AASA / `assetlinks.json`)已正确配置且可访问。
* 在真实设备上测试（模拟器/仿真器可能会因链路关联而表现出不同的行为）。

+++

+++ 应用程序将打开，但未导航到预期的屏幕。

* 确认应用端路由器正确解析URL路径/查询。
* 检查URL编码：保留字符应该使用URL编码。
* 验证参数名称和值是否与路由器的预期相符。

+++

+++ 如果未安装应用程序，会发生什么情况？

* 如果您的网站可以提供相同的HTTPS URL，则当未安装应用程序时，该链接会打开网页作为回退措施（相应地配置Web目标和路由）。

+++

+++ 如何在参数中安全地包含特殊字符？

URL编码查询参数值。 这减少了交付和渲染问题，并有助于防止应用程序中出现解析错误。

+++

+++ 我们应如何测试端到端？

* 使用深层链接创建验证，在iOS和Android设备（已安装或未安装方案）上单击它。
* 验证：
   * 最终电子邮件或短信链接值（主机/路径/查询）
   * 操作系统级别的关联（如果使用通用链接/应用程序链接）
   * 应用程序内路由结果

+++

+++ 我有一个应用程序，但组织的子域不同。 我是否应该请求为每个子域创建AASA和assetLinks.json？

可以。 如果您希望对每个委派的子域进行深层链接，请为应支持该功能的每个子域请求AASA和`assetlinks.json`配置。

+++

+++ 我配置的URL是否应使用深层链接格式（例如`appname://path`）？

您可以使用自定义URL方案（例如`appname://path`），但推荐的方法是通用链接或应用程序链接(`https://`)，它与此页上的配置和实施部分中基于HTTPS的设置相匹配。

+++

+++ URL上的UTM参数是否会在用于分析的移动设备应用程序中可用？

可以。 当您的应用程序对`mclick` URL执行GET时，在[!DNL Journey Optimizer]中配置的UTM参数将包含在`Location`标头中返回的最终URL中，以便您将其用于应用程序内分析。

+++

+++ `/ee/v1/click/` URL的用户体验是什么？

该链接在设备的默认Web浏览器中打开（标准点击跟踪行为），而不是通过本页面上描述的`mclick`流程作为应用程序深层链接处理。

+++
