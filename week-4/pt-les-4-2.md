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
## Progressive enhancement / graceful degredation
(eigen onderzoek)
## Coding standards
### Clean code
https://github.com/ryanmcdermott/clean-code-javascript

### ES6
* Var, let & const
* arrow functions
* to puntkomma or not to puntkomma

### Linters
