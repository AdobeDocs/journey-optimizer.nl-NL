---
solution: Journey Optimizer
product: journey optimizer
title: E-mailuitschakelbeheer
description: Ervaar hoe u de optie om te weigeren beheert met e-mails
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: opt-out, e-mail, link, abonnement opzeggen
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: 38496b93f073c0e9cb208b0c62e6c4cb8a2d8c03
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 0%

---

# E-mailuitschakelbeheer {#email-opt-out}

Wanneer het verzenden van berichten van reizen of campagnes, moet u altijd ervoor zorgen dat de klanten van toekomstige mededelingen kunnen opzeggen. Als u het abonnement opzegt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten.  [Meer informatie over privacy- en opt-outbeheer](../privacy/opt-out.md)

>[!NOTE]
>
>In al uw marketingberichten moet een koppeling naar de optie Weigeren zijn opgenomen. Dit is niet vereist voor transactieberichten. De berichtcategorie - **[!UICONTROL Marketing]** of **[!UICONTROL Transactional]** - wordt gedefinieerd op de [kanaaloppervlak](../configuration/channel-surfaces.md#email-type) niveau en bij het maken van het bericht.

Als u een koppeling zonder abonnement wilt invoegen in uw e-mailinhoud, kunt u:

* Voeg één klik toe unsubscribe URL in de e-mailkopbal. Het inschakelen van de **[!UICONTROL List-Unsubscribe Header]** Hiermee voegt u een uitschakelkoppeling toe aan de koptekst van de e-mail. [Meer informatie over opt-out in e-mailkoptekst](#unsubscribe-header)

* De optie **one-click opt-out link** voor uw e-mail.  [Meer informatie over het toevoegen van een koppeling om te weigeren met één klik](#one-click-opt-out)

* Een **koppeling naar een bestemmingspagina**. [Meer informatie over het toevoegen van een bestemmingspagina met de optie Weigeren](#opt-out-external-lp)


## Eén stap voor opt-out {#opt-out-one-step}

### Klik eenmaal op URL voor abonnement opheffen in de e-mailheader {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Afmelde URL toevoegen in de koptekst van de e-mail"
>abstract="Schakel List-Unsubscribe Header in om een niet-geabonneerde URL toe te voegen in de e-mailkoptekst. Als u een URL voor afmelden wilt instellen, voegt u een koppeling om te weigeren in de e-mailinhoud in."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#one-click-opt-out" text="Eén klik op Weigeren"

Een-klik lijst voor annuleren URL is een afmeldingskoppeling of knop die wordt weergegeven naast de e-mailverzendgegevens en biedt ontvangers de mogelijkheid om met één klik direct te weigeren in uw mailinglijsten. In Adobe Journey Optimizer, wanneer **List-Unsubscribe inschakelen** Als deze optie is ingeschakeld, bevat de koptekst van de e-mail standaard zowel een mailto als een URL waarmee ontvangers zich van uw mailinglijst kunnen afmelden.

De [List-Unsubscribe inschakelen](email-settings.md#list-unsubscribe) De schakeloptie moet op het niveau van de kanaaloppervlakte worden geactiveerd zodat e-mails die dit oppervlak gebruiken de éénklikige niet-abonneeURL in de e-mailkoptekst bevatten.

>[!NOTE]
>
>Als u één klik wilt weergeven, klikt u op de URL voor afmelden in de e-mailheader, moet de e-mailclient van de ontvangers deze functie ondersteunen.


Met de URL voor het afmelden van abonnementen met één klik wordt bijvoorbeeld een koppeling voor het afmelden van abonnementen als deze weergegeven in Gmail:

![](assets/unsubscribe-header.png)


Met Adobe Journey Optimizer kunt u de instellingen van uw e-mailoppervlak configureren met een automatisch gegenereerde klik op URL en mailto-adres opzeggen in de koptekst van de e-mail. U kunt ook een één-klik-URL opnemen in de hoofdtekst van de e-mail: wanneer een ontvanger op de één-klik-optie-out klikt, wordt de aanvraag voor het opzeggen van het abonnement van de ontvanger dienovereenkomstig verwerkt.

<!--
>[!AVAILABILITY]
>
>One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
>
-->

Afhankelijk van de e-mailclient en de [Abonnementsinstellingen voor e-mailoppervlak](email-settings.md#list-unsubscribe)Als u klikt op de koppeling voor het afmelden van uw abonnement in de e-mailheader, heeft dit mogelijk de volgende gevolgen:

* Wanneer de **Mailto (afmelden)** -functie wordt door u ingeschakeld, wordt de aanvraag voor afmelden verzonden naar het standaardadres voor afmelden op basis van het subdomein dat door u is gemaakt.
* Wanneer de **Eén klik op URL voor abonnement opzeggen** -functie wordt ingeschakeld door u - of als u een niet-abonnements-URL hebt ingevoegd in de inhoud van de e-mail -, wordt de ontvanger direct uitgepakt, op kanaalniveau of op id-niveau (afhankelijk van hoe de toestemming is ingesteld), wanneer de ontvanger klikt op de éénklikige niet-abonneeURL, die is gebaseerd op het subdomein dat door u is gemaakt.

In beide gevallen wordt het corresponderende profiel voor de ontvanger onmiddellijk uitgeschakeld en wordt deze keuze in het Experience Platform bijgewerkt. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

Als u de optie **[!UICONTROL Enable List-Unsubscribe]** ten aanzien van de header List Unsubscribe raden we u aan beide methoden in te schakelen - **Mailto (afmelden)** en **URL voor abonnement met één klik opheffen**. Niet alle e-mailclients ondersteunen de HTTP-methode. Met de lijst-unsubscribe van de Brievenbus eigenschap die als functionaliteit voor u wordt verstrekt om een alternatief te selecteren, kan uw afzenderreputatie beter worden beschermd en al uw ontvangers kunnen toegang hebben om de unsubscribe functionaliteit te gebruiken. [Meer informatie](email-settings.md#list-unsubscribe)


### Eén klik op Weigeren in de e-mailinhoud {#one-click-opt-out}

Als u een gepersonaliseerde URL voor annuleren wilt instellen, voegt u een koppeling voor een eenmalige aanmelding in de inhoud van het e-mailbericht in en voert u de URL van uw keuze in, zoals hieronder wordt beschreven:

1. Toegang tot uw e-mailinhoud en [een koppeling invoegen](../email/message-tracking.md#insert-links).
1. Selecteren **[!UICONTROL One click Opt-out]** als het type koppeling.

   ![](assets/message-tracking-opt-out.png)

1. Voer de URL in van de bestemmingspagina waarop de gebruiker wordt omgeleid zodra het abonnement is opgezegd. Deze pagina is hier om te bevestigen dat het afmelden is gelukt.

   >[!NOTE]
   >
   >Als u de optie **[!UICONTROL List-Unsubscribe]** in de [kanaaloppervlak](email-settings.md#list-unsubscribe) en als de standaard URL voor weigeren met één klik is uitgeschakeld, wordt deze URL gebruikt wanneer gebruikers op de koppeling voor het afmelden van abonnementen in de e-mailheader klikken. [Meer informatie](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   U kunt uw koppelingen aanpassen. Meer informatie over gepersonaliseerde URL&#39;s vindt u in [deze sectie](../personalization/personalization-syntax.md).

1. Selecteer hoe u de optie Weigeren wilt toepassen: op het kanaal, de identiteit of het abonnementsniveau.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: De optie om te weigeren is van toepassing op toekomstige berichten die naar het doel van het profiel (e-mailadres) voor het huidige kanaal worden verzonden. Als er meerdere doelen aan een profiel zijn gekoppeld, geldt de opt-out voor alle doelen (e-mailadressen) in het profiel voor dat kanaal.
   * **[!UICONTROL Identity]**: De opt-out is van toepassing op toekomstige berichten die worden verzonden naar het specifieke doel (d.w.z. e-mailadres) dat voor het huidige bericht wordt gebruikt.
   * **[!UICONTROL Subscription]**: De optie om te weigeren is van toepassing op toekomstige berichten die aan een specifieke abonnementenlijst zijn gekoppeld. Deze optie kan alleen worden geselecteerd als het huidige bericht is gekoppeld aan een abonnementenlijst.

1. Sla uw wijzigingen op.



## Optie in twee stappen {#opt-out-external-lp}

Het standaardmechanisme voor opt-out is gebaseerd op twee stappen: de abonnee klikt in een e-mail op de koppeling om te weigeren en vervolgens wordt hij omgeleid naar een bestemmingspagina om zijn abonnement te bevestigen.

Als u deze uitstapmodus wilt implementeren, moet u een bestemmingspagina voor een opt-out maken en publiceren en een koppeling voor een abonnement toevoegen in uw e-mailberichten met een koppeling naar de bestemmingspagina. Deze stappen worden hieronder beschreven.


### Vereisten {#prereq-lp}

Als u een systeem met twee stappen wilt instellen voor het weigeren van toegang, moet u uw eigen bestemmingspagina&#39;s voor abonnementen maken. De eerste het landen pagina zal van uw bericht worden verbonden en moet een vraag-aan-actie knoop bevatten. Er moet een bevestigingsbericht worden weergegeven wanneer de gebruiker op de knop klikt.

Leer hoe u een bestemmingspagina maakt in Adobe Journey Optimizer om abonnementen te beheren in [deze pagina](../landing-pages/lp-use-cases.md#opt-out).

U kunt ook een externe bestemmingspagina gebruiken. In dat geval configureert u de API zodanig dat de informatie naar Adobe Journey Optimizer wordt verzonden wanneer een ontvanger zich niet meer abonneert.

+++ Leer hoe u een opt-out API-aanroep implementeert

Als u wilt dat de ontvangers de optie Weigeren kiezen wanneer ze hun keuze op de bestemmingspagina indienen, moet u een **API-oproep voor abonnement** doorheen [Adobe Developer](https://developer.adobe.com){target="_blank"} om de voorkeuren van de overeenkomstige profielen bij te werken.

Deze vraag van de POST is als volgt:

Eindpunt: https://platform.adobe.io/journey/imp/consent/preferences

Parameters query:

* **param**: bevat de gecodeerde payload
* **pid**: gecodeerde profiel-id

Deze drie parameters worden opgenomen in de URL van de bestemmingspagina van derden die naar de ontvanger wordt verzonden:

![](assets/opt-out-parameters.png)

Eisen voor koptekst:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorisatie (gebruikerstoken van uw technische account)

Instantie van aanvraag:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] gebruikt deze parameters om de keuze van het corresponderende profiel bij te werken via de [Adobe Developer](https://developer.adobe.com){target="_blank"} API-aanroep.

+++


### Koppeling voor annuleren toevoegen {#add-unsubscribe-link}

Eerst moet u een afmeldingskoppeling toevoegen aan een bericht. Hiervoor voert u de volgende stappen uit:

1. Maak een bericht en [een koppeling invoegen](../email/message-tracking.md#insert-links) gebruiken van de contextafhankelijke werkbalk.

   ![](assets/opt-out-insert-link.png)

1. Selecteer de **[!UICONTROL Landing page]** van de **[!UICONTROL Type]** vervolgkeuzelijst en selecteer de bestemmingspagina van de optie Weigeren in de **[!UICONTROL Landing page]** veld.

   Als u een externe bestemmingspagina gebruikt, selecteert u **[!UICONTROL External Opt-out/Unsubscription]** van de **[!UICONTROL Type]** vervolgkeuzelijst.

   ![](assets/opt-out-link-type.png)

   In de **[!UICONTROL Link]** plakken, plakt u de koppeling naar de bestemmingspagina van derden.

   ![](assets/opt-out-link-url.png)

1. Klik op **[!UICONTROL Save]**.


### Bericht verzenden met afmeldingskoppeling {#send-message-unsubscribe-link}

Zodra u de unsubscribe verbinding aan uw landende pagina vormde, kunt u uw bericht creëren en verzenden.

1. Vorm uw bericht met een unsubscription verbinding en verzend het naar uw abonnees.

1. Zodra het bericht wordt ontvangen, als de ontvanger de unsubscribe verbinding klikt, wordt uw landende pagina getoond.

   ![](assets/opt-out-lp-example.png)

1. Indien de ontvanger het formulier indient - hier, door op de **[!UICONTROL Unsubscribe]** op uw landingspagina - de profielgegevens worden bijgewerkt via de API-aanroep.

1. De ontvanger van de optie-uit wordt dan opnieuw gericht aan een bevestigingsberichtscherm erop wijzend dat het kiezen uit succesvol was.

   ![](assets/opt-out-confirmation-example.png)

   Dit heeft tot gevolg dat deze gebruiker geen communicatie van uw merk ontvangt, tenzij hij opnieuw een abonnement neemt.

1. Als u wilt controleren of de keuze van het corresponderende profiel is bijgewerkt, gaat u naar het Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   In de **[!UICONTROL Attributes]** tab, kunt u de waarde zien voor **[!UICONTROL choice]** is gewijzigd in **[!UICONTROL no]**.

