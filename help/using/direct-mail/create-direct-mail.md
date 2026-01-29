---
title: Een direct-mailbericht maken
description: Leer hoe u een direct-mailbericht maakt in Journey Optimizer
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: direct mail, bericht, campagne
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 3fdfc98c0049f39d12b1cb2241fde892f449cdc1
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 2%

---

# Een direct-mailbericht maken {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Direct mail maken"
>abstract="Maak direct-mailberichten in geplande campagnes en reizen en ontwerp de extractiebestanden die de direct-mailproviders nodig hebben om e-mail naar uw klanten te sturen."

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="Eindactiviteit"
>abstract="Directe post is een off-line kanaal dat u toestaat om de extractiedossiers te personaliseren en te produceren die door derde directe postleveranciers worden vereist om post naar uw klanten te verzenden."

Als u direct-mailberichten wilt maken, maakt u een geplande campagne of een reis en configureert u het extractiebestand. Dit bestand is vereist door directe-mailproviders om e-mail naar uw klanten te verzenden.

>[!IMPORTANT]
>
>Voordat u een direct-mailbericht maakt, moet u controleren of u het volgende hebt geconfigureerd:
>
>1. A [&#x200B; dossier dat configuratie &#x200B;](../direct-mail/direct-mail-configuration.md#file-routing-configuration) verplettert die de server specificeert waar het extractiedossier zou moeten worden geupload en worden opgeslagen,
>1. A [&#x200B; direct-mailberichtconfiguratie &#x200B;](../direct-mail/direct-mail-configuration.md#direct-mail-surface) die het dossier zal van verwijzingen voorzien dat configuratie verplettert.

## Een e-mailbericht toevoegen {#create-dm-campaign}

Blader op de onderstaande tabbladen om te leren hoe u een direct-mailbericht kunt toevoegen aan een campagne of een reis.

>[!BEGINTABS]

>[!TAB voeg een Directe postbericht aan een Reis  toe]

1. Open uw reis dan belemmering en laat vallen a **[!UICONTROL Direct mail]** activiteit van de **2&rbrace; sectie van Acties &lbrace;van het palet.**

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtconfiguratie aan gebruik. Het veld **[!UICONTROL configuration]** wordt standaard voorgevuld met de laatste configuratie die de gebruiker voor dat kanaal heeft gebruikt. Voor meer informatie over hoe te om een reis te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../building-journeys/journey-gs.md).

1. Configureer het extractiebestand dat u naar uw directe-mailprovider wilt verzenden. Klik hiertoe op de knop **[!UICONTROL Edit content]** .

   ![](assets/direct-mail-add-journey.png)

1. Pas de eigenschappen van het extractiebestand aan, zoals de bestandsnaam, of de kolommen die u wilt weergeven. Voor meer informatie over hoe te om de eigenschappen van het extractiedossier te vormen, verwijs naar deze sectie: [&#x200B; creeer een direct-mailbericht &#x200B;](../direct-mail/create-direct-mail.md#extraction-file).

   ![](assets/direct-mail-journey-content.png)

1. Nadat de inhoud van het extractiebestand is gedefinieerd, kunt u er testprofielen voor gebruiken. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

   Klik hiertoe op **[!UICONTROL Simulate content]** en voeg vervolgens een testprofiel toe om te controleren hoe het extractiebestand met de testprofielgegevens wordt gerenderd. De gedetailleerde informatie over hoe te om testprofielen en voorproef uw inhoud te selecteren is beschikbaar in de [&#x200B; sectie van het Beheer van de Inhoud &#x200B;](../content-management/preview-test.md).

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

Wanneer uw extractiedossier klaar is, voltooi de configuratie van uw [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md) om het te verzenden.

>[!TAB  voeg een Directe postbericht aan een Campagne toe ]

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .

1. Selecteer het **Gepland - marketing** campagneretype.

1. Bewerk in de sectie **[!UICONTROL Properties]** de items **[!UICONTROL Title]** en **[!UICONTROL Description]** van uw campagne.

1. Als u het doelpubliek wilt definiëren, klikt u op de knop **[!UICONTROL Select audience]** en kiest u een van de beschikbare Adobe Experience Platform-doelgroepen. [Meer informatie](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Momenteel is de selectie van het publiek beperkt tot 3 miljoen profielen. Deze beperking kan op verzoek aan je Adobe-vertegenwoordiger worden opgeheven.

1. Selecteer in het veld **[!UICONTROL Identity namespace]** de juiste naamruimte om personen in het gekozen publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Kies in de sectie **[!UICONTROL Actions]** de optie **[!UICONTROL Direct mail]** .

1. Selecteer of maak een **[!UICONTROL Direct mail configuration]** die u wilt gebruiken. [&#x200B; Leer hoe te om een direct-mailconfiguratie &#x200B;](direct-mail-configuration.md#direct-mail-surface) tot stand te brengen.

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

   >[!AVAILABILITY]
   >
   >De directe Post steunt de **Holdout** functionaliteit maar steunt momenteel niet **Behandelingen**. [&#x200B; leren hoe te met experimenten &#x200B;](../content-management/get-started-experiment.md) te werken

1. De campagnes kunnen voor een specifieke datum worden gepland of worden geplaatst om met regelmatige intervallen opnieuw te komen. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [&#x200B; te vormen deze sectie &#x200B;](../campaigns/campaign-schedule.md).

U kunt nu het extractiebestand configureren en verzenden naar uw directe-mailprovider.

>[!ENDTABS]

## Het extractiebestand configureren {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="Gegevensvelden"
>abstract="Voeg en vorm de kolommen en de informatie toe die in het extractiedossier moet worden getoond dat door directe postleveranciers wordt vereist om post naar uw klanten te verzenden. U kunt maximaal 50 kolommen toevoegen."

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="Opmaak van extractiebestanden"
>abstract="Geef voor elk veld een label en de informatie op die u wilt weergeven met de verpersoonlijkingseditor. <br/><br/> De <b> Soort door </b> optie staat u toe om het geselecteerde gebied te gebruiken om de kolommen van het extractiedossier te sorteren."

Het extractiebestand wordt vereist door directe-mailproviders om e-mail naar uw klanten te sturen. Voer de volgende stappen uit om de configuratie van het extractiebestand te definiëren:

1. Klik in het scherm Campagneconfiguratie op de knop **[!UICONTROL Edit content]** om de inhoud van het extractiebestand te configureren.

1. Pas de eigenschappen van het extractiebestand aan:

   1. Geef in het veld **[!UICONTROL Filename]** een naam op voor het extractiebestand.

      >[!NOTE]
      >
      >Standaard wordt het bestand naar de hoofdmap op de server geschreven. Het veld **[!UICONTROL Filename]** accepteert ook de notatie &quot;/your/path/here/Filename.csv&quot;, waarbij het opgegeven pad de doelmap op de geselecteerde server is. <!--TBC if for SFTP and Azure only, or for all servers including S3-->

   1. Schakel desgewenst de optie **[!UICONTROL Append timestamp to export filename]** in als u een automatische tijdstempel wilt toevoegen aan de opgegeven bestandsnaam.

   1. Soms moet u informatie toevoegen aan het begin of aan het einde van het extractiebestand. Hiervoor gebruikt u het veld **[!UICONTROL Notes]** en geeft u op of u de notitie wilt opnemen als kop- of voettekst.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. Configureer de kolommen en de informatie die in het extractiebestand moeten worden weergegeven:

   1. Klik op **[!UICONTROL Add]** om een nieuwe kolom te maken.

   1. Het deelvenster **[!UICONTROL Formatting]** wordt aan de rechterkant weergegeven, zodat u de geselecteerde kolom kunt instellen. Geef een **[!UICONTROL Label]** voor de kolom op.

   1. Op het **[!UICONTROL Data]** gebied, selecteer de profielattributen om te tonen gebruikend de [&#x200B; verpersoonlijkingsredacteur &#x200B;](../personalization/personalization-build-expressions.md).

   1. Als u het extractiebestand wilt sorteren met een kolom, selecteert u de kolom en schakelt u de optie **[!UICONTROL Sort by]** in. Het pictogram **[!UICONTROL Sort By]** wordt weergegeven naast het label van de kolom in de sectie **[!UICONTROL Data Fields]** .

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. Herhaal deze stappen om zoveel kolommen toe te voegen als u nodig hebt voor het extractiebestand. U kunt maximaal 50 kolommen toevoegen.

      Als u de positie van een kolom wilt wijzigen, sleept u de kolom naar de gewenste locatie in de sectie **[!UICONTROL Data field]** . Als u een kolom wilt verwijderen, selecteert u deze en klikt u op de knop **[!UICONTROL Remove]** in het deelvenster **[!UICONTROL Formatting]** .

U kunt nu uw directe-mailbericht testen en verzenden naar uw publiek. [&#x200B; Leer hoe te om direct-mailberichten te testen en te verzenden &#x200B;](test-send-direct-mail.md)
