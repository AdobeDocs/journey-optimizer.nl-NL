---
title: PTR-records
description: Leer hoe u PTR-records beheert
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# PTR-records {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="PTR-records van subdomeinen"
>abstract="Een wijzerverslag (PTR) is een type van DNS verslag dat de domeinnaam verbonden aan een IP adres verstrekt, dat de ontvangende postservers helpt om de IP van afzenders adressen te verifiëren."

## PTR-records {#about-ptr-records}

Een wijzerverslag (PTR) is een type van het verslag van het Systeem van de Naam van het Domein (DNS) dat de domeinnaam verbonden aan een IP adres verstrekt.

Met PTR verslagen, kunnen het ontvangen van postservers de authenticiteit van het verzenden van postservers controleren door te identificeren of hun IP adressen aan de namen beantwoorden die de servers verbinden met.

## De PTR-records van uw subdomeinen openen {#access-ptr-records}

Eenmaal [een subdomein wordt gedelegeerd](delegate-subdomain.md) in Adobe Journey Optimizer wordt automatisch een PTR-record gemaakt en gekoppeld aan dit subdomein. U hebt toegang tot dit bestand via het dialoogvenster **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** -menu.

![](assets/ptr-records.png)

In de lijst worden de PTR-records weergegeven die voor elk gedelegeerd subdomein zijn gegenereerd. Hierbij wordt de volgende syntaxis gebruikt:

* &quot;r&quot; voor opnamen,
* &quot;xx&quot; voor de twee laatste cijfers van het IP-adres,
* subdomeinnaam.

U kunt een PTR-record in de lijst openen om de bijbehorende subdomeinnaam en het IP-adres weer te geven.

## Een PTR-record bewerken {#edit-ptr-record}

U kunt een PTR-record wijzigen om het subdomein te bewerken dat aan een IP-adres is gekoppeld.

>[!CAUTION]
>
>Ga voorzichtig verder met het bewerken van PTR-records. Neem in geval van twijfel contact op met een leverancier.<!--why?-->

>[!NOTE]
>
>U kunt de **[!UICONTROL IP]** en **[!UICONTROL PTR record]** velden.

### Volledig gedelegeerde subdomeinen {#fully-delegated-subdomains}

Een PTR-record bewerken met een subdomein dat [volledig gedelegeerd](delegate-subdomain.md#full-subdomain-delegation) om te Adobe, volg de hieronder stappen.

1. Klik in de lijst op de naam van een PTR-record om deze te openen.

   ![](assets/ptr-record-select.png)

1. Een subdomein selecteren [volledig gedelegeerd](delegate-subdomain.md#full-subdomain-delegation) naar Adobe in de lijst.

   ![](assets/ptr-record-subdomain.png)

1. Klikken **[!UICONTROL Save]** om uw wijzigingen te bevestigen.

### Gedelegeerde subdomeinen die de methode CNAME gebruiken {#edit-ptr-subdomains-cname}

Als u een PTR-record wilt bewerken met een subdomein dat is gedelegeerd aan Adobe, gebruikt u de opdracht [CNAME, methode](delegate-subdomain.md#cname-subdomain-delegation)volgt u de onderstaande stappen.

1. Klik in de lijst op de naam van een PTR-record om deze te openen.

   ![](assets/ptr-record-select-cname.png)

1. Selecteer een subdomein dat aan Adobe wordt gedelegeerd met de opdracht [CNAME, methode](delegate-subdomain.md#cname-subdomain-delegation) in de lijst.

   ![](assets/ptr-record-subdomain-cname.png)

1. U moet een nieuw voorwaarts DNS verslag op uw het ontvangen platform tot stand brengen. Hiervoor kopieert u de record die door Adobe is gegenereerd. Als u klaar bent, schakelt u het selectievakje &quot;Ik bevestig...&quot; in.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Als u dit bericht krijgt: &quot;Maak eerst een nieuwe DNS en probeer het opnieuw&quot;, volg de onderstaande stappen:
   >   * Controleer de DNS leverancier als het voorwaartse DNS verslag met succes werd gecreeerd.
   >   * Records in de DNS worden mogelijk niet meteen gesynchroniseerd. Wacht een paar minuten en probeer het opnieuw.


1. Klikken **[!UICONTROL Save]** om uw wijzigingen te bevestigen.

## Details van PTR-recordupdate controleren {#check-ptr-record-update}

A **[!UICONTROL Processing]** wordt weergegeven naast de naam van de PTR-record in de lijst.

![](assets/ptr-record-updating.png)

Klik op de knop **[!UICONTROL Updating]** of **[!UICONTROL Recent updates]** pictogram.

![](assets/ptr-record-recent-update.png)

U kunt informatie zoals de updatestatus, en de gevraagde veranderingen zien.

![](assets/ptr-record-updates.png)

## PTR-recordupdatestatus {#ptr-record-update-statuses}

Een PTR-recordupdate kan de volgende statussen hebben:

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL Processing]**: De PTR-recordupdate is verzonden en wordt momenteel gecontroleerd.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Success]**: Het bijgewerkte PTR-record is geverifieerd en het nieuwe subdomein is nu gekoppeld aan het IP-adres.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de PTR-recordupdate.

### Verwerking {#processing}

Verscheidene leveringscontroles zullen worden uitgevoerd om te verifiëren dat nieuwe subdomain aan vennoot met het IP adres geldig is. <!--The processing time is around **48h-72h**, and can take up to **7-10 days**.-->

>[!NOTE]
>
>U kunt een PTR-record niet wijzigen terwijl er een update wordt uitgevoerd. U kunt nog steeds op de naam klikken, maar wel op de knop **[!UICONTROL Subdomain]** veld wordt grijs weergegeven. De wijzigingen worden pas doorgevoerd als de update is gelukt.

Tijdens het validatieproces wordt het oude subdomein nog steeds gekoppeld aan het IP-adres.

### Succes {#success}

Wanneer het validatieproces is voltooid, wordt het nieuwe subdomein automatisch gekoppeld aan het IP-adres.

### Mislukt {#failes}

Als het validatieproces mislukt, wordt de oudere PTR-record weergegeven. Het geldige subdomein dat eerder aan het IP adres werd geassocieerd blijft onveranderd.

De mogelijke updatefouten zijn als volgt:
* Fout bij het maken van een nieuwe, voorwaartse DNS voor de PTR-record
* Kan de record niet bijwerken
* Niet opnieuw aan boord gaan van de affinities

Als de update mislukt, kan de PTR-record opnieuw worden bewerkt. U kunt op de naam van het subdomein klikken en het subdomein opnieuw bijwerken.
