# specificiteit

In deze oefening oefen je op de [voorrangsregels](https://webtechnologie.apload.be/css/voorrangsregels): welke stijlregel wint als er meerdere regels op hetzelfde element van toepassing zijn?

## Stap 1: neem de code over

Neem de onderstaande HTML over in `index.html`. Verander niets aan de structuur, de classes of de id.

```html
<main id="content">
	<article class="article">
		<p>Paragraaf 1</p>
		<p class="intro">Paragraaf 2</p>
		<p class="intro highlight">Paragraaf 3</p>
		<p class="intro" id="summary">Paragraaf 4</p>
		<p class="alert tip">Paragraaf 5</p>
	</article>
</main>
```

Neem daarna deze stijlregels over in `css/style.css`. Hou de volgorde exact zoals hieronder, want die volgorde doet mee.

```css
p {
	color: black;
}
article p {
	color: green;
}
.intro {
	color: blue;
}
.highlight {
	color: teal;
}
p.intro.highlight {
	color: orange;
}
#summary {
	color: purple;
}
.tip {
	color: brown;
}
.alert {
	color: magenta;
}
```

## Stap 2: bereken de specificiteit

Noteer in je stylesheet **boven elke stijlregel** de specificiteit van die selector in een commentaar, in de notatie uit de theorie (bv. `/* 0,0,2,0 */` voor `article p`).

## Stap 3: voorspel de kleur

Voorspel voor elke paragraaf welke kleur hij krijgt en waarom. Noteer je voorspelling bovenaan je stylesheet in een commentaarblok, bijvoorbeeld:

```css
/*
	paragraaf 1: ... want ...
	paragraaf 2: ... want ...
*/
```

Let goed op bij paragraaf 5: beide selectoren die erop passen hebben **dezelfde** specificiteit. Wat bepaalt dan wie wint? En is dat de volgorde van de classes in het `class`-attribuut, of de volgorde van de regels in de stylesheet?

## Stap 4: controleer

Open de pagina nu pas met Live server en controleer je voorspellingen. Zat je ergens fout, zoek dan uit waarom en pas je commentaar aan.

> Tip: als je in Codium met je muis over een selector zweeft, toont Codium de specificiteit van die selector. Inspecteer in de DevTools van je browser ook eens een paragraaf: de doorstreepte regels zijn de regels die het verloren hebben.

## Stap 5: overschrijf zonder te slopen

Zorg er nu voor dat paragraaf 2 toch dezelfde groene kleur krijgt als paragraaf 1. Daarbij gelden drie regels:

* je mag geen enkele bestaande stijlregel aanpassen of verwijderen
* je mag `!important` niet gebruiken
* je mag niets aanpassen in de HTML

Je voegt dus **één** nieuwe stijlregel toe, met een selector die een hogere specificiteit heeft dan `.intro`. Controleer achteraf dat paragraaf 3, 4 en 5 hun kleur behouden.
