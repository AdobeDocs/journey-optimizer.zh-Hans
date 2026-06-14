---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 受众
description: 了解如何使用 Adobe Experience Platform 受众
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a51edc00631334874d111d8350ee7b0eb8e81aa5
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 9%

---

# 自定义上载 {#custom-upload}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用Adobe Experience Platform受众门户从CSV文件导入受众，并将其标识属性映射到客户配置文件。

>[!ENDSHADEBOX]

Adobe Experience Platform受众门户允许您使用CSV文件导入受众。

在自定义上传过程中，指定要用作身份的CSV属性及其映射到的配置文件身份。 这会在受众数据和用户档案之间建立链接。 如果CSV文件包含未在配置文件中找到的标识值，则会使用该标识值创建新配置文件。

>[!NOTE]
>
>对于自定义上传受众，如果在定期历程中启用了“增量读取”，则仅在第一次定期时检索用户档案，因为这些受众已修复。

![](assets/import-audience.png)

有关如何导入受众的详细信息，请参阅Adobe Experience Platform [分段服务文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}。

了解如何在视频中以CSV格式上传受众：

>[!VIDEO](https://video.tv.adobe.com/v/3423354?captions=chi_hans&quality=12)
