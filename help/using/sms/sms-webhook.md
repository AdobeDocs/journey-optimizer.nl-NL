---
solution: Journey Optimizer
product: journey optimizer
title: Vorm uw Webhaak van SMS
description: Leer hoe u Webhooks configureert om binnenkomende reacties vast te leggen voor het beheer van de toestemming om te weigeren of te weigeren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: a0f3e385-934d-44d6-a487-6035161aef0e
source-git-commit: 7b6efb1997074723be25b0f99d47debb1f1188e0
workflow-type: tm+mt
source-wordcount: '2579'
ht-degree: 0%

---

# Webhaak maken {#webhook}

>[!CONTEXTUALHELP]
>id="ajo_channels_sms_webhook_settings_create"
>title="Een SMS-webhaak maken"
>abstract="U kunt Webhooks configureren om binnenkomende reacties vast te leggen voor het beheer van de toestemming om te weigeren of te weigeren en om leveringsrapporten te ontvangen, inclusief leesontvangstbewijzen indien beschikbaar."


>[!CONTEXTUALHELP]
>id="ajo_admin_sms_webhook_flow_type"
>title="Kies het type WebHaak"
>abstract="Wanneer vestiging een webhaak, kies **Binnenkomend** om toestemmingsreacties en gebruikersvoorkeur te vangen, of **[!UICONTROL Feedback]** om levering en betrokkenheidsgebeurtenissen voor het melden en analyse te volgen."

>[!BEGINSHADEBOX]

Wanneer er nieuwe API-referenties worden gemaakt in Journey Optimizer, kunt u met SMS-websites zowel binnenkomende trefwoorden als feedbackgebeurtenissen zoals leveringen en fouten vastleggen. Omdat elke provider verschillende mogelijkheden heeft, zijn er aparte instructies om webhaken in te schakelen.
Met websites die nu aangepaste providers ondersteunen, is het nu mogelijk feedback en inkomende trefwoordverzameling te verzamelen bij elke provider die in Journey Optimizer moet worden gerapporteerd en waarop moet worden gereageerd.

* **Nieuwe klanten:** de instructies kunnen hier worden gevolgd om de websites van SMS correct te vormen.

* **Bestaande klanten:** u kunt van informatie migreren die in API Geloofsbrieven aan Webhooks wordt opgeslagen en er is geen chronologie voor klanten om te migreren. Voor bestaande klanten die wel naar SMS Webhooks willen migreren, moeten de migratiestappen worden uitgevoerd zoals gedocumenteerd in de migratiehandleiding.

>[!ENDSHADEBOX]

## Overzicht {#overview}

Nadat de API-referenties zijn gemaakt, kunt u nu webhooks configureren om binnenkomende reacties vast te leggen voor het beheer van de toestemming om zich aan te melden en te weigeren, en leveringsrapporten ontvangen, inclusief leesontvangstbewijzen, indien beschikbaar.

Wanneer u een webhaak instelt, kunt u het doel ervan definiëren op basis van het type gegevens dat u wilt vastleggen:

* **Binnenkomend**: Gebruik deze optie als u toestemmingsreacties, zoals opt-ins of opt-outs wilt vangen, en gebruikersvoorkeur verzamelen.

* **Terugkoppeling**: Kies deze optie om levering en betrokkenheidsgebeurtenissen, met inbegrip van leveringen, uitgaande fouten, read ontvangstbewijzen (indien van toepassing) te volgen om rapportering en analyse te steunen.

Afhankelijk van uw leverancier, zullen er verschillende verwachtingen zijn over wat moet opstelling om een succesvolle implementatie van SMS te hebben:

* **Sinch en Sinch Conversational**: Creeer één webhaak die zowel binnenkomende als terugkoppelen gebeurtenissen behandelt. Er is geen payload-configuratie vereist.

* **Infobip**: Creeer twee afzonderlijke webhooks, voor binnenkomende gebeurtenissen en voor terugkoppel gebeurtenissen. Voor geen van beide websites is een payload-configuratie vereist.

* **Twilio**: Webhooks zijn niet beschikbaar. De binnenkomende en terugkoppelen gegevensinzameling wordt niet gesteund.

* **Leverancier van de Douane**: Creeer twee afzonderlijke websites, voor binnenkomende gebeurtenissen en voor terugkoppelt gebeurtenissen. De configuratie van de lading wordt vereist voor beide websites behoorlijk te functioneren.

### Ondersteuning van leveranciers {#provider-support}

>[!NOTE]
>
>JSON is de enige ondersteunde webhaakindeling. Formuliergegevens voor websites worden niet ondersteund.

In de volgende tabel wordt aangegeven welke providers binnenkomende webhooks ondersteunen en feedback geven, en of er een payload moet worden gemaakt:

| Provider | Binnenkomende WebHaak | Feedback Webhaak | Trefwoorden | Payload-ontwerp vereist | Webhaak vereist | Payload maken |
| --- | --- | --- | --- | --- | --- | --- |
| Infobip | Configureerbaar | Configureerbaar | Configureerbaar | Niet vereist | Vereist | Niet vereist |
| Sinch | Configureerbaar | Configureerbaar | Configureerbaar | Niet vereist | Nee. Geïntegreerd | N.v.t. |
| Sinch-gesprek | Configureerbaar | Configureerbaar | Configureerbaar | Niet vereist | Nee. Geïntegreerd | N.v.t. |
| Twilio | Niet beschikbaar | Niet beschikbaar | Niet beschikbaar | Niet beschikbaar | Niet beschikbaar | N.v.t. |
| Aangepast | Configureerbaar | Configureerbaar | Configureerbaar | Vereist | Vereist | Vereist |

Voor klanten die van API geloofsbrieven aan de websites van SMS bewegen, wordt de informatie over de migratieweg gevonden in de migratiegids.

## Webhaak maken

### Voor Sinch- en Sinch-gesprekken {#create-webhook-sinch}

Voor Sinch en Sinch Conversational, creeer één enkele webhaak die zowel binnenkomende als feedbackgebeurtenissen behandelt. Er is geen aangepaste payload-configuratie vereist.

1. Navigeer in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** , selecteer het menu **[!UICONTROL SMS Webhooks]** onder **[!UICONTROL SMS settings]** en klik op de knop **[!UICONTROL Create Webhook]** .

   ![](assets/webhook-1.png)

1. Configureer uw WebHaak-instellingen, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: voer een naam in voor uw webhaak.

   * **[!UICONTROL Select SMS vendor]**: Sinch- of Sinch-gesprek.

   * **[!UICONTROL API credentials]**: Kies van drop-down u [ eerder gevormde API geloofsbrieven ](sms-configuration-sinch.md).

   * **[!UICONTROL Sender Phone Number]**: ga het aantal van de afzendertelefoon in u voor uw mededelingen wilt gebruiken.

   ![](assets/webhook-2.png)

1. Start het instellen van de binnenkomende trefwoorden door trefwoorden in te voeren in het veld **[!UICONTROL Enter a Keyword]** . U kunt meerdere trefwoorden toevoegen en verwijderen. Trefwoorden zijn niet hoofdlettergevoelig.

   ![](assets/webhook-3.png)

1. Selecteer een trefwoordcategorie in de vervolgkeuzelijst **[!UICONTROL Inbound Keyword Category]** die u wilt configureren:

   * 
     +++ Inschakelen

      * Trefwoorden inschakelen die gebruikers met hun toestemming aanmelden. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, wordt hun telefoonaantal verkozen binnen om de berichten van SMS te ontvangen.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Abonneren, Ja, Stoppen, Doorgaan, Hervatten en Beginnen. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een Opt-In-trefwoord.

     +++

   * 
     +++ Uitschakelen

      * Schakel trefwoorden in die gebruikers weigeren en verwijder toestemming om tekstberichten te verzenden. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, wordt hun telefoonaantal uit het ontvangen van de berichten van SMS verkozen.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Stoppen, Afsluiten, Annuleren, Einde, Afmelden, Nee. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een uitschakeltrefwoord.

      * Schakel **[!UICONTROL Fuzzy Logic]** in om vergelijkbare trefwoorden te detecteren als geconfigureerde uitschakeltrefwoorden. Als de reactie van een gebruiker dicht maar niet nauwkeurig is, wordt het bericht ingegaan in het **[!UICONTROL Fuzzy Auto Response]** gebied verzonden. Doorgaans geeft dit bericht aan dat de optie niet is ingeschakeld en geeft het exacte trefwoord op dat nodig is om het abonnement op te zeggen.

     +++

   * 
     +++ Dubbele plug-in

      * Trefwoorden inschakelen voor de vereiste dubbele aanmelding. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, zijn zij niet volledig open-binnen in dit stadium. Deze tweestapstoestemmingswerkstroom vereist gebruikers om hun opt-in met een tweede sleutelwoord te bevestigen.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer een trefwoord voor dubbele aanmelding overeenkomt. Dit bericht instrueert de gebruiker om een Opt-In sleutelwoord in te gaan om het opt-in proces te voltooien.

     +++

   * 
     +++ Help

      * Laat sleutelwoorden toe die een standaardreactie verstrekken wanneer de hulp wordt gevraagd. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, ontvangen zij het het antwoordbericht van de Hulp.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Help, Info, Informatie. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een Help-trefwoord.

     +++

   * 
     +++ Aangepast

      * Configureer één aangepast trefwoord. Wanneer het bericht van een gebruiker dit sleutelwoord aanpast, wordt het sleutelwoord geschreven aan de **[!UICONTROL Message Feedback tracking]** dataset voor het melden van en publiek het opbouwen.

      * Bouw een Publiek (het stromen of de partij) die verwijzingen dit sleutelwoord voor gebruik in uw reizen en campagnes.

     +++

1. Voer een **[!UICONTROL Default Reply Message]** in. Dit bericht wordt automatisch verzonden wanneer de reactie van een gebruiker geen gevormd sleutelwoord aanpast.

   ![](assets/webhook-4.png)

1. Klik op **[!UICONTROL Submit]** om de configuratie van uw webhaak op te slaan.

1. Vanuit het menu **[!UICONTROL Webhooks]** kunt u bestaande webhaken bewerken of verwijderen.

1. Open de nieuwe webhaak en kopieer de **[!UICONTROL Webhook URL]** .

   ![](assets/webhook-5.png)

1. Gebruik uw **[!UICONTROL Webhook URL]** om de **Terugkoppeling** en **Binnenkomende** gebeurtenissen toe te laten om in Journey Optimizer te komen.

   * Voor het kanaal van SMS, [ leren meer in de documentatie van de Sondt ](https://community.sinch.com/t5/SMS/How-do-I-assign-a-callback-URL-to-an-SMS-service/ta-p/8414)

   * Voor het kanaal MMS, [ leer meer in de documentatie van het Sondje ](https://developers.sinch.com/docs/conversation/getting-started#5-handle-incoming-messages)

   * Voor klanten die SMS rechtstreeks via Journey Optimizer hebben aangeschaft, kunt u een ondersteuningsticket indienen bij de ondersteuning van Adobe. Het Adobe-accountteam configureert de URL van de webhaak voor u.
     ![](assets/webhook-4.png)

Als uw webhaak API-referenties gebruikt die aan een bestaande kanaalconfiguratie zijn gekoppeld, wordt de webhaak onmiddellijk van kracht. Anders maakt u een nieuwe kanaalconfiguratie.

➡️[ leer meer op kanaalconfiguratie ](sms-configuration-surface.md)

### Voor Infobip {#create-webhook-infobip}

Voor Infobip, creeer twee afzonderlijke websites: voor de gebeurtenissen van de Terugkoppeling en voor Inkomende gebeurtenissen.

1. Navigeer in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** , selecteer het menu **[!UICONTROL SMS Webhooks]** onder **[!UICONTROL SMS settings]** en klik op de knop **[!UICONTROL Create Webhook]** .

   ![](assets/webhook-1.png)

1. Configureer uw WebHaak-instellingen, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: voer een naam in voor uw webhaak.

   * **[!UICONTROL Select SMS vendor]**: Infobip.

   * **[!UICONTROL Type]**: Kies Feedback of Binnenkomend. U moet beide afzonderlijk creëren, hier, beginnen wij met Binnenkomend.

   * **[!UICONTROL API credentials]**: Kies van drop-down u [ eerder gevormde API geloofsbrieven ](sms-configuration-infobip.md#api-credential).

   * **[!UICONTROL Sender Phone Number]**: ga het aantal van de afzendertelefoon in u voor uw mededelingen wilt gebruiken.

   ![](assets/webhook-6.png)

1. Start het instellen van de binnenkomende trefwoorden door trefwoorden in te voeren in het veld **[!UICONTROL Enter a Keyword]** . U kunt meerdere trefwoorden toevoegen en verwijderen. Trefwoorden zijn niet hoofdlettergevoelig.

   ![](assets/webhook-7.png)

1. Selecteer een trefwoordcategorie in de vervolgkeuzelijst **[!UICONTROL Inbound Keyword Category]** die u wilt configureren:

   * 
     +++ Inschakelen

      * Trefwoorden inschakelen die gebruikers met hun toestemming aanmelden. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, wordt hun telefoonaantal verkozen binnen om de berichten van SMS te ontvangen.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Abonneren, Ja, Stoppen, Doorgaan, Hervatten en Beginnen. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een Opt-In-trefwoord.

     +++

   * 
     +++ Uitschakelen

      * Schakel trefwoorden in die gebruikers weigeren en verwijder toestemming om tekstberichten te verzenden. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, wordt hun telefoonaantal uit het ontvangen van de berichten van SMS verkozen.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Stoppen, Afsluiten, Annuleren, Einde, Afmelden, Nee. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een uitschakeltrefwoord.

      * Schakel **[!UICONTROL Fuzzy Logic]** in om vergelijkbare trefwoorden te detecteren als geconfigureerde uitschakeltrefwoorden. Als de reactie van een gebruiker dicht maar niet nauwkeurig is, wordt het bericht ingegaan in het **[!UICONTROL Fuzzy Auto Response]** gebied verzonden. Doorgaans geeft dit bericht aan dat de optie niet is ingeschakeld en geeft het exacte trefwoord op dat nodig is om het abonnement op te zeggen.

     +++

   * 
     +++ Dubbele plug-in

      * Trefwoorden inschakelen voor de vereiste dubbele aanmelding. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, zijn zij niet volledig open-binnen in dit stadium. Deze tweestapstoestemmingswerkstroom vereist gebruikers om hun opt-in met een tweede sleutelwoord te bevestigen.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer een trefwoord voor dubbele aanmelding overeenkomt. Dit bericht instrueert de gebruiker om een Opt-In sleutelwoord in te gaan om het opt-in proces te voltooien.

     +++

   * 
     +++ Help

      * Laat sleutelwoorden toe die een standaardreactie verstrekken wanneer de hulp wordt gevraagd. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, ontvangen zij het het antwoordbericht van de Hulp.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Help, Info, Informatie. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een Help-trefwoord.

     +++

   * 
     +++ Aangepast

      * Configureer één aangepast trefwoord. Wanneer het bericht van een gebruiker dit sleutelwoord aanpast, wordt het sleutelwoord geschreven aan de **[!UICONTROL Message Feedback tracking]** dataset voor het melden van en publiek het opbouwen.

      * Bouw een Publiek (het stromen of de partij) die verwijzingen dit sleutelwoord voor gebruik in uw reizen en campagnes.

     +++

1. Voer een **[!UICONTROL Default Reply Message]** in. Dit bericht wordt automatisch verzonden wanneer de reactie van een gebruiker geen gevormd sleutelwoord aanpast.

   ![](assets/webhook-8.png)

1. Klik op **[!UICONTROL Submit]** om de configuratie van uw webhaak op te slaan.

1. In het **[!UICONTROL Webhooks]** menu, moet u nu a **Feedback** webhaak voor Infobip tot stand brengen.

1. Configureer uw WebHaak-instellingen, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: voer een naam in voor uw webhaak.

   * **[!UICONTROL Select SMS vendor]**: Infobip.

   * **[!UICONTROL Type]**: kies Feedback.

   ![](assets/webhook-9.png)

1. Klik op **[!UICONTROL Submit]** om de configuratie van uw feedbackwebsite op te slaan.

1. Vanuit het menu **[!UICONTROL Webhooks]** kunt u bestaande webhaken bewerken of verwijderen.

1. Open de nieuwe webhaken en kopieer de **[!UICONTROL Webhook URL]** van elk van uw webhaken.

   ![](assets/webhook-10.png)

1. U kunt die URLs nu gebruiken om zowel Callback URLs toe te laten om Terugkoppeling als Inkomende gebeurtenissen in Journey Optimizer te brengen.

Als uw webhaak API-referenties gebruikt die aan een bestaande kanaalconfiguratie zijn gekoppeld, wordt de webhaak onmiddellijk van kracht. Anders maakt u een nieuwe kanaalconfiguratie.

➡️[ leer meer op kanaalconfiguratie ](sms-configuration-surface.md)

### Voor aangepaste provider {#create-webhook-custom}

Voor Aangepaste SMS-providers maakt u twee aparte websites: een voor feedbackgebeurtenissen en een voor Inbound-gebeurtenissen.

1. Navigeer in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** , selecteer het menu **[!UICONTROL SMS Webhooks]** onder **[!UICONTROL SMS settings]** en klik op de knop **[!UICONTROL Create Webhook]** .

   ![](assets/webhook-1.png)

1. Configureer uw WebHaak-instellingen, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: voer een naam in voor uw webhaak.

   * **[!UICONTROL Select SMS vendor]**: Aangepast.

   * **[!UICONTROL Type]**: Kies Feedback of Binnenkomend. U moet beide afzonderlijk creëren, hier, beginnen wij met Binnenkomend.

   * **[!UICONTROL API credentials]**: Kies van drop-down u [ eerder gevormde API geloofsbrieven ](sms-configuration-custom.md).

   * **[!UICONTROL Sender Phone Number]**: ga het aantal van de afzendertelefoon in u voor uw mededelingen wilt gebruiken.

   ![](assets/webhook-11.png)

1. Start het instellen van de binnenkomende trefwoorden door trefwoorden in te voeren in het veld **[!UICONTROL Enter a Keyword]** . U kunt meerdere trefwoorden toevoegen en verwijderen. Trefwoorden zijn niet hoofdlettergevoelig.

   ![](assets/webhook-12.png)

1. Selecteer een trefwoordcategorie in de vervolgkeuzelijst **[!UICONTROL Inbound Keyword Category]** die u wilt configureren:

   * 
     +++ Inschakelen

      * Trefwoorden inschakelen die gebruikers met hun toestemming aanmelden. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, wordt hun telefoonaantal verkozen binnen om de berichten van SMS te ontvangen.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Abonneren, Ja, Stoppen, Doorgaan, Hervatten en Beginnen. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een Opt-In-trefwoord.

     +++

   * 
     +++ Uitschakelen

      * Schakel trefwoorden in die gebruikers weigeren en verwijder toestemming om tekstberichten te verzenden. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, wordt hun telefoonaantal uit het ontvangen van de berichten van SMS verkozen.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Stoppen, Afsluiten, Annuleren, Einde, Afmelden, Nee. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een uitschakeltrefwoord.

      * Schakel **[!UICONTROL Fuzzy Logic]** in om vergelijkbare trefwoorden te detecteren als geconfigureerde uitschakeltrefwoorden. Als de reactie van een gebruiker dicht maar niet nauwkeurig is, wordt het bericht ingegaan in het **[!UICONTROL Fuzzy Auto Response]** gebied verzonden. Doorgaans geeft dit bericht aan dat de optie niet is ingeschakeld en geeft het exacte trefwoord op dat nodig is om het abonnement op te zeggen.

     +++

   * 
     +++ Dubbele plug-in

      * Trefwoorden inschakelen voor de vereiste dubbele aanmelding. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, zijn zij niet volledig open-binnen in dit stadium. Deze tweestapstoestemmingswerkstroom vereist gebruikers om hun opt-in met een tweede sleutelwoord te bevestigen.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer een trefwoord voor dubbele aanmelding overeenkomt. Dit bericht instrueert de gebruiker om een Opt-In sleutelwoord in te gaan om het opt-in proces te voltooien.

     +++

   * 
     +++ Help

      * Laat sleutelwoorden toe die een standaardreactie verstrekken wanneer de hulp wordt gevraagd. Wanneer het bericht van een gebruiker een gevormd sleutelwoord aanpast, ontvangen zij het het antwoordbericht van de Hulp.

      * Standaard zijn de volgende trefwoorden ingeschakeld: Help, Info, Informatie. Verwijder standaardtrefwoorden door op ![](assets/do-not-localize/Smock_Close_18_N.svg) te klikken.

      * Gebruik het veld **[!UICONTROL Reply Message]** om een bericht te maken dat automatisch wordt verzonden wanneer het binnenkomende bericht van een gebruiker overeenkomt met een Help-trefwoord.

     +++

   * 
     +++ Aangepast

      * Configureer één aangepast trefwoord. Wanneer het bericht van een gebruiker dit sleutelwoord aanpast, wordt het sleutelwoord geschreven aan de **[!UICONTROL Message Feedback tracking]** dataset voor het melden van en publiek het opbouwen.

      * Bouw een Publiek (het stromen of de partij) die verwijzingen dit sleutelwoord voor gebruik in uw reizen en campagnes.

     +++

1. Voer een **[!UICONTROL Default Reply Message]** in. Dit bericht wordt automatisch verzonden wanneer de reactie van een gebruiker geen gevormd sleutelwoord aanpast.

   ![](assets/webhook-13.png)

1. Maak een aangepaste payload die overeenkomt met de JSON die afkomstig is van de provider. De enige webhaakindeling die wordt ondersteund, is JSON. Formuliergegevens voor websites worden niet ondersteund.

   De binnenkomende webhaak vereist de volgende gebieden om waarden van WebHaak van uw leverancier te ontvangen:

   * **InboundMessage**: Het binnenkomende bericht of het sleutelwoord dat van de gebruiker wordt ontvangen.
   * **ProfileNumber**: Het telefoonaantal van de gebruiker die het bericht verzond.
   * **RequestID**: Een uniek herkenningsteken dat door uw leverancier van SMS wordt verstrekt om een specifieke transactie te identificeren.
   * **OriginTimestamp**: Tijdstempel toen het bericht, in formaat UTC werd ontvangen.
   * **InboundNumber**: Het telefoonaantal dat voor deze WebHaakconfiguratie wordt gebruikt.

   +++Payload-voorbeeld

        &quot;json 
        
        &quot;inboundMessage&quot;: &quot;{{inboundMessage}}&quot;, 
        &quot;profileNumber&quot;: &quot;{{profileNumber}}&quot;, 
        &quot;requestId&quot;: &quot;{{requestId}}&quot;, 
        &quot;originTimestamp&quot;: &quot;{{originTimestamp}}&quot;, 
        &quot;inboundNumber&quot;: &quot;{{inboundNumber}}&quot;
        
       &quot;
   +++

1. Wanneer uw JSON-bestand is gemaakt, klikt u op **[!UICONTROL View payload editor]**. Vervolgens kopieert en plakt u de JSON-payload in de editor en slaat u deze op.

   ![](assets/webhook-14.png)

1. Klik op **[!UICONTROL Submit]** om de configuratie van uw webhaak op te slaan.

1. In het **[!UICONTROL Webhooks]** menu, moet u nu a **Feedback** webhaak voor de douaneleverancier tot stand brengen.

1. Configureer uw WebHaak-instellingen, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: voer een naam in voor uw webhaak.

   * **[!UICONTROL Select SMS vendor]**: Aangepast.

   * **[!UICONTROL Type]**: kies Feedback.

   ![](assets/webhook-15.png)

1. Maak een aangepaste payload die overeenkomt met de JSON-indeling van uw provider. De enige webhaakindeling die wordt ondersteund, is JSON. Formuliergegevens voor websites worden niet ondersteund.

   Voor de feedbackwebsite moeten de volgende velden waarden ontvangen van de website van uw provider:

   * **Verwijzing van de Cliënt**: Een uniek herkenningsteken dat in de nuttige lading voor het registreren doeleinden is teruggekeerd.
   * **Code**: De mislukkingscode die door uw leverancier van SMS wordt verstrekt.
   * **Status**: De mislukkingsstatus die door uw leverancier van SMS wordt verstrekt.

   +++Payload-voorbeeld

        &quot;json 
        
        &quot;clientReference&quot;: &quot;{{client_reference}}&quot;, 
        &quot;statussen&quot;: [
       {
        &quot;code&quot;: &quot;{{failureCode}}&quot;, 
        &quot;status&quot;: &quot;{{feedbackStatus}}&quot;
        
       ] 
        
       &quot;
   
   +++

1. Klik op **[!UICONTROL View payload editor]** en kopieer en plak de JSON-payload naar de editor en sla deze op.

   ![](assets/webhook-16.png)

1. Klik op **[!UICONTROL Submit]** om de configuratie van uw feedbackwebsite op te slaan.

1. Vanuit het menu **[!UICONTROL Webhooks]** kunt u bestaande webhaken bewerken of verwijderen.

1. Open de nieuwe webhaken en kopieer de **[!UICONTROL Webhook URL]** van elk van uw webhaken.

1. Vorm uw leverancier van SMS om **Terugkoppeling** en **Binnenkomende** gebeurtenissen naar deze webhaak URLs in Journey Optimizer te verzenden.

   De instructies van de configuratie variëren door de leverancier van SMS. Raadpleeg de documentatie van uw provider voor meer informatie over het instellen van callback-URL&#39;s.

Als uw webhaak API-referenties gebruikt die aan een bestaande kanaalconfiguratie zijn gekoppeld, wordt de webhaak onmiddellijk van kracht. Anders maakt u een nieuwe kanaalconfiguratie.

➡️[ leer meer op kanaalconfiguratie ](sms-configuration-surface.md)
