---
title: De vervolgkeuzelijst beheren
description: Leer hoe u de lijst met Journey Optimizer-suppressies kunt openen en beheren
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# De vervolgkeuzelijst beheren {#manage-suppression-list}

Met [!DNL Journey Optimizer], kunt u alle e-mailadressen controleren die automatisch van het verzenden van een reis worden uitgesloten, zoals:

* Adressen die ongeldig zijn (harde grenzen).
* Verwerkt deze voortdurend zachte stuit en kan een negatief effect hebben op de reputatie van uw e-mail als u deze blijft opnemen in uw leveringen.
* Ontvangers die op een of andere manier een spamklacht indienen tegen een van uw e-mailberichten.

Dergelijke e-mailadressen worden automatisch verzameld in de Journey Optimizer **onderdrukkingslijst**. Meer informatie over het concept en het gebruik van de suppressielijst in [deze sectie](../reports/suppression-list.md).

U kunt ook [**handmatig** een adres of domein toevoegen](#add-addresses-and-domains) aan de onderdrukkingslijst.

>[!NOTE]
>
>Het duurt tussen 0 en 60 minuten [!DNL Journey Optimizer] om rekening te houden met de onderdrukte adressen in uitgaande e-mails.

## De lijst met onderdrukking openen {#access-suppression-list}

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** en selecteert u **[!UICONTROL Suppression list]**.

>[!CAUTION]
>
>Machtigingen voor het weergeven, exporteren en beheren van de suppressielijst zijn beperkt tot [Reisbeheerders](../administration/ootb-product-profiles.md#journey-administrator). Meer informatie over beheren [!DNL Journey Optimizer] toegangsrechten van gebruikers in [deze sectie](../administration/permissions-overview.md).

![](assets/suppression-list-access.png)

Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren.

![](assets/suppression-list-filters.png)

U kunt filteren op de **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]**, of **[!UICONTROL Reason]**. Selecteer de optie(s) van uw keuze voor elk criterium. Als deze optie is geselecteerd, kunt u elk filter of alle filters die boven op de lijst worden weergegeven, wissen.

![](assets/suppression-list-filtering-example.png)

Als u per ongeluk handmatig een e-mailadres of een domein toevoegt, **[!UICONTROL Delete]** kunt u dat item verwijderen.

>[!CAUTION]
>
>Gebruik nooit de **[!UICONTROL Delete]** om onderdrukte e-mailadressen of domeinen te verwijderen.

![](assets/suppression-list-delete.png)

Als u een e-mailadres of een domein uit de suppressielijst verwijdert, wordt opnieuw begonnen met het leveren aan dit adres of domein. Dientengevolge, kan dit ernstige gevolgen op uw leverbaarheid en IP reputatie hebben, die uiteindelijk tot uw IP adres of verzendend domein zou kunnen leiden die worden geblokkeerd. Lees meer over het belang van het bijhouden van een onderdrukkingslijst in [deze sectie](../reports/suppression-list.md).

>[!NOTE]
>
>Ga voorzichtig te werk wanneer u overweegt een e-mailadres of domein te verwijderen. Neem in geval van twijfel contact op met een leverancier.

Van de **[!UICONTROL Suppression list]** kunt u ook de onderdrukkingsregels bewerken. [Meer informatie](retries.md)

Als u de onderdrukkingslijst wilt exporteren als een CSV-bestand, selecteert u de optie **[!UICONTROL Download CSV]** knop.

![](assets/suppression-list-download-csv.png)

## Onderdrukkingscategorieën en redenen {#suppression-categories-and-reasons}

Wanneer een bericht niet aan een e-mailadres kan worden bezorgd, [!DNL Journey Optimizer] bepaalt waarom de levering ontbrak en het met een associeert **[!UICONTROL Suppression category]**.

De onderdrukkingscategorieën zijn als volgt:

* **Hard**: Het e-mailadres wordt direct naar de onderdrukkingslijst verzonden.

   >[!NOTE]
   >
   >Wanneer de fout het resultaat van een spamklacht is, valt het ook in **Hard** categorie. Het e-mailadres van de ontvanger die de klacht heeft ingediend, wordt onmiddellijk naar de onderdrukkingslijst gezonden.

* **Zacht**: Zachte fouten verzenden een adres naar de onderdrukkingslijst zodra de foutenteller de grensdrempel bereikt. [Meer informatie over opnieuw proberen](retries.md)

* **Handmatig**: U kunt ook handmatig een e-mailadres of een domein toevoegen aan de lijst met onderdrukking. [Meer informatie](#add-addresses-and-domains)

>[!NOTE]
>
>Meer informatie over zachte grenzen en harde golven in de [Typen leveringsfouten](../reports/suppression-list.md#delivery-failures) sectie.

Voor elk e-mailadres dat wordt vermeld, kunt u ook de **[!UICONTROL Type]** (e-mail of domein), **[!UICONTROL Reason]** om het uit te sluiten, die het toevoegde, en de datum/tijd het aan de onderdrukkingslijst werd toegevoegd.

![](assets/suppression-list.png)

De mogelijke redenen van een leveringsfout zijn:

| Reden | Beschrijving | Onderdrukkingscategorie |
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
>Niet-geabonneerde gebruikers ontvangen geen e-mails van [!DNL Journey Optimizer]Daarom kunnen hun e-mailadressen niet naar de onderdrukkingslijst worden verzonden. Hun keuze wordt op het niveau van de Experience Platform behandeld. [Meer informatie over opt-out](../messages/consent.md)

## Voeg handmatig adressen en domeinen toe {#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_header"
>title="E-mails of domeinen toevoegen aan de onderdrukkingslijst"
>abstract="U kunt de lijst met Journey Optimizer-suppressies handmatig invullen om specifieke e-mailadressen en/of domeinen van uw verzending uit te sluiten."

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="E-mails of domeinen toevoegen aan de onderdrukkingslijst"
>abstract="U kunt de Journey Optimizer-suppressielijst handmatig invullen om specifieke e-mailadressen en/of domeinen van uw verzending uit te sluiten."

<!--New contextual help content for September release:
To populate the Journey Optimizer suppression list, you can manually add email addresses or domains - one at a time, or in bulk mode through a CSV file upload. These specific email addresses and/or domains will be excluded from your sending.-->

Wanneer een bericht niet aan een e-mailadres kan worden geleverd, wordt dit adres automatisch toegevoegd aan de suppressielijst die op de bepaalde suppressieregel of stuiterende telling wordt gebaseerd.

U kunt de opdracht [!DNL Journey Optimizer] suppressielijst om specifieke e-mailadressen en/of domeinen van uw verzending uit te sluiten.

U kunt e-mailadressen of domeinen toevoegen [één voor één](#add-one-address-or-domain), of [in bulkmodus](#upload-csv-file) via een CSV-bestandsupload.

Selecteer hiervoor de optie **[!UICONTROL Add email or domain]** en voert u een van de onderstaande methoden uit.

![](assets/suppression-list-add-email.png)

### Eén adres of domein toevoegen {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="Eén item toevoegen aan de onderdrukkingslijst"
>abstract="U kunt de suppressielijst vullen door e-mailadressen en/of domeinen een voor een toe te voegen."

1. Selecteer **[!UICONTROL One by one]** optie.

   ![](assets/suppression-list-add-email-address.png)

1. Kies het adrestype: **[!UICONTROL Email address]** of **[!UICONTROL Domain address]**.

1. Voer het e-mailadres of domein in dat u van uw verzending wilt uitsluiten.

   >[!NOTE]
   >
   >Zorg ervoor dat u een geldig e-mailadres (zoals abc@company.com) of domein (zoals abc.company.com) opgeeft.

1. Geef indien nodig een reden op.

   >[!NOTE]
   >
   >Alle ASCII-tekens tussen 32 en 126 zijn toegestaan in het dialoogvenster **[!UICONTROL Reason]** veld. De volledige lijst is te vinden op [deze pagina](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target=&quot;_blank&quot;} bijvoorbeeld.

1. Klik op **[!UICONTROL Submit]**.

### Een CSV-bestand uploaden {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="CSV uploaden om items toe te voegen aan de onderdrukkingslijst"
>abstract="U kunt de suppressielijst vullen door een CSV-bestand te uploaden dat is ingevuld met de e-mailadressen/domeinen die u wilt uitsluiten."

1. Selecteer **[!UICONTROL Upload CSV]** optie.

   ![](assets/suppression-list-upload-csv.png)

1. Download de CSV-sjabloon die u wilt gebruiken, inclusief de onderstaande kolommen en indeling:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```
   >[!NOTE]
   >
   >Alle ASCII-tekens tussen 32 en 126 zijn toegestaan in het dialoogvenster **Opmerking** kolom. De volledige lijst is te vinden op [deze pagina](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target=&quot;_blank&quot;} bijvoorbeeld.

   U kunt deze sjabloon ook downloaden via het menu **[!UICONTROL Suppression list]** hoofdweergave.

   >[!CAUTION]
   >
   >Wijzig de namen van de kolommen in de CSV-sjabloon niet.
   >
   >De bestandsgrootte mag niet groter zijn dan 1 MB.

1. Vul de CSV-sjabloon in met de e-mailadressen en/of domeinen die u wilt toevoegen aan de suppressielijst.

1. Wanneer u klaar bent, sleept u het CSV-bestand en klikt u op **[!UICONTROL Submit]**.

   ![](assets/suppression-list-upload-csv-submit.png)

>[!NOTE]
>
>Zodra uploaden wordt gedaan, zorg ervoor het door zijn status van de interface te controleren succesvol was. [Meer informatie](#recent-uploads)

### Status van recente uploads controleren {#recent-uploads}

U kunt de lijst controleren van de recentste CSV dossiers u uploadde.

Om dit te doen, van **[!UICONTROL Suppression list]** klik op de knop **[!UICONTROL Recent uploads]** knop.

![](assets/suppression-list-recent-uploads-button.png)

De meest recente uploads die u hebt verzonden en de bijbehorende statussen worden weergegeven.

Als een foutenrapport met een dossier wordt geassocieerd, kunt u het downloaden om de gevonden fouten te controleren.

![](assets/suppression-list-recent-uploads-error.png)

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
