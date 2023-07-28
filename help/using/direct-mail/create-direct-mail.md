---
title: Een direct-mailbericht maken
description: Leer hoe u een direct-mailbericht maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: direct mail, bericht, campagne
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: d8ae894cc303237f5b2257afd8da5b2d0cf1b7a6
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 4%

---

# Een direct-mailbericht maken {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Direct mail maken"
>abstract="Maak direct-mailberichten in geplande campagnes en ontwerp de extractiedossiers die door directe postleveranciers worden vereist om post naar uw klanten te verzenden."

Als u direct-mailberichten wilt maken, maakt u een geplande campagne en configureert u het extractiebestand. Dit bestand is vereist door directe-mailproviders om e-mail naar uw klanten te verzenden.

>[!IMPORTANT]
>
>Voordat u een direct-mailbericht maakt, moet u controleren of u het volgende hebt geconfigureerd:
>
>1. A [bestand dat configuratie verplettert](../direct-mail/direct-mail-configuration.md#file-routing-configuration) die de server aangeeft waar het extractiebestand moet worden geüpload en opgeslagen,
>1. A [direct-mailberichtoppervlak](../direct-mail/direct-mail-configuration.md#direct-mail-surface) die naar het dossier zal verwijzen dat configuratie verplettert.


## Een campagne voor direct mail maken{#create-dm-campaign}

Voer de volgende stappen uit om een campagne voor directe e-mail te maken:

1. Maak een nieuwe geplande campagne en kies **[!UICONTROL Direct mail]** als de handeling.

1. Selecteer de **[!UICONTROL Direct mail surface]** gebruiken en klikken **[!UICONTROL Create]**. [Leer hoe u een direct-mailoppervlak maakt](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. In de **[!UICONTROL Properties]** sectie, uw campagne bewerken **[!UICONTROL Title]** en **[!UICONTROL Description]**.

1. Om uw doelpubliek te bepalen, klik **[!UICONTROL Select audience]** en kies een van de beschikbare Adobe Experience Platform-doelgroepen. [Meer informatie](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Momenteel is de selectie van het publiek beperkt tot 3 miljoen profielen. Deze beperking kan op verzoek aan uw Adobe-vertegenwoordiger worden opgeheven.

1. In de **[!UICONTROL Identity namespace]** selecteert u de juiste naamruimte om personen in het gekozen publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. De campagnes kunnen voor een specifieke datum worden gepland of worden geplaatst om met regelmatige intervallen opnieuw te komen. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

U kunt nu het extractiebestand configureren en verzenden naar uw directe-mailprovider.

## Het extractiebestand configureren {#extraction-file}

Het extractiebestand wordt vereist door directe-mailproviders om e-mail naar uw klanten te sturen. Voer de volgende stappen uit om de configuratie van het extractiebestand te definiëren:

1. Van het scherm van de campagneconfiguratie, klik **[!UICONTROL Edit content]** om de inhoud van het extractiebestand te configureren.

1. Pas de eigenschappen van het extractiebestand aan:

   1. Geef de gewenste waarden op **[!UICONTROL Filename]** voor het extractiebestand.

   1. Schakel desgewenst de optie **[!UICONTROL Append timestamp to export filename]** als u een automatische tijdstempel wilt toevoegen aan de opgegeven bestandsnaam.

   1. Soms moet u informatie toevoegen aan het begin of aan het einde van het extractiebestand. Om dit te doen, gebruik **[!UICONTROL Notes]** Geef vervolgens aan of u de notitie wilt opnemen als kop- of voettekst.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. Configureer de kolommen en de informatie die in het extractiebestand moeten worden weergegeven:

   1. Klik op de knop **[!UICONTROL Add]** om een nieuwe kolom te maken.

   1. De **[!UICONTROL Formatting]** wordt aan de rechterkant weergegeven, zodat u de geselecteerde kolom kunt instellen. Geef een **[!UICONTROL Label]** voor de kolom.

   1. In de **[!UICONTROL Data]** in het veld selecteert u de profielkenmerken die u wilt weergeven met de [Expressieeditor](../personalization/personalization-build-expressions.md).

   1. Als u het extractiebestand wilt sorteren met een kolom, selecteert u de kolom en schakelt u de optie **[!UICONTROL Sort by]** -optie. De **[!UICONTROL Sort By]** wordt weergegeven naast het label van de kolom in het dialoogvenster **[!UICONTROL Data Fields]** sectie.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. Herhaal deze stappen om zoveel kolommen toe te voegen als u nodig hebt voor het extractiebestand. U kunt maximaal 50 kolommen toevoegen.

      Als u de positie van een kolom wilt wijzigen, sleept u de kolom naar de gewenste locatie in het dialoogvenster **[!UICONTROL Data field]** sectie. Als u een kolom wilt verwijderen, selecteert u deze en klikt u op de knop **[!UICONTROL Remove]** in de **[!UICONTROL Formatting]** venster.

U kunt nu uw directe-mailbericht testen en verzenden naar uw publiek. [Leer hoe u e-mailberichten test en verzendt](test-send-direct-mail.md)
