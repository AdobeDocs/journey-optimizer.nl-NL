---
solution: Journey Optimizer
product: journey optimizer
title: E-mailinstellingen configureren
description: Leer hoe te om lijst-Unsubscript op het niveau van de kanaalconfiguratie te vormen
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: instellingen, e-mail, configuratie
source-git-commit: 8e299b90f601cd931940a64e691e186894d4012e
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---

# Abonnement opzeggen{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Wanneer het vormen van een nieuwe configuratie van het e-mailkanaal, op [ selecterend subdomain ](email-settings.md#subdomains-and-ip-pools) van de lijst, toont de **[!UICONTROL Enable List-Unsubscribe]** optie.

![](assets/preset-list-unsubscribe.png)

## Abonnement op lijst opzeggen inschakelen {#enable-list-unsubscribe}

Deze optie is standaard ingeschakeld om een éénklik-URL voor annuleren op te nemen in de e-mailkoptekst, zoals:

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>Als u deze optie uitschakelt, wordt er geen één-klik-URL voor annuleren weergegeven in de e-mailkoptekst.

De header List unsubscribe biedt twee opties, die standaard zijn ingeschakeld, tenzij u een of beide opties uitschakelt:

![](assets/surface-list-unsubscribe.png){width="80%"}

* A **[!UICONTROL Mailto (unsubscribe)]** adres, dat het bestemmingsadres is waar unsubscribe verzoeken aan voor auto-verwerking worden verpletterd.

  In [!DNL Journey Optimizer], is het unsubscribe e-mailadres het standaard **[!UICONTROL Mailto (unsubscribe)]** adres dat in de kanaalconfiguratie wordt getoond, die op uw [ wordt gebaseerd geselecteerde subdomain ](#subdomains-and-ip-pools). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* De **[!UICONTROL One-click unsubscribe URL]**, die standaard de één-klik opt-out URL produceerde Lijst unsubscribe kopbal is, die op subdomein wordt gebaseerd u plaatst en in de montages van de kanaalconfiguratie vormde. <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

U kunt **[!UICONTROL Consent level]** van de overeenkomstige drop-down lijst selecteren. Dit kan specifiek zijn voor het kanaal of de profielidentiteit. Op basis van deze instelling wordt de toestemming bijgewerkt in [!DNL Adobe Journey Optimizer] wanneer een gebruiker zich afmeldt via de lijst en de URL voor afmelden in de koptekst van een e-mailbericht opzegt, op kanaalniveau of op ID-niveau.

De functies **[!UICONTROL Mailto (unsubscribe)]** en **[!UICONTROL One-click unsubscribe URL]** zijn optioneel.

Als u niet de standaard gegenereerde één-klik wilt gebruiken unsubscribe URL, kunt u de eigenschap uncheck. In het scenario waar de **[!UICONTROL Enable List-Unsubscribe]** optie wordt van een knevel voorzien en de **[!UICONTROL One-click Unsubscribe URL]** eigenschap is ongecontroleerd, als u a [ toe:voegen één-klik opt-out verbinding ](../email/email-opt-out.md#one-click-opt-out) aan een bericht dat gebruikend deze configuratie wordt gecreeerd, neemt de Lijst unsubscribe kopbal de één-klik opt-out verbinding op u in het lichaam van e-mail hebt opgenomen en gebruikt dat als één-klik unsubscribe URL waarde.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Als u geen opt-out-koppeling met één klik toevoegt aan de inhoud van het bericht en de standaardinstelling **[!UICONTROL One-click unsubscribe URL]** is uitgeschakeld in de instellingen voor kanaalconfiguratie, wordt er geen URL doorgegeven aan de e-mailkoptekst als onderdeel van de List unsubscribe header.

Leer meer bij het beheren van unsubscribe mogelijkheden binnen uw berichten in [ deze sectie ](../email/email-opt-out.md#unsubscribe-header).

## Abonnementsgegevens extern beheren {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definiëren hoe afmeldingsgegevens worden beheerd"
>abstract="**beheerde Adobe**: De toestemmingsgegevens worden beheerd door u binnen het systeem van Adobe.<br>**beheerde Klant**: De toestemmingsgegevens worden beheerd door u in een extern systeem en geen synchronisatie van toestemmingsgegevens wordt bijgewerkt in het systeem van Adobe tenzij in werking gesteld door u."

>[!AVAILABILITY]
>
>Dit vermogen wordt vrijgegeven in Beperkte Beschikbaarheid (LA) voor een kleine reeks klanten.

Als u toestemming buiten Adobe beheert, selecteert u de optie **[!UICONTROL Customer managed]** om een aangepast e-mailadres voor opzeggen in te voeren en uw eigen URL voor opzeggen met één klik.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>Als u de optie **[!UICONTROL Customer managed]** gebruikt, slaat Adobe geen gegevens voor annulering of toestemming op. Met de optie **[!UICONTROL Customer managed]** kiezen organisaties voor het gebruik van een extern systeem en zijn ze verantwoordelijk voor het beheer van hun gegevens over machtigingen in een dergelijk extern systeem. Er is geen automatische synchronisatie van toestemmingsgegevens tussen het externe systeem en [!DNL Journey Optimizer]. Elke synchronisatie van toestemmingsgegevens, die afkomstig is van het externe systeem voor het bijwerken van gegevens over gebruikersmachtigingen in [!DNL Journey Optimizer], moet door de organisatie als gegevensoverdracht worden geïnitieerd om de toestemmingsgegevens terug te sturen naar [!DNL Journey Optimizer] .

### De decoderings-API configureren {#configure-decrypt-api}

Als de optie **[!UICONTROL Customer managed]** is geselecteerd en u aangepaste eindpunten invoert en deze in een campagne of reis gebruikt, voegt [!DNL Journey Optimizer] enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming <!--sent to the custom endpoint --> wanneer uw ontvangers op de koppeling Unsubscribe klikken.

Deze parameters worden verzonden naar het eindpunt op een gecodeerde manier. Aldus, moet het externe toestemmingssysteem specifieke API door [ Adobe Developer ](https://developer.adobe.com) uitvoeren {target="_blank"} om de parameters te decrypteren die door Adobe worden verzonden.

De GET-aanroep om deze parameters op te halen is afhankelijk van de optie voor het opzeggen van het abonnement op de lijst die u gebruikt - **[!UICONTROL One-click unsubscribe URL]** of **[!UICONTROL Mailto (unsubscribe)]** .

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ Eén klik op URL voor annuleren

Als u met de optie **[!UICONTROL One-click unsubscribe URL]** op de koppeling Abonnement opzeggen klikt, wordt de abonnement van de gebruiker direct opgezegd.

De GET-oproep ziet er als volgt uit:

Eindpunt: https://platform.adobe.io/journey/imp/consent/decrypt

Parameters query:

* **params**: bevat de gecodeerde lading
* **pid**: Gecodeerde profiel identiteitskaart

Deze twee parameters worden opgenomen in de gebeurtenis voor het bijwerken van de toestemming die naar de aangepaste eindpunten wordt verzonden.

Eisen voor koptekst:

* x-api-key
* x-gw-ims-org-id
* autorisatie (gebruikerstoken van uw technische account)

+++

+++ Mailto (afmelden)

Als u de optie **[!UICONTROL Mailto (unsubscribe)]** gebruikt en op de koppeling Abonnement opzeggen klikt, wordt een ingevuld e-mailbericht verzonden naar het opgegeven afmeldingsadres.

De GET-oproep ziet er als volgt uit.

Eindpunt: https://platform.adobe.io/journey/imp/consent/decrypt

Parameters query:

* **emailParams**: koord dat de **params** (gecodeerde lading) en **pid** (gecodeerde profielidentiteitskaart) parameters bevat.

De **params** en **pid** parameters zullen in de gebeurtenis worden omvat van de toestemmingsupdate die naar de douaneeindpunten wordt verzonden.

Eisen voor koptekst:

* x-api-key
* x-gw-ims-org-id
* autorisatie (gebruikerstoken van uw technische account)

+++
