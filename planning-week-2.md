# Week 2

## Les 2.1 Backend basis
In deze les leren we meer over de techniek die komt kijken bij het opzetten van een dynamisch web-project: hoe werkt precies HTTP, hoe kun je de command line gebruiken voor geavanceerde instructies en wat is het verschil tussen een site met functionaliteit in de frontend en één met functionaliteit in de backend? Ook leren we meer over Node.js en NPM.

Na al deze theorie is het ook tijd een begin te maken met het eindproduct. Je brainstormt over het concept voor de matching-app die je wilt bouwen en documenteert dit in je wiki.

### Command line
Take a couple of hours to understand the basics of the Terminal. Troughout the course we'll be doing a ton with the terminal so it's good to understand how to navigate it. 

*Windows:*  
Modern Windows versions provide Windows PowerShell as a command line interface. Just type 'PowerShell' in the searchbar in your start-menu or taskbar. By default you will start the Powershell as a normal user, but you can also choose to run it as an adminstrator. For everyday use, we recommend to run it as a normal user. You will have less rights to change things, which also means less risk of accidentally breaking things. For the few times you do need more permissions, you can run Powershell as an administrator. On older Windows machines you can also use the Command Prompt, which is less sophisticated. 

The default security settings for PowerShell prevent you from running any scripts without permission. You may run into this problem later on, for example when you try to start nodemon and it doesn't work. You can check your current settings in PowerShell with the command:
```sh
Get-ExecutionPolicy -List
```
and if needed, relax the security settings a bit using the command:
```sh
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

*MacOS:*  
Apple already has a terminal emulator by default to provide a command line interface. Just search for `terminal` in **spotlight** or find it in your applications folder. There are other command-line interfaces out there you can download that add more features. [Hyper](https://hyper.is/) and [iTerm](https://iterm2.com/) are very popular choices.

> 💡 If you have a Mac running MacOS Catalina (or above) the current default shell is `zsh`, previously this was `bash`. If `bash` is still the default on your machine we highly suggest you switch your default shell to `zsh` [using this Apple support article](https://support.apple.com/en-us/HT208050).

Many people also like to use the [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal) directly in your code editor like in VSCode.

1. Follow [A Designer’s Guide to the Terminal](https://react.design/terminal) *(Mac)* or read [Working with files and folders](https://learn.microsoft.com/en-us/powershell/scripting/samples/working-with-files-and-folders?view=powershell-7.3) *(Windows)*
2. Watch the [Command Line Basics video](https://www.youtube.com/watch?v=DP218aBHm1Q) of Wes Bos his CLI course *(Mac)* or [Powershell for Beginners](https://www.youtube.com/watch?v=Jfvg3CS1X3A) *(Windows)*

Toevoegen: hidden files (.dotfiles) en sudo



beetje oefenen, ga naar een directory, maak een file, copieer een file, verwijder het etc.

### Node.js en NPM
[🎦 _Watch a video_ about the browser versus Node.js.](https://www.youtube.com/watch?v=ZpiHUOM_Y-0)
[🎦 _Watch a video_ about NPM.](https://www.youtube.com/watch?v=X8D5Ijpp824)
Watch a live demo about [NPM and packages](https://www.youtube.com/watch?v=shSB9BbK1gU).

Installeer zelf node.js (incl npm)
Zelf modules zoeken op npm registry https://www.npmjs.com/

Improve the developer experience of your application. Look for so called 'developer dependencies' on NPM. nodemon https://nodemon.io/ is a good example, it will monitor for any changes in your source and automatically restart your server. Perfect for development.

### Opstarten API
Voor dit project stellen wij een API beschikbaar. Met deze API kun je data lezen uit een database of opslaan in die database, zonder je zorgen te hoeven maken over de achterliggende techniek. 
* Als je kiest voor de front-end specialisatie, kun je deze API vanuit je code in de browser aanroepen om dynamisch data op te halen of op te slaan.
* Als je kiest voor de back-end specialisatie, vervang je uiteindelijk deze API door een zelfgeschreven backend.

In beide gevallen is het aan de praat krijgen van de API een mooie oefening om de basis van Node.js en NPM onder de knie te krijgen. 

Stap voor stap instructies toevoegen.

### Concept
Think about what feature you are going to work on for the individual part of this project. 

1. Write ~5 [Job Stories](https://jtbd.info/replacing-the-user-story-with-the-job-story-af7cdee10c27) (to generate ideas) and pick one to continue working on.
2. 'Split up' your Job Story into concrete requirements (taks) by making a [requirements list](https://cmdmethods.nl/cards/stepping-stones/requirements-list)
3. Think about your target audience. It always helps to have one core audience you will be designing for. For example; sport fanatics to match people based on sports, netflixers to match people based on what series they want to watch etc. Do some research about your audience and add it to your wiki: what do you know about these people, what are their wishes and challenges? Can you find more information about them online? Can you talk to a few members of your target audience to ask them what they think is important?
4. Think about your concept. Again, do some research and add it to your wiki. What are existing similar concepts that are already out there? Look into a few. What do they do really well that you can learn from, and where do you feel you really can do better than them?
5. Create a small [wireframe (napkin quality)](https://cmdmethods.nl/cards/stepping-stones/design-specification) to roughly sketch out how your interface should look.

Document all this research things in your wiki. Teachers will give feedback on your concept in the next lesson. Remember we are not a UCD or NPD course but thinking about your concept for a bit will help you get clear on what you are going to build. So don't make full design documents, writing them down in your wiki is enough.



## Les 2.2 Frontend basis

## Les 2.3 Verdieping
### A. Verdieping Frontend

### B. Verdieping Backend

## Les 2.4 Q&A lesstof
