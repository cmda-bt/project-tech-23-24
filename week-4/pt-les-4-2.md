# Les 4.2 Frontend optimalisatie
## Git(Hub) voor teams
Git en GitHub bevatten diverse features om een team te helpen samen te werken aan een project. Je wilt liever niet dat alle teamleden tegelijkertijd in dezelfde code werken, want dan zit je elkaar snel in de weg. In plaats daarvan kun je werken in een *branch*, een aparte kopie van de code, waarin je ongestoord aan je feature kunt werken. Zodra de feature gereed is, kan de branch weer worden ge*merge*d (samengevoegd) met de main branch midddels een zogenaamd *Pull Request*.

* 🎦 Bekijk een video over [de GitHub flow en branches](https://www.youtube.com/watch?v=7-q9B6HRbEQ)
* Maak de interactieve oefening over [Reviewing Pull Requests](https://github.com/skills/review-pull-requests) op GitHub Skills
* Maak de interactieve oefening over [Managing Merge Conflicts](https://github.com/skills/resolve-merge-conflicts) op GitHub Skills
* 🎦 Bekijk een video over [Branch protection](https://www.youtube.com/watch?v=rY6IxlkKF30)

Daarnaast heeft GitHub nog meer features die je team kunnen helpen het werk te organiseren:
* 🎦 Bekijk een video over [Projects en Issues](https://www.youtube.com/watch?v=L9e3_YDqNN8)
* 🎦 Bekijk een video over [Samenwerken op GitHub](https://www.youtube.com/watch?v=S4LRwbNjLWY)

Tenslotte is het een goed moment om eens stil te staan bij de vraag hoe je de code voor je hele project logisch en overzichtelijk in een folderstructuur gaat organiseren. Waar komt de front-end code en waar komt de back-end code?
* Het kan handig zijn je node.js webserver een naam te geven die duidelijk maakt dat dit de backend-server is. Iets als server.js kan een goede keuze zijn, app.js zie je ook wel eens. Noem je je server index.js, dan is het makkelijk te verwarren met front-end code die in de browser zou moeten draaien.
* Plaatjes, stylesheets maar ook front-end JavaScript die in de browser moet draaien, kan een plek vinden in je folder met static content
* Statische HTML pagina's die door de front-enders worden gemaakt, kunnen ook worden neergezet in de folder met static content. Maar nog mooier is het de statische pagina's dynamisch te maken door de aangeleverde HTML om te bouwen naar een EJS view in deze dan als een .ejs bestand in de folder met je views te plaatsen.


## Responsive
## Progressive enhancement / graceful degradation
(eigen onderzoek)
## Coding standards
### Clean code
https://github.com/ryanmcdermott/clean-code-javascript

### ES6
* Var, let & const
* arrow functions
* to puntkomma or not to puntkomma

### Linters
Er bestaan allerlei tools die je kunnen helpen 'nette' code te schrijven. Je hebt misschien al gewerkt met een *formatter* als Prettier, die helpt code netjes te formatteren. Met een *linter* kun je nog een stap verder gaan, deze controleert je code ook op inhoudelijke fouten. Er bestaan verschillende Linters. Tijdens dit project gaan we oefenen met **ESLint**.

**Opdracht: ESLint**

1. Denk eerst na over de coding standards die je wilt gebruiken. Tijdens het installeren moet je hierover namelijk een aantal vragen beantwoorden. Het is later altijd nog mogelijk je keuzes te wijzigen.
2. Installeer ESLint in de folder van je project volgens de instructies op [Getting Started with ESLint](https://eslint.org/docs/latest/use/getting-started) en beantwoord zorgvuldig de vragen over je gewenste configuratie.
3. Als alles goed is gegaan, heeft ESLint in de folder van je project een configuratiefile gemaakt met de naam ```.eslintrc.*``` Afhankelijk van je keuze is dit een JavaScript, JSON, of YAML bestand. Als je later je keuzes nog wilt aanpassen, kun je wijzigingen aanbrengen in dit bestand of nog een keer opnieuw de configuratie doorlopen
4. Je kunt ervoor kiezen om je  ```.eslintrc.*``` configuratiefile toe te voegen aan je ```.gitignore```, want feitelijk is dit geen onderdeel van de code van je project. Maar als je als team samenwerkt, kun je er ook voor kiezen de configuratie juist wel aan je repository toe te voegen, want dan werken jullie allemaal volgens dezelfde standaard
5. Als je configuratie voltooid is, gebruik dan ESLint om je eigen JavaScript code te *linten*. Volg ook hiervoor de instructies op Getting Started with ESLint.
6. Je kunt ESLint ook als extensie toevoegen in VSCode. Je ziet dan direct alle problemen in je editor en hoeft niet apart ESLint te gebruiken vanuit je Terminal. Let er op dat deze extensie alleen werkt voor je project, als je eerst binnen dat project ESLint hebt geinstalleerd en geconfigureerd volgens bovenstaande stappen.

Pro-tip: je hebt gemerkt dat je tijdens de configuratie van ESLint hebt moeten aangeven of je code draait op Node.js (en dan waarschijnlijk ```require``` gebruikt om modules in te laden) of in de browser (met ```import``` statements). Je kunt in aparte mappen van je project ook verschillende ```.eslintrc.*``` configuratiebestanden maken. In het ene mapje maak je dan regels om je frontend code te checken, en in een ander mapje kun je regels plaatsen voor je back-end code.
