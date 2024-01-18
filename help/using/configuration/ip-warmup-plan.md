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
badge: label="Beta"
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: a5b3cd4eba18789d6014a7288ce6b0678a07982e
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 0%

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

Om tot IP warmup plannen toegang te hebben, tot stand te brengen, uit te geven en te schrappen, moet u hebben **[!UICONTROL Deliverability Consultant]** rol of IP warmup plannen verwante toestemmingen.

+++Leer hoe te om de rol van de Adviseur van de Leverbaarheid of IP warmteopwarmingsplannen verwante toestemmingen toe te wijzen

De bijbehorende machtiging toewijzen aan een specifieke **[!UICONTROL Role]**:

1. Van de [!DNL Permissions] product, navigeer naar de **[!UICONTROL Roles]** en selecteert u de rol die u wilt bijwerken met het nieuwe **[!UICONTROL IP Warmup Configurations]** machtigingen.

1. Van uw **[!UICONTROL Role]** dashboard, klik **[!UICONTROL Edit]**.

   ![](assets/ip_permissions_1.png)

1. Sleep de **[!UICONTROL IP Warmup Configurations]** bron om bevoegdheid toe te wijzen.

1. Van de **[!UICONTROL IP Warmup Configurations]** bron drop-down, selecteer welke toestemmingen uw gebruiker wenst.

   ![](assets/ip_permissions_2.png)

1. Klik op **[!UICONTROL Save]**.

De bijbehorende rol toewijzen aan een **[!UICONTROL User]**:

1. Van de [!DNL Permissions] product, navigeer naar de **[!UICONTROL Roles]** en selecteert u de **[!UICONTROL Deliverability Consultant]** ingebouwde rol.

1. Van uw **[!UICONTROL Role]** dashboard, toegang tot **[!UICONTROL Users]** tab.

   ![](assets/ip_permissions_3.png)

1. Klikken **[!UICONTROL Add user]** om de **[!UICONTROL Deliverability Consultant]** ingebouwde rol.

   ![](assets/ip_permissions_4.png)

1. Selecteer uw **[!UICONTROL User]** en klik op **[!UICONTROL Save]**.

   ![](assets/ip_permissions_5.png)

+++

## Bereid het IP dossier van het warmlopingsplan voor {#prepare-file}

IP de warmte-up is een activiteit die in het geleidelijk verhogen van het volume van e-mails bestaat die van uw IPs en domein aan de belangrijkste dienstverleners van Internet (ISPs) gaan - om uw reputatie als wettige afzender te vestigen.

Deze activiteit wordt vaak uitgevoerd met de hulp van een leverbaarheidsdeskundige die helpt om een weloverwogen plan voor te bereiden dat op de industrieterreinen, gebruiksgevallen, gebieden, ISPs en diverse andere factoren wordt gebaseerd.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Alvorens een IP warmlopingsplan in te kunnen creëren [!DNL Journey Optimizer] interface, moet u een malplaatje van Excel met alle gegevens invullen die uw plan zullen voeren.

<!--
* From the user interface you can download the blank Excel [IP warmup plan template](assets/IPWarmupPlan-Template.xlsx) to fill in.

* You can also download a [sample IP warmup plan](assets/IPWarmupPlan-Sample.xlsx) already filled in with some data you can use as an example.-->

* Van het gebruikersinterface kunt u het lege malplaatje van het de opwarmingsplan van Excel downloaden IP om in te vullen.

* U kunt een steekproefIP warmteopnameplan ook downloaden dat reeds met sommige gegevens wordt gevuld u als voorbeeld kunt gebruiken.

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

* In dit voorbeeld is een plan voorbereid dat zich over 17 dagen uitstrekt (genoemd &quot;**looppas**&quot;) om een doelvolume van meer dan een miljoen profielen te bereiken.

* Dit plan wordt uitgevoerd via zes **fasen**, die elk ten minste één run bevatten.

* U kunt zoveel kolommen hebben als u wilt voor de domeinen u aan wilt leveren. In dit voorbeeld bestaat het plan uit zes kolommen:

   * Vier ervan komen overeen met **uit-van-de-doos domeingroepen** voor gebruik in uw abonnement (Gmail, Microsoft, Yahoo en Orange).
   * Eén komt overeen met een aangepaste domeingroep (die u moet toevoegen met de opdracht [Aangepaste domeingroep](#custom-domain-group-tab) ).
   * de zesde kolom, **Overige**, bevat alle resterende adressen van andere domeinen die niet uitdrukkelijk in het plan worden behandeld. Deze kolom is optioneel: als deze wordt weggelaten, gaan e-mails alleen naar de opgegeven domeinen.
* De **Betrokkenheidsdagen** uit de kolom blijkt dat alleen de profielen die tijdens de laatste ingevoerde periode met uw merk zijn verbonden, als doelprofiel worden gebruikt.

Het idee moet het aantal gerichte adressen in elke looppas progressief verhogen, terwijl het verminderen van het aantal looppas voor elke fase.

De uit-van-de-doos belangrijkste domeingroepen u aan uw plan kunt toevoegen zijn hieronder vermeld:

<!--
* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple
-->

+++ Gmail gmail.com;google.com;googlemail.com;googlemail.co.uk
+++

+++ Adobe adobe.com
+++

+++WP wp.pl;o2.pl
+++

+++comcast.net
+++

+++Yahoo aol.fi;cs.com;yahoo.com.in;games.com;y7mail.com;yahoo.co.uk;yahoo.hu;yahoo.co.hu;yahoo.cn;yahoogroups.com.sg;yahoogroups.com.au;aol.es yahoo.com.au;yahoo.com.vn yahoo.ca;aol.co.nz;aolaolpol.pnoge.no;bahoo;bo;bco;bahoo;ba;yahoo.hr;aol.cz;yahoo.ee;aol.be;aolcom.tr;yahoo.si;aol.it;yahoo.es;yahoo.dk;yahoo.dk;yahoogroups.ca;document;aol.kr;yahoo.ie;ahoo;jp;yahoo o.lt;document;aol.nl;document;yahoo.bg;documen;aol.se;yahoo.de;aanbevelingen;document;yahoo.nl;document;aol.dk;document;aol.cl;document;yahoo.no;document;yahoo;cz;yahoo.sk;documenten;yahoo.de;yahoo.gr;document;yahoo.ro;document;yahoo.at;document;document;docum;aol.fr;yahoo.in;aol.in;yahoo.rs;yahoo.de;de;document;document;;document;yahoo.se;myahoo;se;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s;s aol.jp;document;yahoo.pt;document;yahoogrupper.dk;yahoo.fr;document;aol.pl;document;docum;aol.ch;yahoo.it;document;aolpolcka.pl;document;document;yagroppi.it;yahoo.cl;document;yahoo;cl;;document;document;document;yahoo.be;document;aol.tw;document;document;document;document;document;document;document;aol.ru;document;document;yahoo.lv;aolpolska.pl;aol.at;yahoo.pl
+++

+++Bigpond bigpond.com;bigpond.com.au;bigpond.net;telstra.com;bigpond.net.au
+++

+++Orange voila.com;francetelecom.com;orange.com;orange.fr;wanadoo.fr;voila.fr
+++

+++++Softbank c.vodafone.ne.jp;jp-h.ne.jp;;jp-d.ne.jp;jp-c.ne.jp;t.vodafone.ne.jp;jp-t.ne.jp;jp-q.ne.jp;r.vodafone.ne.jp;s.vodafone.ne.jp;q.vodafone.ne.jp;jp-s.ne.jp;h.vodafone.ne.jp;b;b;b;k.vodafone.ne.jp;appa;append;appc;appt;appa
+++

+++Docomo docomo.ne.jp
+++

+++United Internet gmx.de;1and1.com;gmx.fr;mail.com;1und1.de;gmx.com;gmx.net;gmx.at;web.de;gmx.ch
+++

++ Microsoft hotmail.com.tr;hotmail.chotmail.jp live.ru;live.nl;live.jp;windowslive.com;xbox.com;mail.fr;hotmail.chotmail.jp.cl;live.at;at;hk hotmail.com.au;hotmail.com;live.com.au;hotmail.co.kr;hotmail.co.th;outlook.com.br;hotmail;hotmail;hotmail;jp;live.outoutoutoutoutout.cl;live.htm;lik;hotmail.co.il;hk live.co.kr;live.co.uk;live.com.mx hotmail.co.uk;live.com.sg;msn.com;hotmail.co.jp;live.co.za;live.com.pt;outlook.com;live.com live.com.ar hotmail.com.br live.com.my;hotmail.com.ar;.;;;;;;;;live.cn;sancties;hotmail.es;live.fr;live.no;live.dk;hotmail.it;live.se;.se;olijf;be;live.in;hotmail.ch;fax;hotmail.ch;document;fax;hotmail.gr;live.it;hotmail.ca;support;fax;live.ca;hotmail.de
+++

+++KDDI au.com;ezweb.ne.jp;uqmobile.jp
+++

+++Italia Online inwind.it;blu.it;virgilio.it;giallo.it;iol.it;libero.it
+++

+++La Poste laposte.net
+++

+++Apple mac.com;icloud.com;apple.com;me.com
+++

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

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** -menu. Alle IP warmup die plannen tot nu toe worden gecreeerd worden getoond.

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
>abstract="Vul het malplaatje van Excel met alle gegevens in die uw plan, zoals IP warmup fasen en doelaantal profielen zullen voeren, en upload het hier."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-plan.html#prepare-file" text="Bereid het IP dossier van het warmlopingsplan voor"

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
   >Als het uploaden mislukt, controleert u of u de juiste opmaak en bestandsindeling (.xls of .xlsx) gebruikt. De sjabloon gebruiken<!--assets/IPWarmupPlan-Template.xlsx--> verstrekt aan u door Adobe.

1. Klik op **[!UICONTROL Create]**. Alle fasen, looppas, kolommen en hun inhoud die in het dossier worden bepaald u uploadde automatisch worden getoond in [!DNL Journey Optimizer] interface.

   ![](assets/ip-warmup-plan-uploaded.png)

   >[!NOTE]
   >
   >De **[!UICONTROL Targeted]** de kolom toont de som alle profielen die voor elke looppas worden gericht, betekenend alle profielen van elke domeingroepen die u, met inbegrip van de **Overige** kolom, indien aanwezig.

U bent nu klaar om uw IP warmlopingsplan uit te voeren. [Meer informatie](ip-warmup-execution.md)
