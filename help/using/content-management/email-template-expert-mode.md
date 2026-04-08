---
solution: Journey Optimizer
product: journey optimizer
title: E-mailsjablonen bewerken met de geavanceerde HTML-editor
description: Gebruik de modus Expert om de HTML-bron van e-mailinhoud in de WYSIWYG-editor weer te geven en te bewerken, met de functie-markering, hulplijnen en validatie opslaan.
feature: Templates
topic: Content Management
role: User
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---

# E-mailsjablonen bewerken met de geavanceerde HTML-editor {#email-template-expert-mode}

>[!AVAILABILITY]
>
>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

De **geavanceerde redacteur van HTML** is een deskundige wijze die u de ruwe broncode van e-mailinhoudsmalplaatjes van de [!DNL Journey Optimizer] e-mailinterface van Designer direct laat bekijken en uitgeven.

Met deze functie kunt u geavanceerde expressies, zoals condities, rechtstreeks in de bron invoegen. Wanneer u terugschakelt naar de visuele weergave (Computer), wordt de inhoud opnieuw gerenderd, zodat u kunt controleren hoe de inhoud eruitziet en in beide weergaven verder kunt bewerken.

>[!NOTE]
>
>Deze functie is alleen beschikbaar in inhoudssjablonen en voor het e-mailkanaal.

## Beveiligingsmechanismen {#guardrails}

Wanneer u de geavanceerde HTML-editor gebruikt, beschermen de volgende instructies de compatibiliteit van inhoud en stellen ze verwachtingen in.

* De geavanceerde redacteur van HTML **bevestigt** uw code niet. Er worden geen syntaxisfouten of verbroken indelingen gecontroleerd. Bekijk de inhoud zorgvuldig voordat u deze opslaat.

* De toekomstige systeemupdates kunnen veranderingen beschrijven u aan standaardprijsverhoging aanbrengt. **Uw veranderingen kunnen niet** blijven.

* Het [!DNL Adobe] ondersteuningsteam **kan niet** kwesties problemen oplossen of oplossen die door douanecode en handveranderingen worden veroorzaakt. Bewaar een back-up van uw inhoud voor het geval u deze moet herstellen.

* U kunt geen inhoud simuleren in de geavanceerde HTML-weergave. Schakel over naar de weergave Computer om een voorvertoning van uw inhoud weer te geven.

* Om inhoudsverenigbaarheid te verzekeren, **kunt u niet** in de geavanceerde mening van HTML bewaren. Schakel terug naar de bureaubladweergave als u klaar bent om uw wijzigingen op te slaan.

>[!WARNING]
>
>De geavanceerde HTML-editor in de inhoudssjabloon is niet dezelfde als de modus **[!UICONTROL Code your own]** in de e-mailtoepassing van Designer. In de modus [!UICONTROL Code your own] kunt u niet terugschakelen naar de visuele editor. Als u eenmaal dat pad hebt gekozen, kunt u alleen codebewerkingen uitvoeren. Met de geavanceerde HTML-editor kunt u daarentegen op elk gewenst moment schakelen tussen de HTML-weergave en de (visuele) desktopweergave. [ leer meer over de coderedacteur ](../email/code-content.md)

## Overschakelen naar de geavanceerde HTML-weergave {#switch-to-html-view}

Voer de volgende stappen uit om de geavanceerde HTML-editor te openen en de sjabloonbron te bewerken.

1. Open of creeer een [ e-mailmalplaatje ](../content-management/create-content-templates.md) en open [ E-mail Designer ](../email/get-started-email-design.md) om de inhoud uit te geven.

1. Klik op de knop **[!UICONTROL HTML]** in de rechterbovenhoek van het scherm.

   ![ Plaats van de knoop van HTML in de toolbar van Designer E-mail ](assets/email-template-expert-mode-button.png)

1. De eerste keer dat u de geavanceerde HTML-editor opent, wordt een waarschuwingsbericht weergegeven. Bekijk deze zorgvuldig en klik op **[!UICONTROL OK]** om door te gaan. [Meer informatie](#guardrails)

   ![ de dialoog van de Waarschuwing wanneer het openen van de geavanceerde redacteur van HTML voor het eerst ](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >Deze waarschuwing wordt alleen weergegeven wanneer u de geavanceerde HTML-editor voor de eerste keer opent en elke maand opnieuw instelt.

1. De geavanceerde HTML-editor wordt weergegeven.

   ![ Geavanceerde de redacteursinterface van HTML die de broncode van het e-mailmalplaatje toont ](assets/email-template-expert-mode.png)

1. Voeg de gewenste wijzigingen toe aan uw e-mailinhoud.

   >[!WARNING]
   >
   >Zorg ervoor dat u de juiste HTML- en CSS-code invoert omdat er geen syntaxisvalidatieproces is en er geen ondersteuning wordt geboden door [!DNL Adobe] . [Meer informatie](#guardrails)

1. Vanwege compatibiliteitsredenen zijn het simuleren en opslaan van inhoud niet beschikbaar in de geavanceerde HTML-weergave. Schakel terug naar de weergave Computer om een voorvertoning van uw inhoud weer te geven en uw wijzigingen op te slaan.

   ![ Schakelaar terug naar de mening van de Desktop om uw veranderingen te bewaren ](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Uw bewerkingen blijven behouden wanneer u van weergave verandert.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}
-->

## Verwante onderwerpen

* [Uw eigen e-mailinhoud coderen](../email/code-content.md)
* [Inhoudssjablonen maken](create-content-templates.md)
* [Aan de slag met Email Designer](../email/get-started-email-design.md)

