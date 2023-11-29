> _Fork_ deze leertaak en ga aan de slag. 
Onderstaande outline ga je gedurende deze taak in jouw eigen GitHub omgeving uitwerken. 
De instructie vind je in: [docs/INSTRUCTIONS.md](docs/INSTRUCTIONS.md)

# Buurtinitiatieven amsterdam west
De directie van De Hallen heeft ons gevraagt om een website te bouwenvanuit de nieuwe Stichting voor buurtinitiatieven. Het is de bedoeling om een online platform te maken waar buurtinitiatieven uit Oud-West verzameld en bekeken kunnen worden.

## Inhoudsopgave
  * [Beschrijving](#beschrijving)
  * [Kenmerken](#kenmerken)
  * [Bronnen](#bronnen)
  * [Licentie](#licentie)

## Beschrijving
Ik heb deze sprint gewerkt aan deze user stories, [overzicht van initiatieven](https://github.com/fdnd-agency/de-hallen/issues/1), [informatie over initiatief](https://github.com/fdnd-agency/de-hallen/issues/2) en [contact formulier](https://github.com/fdnd-agency/de-hallen/issues/4). 
De website heeft verschillende pagina's. 

### 📸 Homepage
De homepage waar je een klein overzicht ziet van wat er deze week te doen is en wat er in de buurt te doen is. Dit hoort bij [overzicht van initiatieven](https://github.com/fdnd-agency/de-hallen/issues/1).

<img width="200" alt="Homepage mobile" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/6149251e-8e3c-41cc-8476-9e3d9bf9b848">
<img width="800" alt="Homepage" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/77e92d14-09a2-4b0b-9f15-ed3b8ee4884f">

### 📸 Aanbodpage
De aanbodpage waar alle initiatieven te bekijken zijn. Met filters zodat je makkelijker kan vinden wat je leuk vindt. Dit hoort bij [overzicht van initiatieven](https://github.com/fdnd-agency/de-hallen/issues/1).

<img width="200" alt="Aanbodpage mobile" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/4fa2b406-d1ed-4ce3-93c5-062736526dbe">
<img width="800" alt="Aanbodpage" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/a231ef3e-15e6-4ece-93eb-266c9e61f30e">


### 📸 Initiatiefpage
De initiatiefpage waar je alle informatie van het initiatief kunt bekijken. Dit hoort bij [informatie over initiatief](https://github.com/fdnd-agency/de-hallen/issues/2).

<img width="200" alt="Initiatiefpage mobile" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/81be6f0b-8b2c-4b8f-8ac5-61b4dc3a885f">
<img width="800" alt="Initiatiefpage" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/5154df03-3590-4f98-8dfa-23a52d159925">

### 📸 Contactpage
De contactpage waar je een idee voor een initiatief kunt invoeren en op sturen zodat het uiteindelijk op de website komt te staan. Dit hoort bij [contact formulier](https://github.com/fdnd-agency/de-hallen/issues/4).

<img width="200" alt="Contactpage mobile" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/82654cb5-dc1b-45b2-9752-ed31988d2b8b">
<img width="800" alt="Contactpage" src="https://github.com/zoepje/look-and-feel-corporate-identity/assets/144004461/1bcdf50f-f4a1-4bd2-88c3-fb3832f2987e">

### 🌐 [Mijn website](https://zoepje.github.io/look-and-feel-corporate-identity/)

## Kenmerken
Bij het bouwen van deze website heb ik gebruik gemaakt van HTML en CSS.
De HTML van elke pagina heeft een `head` met daarin linkjes naar de css bestanden en een link naar google icons. Dan hebben we een `body` die per pagina een beetje anders is ingedeeld. Maar in het algemeen bestaat de `body` uit een `header`, `nav`, `aside`, `main` & `footer`.


Ik heb voor elke pagina een CSS bestand aangemaakt en alle paginas zijn gelinkt aan de main CSS. Ik heb gebruik gemaakt van custom properties.
```css
:root{
  /* Font */
  --primaryFont: system-ui, -apple-system, Roboto, 'Open Sans', sans-serif;
  --secondaryFont: system-ui, -apple-system, Verdana, sans-serif;
	
  /* Kleuren */
  --primaryColor: #34787e;
  --secondaryColor: #c2edce;
  --tertiaryColor: #85bf97;
  --quaternaryColor: #48abb6;
  
  --lightColor100: #ffffff;
  --lightColor200: #f6f6f2;
  --lightCoror300: #e7ece2;

  --darkColor100: #000000;
  --darkColor200: #2f2f2f;
  
  --linkColor: #0151a8;
  --linkColorHov: #25575b;

  /* margin/padding */
  --primaryMargin: 1rem;
  --primaryPadding: 1rem;
  --lineLenght: 30rem;
}
```

Ook heb ik `:hover` gebruikt om ervoor te zorgen dat de kaartjes van grootte veranderen en meer informatie laten zien.

```css
/* Card wordt groter zodat de explanation te lezen is */
.card:hover{
  height: 50vh;

  & img {
    display: none;
  }

  & .explanation {
    opacity: 1;
    overflow: unset;
  }
}
```

En ik media queries gebruikt om de layout te veranderen als je op je laptop de website bekijkt.
```css
@media only screen and (min-width: 750px){
  body{
    display: grid;
    grid-template-columns: 1fr 5fr;
    grid-template-areas:
      "h h"
      "n n"
      "a m"
      "f f";
  }
  
  header{
    grid-area: h;
  }
  
  nav{
    grid-area: n;
  }
  
  aside{
    grid-area: a;
  }
  
  main{
    grid-area: m;
  }

  footer{
    grid-area: f;
  }

  .initiatief{
    width: 85vw; /* Zorgt ervoor dat de grid niet wordt geclipt */
  }
}
```

Als je meer details wilt weten over hoe ik dit nou gebouwt heb kun je dit [hier in mijn wiki](https://github.com/zoepje/look-and-feel-corporate-identity/wiki/3.-Bouwen) bekijken.

## Bronnen
* 
* 

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
