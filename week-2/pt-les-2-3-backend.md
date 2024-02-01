# Les 2.3 Verdieping Backend
## Express
Oefening:
We'll install Express and create a very basic server that responds to our requests. 

1. Install `express` and require it in `server.js`
2. Use _http_ methods to have your server respond with _hello world_ when you open `localhost`. Use the resource below as an example of how to do this.

**Ask yourself upon completion:**
* The server you just wrote? Where does it live? What happens if you turn off your computer?
* What's `localhost` and how does it defer from a full domain?

**Additional resources**
* [Hello World](https://expressjs.com/en/starter/hello-world.html)

1. **Push your changes:**  
Commit your progess in your repository on GitHub under your username in your own matching-app repository.  

## Routes en static
Breid je app uit met static content (image en stylesheet) en meerdere routes
Push je changes

Before you start you'll probably want to read a bit about **express,** **routing,** and **templating**. We'll cover this in the lecture but make sure you fully understand these concept, the resources below can help.

* [_Introducing Express on MDN_][intro-express]
* [_Express Routing guide_][intro-routing]
* [_Using template engines with Express_][intro-templating]

[🎦 _Watch a video_ about routing and express.][videoexpress]  
[🎦 _Watch a video_ about request and response.][videorequest]

You can do these exercises before you start working on the assignments to get comfortable with the topics covered in class. The below are interactive self guided lesson modules from [freeCodeCamp](https://www.freecodecamp.org). If you feel a bit more adventurous you can try the [NodeSchool workshoppers](https://nodeschool.io).

* [freeCodeCamp - Basic Node and Express (exercises)](https://www.freecodecamp.org/learn/back-end-development-and-apis/#basic-node-and-express)
* [Express.js (workshopper)][workshopper]

We'll add more features to our server. It should handle routes and serve static files. Make sure it does (atleast) the following three things:

1. **Basic routing:** Have a couple of different `routes` (e.g. `/about` `/login`) that are useful for your matching-application.
2. **Error handling:** Respond with a `404 Not Found` if you go to a route that doesn't exist.
3. **Serve `static files`:** such CSS but also media files such as images, video's or audio files.

**Ask yourself upon completion:**
* How does the `app instance` work? What makes it possible you can do things like `app.get` or `app.listen`?
* What are the `req` and `res` parameters?

**Additional resources**
* [Basic Routing](https://expressjs.com/en/starter/basic-routing.html)
* [Static Files](https://expressjs.com/en/starter/static-files.html)

## Templating engine
Gebruik de templating engine om voor een route een view te renderen.
Push je changes
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
