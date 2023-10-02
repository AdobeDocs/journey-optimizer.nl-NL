---
solution: Journey Optimizer
product: journey optimizer
title: Creeer een IP warmlopingsplan
description: Leer hoe te om een IP warmup plan in Journey Optimizer te creëren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: 205f26d3f31b9f003fc1dbaf679021464429d144
workflow-type: tm+mt
source-wordcount: '797'
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

## Bereid het IP dossier van het warmlopingsplan voor {#prepare-file}

IP de warmte-up is een activiteit die in het geleidelijk verhogen van het volume van e-mails bestaat die van uw IPs en domein aan de belangrijkste dienstverleners van Internet (ISPs) gaan - om uw reputatie als wettige afzender te vestigen.

Deze activiteit wordt vaak uitgevoerd met de hulp van een leverbaarheidsdeskundige die helpt om een weloverwogen plan voor te bereiden dat op de industrieterreinen, gebruiksgevallen, gebieden, ISPs en diverse andere factoren wordt gebaseerd.

Als u werkt met de [!DNL Journey Optimizer] IP warmup eigenschap, neemt dit plan de vorm van een dossier van Excel dat een aantal vooraf bepaalde kolommen moet bevatten. Alvorens een IP warmlopingsplan in te kunnen creëren [!DNL Journey Optimizer] interface, moet u dit malplaatje met alle gegevens invullen die uw plan zullen voeren.

>[!CAUTION]
>
>Werk met uw leverancier consultant om ervoor te zorgen dat uw IP-bestand met opwarmingsplannen correct is ingesteld.

Hieronder is een voorbeeld van een dossier dat een IP warmlopingsplan bevat.

![](assets/ip-warmup-sample-file.png)

### Het lusje van het Plan van de Warmup

* In dit voorbeeld is een plan voorbereid dat zich over 17 dagen uitstrekt (genoemd &quot;**looppas**&quot;) een streefvolume van meer dan 1 miljoen profielen te bereiken.

* Dit plan wordt uitgevoerd via 6 **fasen**, die elk ten minste één run bevatten.

* U kunt zoveel kolommen hebben als u wilt voor de domeinen u aan wilt leveren. In dit voorbeeld is het plan verdeeld in zes kolommen, waarvan 5 overeenkomen met het **hoofddomeingroepen** te gebruiken in uw plan (Gmail, Microsoft, Yahoo, Orange en Apple) en de zesde kolom, **Overige**, bevat alle resterende adressen van andere domeinen.
* De **Betrokkenheidsdagen** in de kolom staat dat alleen de profielen worden gebruikt die de afgelopen 30 dagen bij uw merk zijn gebruikt.

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

### Tabblad Aangepaste domeingroep

U kunt meer kolommen aan uw plan ook toevoegen door de groepen van het douanedomein te omvatten.

Gebruik de **[!UICONTROL Custom Domain Group]** om een nieuwe domeingroep te definiëren. Voor elk domein kunt u alle subdomeinen toevoegen waarop het betrekking heeft.<!--TBC-->

Als u bijvoorbeeld het aangepaste domein Luma toevoegt, wilt u de volgende subdomeinen opnemen: luma.com, luma.co.uk, luma.it, luma.fr, luma.de, enzovoort.

![](assets/ip-warmup-sample-file-custom.png)

## Toegang en beheer IP-opwarmingsplannen {#manage-ip-warmup-plans}

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]**. Alle IP warmup die plannen tot nu toe worden gecreeerd worden getoond.

   ![](assets/ip-warmup-filter-list.png)

1. U kunt filteren op de status. De verschillende statussen zijn:

   * **Niet gestart**: er is nog geen uitvoering geactiveerd. [Meer informatie](ip-warmup-execution.md#define-runs)
   * **Live**: het plan verandert in deze status zodra de eerste run in de eerste fase met succes is geactiveerd. [Meer informatie](ip-warmup-execution.md#define-runs)
   * **Voltooid**: het plan is gemarkeerd als voltooid. Deze optie is alleen beschikbaar als alle runnen in het abonnement zijn opgenomen **[!UICONTROL Completed]** of **[!UICONTROL Draft]** status (geen run kan worden uitgevoerd) **[!UICONTROL Live]**). [Meer informatie](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Om een IP warmup plan te schrappen, selecteer **[!UICONTROL Delete]** naast de naam van een abonnement en het verwijderen bevestigen.

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

Wanneer een of meer live campagnes met de **[!UICONTROL IP warmup plan activation]** toegelaten optie wordt geactiveerd, kunt u hen met een IP warmlopingsplan associëren.

>[!CAUTION]
>
>Om IP warmup plannen tot stand te brengen, uit te geven en te schrappen, moet u hebben **[!UICONTROL Deliverability Consultant]** toestemming. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** en klik vervolgens op **[!UICONTROL Create IP warmup plan]**.

   ![](assets/ip-warmup-create-plan.png)

1. Vul de IP details van het warmlopingsplan in: geef het een naam en een beschrijving.

   ![](assets/ip-warmup-plan-details.png)

1. Selecteer een [oppervlak](channel-surfaces.md). Alleen marketingoppervlakken zijn beschikbaar voor selectie. [Meer informatie over e-mailtypen](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >U moet de zelfde oppervlakte selecteren zoals die in de campagne wordt geselecteerd u met uw IP warmup plan wilt associëren. [Leer hoe te om een IP warmup campagne te creëren](ip-warmup-campaign.md)

1. Upload het dossier van Excel dat uw IP warmup plan bevat. [Meer informatie](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Klik op **[!UICONTROL Create]**. Alle fasen, looppas, kolommen en hun inhoud die in het dossier worden bepaald u uploadde automatisch worden getoond in [!DNL Journey Optimizer] interface. [Meer informatie](ip-warmup-execution.md)

   ![](assets/ip-warmup-plan-uploaded.png)
