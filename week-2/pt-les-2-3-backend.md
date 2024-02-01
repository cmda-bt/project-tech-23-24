# Les 2.3 Verdieping Backend
## Express
Oefening: we maken onze eerste eenvoudige webserver met behulp van Node.js en Express. Zie bij deze opdracht het voorbeeld wat we hebben behandeld in de les en het vergelijkbare voorbeeld op [Hello World](https://expressjs.com/en/starter/hello-world.html).

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
* [_Introducing Express on MDN_](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction#introducing_express)
* [Basic Routing](https://expressjs.com/en/starter/basic-routing.html)
* [_Express Routing guide_](https://expressjs.com/en/guide/routing.html)
* [Static Files](https://expressjs.com/en/starter/static-files.html)  

Je bent nu klaar om je server uit te breiden met meer functionaliteit. Voeg in elk geval onderstaande drie dingen toe:

1. **Basic routing:** Zorg dat je server verschillende responses kan geven op een aantal verschillende `routes` (b.v. `/about` `/login`) die nuttig zijn voor je matching-application.
2. **Error handling:** Antwoord met een `404 Not Found` als route wordt opgevraagd die niet bestaat.
3. **Serve `static files`:** zoals CSS en afbeeldingen.

Een vraag voor als je klaar bent:
* Wat zijn precies de `req` and `res` parameters die je in je routes gebruikt?

**Push je code**  
Push de nieuwste versie van je webserver code naar je GitHub repository.  

## Templating engine
Gebruik de templating engine om voor een route een view te renderen.
Push je changes

* [_Using template engines with Express_][intro-templating]
> Learn how to use a templating engine to dynamically render data and create components for your matching application.
> 
   
2. Then, **create views and try to render a page** using the templating engine. Start with 'simple' HTML pages and make sure you get different .html for each route.

3. Then, **render dynamic data** using your templating engine. So instead of you writing the .html insert some dynamic data. For example; you can store and array or object on the server and _inject_ data into the view. Later we'll look at how to insert data from a database.
  
4. **Use the features** of your templating engine. Try out atleast the following:
   * Use[`includes`](https://ejs.co/#includes); to insert contents of files into another.
   * Use [`conditionals`](https://pugjs.org/language/conditionals.html); if statements to render html conditionally
   * Use [`mixins`](https://pugjs.org/language/mixins.html); create small reusable blocks of html

5. **Start building out your components** for your matching application feature. You can create different partials and [lay-outs](https://pugjs.org/language/inheritance.html) (includes) for components of your page e.g. header, footer or a form.

> 💡 It's very common to create a consistent naming convention and folder structure for your components. Most people base it on the [Atomic Design method](https://atomicdesign.bradfrost.com/chapter-2/) by Brad Frost. [Here's an example](https://github.com/iSirThijs/Player2) with different partials and lay-out components.

**Ask yourself upon completion:**
* How does express combine the data from the server with the templating engine?
* How do partials work? Can you create a folder structure for all the components?

**Additional resources**
* [Using template engines with Express][template]
