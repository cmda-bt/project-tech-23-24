# Les 3.2 Formulieren verwerken

## Opdracht: Opslaan van nieuwe accounts

Bij deze opdracht gaan we verder met het formulier wat je hebt gemaakt voor het aanmaken van nieuwe accounts. We gaan er nu voor zorgen dat die nieuwe accounts ook echt bewaard gaan worden. Je kunt dan een nieuw account aanmaken en vervolgens, met het inlogformulier uit de vorige les, ook echt inloggen op dat nieuwe account.

De uitwerking van deze opdracht is verschillend voor de front-enders en de back-enders. Volg hieronder het stappenplan voor jouw verdieping.

**Formulier verwerken voor de FRONT-ENDERS**

We gaan nu een stuk JavaScript toevoegen aan je nieuwe formulier om te zorgen dat de ingevulde gegevens voor het nieuwe account ook worden opgeslagen door de Data API. 

1. Schrijf een JavaScript functie die wordt geactiveerd zodra de gebruiker het registratieformulier verstuurd. Doe dit door een onClick event toe te voegen aan de submit button.
2. Gebruik in je JavaScript functie de Fetch API om je nieuwe gebruiker op te laten slaan door de Data API. Hier komen een aantal nieuwe aspecten bij kijken. Bekijk de [documentatie over Fetch](https://developer.mozilla.org/en-US/docs/Web/API/fetch) om te zien hoe je deze nieuwe opties kunt toevoegen.
     * tot nu toe heb je met Fetch HTTP GET requests gedaan. Nu willen we een HTTP POST request doen. We zullen dus de request method moeten aangeven bij de aanroep van Fetch.
     * Het opslaan van gegevens via een API is 'gevaarlijker' dan alleen het uitlezen van gegevens. Je krijgt daarom nu te maken met een extra beveiling, de zogenaamde Cross-Origin Resource Sharing, oftewel CORS. Je zult nu bij de aanroep van Fetch de mode CORS moeten aangeven.
     * Tenslotte wil je nu ook een body meegeven aan je HTTP request met daarin de gegevens over de nieuwe gebruiker in JSON formaat. Hierbij moet je de indeling volgen zoals gespecificeerd in de README van de Data API.
3. Het is een goed idee om nu te controleren of je nieuwe gebruiker goed is opgeslagen. Dit kun je doen door in de browser met tabbed postman een actuele lijst op te vragen van alle gebruikers uit de Data API. Staat de nieuwe gebruiker er tussen en kloppen alle gegevens?
4. Kijk tenslotte of je nu het inlogformulier uit de vorige les kunt gebruiken om in te loggen als je nieuwe gebruiker

**Formulier verwerken voor de BACK-ENDERS**

Meer informatie om deze opdracht te kunnen maken, krijg je vandaag tijdens de backend verdiepingsles. Daarna kun je je formulier om nieuwe accounts te registeren werkend krijgen, door de onderstaande stappen te volgen. Dit is een uitgebreider stappenplan dan voor de front-enders, omdat we eerst het inlogformulier uit de vorige les gaan overzetten naar onze backend server.

Het onderstaande is best een uitgebreide opdracht. Neem er rustig de tijd voor, het hoeft niet in één keer af. Onthoud ook dat deze oefening bedoeld is om de techniek in de vingers te krijgen. De formulieren en bevestgingspagina's mogen er voor nu best simpel uitzien. En als je een gebruiker met twee eigenschappen in de database weet op te slaan, kun je het in principe ook met 10 eigenschappen. Dus begin klein.

1. Verwijder de (front-end) JavaScript uit het inlogformulier, want deze functionaliteit gaan wij nu in de backend realiseren.
2. Maak in je node.js webserver een nieuwe route en een view om het inlogformulier te tonen
3. Geef in het inlogformulier de ```<form>``` een geschikte action (door jou te kiezen URL) en method (POST) als attributen.
4. Maak in je webserver een nieuwe route aan om de POST request op deze URL te kunnen afhandelen
5. Laat deze route in eerste instantie een bevestigingspagina tonen met daarin de informatie die is ontvangen uit het inlogformulier
6. Breid de code in je route voor de bevestigingspagina uit met een stuk logica. Kies voor nu één vaste gebruikersnaam met een wachtwoord. Als de in het inlogformulier ingevulde gegevens daarmee overeenkomen, toon dan een welkomstpagina. Had de gebruiker iets anders ingevuld, toon dan een foutmelding.
7. Zodra je je database werkend hebt, kun je daarin met de hand een aantal testgebruikers aanmaken.
8. Je kunt nu in de code voor je route actuele informatie over je gebruikers uit de database halen. In plaats van de inloggegevens te vergelijken met één vaste waarde, kun je nu kijken of de gebruiker voorkomt in de database en zo ja, of het wachtwoord overeenkomt.
9. Maak vervolgens in je node.js webserver nog een nieuwe route en view om je formulier voor het aanmaken van een nieuw account te tonen
10. Geef ook dit formulier een geschikte action (door jou te kiezen URL) en method (POST).
11. Maak in je webserver een nieuwe route aan om de POST request op deze URL te kunnen afhandelen
12. Voeg code toe aan deze route om de ontvangen gebruikersgegevens op te slaan in de database en een bevestigingspagina te tonen
13. Kijk op dit moment eens zelf in database door in te loggen op MongoDB of via hun GUI. Staat de nieuwe gebruiker er tussen en kloppen alle gegevens?
14. Kijk tenslotte of je nu het inlogformulier kunt gebruiken om in te loggen als je nieuwe gebruiker


## Instructie feedbacksessie

De docent legt uit wat er als voorbereiding op de feedbacksessie van je wordt verwacht.

## Backend verdieping

pt-les-3-2-backend.md
