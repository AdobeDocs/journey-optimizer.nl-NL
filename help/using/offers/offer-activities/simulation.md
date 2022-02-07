---
title: Simulaties maken
description: Leer hoe u simulaties maakt
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# Simulaties maken {#create-simulations}

## Informatie over simulatie

Om uw beslissingslogica te bevestigen, kunt u simuleren welke aanbiedingen aan een testprofiel voor een bepaalde plaatsing zullen worden geleverd.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Hierdoor kunt u verschillende versies van uw aanbiedingen testen en verfijnen, zonder dat dit gevolgen heeft voor de beoogde ontvangers.

>[!NOTE]
>
>Deze mogelijkheid simuleert één verzoek aan de [!DNL Decisions] API. Meer informatie over [Aanbiedingen leveren met behulp van de Besluiten-API](../api-reference/decisions-api/deliver-offers.md).

Als u deze functie wilt openen, selecteert u de optie **[!UICONTROL Simulation]** van de **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** -menu.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Testprofielen selecteren

Eerst moet u de testprofielen selecteren die u voor simulatie gaat gebruiken.

1. Klik op **[!UICONTROL Manage profile]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Selecteer de naamruimte voor de identiteit die u wilt gebruiken om testprofielen te identificeren. In dit voorbeeld gebruiken we de **E-mail** naamruimte.

   >[!NOTE]
   >
   >Een naamruimte voor identiteiten definieert de context van een id, zoals een e-mailadres of CRM-id. Meer informatie over naamruimten in Adobe Experience Platform [in deze sectie](../../start/get-started-identity.md){target=&quot;_blank&quot;}.

1. Voer de identiteitswaarde in en klik op **[!UICONTROL View]** om de beschikbare profielen weer te geven.

   ![](../../assets/offers_simulation-add-profile.png)

1. Voeg andere profielen toe als u andere profielgegevens wilt testen en sla uw selectie op.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Na toevoeging worden alle profielen vermeld in de vervolgkeuzelijst onder **[!UICONTROL Test profile]**. U kunt schakelen tussen de opgeslagen testprofielen om de resultaten voor elk geselecteerd profiel weer te geven.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. U kunt op de knop **[!UICONTROL Profile details]** koppeling gebruiken om de geselecteerde profielgegevens weer te geven.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## Beslissingsbereik toevoegen

Selecteer nu de aanbiedingsbesluiten die u op uw testprofielen wilt simuleren.

1. Selecteer **[!UICONTROL Add decision scope]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Selecteer een plaatsing in de lijst.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. De beschikbare beslissingen worden weergegeven.

   * U kunt het zoekveld gebruiken om de selectie te verfijnen.
   * U kunt op de knop **[!UICONTROL Open offer decisions]** Hiermee opent u de lijst met alle beslissingen die u hebt gemaakt. Meer informatie over [besluiten](create-offer-activities.md).

   Selecteer de gewenste beslissing en klik op **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. Het beslissingsbereik dat u zojuist hebt gedefinieerd, wordt weergegeven in de hoofdwerkruimte.

   U kunt het aantal voorstellen aanpassen dat u wilt verzoeken. Als u bijvoorbeeld 2 selecteert, worden de beste 2 aanbiedingen weergegeven voor dit beslissingsbereik.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Je kunt maximaal 30 voorstellen aanvragen.

1. Herhaal bovenstaande stappen om zoveel beslissingen toe te voegen als u nodig hebt.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Zelfs als u verschillende beslissingsbereiken definieert, wordt slechts één API-aanvraag gesimuleerd.
   >
   >Door gebrek, worden alle vlaggen van de Deduplicatie toegelaten voor simulatie, zo betekent het dat de besluitvormingsmotor duplicaten toestaat en zo de zelfde voorstelling over veelvoudige besluiten/plaatsen kan maken. Meer informatie over de [!DNL Decisions] Eigenschappen voor API-aanvragen in [deze sectie](../api-reference/decisions-api/deliver-offers.md).<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

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

## Simulatieresultaten weergeven {#simulation-results}

Nadat u een beslissingsbereik hebt toegevoegd en een testprofiel hebt geselecteerd, kunt u de resultaten bekijken.

1. Klik op **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. De beste beschikbare aanbiedingen worden weergegeven volgens het geselecteerde profiel voor elke beslissing.

   Selecteer een voorstel om de details ervan weer te geven.

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. Selecteer een ander profiel in de lijst om de resultaten van de biedingsbesluiten voor een ander testprofiel weer te geven.

1. U kunt het beslissingsbereik zo vaak als nodig toevoegen, verwijderen of bijwerken.

>[!NOTE]
>
>Elke keer dat u profielen wijzigt of beslissingsbereik bijwerkt, moet u de resultaten vernieuwen met de opdracht **[!UICONTROL View results]** knop.

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

