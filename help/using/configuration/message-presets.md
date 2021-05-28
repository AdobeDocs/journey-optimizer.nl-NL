---
title: Branding van inhoud
description: Meer informatie over xxxx
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: 364861beb52e5663389a254ba145b31431b696ac
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---


# Voorinstellingen voor berichten maken

Met [!DNL Journey Optimizer] kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten (e-mailtype, e-mail en naam van de afzender, mobiele apps, enz.).

Afhankelijk van de verschillende merken waarvoor u moet communiceren, kunt u zoveel voorinstellingen voor berichten instellen als u wilt.

Nadat berichtvoorinstellingen zijn geconfigureerd, kunt u deze selecteren bij het maken van berichten in de lijst **[!UICONTROL Presets]**.

## Een berichtvoorinstelling maken {#create-message-preset}

Ga als volgt te werk om een berichtvoorinstelling te maken:

1. Open het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** en klik vervolgens op **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Geef een naam en een beschrijving (optioneel) voor de voorinstelling op en geef vervolgens het kanaal of de kanalen op die u wilt configureren.

   ![](../assets/preset-general.png)

1. Configureer de instellingen voor e-mail- en pushmeldingen:

   Geef voor het e-mailkanaal het volgende op:

   * Het type communicatie dat met de voorinstelling wordt verzonden (transactie- of marketingberichten),
   * Het [subdomein](about-subdomain-delegation.md) om de e-mails te verzenden,
   * De [IP pool](ip-pools.md) om aan vooraf ingesteld te associëren,
   * De headerparameters die moeten worden gebruikt voor de e-mails die worden verzonden met behulp van de voorinstelling.

   ![](../assets/preset-email.png)

   Voor het kanaal van het dupbericht, specificeer IOS en/of mobiele toepassingen Android voor uw berichten te gebruiken. Raadpleeg [deze sectie](../push-configuration.md) voor meer informatie over het configureren van uw omgeving voor het verzenden van pushberichten.

   ![](../assets/preset-push.png)

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** om te bevestigen. U kunt de berichtvoorinstelling ook opslaan als concept en de configuratie ervan later hervatten.

   ![](../assets/preset-submit.png)

1. Nadat de berichtvoorinstelling is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Processing]**.

   Tijdens deze stap, zullen verscheidene controles worden uitgevoerd om te verifiëren dat het behoorlijk is gevormd. De verwerkingstijd is ongeveer 48u-72u, en kan tot 7-10 dagen vergen.

   Deze controles omvatten leverbaarheidstests die door het team van de Adobe worden uitgevoerd:

   * SPF-validatie,
   * DKIM-validatie,
   * MX-recordvalidatie,
   * Controleer de zwarte lijst van IP&#39;s,
   * Helo host check,
   * verificatie van de IP-pool;
   * A/PTR-record, t/m/res-subdomeinverificatie.

1. Als de controles zijn voltooid, krijgt de berichtvoorinstelling de status **[!UICONTROL Active]**. Het is klaar om te worden gebruikt om berichten te leveren.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Voorinstellingen voor monitorberichten

Alle voorinstellingen voor berichten worden weergegeven in het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**. Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren (kanaaltype, gebruiker, status).

![](../assets/preset-filters.png)

Voorinstellingen voor berichten kunnen de volgende statussen hebben:

* **[!UICONTROL Draft]**: De berichtvoorinstelling is opgeslagen als een concept en is nog niet verzonden. Open het om de configuratie te hervatten.
* **[!UICONTROL Processing]**: De berichtvoorinstelling is verzonden en wordt door verschillende verificatiestappen uitgevoerd.
* **[!UICONTROL Active]**: De berichtvoorinstelling is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de berichtvoorinstelling.
* **[!UICONTROL De-activated]**: De berichtvoorinstelling is gedeactiveerd. Het kan niet worden gebruikt om nieuwe berichten tot stand te brengen.

## Voorinstellingen voor berichten bewerken

Als u een berichtvoorinstelling wilt bewerken, moet u deze eerst deactiveren zodat deze niet beschikbaar is voor het maken van nieuwe berichten (gepubliceerde berichten met deze voorinstelling worden niet beïnvloed en blijven werken). Vervolgens moet u de berichtvoorinstelling dupliceren om een nieuwe versie te maken waarmee u nieuwe berichten kunt maken:

1. Open de lijst met voorinstellingen voor berichten en deactiveer vervolgens de berichtvoorinstelling die u wilt bewerken.

   ![](../assets/preset-deactivate.png)

1. Dupliceer de uitgeschakelde berichtvoorinstelling. Er wordt automatisch een kopie met de status **[!UICONTROL Draft]** toegevoegd aan de lijst.

   ![](../assets/preset-duplicated.png)

1. Open de gedupliceerde voorinstelling voor berichten, wijzig deze naar wens en verzend uw wijzigingen. De berichtvoorinstelling doorloopt dezelfde validatiecyclus als tijdens de [aanmaakstap](#create-message-preset).

1. Zodra bevestigd, krijgt het de **[!UICONTROL Active]** status en is klaar om worden gebruikt om nieuwe berichten tot stand te brengen.

   >[!NOTE]
   >
   >De-geactiveerde berichtvoorinstellingen kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze voorinstellingen worden gebruikt om berichten te verzenden.

<!-- To add when questions are answered + add link to this section in Create message presets section.

## Header parameters

The fields below allow you to enter information necessary to elaborate email message headers. This information can be personalized??

>[!NOTE]
>
>All fields are required.


To define the name and address of the sender which will appear in the header of messages sent, edit the settings below:

**[!UICONTROL Sender email]**: Address of the sender

**[!UICONTROL Sender name]**: Name of the sender. you can change the sender name

**[!UICONTROL Reply to (email)]**: The email address to use when the recipient clicks the Reply button in their e-mail client software,

**[!UICONTROL Reply to (name)]**: The name, which is customizable, that will be used when the recipient clicks the Reply button in their e-mail client software,

**[!UICONTROL Reply to (forward email)]**:
Cf. https://jira.corp.adobe.com/browse/CJM-9824

**[!UICONTROL Error email]**: Email address of messages with errors. This is the technical address used to handle bounce mail, including emails received by the AJO server due to non-existent target addresses.
This fields is automatically populated with the value you add in the Reply to (forward email) field.

>[!NOTE]
>
>The sender’s address will be used for replies by default.
>The header parameters must not be empty. By default, they contain the values input >when configuring the deployment wizard??
>The sender’s address is mandatory to allow an email to be sent (RFC standard).
Journey Optimizer checks the syntax of email addresses entered.

>[!CAUTION]
>
>In the context of the checks implemented by Internet Access Providers (ISPs) to combat unsolicited email (spam), Adobe recommends creating email accounts that correspond to the addresses specified for deliveries and replies. Check with your messaging system administrator.-->

