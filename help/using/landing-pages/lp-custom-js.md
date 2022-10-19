---
solution: Journey Optimizer
product: journey optimizer
title: Aangepast JavaScript gebruiken in een openingspagina
description: Leer hoe u de inhoud van een bestemmingspagina in Journey Optimizer ontwerpt
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# Aangepast JavaScript gebruiken in een openingspagina {#lp-custom-js}

U kunt de inhoud van de bestemmingspagina definiëren met behulp van aangepaste JavaScript. Als u bijvoorbeeld geavanceerde opmaak moet toepassen of aangepaste gedragingen wilt toevoegen aan uw bestemmingspagina&#39;s, kunt u uw eigen besturingselementen maken en deze uitvoeren in [!DNL Journey Optimizer].

## JavaScript-code invoegen in een bestemmingspagina

Als u aangepaste JavaScript wilt invoegen in openende pagina-inhoud, kunt u het volgende doen:

* Importeer bestaande HTML-inhoud wanneer u begint met het maken van uw inhoud en selecteer het bestand dat uw aangepaste JavaScript-code bevat. Leer hoe u inhoud importeert [in deze sectie](../design/existing-content.md).

* Ontwerp de openingspagina helemaal zelf of op basis van een opgeslagen sjabloon. Sleep de **[!UICONTROL HTML]** inhoudcomponent op het canvas en toon de broncode om uw JavaSCript in de component toe te voegen. Leer hoe u de component HTML gebruikt in [deze sectie](../design/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* Typ of plak JavaScript-code rechtstreeks in de inhoudsontwerper. Leer hoe u uw eigen inhoud codeert [in deze sectie](../design/code-content.md).

>[!NOTE]
>
>U kunt JavaScript momenteel niet in actie tonen wanneer [een voorvertoning weergeven van de bestemmingspagina](create-lp.md#test-landing-page).

Gebruik de volgende syntaxis zoals beschreven in de onderstaande secties om de openingspagina correct weer te geven.

## Codeinitialisatie

Als u uw JavaScript-code wilt initialiseren, moet u de opdracht `lpRuntimeReady` gebeurtenis. Deze gebeurtenis wordt geactiveerd nadat de bibliotheek is geïnitialiseerd. De callback wordt uitgevoerd met de `lpRuntime` -object om de bibliotheekmethode en -haken zichtbaar te maken.

`LpRuntime` staat voor &quot;Landing page Runtime&quot;. Dit object is de belangrijkste bibliotheekid. Hiermee worden koppelingen, methoden voor het verzenden van formulieren en andere hulpprogrammamethoden die in aangepaste JavaScript kunnen worden gebruikt, toegankelijk gemaakt.

**Voorbeeld:**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## Hooks

Met haken kunt u een methode toevoegen tijdens de levenscyclus van het verzenden van het formulier. U kunt bijvoorbeeld haken gebruiken om een formuliervalidatie uit te voeren voordat het formulier daadwerkelijk wordt verzonden.

Hier zijn de haken die u kunt gebruiken:

| Naam | Beschrijving |
|--- |--- |
| addBeforeSubmitHook | Aangepaste haak die moet worden aangeroepen voordat het formulier wordt verzonden. Retourneert true om door te gaan met verzenden, anders retourneert false om verzending te blokkeren. |
| addOnFailedHook | Aangepaste haak die moet worden aangeroepen bij mislukte formulierverzending. |
| addOnSuccessHook | Aangepaste haak die moet worden aangeroepen wanneer het formulier is verzonden. |

**Voorbeeld:**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## Aangepaste formulierverzending

De hieronder vermelde methoden worden gebruikt om aangepaste formulierverzendingen uit te voeren.

>[!NOTE]
>
>Aangezien de formulierverzending wordt afgehandeld door aangepaste JavaScript, moet de standaardverzending expliciet worden uitgeschakeld door een algemene variabele in te stellen `disableDefaultFormSubmission` tot `true`.

| Naam | Beschrijving |
|--- |--- |
| submitForm | Met deze methode wordt het formulier verzonden en wordt de post-verzendstroom afgehandeld. |
| submitFormPartial | Met deze methode wordt ook het formulier verzonden, maar wordt de stroom na verzending overgeslagen. Als u bijvoorbeeld de omleiding naar de pagina voor succesmeldingen hebt geconfigureerd nadat de verzending is voltooid, vindt die omleiding niet plaats in het geval van gedeeltelijke formulierverzending. |

**Voorbeelden:**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## Hulpfunctie

| Naam | Beschrijving |
|--- |--- |
| getFormData | Deze methode kan worden gebruikt om de `formData` in de vorm van een JSON-object. Dit object kan worden doorgegeven aan `submitForm` voor het verzenden van formulieren. |

**Voorbeeld:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Gebruiksscenario’s

### Hoofdlettergebruik 1: Validatie toevoegen vóór verzending van formulier

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### Hoofdlettergebruik 2: Gedeeltelijke verzending van formulieren

U hebt bijvoorbeeld een formulier met meerdere selectievakjes op de pagina. Als u een selectievakje inschakelt, wilt u dat deze gegevens op de achtergrond worden opgeslagen zonder dat de gebruiker op de verzendknop hoeft te klikken.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### Hoofdlettergebruik 3: Aangepaste analysetags

Met JavaScript kunt u listeners van invoervelden toevoegen en een aangepaste trigger voor de analytische aanroep koppelen.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### Hoofdlettergebruik 4: Dynamisch formulier

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
