---
solution: Journey Optimizer
product: journey optimizer
title: E-mailuitschakelbeheer
description: Ervaar hoe u de optie om te weigeren beheert met e-mails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---

# E-mailuitschakelbeheer {#email-opt-out}

Als u ontvangers de mogelijkheid wilt bieden zich af te melden voor het ontvangen van e-mailberichten, moet u altijd een **afmelden, koppeling** in elke e-mail die naar ontvangers wordt verzonden. [Meer informatie over privacy- en opt-outbeheer](../privacy/opt-out.md)

Hiervoor kunt u:

* Een **koppeling naar een externe bestemmingspagina** in een e-mail om gebruikers in staat te stellen zich af te melden voor het ontvangen van communicatie van uw merk. [Meer informatie over het toevoegen van een externe uitschakelkoppeling](#opt-out-external-lp)

* Voeg een **one-click opt-out link** in uw e-mailinhoud. Deze verbinding zal uw ontvangers toestaan om van uw mededelingen snel af te zien, zonder aan een landende pagina worden opnieuw gericht waar zij hun keus moeten bevestigen, die het afmeldingsproces versnellen. [Meer informatie over het toevoegen van een koppeling om te weigeren met één klik](#one-click-opt-out)

Als de **[!UICONTROL List-Unsubscribe]** is ingeschakeld op het niveau van het kanaaloppervlak. De bijbehorende e-mails die met Journey Optimizer worden verzonden, bevatten een koppeling voor het afmelden van abonnementen in de e-mailheader. [Meer informatie over opt-out in e-mailkoptekst](#unsubscribe-header)

>[!NOTE]
>
>E-mailberichten van het type Marketing moeten een opt-out-koppeling bevatten, die niet vereist is voor transactiemeldingen. De berichtcategorie (**[!UICONTROL Marketing]** of **[!UICONTROL Transactional]**) wordt gedefinieerd op de [kanaaloppervlak](../configuration/channel-surfaces.md#email-type) (d.w.z. vooraf ingestelde berichten) en bij het maken van het bericht).

## Externe opt-out {#opt-out-external-lp}

### Koppeling voor annuleren toevoegen {#add-unsubscribe-link}

Eerst moet u een afmeldingskoppeling toevoegen aan een bericht. Volg de onderstaande stappen om dit te doen:

1. Bouw uw eigen bestemmingspagina zonder abonnement.

1. De gastheer het op het derdesysteem van uw keus.

1. Maak een bericht op een reis.

1. Selecteer tekst in uw inhoud en [een koppeling invoegen](../email/message-tracking.md#insert-links) gebruiken van de contextafhankelijke werkbalk.

   ![](assets/opt-out-insert-link.png)

1. Selecteren **[!UICONTROL External Opt-out/Unsubscription]** van de **[!UICONTROL Link type]** vervolgkeuzelijst.

   ![](assets/opt-out-link-type.png)

1. In de **[!UICONTROL Link]** , plakt u de koppeling naar de bestemmingspagina van derden.

   ![](assets/opt-out-link-url.png)

1. Klik op **[!UICONTROL Save]**.

### Een API-aanroep voor opt-out implementeren {#opt-out-api}

Als u wilt dat de ontvangers de optie Weigeren kiezen wanneer ze hun keuze op de bestemmingspagina indienen, moet u een **API-oproep voor abonnement** doorheen [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} om de voorkeuren van de corresponderende profielen bij te werken.

Deze vraag van de POST is als volgt:

Eindpunt: platform.adobe.io/journey/imp/consent/preferences

Parameters query:

* **param**: bevat de gecodeerde lading
* **sig**: handtekening
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

[!DNL Journey Optimizer] gebruikt u deze parameters om de keuze van het corresponderende profiel bij te werken via de [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} API-aanroep.

### Bericht verzenden met afmeldingskoppeling {#send-message-unsubscribe-link}

Zodra u de unsubscribe verbinding aan uw landende pagina vormde en de API vraag uitvoerde, is uw bericht klaar om te worden verzonden.

1. Verzend het bericht inclusief de koppeling via een [reis](../building-journeys/journey.md).

1. Zodra het bericht wordt ontvangen, als de ontvanger de unsubscribe verbinding klikt, wordt uw landende pagina getoond.

   ![](assets/opt-out-lp-example.png)

1. Indien de ontvanger het formulier indient (hier door op de **Abonnement opzeggen** (in uw bestemmingspagina), worden de profielgegevens bijgewerkt via [API-aanroep](#opt-out-api).

1. De ontvanger van de optie-uit wordt dan opnieuw gericht aan een bevestigingsberichtscherm erop wijzend dat het kiezen uit succesvol was.

   ![](assets/opt-out-confirmation-example.png)

   Dit heeft tot gevolg dat deze gebruiker geen communicatie van uw merk ontvangt, tenzij hij opnieuw een abonnement neemt.

1. Als u wilt controleren of de keuze van het corresponderende profiel is bijgewerkt, gaat u naar het Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   In de **[!UICONTROL Attributes]** tab, kunt u de waarde zien voor **[!UICONTROL choice]** is gewijzigd in **[!UICONTROL no]**.

## Eén klik op Weigeren {#one-click-opt-out}

Volg onderstaande stappen om een koppeling om te weigeren toe te voegen in uw e-mail.

1. [Een koppeling invoegen](../email/message-tracking.md#insert-links) en selecteert u **[!UICONTROL One click Opt-out]** als het type koppeling.

   ![](assets/message-tracking-opt-out.png)

1. Selecteer hoe u de optie Weigeren wilt toepassen: op het kanaal, de identiteit, of abonnementsniveau.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: De opt-out is van toepassing op toekomstige berichten die naar het doel van het profiel (d.w.z. e-mailadres) voor het huidige kanaal worden verzonden. Als er meerdere doelen aan een profiel zijn gekoppeld, geldt de opt-out voor alle doelen (e-mailadressen) in het profiel voor dat kanaal.
   * **[!UICONTROL Identity]**: De opt-out is van toepassing op toekomstige berichten die worden verzonden naar het specifieke doel (d.w.z. e-mailadres) dat voor het huidige bericht wordt gebruikt.
   * **[!UICONTROL Subscription]**: De opt-out is van toepassing op toekomstige berichten verbonden aan een specifieke abonnementenlijst. Deze optie kan alleen worden geselecteerd als het huidige bericht is gekoppeld aan een abonnementenlijst.

1. Voer de URL in van de bestemmingspagina waarop de gebruiker wordt omgeleid wanneer het abonnement wordt opgezegd. Deze pagina is alleen hier om te bevestigen dat de optie Weigeren is gelukt.

   >[!NOTE]
   >
   >Als u de optie **List-Unsubscribe** Deze URL wordt ook gebruikt wanneer gebruikers op de koppeling Abonneren in de e-mailheader klikken. [Meer informatie](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   U kunt uw koppelingen aanpassen. Meer informatie over gepersonaliseerde URL&#39;s vindt u in [deze sectie](../personalization/personalization-syntax.md).

1. Sla uw wijzigingen op.

Zodra uw bericht door [reis](../building-journeys/journey.md)Als een ontvanger op de koppeling om te weigeren klikt, wordt zijn profiel onmiddellijk uitgeschakeld.

## Koppeling in e-mailkoptekst opzeggen {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Koppeling voor abonnement toevoegen aan e-mailkoptekst"
>abstract="Schakel List-Unsubscribe in om een koppeling voor afmelden aan de e-mailkoptekst toe te voegen. Als u een URL voor afmelden wilt instellen, voegt u een koppeling om te weigeren in de e-mailinhoud in."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#one-click-opt-out" text="Eén klik op Weigeren"

Als de [List-Unsubscribe, optie](../configuration/channel-surfaces.md#list-unsubscribe) is ingeschakeld op het niveau van het kanaaloppervlak, de bijbehorende e-mails die worden verzonden met [!DNL Journey Optimizer] zal een unsubscribe verbinding in de e-mailkopbal omvatten.

De koppeling voor afmelden wordt bijvoorbeeld als volgt weergegeven in Gmail:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Als u de koppeling voor afmelden in de e-mailheader wilt weergeven, moet de e-mailclient van de ontvangers deze functie ondersteunen.

Het afmeldingsadres is het standaardadres **[!UICONTROL Mailto (unsubscribe)]** adres dat in de overeenkomstige kanaaloppervlakte wordt getoond. [Meer informatie](../configuration/channel-surfaces.md#list-unsubscribe).

Als u een gepersonaliseerde URL voor afmelden wilt instellen, voegt u een koppeling voor een eenmalige aanmelding in de inhoud van het e-mailbericht in en voert u de gewenste URL in. [Meer informatie](#one-click-opt-out)

Afhankelijk van de e-mailclient kan het klikken op de koppeling voor het opzeggen van abonnementen in de koptekst de volgende effecten hebben:

* Het afmeldingsverzoek wordt verzonden naar het standaardadres voor afmelden.

* De ontvanger wordt verwezen naar de bestemmingspagina URL die u toen het toevoegen van de opt-out verbinding aan uw bericht specificeerde.

   >[!NOTE]
   >
   >Als u geen koppeling voor het uitschakelen van een muisklik toevoegt aan uw berichtinhoud, wordt er geen bestemmingspagina weergegeven.

* Het corresponderende profiel wordt direct uitgeschakeld en deze keuze wordt in het Experience Platform bijgewerkt. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.
