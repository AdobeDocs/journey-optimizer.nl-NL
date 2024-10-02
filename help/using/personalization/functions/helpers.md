---
title: Helpers
description: Helpers
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 110c4895ac7f0b683a695e9705a8f8ac54d09637
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# Helpers {#gs-helpers}

## Standaardwaarde voor alternatieven{#default-value}

De `Default Fallback Value` helper wordt gebruikt om een standaardreservewaarde terug te keren als een attribuut leeg of ongeldig is. Dit mechanisme werkt voor Profielkenmerken en Reisgebeurtenissen.

**Syntaxis**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In dit voorbeeld wordt de waarde `there` weergegeven als het `firstName` -kenmerk van dit profiel leeg of null is.

## Voorwaarden{#if-function}

De hulpfunctie `if` wordt gebruikt om een voorwaardelijk blok te definiëren.
Als de uitdrukkingsevaluatie waar terugkeert, wordt het blok teruggegeven anders wordt het overgeslagen.

**Syntaxis**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Na de hulpfunctie `if` kunt u een instructie `else` invoeren om een codeblok op te geven dat moet worden uitgevoerd als dezelfde voorwaarde false is.
De instructie `elseif` geeft een nieuwe voorwaarde op die moet worden getest als de eerste instructie false retourneert.


**Formaat**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Voorbeelden**

1. **geeft verschillende opslagverbindingen terug die op voorwaardelijke uitdrukkingen** worden gebaseerd

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **bepaal de uitbreiding van het e-mailadres**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **voeg een voorwaardelijke verbinding** toe

   Met de volgende bewerking voegt u een koppeling toe naar de website &#39;www.adobe.com/academia&#39; voor profielen met alleen de e-mailadressen &#39;.edu&#39;, naar de website &#39;www.adobe.com/org&#39; voor profielen met de e-mailadressen &#39;.org&#39; en de standaard-URL &#39;www.adobe.com/users&#39; voor alle andere profielen:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Voorwaardelijke inhoud die op publiekslidmaatschap wordt gebaseerd**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Meer over publiek en de segmentatieservice leren, verwijs naar deze [ sectie ](../../audience/about-audiences.md).


## Tenzij{#unless}

De hulpfunctie `unless` wordt gebruikt om een voorwaardelijk blok te definiëren. Als de evaluatie van de expressie false retourneert, wordt het blok gerenderd als dit tegengesteld is aan de functie `if` .

**Syntaxis**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Voorbeeld**

Enige inhoud renderen op basis van extensie e-mailadres:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Elk{#each}

De hulpfunctie `each` wordt gebruikt om een array te doorlopen.
De syntaxis van de hulplijn is ```{{#each ArrayName}}``` YourContent {{/each}}
Wij kunnen naar de individuele seriepunten verwijzen door het sleutelwoord **dit** binnen het blok te gebruiken. De index van het element van de array kan worden gerenderd met {{@index}} .

**Syntaxis**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Voorbeeld**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Voorbeeld**

Een lijst met producten weergeven die deze gebruiker in zijn winkelwagentje heeft:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

## Met{#with}

De `with` helper wordt gebruikt om het evaluatietoken van malplaatje-deel te veranderen.

**Syntaxis**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

De hulpfunctie `with` is nuttig om ook een sneltoetsvariabele te definiëren.

**Voorbeeld**

Wordt gebruikt met voor het aliasing van lange variabelenamen naar kortere namen:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Laat{#let}

Met de functie `let` kan een expressie worden opgeslagen als een variabele die later in een query moet worden gebruikt.

**Syntaxis**

```sql
{% let variable = expression %} {{variable}}
```

**Voorbeeld**

In het volgende voorbeeld kunt u de totale som van prijzen voor producten in de winkelwagen berekenen met prijzen tussen 100 en 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```
