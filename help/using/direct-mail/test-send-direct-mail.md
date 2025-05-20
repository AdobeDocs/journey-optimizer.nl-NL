---
title: Een direct mailbericht controleren en verzenden
description: Leer hoe u een direct-mailbericht kunt controleren en verzenden in Journey Optimizer
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: c314d2e7a48f8eab1f32950e0e4e9056d11fd58b
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Een direct mailbericht controleren en verzenden {#direct-mail-test-send}

## Een voorbeeld van het extractiebestand bekijken {#preview-dm}

Nadat de inhoud van het extractiebestand is gedefinieerd, kunt u er testprofielen voor gebruiken. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Klik hiertoe op **[!UICONTROL Simulate content]** en voeg vervolgens een testprofiel toe om te controleren hoe het extractiebestand met de testprofielgegevens wordt gerenderd.

![](assets/direct-mail-simulate.png){width="800" align="center"}

De gedetailleerde informatie over hoe te om testprofielen en voorproef uw inhoud te selecteren is beschikbaar in de [ sectie van het Beheer van de Inhoud ](../content-management/preview-test.md).

Als de bestandsinhoud klaar is om te worden verzonden, sluit u het simulatiescherm en klikt u op de knop **[!UICONTROL Review to activate]** .

## De campagne Direct mail valideren en activeren {#dm-validate}

>[!IMPORTANT]
>
> Als uw campagne onderworpen is aan een goedkeuringsbeleid, zult u goedkeuring moeten vragen om uw Direct-mailcampagne te kunnen verzenden. [Meer informatie](../test-approve/gs-approval.md)

Voordat u de campagne voor directe mail activeert, moet u controleren of de campagne en het extractiebestand op de juiste wijze zijn geconfigureerd. Om dit te doen, controleer alarm in de hogere sectie van de redacteur. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

* **de Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw SMS-bericht leeg is.

* **de Fouten** verhinderen u de campagne te publiceren, zolang zij niet worden opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.

![](assets/direct-mail-review.png){width="800" align="center"}

Klik op de knop **[!UICONTROL Activate]** als uw campagne voor direct mail gereed is. Wanneer de campagne begint, wordt het extractiedossier automatisch geproduceerd en uitgevoerd naar de server die in uw [ wordt gespecificeerd dossier dat configuratie ](../direct-mail/direct-mail-configuration.md) verplettert.

>[!NOTE]
>
>Het geëxporteerde bestand eindigt standaard met een nieuwe regel. Dit zorgt voor compatibiliteit met standaard gegevensverwerkingstools.


Nadat u de campagne hebt verzonden, kunt u de impact van de campagne voor directe e-mail meten in de campagnerapporten. Voor meer over directe post die, verwijs naar [ deze sectie ](../reports/campaign-global-report-cja-direct.md) rapporteert.

## Toestemming voor direct mail beheren {#dm-consent-management}

In [!DNL Journey Optimizer], wordt de toestemming behandeld door het schema van de Experience Platform [ Toestemming ](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. Standaard is de waarde voor het veld voor toestemming leeg en wordt deze behandeld als toestemming voor het ontvangen van uw communicatie.

Als een profiel ervoor heeft gekozen geen directe e-mail te ontvangen, wordt in de corresponderende Experience Platform-profielkenmerken de waarde voor `consents.marketing.postalMail.val` `n` gebruikt en wordt het corresponderende profiel uitgesloten van volgende leveringen.

Als u het profiel opnieuw wilt inschakelen, moet u het profielkenmerk weer instellen op `consents.marketing.postalMail.val` : `y` .

Als u de kenmerken van een profiel wilt beheren, gaat u naar Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Leer meer in de [ documentatie van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

Leer meer over het beheren van opt-out in Journey Optimizer in [ deze sectie ](../privacy/opt-out.md).
