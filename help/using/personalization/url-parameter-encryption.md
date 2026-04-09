---
solution: Journey Optimizer
product: journey optimizer
title: URL-parameters versleutelen
description: Leer hoe te om gevoelige URL vraagparameters te coderen zodat PII niet in duidelijke teksten op Journey Optimizer het volgen verbindingen en het landen pagina's wordt blootgesteld.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="Beperkte beschikbaarheid" type="Informative"
keywords: codering, URL, bijhouden, landingspagina, sleutelregister, personalisatie, beveiliging, privacy, sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: 5c8d615b5f6b2c2cb80a21c59f3ea5f12325e6fd
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# URL-parameters versleutelen {#url-parameter-encryption}

>[!AVAILABILITY]
>
>Deze functie is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.
>
>Deze mogelijkheid is momenteel alleen beschikbaar voor het e-mailkanaal.

## Waarom URL-parametercodering gebruiken? {#why-url-parameter-encryption}

De gepersonaliseerde het volgen verbindingen en het landen pagina URLs omvatten vaak profielattributen, herkenningstekens, tekenen, of andere waarden in het vraagkoord. Deze parameters zijn doorgaans zichtbaar als onbewerkte tekst in de e-mail of SMS en ze blijven leesbaar als iemand de koppeling kopieert, deelt of bladwijzers geeft. Dit kan een veiligheid en privacyrisico zijn wanneer de waarden persoonlijke identificeerbare informatie (PII) of andere gevoelige gegevens kunnen omvatten die zij moeten beschermen.

[!DNL Journey Optimizer] biedt een coderingsfunctie in de verpersoonlijkingseditor, zodat u elke expressiewaarde tijdens het renderen kunt coderen (bijvoorbeeld een profielkenmerk, een token of een tekenreeks die u van verschillende velden hebt gemaakt). Voor codering is altijd een sleutel uit het register van uw organisatie vereist.

U codeert alleen de queryparameters die u kiest, met behulp van sleutels die beheerders beheren in een register op sandboxniveau, zodat vertrouwelijke waarden niet in duidelijke tekst worden weergegeven wanneer de koppeling wordt gedeeld of geïnspecteerd.

### Werking {#how-it-works}

* **de Beheerders** gebruiken de zeer belangrijke registratie [&#x200B; sleutels &#x200B;](#create-keys) creëren en [&#x200B; leiden sleutels &#x200B;](#manage-keys) in overeenstemming met het veiligheidsbeleid van uw organisatie.
* **de Keters** nemen de `Encrypt` hulp in de verpersoonlijkingsredacteur op en gaan de waarde over om plus een actief zeer belangrijk herkenningsteken van de registratie te beschermen. Voor syntaxis en opties, zie [&#x200B; deze sectie &#x200B;](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>Decryptie is de verantwoordelijkheid van uw organisatie. [!DNL Journey Optimizer] versleutelt waarden wanneer het bericht wordt weergegeven. Uw website, toepassing of API moet parameters decoderen met hetzelfde cryptografisch materiaal en -processen als in uw beveiligingsmodel.

### Voorbeeld

Een bestemmingspagina-URL kan een vraagparameter zoals `token` gebruiken de waarvan waarde een koordteken (bijvoorbeeld een JSON nuttige lading met aanbieding of profielherkenningstekens) is. Zonder codering is dat tekenreekstoken zichtbaar als onbewerkte tekst in de koppeling. Wanneer u die waarde met de coderingshelper omsluit, wordt de vertrouwelijke payload vervangen door ciphertext in de URL, terwijl de rest van de koppeling ongewijzigd blijft.

## Toetsen maken {#create-keys}

Voordat u de URL-parametercoderingsfunctie kunt gebruiken, moet u een sleutel maken. Volg de onderstaande stappen om dit te doen.

>[!NOTE]
>
>Er zijn momenteel geen specifieke machtigingen voor toegang tot en beheer van toetsen. Rollen die toegang verlenen tot de sectie **[!UICONTROL Configurations]** onder **[!UICONTROL Administration]** , bieden ook toegang tot het sleutelregister. Specifieke machtigingen zijn echter gepland voor een toekomstige release.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)
-->

1. Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** .

1. Klik op de knop **[!UICONTROL Manage]** om **[!UICONTROL Key registry]** te openen.

   ![&#x200B; Zeer belangrijke registratiesectie in het menu van het Beleid &#x200B;](assets/encryption-key-registry.png){width="80%"}

1. Gebruik de toegewijde knop om naar wens sleutels voor uw organisatie te maken.

   ![&#x200B; creeer zeer belangrijke knoop in Zeer belangrijke registratiesectie &#x200B;](assets/encryption-create-key.png){width="80%"}

1. Wijs hen een duidelijk etiket of herkenningsteken toe uw teams in de verpersoonlijkingsredacteur kunnen van verwijzingen voorzien.

   ![&#x200B; Zeer belangrijke details in Zeer belangrijke registratiesectie &#x200B;](assets/encryption-key-details.png){width="80%"}

1. Klik op **[!UICONTROL Submit]** om uw wijzigingen te bevestigen.

Zodra een sleutel wordt gecreeerd, kunnen de marketers de [&#x200B; hulp van de de parameterencryptie URL &#x200B;](functions/helpers.md#url-parameter-encryption-helper) in de verpersoonlijkingsredacteur gebruiken om specifieke waarden te coderen die zij in URL vraagparameters plaatsen.

## Sleutels beheren {#manage-keys}

Volg onderstaande stappen om de toetsen te beheren.

1. Open de lus **[!UICONTROL Key registry]** . Alle toetsen die voor de huidige sandbox zijn gemaakt, worden weergegeven in een lijstweergave.

   ![&#x200B; Zeer belangrijke mening van de registratielijst &#x200B;](assets/encryption-key-registry-list.png){width="100%"}

1. Klik op een toets met de status **[!UICONTROL Active]** om de belangrijkste details te openen.

   ![&#x200B; Actieve belangrijkste details &#x200B;](assets/encryption-key-active-details.png){width="80%"}

1. Klik op de knop **[!UICONTROL Revoke]** om de sleutel voor nieuwe versleuteling permanent uit te schakelen.

   Zodra een sleutel wordt ingetrokken, zouden pogingen om het in helper te gebruiken bij teruggegeven tijd moeten ontbreken. Ingetrokken items blijven zichtbaar voor controle. Het is mogelijk dat uw teams nog steeds het overeenkomende materiaal nodig hebben voor het decoderen van oudere ladingen op uw eigen systemen.

1. Klik op de knop **[!UICONTROL Rotate]** om nieuw belangrijk materiaal te leveren terwijl u een stabiele sleutel-id behoudt waarnaar uw reizen en campagnes al verwijzen.

   Het voorgaande materiaal wordt in het register bewaard met een ingetrokken status en een juiste reden (bijvoorbeeld een tijdstempel voor rotatie) en een nieuwe rij of versie geeft de actieve sleutel weer.

   >[!NOTE]
   >
   >Alleen actieve toetsen moeten worden geselecteerd om nieuwe waarden te versleutelen in de verpersoonlijkingseditor. Gebruik geen ingetrokken toetsen voor nieuwe inhoud.
