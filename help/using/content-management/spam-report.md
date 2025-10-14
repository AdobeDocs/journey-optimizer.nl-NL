---
title: E-mailspamrapport gebruiken
description: Leer hoe u het e-mailspamrapport kunt gebruiken.
feature: Preview
role: User
level: Beginner
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# E-mailspamrapport {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="E-mailspamrapport"
>abstract="Met het Spam-rapport kunt u uw spamscoring in e-mailinhoud controleren. Deze score wijst erop als ISPs of de leveranciers van de Brievenbus uw bericht als spam of niet zullen beschouwen. Hoe lager de score, hoe beter. Als de score voor uw e-mailinhoud hoger is dan 2, kunt u problemen verhelpen die ertoe leiden dat tests mislukken."

U kunt de spamscoring in uw e-mailinhoud controleren in een speciaal Spam-rapport. Gebruikend [&#x200B; SpamAssassin &#x200B;](https://spamassassin.apache.org/){target="_blank"} , kan Adobe Journey Optimizer uw e-mailinhoud testen en het een score geven om erop te wijzen als ISPs of de leveranciers van de Brievenbus het als spam of niet zullen beschouwen.

Als u uw e-mailinhoud bewerkt of hiervan een voorvertoning weergeeft, geeft de knop **[!UICONTROL Spam report]** een score en advies om de scores voor elk afzonderlijk aangeboden item te verbeteren.

Dit vermogen staat u toe om te bepalen of een bericht als spam door de anti-anti-spamhulpmiddelen kon worden beschouwd die bij ontvangstbewijs worden gebruikt, en om acties te nemen als dit het geval is. Veel e-mailproviders gebruiken gereedschappen als onderdeel van hun spamfilterproces. Het verzenden van e-mails met een slechte score kan van grote invloed zijn op je leesbaarheid.

Voer de onderstaande stappen uit om **[!UICONTROL Spam report]** te openen.

1. Klik in het **[!UICONTROL Simulate]** -scherm op de knop **[!UICONTROL Spam report]** .

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Er wordt automatisch een anti-spamcontrole uitgevoerd en het venster **[!UICONTROL Spam report]** geeft de resultaten weer. U ziet hier hoe de inhoud werkt op het gebied van de layout, structuur, afbeeldingsgrootte, eventuele spamtriggerwoorden, enzovoort.

   ![](assets/spam-report-high-score.png)

1. Controleer de scores en beschrijvingen voor elk item.

   Hoe lager de score, hoe beter. Als de score hoger is dan 5, wordt een waarschuwing getoond: het wijst erop dat sommige berichten kunnen worden geblokkeerd of als spam wanneer ontvangen worden gemerkt. De beste manier is om een score lager dan 2 te hebben.

   >[!NOTE]
   >
   >De score van spam wordt afgeleid via [&#x200B; SpamAssassin &#x200B;](https://spamassassin.apache.org/){target="_blank"} , en de regels zijn niet bezeten door Adobe. Voor meer details over deze regels, verwijs naar de documentatie SpamAssassin.
   >

1. Gebaseerd op dat het scoren, als u van mening bent dat sommige elementen kunnen worden verbeterd, geef uw inhoud in [&#x200B; E-mail Designer &#x200B;](../email/content-from-scratch.md) uit en maak de noodzakelijke updates.

1. Wanneer de wijzigingen zijn aangebracht, bladert u terug naar het **[!UICONTROL Spam report]** -scherm om te controleren of de score is verbeterd.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more about email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
