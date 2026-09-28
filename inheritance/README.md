# inheritance

In deze oefening onderzoek je hoe [overerving](https://webtechnologie.apload.be/css/cascade/inheritance) werkt en hoe [CSS variabelen](https://webtechnologie.apload.be/css/variabelen) daarvan gebruik maken.

## Stap 1: korte experimenten

1. Maak een `section` met `color: darkslategray` en een `p` en `a` erin. Controleer of de link dezelfde kleur heeft. Zo nee, waarom?
2. Geef een `nav` een `font-family` en forceer dat een `button` binnen die `nav` die font-family erft, zelfs als `button` normaal anders zou worden gestyled.
3. Zet een `article` op `font-size: 18px`. Gebruik `initial` in één van de child-elementen en observeer het verschil.

## Stap 2: variabelen erven door

Neem de tabel uit de oefening `schedule` erbij, of bouw een kleine tabel van drie rijen en drie kolommen.

* Definieer op `:root` twee variabelen: één voor de achtergrondkleur van een cel en één voor de tekstkleur.
* Gebruik die variabelen in de stijlregel voor `td`. Verklaar waarom dat werkt terwijl je de variabelen helemaal bovenaan het document hebt gedefinieerd.
* Herdefinieer nu diezelfde variabelen op één enkele `tr`. Wat gebeurt er met de cellen in die rij, en wat met de rest van de tabel?
* Controleer in de DevTools van je browser welke waarde een `td` in die rij effectief krijgt.

> Tip: `background-color` erft normaal niet, maar de **variabele** erft wel. Dat verschil is precies wat deze stap duidelijk maakt.
