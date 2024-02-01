# Les 2.3 Verdieping Backend
## Express
Opdracht: we maken onze eerste eenvoudige webserver met behulp van Node.js en Express. Zie bij deze opdracht het voorbeeld wat we hebben behandeld in de les en het vergelijkbare voorbeeld op [Hello World](https://expressjs.com/en/starter/hello-world.html).

1. open een terminal
2. maak een nieuwe folder voor je nieuwe node project (`mkdir`)
3. ga naar deze folder (`cd`)
4. start een nieuw node project (`npm init`)
5. installeer express voor dit project (`npm install express`)
6. maak een bestand `index.js` met de code van je server. Maak hierin tenminste één route aan, die als als antwoord op een request de response `Hello World` terugstuurd
7. start de server (`node index.js`)
8. doe vanuit je browser een http request naar deze server op de URL localhost:8000 (of een ander door jou gekozen poortnumer) en kijk of het werkt. Zo niet, check in elk geval in je terminal of je daar een probleem ziet.

Een paar vragen voor als je klaar bent:
* Je hebt net een server gemaakt. Waar draait deze en wat gebeurt er als je je computer uitzet?
* Wat is `localhost` en hoe verschilt dit van een ander domein?

**Push je code**  
Commit je webserver code naar je GitHub repository.  

## Routes en static
Opdracht: breid je webserver uit met meerdere routes en de mogelijkheid om static content (zoals images en een stylesheet) te serveren.

Voordat je begint, is het verstandig je verder te verdiepen in de techniek met behulp van onderstaande resources.
* [🎦 Bekijk een video over routing en express.](https://www.youtube.com/watch?v=SRHQ3FM39Qg)
* [Introducing Express on MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction#introducing_express)
* [Basic Routing](https://expressjs.com/en/starter/basic-routing.html)
* [Express Routing guide](https://expressjs.com/en/guide/routing.html)
* [Static Files](https://expressjs.com/en/starter/static-files.html)  

Je bent nu klaar om je server uit te breiden met meer functionaliteit. Voeg in elk geval onderstaande drie dingen toe:

1. **Basic routing:** Zorg dat je server verschillende responses kan geven op een aantal verschillende `routes` (b.v. `/about` of `/login`) die nuttig zijn voor je matching-application. Kun je al een route maken met een route parameter, bijvoorbeeld `profile/:username`?
2. **Error handling:** Antwoord met een `404 Not Found` als een route wordt opgevraagd die niet bestaat.
3. **Serve static files:** Zoals CSS en afbeeldingen.

Een vraag voor als je klaar bent:
* Wat zijn precies de `req` and `res` parameters die je in je routes gebruikt?

**Push je code**  
Push de nieuwste versie van je webserver code naar je GitHub repository.  

## Templating engine
Opdracht: gebruik de templating engine om voor je routes views te renderen met dynamische data.

Bestudeer eerst onderstaande resource voor meer informatie en voorbeelden voor het gebruik van EJS met Node.js
* [EJS templates met Node](https://www.digitalocean.com/community/tutorials/how-to-use-ejs-to-template-your-node-application)

1. installeer en configureer de templating engine EJS
   
2. maak een paar views voor verschillende routes en laat die renderen vanuit de callback functies voor die routes. Begin met eenvoudige HTML (zonder dynamische logica) in je views en zorg dat er voor elke route een andere view wordt gerenderd.

3. probeer vervolgens vanuit je views dynamische data te tonen. Je kunt in de code van je Node.js webserver een variabele, JavaScript object of array definieren, en de waarde daarvan doorgeven aan de templating engine vanuit je callback functie. Als je een route hebt met een route parameter, is het interessant om de waarde van die route parameter als variabele door te geven aan je view en vanuit daar te tonen.
  
4. Ontdek meer mogelijkheden van je templating engine. Probeer in elk geval:
   * [`includes`](https://ejs.co/#includes); om de inhoud van een (partial) view in een andere view op te nemen.
   * [`if en else`](https://www.includehelp.com/node-js/ejs-if-else-statement-ejs-conditions.aspx); om stukken HTML wel of niet te tonen afhankelijk van de voorwaarden
   * [`loops`](https://www.includehelp.com/node-js/ejs-for-loops.aspx); om een lijst van items uit te schrijven

**Push je code**  
Push tenslotte weer de nieuwste versie van je webserver code naar je GitHub repository.  
