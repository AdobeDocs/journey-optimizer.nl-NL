---
solution: Journey Optimizer
product: journey optimizer
title: Overschakelen naar donkere modus
description: Meer informatie over het gebruik van de donkere modus in de Designer-e-mail
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: donkere modus, e-mail, kleur, editor
hide: true
hidefromtoc: true
exl-id: 27442cb0-5027-4d9c-9d3c-9ec33af7c9ff
source-git-commit: b5d9b9c26824517414982fa539e0b360500cafc6
workflow-type: tm+mt
source-wordcount: '1679'
ht-degree: 0%

---

# Inhoud in de donkere modus beheren {#dark-mode}

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode"
>title="Overschakelen naar donkere modus"
>abstract="Schakel over naar de donkere modus waar u een voorvertoning kunt bekijken van de manier waarop specifieke aangepaste instellingen worden gerenderd en gedefinieerd. <br> Voorzichtigheid: Het definitieve teruggeven hangt van de e-mailcliënt van de ontvanger af. Niet alle e-mailclients ondersteunen de aangepaste donkere modus."

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_image"
>title="Een specifieke afbeelding gebruiken voor de donkere modus"
>abstract="U kunt een andere afbeelding selecteren die wordt weergegeven wanneer de donkere modus is ingeschakeld. <br> Voorzichtigheid: Het toevoegen van een specifiek beeld voor donkere wijze waarborgt het niet correct in alle e-mailcliënten teruggeeft. Niet alle e-mailclients ondersteunen de aangepaste donkere modus."

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_preview"
>title="Overschakelen naar donkere modus"
>abstract="Schakel over naar de donkere modus om te bekijken hoe deze kan worden weergegeven bij ondersteunde e-mailclients. <br> Voorzichtigheid: Het definitieve teruggeven hangt van de e-mailcliënt van de ontvanger af. Niet alle e-mailclients ondersteunen de aangepaste donkere modus."

Wanneer het ontwerpen van uw e-mails, [!DNL Journey Optimizer] [ E-mail Designer ](get-started-email-design.md) staat u toe om aan **[!UICONTROL Dark mode]** te schakelen waar u specifieke douanemontages kunt bepalen. Wanneer de donkere modus is ingeschakeld, geven de ondersteunende e-mailclients de instellingen weer die u voor deze modus hebt gedefinieerd.

>[!WARNING]
>
>De uiteindelijke rendering in de donkere modus is afhankelijk van de e-mailclient van de ontvanger.
>
>Niet alle e-mailclients ondersteunen de aangepaste donkere modus. <!--[See the list](#non-supporting-email-clients)--> Bovendien, passen sommige e-mailcliënten slechts hun eigen standaard donkere wijze voor alle e-mails toe die worden ontvangen. In dit geval kunnen de aangepaste instellingen die u in de e-mailtoepassing hebt gedefinieerd, niet worden weergegeven.

Een lijst van de e-mailcliënten die donkere wijze steunen wordt voorgesteld in [ deze sectie ](#supporting-email-clients).

## Wat is de donkere modus? {#what-is-dark-mode}

In de donkere modus kunnen ondersteunde e-mailclients en apps e-mails weergeven met donkere achtergronden en lichtere kleuren voor tekst, knoppen en andere UI-elementen. Hierdoor kan de belasting van het oog worden verminderd, de levensduur van de batterij worden bespaard en de leesbaarheid in omgevingen met weinig licht worden verbeterd voor een comfortabeler kijkervaring.

<!--Dark Mode uses a dark color palette with light text and UI elements to reduce eye strain, save battery life, and improve readability in low-light environments.-->

Als een groeiende trend in grote besturingssystemen en apps (Apple Mail, Gmail, Outlook, Twitter, Slack), is het een belangrijke overweging geworden in het moderne e-mailontwerp om ervoor te zorgen dat inhoud leesbaar blijft en visueel aantrekkelijk voor alle gebruikers.

Het is echter niet mogelijk te garanderen dat uw e-mail er op alle apparaten in donkere modus precies hetzelfde uitziet. Sommige visuele wijzigingen kunnen ook worden veroorzaakt door de e-mailtoepassing of het apparaat waarmee het originele ontwerp wordt overschreven.

De manier waarop de donkere modus wordt toegepast door e-mailclients kan namelijk als volgt variëren <!--between different devices and apps--> :

* Deze functie wordt niet door alle e-mailclients ondersteund.

  >[!NOTE]
  >
  >Een lijst van de e-mailcliënten die donkere wijze niet steunen wordt voorgesteld in [ deze sectie ](#non-supporting-email-clients).

* Sommige e-mailclients passen kleuren, achtergronden en afbeeldingen automatisch aan. Als u in dit geval aangepaste instellingen definieert in de e-mail-Designer, worden deze instellingen waarschijnlijk niet weergegeven.

* Andere e-mailclients geven de optie om de aangepaste donkere modus te renderen (bijvoorbeeld met de methode `@media (prefers-color-scheme: dark)` ). In dit geval moeten de specifieke instellingen die u in de e-mailtoepassing van de Designer definieert, worden weergegeven. Leer hoe te om de montages van de douane donkere wijze in E-mail Designer in [ te bepalen deze sectie ](#define-custom-dark-mode).

## Donkere modus in de Designer-e-mail {#dark-mode-email-designer}

Wat de donkere modus in de e-mailtoepassing Designer betreft, moet u rekening houden met twee aspecten:

* U kunt een voorvertoning weergeven van hoe de standaard donkere modus wordt weergegeven in de meeste ondersteunde e-mailclients. [Meer informatie](#preview-dark-mode)

<!--
    >[!CAUTION]
    >
    >The final rendering may vary according to the recipient's email client. To see the exact rendering for each email client, use the [Email rendering](../content-management/rendering.md) option.-->

* Als u de standaardinstellingen voor het ondersteunen van e-mailclients wilt overschrijven, kunt u aangepaste instellingen voor de donkere modus definiëren die van toepassing zijn op de e-mail die u bewerkt. [Meer informatie](#define-custom-dark-mode)

<!--
    >[!WARNING]
    >
    >Not all email clients support custom dark mode. Some email clients only apply their own default dark mode for all emails that are received. In this case, the custom settings that you defined in the Email Designer cannot be rendered. [Learn more](#guardrails)-->

### Standaardmodus voor donker voorvertonen {#preview-dark-mode}

Volg onderstaande stappen om de donkere modus te openen in de E-mail-Designer en een voorbeeld te bekijken van de standaard donkere modusinstellingen.

1. Selecteer de optie **[!UICONTROL Design from scratch]** op de homepage van Designer via e-mail. [Meer informatie](content-from-scratch.md)

   >[!NOTE]
   >
   >Momenteel kunt u niet op donkere wijze kunnen schakelen als u een [ e-mailmalplaatje ](use-email-templates.md) selecteert of als u a [ thema ](apply-email-themes.md) toepast.

1. Voeg [ structuren ](content-from-scratch.md) en [ inhoudcomponenten ](content-components.md) aan uw inhoud toe.

1. Rechtsboven op het centrale canvas schakelt u de schakeloptie over naar **[!UICONTROL Dark mode]** .

   ![](assets/light-mode-toggle.png)

1. De standaardvoorvertoning in de donkere modus wordt weergegeven.

   ![](assets/dark-mode-default.png)
<!--
    >[!NOTE]
    >
    >Dark mode applies to all elements, except images and icons.-->

Standaard wordt in de voorvertoning van de donkere modus van e-mail Designer het kleurschema &#39;full color invert&#39; toegepast op alle elementen behalve afbeeldingen en pictogrammen. <!--It fully inverts all colors for all the elements (texts, buttons, etc.)-->

Het betekent dat gebieden met lichte en donkere elementen worden gedetecteerd en omgekeerd, zodat de lichte achtergronden donker worden en donkere tekst licht, terwijl donkere achtergronden licht worden en lichte tekst donker wordt.

>[!CAUTION]
>
>De uiteindelijke rendering kan variëren afhankelijk van de e-mailclient van de ontvanger. Om een simulatie te zien die zo dicht mogelijk bij het definitieve resultaat voor elke e-mailcliënt komt, gebruik de [ E-mail teruggevende ](../content-management/rendering.md) optie.

<!--This is custom dark mode:

  ![](assets/dark-mode-custom.png)

Here you can see that we have applied a different background, defined another image and change the color of the text and button.-->

### Aangepaste donkere modus definiëren {#define-custom-dark-mode}

Nadat u naar **[!UICONTROL Dark mode]** hebt overgeschakeld, kunt u specifieke opmaakelementen van uw inhoud bewerken die alleen worden weergegeven wanneer de donkere modus is ingeschakeld in de e-mailclient van de ontvanger - op voorwaarde dat deze functie wordt ondersteund.

>[!WARNING]
>
>Niet alle e-mailclients ondersteunen de donkere modus. Bovendien passen sommige e-mailclients alleen hun eigen standaard donkere modus toe op alle ontvangen e-mails. In beide gevallen kunnen de aangepaste instellingen die u in de e-mailtoepassing hebt gedefinieerd, niet worden weergegeven.

Als u de aangepaste stijl voor de donkere modus van Designer via e-mail wilt gebruiken, gebruikt Journey Optimizer de <!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` CSS-query, die detecteert of de e-mailclient van de gebruiker is ingesteld op de donkere modus en past het donkere ontwerp toe dat in de e-mail is gedefinieerd.

Volg onderstaande stappen om aangepaste instellingen voor de donkere modus te definiëren.

1. Zorg ervoor dat **[!UICONTROL Dark mode]** is ingeschakeld in de e-mailtoepassing van de Designer. [ leer hoe ](#preview-dark-mode)

1. Bewerk alle opmaakkleurkenmerken, zoals tekst, achtergronden, knoppen, enz.

1. U kunt de kleuren van afbeeldingen en pictogrammen niet wijzigen, maar u kunt wel specifieke elementen alleen voor de donkere modus definiëren. Selecteer een afbeelding om dit te doen. Schakel over naar **[!UICONTROL Dark mode]** met de specifieke schakeloptie in het deelvenster **[!UICONTROL Settings]** en selecteer een ander element.

   ![](assets/dark-mode-image.png)

   <!--![](assets/dark-mode-custom.png)-->

1. U kunt op elk gewenst moment **[!UICONTROL Switch to live view]** gebruiken om te controleren hoe uw inhoud op verschillende apparaatgrootten wordt gerenderd. Selecteer in deze weergave de optie Donkere modus boven op het scherm om een voorvertoning weer te geven van de donkere modusversie van de inhoud op de verschillende apparaten.

   ![](assets/dark-mode-live-view.png){width="80%" align="center"}

   >[!CAUTION]
   >
   >De live weergave is een algemene voorvertoning die is ontworpen om te vergelijken hoe de rendering er tussen verschillende apparaatgrootten uitziet. De uiteindelijke rendering kan variëren afhankelijk van de e-mailclient van de ontvanger.

1. Als u tevreden bent met de wijzigingen in de donkere modus, klikt u op **[!UICONTROL Simulate content]** .

   ![](assets/dark-mode-simulate.png)

1. Selecteer **[!UICONTROL Render email]** en verbind met uw rekening van de NLS. U ziet de uiteindelijke donkere modus voor verschillende e-mailclients. Leer meer op [ E-mail teruggevend ](../content-management/rendering.md).

   >[!WARNING]
   >
   >Hoewel de simulatie nauwkeurig benadert hoe e-mails worden weergegeven in de donkere modus, kan de werkelijke rendering afwijken als gevolg van verschillen in e-mailserviceproviders of instellingen op apparaatniveau.

## Best practices {#best-practices}

Aangezien de donkere wijzetoepassing over belangrijke e-mailcliënten stijgt, is het essentieel om te overwegen hoe uw e-mail in zowel lichte als donkere milieu&#39;s teruggeeft - of u [ douane donkere wijze ](#define-custom-dark-mode) of niet gebruikt.

In de donkere modus kunt u kleuren, achtergronden en afbeeldingen wijzigen. Soms worden ontwerpkeuzen genegeerd. Volg de onderstaande aanbevolen procedures om de visuele consistentie, toegankelijkheid en brandintegriteit te garanderen.

**optimaliseer uw beelden en logo&#39;s**

* Vermijd afbeeldingen met een hardcodeerde witte of lichte achtergrond.

* Sla logo&#39;s en pictogrammen op als PNG&#39;s met transparante achtergronden om zichtbare witte vakken in de donkere modus te voorkomen.

* Als transparantie geen optie is, plaatst u afbeeldingen op een effen achtergrond in uw ontwerp om ongewenste kleurinversies te voorkomen.

**bekijk uw achtergronden**

* Zorg voor voldoende contrast tussen tekst en achtergrondkleuren voor leesbaarheid in zowel de lichte als de donkere modus.

* Vertrouw niet alleen op achtergrondkleuren voor essentiële inhoud. Sommige clients overschrijven achtergrondkleuren in de donkere modus, zodat de belangrijkste gegevens nog steeds zichtbaar zijn.

**Ontwerp toegankelijke inhoud op donkere wijze**

* Gebruik kleurcombinaties die u gemakkelijk kunt herkennen voor mensen met kleurenblindheid.

* Gebruik een palet met middentonen om contrast tegen zowel lichte als donkere achtergronden te waarborgen.

* Gebruik toegankelijke kleurcombinaties met hoog contrast om de leesbaarheid te verbeteren en te voldoen aan de WCAG-standaarden (Web Content Accessibility Guidelines). Gebruik gereedschappen zoals de Contrast Checker van WebAIM om het kleurcontrast te controleren.

* Vermijd dunne lettertypen omdat dit van invloed is op de leesbaarheid. Als uw merk een dun lettertype nodig heeft, kunt u het vet in de donkere modus drukken.

* Overslaan puur wit op puur zwart, omdat dit oogbelasting kan veroorzaken en door sommige e-mailclients automatisch kan worden omgekeerd.

* Maak toegankelijke fallback-stijlen als de donkere modus niet wordt ondersteund.

**Test uw e-mails op donkere wijzemilieu**

* Gebruik de e-mail Designer [ donkere wijzevoorproef ](#preview-dark-mode) die omgekeerde kleurenschema&#39;s aan vlekkwesties vroeg gebruikt.

* Gebruik de [ E-mail die ](../content-management/rendering.md) optie teruggeeft die hefboomwerkingen Litmus om uw ontwerpen over belangrijke e-mailcliënten (de Post van Apple, Gmail, Vooruitzichten) te simuleren en te zien hoe de kleuren en de beelden zich op donkere wijze gedragen.

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->

## E-mailclients die donkere modus ondersteunen {#supporting-email-clients}

Hieronder volgt een lijst met de belangrijkste e-mailclients die donkere modus ondersteunen. Sommige versies van de vermelde e-mailclients bieden echter geen ondersteuning voor de donkere modus, zodat deze versies ook ter wille van de duidelijkheid en nauwkeurigheid in deze tabel worden weergegeven.

>[!WARNING]
>
>De uiteindelijke rendering in de donkere modus is afhankelijk van elke e-mailclient. De resultaten kunnen dus per e-mailclient verschillen. Om een simulatie te zien die zo dicht mogelijk bij het definitieve resultaat voor elke e-mailcliënt komt, gebruik de [ E-mail teruggevende ](../content-management/rendering.md) optie.

| E-mailclients die donkere modus ondersteunen | Compatibele versies | Niet-ondersteunde versies |
|---------|----------|---------|
| Apple Mail macOS | 12.4, 16.0 | *10.3* |
| Apple Mail iOS | 13.0, 16.1 | *12.2* |
| Outloook macOS | 2019, 16.70, 16.80 uur | NA |
| Outlook.com | 2019-07, 2022-12 | NA |
| Outloook iOS | 2020-01, 2022-12 | NA |
| Outloook Android | 2023-03 | *2020-01, 2022-12* |
| Samsung Email (Android) | 6,1 | *6.0* |
| Mozilla Thundervogel (macOS) | 68,4 | *60.8, 78.5, 91.13* |
| Fastmail (bureaublad-webmail) | 2022-12 | *2021-07* |
| HEY (bureaublad-webmail) | 2020-06 | *2022-12* |
| Webmail over oranje bureaublad | 2019-08, 2021-03, 2022-12, 2024-04 | NA |
| Oranje iOS | 2022-12, 2024-04 | *2020-01* |
| Oranje Android | 2024-04 | *2020-01, 2022-12* |
| LaPoste.net | 2021-08, 2022-12 | NA |
| SFR Desktop Webmail | 2019-08, 2022-12 | NA |
| GMX (iOS en Android) | 2022-06 | NA |
| 1&amp;1 (Desktop Webmail en Android) | 2022-06 | NA |
| WEB.DE (iOS en Android) | 2022-06 | NA |
| Free.fr | 2022-12 | NA |

<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

## E-mailclients die geen donkere modus ondersteunen {#non-supporting-email-clients}

Sommige e-mailclients staan gebruikers toe hun interface te schakelen naar de donkere modus, maar deze instelling heeft geen invloed op de manier waarop HTML-e-mails worden weergegeven. Ongeacht of de interface in lichte of donkere modus is, wordt hetzelfde weergegeven in uw e-mail. Hier volgt een lijst met deze clients:

| E-mailclients die geen donkere modus ondersteunen |
|---------|
| Gmail (desktopwebmail, iOS, Android, mobiele webmail) |
| Outlook Windows |
| Outlook Windows Mail |
| Yahoo!Mail |
| AOL |
| ProtonMail |
| SFR iOS |
| SFR Android |
| GMX Desktop Webmail |
| Mail.ru |
| Webmail WEB.DE-desktop |
| T-online.de |
