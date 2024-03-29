---
title: Een direct mailbericht controleren en verzenden
description: Leer hoe u een direct-mailbericht kunt controleren en verzenden in Journey Optimizer
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 1%

---

# Een direct mailbericht controleren en verzenden {#direct-mail-test-send}

## Een voorbeeld van het extractiebestand bekijken {#preview-dm}

Nadat de inhoud van het extractiebestand is gedefinieerd, kunt u er testprofielen voor gebruiken. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Om dit te doen, klik **[!UICONTROL Simulate content]** Voeg vervolgens een testprofiel toe om te controleren hoe het extractiebestand wordt gerenderd met behulp van de testprofielgegevens.

![](assets/direct-mail-simulate.png){width="800" align="center"}

Gedetailleerde informatie over het selecteren van testprofielen en het weergeven van een voorvertoning van de inhoud is beschikbaar in het dialoogvenster [Inhoud beheren](../content-management/preview-test.md) sectie.

Als de bestandsinhoud klaar is om te worden verzonden, sluit u het simulatiescherm en klikt u op de knop **[!UICONTROL Review to activate]** knop.

## De campagne Direct mail valideren en activeren {#dm-validate}

Voordat u de campagne voor directe mail activeert, moet u controleren of de campagne en het extractiebestand op de juiste wijze zijn geconfigureerd. Om dit te doen, controleer alarm in de hogere sectie van de redacteur. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw SMS-bericht leeg is.

* **Fouten** voorkomen dat u de campagne publiceert, zolang deze niet is opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.

![](assets/direct-mail-review.png){width="800" align="center"}

Klik op de knop **[!UICONTROL Activate]** knop. Wanneer de campagne start, wordt het extractiebestand automatisch gegenereerd en geëxporteerd naar de server die in uw [bestand dat configuratie verplettert](../direct-mail/direct-mail-configuration.md).

Nadat u de campagne hebt verzonden, kunt u de impact van de campagne voor directe e-mail meten in de campagnerapporten. Raadpleeg deze sectie voor meer informatie over rapporten.

## Toestemming voor direct mail beheren {#dm-consent-management}

In [!DNL Journey Optimizer], wordt de toestemming door het Experience Platform afgehandeld [Goedkeuringsschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. Standaard is de waarde voor het veld voor toestemming leeg en wordt deze behandeld als toestemming voor het ontvangen van uw communicatie.

Als een profiel ervoor heeft gekozen geen directe e-mail te ontvangen, moet u in de desbetreffende profielkenmerken van het Experience Platform de waarde voor `consents.marketing.postalMail.val` wordt `n` en het corresponderende profiel zal van latere leveringen worden uitgesloten.

Als u dit opnieuw wilt inschakelen, moet u het profielkenmerk wijzigen in `consents.marketing.postalMail.val` : `y`.

Als u de kenmerken van een profiel wilt beheren, gaat u naar het Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

Meer informatie over het beheren van opt-out in Journey Optimizer in [deze sectie](../privacy/opt-out.md).
