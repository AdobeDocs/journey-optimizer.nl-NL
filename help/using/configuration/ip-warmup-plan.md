---
solution: Journey Optimizer
product: journey optimizer
title: Creeer een IP warmlopingsplan
description: Leer hoe te om een IP warmup plan in Journey Optimizer te creëren
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 1%

---

# Creeer een IP warmlopingsplan {#ip-warmup}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarming](ip-warmup-gs.md)
* [IP-warmtecampagnes maken](ip-warmup-campaign.md)
* **[Creeer een IP warmlopingsplan](ip-warmup-plan.md)**
* [Voer het IP warmlopingsplan uit](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Nadat u een of meer [IP-opwarmingscampagnes](ip-warmup-campaign.md) met een specifieke toegelaten oppervlakte en de overeenkomstige toegelaten optie, kunt u beginnen tot uw IP warmup plan te leiden.

>[!CAUTION]
>
>Om tot IP warmup plannen toegang te hebben, tot stand te brengen, uit te geven en te schrappen, moet u hebben **[!UICONTROL Deliverability Consultant]** toestemming. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## Bereid het IP dossier van het warmlopingsplan voor {#prepare-file}

IP de warmte-up is een activiteit die in het geleidelijk verhogen van het volume van e-mails bestaat die van uw IPs en domein aan de belangrijkste dienstverleners van Internet (ISPs) gaan - om uw reputatie als wettige afzender te vestigen.

Deze activiteit wordt vaak uitgevoerd met de hulp van een leverbaarheidsdeskundige die helpt om een weloverwogen plan voor te bereiden dat op de industrieterreinen, gebruiksgevallen, gebieden, ISPs en diverse andere factoren wordt gebaseerd.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Alvorens een IP warmlopingsplan in te kunnen creëren [!DNL Journey Optimizer] interface, moet u een malplaatje van Excel met alle gegevens invullen die uw plan zullen voeren.

>[!CAUTION]
>
>Werk met uw leverancier consultant om ervoor te zorgen dat uw IP-bestand met opwarmingsplannen correct is ingesteld.
>
>Gebruik de indeling die in de sjabloon is opgegeven.

Hieronder is een voorbeeld van een dossier dat een IP warmlopingsplan bevat.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>Voor nu moet u de **Eigenschappen** en **Waarde** cellen onaangeroerd.

### Het lusje van het Plan van de Warmup {#ip-warmup-plan-tab}

* In dit voorbeeld is een plan voorbereid dat zich over 17 dagen uitstrekt (genoemd &quot;**looppas**&quot;) om een streefvolume van meer dan een miljoen profielen te bereiken.

* Dit plan wordt uitgevoerd via zes **fasen**, die elk ten minste één run bevatten.

* U kunt zoveel kolommen hebben als u wilt voor de domeinen u aan wilt leveren. In dit voorbeeld bestaat het plan uit zes kolommen:

   * Vier ervan komen overeen met **uit-van-de-doos domeingroepen** voor gebruik in uw abonnement (Gmail, Microsoft, Yahoo en Orange).
   * Eén komt overeen met een aangepaste domeingroep (die u moet toevoegen met de opdracht [Aangepaste domeingroep](#custom-domain-group-tab) ).
   * de zesde kolom, **Overige**, bevat alle resterende adressen van andere domeinen die niet uitdrukkelijk in het plan worden behandeld. Deze kolom is optioneel: als deze wordt weggelaten, gaan e-mails alleen naar de opgegeven domeinen.
* De **Betrokkenheidsdagen** uit de kolom blijkt dat alleen de profielen die tijdens de laatste ingevoerde periode met uw merk zijn verbonden, als doelprofiel worden gebruikt.

Het idee moet het aantal gerichte adressen in elke looppas progressief verhogen, terwijl het verminderen van het aantal looppas voor elke fase.

De uit-van-de-doos belangrijkste domeingroepen u aan uw plan kunt toevoegen zijn hieronder vermeld:

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigvijver
* Oranje
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

<!--
+++ Gmail
gmail.com;gmail.fr;gmail.de;gmail.co.uk;gmail.it
+++

+++ Adobe
adobe.com;adobe.fr;adobe.es
+++

+++WP
+++

+++Comcast
+++

+++Yahoo
+++

+++Bigpond
+++

+++Orange
+++

+++Softbank
+++

+++Docomo
+++

+++United Internet
+++

+++Microsoft
+++

+++KDDI
+++

+++Italia Online
+++

+++La Poste
+++
-->

### Tabblad Aangepaste domeingroep {#custom-domain-group-tab}

U kunt meer kolommen aan uw plan ook toevoegen door de groepen van het douanedomein te omvatten.

Gebruik de **[!UICONTROL Custom Domain Group]** om een nieuwe domeingroep te definiëren. Voor elk domein kunt u alle subdomeinen toevoegen waarop het betrekking heeft.<!--TBC-->

Als u bijvoorbeeld het aangepaste domein Luma toevoegt, wilt u de volgende subdomeinen opnemen: luma.com, luma.co.uk, luma.it, luma.fr, luma.de, enzovoort.

![](assets/ip-warmup-sample-file-custom.png)

### Voorbeeld {#example}

Stel dat u twee aangepaste domeingroepen wilt hebben:

* Eén voor alleen Hotmail-domeinen.
* Eén voor alle andere domeinen van de domeingroep Microsoft (dus exclusief alle Hotmail-domeinen).

Merk op dat alle andere domeinen in zullen worden verzameld **[!UICONTROL Others]** kolom.

1. In de **[!UICONTROL Custom Domain Group]** tabblad, maakt u de **Hotmail** domeingroep.

1. Voeg alle Hotmail-domeinen op dezelfde rij toe.

   U kunt [kopiëren en plakken](#copy-paste) alle Hotmail-domeinen die in het dialoogvenster [Het lusje van het Plan van de Warmup](#ip-warmup-plan-tab) sectie.

1. Voeg nog een rij toe.

1. Maak de **Microsoft_X** domeingroep.

1. Voeg alle Microsoft-domeinen die geen Hotmail zijn toe aan dezelfde rij. Op dezelfde manier kunt u deze uit de bovenstaande lijst kopiëren en plakken. [Meer informatie](#copy-paste)

1. Ga terug naar de **[!UICONTROL IP Warmup Plan]** tab.

1. Drie kolommen maken: één voor **Hotmail**, één voor **Microsoft_X** en één voor **Overige**.

1. Vul de kolommen naar wens in.

>[!NOTE]
>
>Zodra het IP warmup plan wordt geupload in [!DNL Journey Optimizer], hoeft u de Microsoft-domeingroepen niet uit te sluiten.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Standaarddomeinen kopiëren en plakken {#copy-paste}

Als u een aangepaste domeingroep wilt maken die bijvoorbeeld alle Hotmail-domeinen bevat, kunt u de domeinen kopiëren en plakken vanuit de standaardlijst die u opgeeft [boven](#ip-warmup-plan-tab).

Gebruik vervolgens het gereedschap voor Excel-omzetting om tekst om te zetten in kolommen:

1. Selecteren **[!UICONTROL Data]** > **[!UICONTROL Text to columns...]**, kiest u **[!UICONTROL Delimited]** en selecteert u **[!UICONTROL Next]**.

1. Selecteren **[!UICONTROL Semicolon]**, klikt u op **[!UICONTROL Next]** en **[!UICONTROL Finish]**.

Elk domein wordt nu in een andere kolom op dezelfde rij weergegeven.

## Toegang en beheer IP-opwarmingsplannen {#manage-ip-warmup-plans}

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]**. Alle IP warmup die plannen tot nu toe worden gecreeerd worden getoond.

   ![](assets/ip-warmup-filter-list.png)

1. U kunt filteren op de status. De verschillende statussen zijn:

   * **Niet gestart**: er is nog geen uitvoering geactiveerd. [Meer informatie](ip-warmup-execution.md#define-runs)
   * **Live**: het plan verandert in deze status zodra de eerste run in de eerste fase met succes is geactiveerd. [Meer informatie](ip-warmup-execution.md#define-runs)
   * **Voltooid**: het plan is gemarkeerd als voltooid. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [Meer informatie](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Om een IP warmup plan te schrappen, selecteer **[!UICONTROL Delete]** naast de naam van een abonnement en het verwijderen bevestigen.

   >[!NOTE]
   >
   >Alleen plannen met de **Niet gestart** status kan worden verwijderd.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Het geselecteerde IP warmup plan zal permanent worden geschrapt.

## Creeer een IP warmlopingsplan {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Specificeer uw IP warmtekrachtplan"
>abstract="Download het malplaatje CSV en vul het met gegevens voor IP warmup fasen en doelaantal profielen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Een marketingoppervlak selecteren"
>abstract="U moet de zelfde oppervlakte selecteren zoals die in de campagne wordt geselecteerd u met uw IP warmup plan wilt associëren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="Kanaaloppervlakken instellen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="IP-warmtecampagnes maken"

Om een IP warmup plan tot stand te brengen, volg de hieronder stappen.

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** en klik vervolgens op **[!UICONTROL Create IP warmup plan]**.

   ![](assets/ip-warmup-create-plan.png)

1. Vul de IP details van het warmlopingsplan in: geef het een naam en een beschrijving.

   ![](assets/ip-warmup-plan-details.png)

1. Selecteer de [oppervlak](channel-surfaces.md) die je wilt opwarmen. Alleen marketingoppervlakken zijn beschikbaar voor selectie. [Meer informatie over e-mailtypen](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >De campagnes u met uw IP warmlopingsplan wilt associëren moeten de zelfde oppervlakte gebruiken. [Leer hoe te om een IP warmup campagne te creëren](ip-warmup-campaign.md)

1. Upload het dossier van Excel dat uw IP warmup plan bevat. [Meer informatie](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >Als het uploaden mislukt, controleert u of u de juiste opmaak en bestandsindeling (.xls of .xlsx) gebruikt. Gebruik het voorbeeld dat u van de Adobe hebt ontvangen.

1. Klik op **[!UICONTROL Create]**. Alle fasen, looppas, kolommen en hun inhoud die in het dossier worden bepaald u uploadde automatisch worden getoond in [!DNL Journey Optimizer] interface.

   ![](assets/ip-warmup-plan-uploaded.png)

U bent nu klaar om uw IP warmlopingsplan uit te voeren. [Meer informatie](ip-warmup-execution.md)
