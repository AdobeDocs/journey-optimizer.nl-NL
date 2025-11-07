---
title: Testprofielen selecteren
description: Leer hoe u testprofielen selecteert om inhoud voor te vertonen en te testen.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 95a6d032808bc735a27a98dcb61efefa93cf5047
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---

# Testprofielen selecteren {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Gebruik testprofielen om uw inhoud te controleren"
>abstract="Gebruik testprofielen om de inhoud voor te vertonen en te testen. Als u persoonlijke velden hebt toegevoegd, kunt u controleren hoe deze worden weergegeven met de gegevens van het testprofiel."

Testprofielen zijn aanvullende ontvangers die niet voldoen aan de gedefinieerde doelcriteria. [ Leer hoe te om testprofielen tot stand te brengen ](../audience/creating-test-profiles.md)

Voordat u testprofielen gebruikt om uw inhoud te testen, moet u deze eerst selecteren. Ga als volgt te werk om dit te doen:

1. Klik in het scherm Inhoud bewerken van uw bericht of in de Designer-e-mail op de knop **[!UICONTROL Simulate content]** en selecteer **[!UICONTROL Simulate content]** .

1. Klik op de knop **[!UICONTROL Manage test profiles]** en selecteer de naamruimte die u wilt gebruiken om testprofielen te identificeren door op het selectiepictogram **[!UICONTROL Identity namespace]** te klikken. [ Leer meer over de identiteitsnamespaces van Adobe Experience Platform ](../audience/get-started-identity.md).

   In het voorbeeld hieronder, gebruiken wij **E-mail** namespace.

   ![](../email/assets/previewselect-namespace.png)

1. Gebruik het zoekveld om de naamruimte te zoeken, selecteer deze en klik op **[!UICONTROL Select]**

   ![](../email/assets/preview-email-namespace.png)

1. Voer in het veld **[!UICONTROL Identity value]** de waarde (hier het e-mailadres) in om het testprofiel te identificeren en klik op **[!UICONTROL Add profile]** .

   <!--![](assets/preview-identity-value.png)-->

1. Als u personalisatie aan uw bericht toevoegde, voeg andere profielen toe zodat u verschillende varianten van het bericht afhankelijk van profielgegevens kunt testen. Als profielen eenmaal zijn toegevoegd, worden deze weergegeven onder de geselecteerde velden.

   ![](../email/assets/preview-profile-list.png)

   Gebaseerd op de elementen van de berichtverpersoonlijking, toont deze lijst gegevens voor elk testprofiel in de verwante kolommen.

>[!NOTE]
>
>Naast testprofielen kunt u met [!DNL Journey optimizer] ook verschillende varianten van de inhoud testen door deze voor te vertonen en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [ leer hoe te om inhoudvariaties ](../test-approve/simulate-sample-input.md) te simuleren
