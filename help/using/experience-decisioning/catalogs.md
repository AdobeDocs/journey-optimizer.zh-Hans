---
title: Item catalog
description: Learn how to work with the item catalog
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Item catalog {#catalog}

In Decisioning, catalogs serve as central containers for organizing decision items. Each catalog is linked to an Adobe Experience Platform schema, encompassing all the attributes assignable to a decision item.

****

![](assets/catalogs-list.png)

To access the catalog&#39;s schema where decision items&#39; attributes are stored, follow these steps:

1. ********

1. The catalog&#39;s schema opens in a new tab, following the structure below:

   * **`_experience`**
   * **`_<imsOrg>`** By default, no custom attributes are configured, but you can add as many as needed to suit your requirements. Once done, custom attributes appear in the decision item creation screen alongside the standard attributes.

   ![](assets/catalogs-schema.png)

1. **`_<imsOrg>`**

   ![](assets/catalogs-add.png)

1. ****

   >[!CAUTION]
   >
   >For now, Decisioning exclusively supports the following data types: String, Integer, Boolean, Date, DateTime and Decisioning Asset. Any field falling outside these data types will not be available for use when authoring a decision item or a catalog.

   The value that is input on an attribute with decisioning asset attribute is a public url. Most of the time this would point to an image.

   [](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=zh-Hans)

1. Once your desired custom attributes are added, save the schema. ****
