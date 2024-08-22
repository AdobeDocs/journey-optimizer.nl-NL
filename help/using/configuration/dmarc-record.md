---
solution: Journey Optimizer
product: journey optimizer
title: DMARC-record
description: Leer hoe u DMARC-record instelt in Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, domein, mail, dmarc, record
exl-id: f9e217f8-5aa8-4d3a-96fc-65defcb5d340
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 0%

---

# DMARC-record {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="DMARC-record instellen"
>abstract="DMARC is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik te beschermen en leveringskwesties met brievenbusleveranciers te vermijden.<br> als deel van hun het handhaven van industrie beste praktijken, Google en Yahoo! U hebt beide een DMARC-record nodig voor elk domein dat u gebruikt om e-mail naar hen te verzenden."

## Wat is DMARC? {#what-is-dmarc}

De op domein-gebaseerde Authentificatie van het Bericht, het Melden, en de Conformiteit (DMARC) is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik te beschermen. Door een duidelijk beleid aan e-mailleveranciers en dienstverleners van Internet (ISPs) aan te bieden, helpt het kwaadwillige acteurs verhinderen e-mails te verzenden die beweren van uw domein te zijn. DMARC implementeren verkleint het risico dat legitieme e-mailberichten worden gemarkeerd als spam of afgewezen, en verbetert uw e-mailleverbaarheid.

DMARC biedt ook rapportering over berichten die authentificatie ontbreken, samen met controle over de behandeling van e-mails die geen bevestiging DMARC overgaan. Afhankelijk van het uitgevoerde [ beleid DMARC ](#dmarc-policies), kunnen deze e-mails worden gecontroleerd, in quarantaine worden geplaatst, of worden verworpen. Met deze functies kunt u acties uitvoeren om mogelijke fouten te beperken en aan te pakken.

Om u te helpen leveringsproblemen verhinderen terwijl het verkrijgen van controle over post die authentificatie ontbreekt, steunt [!DNL Journey Optimizer] nu direct de technologie DMARC in zijn beleidsinterface. [Meer informatie](#implement-dmarc)

### Hoe werkt DMARC? {#how-dmarc-works}

SPF en DKIM worden allebei gebruikt om een e-mail met een domein te associëren en samen te werken om e-mail voor authentiek te verklaren. DMARC neemt deze één stap verder en helpt spoofing te verhinderen door het domein aan te passen dat door DKIM en SPF wordt gecontroleerd.

>[!NOTE]
>
>In Journey Optimizer zijn SPF en DKIM geconfigureerd voor u.

Om DMARC over te gaan, moet een bericht SPF of DKIM overgaan:

* SPF (het Kader van het Beleid van de Afzender) helpt verifiëren dat het e-mailbericht uit een erkende bron door het IP van de verzendende server adres tegen een lijst van erkende IP adressen voor het domein te controleren komt.
* DKIM (DomainKeys Identified Mail) voegt een digitale handtekening toe aan e-mailberichten, zodat de ontvanger de integriteit en authenticiteit van het bericht kan verifiëren.

Als beide of een van deze niet-verificatie wordt uitgevoerd, mislukt DMARC en wordt het e-mailbericht verzonden volgens het geselecteerde DMARC-beleid.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### DMARC-beleid {#dmarc-policies}

Als een e-mail DMARC-verificatie mislukt, kunt u beslissen welke actie op dat bericht wordt toegepast. DMARC heeft drie beleidsopties:

* Monitor (p=none): instrueert de postbusprovider/ISP om te doen wat zij normaal aan het bericht zouden doen.
* Quarantine (p=quarantaine): Instrueert de brievenbusleverancier/ISP om post te leveren die geen DMARC tot spam of junk omslag van de ontvanger overgaat.
* Weigeren (p=weiger): Instrueert de brievenbusleverancier/ISP om post te blokkeren die DMARC niet overgaat resulterend in een stuit.

>[!NOTE]
>
>Leer hoe te om het beleid DMARC met [!DNL Journey Optimizer] in [ te plaatsen deze sectie ](#set-up-dmarc).

## DMARC-vereiste bijwerken {#dmarc-update}

Google en Yahoo zijn een onderdeel van hun best practices in de branche. allebei vereisen dat u het verslag van a **DMARC** voor om het even welk domein hebt u gebruikt om e-mail naar hen te verzenden. Dit nieuwe vereiste is beginnend **Februari 1st, 2024** van toepassing.

>[!CAUTION]
>
>Gmail en Yahoo voldoen niet aan deze nieuwe eis! wordt verwacht dat e-mailberichten in de map spam zullen landen of geblokkeerd zullen raken.

Daarom beveelt de Adobe u ten zeerste aan de volgende maatregelen te nemen:

* Zorg ervoor om **DMARC verslag** opstelling voor **alle subdomeinen te hebben die u** aan Adobe in [!DNL Journey Optimizer] reeds hebt gedelegeerd. [ leer hoe ](#check-subdomains-for-dmarc)

* Wanneer **het delegeren van om het even welk nieuw subdomain** aan Adobe, kunt u **opstelling DMARC** direct **in de [!DNL Journey Optimizer] beleidsinterface**. [ leer hoe ](#implement-dmarc)

## DMARC implementeren in [!DNL Journey Optimizer] {#implement-dmarc}

Met de beheerinterface van [!DNL Journey Optimizer] kunt u een DMARC-record instellen voor alle subdomeinen die u al hebt gedelegeerd of aan Adobe delegeert. De gedetailleerde stappen worden hieronder beschreven.

### Controleer uw bestaande subdomeinen voor DMARC {#check-subdomains-for-dmarc}

Volg onderstaande stappen om ervoor te zorgen dat u DMARC-record hebt ingesteld voor alle subdomeinen die u in [!DNL Journey Optimizer] hebt gedelegeerd.

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** en klik op **[!UICONTROL Set up subdomain]** .

1. Controleer de kolom **[!UICONTROL DMARC Record]** voor elk gedelegeerd subdomein. Als er geen record is gevonden voor een bepaald subdomein, wordt een waarschuwing weergegeven.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Om aan het nieuwe vereiste van Gmail en Yahoo! te voldoen, en leveringskwesties met hoogste ISPs te vermijden, wordt het geadviseerd aan opstellingsDMARC verslag voor alle gedelegeerde subdomeinen. [Meer informatie](dmarc-record-update.md)

1. Selecteer een subdomein waaraan geen DMARC-record is gekoppeld en vul de sectie **[!UICONTROL DMARC record]** in op basis van de behoeften van uw organisatie. De stappen om de DMARC- verslaggebieden te bevolken zijn gedetailleerd in [ deze sectie ](#implement-dmarc).

1. Houd rekening met de volgende twee opties:

   * Als u een subdomeinopstelling met [ CNAME ](delegate-subdomain.md#cname-subdomain-delegation) uitgeeft, moet u het DNS verslag voor DMARC in uw het ontvangen oplossing kopiëren om de passende DNS verslagen te produceren.

     ![](assets/dmarc-record-edit-cname.png)

     Controleer of het DNS-record is gegenereerd in uw domeinhostingoplossing en schakel het selectievakje &quot;I confirm...&quot; in.

   * Als u een subdomain [ uitgeeft volledig ](delegate-subdomain.md#full-subdomain-delegation) aan Adobe wordt afgevaardigd, vul eenvoudig de **[!UICONTROL DMARC record]** gebieden in die in [ worden gedetailleerd deze sectie ](#implement-dmarc). Er is geen verdere actie nodig.

     ![](assets/dmarc-record-edit-full.png)

1. Sla uw wijzigingen op.

### DMARC instellen voor nieuwe subdomeinen {#set-up-dmarc}

Wanneer het delegeren van nieuwe subdomeinen aan Adobe in [!DNL Journey Optimizer], zal een verslag DMARC in DNS voor uw domein worden gecreeerd. Voer de onderstaande stappen uit om DMARC te implementeren.

>[!CAUTION]
>
>Om aan het nieuwe vereiste van Gmail en Yahoo! te voldoen, en leveringskwesties met hoogste ISPs te vermijden, wordt het geadviseerd aan opstellingsDMARC verslag voor alle gedelegeerde subdomeinen. [Meer informatie](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Stel een nieuw subdomein in. [ leer hoe ](delegate-subdomain.md)

1. Ga naar de sectie **[!UICONTROL DMARC record]** .

   Als het subdomein een bestaande DMARC-record heeft en door [!DNL Journey Optimizer] wordt opgehaald, kunt u dezelfde waarden gebruiken als in de interface zijn gemarkeerd, of deze naar wens wijzigen.

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >Als u geen waarden toevoegt, worden de vooraf ingevulde standaardwaarden gebruikt.

1. Bepaal de actie die de ontvankelijke server zal uitvoeren als DMARC ontbreekt. Afhankelijk van het [ beleid DMARC ](#dmarc-policies) u wilt toepassen, selecteer één van de drie opties:

   * **[!UICONTROL None]** (standaardwaarde): geeft aan dat de ontvanger geen acties mag uitvoeren tegen berichten die geen DMARC-verificatie hebben, maar wel e-mailrapporten moet verzenden naar de afzender.
   * **[!UICONTROL Quarantine]**: hiermee wordt aan de ontvangende e-mailserver doorgegeven dat DMARC-verificatie mislukt. Dit betekent doorgaans dat de berichten in de spam- of junkmap van de ontvanger worden geplaatst.
   * **[!UICONTROL Reject]**: geeft aan dat de ontvanger alle e-mails voor het domein waarvoor de verificatie mislukt, volledig moet weigeren (stuiteren). Als dit beleid is ingeschakeld, heeft alleen e-mail die is geverifieerd als 100% en die voor uw domein is geverifieerd, een kans bij plaatsing in het postvak.

   >[!NOTE]
   >
   >Als beste praktijken, wordt het geadviseerd om implementatie DMARC langzaam uit te voeren door uw beleid DMARC van **te escaleren niets**, aan **Quarantine**, aan **Weigeren** aangezien u inzicht in het potentiële effect van DMARC krijgt.

1. Naar keuze, voeg één of meerdere e-mailadressen van uw keus toe om erop te wijzen waar **DMARC** op e-mail meldt dat [ authentificatie ](#how-dmarc-works) binnen uw organisatie zou ontbreken. U kunt maximaal vijf adressen voor elk rapport toevoegen.

   >[!NOTE]
   >
   >Zorg ervoor u echte inbox (niet Adobe) in uw controle hebt waar u die rapporten kunt ontvangen.

   Er zijn twee verschillende rapporten die door ISPs worden geproduceerd die de afzenders door de markeringen RUA/RUF in hun beleid kunnen ontvangen DMARC:

   * **samengevoegde rapporten** (RUA): Zij bevatten geen PII (Persoonlijk Identificeerbare Informatie) die GDPR-gevoelig zou kunnen zijn.
   * **Forensische mislukkingsrapporten** (RUF): Zij bevatten GDPR-Gevoelige e-mailadressen. Voordat u gaat gebruiken, controleert u intern hoe u omgaat met informatie die compatibel moet zijn met GDPR.

   >[!NOTE]
   >
   >Deze hoogst technische rapporten verstrekken een overzicht van e-mails die voor de gek houden worden geprobeerd. U kunt ze het beste verteren met een hulpprogramma van derden.

1. Selecteer het **toepasselijke percentage** van e-mails voor DMARC.

   Dit percentage is afhankelijk van uw vertrouwen in uw e-mailinfrastructuur en de tolerantie voor valse positieven (legitieme e-mails die als frauduleus worden gemarkeerd). Het is gemeenschappelijk voor organisaties om met beleid te beginnen DMARC dat aan **wordt geplaatst niets**, verhoogt geleidelijk het DMARC beleidspercentage, en controleert dicht het effect op wettige e-maillevering.

   >[!NOTE]
   >
   >Werk samen met uw e-mailbeheerders en IT-team om het percentage geleidelijk te verhogen terwijl u vertrouwen krijgt in uw e-mailverificatiepraktijken.

   Als beste praktijk, streven naar een hoog DMARC nalevingspercentage, idealiter dicht bij 100%, om de veiligheidsvoordelen te maximaliseren terwijl het risico van valse positieven minimaliseert.

1. Selecteer a **rapporterend interval** tussen 24 en 168 uren. Hiermee kunnen eigenaars van domeinen regelmatig updates ontvangen over de resultaten van e-mailverificatie en de nodige maatregelen nemen om de e-mailbeveiliging te verbeteren.

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->
