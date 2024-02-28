# Les 3.1 Formulieren

## Theorie

Leer meer over formulieren, soorten inputs en hun attributen door het volgende materiaal te bestuderen:
* 🎦 [Bekijk een video over formulieren](https://dlo.mijnhva.nl/d2l/le/content/536505/viewContent/1996729/View)
* De belangrijkste info uit bovenstaande video is ook terug te vinden in onze [kennisbank](https://bnieskens.notion.site/Formulieren-9265d336e2954c71be6be4ab847f8fcc)
* Learn [Web Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms) op MDN. Lees de hoofdstukken:
  * Introductory guides
  * The different form controls
  * Form styling guides en Validating
  * Submitting form data.

## Oefening: Login op basis van JSON

1. Bestudeer het [codevoorbeeld voor een inlogfomulier](https://scrimba.com/scrim/co3f042a6a22d4846e9104959) op Scrimba
2. Bespreek met je mede-studenten hoe dit precies werkt:
    * in welke variabelen staan de inloggevens die de gebruiker heeft ingevuld?
    * in welke variabelen staan de geldige inloggevens?
    * hoe worden de ingevulde gegevens vergeleken met de geldige gegevens?
3. Start je Data API en maak een paar gebruikers aan
    * gebruik tabbed postman in je browser om handmatig gebruikers toe te voegen
    * geef je users een naam en wachtwoord
4. Verander het codevoorbeeld zodat het de lijst met bestaande gebruikers ophaalt uit jouw Data API in plaats van het JSON bestand
    * welke URL moet je nu meegeven aan de Fetch API?
    * hoe is de structuur van de JSON-data uit de API anders dan de structuur van het eerdere JSON bestand?

## Oefening: Formulier voor het aanmaken van een nieuw account
* Maak een formulier waarmee nieuwe gebruikers zich kunnen registreren
* Een gebruiker heeft in elk geval een naam en een wachtwoord
* Voeg velden toe die voor jouw feature nuttig zijn: e-mail, leeftijd, woonplaats, favoriete muziek, huisdier???
* Maak alleen de HTML / CSS, dus nog geen JS code om het formulier te verwerken

Maak deze opdracht af voor de volgende les.

## Frontend verdieping

Volg pt-les-3-1-frontend.md

## Backend verdieping

Maak voor de volgende verdiepingsles vast een eigen Atlas MongoDB account en database aan volgens de instructies in de officiele [MongoDB start with guide](https://www.mongodb.com/docs/guides/atlas/account/). Volg in elk geval de stappen:
1. Create MongoDB account
2. Create a cluster
3. Add a database user
4. Configure a network connection
