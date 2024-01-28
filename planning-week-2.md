# Week 2

## Les 2.1 Backend basis
In deze les leren we meer over de techniek die komt kijken bij het opzetten van een dynamisch web-project: hoe werkt precies HTTP, hoe kun je de command line gebruiken voor geavanceerde instructies en wat is het verschil tussen een site met functionaliteit in de frontend en één met functionaliteit in de backend? Ook leren we meer over Node.js en NPM.

Na al deze theorie is het ook tijd een begin te maken met het eindproduct. Je brainstormt over het concept voor de matching-app die je wilt bouwen en documenteert dit in je wiki.

### Command line
Gedurende dit blok zullen we regelmatig gebruik maken van de Terminal. Neem een moment om deze op je computer gereed te maken en de basis te leren.

*Windows:*  
Nieuwe versies van Windows gebruiken PowerShell als command line interface. Type 'PowerShell' in de zoekbalk van je start-menu of taakbalk. Je start PowerShell standaard als gewone gebruiker, maar je kunt er ook voor kiezen het te starten als administrator. Normaal gesproken is het verstandig PowerShell uit te voeren als gewone gebruiker. Je hebt dan iets minder rechten, maar ook minder kans per ongeluk dingen kaport te maken.

Standaard heeft PowerShell een aantal beveiligingsinstellingen, waarbij het bijvoorbeeld niet mogelijk is scripts te runnen zonder permissie. Dit kan later in dit blok een probleem worden, als je bijvoorbeeld nodemon wilt starten en het werkt niet. Je kunt je huidige instellingen controleren in PowerShell met het commando: 
```sh
Get-ExecutionPolicy -List
```
en deze eventueel iets versoepelen met het commando:
```sh
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

*MacOS:*  
Apple heeft ook een ingebouwde command line interface. Zoek naar `terminal` met **spotlight** of kijk in je applications folder. Ook op Mac voer je in de Terminals standaard commando's uit met de rechten van een gewone gebruiker. De meeste dingen kun je hiermee doen, met minder risico belangrijke zaken kapot te maken. Voor sommige instellingen of het installeren van software heb je soms administrator rechten nodig. Je kunt dan `sudo` voor een commando zetten. Stel dat je geen toegang hebt tot een bepaalde directory, en `ls` geeft daarom een foutmelding, dan zou `sudo ls` wel kunnen werken.

> 💡 Op Macs met MacOS Catalina (of nieuwer) is de standaard shell `zsh`, daarvoor was het `bash`. Als je `bash` hebt als standaard instelling, raden we aan dat aan te passen volgens de instructie in dit [Apple support article](https://support.apple.com/en-us/HT208050).

Veel mensen vinden het ook fijn de [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal) direct vanuit VSCode te gebruiken.

Opdracht:
* Voor Windows gebruikers: Lees [Working with files and folders](https://learn.microsoft.com/en-us/powershell/scripting/samples/working-with-files-and-folders?view=powershell-7.3) en kijk de video: [Powershell for Beginners](https://www.youtube.com/watch?v=Jfvg3CS1X3A)
* Voor Mac gebruikers: volg [A Designer’s Guide to the Terminal](https://react.design/terminal) en kijk de video: [Command Line Basics video](https://www.youtube.com/watch?v=DP218aBHm1Q) van CLI cursus door Wes Bos

Oefening: maak de volgende opdrachten om de basis van de command line onder de knie te krijgen
* Zoek de folder met je documenten voor Project Tech in je verkenner of finder. Open nu een terminal venster en zoek daar dezelfde folder op. Tip: gebruik `cd` en `pwd`
* Vraag een lijst op van de bestanden in deze folder. Tip: gebruik `ls`
* Maak een kopie van een van deze bestanden.
* Maak in de folder een nieuwe lege directory aan
* Verplaats de kopie die je net gemaakt had, naar de nieuwe directory
* Verwijder de nieuwe directory inclusief het gekopieerde bestand
* Kijk of je in de folder van je project zogenaamde `dotfiles` kunt vinden. Dit zijn bestanden of folders waarvan de filenaam begint met een . (punt), zoals bijvoorbeeld `.gitignore`, `.DS_Store`, `.git` of `.env`. Dit zijn bestanden met systeeminstellingen, die standaard verborgen zijn (niet getoond worden). Op de Mac kun je ze laten zien met het commando `ls -a` en op Windows met `ls -hidden`. Op Windows is het ook handig in de verkenner onder het menu Weergeven de verborgen items aan te vinken.

### Node.js en NPM
Bekijk onderstaande video's:
* [De browser versus Node.js](https://www.youtube.com/watch?v=ZpiHUOM_Y-0)
* [NPM](https://www.youtube.com/watch?v=X8D5Ijpp824)
* [Live demo NPM en packages](https://www.youtube.com/watch?v=shSB9BbK1gU).

Installeer nu op je eigen computer Node (inclusief NPM)

#### Node - installeren op Mac

Open je **terminal**, en installeer [nvm](https://github.com/creationix/nvm) als volgt:

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

Controleer of `nvm` goed is geinstalleerd:
```sh
nvm --version # Should print a version number
```

> Zie je de foutmelding `nvm command not found`? Dan is NVM niet goed geïnstalleerd. Lees  [troubleshouting section on nvm](https://github.com/nvm-sh/nvm#troubleshooting-on-macos) zorgvuldig om dit op te lossen. 

**Sluit je terminal af en start deze opnieuw**. Type vervolgens:

```sh
nvm install stable
```

Node en NPM zijn nu geïnstalleerd. Check dit met:

```sh
node -v # Should print v18.12.1 (or a higher version)
npm -v # Something like 9.2.0 (or a higher version)
```

[🎦 Video over het intalleren van Node op MacOS](https://www.youtube.com/watch?v=EQWyWQhphGw)

> Als je in plaats van bovenstaande instructies gebruik maakt van de Node [installer](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm), kun je geconfronteerd worden met een [`eaccess`](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally) probleem. Om die reden raden wij bovenstaande werkwijze met nvm aan. De node installer installeert npm in een directory met local permissions, wat problemen zal geven als je npm packages global wilt gebruiken.

#### Node - installaren op Windows
Er is geen NVM voor Windows. We gaan daarom naar de [node.js website](https://nodejs.org/) om node.js voor Windows te downloaden en installeren. Kies de LTS (Long-Term Support) versie, dit is de nieuwste stabiele versie. 

Node en npm zijn nu geinstalleerd. Dit kun je als volgt in PowerShell controleren:

```sh
node -v # Should print 18.13.0 (or a higher version)
npm -v # Something like 8.19.0 (or a higher version)
```

### Node modules
Kijk eens rond op de [npm registry](https://www.npmjs.com/) of je packages kunt vinden, die handig zouden kunnen zijn voor je (backend) project. Daarnaast kun je kijken of je handige 'developer dependencies' op NPM kunt vinden, die straks je leven als developer makkelijk kunnen maken. Een goed voorbeeld is [nodemon](https://nodemon.io/), die automatisch je server herstart als je je code hebt aangepast. Super handig, dus dit is een goed moment om die vast te installeren.

### Installeren en uitproberen API
Voor dit project stellen wij een API beschikbaar. Met deze API kun je data lezen uit een database of opslaan in die database, zonder je zorgen te hoeven maken over de achterliggende techniek. 
* Als je kiest voor de front-end specialisatie, kun je deze API vanuit je code in de browser aanroepen om dynamisch data op te halen of op te slaan.
* Als je kiest voor de back-end specialisatie, vervang je uiteindelijk deze API door een zelfgeschreven backend.

In beide gevallen is het aan de praat krijgen van de API een mooie oefening om de basis van Node.js en NPM onder de knie te krijgen. 

Je kunt onze [API vinden op GitHub](https://github.com/ivo-online/database_api). Volg daar de instructies in de README.md om een kopie te maken van deze API op je eigen computer. Je moet hierbij een aantal persoonlijke toegangsgegevens invullen in een eigen .env file. De benodigde waardes krijg je van je docenten.

Zodra je de API succesvol hebt draaien in je terminal, kun je proberen een aantal HTTP requests naar de API te sturen om te kijken wat er gebeurd. De mogelijke requests zijn gedocumenteerd in de [README.md](https://github.com/ivo-online/database_api/blob/main/README.md) van de API. 

Vanuit frontend JavaScript code, die draait in de browser, kun je straks gebruik maken van [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) om requests naar de API te sturen. Om, zonder te coderen, al vast een beetje gevoel te krijgen hoe de API werkt, kun je ook handmatig HTTP requests sturen naar de API en de responses zien met een geschikte browser plugin zoals [Tabbed PostMan](https://chromewebstore.google.com/detail/tabbed-postman-rest-clien/coohjcphdfgbiolnekdpbcijmhambjff) voor Chrome.

Oefening: stuur HTTP requests naar de API om het volgende te doen:
* Vul je database met testdata
* Vraag een overzicht op van alle zojuist aangemaakte testdata
* Vraag 1 specifiek object op uit de aangemaakte testdata, bijvoorbeeld iemand met een bepaald beroep.
* Update een object uit de testdata, bijvoorbeeld door een beroep te veranderen in een ander beroep.

### Concept
Denk na over de matching site die je wilt gaan bouwen en uit welke afzonderlijke onderdelen deze kan bestaan.

1. Denk na over een concept voor de matching site. Wie ga je matchen met wie of wat? Kun je een creatieve manier bedenken, om matches tot stand te brengen? Brainstorm over een aantal mogelijkheden. Door welke bestaande concepten kun je je laten inspireren? Documenteer je onderzoek op je wiki en kies vervolgens een concept uit om verder uit te werken.
2. Denk na over je doelgroep. Wat zijn dit voor mensen, wat vinden ze leuk en wat voor functionaliteit verwachten ze? Wat zijn hun wensen en uitdagingen? Misschien kun je een aantal mensen interviewen of online informatie vinden over deze groep. Documenteer je onderzoek wederom op de wiki.
3. Beschrijf op je wiki een aantal (ongeveer 5) [Job Stories](https://jtbd.info/replacing-the-user-story-with-the-job-story-af7cdee10c27) op om ideeën te genereren over de functionaliteit die nodig is op je matching site. Maak uit de gevonden job stories een keuze voor een functionaliteit die jij verder uit gaat werken.
4. Werk de gekozen job story op je wiki verder uit door hier een [requirements list](https://cmdmethods.nl/cards/stepping-stones/requirements-list) voor op te stellen.
5. Schets ten slotte één of meer lo-fi [wireframes](https://cmdmethods.nl/cards/stepping-stones/design-specification) om een idee te krijgen van het gebruikers interface.

Leg al het bovenstaande vast op je wiki, zodat we je hier ook feedback op kunnen geven. De focus van dit project is Tech, dus het is niet nodig een volledig design uit te werken. Voor nu is het vooral belangrijk om meer duidelijkheid te krijgen over wat je de komende weken gaat maken.

## Les 2.2 Frontend basis

## Les 2.3 Verdieping
### A. Verdieping Frontend

### B. Verdieping Backend

## Les 2.4 Q&A lesstof
