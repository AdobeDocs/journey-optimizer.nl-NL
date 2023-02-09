---
solution: Journey Optimizer
product: journey optimizer
title: De vervolgkeuzelijst beheren
description: Leer hoe u de lijst met Journey Optimizer-suppressies kunt openen en beheren
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: onderdrukken, lijst, stuiteren, e-mail, optimaliseren, quarantaine
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 1af4f6c0ec3b529eb53c45e1cfa2fd0148a98b04
workflow-type: tm+mt
source-wordcount: '1457'
ht-degree: 1%

---

# De vervolgkeuzelijst beheren {#manage-suppression-list}

Met [!DNL Journey Optimizer], kunt u alle e-mailadressen controleren die automatisch worden uitgesloten van het verzenden van een reis of een campagne, zoals harde stuiteringen, zachte stuiters, en spamklachten.

Dergelijke e-mailadressen worden automatisch verzameld in de Journey Optimizer **onderdrukkingslijst**. Een suppressielijst bestaat uit adressen en domeinen die van uw publiek moeten worden uitgesloten. Het verzamelt e-mailadressen en domeinen die over alle post in één enkele cliëntmilieu worden onderdrukt, betekenend specifiek voor een organisatie ID verbonden aan een zandbak identiteitskaart

Meer informatie over het concept en het gebruik van de suppressielijst in [deze sectie](../reports/suppression-list.md).



## De lijst met onderdrukking openen {#access-suppression-list}

Blader naar de gedetailleerde lijst met uitgesloten e-mailadressen en domeinen voor toegang tot deze lijst **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** en selecteert u **[!UICONTROL Suppression list]**.


![](assets/suppression-list-access.png)

>[!CAUTION]
>
>Machtigingen voor het weergeven, exporteren en beheren van de suppressielijst zijn beperkt tot [Reisbeheerders](../administration/ootb-product-profiles.md#journey-administrator). Meer informatie over beheren [!DNL Journey Optimizer] toegangsrechten van gebruikers in [deze sectie](../administration/permissions-overview.md).


Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren.

![](assets/suppression-list-filters.png)

U kunt filteren op de **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]**, of **[!UICONTROL Reason]**. Selecteer een of meer opties voor elk criterium. Als deze optie is geselecteerd, kunt u elk filter of alle filters die boven op de lijst worden weergegeven, wissen.

![](assets/suppression-list-filtering-example.png)


## Redenen voor fouten begrijpen {#suppression-categories-and-reasons}

Wanneer een bericht niet aan een e-mailadres kan worden bezorgd, [!DNL Journey Optimizer] bepaalt waarom de levering ontbrak en het met een associeert **[!UICONTROL Suppression category]**.

De onderdrukkingscategorieën zijn als volgt:

* **Hard**: Een vaste stuit geeft een ongeldig e-mailadres aan (een e-mailadres dat niet bestaat). Dit omvat een stuitbericht van de ontvangende e-mailserver waarin expliciet wordt vermeld dat het adres ongeldig is. Het e-mailadres wordt direct naar de onderdrukkingslijst verzonden.

   Wanneer de fout het resultaat van een spamklacht is, valt het ook in **Hard** categorie. Het e-mailadres van de ontvanger die de klacht heeft ingediend, wordt onmiddellijk naar de onderdrukkingslijst gezonden.

* **Zacht**: Een zachte stuit is een tijdelijke e-mailstuit die voor een geldig e-mailadres voorkwam. Het e-mailadres wordt toegevoegd aan de suppressielijst nadat u het opnieuw hebt geprobeerd. Zachte fouten verzenden een adres naar de onderdrukkingslijst zodra de foutenteller de grensdrempel bereikt. [Meer informatie over pogingen](retries.md)

* **Handmatig**: Handmatige fouten zijn handmatig toegevoegd aan de onderdrukkingslijst. [Meer informatie](#add-addresses-and-domains)

Voor elk e-mailadres dat wordt vermeld, kunt u ook de **[!UICONTROL Type]** (e-mail of domein), **[!UICONTROL Reason]** om het uit te sluiten, die het toevoegde, en de datum/tijd het aan de onderdrukkingslijst werd toegevoegd.

![](assets/suppression-list.png)

Mogelijke oorzaken voor een mislukking van de levering zijn:

| Reden | Beschrijving | Categorie |
| --- | --- | --- |
| **[!UICONTROL Invalid Recipient]** | De ontvanger is ongeldig of bestaat niet. | Hard |
| **[!UICONTROL Soft Bounce]** | De berichtzachte die tegen een andere reden dan de zachte fouten in deze lijst worden vermeld, zoals wanneer het verzenden over het toegestane tarief door ISP wordt geadviseerd. | Zacht |
| **[!UICONTROL DNS Failure]** | Het bericht dat als gevolg van een DNS-fout is teruggestuurd. | Zacht |
| **[!UICONTROL Mailbox Full]** | Het bericht dat door de brievenbus van de ontvanger wordt teruggestuurd die volledig is en niet meer berichten kan goedkeuren. | Zacht |
| **[!UICONTROL Relaying Denied]** | Het bericht is geblokkeerd door de ontvanger omdat het opnieuw afspelen niet is toegestaan. | Zacht |
| **[!UICONTROL Challenge-Response]** | De boodschap is een uitdaging-antwoord sonde. | Zacht |
| **[!UICONTROL Spam Complaint]** | Het bericht werd geblokkeerd omdat duidelijk als spam door de ontvanger. | Hard |

>[!NOTE]
>
>Niet-geabonneerde gebruikers ontvangen geen e-mails van [!DNL Journey Optimizer]Daarom kunnen hun e-mailadressen niet naar de onderdrukkingslijst worden verzonden. Hun keuze wordt op het niveau van de Experience Platform behandeld. [Meer informatie over opt-out](../privacy/opt-out.md)


### Regels voor onderdrukking  {#suppression-rules}

Van de **[!UICONTROL Suppression list]** kunt u ook de parameter retry bewerken die is gekoppeld aan de onderdrukkingsregels in het menu **[!UICONTROL Edit suppression rules]** knop. Gebruik deze optie om de drempel voor opnieuw proberen voor de huidige zandbak bij te werken. [Meer informatie over pogingen](retries.md).


## Voeg adressen en domeinen aan de onderdrukkingslijst toe{#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_header"
>title="E-mails of domeinen toevoegen aan de onderdrukkingslijst"
>abstract="U kunt de lijst met Journey Optimizer-suppressies handmatig invullen om specifieke e-mailadressen en/of domeinen van uw verzending uit te sluiten."

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="E-mails of domeinen toevoegen aan de onderdrukkingslijst"
>abstract="Als u de lijst met onderdrukking wilt vullen, kunt u handmatig e-mailadressen of domeinen toevoegen: één voor één, of in bulkwijze door een Csv- dossierupload. Deze specifieke e-mailadressen en/of domeinen worden van uw verzending uitgesloten."

Wanneer een bericht niet aan een e-mailadres kan worden geleverd, wordt dit adres automatisch toegevoegd aan de suppressielijst die op de bepaalde suppressieregel of stuiterende telling wordt gebaseerd.

U kunt de opdracht [!DNL Journey Optimizer] suppressielijst om specifieke e-mailadressen en/of domeinen van uw verzending uit te sluiten.

>[!NOTE]
>
>Het kan tot 60 minuten duren [!DNL Journey Optimizer] om rekening te houden met de onderdrukte adressen in uitgaande e-mails.

U kunt e-mailadressen of domeinen toevoegen [één voor één](#add-one-address-or-domain), of [in bulkmodus](#upload-csv-file) via een CSV-bestandsupload.

### Eén adres of domein toevoegen {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="Eén item toevoegen aan de onderdrukkingslijst"
>abstract="U kunt de suppressielijst vullen door e-mailadressen en/of domeinen een voor een toe te voegen."

Voer de onderstaande stappen uit om een e-mailadres of domein toe te voegen aan de lijst met onderdrukking:

1. Selecteer de knop **[!UICONTROL Add email or domain]**.

   ![](assets/suppression-list-add-email.png)

1. Kies de optie **[!UICONTROL One by one]**.

   ![](assets/suppression-list-add-email-address.png)

1. Selecteer het adrestype: **[!UICONTROL Email]** of **[!UICONTROL Domain]**.

1. Voer het e-mailadres of domein in dat u van uw verzending wilt uitsluiten.

   >[!NOTE]
   >
   >Zorg ervoor dat u een geldig e-mailadres (zoals abc@company.com) of domein (zoals abc.company.com) opgeeft.

1. (optioneel) Voer een reden in. Alle afdrukbare ASCII-tekens tussen 32 en 126 zijn toegestaan in dit veld.

1. Gebruik de **[!UICONTROL Submit]** ter bevestiging.

### Een CSV-bestand uploaden {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="CSV uploaden om items toe te voegen aan de onderdrukkingslijst"
>abstract="U kunt de suppressielijst vullen door een CSV-bestand te uploaden dat is ingevuld met de e-mailadressen/domeinen die u wilt uitsluiten."

Voer de onderstaande stappen uit om een groep e-mailadressen of domeinen toe te voegen aan de lijst met onderdrukking:

1. Selecteer de knop **[!UICONTROL Add email or domain]**.
1. Kies de optie **[!UICONTROL Upload CSV]**.

   ![](assets/suppression-list-upload-csv.png)

1. Download de CSV-sjabloon die u wilt gebruiken, inclusief de onderstaande kolommen en indeling:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```

1. Vul de CSV-sjabloon in met de e-mailadressen en/of domeinen die u wilt toevoegen aan de suppressielijst. Alle ASCII-afdrukbare tekens tussen 32 en 126 zijn toegestaan in het dialoogvenster **OPMERKING** kolom.

   >[!CAUTION]
   >
   >Wijzig de naam van de kolommen in de CSV-sjabloon niet.
   >
   >De bestandsgrootte mag niet groter zijn dan 1 MB.

1. Als u klaar bent, sleept u het CSV-bestand en gebruikt u de **[!UICONTROL Submit]** ter bevestiging.

   ![](assets/suppression-list-upload-csv-submit.png)

Wanneer het uploaden is voltooid, kunt u de status controleren via de [Recente uploads](#recent-uploads) zoals hieronder beschreven.

### Status van uploaden controleren {#recent-uploads}

Gebruik de **[!UICONTROL Recent uploads]** om de status van de meest recente geüploade CSV-bestanden te controleren.

![](assets/suppression-list-recent-uploads-button.png)

Mogelijke statussen zijn:

* **[!UICONTROL Pending]**: De bestandsupload wordt verwerkt.
* **[!UICONTROL Error]**: Het uploaden van het bestand is mislukt als gevolg van een technische fout of een fout in de bestandsindeling.
* **[!UICONTROL Complete]**: Het uploaden van het bestand is voltooid.

Als tijdens het uploaden sommige adressen niet in het correcte formaat zijn, worden zij niet toegevoegd aan [!DNL Journey Optimizer] suppressielijst.

In dat geval, wanneer uploaden volledig is, wordt het geassocieerd met een rapport. U kunt het downloaden om de fouten te controleren<!-- and understand why they were not added to the suppression list-->.

![](assets/suppression-list-recent-uploads-report.png)

Hieronder ziet u een voorbeeld van het type items dat u kunt vinden in het foutrapport:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```

## Een adres uit de lijst met onderdrukking verwijderen{#remove-from-suppression-list}

U kunt de onderdrukkingslijst handmatig bijwerken. Het verwijderen van een e-mailadres uit quarantaine is een gevoelige verrichting en kan uw IP reputatie en leverbaarheidstarieven beïnvloeden. Wees voorzichtig.

Wanneer u een e-mailadres of domein uit de suppressielijst verwijdert, kan Adobe Journey Optimizer opnieuw beginnen met het leveren aan dit adres of domein.  Meer informatie over leverbaarbaarheid in [deze sectie](../reports/deliverability.md).

Als u een adres uit de lijst met onderdrukking wilt verwijderen, gebruikt u de opdracht **[!UICONTROL Delete]** knop.

![](assets/suppression-list-delete.png)


>[!NOTE]
>
>Ga voorzichtig te werk wanneer u overweegt een e-mailadres of domein te verwijderen. Neem in geval van twijfel contact op met een leverancier.


Bijvoorbeeld in het geval van een stroomonderbreking van Internet Service Provider (ISP), kunnen de e-mails verkeerd als harde grenzen worden gemerkt omdat zij niet met succes aan hun ontvanger kunnen worden geleverd. Deze e-mailadressen moeten uit de onderdrukkingslijst worden verwijderd.

Om dit te doen, filter de suppressielijst aan vertoningsbeïnvloede e-mailadressen of domeinen. Bijvoorbeeld als een ISP stroomonderbreking van 11 Nov, 2022 aan 13 Nov, 2022 op **test.com** -domein, filtert u de adressen die in die tijdlijn aan de suppressielijst zijn toegevoegd, zoals hieronder:

![](assets/remove-from-supp-list.png)

U moet ook een filter op het type van stuit toevoegen, afhankelijk van de details van de stroomonderbreking. Deze details worden verstrekt door ISP, zoals de nauwkeurige foutencode die aan de afzender is teruggekeerd. Bijvoorbeeld: `550 <email address> recipient rejected` of `550 5.1.1 ‘email address’: user lookup success but no user record found`.

Zodra geïdentificeerd, kunnen deze adressen manueel uit de onderdrukkingslijst worden verwijderd gebruikend **[!UICONTROL Delete]** knop. Deze adressen kunnen dan in toekomstige e-mailcampagnes worden omvat.

## De suppressielijst downloaden {#download-suppression-list}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_download"
>title="Export the list as a CSV file"
>abstract="To download the suppression list, you can either export the current list by generating a new file, or download the file that was previously generated."
-->

Voer de volgende stappen uit om de lijst met onderdrukking als een CSV-bestand te exporteren:

1. Selecteer de knop **[!UICONTROL Download CSV]**.

   ![](assets/suppression-list-download-csv.png)

1. Wacht tot het bestand is gegenereerd.

   ![](assets/suppression-list-download-generate.png)

   >[!NOTE]
   >
   >De downloadtijd is afhankelijk van de bestandsgrootte. Dit houdt in dat het aantal adressen in de lijst met downloads wordt weergegeven.
   >
   >Voor een bepaalde sandbox kan één downloadverzoek tegelijkertijd worden verwerkt.

1. Nadat het bestand is gegenereerd, ontvangt u een melding. Klik op het belpictogram rechtsboven op het scherm om het scherm weer te geven.

1. Klik op de melding zelf om het bestand te downloaden.

   ![](assets/suppression-list-download-notification.png)

   >[!NOTE]
   >
   >De koppeling is 24 uur geldig.

<!--When downloading the CSV file, you can choose to either:

* Download the file that was previously generated by another user or yourself.

* Generate a new file in order to export the current suppression list.-->