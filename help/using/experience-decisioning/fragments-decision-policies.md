---
title: Hefboomfragmenten in besluitvormingsbeleid
description: Leer hoe u fragmenten kunt gebruiken in beleidsregels voor beslissingen
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: 083545ff7b2dc5ce45ef3766321fdf12e1b96c5c
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---


# Hefboomfragmenten in besluitvormingsbeleid {#fragments}

Als uw besluitvormingsbeleid besluitpunten met inbegrip van fragmenten bevat, kunt u deze fragmenten in de code van het besluitvormingsbeleid hefboomwerking. [ Leer meer op fragmenten ](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Dit vermogen is momenteel slechts beschikbaar voor het **op code-Gebaseerde ervarings** kanaal en voor een reeks organisaties (Beperkte Beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

Stel bijvoorbeeld dat u verschillende inhoud wilt weergeven voor verschillende modellen van mobiele apparaten. Zorg ervoor u fragmenten die aan die apparaten beantwoorden aan het besluitvormingspunt toevoegde dat u in het besluitvormingsbeleid gebruikt. [ leer hoe ](items.md#attributes).

![](assets/item-fragments.png){width=70%}

Nadat u dit hebt gedaan, kunt u een van de volgende methoden gebruiken:

>[!BEGINTABS]

>[!TAB  neemt direct de code ] op

U plakt gewoon het codeblok hieronder in de code voor het beslissingsbeleid. Vervang `variable` door de fragment-id en `placement` door de fragmentverwijzingssleutel:

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB  volg de gedetailleerde stappen ]

1. Navigeer aan **[!UICONTROL Helper functions]** en voeg **** functie `{% let variable = expression %} {{variable}}` aan de coderuit toe, waar u de variabele voor uw fragment kunt verklaren.

   ![](assets/decision-let-function.png)

1. Gebruik de **Kaart** > **krijgt** functie `{%= get(map, string) %}` om uw uitdrukking te bouwen. De kaart is het fragment waarnaar wordt verwezen in het beslissingsitem en de tekenreeks kan het apparaatmodel zijn dat u als **[!UICONTROL Fragment reference key]** hebt ingevoerd in het beslissingsitem.

   ![](assets/decision-map-function.png)

1. U kunt ook een contextueel kenmerk gebruiken dat deze id van het apparaatmodel zou bevatten.

   ![](assets/decision-contextual-attribute.png)

1. Voeg de variabele toe die u als fragment-id voor het fragment hebt gekozen.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

De fragment-id en de verwijzingssleutel worden geselecteerd in de sectie **[!UICONTROL Fragments]** van het beslissingsitem.

>[!WARNING]
>
>Als de fragmentsleutel onjuist is of als de fragmentinhoud niet geldig is, zal de rendering mislukken en een fout veroorzaken in de Edge-aanroep.

## Afbeeldingen bij gebruik van fragmenten {#fragments-guardrails}

**punt van het Besluit en contextattributen**

Kenmerken van beslissingsitems en contextafhankelijke kenmerken worden standaard niet ondersteund in [!DNL Journey Optimizer] -fragmenten. In plaats daarvan kunt u echter algemene variabelen gebruiken, zoals hieronder beschreven.

Laten wij zeggen u de *sport* variabele in uw fragment wilt gebruiken.

1. Verwijs naar deze variabele in het fragment, bijvoorbeeld:

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. Bepaal de variabele met **laat** functie binnen het blok van het besluitvormingsbeleid. In het voorbeeld hieronder, *sport* wordt bepaald met de attributen van het besluitvormingspunt:

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**de inhoudsbevestiging van het het puntfragment van het Besluit**

* Wegens de dynamische aard van deze fragmenten, wanneer gebruikt in een campagne, wordt de berichtbevestiging tijdens de verwezenlijking van de campagneinhoud overgeslagen voor fragmenten die in besluitpunten van verwijzingen worden voorzien.

* De validatie van de fragmentinhoud vindt alleen plaats tijdens het maken en publiceren van het fragment.

* In het geval van JSON-fragmenten is de geldigheid van het JSON-object niet gegarandeerd. Zorg ervoor dat de inhoud van het uitdrukkingsfragment een geldige JSON is zodat het in besluitvormingspunten kan worden gebruikt.

Tijdens runtime wordt de inhoud van de campagne (inclusief fragmentinhoud van besluitvormingsitems) gevalideerd. Als de validatie mislukt, wordt de campagne niet weergegeven.
