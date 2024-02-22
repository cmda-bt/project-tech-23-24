# Les 3.2 Verdieping backend

## Formulieren verwerken
Tot nu toe hebben we met onze server alleen informatie (HTTP responses) naar de client gestuurd. Een eenzijdige conversatie. We gaan nu ook gegevens ontvangen van onze gebruikers, bijvoorbeeld uit formulieren die ze invullen. Denk aan een fornulier om een nieuw account aan te maken, in te loggen, je profiel bij te werken, etc.

Er zijn twee manieren om in een HTTP request van de client naar de server data mee te sturen:
1. In de querystring als onderdeel van de URL. Bijvoorbeeld:
```productoverzicht.html?producttype=laptops&pagina=5```
De variabelen zijn nu zichtbaar in de URL, zowel voor gebruikers als zoekmachines. Soms is dit handig, zoals in het voorbeeld hierboven, maar vaak ook niet. Bovendien beperkt zich dit tot een kleine hoeveelheid korte informatie. Een profielfoto of lange beschrijving kun je hier niet in kwijt.
2. In de body van de HTTP request. De informatie wordt nu 'onder water' mee gestuurd in de HTTP request. Dit is bijvoorbeeld wat er gebeurt als we een formulier posten. Met deze methode is ruimte voor meer uitgebreide informatie.

We gaan vandaag aan de slag met optie 2. Hierbij vult de gebruiker een formulier in en drukt op de submit knop. Op dat moment stuurt de browser een HTTP request naar de server, naar de URL die als *action* in het formulier is opgegeven. De te gebruiken HTTP request *method* wordt ook in het formulier aangegeven. Normaal gesproken is dit **POST**.

**Opdracht: Formulier posten**

Breid je node.js server uit met code om een gepost formulier te verwerken:
1. Maak in je node.js server een route en een view om je formulier te tonen
2. Geef het formulier een action en de method POST
3. Maak een route om de POST request af te handelen als het formulier wordt verstuurd
4. Maak een view om een HTTP response op de POST request te sturen. Laat in deze view de ontvangen formulier data zien.

Als dit gelukt is, kun je zien dat de verstuurde formulier data op de server is aangekomen. Op dit moment wordt deze daar nog niet bewaard. Daarvoor hebben we de volgende stap nodig: het opslaan van gegevens in een database.

Tips:
* Begin klein. Kijk eens of je een formulier met 1 input veld aan de praat kunt krijgen. Daarna kun je het altijd nog uitbreiden met meer. Bouw je werk stap voor stap op.
* Commit regelmatig en push je werk naar GitHub. De eerste versies hoeven niet perfect te zijn, probeer zo ver te komen als je kunt
* Bekijk voorbeelden in onze slides, op Internet en kijk vooral hoe je mede-studenten het aanpakken.

## Database
We'll cover actually storing the user input and learning about databases the next lesson but what you already do is create a MongoDB atlas account and set-up your mongodb connection.

All of your data is going to be stored in MongoDB. Take ± 2 hours to set-up your database and connect to it. There are roughly two options: go with a database as a service DBaaS or use MongoDB locally.

We highly recommend you use the DBaaS option (MongoDB atlas) that's why we don't include any instruction on how to set-up mongodb locally.

DBaaS
DBaaS stands for database as a service. Instead of having the database stored locally on your laptop, it saves your data to the cloud. MongoDB Atlas is a great option since they offer a free plan for prototypes. These are not meant to be used in production environments but for this course it's good enough for a prototype.

Setting-up a database connection isn't 'difficult' but there are lots of small steps involved. So read the guides carefully and follow each step. If you make a small mistake somewhere then all other steps won't work.

💡There isn't realy a 'good' way to check if the database connection is working. We think the best way to check is to actually fill your database with dummy data and try a find and console.log that to the terminal. If you get a javascript like object in the terminal that's the same as the data you put in the database it has works!

Ask questions in the #back-end channel if you are stuck! We try to link to relevant resources for common 'start-up' issues but if you encounter a specific problem don't try to fix it yourself but ask for help.

→ The best resource we found to set-up your database is the official 'MongoDB start with guide. Which roughly outline the following steps:

1. Create MongoDB account
2. Create a cluster
3. Add a database user
4. Configure a network connection
5. Load sample data
6. Get connection string
When you create your Cluster in Atlas you might need to Whitelist your IP.

🚨 Never ever put your username, password or database URI directly in your code. Store sensitive information such as your database URI, password and username in a .env using the dotenv package. Make sure you add the file to your .gitignore. If you commit your environment variables it's hard to undo!

Additional resources

Start using the MongoDB driver for Node.js
Hiding API Keys with Environment Variables - dotenv
