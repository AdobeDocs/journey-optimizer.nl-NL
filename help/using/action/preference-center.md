---
solution: Journey Optimizer
product: journey optimizer
title: De voorkeuren van uw klanten beheren
description: Leer hoe u de voorkeuren van gebruikers kunt beheren met behulp van het beleid voor machtigingen
feature: Journeys, Privacy, Consent Management, Landing Pages
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: beleid, bestuur, platform, toestemming, gezondheidszorgschild
hide: true
hidefromtoc: true
source-git-commit: 95f101c3d8f875dbf7988f10b106fc58f705e926
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# De voorkeuren van uw klanten beheren {#preference-center}

>[!AVAILABILITY]
>
>Dit vermogen is momenteel slechts beschikbaar voor organisaties die het 3} toe:voegen-op dienstenaanbod van het Schild van de Gezondheidszorg van Adobe **of** Privacy en van het Schild van de Veiligheid {hebben gekocht.****

In een modern ecosysteem voor marketingautomatisering werken merken met klanten in verschillende aanraakpunten, waarbij ze het risico lopen van irrelevante of excessieve communicatie, wat leidt tot terugtrekking, spamklachten en nalevingsrisico&#39;s. Daarom moeten zij de voorkeuren van hun klanten beheren om inzicht in real time over hun publiek te verwerven en gepersonaliseerde, respectvolle mededeling te leveren.

Met [!DNL Adobe Journey Optimizer], door het gebruik van [ toestemmingsbeleid ](consent.md), kunt u de voorkeur van uw klanten <!-- in terms of **channels** and **topics**--> eren. Dit zorgt ervoor dat [!DNL Journey Optimizer] slechts klanten richt die op hun keuzen <!-- their preferred channels and on the subscription topics--> worden gebaseerd, terwijl het respecteren van hun toestemming.

Als u de gebruikersvoorkeuren wilt beheren met [!DNL Journey Optimizer] , kunt u:

* Haal de toestemming van uw klanten op om in of uit te kiezen voor een native uitgaand kanaal. Maak bijvoorbeeld een toestemmingsbeleid in [!DNL Experience Platform] om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van communicatie voor een bepaald kanaal. Pas vervolgens dit toestemmingsbeleid toe in [!DNL Journey Optimizer] met behulp van een configuratie met een e-mailkanaal. [ leer hoe ](consent.md#surface-marketing-actions)

  >[!NOTE]
  >
  >De ondersteunde kanalen zijn Email, Push, SMS en InApp.<!--To check-->

* Vraag uw klanten welke onderwerpen zij om willen intekenen aan (zoals het type van mededelingen zij om overeenkomen te ontvangen of niet). [ leer hoe ](#manage-preferences)

>[!IMPORTANT]
>
>Goedkeuring heeft voorrang op voorkeuren. Bijvoorbeeld, wees één van uw klanten erop dat hun aangewezen kanaal e-mail is en dat zij ermee instemden om nieuwsbrieven <!-- they are interested in yoga--> te ontvangen; nochtans, als zij uit het ontvangen van om het even welke mededelingen van u verkozen, kunnen zij niet door een e-mailbulletin worden gericht dat u <!-- on yoga--> verzendt.

## Voorkeuren voor opnemen en respecteren {#manage-preferences}

Met het toestemmingsbeleid in [!DNL Journey Optimizer], kunt u de voorkeur van uw klanten centraal beheren. Dit staat u toe om ervoor te zorgen u slechts klanten richt die op de onderwerpen worden gebaseerd zij terwijl het eerbiedigen van hun toestemmingskeuzen selecteerden. Volg de onderstaande stappen om dit te doen.

Laten wij zeggen u uw klanten door reizen en campagnes wilt richten die op hun communicatie voorkeur over veelvoudige abonnementonderwerpen (*Nieuwsbrieven* worden gebaseerd, *Aanbiedingen*, en *Nieuwe Lanceringen van het Product*).

1. Bepaal voorkeur attributen met de exploitant Van Boole op het profielniveau <!--how??-->. U kunt bijvoorbeeld het volgende opgeven:

   * *Newsletter_Email* - Van Boole (waar/vals)
   * *Offers_Push* - Van Boole (waar/vals)
   * *Nieuwe Lanceringen van het Product* - Van Boole (waar/vals)

   Deze attributen worden gevangen in het schema van een profiel-toegelaten [ dataset ](../data/get-started-datasets.md) en in kaart gebracht aan het [ verenigde klantenprofiel ](../audience/get-started-profiles.md).

   >[!NOTE]
   >
   >De toestemming van de klant en de contactvoorkeur zijn complexe onderwerpen. Als u wilt weten hoe toestemmings- en contextvoorkeuren kunnen worden verzameld, verwerkt en gefilterd in [!DNL Experience Platform] , kunt u het beste de volgende documenten lezen:
   >
   >* Om over de groepen van het schemagebied te leren die worden vereist om toestemmingsgegevens te verzamelen, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview){target="_blank"}. Het details hoe te om toestemmingsgegevens te verwerken u van uw klanten hebt verzameld en het in uw opgeslagen klantenprofielen te integreren.
   >* Om meer op de het gebiedsgroep van de Toestemming en van de Voorkeur te leren, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents#ingest){target="_blank"}.
   >* Om de gebieden van de douanevoorkeur aan het schema toe te voegen, volg de stappen in [ deze sectie ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/dataset#custom-consent){target="_blank"}.

1. Maak een pagina om de voorkeuren van uw klanten vast te leggen. Gebruik een van de volgende methoden:

   * Creeer een Web-pagina om de voorkeur van uw klanten te registreren gebruikend het [ Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home){target="_blank"}.

   * Gebruik a [!DNL Journey Optimizer] [ landende pagina ](../landing-pages/create-lp.md) die vormen omvat om de voorkeur van uw klanten door profielgegevens te vangen.  [ Leer meer op vormen ](../landing-pages/lp-forms.md) <!--Forms not released/announced yet - TBC-->

     >[!NOTE]
     >
     >Zorg ervoor dat het domein van de landingspagina die wordt gebruikt tot het merk op het hoogste niveau behoort en niet tot een submerk. Dit is om vertrouwen onder eindgebruikers te verzekeren. <!--Please clarify-->

1. Op deze pagina kunnen klanten hun voorkeuren, zoals abonnementen per onderwerp, bijwerken door selectievakjes in of uit te schakelen.

   Elke actie brengt een toestemmingsgebeurtenis teweeg die tegen de overeenkomstige profielattributen (`true` voor opted-in, `false` voor opted-out) door de gegevens in het profiel-Toegelaten datasetschema <!-- that contains the corresponding preference fields--> in te voeren wordt opgeslagen.

   <!--Record your users' preferences through the web page or landing page that you created. The data is saved against the corresponding profile, meaning that the preference data is ingested into a Profile-enabled dataset whose schema contains consent/preference fields.-->

   Een gebruiker <!--whose email address is john.black@lumamail.com--> heeft bijvoorbeeld ingestemd met pushaanbiedingen, maar wil geen e-mailnieuwsbrieven ontvangen. Het bijbehorende profiel wordt als volgt bijgewerkt:

   ![](assets/profile-preference-attributes.png){width=80%}

<!--The corresponding profile dataset is updated as follows:

|Attribute = Email id | Attribute = Offers_Push | Attribute = Newsletters_Email |
|---------|----------|---------|
| john.black@lumamail.com | Y | N |-->

    >[!NOTE] 
    > 
    >De inkomende toestemmingsgebeurtenissen voeren in het klantenprofiel in, die updates in real time verzekeren. Elk profiel weerspiegelt hun meest recente keuzes in de abonnementsvoorkeuren.

1. Maak in Adobe Experience Platform een aangepast beleid (via het menu **[!UICONTROL Privacy]** > **[!UICONTROL Policies]** ). [ leer hoe ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-policy){target="_blank"}

   >[!AVAILABILITY]
   >
   >Het toestemmingsbeleid is momenteel slechts beschikbaar voor organisaties die het 3} toe:voegen-op dienstenaanbod van het Schild van de Gezondheidszorg van Adobe **of** of **Privacy en van het Schild van de Veiligheid {hebben gekocht.** [ leer meer over toestemmingsbeleid ](consent.md)

   Om gebruik te kunnen maken van toestemmingsbeleid, moeten voorkeurattributen in de profielgegevens aanwezig zijn. Daarom moet u deze kenmerken definiëren op profielniveau (zoals beschreven in stap 1).

1. Kies het type **[!UICONTROL Consent policy]** en configureer een voorwaarde als volgt. [ leer hoe te om toestemmingsbeleid te vormen ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy){target="_blank"}

<!--Consent policies are comprised of two logical components:

* **If**: The condition that will trigger the policy check, based on a certain marketing action (email, SMS, push, custom action, etc.) being performed, the presence of certain data usage labels, or a combination of the two.

* **Then**: The consent attribute must be present for a profile to be included in the action that triggered the policy. More than one field can also be selected.-->

     bijvoorbeeld, om mededelingen slechts naar uw klanten te verzenden die niet van het ontvangen van e-mailbulletins hebben gekozen, creeer een douanebeleid en bepaal de volgende voorwaarde:
    
     * Als **[!UICONTROL Marketing action] *** evenaart ** [!UICONTROL Email] ** 
    
     * toen * * [!UICONTROL Newsletter_Email] * * * * niet bestaat ** [!UICONTROL false] * of * ** [!UICONTROL Newsletter_Email] * niet evenaart **[!UICONTROL false]* 
    
    }![] (assets/consent-policy-email-newsletter.png){width=80%} 
    
    >[!TIP] 
    > 
    >De profiel-Toegelaten dataset moet de profielattributen ** [!UICONTROL Newsletter_Email]* met de waarde omvatten die aan &quot;waar ` wordt geplaatst (zoals die in stap 1 wordt beschreven.) 

1. Zodra u het toestemmingsbeleid creeerde, hefboomwerking het in [!DNL Journey Optimizer] gebruikend [ kanaalconfiguraties ](consent.md#surface-marketing-actions) of [ de acties van de reisdouane ](consent.md#journey-custom-actions).

1. Nu kunt u deze kanaalconfiguraties of aangepaste acties tijdens uw reizen en campagnes gebruiken om ervoor te zorgen dat de voorkeuren van uw klanten voor <!--targeted--> worden gerespecteerd.
