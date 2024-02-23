# Les 3.2 Verdieping backend
## Boilerplate
Verspreid over de lessen en opdrachten kom je verschillende stukken code tegen die je nodig hebt om je webserver aan de praat te krijgen. Deze zijn verzameld in een [boilerplate voor je Node.js webserver](/verdieping-backend/server-boilerplate.js), zodat je niet de sheets hoeft over te typen ;)

## Formulieren verwerken
Tot nu toe hebben we met onze server alleen informatie (HTTP responses) naar de client gestuurd. Een eenzijdige conversatie. We gaan nu ook gegevens ontvangen van onze gebruikers, bijvoorbeeld uit formulieren die ze invullen. Denk aan een fornulier om een nieuw account aan te maken, in te loggen, je profiel bij te werken, etc.

Er zijn twee manieren om in een HTTP request van de client naar de server data mee te sturen:
1. In de querystring als onderdeel van de URL. Bijvoorbeeld:
```productoverzicht.html?producttype=laptops&pagina=5```
De variabelen zijn nu zichtbaar in de URL, zowel voor gebruikers als zoekmachines. Soms is dit handig, zoals in het voorbeeld hierboven, maar vaak ook niet. Bovendien beperkt zich dit tot een kleine hoeveelheid korte informatie. Een profielfoto of lange beschrijving kun je hier niet in kwijt.
2. In de body van de HTTP request. De informatie wordt nu 'onder water' mee gestuurd in de HTTP request. Dit is bijvoorbeeld wat er gebeurt als we een formulier posten. Dit heb je trouwens ook gedaan toen je eerder met Postman requests stuurde naar onze Data API en daarbij JSON meegaf. Met deze methode is er ruimte voor meer uitgebreide informatie.

We gaan vandaag verder aan de slag met optie 2. Hierbij vult de gebruiker een formulier in en drukt op de submit knop. Op dat moment stuurt de browser een HTTP request naar de server, naar de URL die als *action* in het formulier is opgegeven. De te gebruiken HTTP request *method* wordt ook in het formulier aangegeven. Normaal gesproken is dit **POST**.

**Opdracht: Formulier posten**

Breid je node.js server uit met code om een gepost formulier te verwerken. Je kunt hiervoor het inlogformulier uit de vorige les gebruiken, als je daaruit eerst de (front-end) JavaScript weghaalt. We gaan deze functionaliteit nu immers in de back-end bouwen. 
1. Maak in je node.js server een route en een view om je formulier te tonen
2. Geef het formulier een action en de method POST
3. Maak een route om de POST request af te handelen als het formulier wordt verstuurd
4. Maak een view om een HTTP response op de POST request te sturen. Laat in deze view de ontvangen formulier data zien. De ingevulde formulier velden zijn beschikbaar als eigenschappen van **req.body** als je in Express de juiste middleware hebt aangezet met ```app.use(express.urlencoded({extended: true}))```

Als dit gelukt is, kun je zien dat de verstuurde formulier data op de server is aangekomen. Op dit moment wordt deze daar nog niet bewaard. Daarvoor hebben we de volgende stap nodig: het maken van een verbinding met een database.

Tips:
* Begin klein. Kijk eens of je een formulier met 1 input veld aan de praat kunt krijgen. Daarna kun je het altijd nog uitbreiden met meer. Bouw je werk stap voor stap op.
* Commit regelmatig en push je werk naar GitHub. De eerste versies hoeven niet perfect te zijn, probeer zo ver te komen als je kunt
* Bekijk voorbeelden in onze slides, op Internet en kijk vooral ook hoe je mede-studenten het aanpakken.

## Database
In dit project gebruiken we MongoDB als database. De eerste stap is het aanmaken van een MongoDB Atlas account met daarin een eigen database.

[MongoDB Atlas](https://www.mongodb.com/atlas/database) is een DBaaS, oftewel database as a service. Dit is een dienst die via de cloud wordt aangeboden, zodat we niet zelf een database hoeven te installeren op onze laptop. Voor dit project kunnen we gebruik maken van een gratis account. Voor grotere projecten in een productieomgeving zou je waarschijnlijk wel een betaald abonnement willen afsluiten. 

Het aanmaken van je database is niet moeilijk, maar er is wel een flink aantal stapjes voor nodig. Volg de instructies daarom zorgvuldig, want als je een stap overslaat, gaat de rest ook niet werken. En stel vooral je vragen op Teams in het #back-enders kanaal als je vastloopt.

**Opdracht: opzetten van de database verbinding**

Volg de instructies in de officiele [MongoDB start with guide](https://www.mongodb.com/docs/guides/atlas/account/). Hierin staan de volgende stappen:
1. Create MongoDB account
2. Create a cluster
3. Add a database user
4. Configure a network connection
5. Load sample data (optioneel, misschien vind je het fijner zelf testdata aan te maken die past bij je eigen project)
6. Get connection string

Bij stap 4 geef je aan vanaf welke IP adressen je node.js server straks verbinding mag maken met de database. Je kunt hier je huidige IP-adres toevoegen, maar als je op verschillende plekken werkt met een laptop, zal je IP-adres ook steeds veranderen. Op de HvA krijg je bijvoorbeeld elke keer een ander IP-adres toegewezen als je inlogt op Eduroam. Je kunt alle HvA adressen toevoegen met een [*subnetmask*](https://www.youtube.com/watch?v=yK__SdS2meo) door als IP-adres ```145.0.0.0/8``` toe te voegen. Voeg daarnaast ook je IP-adres thuis toe en eventueel andere adressen die je wilt gebruiken. Als je node.js server geen verbinding wil maken met de database, is het altijd goed om even te checken wat je [huidige IP-adres](https://showip.net/) is en dit toe te voegen aan de whitelist.

🚨 Zet nooit je gebruikersnaam, wachtwoord en URL van de database in je code. Als dit eenmaal op GitHub staat (al is het in een oudere commit) is het een kwestie van tijd voordat hackers je database over zullen nemen. Zet daarom dit soort info in een los ```.env``` file en voeg dit toe aan je ```.gitignore```.

🎦 [Bekijk een video over .env](https://www.youtube.com/watch?v=17UVejOw3zA)

* Je kunt nu code toevoegen aan je node.js webserver om een verbinding met je database te openen.
* Maak met de hand wat testdata aan in je database. Dat kan rechtstreeks in de webinterface van MongoDB, maar het kan ook handig zijn de [MongoDB GUI compass](https://www.mongodb.com/products/tools/compass) te downloaden en gebruiken.
* Maak een route aan in je node.js server en doe daarin een find. Vervolgens kun je de gevonden data naar de console loggen. Als je dan in de terminal een javascript object ziet wat overeenkomt met de inhoud van je database, is het mission accomplished.

**Theorie**

Voor je verder gaat, is het goed meer te leren over MongoDB:
* [Introduction to MongoDB](https://www.mongodb.com/docs/manual/introduction/)
* [Introduction to documents](https://www.mongodb.com/docs/manual/core/document/)
* MongoDB gebruiken vanuit Node.js met de [MongoDB module](https://www.npmjs.com/package/mongodb)

**Opdracht: werk verder aan je component**

Je hebt nu alle informatie om je component te kunnen bouwen. Je server kan informatie sturen en ontvangen en die informatie kan permanent worden opgeslagen in een database, zodat deze ook bewaard blijft als je de server uitzet. Je kunt nu verder werken aan de volgende zaken:
1. **URL structuur**: welke URL's heeft je component voor de verschillende pagina's en hoe zijn de URL's opgebouwd? Met welke routes in Node.js komt dit overeen en zijn er ook route parameters zoals ```profiel/:gebruikersnaam```?
2. **Data modelling**: welke soorten objecten wil je opslaan in de database? Misschien zijn er meerdere soorten objecten, zoals bijvoorbeeld gebruikers, sportscholen, games, artiesten, katten, fashion-styles etc. Dit zouden verschillende collecties in je database kunnen worden. Welke informatie ga je precies opslaan voor een object? Heeft een gebruiker bijvoorbeeld een naam, of een voornaam en een achternaam? Welke datatypes ga je gebruiken? Een like kan bijvoorbeeld een boolean (true or false) zijn. Is een telefoonnummer een getal of een string?
3. Welke **CRUD operaties** van MongoDB heeft je component nodig? Bijvoorbeeld find om data uit een collectie te lezen, insert om nieuwe data toe te voegen, of update om bestaande data te wijzigen.

Tip: probeer weer zoveel mogelijke kleine stapjes te zetten. Voeg een klein stukje functionaliteit toe en check of het werkt. Zo nee, dan is het vinden van het probleem relatief overzichtelijk. Werkt het wel, dan kun je verder naar de volgende kleine stap.
