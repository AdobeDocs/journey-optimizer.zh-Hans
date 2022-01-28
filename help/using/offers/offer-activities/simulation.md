---
title: 创建模拟
description: 了解如何创建模拟
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 39b52f39ec19c185d2cd95634a60e37f62a66f83
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

---

# 创建模拟

## 关于模拟

要验证决策逻辑，您可以模拟哪些选件将交付到给定版面的测试用户档案。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

这样，您就可以测试和优化各种版本的选件，而不会对目标收件人产生任何影响。

>[!NOTE]
>
>此功能模拟对 [!DNL Decisions] API。 了解详情 [使用决策API提供优惠](../api-reference/decisions-api/deliver-offers.md).

要访问此功能，请选择 **[!UICONTROL Simulation]** 选项卡 **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** 菜单。

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## 选择测试用户档案

首先，您需要选择要用于模拟的测试用户档案。

1. 单击 **[!UICONTROL Manage profile]**。

   ![](../../assets/offers_simulation-manage-profile.png)

1. 选择要用于标识测试用户档案的身份命名空间。 在本例中，我们将使用 **电子邮件** 命名空间。

   >[!NOTE]
   >
   >标识命名空间定义标识符的上下文，如电子邮件地址或CRM ID。 进一步了解Adobe Experience Platform身份命名空间 [在此部分中](../../get-started-identity.md){target=&quot;_blank&quot;}。

1. 输入标识值并单击 **[!UICONTROL View]** 列出可用的用户档案。

   ![](../../assets/offers_simulation-add-profile.png)

1. 如果要测试不同的用户档案数据，请添加其他用户档案，并保存您的选择。

   ![](../../assets/offers_simulation-save-profiles.png)

1. 添加后，所有用户档案都会列在 **[!UICONTROL Test profile]**. 您可以在保存的测试用户档案之间切换，以显示每个选定用户档案的结果。

   ![](../../assets/offers_simulation-saved-profiles.png)

1. 您可以单击 **[!UICONTROL Profile details]** 链接以显示所选的用户档案数据。

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## 添加决策作用域

现在，选择要在测试用户档案上模拟的选件决策。

1. 选择 **[!UICONTROL Add decision scope]**。

   ![](../../assets/offers_simulation-add-decision.png)

1. 从列表中选择版面。

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. 将显示可用的决策。

   * 您可以使用搜索字段来优化选择。
   * 您可以单击 **[!UICONTROL Open offer decisions]** 链接以打开您创建的所有决策的列表。 了解详情 [决策](create-offer-activities.md).

   选择您选择的决策并单击 **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. 您刚刚定义的决策范围将显示在主工作区中。

   您可以调整要请求的选件数量。 例如，如果您选择2，则此决策范围将显示2个最佳选件。

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >您最多可以请求30个选件。

1. 重复上述步骤，以根据需要添加任意数量的决策。

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >即使您定义多个决策范围，也只会模拟一个API请求。
   >
   >默认情况下，会启用所有重复数据删除标记以进行模拟，这意味着决策引擎允许重复项，因此可以在多个决策/投放中提出相同的建议。 了解 [!DNL Decisions] 中的API请求属性 [此部分](../api-reference/decisions-api/deliver-offers.md).<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## 查看模拟结果 {#simulation-results}

添加决策范围并选择测试用户档案后，即可查看结果。

1. 单击 **[!UICONTROL View results]**。

   ![](../../assets/offers_simulation-view-results.png)

1. 将根据为每个决策选择的用户档案显示最佳的可用选件。

   选择选件以显示其详细信息。

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. 从列表中选择其他用户档案以显示其他测试用户档案的选件决策结果。

1. 您可以根据需要多次添加、删除或更新决策范围。

>[!NOTE]
>
>每次更改用户档案或更新决策范围时，您都需要使用 **[!UICONTROL View results]** 按钮。

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

