---
product: Journey Optimizer
audience: end-user
user-guide-title: Handleiding voor Journey Optimizer
user-guide-description: Gebruik Journey Optimizer om verbonden, contextuele en gepersonaliseerde ervaringen op te bouwen en te leveren aan uw klanten
type: Documentation
solution: Journey Optimizer
source-git-commit: d3f15c09194a50b95107fb84d680606a468f8644
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 20%

---

# Adobe Journey Optimizer Help {#using}

+ [Journey Optimizer-documentatie](ajo-home.md)
+ Nieuwe functies {#whats-new}
   + [Vroege aanvullende informatie](using/rn/e-release-notes.md)
   + [Opmerkingen bij de laatste release](using/rn/release-notes.md)
   + Opmerkingen bij vorige release {#previous-rn-new}
      + [2025](using/rn/release-notes-2025.md)
      + [2024](using/rn/release-notes-2024.md)
      + [2023](using/rn/release-notes-2023.md)
      + [2022](using/rn/release-notes-2022.md)
      + [2021](using/rn/release-notes-2021.md)
   + [Documentatie-updates](using/rn/documentation-updates.md)
   + [Verbeterd reiscanvas](using/rn/new-canvas.md)
+ Aan de slag{#get-started}
   + [Wat is Journey Optimizer](using/start/get-started.md)
   + Hulplijnen voor snel starten{#quick-start}
      + [Overzicht](using/start/quick-start.md)
      + [Aan de slag als een marketeter](using/start/path/marketer.md)
      + [Aan de slag als Data engineer](using/start/path/data-engineer.md)
      + [Aan de slag als beheerder](using/start/path/administrator.md)
      + [Aan de slag als ontwikkelaar](using/start/path/developer.md)
   + [Gebruikersinterface](using/start/user-interface.md)
   + [Zoeken, filteren en categoriseren](using/start/search-filter-categorize.md)
   + [Toegankelijkheid](using/start/accessibility.md)
   + [Playbooks voor gebruiksscenario&#39;s](using/start/playbooks.md)
   + [Werken met AI-assistent](using/start/ai-assistant.md)
   + [Guardrails](using/start/guardrails.md)
   + [Best practices](using/start/best-practices.md)
+ Journeys {#orchestrate-journeys}
   + [Aan de slag met reizen](using/building-journeys/journey.md)
   + Een journey maken{#create-journey}
      + [Uw eerste journey maken](using/building-journeys/journey-gs.md)
      + [De eigenschappen van uw reis instellen](using/building-journeys/journey-properties.md)
      + [Vorm en spoor uw reismetriek](using/building-journeys/success-metrics.md)
      + [Uw reis ontwerpen](using/building-journeys/using-the-journey-designer.md)
      + [Uw reis testen](using/building-journeys/testing-the-journey.md)
      + [Uw reis simuleren](using/building-journeys/journey-simulation.md)
      + [Uw reis publiceren](using/building-journeys/publishing-the-journey.md)
      + [Live melding op reis](using/building-journeys/report-journey.md)
   + Uw reizen beheren{#manage-journey}
      + [Bladeren en uw reizen filteren](using/building-journeys/journey-ui.md)
      + [Profielingang bij reizen](using/building-journeys/entry-management.md)
      + [Aanvullende identificatiecode bij door gebeurtenissen veroorzaakte reizen](using/building-journeys/supplemental-identifier.md)
      + [Tijdzonebeheer](using/building-journeys/timezone-management.md)
      + [Send-Time optimalisatie](using/building-journeys/send-time-optimization.md)
      + [Beëindig uw reis](using/building-journeys/end-journey.md)
      + [Een journey naar een andere sandbox kopiëren](using/building-journeys/copy-to-sandbox.md)
      + [Uw reis oplossen](using/building-journeys/troubleshooting.md)
      + [Binnenkomende acties tijdens reizen oplossen](using/building-journeys/troubleshooting-inbound.md)
      + [ integreren met de Intelligente Diensten ](using/building-journeys/ai-services-overview.md)
   + Activiteiten {#about-journey-building}
      + [Aan de slag met reisactiviteiten](using/building-journeys/about-journey-activities.md)
      + [Algemene gebeurtenissen](using/building-journeys/general-events.md)
      + [Reactie](using/building-journeys/reaction-events.md)
      + [kwalificatie publiek](using/building-journeys/audience-qualification-events.md)
      + [Voorwaarde](using/building-journeys/condition-activity.md)
      + [Wachten](using/building-journeys/wait-activity.md)
      + [Doelgroep lezen](using/building-journeys/read-audience.md)
      + [Ingebouwde kanaalhandelingen](using/building-journeys/journeys-message.md)
      + [Aangepaste acties](using/building-journeys/using-custom-actions.md)
      + [Adobe Campaign Standard-acties](using/building-journeys/using-adobe-campaign-standard.md)
      + [Handelingen voor Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-v7-v8.md)
      + [Springen](using/building-journeys/jump.md)
      + [Profiel bijwerken](using/building-journeys/update-profiles.md)
   + Expressies maken {#building-advanced-conditions-journeys}
      + [Werken met de geavanceerde expressie-editor](using/building-journeys/expression/expressionadvanced.md)
      + Syntaxis {#syntax}
         + [Syntaxis van geavanceerde expressie-editor](using/building-journeys/expression/generalities.md)
         + [Voorwaardelijke instructie](using/building-journeys/expression/conditional-instruction.md)
         + [Datatypen](using/building-journeys/expression/data-types.md)
         + [Veldverwijzingen](using/building-journeys/expression/field-references.md)
         + [Functies voor het beheer van verzamelingen](using/building-journeys/expression/collection-management-functions.md)
         + [Operatoren](using/building-journeys/expression/operators.md)
         + [Journeyeigenschappen](using/building-journeys/expression/journey-properties.md)
         + [Voorbeelden](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Functies {#main-functions-journey}
         + [Hoofdfuncties](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inPubliek](using/building-journeys/functions/functioninaudience.md)
         + Samenvoeging {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + Conversie {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + Datum {#date}
            + [currentTimeInMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + Lijst {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [limiet](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Math {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + String {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [lengte](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Gebruiksscenario’s {#journey-use-cases}
      + Kwesties voor zakelijk gebruik {#business-use-cases}
         + [Multikanaalberichten verzenden](using/building-journeys/journeys-uc.md)
         + [Een bericht verzenden met Campagne v7/v8](using/building-journeys/ajo-ac.md)
         + [Een bericht verzenden naar abonnees](using/building-journeys/message-to-subscribers-uc.md)
      + Kwesties van technisch gebruik {#technical-use-cases}
         + [Verzamelingen dynamisch doorgeven met behulp van aangepaste handelingen](using/building-journeys/collections.md)
         + [Leveringen opwaarderen](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Productie beperken met externe gegevensbronnen en aangepaste acties](using/building-journeys/limit-throughput.md)
         + [Aangepaste acties gebruiken om gebeurtenissen voor reizen in Experience Platform te schrijven](using/building-journeys/custom-action-aep.md)
+ Geordende campagnes {#orchestrated-campaigns}
   + [Aan de slag met georkestreerde campagnes](using/ms/gs-ms-campaigns.md)
   + [Belangrijkste beginselen](using/ms/gs-campaign-creation.md)
   + [ Stappen om georkestreerde campagnes  te creëren](using/ms/gs-campaign-steps.md)
   + Configuratiestappen {#ms-config}
      + [Relationele schema&#39;s maken](using/ms/ms-schemas.md)
   + Aanmaakstappen{#create-ms-campaign}
      + [Een georkestreerde campagne maken](using/ms/create-ms-campaign.md)
      + [Campagne-instellingen configureren](using/ms/ms-campaign-settings.md)
      + [Uw campagnes plannen en starten](using/ms/start-monitor-campaigns.md)
      + [ bouwt vragen ](using/ms/ms-query-modeler.md)
   + Activiteiten {#design-campaigns}
      + [Aan de slag met activiteiten](using/ms/activities/about-activities.md)
      + [Orchestraten](using/ms/orchestrate-activities.md)
      + [En-join](using/ms/activities/and-join.md)
      + [publiek opbouwen](using/ms/activities/build-audience.md)
      + [Dimensie wijzigen](using/ms/activities/change-dimension.md)
      + [Combineren](using/ms/activities/combine.md)
      + [Deduplicatie](using/ms/activities/deduplication.md)
      + [Verrijking](using/ms/activities/enrichment.md)
      + [Vertakking](using/ms/activities/fork.md)
      + [Afstemming](using/ms/activities/reconciliation.md)
      + [Splitsen](using/ms/activities/split.md)
      + [Testen](using/ms/activities/test.md)
      + [Wachten](using/ms/activities/wait.md)
   + Berichten {#messages}
      + [Kanaalhandelingen](using/ms/activities/channels.md)
      + [ Personaliseer uw inhoud ](using/ms/ms-personalization.md)
      + [Uw berichten testen en valideren](using/ms/ms-proofs.md)
   + Rapportage en bewaking {#report}
      + [Rapportage](using/ms/reporting-campaigns.md)
+ Campagnes {#campaigns}
   + [Aan de slag met campagnes](using/campaigns/get-started-with-campaigns.md)
   + [Een campagne maken](using/campaigns/create-campaign.md)
   + [Een campagne bekijken en activeren](using/campaigns/review-activate-campaign.md)
   + [Campagnes beheren](using/campaigns/modify-stop-campaign.md)
   + [Campagnes activeren met API&#39;s](using/campaigns/api-triggered-campaigns.md)
+ Conflictbeheer en prioritering {#conflict-prioritization}
   + [Aan de slag met conflictbeheer en -prioriteiten](using/conflict-prioritization/gs-conflict-prioritization.md)
   + [Mogelijke conflicten identificeren](using/conflict-prioritization/conflicts.md)
   + [Prioriteitsscores toewijzen](using/conflict-prioritization/priority-scores.md)
   + [Afbakening van reizen en arbitrage](using/conflict-prioritization/journey-capping.md)
+ Testen en goedkeuren {#test}
   + Inhoud voorvertonen en testen {#preview-test}
      + [Aan de slag met voorvertoning en testen](using/content-management/preview-test.md)
      + [Testprofielen selecteren](using/content-management/test-profiles.md)
      + [Voorvertonen met testprofielen](using/content-management/preview.md)
      + [Proefdrukken verzenden met testprofielgegevens](using/content-management/proofs.md)
      + [E-mailrendering testen](using/content-management/rendering.md)
      + [Inhoudsvariaties simuleren](using/test-approve/simulate-sample-input.md)
      + [E-mailspamrapport](using/content-management/spam-report.md)
   + Reizen en campagnes goedkeuren {#approve}
      + [Aan de slag met goedkeuringen](using/test-approve/gs-approval.md)
      + [Goedkeuringsbeleid maken en beheren](using/test-approve/approval-policies.md)
      + [Goedkeuring aanvragen](using/test-approve/request-approval.md)
      + [Een verzoek goedkeuren](using/test-approve/review-approve-request.md)
+ Communicatiekanalen {#channels}
   + [Aan de slag met communicatiekanalen](using/channels/gs-channels.md)
   + Email channel {#email}
      + [Aan de slag met e-mails](using/email/get-started-email.md)
      + [Een e-mail maken](using/email/create-email.md)
      + Uw e-mailinhoud ontwerpen {#design-email}
         + [Aan de slag met e-mailontwerp](using/email/get-started-email-design.md)
         + Inhoud maken {#start-creating-content}
            + [Inhoud helemaal opnieuw ontwerpen](using/email/content-from-scratch.md)
            + [Uw inhoud importeren](using/email/existing-content.md)
            + [Uw eigen inhoud coderen](using/email/code-content.md)
            + [E-mailsjablonen gebruiken](using/email/use-email-templates.md)
            + [E-mailthema&#39;s gebruiken](using/email/apply-email-themes.md)
         + Uw inhoud ontwerpen {#add-content}
            + [Inhoudscomponenten gebruiken](using/email/content-components.md)
            + [Gebruik visuele fragmenten](using/email/use-visual-fragments.md)
            + [Koppelingen toevoegen en berichten bijhouden](using/email/message-tracking.md)
            + [Aangepaste aanbiedingen invoegen](using/email/add-offers-email.md)
            + [De tekstversie genereren](using/email/text-version-email.md)
            + [Metagegevens toevoegen](using/email/email-metadata.md)
         + Stijl bewerken {#edit-style}
            + [Aan de slag met e-mailstijl](using/email/get-started-email-style.md)
            + [Achtergrondinstellingen bewerken](using/email/backgrounds.md)
            + [Verticale uitlijning en opvulling aanpassen](using/email/alignment-and-padding.md)
            + [Inline-opmaakkenmerken toevoegen](using/email/inline-styling.md)
      + [ beheer e-mailopt-out ](using/email/email-opt-out.md)
      + E-mailkanaal configureren {#configure-email}
         + [Aan de slag met e-mailconfiguratie](using/email/get-started-email-config.md)
         + [Instellingen voor e-mailconfiguratie definiëren](using/email/email-settings.md)
         + [Abonnement op lijst opzeggen inschakelen](using/email/list-unsubscribe.md)
         + [Parameters koptekst](using/email/header-parameters.md)
         + [URL-tracking](using/email/url-tracking.md)
         + [E-mailconfiguratie aanpassen](using/email/surface-personalization.md)
   + Kanaal in app{#in-app}
      + [Aan de slag met In-app-kanaal](using/in-app/get-started-in-app.md)
      + [Voorwaarden voor kanalen in de app](using/in-app/inapp-configuration.md)
      + [Een mobiel bericht in de app maken](using/in-app/create-in-app.md)
      + [Een bericht voor een webtoepassing maken](using/in-app/create-in-app-web.md)
      + [In-app-inhoud ontwerpen](using/in-app/design-in-app.md)
      + [Meldingen voor In-app controleren en verzenden](using/in-app/send-in-app.md)
   + Push-meldingskanaal{#push}
      + [Aan de slag met pushmeldingen](using/push/get-started-push.md)
      + [Een pushmelding maken](using/push/create-push.md)
      + [Uw pushmelding ontwerpen](using/push/design-push.md)
      + [Uw pushmelding controleren en verzenden](using/push/send-push.md)
      + Pushmeldingen configureren{#push-config}
         + [Pushmeldingsstroom](using/push/push-gs.md)
         + [Pushmeldingskanaal configureren](using/push/push-configuration.md)
         + [Snelstartworkflow voor mobiele instaptoegang](using/push/mobile-onboarding-wf.md)
   + SMS/MMS-kanaal{#sms}
      + [Aan de slag met tekstberichten](using/sms/get-started-sms.md)
      + [Een tekstbericht maken (SMS/MMS)](using/sms/create-sms.md)
      + [Tekstberichten controleren en verzenden](using/sms/send-sms.md)
      + [ beheer de opt-out van het tekstbericht ](using/sms/sms-opt-out.md)
      + [SMS-subdomeinen instellen](using/sms/sms-subdomains.md)
      + SMS/MMS-kanaal configureren{#configure-sms}
         + [Ga aan de slag met de configuratie van SMS](using/sms/sms-configuration.md)
         + [Sinch-provider configureren](using/sms/sms-configuration-sinch.md)
         + [Infobip-provider configureren](using/sms/sms-configuration-infobip.md)
         + [Twilio-provider configureren](using/sms/sms-configuration-twilio.md)
         + [Een aangepaste provider configureren](using/sms/sms-configuration-custom.md)
         + [Een SMS-configuratie maken](using/sms/sms-configuration-surface.md)
   + Direct mail {#direct-mail}
      + [Aan de slag met direct mail](using/direct-mail/get-started-direct-mail.md)
      + [Een directe e-mail maken](using/direct-mail/create-direct-mail.md)
      + [Een direct mailbericht controleren en verzenden](using/direct-mail/test-send-direct-mail.md)
      + [Direct mail configureren](using/direct-mail/direct-mail-configuration.md)
   + Webkanaal {#web}
      + [Aan de slag met webkanaal](using/web/get-started-web.md)
      + Webkanaal configureren {#configure-web-channel}
         + [Voorwaarden voor webkanalen](using/web/web-prerequisites.md)
         + [Websubdomeinen configureren](using/web/web-delegated-subdomains.md)
         + [Webkanaalconfiguratie maken](using/web/web-configuration.md)
      + [Webervaringen maken](using/web/create-web.md)
      + Webpagina&#39;s van auteurs {#author-web-pages}
         + [Werken met de webontwerper](using/web/web-visual-editor.md)
         + [De niet-visuele editor gebruiken](using/web/web-non-visual-editor.md)
         + [Wijzigingen beheren](using/web/manage-web-modifications.md)
         + [Uw webervaringen bewaken](using/web/monitor-web-experiences.md)
         + [Toepassingen van één pagina maken](using/web/web-spa.md)
   + Ervaring op basis van code {#code-based-experience}
      + [Aan de slag met op code gebaseerd kanaal](using/code-based/get-started-code-based.md)
      + Op code gebaseerd kanaal configureren {#configure-code-based-channel}
         + [Afbeeldingen en voorwaarden](using/code-based/code-based-prerequisites.md)
         + [Op code gebaseerde ervaringsoppervlakken](using/code-based/code-based-surface.md)
         + [Voorbeelden van implementatiemethoden](using/code-based/code-based-implementation-samples.md)
         + [Beslissing in op code-gebaseerde ervaringsimplementaties](using/code-based/code-based-decisioning-implementations.md)
         + [Op code gebaseerde ervaringsconfiguratie maken](using/code-based/code-based-configuration.md)
      + Op code gebaseerde ervaringen maken {#create-code-based-experiences}
         + [Codegebaseerde ervaringen opbouwen en samenstellen](using/code-based/create-code-based.md)
         + [Ervaringen op basis van code testen](using/code-based/test-code-based.md)
         + [Op code gebaseerde ervaringen beheren](using/code-based/publish-code-based.md)
   + Inhoudskaarten{#content-card}
      + [Aan de slag met inhoudskaarten](using/content-card/get-started-content-card.md)
      + Inhoud kaartkanaal configureren {#configure}
         + [Voorwaarden voor inhoudskaarten](using/content-card/content-card-configuration-prereq.md)
         + [Het kanaal voor inhoudskaarten in Journey Optimizer configureren](using/content-card/content-card-configuration.md)
         + [Ondersteuning voor inhoudskaarten configureren in Mobile SDK](using/content-card/content-card-lp.md)
         + [Ondersteuning voor inhoudskaarten configureren in Web SDK](using/content-card/content-card-configuration-sdk.md)
      + [Inhoudskaarten maken](using/content-card/create-content-card.md)
      + [Inhoudskaarten ontwerpen](using/content-card/design-content-card.md)
   + WhatsApp{#whatsapp}
      + [Aan de slag met WhatsApp-berichten](using/whatsapp/get-started-whatsapp.md)
      + [WhatsApp-kanaal configureren in Journey Optimizer](using/whatsapp/whatsapp-configuration.md)
      + [Een whatsApp-bericht maken](using/whatsapp/create-whatsapp.md)
      + [Controleer en verzend uw WhatsApp-berichten](using/whatsapp/send-whatsapp.md)
   + REGEL {#line}
      + [Aan de slag met LINE-kanaal](using/line/get-started-line.md)
      + [Regelkanaal configureren in Journey Optimizer](using/line/line-configuration.md)
      + [Een LIJNbericht maken](using/line/create-line.md)
      + [Controleer en verzend uw berichten van de LIJN](using/line/send-line.md)
+ Inhoudsbeheer {#content-management}
   + Landingspagina&#39;s {#landing-pages}
      + [Aan de slag met bestemmingspagina&#39;s](using/landing-pages/get-started-lp.md)
      + [Een landingspagina maken](using/landing-pages/create-lp.md)
      + [Uw openingspagina&#39;s beheren](using/landing-pages/manage-lp.md)
      + Inhoud ontwerpen {#landing-pages-design}
         + [Informatie over het ontwerpen van bestemmingspagina](using/landing-pages/design-lp.md)
         + [De inhoud van de openingspagina maken](using/landing-pages/lp-content.md)
         + [Sjablonen maken](using/landing-pages/lp-templates.md)
         + [Aangepaste JavaScript toevoegen](using/landing-pages/lp-custom-js.md)
      + [Een lidmaatschapslijst maken](using/landing-pages/subscription-list.md)
      + [Gebruikskwesties leren](using/landing-pages/lp-use-cases.md)
      + Landingspagina’s configureren {#lp-configuration}
         + [Subdomeinen van bestemmingspagina configureren](using/landing-pages/lp-subdomains.md)
         + [Voorinstellingen voor openingspagina definiëren](using/landing-pages/lp-presets.md)
   + Personalisatie {#personalization}
      + [Aan de slag met personalisatie](using/personalization/personalize.md)
      + [ voeg verpersoonlijking  toe](using/personalization/personalization-build-expressions.md)
      + [Personalization-syntaxis](using/personalization/personalization-syntax.md)
      + [ hergebruik uitdrukkingsfragmenten ](using/personalization/use-expression-fragments.md)
      + [ gegevens van Adobe Experience Platform van het Gebruik voor verpersoonlijking (Beta) ](using/personalization/lookup-aep-data.md)
      + Lijst met hulpfuncties {#functions}
         + [Aan de slag met hulpfuncties](using/personalization/functions/functions.md)
         + [Samenvoegingsfuncties](using/personalization/functions/aggregation.md)
         + [Rekenkundige functies](using/personalization/functions/arithmetic-functions.md)
         + [Arrays en lijstfuncties](using/personalization/functions/arrays-list.md)
         + [Datumfuncties](using/personalization/functions/dates.md)
         + [Boolean- en vergelijkingsfuncties](using/personalization/functions/operators.md)
         + [Helpers](using/personalization/functions/helpers.md)
         + [Toewijzingsfuncties](using/personalization/functions/maps.md)
         + [Math-functies](using/personalization/functions/math.md)
         + [Objectfuncties](using/personalization/functions/objects.md)
         + [ functies van het Koord ](using/personalization/functions/string.md)
      + Personalization-gebruikskwesties{#personalization-use-cases}
         + [Statusmelding van bestelling](using/personalization/personalization-use-case.md)
         + [E-mailadres voor afmelden van winkelwagentje](using/personalization/personalization-use-case-helper-functions.md)
         + [E-mail met voorschriften voor het gezondheidsplan](using/personalization/perso-uc-plan-prescriptions.md)
   + Contentsjablonen {#content-templates}
      + [Aan de slag met inhoudssjablonen](using/content-management/content-templates.md)
      + [Sjablonen openen en beheren](using/content-management/access-content-templates.md)
      + [Inhoudssjablonen maken](using/content-management/create-content-templates.md)
      + [Inhoud in e-mailsjablonen vergrendelen](using/content-management/content-locking.md)
      + [Inhoudssjablonen testen](using/content-management/test-content-templates.md)
      + [Inhoudssjablonen gebruiken](using/content-management/use-content-templates.md)
   + Herbruikbare inhoudsfragmenten {#fragments}
      + [Aan de slag met fragmenten](using/content-management/fragments.md)
      + [Een fragment maken](using/content-management/create-fragments.md)
      + [Bestaande inhoud opslaan als fragment](using/content-management/save-fragments.md)
      + [Aanpasbare fragmenten](using/content-management/customizable-fragments.md)
      + [Fragmenten beheren](using/content-management/manage-fragments.md)
   + Dynamische inhoud {#dynamic}
      + [Aan de slag met dynamische inhoud](using/personalization/get-started-dynamic-content.md)
      + [Voorwaardelijke regels maken](using/personalization/create-conditions.md)
      + [Dynamische inhoud maken](using/personalization/dynamic-content.md)
   + Gebruiksscenario&#39;s tussen oplossingen {#combine}
      + [Combineer oplossingen om uw inhoud te beheren](using/integrations/content-integrations.md)
      + [Werken met Experience Manager Assets](using/integrations/assets.md)
      + [Werken met Adobe Stock](using/integrations/stock.md)
      + [Werken met Adobe Express](using/integrations/express.md)
      + [Werken met Experience Manager-sjablonen](using/integrations/aem-templates.md)
      + [Werken met Experience Manager-inhoudsfragmenten](using/integrations/aem-fragments.md)
      + [Werken met dynamische media](using/integrations/aem-dynamic.md)
      + [Werken met GenStudio for Performance Marketing](using/integrations/genstudio.md)
   + AI Assistant voor het genereren van inhoud{#ai-assistant}
      + [Aan de slag met AI Assistant](using/content-management/gs-generative.md)
      + [E-mailgeneratie met AI](using/content-management/generative-email.md)
      + [Push generation met AI](using/content-management/generative-push.md)
      + [SMS genereren met AI](using/content-management/generative-sms.md)
      + [Web genereren met AI](using/content-management/generative-web.md)
      + [Experimenteer met inhoud met AI](using/content-management/generative-experimentation.md)
      + [Openingspagina met AI](using/content-management/generative-lp.md)
      + [Gebruiksgevallen van AI Assistant](using/content-management/generative-uc.md)
      + Merken (bèta){#brands}
         + [Uw merken maken en beheren](using/content-management/brands.md)
         + [Uw Brand-uitlijningsscore evalueren](using/content-management/brands-score.md)
   + Meertalige inhoud{#content-multilingual}
      + [Aan de slag met meertalige inhoud](using/content-management/multilingual-gs.md)
      + [Een landinstelling maken](using/content-management/multilingual-locale.md)
      + [Een taalprovider maken](using/content-management/multilingual-provider.md)
      + [Meertalige inhoud maken met handmatige vertaling](using/content-management/multilingual-manual.md)
      + [Meertalige inhoud maken met automatische vertaling](using/content-management/multilingual-automated.md)
   + Inhoudsexperiment {#content-experiment}
      + [Aan de slag met het experimenteren met inhoud](using/content-management/get-started-experiment.md)
      + [Een inhoudexperiment maken](using/content-management/content-experiment.md)
      + Technische opmerkingen {#technotes}
         + [Statistische berekeningen begrijpen](using/content-management/experiment-calculations.md)
         + [Statistische berekeningen in het Experimentenrapport begrijpen](using/content-management/experiment-report-calculations.md)
+ Soorten publiek, profielen en identiteit{#audiences-profiles-identities}
   + Doelgroepen {#audiences}
      + [Aan de slag met het publiek](using/audience/about-audiences.md)
      + Soorten publiek maken {#create}
         + [Segmentdefinities](using/audience/creating-a-segment-definition.md)
         + [Samenstelling publiek](using/audience/get-started-audience-orchestration.md)
         + [Aangepaste upload](using/audience/custom-upload.md)
         + [Samenstelling van Federated-doelgroep](using/audience/federated-audience-composition.md)
      + [Activering van het publiek in campagnes en reizen](using/audience/target-audiences.md)
      + [Verrijkingskenmerken benutten](using/audience/enrichment-attributes.md)
   + Profielen{#profiles}
      + [Aan de slag met profielen](using/audience/get-started-profiles.md)
      + [Testprofielen maken](using/audience/creating-test-profiles.md)
      + [Werken met berekende kenmerken](using/audience/computed-attributes.md)
   + [Identiteiten](using/audience/get-started-identity.md)
   + [Licentiegebruik](using/audience/license-usage.md)
+ Track &amp; monitor {#reporting}
   + Live-rapport {#live-report}
      + [Aan de slag met Live-rapport](using/reports/live-report.md)
      + [Lijst met meetwaarden](using/reports/live-report-components.md)
      + [Journey Live-rapport](using/reports/journey-live-report.md)
      + [Campagne Live-rapport](using/reports/campaign-live-report.md)
      + [Openingspagina Live-rapport](using/reports/lp-report-live.md)
      + [Abonnementenlijst Live-rapport](using/reports/subscription-report-live.md)
   + Alle tijdrapporten{#channel-report}
      + [Aan de slag met alle tijdrapporten](using/reports/report-gs-cja.md)
      + [Lijst met meetwaarden](using/reports/global-report-components-cja.md)
      + [Customer Journey Analytics handmatig configureren](using/reports/cja-ajo.md)
      + [Uw rapporten beheren](using/reports/report-cja-manage.md)
      + [Voorwaarden voor rapportage en experimenten](using/reports/reporting-configuration.md)
      + Campagneverslagen{#reporting}
         + [Campagnerapport](using/reports/campaign-global-report-cja.md)
         + [Op code gebaseerd campagnerapport](using/reports/campaign-global-report-cja-code.md)
         + [Campagnerapport voor inhoudskaart](using/reports/campaign-global-report-cja-content.md)
         + [Campagnerapport voor e-mail](using/reports/campaign-global-report-cja-direct.md)
         + [E-mailcampagnerapport](using/reports/campaign-global-report-cja-email.md)
         + [campagnerapport voor experimenten](using/reports/campaign-global-report-cja-experimentation.md)
         + [Campagnerapport in app](using/reports/campaign-global-report-cja-inapp.md)
         + [Campagnerapport voor pushmeldingen](using/reports/campaign-global-report-cja-push.md)
         + [Rapport voor SMS-campagne](using/reports/campaign-global-report-cja-sms.md)
         + [Rapport webcampagne](using/reports/campaign-global-report-cja-web.md)
      + Reisrapporten{#reporting}
         + [Reisrapport](using/reports/journey-global-report-cja.md)
         + [Op code gebaseerd reisrapport](using/reports/journey-global-report-cja-code.md)
         + [Reisrapport voor inhoudskaart](using/reports/journey-global-report-cja-content.md)
         + [Directe-mailreisrapport](using/reports/journey-global-report-cja-direct.md)
         + [E-mailreisrapport](using/reports/journey-global-report-cja-email.md)
         + [Reisrapport in de app](using/reports/journey-global-report-cja-inapp.md)
         + [Push-reisrapport](using/reports/journey-global-report-cja-push.md)
         + [Vervoersrapport voor SMS](using/reports/journey-global-report-cja-sms.md)
         + [Webreisrapport](using/reports/journey-global-report-cja-web.md)
      + [Overzichtsrapport](using/reports/channel-report-cja.md)
      + [Rapport van bestemmingspagina](using/reports/lp-report-global-cja.md)
      + [Abonnementenlijstrapport](using/reports/subscription-report-global-cja.md)
   + Reisrapporten {#reports}
      + [Trainingsrapporten maken](using/reports/sharing-overview.md)
      + [Lijst met gebeurtenisvelden voor stappen](using/reports/sharing-field-list.md)
      + Gebeurtenisvelden voor oudere stappen {#legacy-step-event-fields}
         + [Oudere velden](using/reports/sharing-legacy-fields.md)
         + [Reisvelden](using/reports/sharing-journey-fields.md)
         + [Algemene velden](using/reports/sharing-common-fields.md)
         + [Uitvoeringsvelden voor handelingen](using/reports/sharing-execution-fields.md)
         + [Velden voor ophalen van gegevens](using/reports/sharing-fetch-fields.md)
         + [Identiteitsvelden](using/reports/sharing-identity-fields.md)
      + [Voorbeelden van query&#39;s](using/reports/query-examples.md)
   + Strategie en definitie {#deliverability}
      + [Aan de slag met de prestaties](using/reports/deliverability.md)
      + [De onderdrukkingslijst begrijpen](using/reports/suppression-list.md)
      + [Nieuwe DMARC-vereiste](using/configuration/dmarc-record-update.md)
   + [Waarschuwingen](using/reports/alerts.md)
   + [Uitsluitingsredenen](using/reports/exclusion-list.md)
+ Beslissingsmogelijkheden {#decisioning}
   + [Aan de slag met beslissingsmogelijkheden](using/experience-decisioning/gs-decision.md)
   + Beslissing {#experience-decisioning}
      + [Aan de slag met beslissing](using/experience-decisioning/gs-experience-decisioning.md)
      + [Afbakening en beperkingen](using/experience-decisioning/decisioning-guardrails.md)
      + API-referentie{#api-reference}
         + Aanbiedingsobjecten maken en beheren {#create-manage}
            + Beslissingsitems{#decision-items}
               + [Beslissingsitems maken](using/experience-decisioning/api-reference/decisions-items/create.md)
               + [Lijst met beslissingsitems](using/experience-decisioning/api-reference/decisions-items/decision-items-list.md)
               + [Beslissingsitems verwijderen](using/experience-decisioning/api-reference/decisions-items/delete.md)
               + [Opzoeken, beslissingsitems](using/experience-decisioning/api-reference/decisions-items/lookup.md)
               + [Beslissingsitems bijwerken](using/experience-decisioning/api-reference/decisions-items/update.md)
            + Items verzamelen{#items-collections}
               + [Items verzamelen](using/experience-decisioning/api-reference/items-collections/create.md)
               + [Itemverzamelingen verwijderen](using/experience-decisioning/api-reference/items-collections/delete.md)
               + [Lijst met verzamelingen items](using/experience-decisioning/api-reference/items-collections/items-collections-list.md)
               + [Opzoekitemverzamelingen](using/experience-decisioning/api-reference/items-collections/lookup.md)
               + [Items verzamelen bijwerken](using/experience-decisioning/api-reference/items-collections/update.md)
            + Selectiestrategieën{#selection-strategies}
               + [Selectiestrategieën maken](using/experience-decisioning/api-reference/selection-strategies/create.md)
               + [Selectiestrategieën verwijderen](using/experience-decisioning/api-reference/selection-strategies/delete.md)
               + [Selectiestrategieën opzoeken](using/experience-decisioning/api-reference/selection-strategies/lookup.md)
               + [Lijst met selectiestrategieën](using/experience-decisioning/api-reference/selection-strategies/selection-strategies-list.md)
               + [Selectiestrategieën bijwerken](using/experience-decisioning/api-reference/selection-strategies/update.md)
            + Beoordelingsformule{#ranking-formulas}
               + [Rangschikkingsformules maken](using/experience-decisioning/api-reference/ranking-formulas/create.md)
               + [Classificatieformules verwijderen](using/experience-decisioning/api-reference/ranking-formulas/delete.md)
               + [Opzoeken van rangschikkingsformules](using/experience-decisioning/api-reference/ranking-formulas/lookup.md)
               + [Selectierangstformules](using/experience-decisioning/api-reference/ranking-formulas/ranking-formulas-list.md)
               + [Rangschikkingsformules bijwerken](using/experience-decisioning/api-reference/ranking-formulas/update.md)
            + Subsidiabiliteitsregels{#eligibility-rules}
               + [Subsidiabiliteitsregels maken](using/experience-decisioning/api-reference/eligibility-rules/create.md)
               + [Subsidiabiliteitsregels verwijderen](using/experience-decisioning/api-reference/eligibility-rules/delete.md)
               + [Subsidiabiliteitsregels voor opzoeken](using/experience-decisioning/api-reference/eligibility-rules/lookup.md)
               + [Lijst van subsidiabiliteitsregels](using/experience-decisioning/api-reference/eligibility-rules/eligibility-rules-list.md)
               + [Subsidiabiliteitsregels bijwerken](using/experience-decisioning/api-reference/eligibility-rules/update.md)
         + [Aanbiedingen leveren met behulp van het op code-gebaseerde Ervingenkanaal](using/experience-decisioning/api-reference/deliver.md)
      + Beslissingsitems beheren {#decision-items}
         + [De itemcatalogus configureren](using/experience-decisioning/catalogs.md)
         + [Beslissingsitems maken](using/experience-decisioning/items.md)
         + [Itemverzamelingen beheren](using/experience-decisioning/collections.md)
      + Itemselectie configureren {#selection}
         + [Beslissingsregels maken](using/experience-decisioning/rules.md)
         + [Classificatiemethoden maken](using/experience-decisioning/ranking.md)
         + [De AI-formulebuilder gebruiken](using/experience-decisioning/exd-ranking-formulas.md)
         + [Gebruik van contextgegevens](using/experience-decisioning/context-data.md)
      + [Selectiestrategieën maken](using/experience-decisioning/selection-strategies.md)
      + [Beslissingsbeleid maken](using/experience-decisioning/create-decision.md)
      + [Verslag over het besluit](using/experience-decisioning/cja-reporting.md)
      + [Gebruiksscenario voor beslissing](using/experience-decisioning/experience-decisioning-uc.md)
   + Beslissingsbeheer {#offer-decisioning}
      + Aan de slag met het beheer van beslissingen {#get-started-decision}
         + [Over het beheer van besluiten](using/offers/get-started/starting-offer-decisioning.md)
         + [Belangrijke beheerinstructies en beperkingen](using/offers/decision-management-guardrails.md)
         + [Gebruikersinterface](using/offers/get-started/user-interface.md)
         + [Belangrijke stappen voor het maken en beheren van aanbiedingen](using/offers/offer-library/key-steps.md)
         + [Aangepast uploadpubliek gebruiken voor beslissingen](using/offers/custom-upload-decisioning.md)
         + [Kwestie gebruiken: aanbiedingen invoegen in een e-mail](using/offers/offers-e2e.md)
      + Componenten maken {#create-components}
         + [Plaatsingen maken](using/offers/offer-library/creating-placements.md)
         + [Beslissingsregels maken](using/offers/offer-library/creating-decision-rules.md)
         + [Verzamelingsaanduidingen maken](using/offers/offer-library/creating-tags.md)
      + Classificaties maken {#rankings}
         + [Aan de slag met waarderingen](using/offers/ranking/get-started-rankings.md)
         + [Beoordelingsformule](using/offers/ranking/create-ranking-formulas.md)
         + AI-modellen {#ai-models}
            + [AI-modellen](using/offers/ranking/ai-models.md)
            + AI-modeltypen {#ai-model-types}
            + [Model voor automatische optimalisatie](using/offers/ranking/auto-optimization-model.md)
            + [Gepersonaliseerd optimalisatiemodel](using/offers/ranking/personalized-optimization-model.md)
            + [AI-modellen maken](using/offers/ranking/create-ranking-strategies.md)
      + Aanbiedingen maken en beheren {#managing-offers-in-the-offer-library}
         + Aanbiedingen configureren {#configure-offers}
            + [Gepersonaliseerde aanbiedingen maken](using/offers/offer-library/creating-personalized-offers.md)
            + [Afbeeldingen toevoegen](using/offers/offer-library/add-representations.md)
            + [Beperkingen toevoegen](using/offers/offer-library/add-constraints.md)
         + [Alternatieve aanbiedingen maken](using/offers/offer-library/creating-fallback-offers.md)
         + [Verzamelingen maken](using/offers/offer-library/creating-collections.md)
      + Besluiten maken en beheren {#create-manage-activities}
         + [Beslissingen nemen](using/offers/offer-activities/create-offer-activities.md)
         + [Selectie van aanbiedingen in beslissingen configureren](using/offers/offer-activities/configure-offer-selection.md)
         + [Simulaties maken](using/offers/offer-activities/simulation.md)
      + [Batchbeslissingen gebruiken](using/offers/batch-delivery.md)
      + Gebeurtenisgegevens verzamelen {#collect-event-data}
         + [Aan de slag met gegevensverzameling](using/offers/data-collection/data-collection.md)
         + [Een gegevensset maken om gebeurtenissen te verzamelen](using/offers/data-collection/create-dataset.md)
         + [Vastleggen van gebeurtenissen configureren](using/offers/data-collection/schema-requirement.md)
      + Gebruik van contextgegevens {#context-data}
         + [Aan de slag met contextgegevens](using/offers/context-data.md)
         + [Contextgegevens en Edge-beslissingsverzoeken](using/offers/context-data-edge.md)
         + [Contextgegevens- en beslissingsverzoek](using/offers/context-data-decisioning.md)
      + Beslissingsbeheerrapporten maken {#create-reports}
         + [Werken met gebeurtenissen in verband met het beheer van beslissingen](using/offers/reports/get-started-events.md)
         + [Toegang tot gebeurtenissen van XDM-velden](using/offers/reports/xdm-fields.md)
      + Uw aanbiedingencatalogus exporteren {#export-catalog}
         + [Aan de slag met het exporteren van de aanbiedingscatalogus](using/offers/export-catalog/get-started-export.md)
         + [De geëxporteerde aanbiedingscatalogus openen](using/offers/export-catalog/access-dataset.md)
         + [Dataset met gepersonaliseerde aanbiedingen](using/offers/export-catalog/export-offers.md)
         + [Dataset met beslissingen](using/offers/export-catalog/export-decisions.md)
         + [Dataset met plaatsingen](using/offers/export-catalog/export-placements.md)
         + [Dataset met alternatieven](using/offers/export-catalog/export-fallback.md)
      + API-naslag {#api-reference}
         + [Aan de slag](using/offers/api-reference/getting-started.md)
         + Aanbiedingen maken en beheren met behulp van API&#39;s {#offers-api}
            + Plaatsen {#placements}
               + [Plaatsingen weergeven](using/offers/api-reference/offers-api/placements/placements-list.md)
               + [Een plaatsing opzoeken](using/offers/api-reference/offers-api/placements/lookup.md)
               + [Een plaatsing maken](using/offers/api-reference/offers-api/placements/create.md)
               + [Een plaatsing bijwerken](using/offers/api-reference/offers-api/placements/update.md)
               + [Een plaatsing verwijderen](using/offers/api-reference/offers-api/placements/delete.md)
            + Besluitvormingsregels {#decision-rules}
               + [Beslissingsregels weergeven](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
               + [Een beslissingsregel opzoeken](using/offers/api-reference/offers-api/decision-rules/lookup.md)
               + [Een beslissingsregel maken](using/offers/api-reference/offers-api/decision-rules/create.md)
               + [Een beslissingsregel bijwerken](using/offers/api-reference/offers-api/decision-rules/update.md)
               + [Een beslissingsregel verwijderen](using/offers/api-reference/offers-api/decision-rules/delete.md)
            + Verzamelingsaanduidingen {#tags}
               + [Kwaliteitsaanduidingen voor verzamelingen weergeven](using/offers/api-reference/offers-api/tags/tags-list.md)
               + [Een verzamelingskwalificatie opzoeken](using/offers/api-reference/offers-api/tags/lookup.md)
               + [Een verzamelingskwalificatie maken](using/offers/api-reference/offers-api/tags/create.md)
               + [Een verzamelingskwalificatie bijwerken](using/offers/api-reference/offers-api/tags/update.md)
               + [Een verzamelingskwalificatie verwijderen](using/offers/api-reference/offers-api/tags/delete.md)
            + Aangepaste aanbiedingen {#personalized-offers}
               + [Persoonlijke aanbiedingen weergeven](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
               + [Een persoonlijke aanbieding opzoeken](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
               + [Een persoonlijke aanbieding maken](using/offers/api-reference/offers-api/personalized-offers/create.md)
               + [Een persoonlijke aanbieding bijwerken](using/offers/api-reference/offers-api/personalized-offers/update.md)
               + [Een persoonlijke aanbieding verwijderen](using/offers/api-reference/offers-api/personalized-offers/delete.md)
            + Verzamelingen {#collections}
               + [Verzamelingen weergeven](using/offers/api-reference/offers-api/collections/collections-list.md)
               + [Een verzameling opzoeken](using/offers/api-reference/offers-api/collections/lookup.md)
               + [Een verzameling maken](using/offers/api-reference/offers-api/collections/create.md)
               + [Een verzameling bijwerken](using/offers/api-reference/offers-api/collections/update.md)
               + [Een verzameling verwijderen](using/offers/api-reference/offers-api/collections/delete.md)
            + Herkansingsaanbiedingen {#fallback-offers}
               + [Alternatieve aanbiedingen weergeven](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
               + [Een alternatieve aanbieding opzoeken](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
               + [Een alternatieve aanbieding maken](using/offers/api-reference/offers-api/fallback-offers/create.md)
               + [Een alternatieve aanbieding bijwerken](using/offers/api-reference/offers-api/fallback-offers/update.md)
               + [Een alternatieve aanbieding verwijderen](using/offers/api-reference/offers-api/fallback-offers/delete.md)
            + Besluiten {#decisions-api}
               + [Beslissingen weergeven](using/offers/api-reference/activities-api/activities/activities-list.md)
               + [Een beslissing opzoeken](using/offers/api-reference/activities-api/activities/lookup.md)
               + [Een beslissing nemen](using/offers/api-reference/activities-api/activities/create.md)
               + [Een beslissing bijwerken](using/offers/api-reference/activities-api/activities/update.md)
               + [Een beslissing verwijderen](using/offers/api-reference/activities-api/activities/delete.md)
            + Verouderde API&#39;s {#legacy-api}
               + [Oudere API&#39;s](using/offers/api-reference/offers-api/legacy-apis/about-legacy-apis.md)
               + Plaatsen {#placements}
                  + [Plaatsingen weergeven](using/offers/api-reference/offers-api/legacy-apis/placements/placements-list.md)
                  + [Een plaatsing opzoeken](using/offers/api-reference/offers-api/legacy-apis/placements/lookup.md)
                  + [Een plaatsing maken](using/offers/api-reference/offers-api/legacy-apis/placements/create.md)
                  + [Een plaatsing bijwerken](using/offers/api-reference/offers-api/legacy-apis/placements/update.md)
                  + [Een plaatsing verwijderen](using/offers/api-reference/offers-api/legacy-apis/placements/delete.md)
               + Besluitvormingsregels {#decision-rules}
                  + [Beslissingsregels weergeven](using/offers/api-reference/offers-api/legacy-apis/decision-rules/rules-list.md)
                  + [Een beslissingsregel opzoeken](using/offers/api-reference/offers-api/legacy-apis/decision-rules/lookup.md)
                  + [Een beslissingsregel maken](using/offers/api-reference/offers-api/legacy-apis/decision-rules/create.md)
                  + [Een beslissingsregel bijwerken](using/offers/api-reference/offers-api/legacy-apis/decision-rules/update.md)
                  + [Een beslissingsregel verwijderen](using/offers/api-reference/offers-api/legacy-apis/decision-rules/delete.md)
               + Verzamelingsaanduidingen {#tags}
                  + [Kwaliteitsaanduidingen voor verzamelingen weergeven](using/offers/api-reference/offers-api/legacy-apis/tags/tags-list.md)
                  + [Een verzamelingskwalificatie opzoeken](using/offers/api-reference/offers-api/legacy-apis/tags/lookup.md)
                  + [Een verzamelingskwalificatie maken](using/offers/api-reference/offers-api/legacy-apis/tags/create.md)
                  + [Een verzamelingskwalificatie bijwerken](using/offers/api-reference/offers-api/legacy-apis/tags/update.md)
                  + [Een verzamelingskwalificatie verwijderen](using/offers/api-reference/offers-api/legacy-apis/tags/delete.md)
               + Aangepaste aanbiedingen {#personalized-offers}
                  + [Persoonlijke aanbiedingen weergeven](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/offers-list.md)
                  + [Een persoonlijke aanbieding opzoeken](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/lookup.md)
                  + [Een persoonlijke aanbieding maken](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/create.md)
                  + [Een persoonlijke aanbieding bijwerken](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/update.md)
                  + [Een persoonlijke aanbieding verwijderen](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/delete.md)
               + Herkansingsaanbiedingen {#fallback-offers}
                  + [Alternatieve aanbiedingen weergeven](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/fallback-list.md)
                  + [Een alternatieve aanbieding opzoeken](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/lookup.md)
                  + [Een alternatieve aanbieding maken](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/create.md)
                  + [Een alternatieve aanbieding bijwerken](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/update.md)
                  + [Een alternatieve aanbieding verwijderen](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/delete.md)
               + Verzamelingen {#collections}
                  + [Verzamelingen weergeven](using/offers/api-reference/offers-api/legacy-apis/collections/collections-list.md)
                  + [Een verzameling opzoeken](using/offers/api-reference/offers-api/legacy-apis/collections/lookup.md)
                  + [Een verzameling maken](using/offers/api-reference/offers-api/legacy-apis/collections/create.md)
                  + [Een verzameling bijwerken](using/offers/api-reference/offers-api/legacy-apis/collections/update.md)
                  + [Een verzameling verwijderen](using/offers/api-reference/offers-api/legacy-apis/collections/delete.md)
               + Besluiten {#decisions-api}
                  + [Beslissingen weergeven](using/offers/api-reference/offers-api/legacy-apis/activities-api/activities-list.md)
                  + [Een beslissing opzoeken](using/offers/api-reference/offers-api/legacy-apis/activities-api/lookup.md)
                  + [Een beslissing nemen](using/offers/api-reference/offers-api/legacy-apis/activities-api/create.md)
                  + [Een beslissing bijwerken](using/offers/api-reference/offers-api/legacy-apis/activities-api/update.md)
                  + [Een beslissing verwijderen](using/offers/api-reference/offers-api/legacy-apis/activities-api/delete.md)
         + Aanbiedingen leveren met behulp van API&#39;s {#offer-delivery-api}
            + [Aan de slag met API&#39;s voor levering van aanbiedingen](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
            + [API voor besluitvorming](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
            + [Edge-API voor besluitvorming](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
            + [Batchbeslissing-API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Gegevensbeheer {#data-management}
   + [Aan de slag met gegevensbeheer](using/data/gs-data.md)
   + [Werken met schema&#39;s](using/data/get-started-schemas.md)
   + Journey Optimizer-gegevenssets {#datasets}
      + [Aan de slag met gegevenssets](using/data/get-started-datasets.md)
      + [Datasets Time-to-live (TTL)-instructies](using/data/datasets-ttl.md)
      + [Journey Optimizer-gegevenssets exporteren](using/data/export-datasets.md)
      + [Voorbeelden van query](using/data/datasets-query-examples.md)
      + [ Ingebouwde schema&#39;s > ](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
   + [Zoekopdrachten](using/data/get-started-queries.md)
+ Kanaalconfiguratie {#configuration}
   + [Uw kanalen configureren](using/configuration/get-started-configuration.md)
   + [Kanaalconfiguraties instellen](using/configuration/channel-surfaces.md)
   + Kanaalinstellingen met instructies {#guided-setup}
      + [Aan de slag met de instelling van het kanaal met instructies](using/configuration/set-mobile-config.md)
      + [Een kanaalinstelling maken](using/configuration/create-channel-set-up.md)
   + E-mailsubdomeinen delegeren {#delegate-subdomains}
      + [Aan de slag met subdomeindelegatie](using/configuration/about-subdomain-delegation.md)
      + [Een subdomein delegeren](using/configuration/delegate-subdomain.md)
      + [DMARC-record instellen](using/configuration/dmarc-record.md)
      + [Een Google TXT-record toevoegen](using/configuration/google-txt.md)
      + [PTR-records openen en bewerken](using/configuration/ptr-records.md)
      + [IP-pools maken](using/configuration/ip-pools.md)
   + Voer een IP warmlopingsplan uit {#implement-ip-warmup-plan}
      + [Ga aan de slag met IP-opwarmingsplannen](using/configuration/ip-warmup-gs.md)
      + [IP-warmtecampagnes maken](using/configuration/ip-warmup-campaign.md)
      + [Creeer een IP warmlopingsplan](using/configuration/ip-warmup-plan.md)
      + [Voer het IP-opwarmingsplan uit](using/configuration/ip-warmup-execution.md)
      + [IP-bestanden voor opwarmingsplannen](using/configuration/ip-warmup-plan-files.md)
   + E-mailadressen controleren {#monitor-reputation}
      + [Onderdrukkingslijst](using/configuration/manage-suppression-list.md)
      + [Opnieuw](using/configuration/retries.md)
      + [Lijst van gewenste personen](using/configuration/allow-list.md)
   + [zaadlijsten gebruiken](using/configuration/seed-lists.md)
   + [Ondersteuning voor archivering](using/configuration/archiving-support.md)
   + [Uitvoeringadressen wijzigen](using/configuration/primary-email-addresses.md)
   + [Bedrijfsregels configureren](using/configuration/frequency-rules.md)
   + [Werken met regelsets](using/configuration/rule-sets.md)
+ Reisconfiguratie {#configure-journeys}
   + [Gegevensbronnen, gebeurtenissen en handelingen configureren](using/configuration/about-data-sources-events-actions.md)
   + Gebeurtenisconfiguratie {#events-journeys}
      + [Werken met reisgebeurtenissen](using/event/about-events.md)
      + [Een eenheidsgebeurtenis configureren](using/event/about-creating.md)
      + [ExperienceEvent-schema’s](using/event/experience-event-schema.md)
      + [Werken met Adobe Analytics-gegevens](using/event/about-analytics.md)
      + [Een bedrijfsgebeurtenis configureren](using/event/about-creating-business.md)
      + [Aanvullende stappen om gebeurtenissen te verzenden](using/event/additional-steps-to-send-events-to-journey.md)
   + Gegevensbronconfiguratie{#data-source-journeys}
      + [Aan de slag met gegevensbronnen](using/datasource/about-data-sources.md)
      + [Een gegevensbron configureren](using/datasource/configure-data-sources.md)
      + [Adobe Experience Platform-databron](using/datasource/adobe-experience-platform-data-source.md)
      + [Externe databronnen](using/datasource/external-data-sources.md)
   + Actieconfiguratie {#action-journeys}
      + [Aan de slag met aangepaste handelingen](using/action/action.md)
      + [Een aangepaste handeling configureren](using/action/about-custom-action-configuration.md)
      + [Een aangepaste handeling oplossen](using/action/troubleshoot-custom-action.md)
      + [API-aanroepreacties gebruiken in aangepaste handelingen](using/action/action-response.md)
+ Sluit uw systemen en omgevingen aan {#connect-systems}
   + [Integreren met andere oplossingen](using/integrations/ajo-integrations.md)
   + [Werken met Journey Optimizer API&#39;s](using/configuration/ajo-apis.md)
   + Uw reizen integreren met externe systemen {#external-systems}
      + [Reisintegratie met externe systemen](using/configuration/external-systems.md)
      + [Afkappings-API](using/configuration/capping.md)
      + [API voor beperken](using/configuration/throttling.md)
   + Verzenden met Adobe-oplossingen {#adobe-solutions}
      + [Campaign Standard-actie tijdens reizen](using/action/acs-action.md)
      + [Campagne v7/v8 - actie tijdens reizen](using/action/acc-action.md)
      + [Marketo Engage-actie tijdens reizen](using/action/marketo-engage.md)
   + Sandboxbeheer {#sandbox}
      + [Sandboxen gebruiken en toewijzen](using/administration/sandboxes.md)
      + [Objecten exporteren naar een andere sandbox](using/configuration/copy-objects-to-sandbox.md)
   + [Vorm de Bronschakelaar](using/start/get-started-sources.md)
+ Toegangsbeheer {#access-control}
   + Overzicht van toegangsbeheer {#privacy}
      + [Aan de slag met gebruikersbeheer](using/administration/permissions-overview.md)
      + [Ingebouwde rollen](using/administration/ootb-product-profiles.md)
      + [Ingebouwde machtigingen](using/administration/ootb-permissions.md)
      + [Machtigingsniveaus](using/administration/high-low-permissions.md)
   + [Gebruikers en rollen beheren](using/administration/permissions.md)
   + [Toegangsbeheer op basis van kenmerken](using/administration/attribute-based-access.md)
   + [Toegangsbeheer op objectniveau](using/administration/object-based-access.md)
+ Privacy {#privacy}
   + [Aan de slag met privacy](using/privacy/get-started-privacy.md)
   + [Privacyverzoeken](using/privacy/requests.md)
   + [Controleregelingen op middelen](using/privacy/audit-logs.md)
   + [Levenscyclusbewerkingen voor gegevens uitvoeren](using/privacy/data-hygiene.md)
   + Toestemming beheren {#consent}
      + [Weigeren beheren](using/privacy/opt-out.md)
      + [Werken met toestemmingsbeleid](using/action/consent.md)
   + [Datagovernance](using/action/action-privacy.md)
   + [Door de klant beheerde sleutels instellen en beheren](using/privacy/cmk.md)
