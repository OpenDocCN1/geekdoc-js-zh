![](Images/default_cover.jpeg)

![](Images/default_cover.jpeg)

## Vue.js: 11 Practical Projects

Copyright © 2019 SitePoint Pty. Ltd.

Ebook ISBN: 978-1-925836-27-1

*   **Cover Design:** Alex Walker
*   **Project Editor:** James Hibbard

## Notice of Rights

All rights reserved. No part of this book may be reproduced, stored in a retrieval system or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical articles or reviews.

## Notice of Liability

The author and publisher have made every effort to ensure the accuracy of the information herein. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors and SitePoint Pty. Ltd., nor its dealers or distributors will be held liable for any damages to be caused either directly or indirectly by the instructions contained in this book, or by the software or hardware products described herein.

## Trademark Notice

Rather than indicating every occurrence of a trademarked name as such, this book uses the names only in an editorial fashion and to the benefit of the trademark owner with no intention of infringement of the trademark.

![SitePoint logo](Images/sitepoint-logo-2012.png)
Published by SitePoint Pty. Ltd.

48 Cambridge Street Collingwood
VIC Australia 3066
Web: www.sitepoint.com
Email: books@sitepoint.com

## About SitePoint

SitePoint specializes in publishing fun, practical, and easy-to-understand content for web professionals. Visit [http://www.sitepoint.com/](http://www.sitepoint.com/) to access our blogs, books, newsletters, articles, and community forums. You’ll find a stack of information on JavaScript, PHP, design, and more.

# Preface

Since its release in 2014, Vue.js has seen a meteoric rise to popularity and is is now considered one of the primary front-end frameworks, and not without good reason. Its component-based architecture was designed to be flexible and easy to adopt, making it just as easy to integrate into projects and use alongside non-Vue code as it is to build complex client-side applications.

This book contains a selection of 11 practical projects covering different aspects of working with Vue. It contains:

1.  *Build a Basic CRUD App with Vue.js, Node and MongoDB* by James Hibbard
2.  *Creating Beautiful Charts Using Vue.js Wrappers for Chart.js* by Yomi Eluwande
3.  *Build a Real-time Chat App with Pusher and Vue.js* by Michael Wanyoike
4.  *Building a Vue Front End for a Headless CMS* by Michael Wanyoike
5.  *How to Build a Chrome Extension with Vue* by James Hibbard
6.  *Build Your Own Link-sharing Site with Nuxt.js and vue-kindergarten* by Nilson Jacques
7.  *An Introduction to Data Visualization with Vue and D3.js* by Christopher Vundi
8.  *How to Build a Reusable Component with Vue* by Deji Atoyebi
9.  *How to Build a Game with Vue.js* by Ivaylo Gerchev
10.  *Build a Shopping List App with Vue, Vuex and Bootstrap Vue* by Michael Wanyoike
11.  *How to Develop and Test Vue Components with Storybook* by Ivaylo Gerchev

## Who Should Read This Book?

This book is for developers with experience of JavaScript.

## Conventions Used

### Code Samples

Code in this book is displayed using a fixed-width font, like so:

```
 <h1>A Perfect Summer's Day</h1>
<p>It was a lovely day for a walk in the park.
The birds were singing and the kids were all back at school.</p> 
```

Where existing code is required for context, rather than repeat all of it, ⋮ will be displayed:

```
 function animate() {
    ⋮
new_variable = "Hello";
}
```

Some lines of code should be entered on one line, but we’ve had to wrap them because of page constraints. An ➥ indicates a line break that exists for formatting purposes only, and should be ignored:

```
 URL.open("http://www.sitepoint.com/responsive-web-
➥design-real-user-testing/?responsive1");
```

You’ll notice that we’ve used certain layout styles throughout this book to signify different types of information. Look out for the following items.

### Tips, Notes, and Warnings

#### Hey, You!

Tips provide helpful little pointers.

#### Ahem, Excuse Me ...

Notes are useful asides that are related—but not critical—to the topic at hand. Think of them as extra tidbits of information.

#### Make Sure You Always ...

... pay attention to these important points.

#### Watch Out!

Warnings highlight any gotchas that are likely to trip you up along the way.

# Chapter 1: Build a Basic CRUD App with Vue.js, Node and MongoDB

### by James Hibbard

Most web applications need to persist data in one form or other. When working with a server-side language, this is normally a straightforward task. However, when you add a front-end JavaScript framework to the mix, things start to get a bit trickier.

In this tutorial, I’m going to show you how to build a simple [CRUD app](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) (Create, Read, Update and Delete) using Node, MongoDB and Vue. I’ll walk you through getting all of the pieces set up and demo each of the CRUD operations. After reading, you’ll be left with a fully functional app that you can adapt to your own purposes. You’ll also able to use this approach in projects of your own.

As the world really doesn’t need another to-do list, we’ll be building an app to help students of a foreign language learn vocabulary. As you might notice from my author bio, I’m a Brit living in Germany and this is something I wish I’d had 20 years ago.

You can check out the finished product in [this GitHub repo](https://github.com/sitepoint-editors/vocab-builder). And if you’re stuck for German words at any point, [try out some of these](https://bilingua.io/short-and-easy-german-words).

## Install the Tooling

In this section, we’ll install the tools we’ll need to create our app. These are Node, npm, MongoDB, MongoDB Compass (optional) and Postman. I won’t go too into depth on the various installation instructions, but if you have any trouble getting set up, please [visit our forums](https://www.sitepoint.com/community/) and ask for help there.

### Node.js

Many websites will recommend that you head to [the official Node download page](https://nodejs.org/en/download/) and grab the Node binaries for your system. While that works, I’d suggest using a version manager (such as [nvm](https://github.com/creationix/nvm)) instead. This is a program which allows you to install multiple versions of Node and switch between them at will. If you’d like to find out more about this, please consult our quick tip, [Install Multiple Versions of Node.js Using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

### npm

npm is a JavaScript package manager which comes bundled with Node, so no extra installation is necessary here. We’ll be making quite extensive use of npm throughout this tutorial, so if you’re in need of a refresher, please consult [A Beginner’s Guide to npm — the Node Package Manager](https://www.sitepoint.com/beginners-guide-node-package-manager/).

### MongoDB

MongoDB is a document database which stores data in flexible, JSON-like documents.

The quickest way to get up and running with Mongo is to use a service such as mLabs. They have a free sandbox plan which provides a single database with 496MB of storage running on a shared virtual machine. This is more than adequate for a simple app with a handful of users. If this sounds like the best option for you, please consult their [quick start guide](http://docs.mlab.com/).

You can also install Mongo locally. To do this, please visit the [official download page](https://www.mongodb.com/download-center#community) and download the correct version of the community server for your operating system. There’s a link to detailed, OS-specific installation instructions next to the download link.

### A MongoDB GUI

Although not strictly necessary for following along with this tutorial, you might also like to install [Compass, the official GUI for MongoDB](https://www.mongodb.com/download-center#compass). This tool helps you visualize and manipulate your data, allowing you to interact with documents with full CRUD functionality.

At the time of writing, you’ll need to fill out your details to download Compass, but you won’t need to create an account.

### Postman

This is an extremely useful tool for working with and testing APIs. You can download the correct version for your OS from the [project’s home page](https://www.getpostman.com/). You can find OS-specific installation instructions [here](https://learning.getpostman.com/docs/postman/launching_postman/installation_and_updates/).

### Check That Everything Is Installed Correctly

To check that Node and npm are installed correctly, open your terminal and type this:

```
node -v
```

Follow that with this:

```
npm -v
```

This will output the version number of each program (`11.1.0` and `6.4.1` respectively at the time of writing).

If you installed Mongo locally, you can check the version number using this:

```
mongo --version
```

This should output a bunch of information, including the version number (`4.0.4` at the time of writing).

### Check the Database Connection Using Compass

If you have installed Mongo locally, you start the server by typing the following command into a terminal:

```
mongod
```

Next, open Compass. You should be able to accept the defaults (Hostname: `localhost`, Port: 27017), press the *CONNECT* button, and establish a connection to the database server.

![MongoDB Compass connected to localhost:27107](Images/compass-local.jpg) 

Note that the databases `admin`, `config` and `local` are created automatically.

#### Using a Cloud-hosted Solution

If you’re using mLabs, create a database subscription (as described in their [quick-start guide](http://docs.mlab.com/)), then copy the connection details to the clipboard. This should be in the following form:

```
mongodb://<dbuser>:<dbpassword>@<instance>.mlab.com:<port>/<dbname>
```

When you open Compass, it will inform you that it has detected a MongoDB connection string and asks if you’d like to use it to fill out the form. Click *Yes*, then click *CONNECT* and you should be off to the races.

![MongoDB Compass connected to mLabs](Images/compass-mlabs.jpg) 

Note that I called my database `node-vue-crud-app`. You can call yours what you like.

## Creating the Node Back End

In this section, we’ll create a RESTful API for our Vue front end to consume and test it using Postman. I don’t want to go into too much detail on how a RESTful API works, as the focus of this guide should be the Vue front end. If you’d like a more in-depth tutorial, there are plenty on the Internet. I found that [Build Node.js RESTful APIs in 10 Minutes](https://www.codementor.io/olatundegaruba/nodejs-restful-apis-in-10-minutes-q0sgsfhbd) was quite easy to follow, and it served as inspiration for the code in this section.

### Basic Setup

First, let’s create the files and directories we’ll need and initialize the project:

```
mkdir -p vocab-builder/server/api/{controllers,models,routes}
cd vocab-builder/server
touch server.js
touch api/controllers/vocabController.js
touch api/models/vocabModel.js
touch api/routes/vocabRoutes.js
npm init -y
```

This should give us the following folder structure:

```
.
└── server
    ├── api
    │   ├── controllers
    │   │   └── vocabController.js
    │   ├── models
    │   │   └── vocabModel.js
    │   └── routes
    │       └── vocabRoutes.js
    ├── package.json
    └── server.js
```

### Install the Dependencies

For our API, we’ll be using the following libraries:

*   [express](https://www.npmjs.com/package/express)—a small framework for Node that provides many useful features, such as routing and middleware.
*   [cors](https://www.npmjs.com/package/cors)—Express middleware that can be used to enable [CORS](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing) in our project.
*   [body-parser](https://www.npmjs.com/package/body-parser)—Express middleware to parse the body of incoming requests.
*   [mongoose](https://www.npmjs.com/package/mongoose)—a MongoDB ODM (the NoSQL equivalent of an ORM) for Node. It provides a simple validation and query API to help you interact with your MongoDB database.
*   [nodemon](https://www.npmjs.com/package/nodemon)—a simple monitor script which will automatically restart a Node application when file changes are detected.

Let’s get them installed:

```
npm i express cors body-parser mongoose
npm i nodemon --save-dev
```

Next, open up `package.json` and alter the `scripts` section to read as follows:

```
"scripts": {
  "start": "nodemon server.js"
},
```

And that’s the setup done.

### Create the Server

Open up `server.js` and add the following code:

```
const express = require('express');
const port = process.env.PORT || 3000;
const app = express();

app.listen(port);

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

console.log(`Server started on port ${port}`);
```

Then hop into the terminal and run `npm run start`. You should see a message that the server has started on port 3000\. If you visit [http://localhost:3000/](http://localhost:3000/), you should see “Hello, World!” displayed.

### Define a Schema

Next, we need to define what the data should look like in our database. Essentially I wish to have two fields per document, `english` and `german`, to hold the English and German translations of a word. I’d also like to apply some simple validation and ensure that neither of these fields can be empty.

Open up `api/models/vocabModel.js` and add the following code:

```
const mongoose = require('mongoose');

const { Schema } = mongoose;

const VocabSchema = new Schema(
  {
    english: {
      type: String,
      required: 'English word cannot be blank'
    },
    german: {
      type: String,
      required: 'German word cannot be blank'
    }
  },
  { collection: 'vocab' }
);

module.exports = mongoose.model('Vocab', VocabSchema);
```

Note that I’m also specifying the name of the collection I wish to create, as otherwise Mongoose will attempt to name it “vocabs”, which is silly.

### Setting Up the Routes

Next we have to specify how our API should respond to requests from the outside world. We’re going to create the following endpoints:

*   GET `/words`—return a list of all words
*   POST `/words`—create a new word
*   GET `/words/:wordId`—get a single word
*   PUT `/words/:wordId`—update a single word
*   DELETE `/words/:wordId`—delete a single word

To do this, open up `api/routes/vocabRoutes.js` and add the following:

```
const vocabBuilder = require('../controllers/vocabController');

module.exports = app => {
  app
    .route('/words')
    .get(vocabBuilder.list_all_words)
    .post(vocabBuilder.create_a_word);

  app
    .route('/words/:wordId')
    .get(vocabBuilder.read_a_word)
    .put(vocabBuilder.update_a_word)
    .delete(vocabBuilder.delete_a_word);
};
```

You’ll notice that we’re requiring the `vocabController` at the top of the file. This will contain the actual logic to handle the requests. Let’s implement that now.

### Creating the Controller

Open up `api/controllers/vocabController.js` and add the following code:

```
const mongoose = require('mongoose');
const Vocab = mongoose.model('Vocab');

exports.list_all_words = (req, res) => {
  Vocab.find({}, (err, words) => {
    if (err) res.send(err);
    res.json(words);
  });
};

exports.create_a_word = (req, res) => {
  const newWord = new Vocab(req.body);
  newWord.save((err, word) => {
    if (err) res.send(err);
    res.json(word);
  });
};

exports.read_a_word = (req, res) => {
  Vocab.findById(req.params.wordId, (err, word) => {
    if (err) res.send(err);
    res.json(word);
  });
};

exports.update_a_word = (req, res) => {
  Vocab.findOneAndUpdate(
    { _id: req.params.wordId },
    req.body,
    { new: true },
    (err, word) => {
      if (err) res.send(err);
      res.json(word);
    }
  );
};

exports.delete_a_word = (req, res) => {
  Vocab.deleteOne({ _id: req.params.wordId }, err => {
    if (err) res.send(err);
    res.json({
      message: 'Word successfully deleted',
     _id: req.params.wordId
    });
  });
};
```

Here we’re importing our model, then defining five functions corresponding to the desired CRUD functionality. If you’re unsure as to what any of these functions do or how they work, please consult the [Mongoose documentation](https://mongoosejs.com/docs/api.html).

### Wiring Everything Together

Now all of the pieces are in place and the time has come to wire them together. Hop back into `server.js` and replace the existing code with the following:

```
const express = require('express');
const cors = require('cors');
const mongoose = require('mongoose');
const bodyParser = require('body-parser');

global.Vocab = require('./api/models/vocabModel');
const routes = require('./api/routes/vocabRoutes');

mongoose.Promise = global.Promise;
mongoose.set('useFindAndModify', false);
mongoose.connect(
  'mongodb://localhost/vocab-builder',
  { useNewUrlParser: true }
);

const port = process.env.PORT || 3000;
const app = express();

app.use(cors());
app.use(bodyParser.urlencoded({ extended: true }));
app.use(bodyParser.json());

routes(app);
app.listen(port);

app.use((req, res) => {
  res.status(404).send({ url: `${req.originalUrl} not found` });
});

console.log(`Server started on port ${port}`);
```

Here we start off by requiring the necessary libraries, as well as our model and routes files. We then use Mongoose’s `connect` method to connect to our database (don’t forget to make sure MongoDB is running if you installed it locally), before creating a new Express app and telling it to use the `bodyParser` and `cors` middleware. We then tell it to use the routes we defined in `api/routes/vocabRoutes.js` and to listen for connections on port 3000\. Finally, we define a function to deal with nonexistent routes.

You can test this is working by hitting [http://localhost:3000/](http://localhost:3000/) in your browser. You should no longer see a “Hello, World!” message, but rather `{"url":"/ not found"}`.

Also, please note that if you’re using mLabs, you’ll need to replace:

```
mongoose.connect(
  'mongodb://localhost/vocab-builder',
  { useNewUrlParser: true }
);
```

with the details you received when creating your database:

```
mongoose.connect(
  'mongodb://<dbuser>:<dbpassword>@<instance>.mlab.com:<port>/<dbname>',
  { useNewUrlParser: true }
);
```

### Testing the API with Postman

To test the API, start up Postman. How you do this will depend on how you installed it.

#### Create

We’ll start off by creating a new word pair. Select *POST* as the method and enter `http://localhost:3000/words` as the URL. Select the *Body* tab and the radio button `x-www-form-urlencoded`, then enter two key/value pairs into the fields below. Press *Send* and you should receive the newly created object from the server by way of a response.

![Postman—a successful POST request](Images/postman-01.jpg) 

At this point, you can also view the database using Compass, to assure yourself that the collection was created with the correct entry.

#### Read

To test the read functionality of our API, we’ll first attempt to get all words in our collection, then an individual word.

To get all of the words, change the method to *GET* and *Body* to *none*. Then hit *Send*. The response should be similar to this:

```
[
  {
    "_id": "5bed3d46d311354a6ae48b2d",
    "english": "Dog",
    "german": "Hund",
    "__v": 0
  }
]
```

Copy the `_id` value of the first word returned and change the URL to `http://localhost:3000/words/<_id>`. For me this would be:

```
http://localhost:3000/words/5bed3d46d311354a6ae48b2d
```

Hit *Send* again to retrieve just that word from our API. The response should be similar to this:

```
{
  "_id": "5bed3d46d311354a6ae48b2d",
  "english": "Dog",
  "german": "Hund",
  "__v": 0
}
```

Notice that now just the object is returned, not an array of objects.

#### Update

Finally, let’s update a word, then delete it. To update the word, select PUT as the method and enter `http://localhost:3000/words/<word _id>` as the URL (where the ID of the word corresponds to `_id` as described above). Select the *Body* tab and the radio button `x-www-form-urlencoded`, then enter two key/value pairs into the fields below different than before. Press *Send* and you should receive the newly updated object from the server by way of a response:

```
{
  "_id": "5bed3d46d311354a6ae48b2d",
  "english": "Cat",
  "german": "Katze",
  "__v": 0
}
```

![Postman - a successful PUT request](Images/postman-02.jpg) 

#### Destroy

To delete a word, just change the method to *DELETE* and press *Send*. Zap! The word should be gone and your collection should be empty. You can test that this is indeed the case, either using Compass, or by selecting the original request to get all words from the left hand pane in Postman and firing that off again. This time it should return an empty array.

And that’s it. We’re done with our back end. Don’t forget that [you can find all of the code for this guide on GitHub](https://github.com/sitepoint-editors/vocab-builder), so if something didn’t work as expected, try cloning the repo and running that.

## Creating the Vue Front End

Previously we created our back end in a `server` folder. We’ll create the front-end part of the app in a `front-end` folder. This separation of concerns means that it would be easier to swap out the front end if we ever decided we wanted to use a framework other than Vue.

Let’s get to it.

### Basic Setup

We’ll use [Vue CLI](https://cli.vuejs.org/) to scaffold the project:

```
npm install -g @vue/cli
```

Make sure you’re in the root folder of the project (`vocab-builder`), then run the following:

```
vue create front-end
```

This will open a wizard to walk you through creating a new Vue app. Answer the questions as follows:

```
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, Linter
? Use history mode for router? Yes
? Pick a linter / formatter config: ESLint with error prevention only
? Pick additional lint features: Lint on save
? Where do you prefer placing config for Babel etc.? In dedicated config files
? Save this as a preset for future projects? No
```

The main thing to note here is that we’re installing the Vue router, which we’ll use to display the different views in our front end.

Next, change into our new directory:

```
cd front-end
```

There are a few files created by the CLI that we don’t need. We can delete these now:

```
rm src/assets/logo.png src/components/HelloWorld.vue src/views/About.vue src/views/Home.vue
```

There are also a bunch of files we’ll need to create:

```
cd src
touch components/{VocabTest.vue,WordForm.vue}
touch views/{Edit.vue,New.vue,Show.vue,Test.vue,Words.vue}
mkdir helpers
touch helpers/helpers.js
```

When you’re finished, the contents of your `vocab-builder/front-end/src` folder should look like this:

```
.
├── App.vue
├── assets
├── components
│   ├── VocabTest.vue
│   └── WordForm.vue
├── helpers
│   └── helpers.js
├── main.js
├── router.js
└── views
    ├── Edit.vue
    ├── New.vue
    ├── Show.vue
    ├── Test.vue
    └── Words.vue
```

### Install the Dependencies

For the front end, we’ll be using the following libraries:

*   [axios](https://www.npmjs.com/package/axios)—a Promise-based HTTP client which will allow us to make Ajax requests from our front end to our back end.
*   [semantic-ui-css](https://www.npmjs.com/package/semantic-ui-css)—a lightweight, CSS-only version of Semantic UI.
*   [vue-flash-message](https://www.npmjs.com/package/vue-flash-message)—a Vue flash message component which we will use to display information to the user.

Let’s get them installed:

```
npm i axios semantic-ui-css vue-flash-message
```

And with that, we’re ready to start coding.

### Creating the Routes

Firstly, we need to consider which routes our application will have. We’ll need to perform all of the CRUD options we discussed previously, and it would also be nice if the user could test themselves against whatever words have been added to the database.

To this end, we’ll create the following:

*   `/words`—display all the words in the database
*   `/words/new`—create a new word
*   `/words/:id`—display a word
*   `/words/:id/edit`—edit a word
*   `/test`—test your knowledge

Deleting a word doesn’t require its own route. We’ll just fire off the appropriate request and redirect to `/words`.

To put this into action, open up `src/router.js` and replace the existing code with the following:

```
import Vue from 'vue';
import Router from 'vue-router';
import Words from './views/Words.vue';
import New from './views/New.vue';
import Show from './views/Show.vue';
import Edit from './views/Edit.vue';
import Test from './views/Test.vue';

Vue.use(Router);

export default new Router({
  mode: 'history',
  base: process.env.BASE_URL,
  linkActiveClass: 'active',
  routes: [
    {
      path: '/',
      redirect: '/words'
    },
    {
      path: '/words',
      name: 'words',
      component: Words
    },
    {
      path: '/words/new',
      name: 'new-word',
      component: New
    },
    {
      path: '/words/:id',
      name: 'show',
      component: Show
    },
    {
      path: '/words/:id/edit',
      name: 'edit',
      component: Edit
    },
    {
      path: '/test',
      name: 'test',
      component: Test
    }
  ]
});
```

This creates the routes we discussed above. It also redirects the root URL `/` to `/words` and tells the router to apply a class of `active` to the currently activated navigation link (the default would be `router-link-active`, which wouldn’t play nicely with `semantic-ui-css`).

Talking of which, next we need to open up `src/main.js` and tell Vue to use `semantic-ui-css`:

```
import Vue from 'vue';
import App from './App.vue';
import router from './router';

import 'semantic-ui-css/semantic.css';

Vue.config.productionTip = false;

new Vue({
  router,
  render: h => h(App)
}).$mount('#app');
```

And finally, we need to replace the code in `src/App.vue` with the following:

```
<template>
  <div id="app">
    <div class="ui inverted segment navbar">
      <div class="ui center aligned container">
        <div class="ui large secondary inverted pointing menu compact">
          <router-link to="/words" exact class="item">
            <i class="comment outline icon"></i> Words
          </router-link>
          <router-link to="/words/new" class="item">
            <i class="plus circle icon"></i> New
          </router-link>
          <router-link to="/test" class="item">
            <i class="graduation cap icon"></i> Test
          </router-link>
        </div>
      </div>
    </div>

    <div class="ui text container">
      <div class="ui one column grid">
        <div class="column">
          <router-view />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app'
};
</script>

<style>
#app > div.navbar {
  margin-bottom: 1.5em;
}
.myFlash {
  width: 250px;
  margin: 10px;
  position: absolute;
  top: 50;
  right: 0;
}
input {
  width: 300px;
}
div.label {
  width: 120px;
}
div.input {
  margin-bottom: 10px;
}
button.ui.button {
  margin-top: 15px;
  display: block;
}
</style>
```

This creates a nav bar at the top of the screen, then declares an outlet (the `<router-view />` component) for our views.

Start the application from within the `front-end` folder with the command `npm run serve`.

You should now be able to go to [http://localhost:8080](http://localhost:8080) and navigate around the shell of our app.

Exciting times, huh?

### Communicating with the Back End

The next thing we need to do is establish a method of communicating with our Node back end. This is where the axios library comes in that we installed previously. To make our app flexible, we can add any axios-related code to a helper file which can be included in any component that needs it. Setting things up this way has the advantage of keeping all of our Ajax logic in one place, and also means that if we ever wanted to swap out axios for a different library, it would be pretty easy.

So open up `src/helpers/helpers.js` and add the following code:

```
import axios from 'axios';

const baseURL = 'http://localhost:3000/words/';

const handleError = fn => (...params) =>
  fn(...params).catch(error => {
    console.log(error);
  });

export const api = {
  getWord: handleError(async id => {
    const res = await axios.get(baseURL + id);
    return res.data;
  }),
  getWords: handleError(async () => {
    const res = await axios.get(baseURL);
    return res.data;
  }),
  deleteWord: handleError(async id => {
    const res = await axios.delete(baseURL + id);
    return res.data;
  }),
  createWord: handleError(async payload => {
    const res = await axios.post(baseURL, payload);
    return res.data;
  }),
  updateWord: handleError(async payload => {
    const res = await axios.put(baseURL + payload._id, payload);
    return res.data;
  })
};
```

There are a couple of things to be aware of here. Firstly, we’re exporting an `api` object that exposes methods corresponding to the endpoints we created in the previous section. These methods will make Ajax calls to our back end, which will carry out the various CRUD operations.

Secondly, due to the asynchronous nature of Ajax, we’re using [async/await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function), which allows us to wait for the result of an asynchronous operation (such as writing to the database) before continuing with the rest of the code. However, there’s a slight caveat here. The normal way of dealing with errors within `async/await` is to wrap everything in a `try/catch` block:

```
export const api = {
  getWord: async id => {
    try {
      await axios.get(baseURL + id);
      return res.data;
    } catch(error) {
      console.log(error);
    }
  }
  ...
}
```

However, this is very verbose and would make for some bloated code, as we would need to do it for each Ajax call. An alternative approach is to use a [higher-order function](https://www.sitepoint.com/higher-order-functions-javascript/) to handle the error for us.

This higher-order function takes a function as an argument (function `a`) and returns a function (function `b`), which, when called, will call function `a`, passing along any arguments it received. Function `b` will also chain a `catch` block to the end of function `a`, meaning that if an error occurs in function `a`, it will be caught and dealt with.

```
const handleError = fn => (...params) =>
  fn(...params).catch(error => {
    console.log(error);
  });

export const api = {
  getWord: handleError(async id => {
    const res = await axios.get(baseURL + id);
    return res.data;
  })
  ...
}
```

If you’d like to dive into this some more, check out our article [Flow Control in Modern JS: Callbacks to Promises to Async/Await](https://www.sitepoint.com/flow-control-callbacks-promises-async-await/).

### Fetching Words from the Database

So let’s get some words to display to the user. Open up the `src/views/Words.vue` component and add the following code:

```
<template>
  <div>
    <h1>Words</h1>
    <table id="words" class="ui celled compact table">
      <thead>
        <tr>
          <th>English</th>
          <th>German</th>
          <th colspan="3"></th>
        </tr>
      </thead>
      <tr v-for="(word, i) in words" :key="i">
        <td>{{ word.english }}</td>
        <td>{{ word.german }}</td>
        <td width="75" class="center aligned">Show</td>
        <td width="75" class="center aligned">Edit</td>
        <td width="75" class="center aligned">Destroy</td>
      </tr>
    </table>
  </div>
</template>

<script>
import { api } from '../helpers/helpers';

export default {
  name: 'words',
  data() {
    return {
      words: []
    };
  },
  async mounted() {
    this.words = await api.getWords();
  }
};
</script>
```

As you can see, we’re importing our API to perform operations against the back end, then in the component’s `mounted` lifecycle hook we’re calling its `getWords` method to fetch all of the words from the database. As the component has a `words` property on its `data` object, we can await the answer from the back end, then insert the response into `this.words` and the component will update.

Give it a try. Use Compass or Postman to insert a word into the database, then observe that it’s displayed on the page at `/words`.

### Displaying a Single Word

Let’s now add the functionality to display a single word from the list of words. In `src/views/Words.vue`, replace:

```
<td width="75" class="center aligned">Show</td>
```

with:

```
<td width="75" class="center aligned">
  <router-link :to="{ name: 'show', params: { id: word._id }}">Show</router-link>
</td>
```

This creates a link to the `show` route which we defined in our `src/router.js` file. It uses the current word’s `_id` property to build the URL, resulting in something like `http://localhost:8081/words/5bed4462bbd0ff553fb008d4`.

Now open up `src/views/Show.vue` and add the following code:

```
<template>
  <div>
    <h1>Show Word</h1>

    <div class="ui labeled input fluid">
      <div class="ui label">
        <i class="germany flag"></i> German
      </div>
      <input type="text" readonly  :value="word.german"/>
    </div>
    <div class="ui labeled input fluid">
      <div class="ui label">
        <i class="united kingdom flag"></i> English
      </div>
      <input type="text" readonly  :value="word.english"/>
    </div>
    <div class="actions">
      <router-link :to="{ name: 'edit', params: { id: this.$route.params.id }}">
        Edit word
      </router-link>
    </div>
  </div>
</template>

<script>
import { api } from '../helpers/helpers';

export default {
  name: 'show',
  data() {
    return {
      word: ''
    };
  },
  async mounted() {
    this.word = await api.getWord(this.$route.params.id);
  }
};
</script>

<style scoped>
.actions a {
  display: block;
  text-decoration: underline;
  margin: 20px 10px;
}
</style>
```

When mounted, this component will use the same technique as before to get a single word from the database. It identifies the word in question by extracting its ID from the URL using `this.$route.params.id`. This is possible because of how we declared the route in `src/router.js`. Here we used `path: "/words/:id"` which means that anything after `/words/` should be available to us as `$route.params.id`.

Also take note of the `scoped` attribute on the `<style>` tag. This means that any styles declared here are applied to this component only.

If you run the app at this point, you should be able to see a list of words contained in the database under `/words` and view individual words by clicking on *Show*.

![Show Word screen displaying "Person" "Mensch"](Images/chrome-1.jpg) 

You’ll notice there’s an *Edit word* link in the screenshot above. Let’s implement that now.

### Editing a Word

Open `src/views/Edit.vue` and add the following:

```
<template>
  <div>
    <h1>Edit Word</h1>
    <word-form :word=this.word></word-form>
  </div>
</template>

<script>
import WordForm from '../components/WordForm.vue';
import { api } from '../helpers/helpers';

export default {
  name: 'edit',
  components: {
    'word-form': WordForm
  },
  data: function() {
    return {
      word: {}
    };
  },
  async mounted() {
    this.word = await api.getWord(this.$route.params.id);
  }
};
</script>
```

There’s something slightly different going on in this component. If you look within the `<template>` tag, you’ll notice that we’re including another component, `WordForm`, and passing it the value of `this.word` as a prop. The value of `this.word` is being retrieved within the `mounted` lifecycle hook, just as we’ve done in the other components. Also notice that we’re declaring the child component that the `Edit` component requires, like so:

```
components: {
  "word-form": WordForm
}
```

So why are we including a `WordForm` component and handing the word to be edited off to that? Well, the reason is reusability. By structuring things this way, we’ll be able to use the same `WordForm` component in a little while when we come to implement the functionality to create a new word.

Let’s have a look at the `WordForm` component. Open up `src/components/WordForm.vue` and add the following code:

```
<template>
 <form action="#" @submit.prevent="onSubmit">
    <p v-if="errorsPresent" class="error">Please fill out both fields!</p>

    <div class="ui labeled input fluid">
      <div class="ui label">
        <i class="germany flag"></i> German
      </div>
      <input type="text" placeholder="Enter word..." v-model="word.german" />
    </div>

    <div class="ui labeled input fluid">
      <div class="ui label">
        <i class="united kingdom flag"></i> English
      </div>
      <input type="text" placeholder="Enter word..." v-model="word.english" />
    </div>

    <button class="positive ui button">Submit</button>
  </form>
</template>

<script>
export default {
  name: 'word-form',
  props: {
    word: {
      type: Object,
      required: false
    }
  },
  data() {
    return {
      errorsPresent: false
    };
  },
  methods: {
    onSubmit: function() {
      console.log(`English: ${this.word.english}`);
      console.log(`German: ${this.word.german}`);
    }
  }
};
</script>

<style scoped>
.error {
  color: red;
}
</style>
```

There’s quite a bit going on here. Firstly, we have a form tag and we’ve bound the `submit` event to the `onSubmit` method we’ve defined in our `methods` object. We’re also using the `prevent` modifier to prevent the browser’s default action—in this case, submitting the form.

Next comes a paragraph tag to display an error message if either of the input fields is empty. We use [v-if](https://vuejs.org/v2/api/#v-if) to only display this if the `errorsPresent` property evaluates to something truthy.

Then we have our form with two input fields, one for the English word and one for its German equivalent. We’re using [v-model](https://vuejs.org/v2/guide/forms.html) to set up two-way data binding between the `english` and `german` properties of the prop we’re passed and the input fields.

In the `<script>` section, we then declare that the `word` prop is of type `Object`, and that it isn’t required (because we’ll also use this form to create a new word). The `data` object declares the aforementioned `errorsPresent` property and our method object, the `onSubmit` method. All we’re doing in this method is logging out the value of whatever has been entered into the inputs.

At this point, if you visit the *Edit word* view, you should see the correct word displayed in the fields. And when you click *Submit*, you should see the value of both input fields logged to the console.

![Edit Word screen displaying "Eagle" "Adler"](Images/chrome-2.jpg) 

Finally, we need to expand our `onSubmit` method to do something other than log the values of the inputs to the console. Alter it like so:

```
onSubmit: function() {
  if (this.word.english === '' || this.word.german === '') {
    this.errorsPresent = true;
  } else {
    this.$emit('createOrUpdate', this.word);
  }
}
```

This checks that both fields have a value. If not, it flags the error, otherwise it emits an event `createOrUpdate` which we can listen for in the parent component (in this case, `Edit`). I’ve called it `createOrUpdate`, as the corresponding functionality in the parent component will be doing one of these two things.

Back in `src/views/Edit.vue`, we need to listen for and respond to the `createOrUpdate` event. Change:

```
<word-form :word=this.word></word-form>
```

to:

```
<word-form @createOrUpdate="createOrUpdate" :word=this.word></word-form>
```

And implement the update functionality in the `methods` object:

```
methods: {
  createOrUpdate: async function(word) {
    await api.updateWord(word);
    alert('Word updated sucessfully!');
    this.$router.push(`/words/${word._id}`);
  }
}
```

Now when you try to update a word, it will check that neither field is blank, and if not, update the word, before alerting a success message and redirecting you to the newly updated word.

As a final touch to this section, hop back into `src/views/Words.vue` and change:

```
<td width="75" class="center aligned">Edit</td>
```

to:

```
<td width="75" class="center aligned">
  <router-link :to="{ name: 'edit', params: { id: word._id }}">Edit</router-link>
</td>
```

### Adding Flash Messages

Okay, so our app is looking pretty good, but using alerts to inform the user that something happened is a jarring experience. Let’s use flash messages instead. These are nicely styled, configurable messages which won’t block the execution of JavaScript in the browser.

The first thing we’ll need to do is to tell our app to use them. To this end, hop back into `src/helpers/helpers.js` and make sure the top of the file reads like so:

```
import axios from 'axios';
import Vue from 'vue';
import VueFlashMessage from 'vue-flash-message';
import 'vue-flash-message/dist/vue-flash-message.min.css';

Vue.use(VueFlashMessage, {
  messageOptions: {
    timeout: 3000,
    pauseOnInteract: true
  }
});

const vm = new Vue();
const baseURL = 'http://localhost:3000/words/';

const handleError = fn => (...params) =>
  fn(...params).catch(error => {
    vm.flash(`${error.response.status}: ${error.response.statusText}`, 'error');
  });

export const api = { ... };
```

There are a few things going on here. We start by importing Vue and VueFlashMessages. We then tell Vue to use the VueFlashMessages plugin and pass it a couple of options. Finally, we create a new instance of Vue, as we also want to use the flash messages from within the helper file. You can see this happening within our `handleError` function in the call to `vm.flash()`.

So that we can actually display the messages, let’s add a `FlashMessage` component to `src/App.vue`:

```
<div class="ui text container">
  <flash-message class="myFlash"></flash-message>

  <div class="ui one column grid">
    <div class="column">
      <router-view />
    </div>
  </div>
</div>
```

To test out whether it’s working, try changing the value of the `baseURL` variable in `src/helpers/helpers.js` to something non-existent. If all has gone according to plan, you should see a nicely formatted error message on the right hand of the screen when you visit any of our routes.

Finally, to make a flash message appear when a word was successfully edited, go back to `src/views/Edit.vue` and change:

```
alert("Word updated sucessfully!");
```

to:

```
this.flash('Word updated sucessfully!', 'success');
```

### Creating a New Word

We’ve almost implemented all of our CRUD functionality. Next up is giving users the opportunity to add words of their own to our database. Open up `src/views/New.vue` and add the following:

```
<template>
  <div>
    <h1>New Word</h1>
    <word-form @createOrUpdate="createOrUpdate"></word-form>
  </div>
</template>

<script>
import WordForm from '../components/WordForm.vue';
import { api } from '../helpers/helpers';

export default {
  name: 'new-word',
  components: {
    'word-form': WordForm
  },
  methods: {
    createOrUpdate: async function(word) {
      const res = await api.createWord(word);
      this.flash('Word created', 'success');
      this.$router.push(`/words/${res._id}`);
    }
  }
};
</script>
```

This should hopefully look familiar to you, as it’s quite similar to the `Edit` component. It also uses the `WordForm` child component, but doesn’t pass it a prop. And, like the `Edit` component, it also listens for the `createOrUpdate` event. When it receives this event, it creates a new word with the given input and redirects to the newly created word.

Before we can use it, however, there are a couple of changes that need to be made to the `WordForm` component. Head back to `src/components/WordForm.vue` and expand the `props` object like so:

```
props: {
  word: {
    type: Object,
    required: false,
    default: () => {
      return {
        english: '',
        german: ''
      };
    }
  }
},
```

Here, we’re initializing both values as empty strings.

Now when you head to [http://localhost:8080/words/new](http://localhost:8080/words/new) you should be able to create new words.

### Destroying a Word

We won’t need a separate component to destroy a word, as there’s no view involved. The action takes place in `src/views/Words.vue`:

First change:

```
<td width="75" class="center aligned">Destroy</td>
```

to:

```
<td width="75" class="center aligned" @click.prevent="onDestroy(word._id)">
  <a :href="`/words/${word._id}`">Destroy</a>
</td>
```

This will intercept the click on the table cell, prevent the browser’s default action, then call the `onDestroy` method. Let’s implement that now:

```
methods: {
  async onDestroy(id) {
    const sure = window.confirm('Are you sure?');
    if (!sure) return;

    await api.deleteWord(id);
    this.flash('Word deleted sucessfully!', 'success');
    const newWords = this.words.filter(word => word._id !== id);
    this.words = newWords;
  }
},
```

To make sure the user really intended to delete a word, we use a dialogue to ask them to confirm the delete. If the user clicks *OK*, a request is sent to the API to delete the word. We then flash a message to let them know that the delete was successful before removing the word from the list of words in the `data` object. This will ensure that the UI updates.

And with that, our CRUD app is fully functional. Yay!

## Taking it Further

By way of a final touch, let’s add the possibility for users to test themselves on the words stored in the database.

Open up `src/views/Test.vue` and add the following code:

```
<template>
  <div>
    <h1>Test</h1>

    <div v-if="words.length < 5">
      <p>You need to enter at least five words to begin the test</p>
    </div>
    <div v-else>
      <vocab-test :words="words"></vocab-test>
    </div>
  </div>
</template>

<script>
import { api } from '../helpers/helpers';
import VocabTest from '../components/VocabTest.vue';

export default {
  name: 'test',
  components: {
    'vocab-test': VocabTest
  },
  data() {
    return {
      words: []
    };
  },
  async mounted() {
    this.words = await api.getWords();
  }
};
</script>
```

Here, we’re waiting until the component has been mounted, then fetching all of our words from the database. If there are less than five, we display a message that there aren’t enough words to begin the test. Otherwise, we load the `VocabTest` component and pass it our list of words as a prop.

Now all that remains is to code the test itself. Open up `src/components/VocabTest.vue` and add the following:

```
<template>
  <div>
    <h2>Score: {{ score }} out of {{ this.words.length }}</h2>

    <form action="#" @submit.prevent="onSubmit">
      <div class="ui labeled input fluid">
        <div class="ui label">
          <i class="germany flag"></i> German
        </div>
        <input type="text" readonly :disabled="testOver" :value="currWord.german"/>
      </div>
      <div class="ui labeled input fluid">
        <div class="ui label">
          <i class="united kingdom flag"></i> English
        </div>
        <input type="text" placeholder="Enter word..." v-model="english" :disabled="testOver" autocomplete="off" />
      </div>

      <button class="positive ui button" :disabled="testOver">Submit</button>
    </form>

    <p :class="['results', resultClass]">
      <span v-html="result"></span>
    </p>
  </div>
</template>

<script>
export default {
  name: 'vocab-test',
  props: {
    words: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      randWords: [...this.words.sort(() => 0.5 - Math.random())],
      incorrectGuesses: [],
      result: '',
      resultClass: '',
      english: '',
      score: 0,
      testOver: false
    };
  },
  computed: {
    currWord: function() {
      return this.randWords.length ? this.randWords[0] : '';
    }
  },
  methods: {
    onSubmit: function() {
      if (this.english === this.currWord.english) {
        this.flash('Correct!', 'success', { timeout: 1000 });
        this.score += 1;
      } else {
        this.flash('Wrong!', 'error', { timeout: 1000 });
        this.incorrectGuesses.push(this.currWord.german);
      }

      this.english = '';
      this.randWords.shift();

      if (this.randWords.length === 0) {
        this.testOver = true;
        this.displayResults();
      }
    },
    displayResults: function() {
      if (this.incorrectGuesses.length === 0) {
        this.result = 'You got everything correct. Well done!';
        this.resultClass = 'success';
      } else {
        const incorrect = this.incorrectGuesses.join(', ');
        this.result = `<strong>You got the following words wrong:</strong> ${incorrect}`;
        this.resultClass = 'error';
      }
    }
  }
};
</script>

<style scoped>
.results {
  margin: 25px auto;
  padding: 15px;
  border-radius: 5px;
}

.error {
  border: 1px solid #ebccd1;
  color: #a94442;
  background-color: #f2dede;
}

.success {
  border: 1px solid #d6e9c6;
  color: #3c763d;
  background-color: #dff0d8;
}
</style>
```

This guide is already very long, so I won’t explain what every line of the code does. In a nutshell, however, we’re receiving the word list, `words`, as a prop (this is an array of objects). We then declare some data properties, mostly related to displaying the test. The `randWords` property makes use of the spread operator and an arrow function to sort the words into a random order.

We’re declaring `currWord` as a [computed property](https://vuejs.org/v2/guide/computed.html), which will return the next word in the list of random words. I’ve used a computed property, as in the `onSubmit` method I’m removing the first item of the `randWords` array using `shift()` every time the user makes a guess. Mutating the array like this will cause `currWord` to be recalculated and the test will update.

Finally, the `onSubmit` method and the `displayResults` method handle form submission (when the user makes a guess) and, as you might have guessed, displaying the results.

## Conclusion

This has been a long tutorial, so congratulations if you made it this far. I hope you now have a better understanding of how to set up a Vue.js front end to consume a Node API which can then persist data to a database.

And please don’t forget, [the complete code is available on GitHub](https://github.com/sitepoint-editors/vocab-builder).

# Chapter 2: Creating Beautiful Charts Using Vue.js Wrappers for Chart.js

### by Yomi Eluwande

Charts are an important part of modern websites and applications. They help to present information that can’t be easily represented in text. Charts also help to make sense of data that would ordinarily not make sense in a textual format by presenting them in a view that’s easy to read and understand.

In this guide, I’ll show you how to represent data in the form of various types of chart with the help of [Chart.js](http://www.chartjs.org/) and [Vue.js](https://vuejs.org/). Chart.js is a simple yet flexible JavaScript charting library for developers and designers that allows drawing of different kinds of charts by using the HTML5 `canvas` element. A good refresher on Chart.js can be read [here](https://www.sitepoint.com/creating-beautiful-charts-chart-js/).

Vue.js is a progressive JavaScript framework, which we’ll use alongside Chart.js to demonstrate the chart examples. If you’re new to Vue.js, there’s [an awesome primer on using Vue.js](https://www.sitepoint.com/up-and-running-vue-js-2-0/) on SitePoint. We’ll also be using [Vue CLI](https://cli.vuejs.org/) to scaffold a Vue.js project for the demo we’re going to build.

## Charts, Charts, Charts

There’s an awesome collection of Vue wrappers for various charting libraries on the [awesome-vue](https://github.com/vuejs/awesome-vue#charts) repo on GitHub. However, as we’re concentrating on Chart.js, we’ll be looking at the following wrappers for that library:

*   [vue-charts](https://github.com/hchstera/vue-charts)
*   [vue-chartjs](https://github.com/apertureless/vue-chartjs)
*   [vue-chartkick](https://github.com/ankane/vue-chartkick)

We’ll be using these wrappers to demonstrate how to create different types of charts and also touch on the unique features that each of them offers.

#### Source Code

The source code for this tutorial is [available on GitHub](https://github.com/sitepoint-editors/vue-charts).

## Scaffolding the Project with Vue CLI

Let’s get started by installing Vue CLI with the following command:

```
npm install -g @vue/cli
```

Once that’s done, we can then get started with scaffolding a project by typing:

```
vue create chart-js-demo
```

This will open a wizard to walk you through creating a new Vue app. Answer the questions as follows:

```
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, Linter
? Use history mode for router? Yes
? Pick a linter / formatter config: ESLint with error prevention only
? Pick additional lint features: Lint on save
? Where do you prefer placing config for Babel etc.? In dedicated config files
? Save this as a preset for future projects? No
```

Now let’s install Chart.js, as well as the various wrappers we need for our app:

```
cd chart-js-demo
npm install chart.js chartkick hchs-vue-charts vue-chartjs vue-chartkick
```

#### The --save Flag

If you use npm 5, there’s no need for the `--save` flag anymore, as all packages are automatically saved now. Read more about that [here](http://blog.npmjs.org/post/161081169345/v500).

Let’s test what we have so far and run our application:

```
npm run serve
```

If all has gone well, you should be able to open [localhost:8080](http://localhost:8080) and see the standard welcome page.

### Basic Setup

Next, we’ll need to add a view for each wrapper. Create the following files in `src/views`:

*   `VueChartJS.vue`
*   `VueChartKick.vue`
*   `VueCharts.vue`

```
touch src/views/{VueChartJS.vue,VueChartKick.vue,VueCharts.vue}
```

Then create the following files in `src/components`:

*   `LineChart.vue`
*   `BarChart.vue`
*   `BubbleChart.vue`
*   `Reactive.vue`

```
touch src/components/{LineChart.vue,BarChart.vue,BubbleChart.vue,Reactive.vue}
```

These correspond to the type of charts we’ll be using.

Finally, you can delete the `About.vue` file in `src/views`, the `HelloWorld.vue` file in `src/components`, as well as the `assets` folder in `src`. We’ll not be needing those.

The contents of your `src` directory should look like this:

```
.
├── App.vue
├── components
│   ├── BarChart.vue
│   ├── BubbleChart.vue
│   ├── LineChart.vue
│   └── Reactive.vue
├── main.js
├── router.js
└── views
    ├── Home.vue
    ├── VueChartJS.vue
    ├── VueChartKick.vue
    └── VueCharts.vue
```

### Adding Routes

The next thing we want to do is create the different routes in which we can view the charts for each of the wrappers we created above. We would like to have a `/charts` route to display charts made with the `vue-charts` wrapper, `/chartjs` to display charts made with the `vue-chartjs` wrapper, and lastly `/chartkick` to display charts made with the `vue-chartkick` wrapper. We’ll also leave the `/` route in place to display the `Home` view.

Navigate to the `src` folder of the app and open up the`router.js` file. Replace the contents of that file with this:

```
import Vue from 'vue'
import Router from 'vue-router'
import Home from '@/views/Home'
import VueChartJS from '@/views/VueChartJS'
import VueChartKick from '@/views/VueChartKick'
import VueCharts from '@/views/VueCharts'

Vue.use(Router)

export default new Router({
  routes: [
    {
      path: '/',
      name: 'Home',
      component: Home
    },
    {
      path: '/chartjs',
      name: 'VueChartJS',
      component: VueChartJS
    },
    {
      path: '/chartkick',
      name: 'VueChartKick',
      component: VueChartKick
    },
    {
      path: '/charts',
      name: 'VueCharts',
      component: VueCharts
    }
  ]
})
```

Here we imported the Vue components that we created above. [Components](https://vuejs.org/v2/guide/components.html) are one of the most powerful features of Vue. They help us extend basic HTML elements to encapsulate reusable code. At a high level, components are custom elements that Vue’s compiler attaches behavior to.

Lastly, we defined the routes and components which will serve the different pages we need to display the different charts.

### Adding Navigation

We can define our navigation to be used across components in `src/App.vue`. We’ll also add some basic styling:

```
<template>
  <div id="app">
    <div id="nav">
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/chartjs">vue-chartjs</router-link></li>
        <li><router-link to="/charts">vue-charts</router-link></li>
        <li><router-link to="/chartkick">vue-chartkick</router-link></li>
      </ul>
    </div>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  height: 90px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: underline;
}

#nav a.router-link-exact-active {
  color: #42b983;
  text-decoration: none;
}

#nav ul {
  list-style-type: none;
  padding: 0;
}

#nav ul li {
  display: inline-block;
  margin: 0 10px;
}

h1 {
  font-size: 1.75em;
}

h2 {
  line-height: 2.5em;
  font-size: 1.25em;
}
</style>
```

Nothing too revolutionary here. Note the use of the `<router-view />` component, which is where we’ll display our views.

### Home Component

As mentioned above, the `Home` component serves as the default (`/`) route. Open it up and replace the content with the code block below:

```
<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <h1>Creating Beautiful Charts Using Vue.js Wrappers For Chart.js</h1>
        <h2>
          Read the article on SitePoint:
          <a href="https://www.sitepoint.com/creating-beautiful-charts-vue-chart-js/">
            https://www.sitepoint.com/creating-beautiful-charts-vue-chart-js/
          </a>
        </h2>
        <h3>
          Download the repo from GitHub:
          <a href="https://github.com/sitepoint-editors/vue-charts">
            https://github.com/sitepoint-editors/vue-charts
          </a>
        </h3>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'home'
}
</script>
```

### Adding Bulma

One more thing before we start adding charts. Let’s add the [Bulma CSS framework](http://bulma.io/) to the app. This should make things easier when it comes to CSS.

Open the `public/index.html` file and add the following inside the `head` tag:

```
<link href="https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.2/css/bulma.min.css" rel="stylesheet">
```

Now if you visit [localhost:8080](http://localhost:8080), you should be able to navigate around the shell of the app.

Finally we can move on to creating charts!

## Making Charts with vue-chartjs

`vue-chartjs` is a Chart.js wrapper that allows us to easily create reusable chart components. Reusability means we can import the base chart class and extend it to create custom components.

With that being said, we’ll be demonstrating four types of charts that can be built using `vue-chartjs`: a line chart, a bar chart, a bubble chart, and a bar chart that demonstrates reactivity (the chart updates whenever there’s a change in the data set).

### Line Chart

To create a line chart, we’ll create a component to render this type of chart only. Open the `LineChart.vue` component file inside the `src/components` folder and add the following code:

```
<script>
  //Importing Line class from the vue-chartjs wrapper
  import { Line } from 'vue-chartjs'

  //Exporting this so it can be used in other components
  export default {
    extends: Line,
    data () {
      return {
        datacollection: {
          //Data to be represented on x-axis
          labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
          datasets: [
            {
              label: 'Data One',
              backgroundColor: '#f87979',
              pointBackgroundColor: 'white',
              borderWidth: 1,
              pointBorderColor: '#249EBF',
              //Data to be represented on y-axis
              data: [40, 20, 30, 50, 90, 10, 20, 40, 50, 70, 90, 100]
            }
          ]
        },
        //Chart.js options that controls the appearance of the chart
        options: {
          scales: {
            yAxes: [{
              ticks: {
                beginAtZero: true
              },
              gridLines: {
                display: true
              }
            }],
            xAxes: [ {
              gridLines: {
                display: false
              }
            }]
          },
          legend: {
            display: true
          },
          responsive: true,
          maintainAspectRatio: false
        }
      }
    },
    mounted () {
      //renderChart function renders the chart with the datacollection and options object.
      this.renderChart(this.datacollection, this.options)
    }
  }
</script>
```

Let’s discuss what the code above is doing. The first thing we did was import the chart class we needed (in this case, `Line`) from the `vue-chartjs` and exported it.

The `data` property contains a `datacollection` object which contains all the information we’ll need to build the line chart. This includes the Chart.js configuration, like `labels`, which will be represented on the x-axis, the `datasets`, which will be represented on the y-axis, and the `options` object, which controls the appearance of the chart.

The `mounted` function calls `renderChart()` which renders the chart with the `datacollection` and `options` objects passed in as parameters.

Now, let’s open the `views/VueChartJS.vue` file and add in the following code:

```
<template>
  <section class="container">
    <h1>Demo examples of vue-chartjs</h1>
    <div class="columns">
      <div class="column">
        <h3>Line Chart</h3>
        <line-chart></line-chart>
      </div>
      <div class="column">
        <h3>Bar Chart</h3>
        <!--Bar Chart example-->
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <h3>Bubble Chart</h3>
        <!--Bubble Chart example-->
      </div>
      <div class="column">
        <h3>Reactivity - Live update upon change in datasets</h3>
        <!--Reactivity Line Chart example-->
      </div>
    </div>
  </section>
</template>

<script>
  import LineChart from '@/components/LineChart'
  import BarChart from '@/components/BarChart'
  import BubbleChart from '@/components/BubbleChart'
  import Reactive from '@/components/Reactive'

  export default {
    name: 'VueChartJS',
    components: {
      LineChart,
      BarChart,
      BubbleChart,
      Reactive
    }
  }
</script>
```

The `VueChartJS.vue` file contains the `template` section which holds the HTML code, a `script` section which holds the JavaScript code, and a `style` section which holds the CSS code.

Inside the `template` section, we used the `columns` class from Bulma to create a layout that has two columns and two rows. We also added a `line-chart` component which will be created in the `script` section.

Inside the `script` section, we imported the `.vue` files we created earlier and referenced them in the `components` object. This means we can then use them in the HTML code like this: `line-chart`, `bar-chart`, `bubble-chart` and `reactive`.

Now if you navigate to `/chartjs`, the line chart should display on that page.

#### Live Code

![Line chart](Images/charts1.png)

See the Pen [vue-chart.js - line chart](https://codepen.io/SitePoint/pen/zdGNNz/)

### Bar Chart

For the next chart, we’ll create a custom component that helps to render bar charts only. Open the `BarChart.vue` component file inside the `src/components` folder and add the following code:

```
<script>
  //Importing Bar class from the vue-chartjs wrapper
  import { Bar } from 'vue-chartjs'
  //Exporting this so it can be used in other components
  export default {
    extends: Bar,
    data () {
      return {
        datacollection: {
          //Data to be represented on x-axis
          labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
          datasets: [
            {
              label: 'Data One',
              backgroundColor: '#f87979',
              pointBackgroundColor: 'white',
              borderWidth: 1,
              pointBorderColor: '#249EBF',
              //Data to be represented on y-axis
              data: [40, 20, 30, 50, 90, 10, 20, 40, 50, 70, 90, 100]
            }
          ]
        },
        //Chart.js options that controls the appearance of the chart
        options: {
          scales: {
            yAxes: [{
              ticks: {
                beginAtZero: true
              },
              gridLines: {
                display: true
              }
            }],
            xAxes: [ {
              gridLines: {
                display: false
              }
            }]
          },
          legend: {
            display: true
          },
          responsive: true,
          maintainAspectRatio: false
        }
      }
    },
    mounted () {
      //renderChart function renders the chart with the datacollection and options object.
      this.renderChart(this.datacollection, this.options)
    }
  }
</script>
```

The code above works similarly to the one in the `LineChart.vue` file. The only difference here is that the `Bar` class is imported and extended instead of `Line`.

One more thing: before we can see our bar chart, we need to edit the `VueChartJS.vue` file and replace `<!--Bar Chart example-->` with `<bar-chart></bar-chart>`. We’re simply using the Bar component we created inside in our HTML template.

#### Live Code

![bar chart](Images/charts2.png)

See the Pen [vuechart-js - bar chart](https://codepen.io/SitePoint/pen/LjVxym/).

### Bubble Chart

For the bubble chart, we’ll create a component that helps to render bubble charts only.

#### Bubble Charts

Bubble charts use bubbles/circles to display data in a three dimension method (x, y, r). `x` is used to display the horizontal axis data, `y` is used to display the vertical data, and `r` is used to display the size of the individual bubbles.

Open the `BubbleChart.vue` component file inside the src/components folder and add the following code:

```
<script>
  //Importing Bubble class from the vue-chartjs wrapper
  import { Bubble } from 'vue-chartjs'
  //Exporting this so it can be used in other components
  export default {
    extends: Bubble,
    data () {
      return {
        datacollection: {
          //Data to be represented on x-axis
          labels: ['Data'],
          datasets: [
            {
              label: 'Data One',
              backgroundColor: '#f87979',
              pointBackgroundColor: 'white',
              borderWidth: 1,
              pointBorderColor: '#249EBF',
              //Data to be represented on y-axis
              data: [
                {
                  x: 100,
                  y: 0,
                  r: 10
                },
                {
                  x: 60,
                  y: 30,
                  r: 20
                },
                {
                  x: 40,
                  y: 60,
                  r: 25
                },
                {
                  x: 80,
                  y: 80,
                  r: 50
                },
                {
                  x: 20,
                  y: 30,
                  r: 25
                },
                {
                  x: 0,
                  y: 100,
                  r: 5
                }
              ]
            }
          ]
        },
        //Chart.js options that controls the appearance of the chart
        options: {
          scales: {
            yAxes: [{
              ticks: {
                beginAtZero: true
              },
              gridLines: {
                display: true
              }
            }],
            xAxes: [ {
              gridLines: {
                display: false
              }
            }]
          },
          legend: {
            display: true
          },
          responsive: true,
          maintainAspectRatio: false
        }
      }
    },
    mounted () {
      //renderChart function renders the chart with the datacollection and options object.
      this.renderChart(this.datacollection, this.options)
    }
  }
</script>
```

The code above works similarly to the code in the `LineChart.vue` and `BarChart.vue` files. The difference here is that the `Bubble` class is imported and extended instead of `Line` or `Bar` and the `datasets` object takes in different values for `x`, `y` and `z`.

We need to do one more thing before we can see our bubble chart—the same thing we did for other charts: edit the `VueChartJS.vue` file and replace `<!--Bubble Chart example-->` with `<bubble-chart></bubble-chart>`.

#### Live Code

![bubble chart](Images/charts3.png)

See the Pen [vue-chartjs - bubble chart](https://codepen.io/SitePoint/pen/mMJRxg/).

### Bar Chart That Demonstrates Reactivity

The last example we’ll be demonstrating with `vue-chartjs` is how it can be used to make a chart that automatically updates whenever there’s a change in the data set. It’s important to note that Chart.js ordinarily doesn’t offer this feature, but `vue-chartjs` does—with the help of either of these two mixins:

*   `reactiveProp`
*   `reactiveData`

Open the `Reactive.vue` component file inside the src/components folder and type in the following code:

```
<script>
  //Importing Bar and mixins class from the vue-chartjs wrapper
  import { Bar, mixins } from 'vue-chartjs'
  //Getting the reactiveProp mixin from the mixins module.
  const { reactiveProp } = mixins
  export default Bar.extend({
    mixins: [ reactiveProp ],
    data () {
      return {
        //Chart.js options that control the appearance of the chart
        options: {
          scales: {
            yAxes: [{
              ticks: {
                beginAtZero: true
              },
              gridLines: {
                display: true
              }
            }],
            xAxes: [ {
              gridLines: {
                display: false
              }
            }]
          },
          legend: {
            display: true
          },
          responsive: true,
          maintainAspectRatio: false
        }
      }
    },
    mounted () {
      // this.chartData is created in the mixin and contains all the data needed to build the chart.
      this.renderChart(this.chartData, this.options)
    }
  })
</script>
```

The first thing we did in the code above was to import the `Bar` and `mixins` classed from the `vue-chartjs` wrapper and extend `Bar`. We also extracted the `reactiveProp` mixin from the `mixins` module to be used for reactivity.

The `reactiveProp` mixin extends the logic of your chart component, automatically creates a prop named `chartData`, and adds a Vue watcher to this prop. We didn’t create a `dataset` object this time, as all the data needed will be inside the `chartData` prop.

For this to work, we’ll need to edit our `VueChartJS.vue` even further. Open `VueChartJS.vue`, and after the `components` property, add the following code:

```
data () {
  return {
    // instantiating datacollection with null
    datacollection: null
  }
},
created () {
  //anytime the vue instance is created, call the fillData() function.
  this.fillData()
},
methods: {
  fillData () {
    this.datacollection = {
      // Data for the y-axis of the chart
      labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
      datasets: [
        {
          label: 'Data One',
          backgroundColor: '#f87979',
          // Data for the x-axis of the chart
          data: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt()]
        }
      ]
    }
  },
  getRandomInt () {
    // JS function to generate numbers to be used for the chart
    return Math.floor(Math.random() * (50 - 5 + 1)) + 5
  }
}
```

Let’s go through the code above. In the `data` object we return `datacollection`, which is set to `null`, and in the `created` method, we call `fillData()` anytime the component instance is created. The `fillData` function will be created in the `methods` object.

In the `methods` object, we create a function called `fillData`. This function creates a `datacollection` object, which contains a `label` array (data for the x-axis), and a `datasets` array, which holds the `data` array needed for the y-axis.

#### getRandomInt

The content of the `data` array is a `getRandomInt` function, which generates a random number for us.

Finally, to display our chart and see if reactivity works, replace `<!--Reactivity Line Chart example-->` with this:

```
<reactive :chart-data="datacollection"></reactive>
<button class="button is-primary" @click="fillData()">Randomize</button>
```

We’re using the `reactive` component we created and passing the contents of `datacollection` to the `chart-data` props to display the chart. And we also have a button that calls the `fillData()` method any time it’s clicked on.

Navigate to `/chartjs` route in the app to see the new chart and click on the *Randomize* button to see the chart automatically render again with the new data in real time.

#### Live Code

![reactive bar chart](Images/charts4.png)

See the Pen [vue-chartjs - reactive bar chart](https://codepen.io/SitePoint/pen/dzoNxr/).

## Making Charts with vue-charts

`vue-charts` takes a very different approach to building charts from `vue-chartjs`. It doesn’t require you to create separate components to process data and render the chart. All data required for the chart can be instantiated in the Vue instance like this:

```
data () {
  return {
    labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
    dataset: [65, 59, 80, 81, 56, 55, 40]
  }
}
```

And we can easily display a line chart by using `<chartjs-line></chartjs-line>` in our template, a bar chart by using `<chartjs-bar></chartjs-bar>`, and a radar chart by using `<chartjs-radar></chartjs-radar>`.

Before we go on, we need to register vue-charts globally. Open the `main.js` inside the `src` folder and add the following lines of code under the existing `import` statements:

```
import 'chart.js'
import 'hchs-vue-charts'

Vue.use(window.VueCharts)
```

Here we import the Chart.js library and `hchs-vue-charts` wrapper from the `node_modules` folder and register it globally with `Vue.use(window.VueCharts)`.

Now let’s get started with `vue-charts`. Open up the `VueCharts.vue` file we created earlier and type in the following code:

```
<template>
  <section class="container">
    <h1>Demo examples of vue-charts</h1>
    <div class="columns">
      <div class="column">
        <h3>Line Chart</h3>
        <!--Line Chart Example-->
      </div>
      <div class="column">
        <h3>Bar Chart</h3>
        <!--Bar Chart Example-->
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <h3>Radar Chart</h3>
        <!--Radar Chart Example-->
      </div>
      <div class="column">
        <h3>Data Binding Line Chart</h3>
        <!--Data Binding Line Chart Example-->
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'VueCharts',
    data () {
      return {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
        dataset: [65, 59, 80, 81, 56, 55, 40]
      }
    }
  }
</script>
```

In the code block above we created placeholders for charts, and all we have to do is start putting them in.

We then added the labels and data we’ll be using for the various charts in the `data` object inside the `script` section.

Let’s begin to create the charts now.

### Line Chart

To add the line chart, all we have to is add `<chartjs-line></chartjs-line>` in place of the comment `<!--Line Chart Example-->` in the template section of the `VueCharts.vue` file. We don’t need to import any component because `vue-charts` has been declared globally in `main.js`.

### Bar Chart

We do the same for bar charts. Add `<chartjs-bar></chartjs-bar>` in place of the comment `<!--Bar Chart Example-->` in the template section of the `VueCharts.vue` file.

### Radar Chart

We do the same for radar charts. Add `<chartjs-radar></chartjs-radar>` in place of the comment `<!--Radar Chart Example-->` in the template section of the `VueCharts.vue` file.

Once that’s done, you can navigate to `/charts` and check out the charts we just created.

#### Live Code

![vue charts demo](Images/charts5.png)

See the Pen [vue-charts demo](https://codepen.io/SitePoint/pen/QMbpWp/).

### A Data Binding Example with a Line Chart

Data binding in `vue-charts` is similar to that of `vue-chartjs`, although `vue-charts` automatically updates the chart whenever the data set changes.

To test this, we’ll create a function named `addData` and add it to the `methods` object of the component:

```
methods: {
  addData () {
    this.dataset.push(this.dataentry)
    this.labels.push(this.datalabel)
    this.datalabel = ''
    this.dataentry = ''
  }
}
```

The `addData` method pushes the current value of the data form input and label form input (which we’ll be adding soon) to the current data set. Now let’s add the component as well as the form to add new data and a label.

Add the following piece of code in place of the comment `<!--Data Binding Line Chart Example-->`:

```
<form @submit.prevent="addData">
  <input placeholder="Add a Data" v-model="dataentry">
  <input placeholder="Add a Label" v-model="datalabel">
  <button type="submit">Submit</button>
</form>
<chartjs-line :labels="labels" :data="dataset" :bind="true"></chartjs-line>
```

The code above is a form that allows you to type in values of data and label and then submit the form. The chart will render automatically with the latest entry.

#### Live Code

![vue charts data binding](Images/charts6.png)

See the Pen [vue-charts data binding](https://codepen.io/SitePoint/pen/eENvmV/).

## Making Charts with vue-chartkick

[vue-chartkick](https://github.com/ankane/vue-chartkick) is a Vue wrapper that allows you to create beautiful charts with one line. We’ll be demonstrating the use of this library with four examples. We’ll be creating a line chart, bar chart, scatter chart and also use the download feature (downloadable charts).

In terms of handling data needed for the chart data set, `vue-chartkick` gives us two options. We can do something like `<bar-chart :data="[['Work', 1322], ['Play', 1492]]"></bar-chart>`, in which the data is added inline, or `<line-chart :data="chartData"></line-chart>`, and we declare the `chartData` array in the Vue data object like this:

```
data () {
  return {
    chartData: [['Jan', 44], ['Feb', 27], ['Mar', 60], ['Apr', 55], ['May', 37], ['Jun', 40], ['Jul', 69], ['Aug', 33], ['Sept', 76], ['Oct', 90], ['Nov', 34], ['Dec', 22]]
  }
}
```

Let’s get started with using vue-chartkick. Before we go on, open the `main.js` file inside the `src` folder and add the following code:

```
import Chartkick from 'chartkick'
import VueChartkick from 'vue-chartkick'

Vue.use(VueChartkick, { Chartkick })
```

Here we import the Chartkick library and the `vue-chartkick` wrapper from `node_modules` and register it globally with `Vue.use(VueChartkick, { Chartkick })`.

To start creating charts with vue-chartkick, open up the `VueChartKick.vue` file we created earlier and add the following code:

```
<template>
  <section class="container">
    <h1>Demo examples of vue-chartkick</h1>
    <div class="columns">
      <div class="column">
        <h3>Line Chart</h3>
        <!--Line Chart example-->
      </div>
      <div class="column">
        <h3>Bar Chart</h3>
        <!--Bar Chart example-->
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <h3>Scatter Chart</h3>
        <!--Scatter chart example-->
      </div>
      <div class="column">
        <h3>Downloadable Line Chart</h3>
        <!--Downloadable line chart-->
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'VueChartKick',
    data () {
      return {
        chartData: [['Jan', 44], ['Feb', 27], ['Mar', 60], ['Apr', 55], ['May', 37], ['Jun', 40], ['Jul', 69], ['Aug', 33], ['Sept', 76], ['Oct', 90], ['Nov', 34], ['Dec', 22]]
      }
    }
  }
</script>
```

In the code block above, we again created placeholders for the different types of charts we’ll be creating, and all we have to do is start putting them in.

We then created the `chartData` array that holds data we’ll be using for the various charts in the `data` object inside the `script` section. Let’s begin to create the charts now.

### Line Chart

Creating a line chart with `vue-chartkick` is very simple and straightforward. All you have to do is bring in the `vue-chartkick` `line-chart` component and also determine what dataset you want to use—something like this: `<line-chart :data="chartData"></line-chart>`. In this case, the `data` prop is set to the `chartData` array in the Vue `data` object.

Therefore, replace the comment `<!--Line Chart example-->` inside the `VueChartKick.vue` file with `<line-chart :data="chartData"></line-chart>` and the line chart should display nicely now.

### Bar Chart

We can create a bar chart in the same way we created the line chart above. But in this case, we’ll try something different. Instead of using the `chartData` array as the data set, we’ll add the data set inside the props, like this: `<bar-chart :data="[['Work', 1322], ['Play', 1492]]"></bar-chart>`.

Replace the comment `<!--Bar Chart example-->` inside the `VueChartKick.vue` file with `<bar-chart :data="[['Work', 1322], ['Play', 1492]]"></bar-chart>`, and your bar chart should display now.

### Scatter Chart

Scatter charts also work like the line and bar charts above. Replace the comment `<!--Scatter Chart example-->` inside the `VueChartKick.vue` file with `<scatter-chart :data="[[174.0, 80.0], [176.5, 82.3], [180.3, 73.6]]"></scatter-chart>` and your scatter chart should display now.

### Downloading a Chart

`vue-chartkick` has a pretty neat feature that `vue-chartjs` and `vue-charts` lack: the ability to create downloadable charts. Once a chart has been set to downloadable, users can easily save the chart as an image. So how does this work? Let's check it out with a line chart:

```
<line-chart :data="chartData" :download="true"></line-chart>
```

We set the `:download` prop to true, and that means the chart is downloadable. That’s all!

Replace the comment `<!--Downloadable line chart-->` inside the `VueChartKick.vue` file with `<line-chart :data="chartData" :download="true"></line-chart>` to see and test the download feature on your app. You can hover over the new chart to see the download button.

#### Live Code

![demo of vue-chartkick](Images/charts7.png)

See the Pen [vue-chartkick demos](https://codepen.io/SitePoint/pen/oeXZjO/).

## Comparisons

So now that we’ve gone through the three Vue.js wrappers for Chart.js, what are the pros and cons of each?

### vue-chartjs

`vue-chartjs` is perhaps the most powerful of the three wrappers. It gives so much room for flexibility and also ships with a reactivity feature (the ability to re-render a chart automatically if there’s been a change in the data).

A con for the wrapper would be that configuring the chart can be somewhat complex at the beginning, due to the various options available, and also because you have to create an external file to hold the configuration for the wrapper.

### vue-charts

`vue-chartjs` is a pretty good Chart.js wrapper. It’s very easy to set up, unlike `vue-chartjs`. It doesn’t require you to create separate components to process data and render charts. All the data required for the chart can be instantiated in the Vue instance, as seen in the examples above. It also ships with a reactivity feature (the ability to render a chart automatically if there’s been a change in the data set) without a need for mixins.

#### vue-chartkick

`vue-chartkick` is also a pretty good Chart.js wrapper. It may be the wrapper with the easiest path to usage among the three Chart.js wrappers.

The data set for the chart can be added in two different ways in `vue-chartkick`. We can do something like `<bar-chart :data="[['Work', 1322], ['Play', 1492]]"></bar-chart>`, in which the data is added inline, or `<line-chart :data="chartData"></line-chart>`, and we declare the `chartData` array in the Vue data object as seen above in the examples. It also ships with an awesome feature that allows you to download your charts as an image—something that the other wrappers lack.

The only disadvantage of `vue-chartkick` is that it doesn’t support reactivity out of the box.

## Conclusion

In this guide, I introduced various Vue wrappers for Chart.js, and also demonstrated examples of how to use each of them to create beautiful charts for your next web project.

The source code for this tutorial is [available on GitHub](https://github.com/sitepoint-editors/vue-charts), and if you’d like to see a live demo of the tutorial, you can also see that [here](https://vue-charts.herokuapp.com/).

# Chapter 3: Build a Real-time Chat App with Pusher and Vue.js

### by Michael Wanyoike

Apps that communicate in real time are becoming more and more popular nowadays, as they make for a smoother, more natural user experience.

In this tutorial, we’re going to build a real-time chat application using Vue.js powered by [ChatKit](https://pusher.com/chatkit), a service provided by [Pusher](https://pusher.com). The ChatKit service will provide us with a complete back end necessary for building a chat application on any device, leaving us to focus on building a front-end user interface that connects to the ChatKit service via the [ChatKit client package](https://www.npmjs.com/package/@pusher/chatkit-client).

## Prerequisites

This is an intermediate- to advanced-level tutorial. You’ll need to be familiar with the following concepts to follow along:

*   Vue.js basics
*   Vuex fundamentals
*   employing a CSS framework

You’ll also need Node installed on your machine. You can do this by downloading the binaries from the [official website](https://nodejs.org/), or by using a [version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). This is probably the easiest way, as it allows you to manage multiple versions of Node on the same machine.

Finally, you’ll need to install Vue CLI globally with the following command:

```
npm install -g @vue/cli
```

At the time of writing, Node 10.14.1 and Vue CLI 3.2.1 are the latest versions.

## About the Project

We’re going to build a rudimentary chat application similar to Slack or Discord. The app will do the following:

*   have multiple channels and rooms
*   list room members and detect presence status
*   detect when other users start typing

As mentioned earlier, we’re just building the front end. The ChatKit service has a back-end interface that will allows us to manage users, permissions and rooms.

You can find the complete code for this project on [GitHub](https://github.com/sitepoint-editors/vue-chatkit).

## Setting up a ChatKit Instance

Let’s create our ChatKit instance, which is similar to a server instance if you’re familiar with Discord.

Go to the [ChatKit](https://pusher.com/chatkit) page on Pusher’s website and click the *Sign Up* button. You’ll be prompted for an email address and password, as well as the option to sign in with GitHub or Google.

Select which option suits you best, then on the next screen fill out some details such as *Name*, *Account type*, *User role* etc.

Click *Complete Onboarding* and you’ll be taken to the main Pusher dashboard. Here, you should click the ChatKit Product.

![The ChatKit dashboard](Images/chatkit-dashboard.png) 

Click the Create button to create a new ChatKit Instance. I’m going to call mine `VueChatTut`.

![Creating a new ChatKit instance](Images/create-chatkit-instance.png) 

We’ll be using the free plan for this tutorial. It supports up to 1,000 unique users, which is more than sufficient for our needs. Head over to the *Console* tab. You’ll need to create a new user to get started. Go ahead and click the *Create User* button.

![Creating a ChatKit user](Images/chatkit-create-user.png) 

I’m going to call mine “john” (*User Identifier*) and “John Wick” (*Display Name*), but you can name yours however you want. The next part is easy: create the two or more users. For example:

*   salt, Evelyn Salt
*   hunt, Ethan Hunt

Create three or more rooms and assign users. For example:

*   General (john, salt, hunt)
*   Weapons (john, salt)
*   Combat (john, hunt)

Here’s a snapshot of what your *Console* interface should like.

![A snapshot of the console](Images/create-users-and-rooms.png) 

Next, you can go to the *Rooms* tab and create a message using a selected user for each room. This is for testing purposes. Then go to the *Credentials* tab and take note of the *Instance Locator*. We’ll need to activate the *Test Token Provider*, which is used for generating our HTTP endpoint, and take a note of that, too.

![Test token](Images/test-token.png) 

Our ChatKit back end is now ready. Let’s start building our Vue.js front end.

## Scaffolding the Vue.js Project

Open your terminal and create the project as follows:

```
vue create vue-chatkit
```

Select *Manually select features* and answer the questions as shown below.

![Questions to be answered](Images/create-project.png) 

Make doubly sure you’ve selected Babel, Vuex and Vue Router as additional features. Next, create the following folders and files as follows:

![Files and folders to create](Images/project-structure.png) 

Make sure to create all the folders and files as demonstrated. Delete any unnecessary files that don’t appear in the above illustration.

For those of you that are at home in the console, here are the commands to do all that:

```
mkdir src/assets/css
mkdir src/store

touch src/assets/css/{loading.css,loading-btn.css}
touch src/components/{ChatNavBar.vue,LoginForm.vue,MessageForm.vue,MessageList.vue,RoomList.vue,UserList.vue}
touch src/store/{actions.js,index.js,mutations.js}
touch src/views/{ChatDashboard.vue,Login.vue}
touch src/chatkit.js

rm src/components/HelloWorld.vue
rm src/views/{About.vue,Home.vue}
rm src/store.js
```

When you’re finished, the contents of the `src` folder should look like so:

```
.
├── App.vue
├── assets
│   ├── css
│   │   ├── loading-btn.css
│   │   └── loading.css
│   └── logo.png
├── chatkit.js
├── components
│   ├── ChatNavBar.vue
│   ├── LoginForm.vue
│   ├── MessageForm.vue
│   ├── MessageList.vue
│   ├── RoomList.vue
│   └── UserList.vue
├── main.js
├── router.js
├── store
│   ├── actions.js
│   ├── index.js
│   └── mutations.js
└── views
    ├── ChatDashboard.vue
    └── Login.vue
```

For the [loading-btn.css](https://loading.io/css/loading-btn.css) and the [loading.css](https://loading.io/css/loading.css) files, you can find them on the [loading.io](https://loading.io/button/) website. These files are not available in the npm repository, so you need to manually download them and place them in your project. Do make sure to read the documentation to get an idea on what they are and how to use the customizable loaders.

Next, we’re going to install the following dependencies:

*   [@pusher/chatkit-client](https://docs.pusher.com/chatkit/reference/javascript), a real-time client interface for the ChatKit service
*   [bootstrap-vue](https://bootstrap-vue.js.org/), a CSS framework
*   [moment](https://momentjs.com/), a date and time formatting utility
*   [vue-chat-scroll](https://www.npmjs.com/package/vue-chat-scroll), which scrolls to the bottom automatically when new content is added
*   [vuex-persist](https://www.npmjs.com/package/vuex-persist), which saves Vuex state in browser’s local storage

```
npm i @pusher/chatkit-client bootstrap-vue moment vue-chat-scroll vuex-persist
```

Do check out the links to learn more about what each package does, and how it can be configured.

Now, let’s configure our Vue.js project. Open `src/main.js` and update the code as follows:

```
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
import VueChatScroll from 'vue-chat-scroll'

import App from './App.vue'
import router from './router'
import store from './store/index'

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import './assets/css/loading.css'
import './assets/css/loading-btn.css'

Vue.config.productionTip = false
Vue.use(BootstrapVue)
Vue.use(VueChatScroll)

new Vue({
  router,
  store,
  render: h => h(App)
}).$mount('#app')
```

Update `src/router.js` as follows:

```
import Vue from 'vue'
import Router from 'vue-router'
import Login from './views/Login.vue'
import ChatDashboard from './views/ChatDashboard.vue'

Vue.use(Router)

export default new Router({
  mode: 'history',
  base: process.env.BASE_URL,
  routes: [
    {
      path: '/',
      name: 'login',
      component: Login
    },
    {
      path: '/chat',
      name: 'chat',
      component: ChatDashboard,
    }
  ]
})
```

Update `src/store/index.js`:

```
import Vue from 'vue'
import Vuex from 'vuex'
import VuexPersistence from 'vuex-persist'
import mutations from './mutations'
import actions from './actions'

Vue.use(Vuex)

const debug = process.env.NODE_ENV !== 'production'

const vuexLocal = new VuexPersistence({
  storage: window.localStorage
})

export default new Vuex.Store({
  state: {
  },
  mutations,
  actions,
  getters: {
  },
  plugins: [vuexLocal.plugin],
  strict: debug
})
```

The `vuex-persist` package ensures that our Vuex state is saved between page reloads or refreshes.

Our project should be able to compile now without errors. However, don’t run it just yet, as we need to build the user interface.

## Building the UI Interface

Let’s start by updating `src/App.vue` as follows:

```
<template>
  <div id="app">
    <router-view/>
  </div>
</template>
```

Next, we need to define our Vuex store states as they’re required by our UI components to work. We’ll do this by going to our Vuex store in `src/store/index.js`. Just update the `state` and `getters` sections as follows:

```
state: {
  loading: false,
  sending: false,
  error: null,
  user: [],
  reconnect: false,
  activeRoom: null,
  rooms: [],
  users: [],
  messages: [],
  userTyping: null
},
getters: {
  hasError: state => state.error ? true : false
},
```

These are all the state variables that we’ll need for our chat application. The `loading` state is used by the UI to determine whether it should run the CSS loader. The `error` state is used to store information of an error that has just occurred. We’ll discuss the rest of the state variables when we cross their bridges.

Next open `src/view/Login.vue` and update as follows:

```
<template>
  <div class="login">
    <b-jumbotron  header="Vue.js Chat"
                  lead="Powered by Chatkit SDK and Bootstrap-Vue"
                  bg-variant="info"
                  text-variant="white">
      <p>For more information visit website</p>
      <b-btn target="_blank" href="https://pusher.com/chatkit">More Info</b-btn>
    </b-jumbotron>
    <b-container>
      <b-row>
        <b-col lg="4" md="3"></b-col>
        <b-col lg="4" md="6">
          <LoginForm />
        </b-col>
        <b-col lg="4" md="3"></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import LoginForm from '@/components/LoginForm.vue'

export default {
  name: 'login',
  components: {
    LoginForm
  }
}
</script>
```

Next, insert code for `src/components/LoginForm.vue` as follows:

```
<template>
  <div class="login-form">
    <h5 class="text-center">Chat Login</h5>
    <hr>
    <b-form @submit.prevent="onSubmit">
       <b-alert variant="danger" :show="hasError">{{ error }} </b-alert>

      <b-form-group id="userInputGroup"
                    label="User Name"
                    label-for="userInput">
        <b-form-input id="userInput"
                      type="text"
                      placeholder="Enter user name"
                      v-model="userId"
                      autocomplete="off"
                      :disabled="loading"
                      required>
        </b-form-input>
      </b-form-group>

      <b-button type="submit"
                variant="primary"
                class="ld-ext-right"
                v-bind:class="{ running: loading }"
                :disabled="isValid">
                Login <div class="ld ld-ring ld-spin"></div>
      </b-button>
    </b-form>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  name: 'login-form',
  data() {
    return {
      userId: '',
    }
  },
  computed: {
    isValid: function() {
      const result = this.userId.length < 3;
      return result ? result : this.loading
    },
    ...mapState([
      'loading',
      'error'
    ]),
    ...mapGetters([
      'hasError'
    ])
  }
}
</script>
```

As mentioned earlier, this is an advanced tutorial. If you have trouble understanding any of the code here, please go to the prerequisites or the project dependencies for information.

We can now start the Vue dev server via `npm run serve` to ensure our application is running without any compilation issues.

![Our login UI](Images/vue-login-ui.png)

You can confirm the validation is working by entering a username. You should see the *Login* button activate after entering three characters. The *Login* button doesn’t work for now, as we haven’t coded that part. We’ll look into it later. For now, let’s continue building our chat user interface.

Go to `src/view/ChatDashboard.vue` and insert the code as follows:

```
<template>
  <div class="chat-dashboard">
    <ChatNavBar />
    <b-container fluid class="ld-over" v-bind:class="{ running: loading }">
      <div class="ld ld-ring ld-spin"></div>
      <b-row>
        <b-col cols="2">
          <RoomList />
        </b-col>

        <b-col cols="8">
          <b-row>
            <b-col id="chat-content">
              <MessageList />
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <MessageForm />
            </b-col>
          </b-row>
        </b-col>

        <b-col cols="2">
          <UserList />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import ChatNavBar from '@/components/ChatNavBar.vue'
import RoomList from '@/components/RoomList.vue'
import MessageList from '@/components/MessageList.vue'
import MessageForm from '@/components/MessageForm.vue'
import UserList from '@/components/UserList.vue'
import { mapState } from 'vuex';

export default {
  name: 'Chat',
  components: {
    ChatNavBar,
    RoomList,
    UserList,
    MessageList,
    MessageForm
  },
  computed: {
    ...mapState([
      'loading'
    ])
  }
}
</script>
```

The `ChatDashboard` will act as a layout parent for the following child components:

*   `ChatNavBar`, a basic navigation bar
*   `RoomList`, which lists rooms that the logged in user has access to, and which is also a room selector
*   `UserList`, which lists members of a selected room
*   `MessageList`, which displays messages posted in a selected room
*   `MessageForm`, a form for sending messages to the selected room

Let’s put some boilerplate code in each component to ensure everything gets displayed.

Insert boilerplate code for `src/components/ChatNavBar.vue` as follows:

```
<template>
  <b-navbar id="chat-navbar" toggleable="md" type="dark" variant="info">
    <b-navbar-brand href="#">
      Vue Chat
    </b-navbar-brand>
    <b-navbar-nav class="ml-auto">
      <b-nav-text>{{ user.name }} | </b-nav-text>
      <b-nav-item href="#" active>Logout</b-nav-item>
    </b-navbar-nav>
  </b-navbar>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'ChatNavBar',
  computed: {
    ...mapState([
      'user',
    ])
  },
}
</script>

<style>
  #chat-navbar {
    margin-bottom: 15px;
  }
</style>
```

Insert boilerplate code for `src/components/RoomList.vue` as follows:

```
<template>
  <div class="room-list">
    <h4>Channels</h4>
    <hr>
    <b-list-group v-if="activeRoom">
      <b-list-group-item v-for="room in rooms"
                        :key="room.name"
                        :active="activeRoom.id === room.id"
                        href="#"
                        @click="onChange(room)">
        # {{ room.name }}
      </b-list-group-item>
    </b-list-group>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'RoomList',
  computed: {
    ...mapState([
      'rooms',
      'activeRoom'
    ]),
  }
}
</script>
```

Insert boilerplate code for `src/components/UserList.vue` as follows:

```
<template>
  <div class="user-list">
    <h4>Members</h4>
    <hr>
    <b-list-group>
      <b-list-group-item v-for="user in users" :key="user.username">
        {{ user.name }}
        <b-badge v-if="user.presence"
        :variant="statusColor(user.presence)"
        pill>
        {{ user.presence }}</b-badge>
      </b-list-group-item>
    </b-list-group>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'user-list',
  computed: {
    ...mapState([
      'loading',
      'users'
    ])
  },
  methods: {
    statusColor(status) {
      return status === 'online' ? 'success' : 'warning'
    }
  }
}
</script>
```

Insert boilerplate code for `src/components/MessageList.vue` as follows:

```
<template>
  <div class="message-list">
    <h4>Messages</h4>
    <hr>
    <div id="chat-messages" class="message-group" v-chat-scroll="{smooth: true}">
      <div class="message" v-for="(message, index) in messages" :key="index">
        <div class="clearfix">
          <h4 class="message-title">{{ message.name }}</h4>
          <small class="text-muted float-right">@{{ message.username }}</small>
        </div>
        <p class="message-text">
          {{ message.text }}
        </p>
        <div class="clearfix">
          <small class="text-muted float-right">{{ message.date }}</small>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'message-list',
  computed: {
    ...mapState([
      'messages',
    ])
  }
}
</script>

<style>
.message-list {
  margin-bottom: 15px;
  padding-right: 15px;
}
.message-group {
  height: 65vh !important;
  overflow-y: scroll;
}
.message {
  border: 1px solid lightblue;
  border-radius: 4px;
  padding: 10px;
  margin-bottom: 15px;
}
.message-title {
  font-size: 1rem;
  display:inline;
}
.message-text {
  color: gray;
  margin-bottom: 0;
}
.user-typing {
  height: 1rem;
}
</style>
```

Insert boilerplate code for `src/components/MessageForm.vue` as follows:

```
<template>
  <div class="message-form ld-over">
    <small class="text-muted">@{{ user.username }}</small>
    <b-form @submit.prevent="onSubmit" class="ld-over" v-bind:class="{ running: sending }">
      <div class="ld ld-ring ld-spin"></div>
      <b-alert variant="danger" :show="hasError">{{ error }} </b-alert>
      <b-form-group>
        <b-form-input id="message-input"
                      type="text"
                      v-model="message"
                      placeholder="Enter Message"
                      autocomplete="off"
                      required>
        </b-form-input>
      </b-form-group>
      <div class="clearfix">
        <b-button type="submit" variant="primary" class="float-right">
          Send
        </b-button>
      </div>
    </b-form>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  name: 'message-form',
  data() {
    return {
      message: ''
    }
  },
  computed: {
    ...mapState([
      'user',
      'sending',
      'error',
      'activeRoom'
    ]),
    ...mapGetters([
      'hasError'
    ])
  }
}
</script>
```

Go over the code to ensure nothing is a mystery to you. Navigate to [http://localhost:8080/chat](http://localhost:8080/chat) to check if everything is running. Check the terminal and browser consoles to ensure there are no errors at this point. You should now have the following view.

![The blank chat dashboard](Images/chatdashboard-blank.png) 

Pretty empty, right? Let’s go to `src/store/index.js` and insert some mock data in state:

```
state: {
  loading: false,
  sending: false,
  error: 'Relax! This is just a drill error message',
  user: {
    username: 'Jack',
    name: 'Jack Sparrow'
  },
  reconnect: false,
  activeRoom: {
    id: '124'
  },
  rooms: [
    {
      id: '123',
      name: 'Ships'
    },
    {
      id: '124',
      name: 'Treasure'
    }
  ],
  users: [
    {
      username: 'Jack',
      name: 'Jack Sparrow',
      presence: 'online'
    },
    {
      username: 'Barbossa',
      name: 'Hector Barbossa',
      presence: 'offline'
    }
  ],
  messages: [
    {
      username: 'Jack',
      date: '11/12/1644',
      text: 'Not all treasure is silver and gold mate'
    },
    {
      username: 'Jack',
      date: '12/12/1644',
      text: 'If you were waiting for the opportune moment, that was it'
    },
    {
      username: 'Hector',
      date: '12/12/1644',
      text: 'You know Jack, I thought I had you figured out'
    }
  ],
  userTyping: null
},
```

After saving the file, your view should match the image below.

![Displaying mock data](Images/chat-mock-data.png) 

This simple test ensures that all components and states are all tied up together nicely. You can now revert the state code back to its original form:

```
state: {
  loading: false,
  sending: false,
  error: null,
  user: null,
  reconnect: false,
  activeRoom: null,
  rooms: [],
  users: [],
  messages: [],
  userTyping: null
}
```

Let’s start implementing concrete features, starting with the login form.

## Password-less Authentication

For this tutorial, we’ll employ a password-less non-secure authentication system. A proper, secure authentication system is outside the scope of this tutorial. To start with, we need to start building our own interface that will interact with ChatKit service via the `@pusher/chatkit-client` package.

Go back to the ChatKit dashboard and copy the *instance* and *test token* parameters. Save them in the file `.env.local` at the root of your project like this:

```
VUE_APP_INSTANCE_LOCATOR=
VUE_APP_TOKEN_URL=
VUE_APP_MESSAGE_LIMIT=10
```

I’ve also added a `MESSAGE_LIMIT` parameter. This value simply restricts the number of messages our chat application can fetch. Make sure to fill in the other parameters from the credentials tab.

Next, go to `src/chatkit.js` to start building our chat application foundation:

```
import { ChatManager, TokenProvider } from '@pusher/chatkit-client'

const INSTANCE_LOCATOR = process.env.VUE_APP_INSTANCE_LOCATOR;
const TOKEN_URL = process.env.VUE_APP_TOKEN_URL;
const MESSAGE_LIMIT = Number(process.env.VUE_APP_MESSAGE_LIMIT) || 10;

let currentUser = null;
let activeRoom = null;

async function connectUser(userId) {
  const chatManager = new ChatManager({
    instanceLocator: INSTANCE_LOCATOR,
    tokenProvider: new TokenProvider({ url: TOKEN_URL }),
    userId
  });
  currentUser = await chatManager.connect();
  return currentUser;
}

export default {
  connectUser
}
```

Notice that we’re casting the `MESSAGE_LIMIT` constant to a number, as by default the `process.env` object forces all of its properties to be of type string.

Insert the following code for `src/store/mutations`:

```
export default {
  setError(state, error) {
    state.error = error;
  },
  setLoading(state, loading) {
    state.loading = loading;
  },
  setUser(state, user) {
    state.user = user;
  },
  setReconnect(state, reconnect) {
    state.reconnect = reconnect;
  },
  setActiveRoom(state, roomId) {
    state.activeRoom = roomId;
  },
  setRooms(state, rooms) {
    state.rooms = rooms
  },
  setUsers(state, users) {
    state.users = users
  },
 clearChatRoom(state) {
    state.users = [];
    state.messages = [];
  },
  setMessages(state, messages) {
    state.messages = messages
  },
  addMessage(state, message) {
    state.messages.push(message)
  },
  setSending(state, status) {
    state.sending = status
  },
  setUserTyping(state, userId) {
    state.userTyping = userId
  },
  reset(state) {
    state.error = null;
    state.users = [];
    state.messages = [];
    state.rooms = [];
    state.user = null
  }
}
```

The code for mutations is really simple—just a bunch of setters. You’ll soon understand what each mutation function is for in the later sections. Next, update `src/store/actions.js` with this code:

```
import chatkit from '../chatkit';

// Helper function for displaying error messages
function handleError(commit, error) {
  const message = error.message || error.info.error_description;
  commit('setError', message);
}

export default {
  async login({ commit, state }, userId) {
    try {
      commit('setError', '');
      commit('setLoading', true);
      // Connect user to ChatKit service
      const currentUser = await chatkit.connectUser(userId);
      commit('setUser', {
        username: currentUser.id,
        name: currentUser.name
      });
      commit('setReconnect', false);

      // Test state.user
      console.log(state.user);
    } catch (error) {
      handleError(commit, error)
    } finally {
      commit('setLoading', false);
    }
  }
}
```

Next, update `src/components/LoginForm.vue` as follows:

```
import { mapState, mapGetters, mapActions } from 'vuex'

//...
export default {
  //...
  methods: {
    ...mapActions([
      'login'
    ]),
    async onSubmit() {
      const result = await this.login(this.userId);
      if(result) {
        this.$router.push('chat');
      }
    }
  }
}
```

You’ll have to restart the Vue.js server in order to load `env.local` data. If you see any errors regarding unused variables, ignore them for now. Once you’ve done that, navigate to [http://localhost:8080/](http://localhost:8080/) and test the login feature:

![A login error](Images/login-error.png) 

In the above example, I’ve used an incorrect username just to make sure the error handling feature is working correctly.

![A successful login](Images/login-successful.png) 

In this screenshot, I’ve used the correct username. I’ve also opened up the browser console tab to ensure that the `user` object has been populated. Better yet, if you’ve installed [Vue.js Dev Tools in Chrome](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/), you should be able to see more detailed information.

![More detailed login information](Images/login-vuex-plugin.png) 

If everything’s working correctly for you at this point, move on to the next step.

## Subscribing to a Room

Now that we’ve successfully verified that the login feature works, we need to redirect users to the `ChatDashboard` view. The code `this.$router.push('chat');` does this for us. However, our action `login` needs to return a Boolean to determine when it’s okay to navigate to the `ChatDashboard` view. We also need to populate the `RoomList` and `UserList` components with actual data from the ChatKit service.

Update `src/chatkit.js` as follows:

```
//...
import moment from 'moment'
import store from './store/index'

//...
function setMembers() {
  const members = activeRoom.users.map(user => ({
    username: user.id,
    name: user.name,
    presence: user.presence.state
  }));
  store.commit('setUsers', members);
}

async function subscribeToRoom(roomId) {
  store.commit('clearChatRoom');
  activeRoom = await currentUser.subscribeToRoom({
    roomId,
    messageLimit: MESSAGE_LIMIT,
    hooks: {
      onMessage: message => {
        store.commit('addMessage', {
          name: message.sender.name,
          username: message.senderId,
          text: message.text,
          date: moment(message.createdAt).format('h:mm:ss a D-MM-YYYY')
        });
      },
      onPresenceChanged: () => {
        setMembers();
      },
      onUserStartedTyping: user => {
        store.commit('setUserTyping', user.id)
      },
      onUserStoppedTyping: () => {
        store.commit('setUserTyping', null)
      }
    }
  });
  setMembers();
  return activeRoom;
}

export default {
  connectUser,
  subscribeToRoom
}
```

If you look at the `hooks` section, we have event handlers used by the ChatKit service to communicate with our client application. You can find the full documentation [here](https://docs.pusher.com/chatkit/reference/javascript). I’ll quickly summarize the purpose of each hook method:

*   `onMessage` receives messages
*   `onPresenceChanged` receives an event when a user logs in or out
*   `onUserStartedTyping` receives an event that a user is typing
*   `onUserStoppedTyping` receives an event that a user has stopped typing

For the `onUserStartedTyping` to work, we need to emit a typing event from our `MessageForm` while a user is typing. We’ll look into this in the next section.

Update the `login` function in `src/store/actions.js` with the following code:

```
//...
try {
  //... (place right after the `setUser` commit statement)
  // Save list of user's rooms in store
  const rooms = currentUser.rooms.map(room => ({
    id: room.id,
    name: room.name
  }))
  commit('setRooms', rooms);

  // Subscribe user to a room
  const activeRoom = state.activeRoom || rooms[0]; // pick last used room, or the first one
  commit('setActiveRoom', {
    id: activeRoom.id,
    name: activeRoom.name
  });
  await chatkit.subscribeToRoom(activeRoom.id);

  return true;
} catch (error) {
  //...
}
```

After you’ve saved the code, go back to the login screen and enter the correct username. You should be taken to the following screen.

![The current chat dashboard](Images/chatdashboard.png) 

Nice! Almost all the components are working without additional effort since we wired them up properly to the Vuex store. Try sending a message via ChatKit’s dashboard console interface. Create a message and post it to the `General` room. You should see the new messages pop up automatically in the `MessageList` component. Soon, we’ll implement the logic for sending messages from our Vue.js app.

### If You Experience Issues

In case you’re experiencing issues, try the following:

*   restart the Vue.js server
*   clear your browser cache
*   do a hard reset/refresh (available in Chrome if the *Console* tab is open and you hold the *Reload* button for five seconds)
*   clear localStorage using your browser console

If everything is running okay up to this point, continue with the next section, where we implement logic for changing rooms.

## Changing Rooms

This part is quite simple, since we’ve already laid out the foundation. First, we’ll create an `action` that will allow users to change rooms. Go to `src/store/actions.js` and add this function right after the `login` action handler:

```
async changeRoom({ commit }, roomId) {
  try {
    const { id, name } = await chatkit.subscribeToRoom(roomId);
    commit('setActiveRoom', { id, name });
  } catch (error) {
    handleError(commit, error)
  }
},
```

Next, go to `src/componenents/RoomList.vue` and update the script section as follows:

```
import { mapState, mapActions } from 'vuex'
//...
export default {
  //...
  methods: {
    ...mapActions([
      'changeRoom'
    ]),
    onChange(room) {
      this.changeRoom(room.id)
    }
  }
}
```

If you recall, we’ve already defined `@click="onChange(room)"` in the `b-list-group-item` element. Let’s test out this new feature by clicking the items in the `RoomList` component.

![Changing chat rooms](Images/change-room.png) 

Your UI should update with each click of the room. The `MessageList` and `UserList` component should display the correct information for the selected room. For the next section, we’ll implement multiple features at once.

## Reconnecting the User After a Page Refresh

You may have noticed that, when you do some changes to `store/index.js`, or you do a page refresh, you get the following error: `Cannot read property 'subscribeToRoom' of null`. This happens because the state of your application gets reset. Luckily, the `vuex-persist` package maintains our Vuex state between page reloads by saving it in the browser’s local storage.

Unfortunately, the references that connect our app to the ChatKit server are reset back to null. To fix this, we need to perform a reconnect operation. We also need a way to tell our app that a page reload has just happened and that our app needs to reconnect in order to continue functioning properly. We’ll implement this code in `src/components/ChatNavbar.vue`. Update the script section as follows:

```
<script>
import { mapState, mapActions, mapMutations } from 'vuex'

export default {
  name: 'ChatNavBar',
  computed: {
    ...mapState([
      'user',
       'reconnect'
    ])
  },
  methods: {
    ...mapActions([
      'logout',
      'login'
    ]),
    ...mapMutations([
      'setReconnect'
    ]),
    onLogout() {
      this.$router.push({ path: '/' });
      this.logout();
    },
    unload() {
      if(this.user.username) { // User hasn't logged out
        this.setReconnect(true);
      }
    }
  },
  mounted() {
    window.addEventListener('beforeunload', this.unload);
    if(this.reconnect) {
      this.login(this.user.username);
    }
  }
}
</script>
```

Let me break down the sequence of events so that you can understand the logic behind reconnecting to the ChatKit service:

1.  `unload`. When a page refresh occurs, this method gets called. It checks first the state `user.username` has been set. If it has, it means the user has not logged out. The state `reconnect` is set to true.
2.  `mounted`. This method gets called every time `ChatNavbar.vue` has just finished rendering. It first assigns a handler to an event listener that gets called just before the page unloads. It also does a check if `state.reconnect` has been set to true. If so, then the login procedure is executed, thus reconnecting our chat application back to our ChatKit service.

I’ve also added a `Logout` feature, which we’ll look into later.

After making these changes, try refreshing the page. You’ll see the page update itself automatically as it does the reconnection process behind the scenes. When you switch rooms, it should work flawlessly.

## Sending Messages, Detecting User Typing and Logging Out

Let’s start with implementing these features in `src/chatkit.js` by adding the following code:

```
//...
async function sendMessage(text) {
  const messageId = await currentUser.sendMessage({
    text,
    roomId: activeRoom.id
  });
  return messageId;
}

export function isTyping(roomId) {
  currentUser.isTypingIn({ roomId });
}

function disconnectUser() {
  currentUser.disconnect();
}

export default {
  connectUser,
  subscribeToRoom,
  sendMessage,
  disconnectUser
}
```

While the functions `sendMessage` and `disconnectUser` will be bundled in ChatKit’s module export, `isTyping` function will be exported separately. This is to allow `MessageForm` to directly send typing events without involving the Vuex store.

For `sendMessage` and `disconnectUser`, we’ll need to update the store in order to cater for things like error handling and loading status notifications. Go to `src/store/actions.js` and insert the following code right after the `changeRoom` function:

```
async sendMessage({ commit }, message) {
  try {
    commit('setError', '');
    commit('setSending', true);
    const messageId = await chatkit.sendMessage(message);
    return messageId;
  } catch (error) {
    handleError(commit, error)
  } finally {
    commit('setSending', false);
  }
},
async logout({ commit }) {
  commit('reset');
  chatkit.disconnectUser();
  window.localStorage.clear();
}
```

For the `logout` function, we call `commit('reset')` to reset our store back to its original state. It’s a basic security feature to remove user information and messages from the browser cache.

Let’s start by updating the form input in `src/components/MessageForm.vue` to emit typing events by adding the `@input` directive:

```
<b-form-input id="message-input"
              type="text"
              v-model="message"
              @input="isTyping"
              placeholder="Enter Message"
              autocomplete="off"
              required>
</b-form-input>
```

Let’s now update the script section for `src/components/MessageForm.vue` to handle message sending and emitting of typing events. Update as follows:

```
<script>
import { mapActions, mapState, mapGetters } from 'vuex'
import { isTyping } from '../chatkit.js'

export default {
  name: 'message-form',
  data() {
    return {
      message: ''
    }
  },
  computed: {
    ...mapState([
      'user',
      'sending',
      'error',
      'activeRoom'
    ]),
    ...mapGetters([
      'hasError'
    ])
  },
  methods: {
    ...mapActions([
      'sendMessage',
    ]),
    async onSubmit() {
      const result = await this.sendMessage(this.message);
      if(result) {
        this.message = '';
      }
    },
     async isTyping() {
      await isTyping(this.activeRoom.id);
    }
  }
}
</script>
```

And in `src/MessageList.vue`:

```
import { mapState } from 'vuex'

export default {
  name: 'message-list',
  computed: {
    ...mapState([
      'messages',
      'userTyping'
    ])
  }
}
```

The send message feature should now work. In order to display a notification that another user is typing, we need to add an element for displaying this information. Add the following snippet in the template section of `src/components/MessageList.vue`, right after the `message-group` div:

```
<div class="user-typing">
  <small class="text-muted" v-if="userTyping">@{{ userTyping }} is typing....</small>
</div>
```

To test out this feature, simply log in as another user using a different browser and start typing. You should see a notification appear on the other user’s chat window.

![A notification in another user’s chat window](Images/send-message-user-type.png) 

Let’s finish this tutorial by implementing the last feature, `logout`. Our Vuex store already has the necessary code to handle the logout process. We just need to update `src/components/ChatNavBar.vue`. Simply link the `Logout` button with function handler `onLogout` that we had specified earlier:

```
 <b-nav-item href="#" @click="onLogout" active>Logout</b-nav-item>
```

That’s it. You can now log out and log in again as another user.

![Switching between member accounts](Images/logout-login.png) 

## Summary

We’ve now come to the end of the tutorial. The ChatKit API has enabled us to rapidly build a chat application in a short time. If we were to build a similar application from scratch, it would take us several weeks, since we’d have to flesh out the back end as well. The great thing about this solution is that we don’t have to deal with hosting, managing databases and other infrastructure issues. We can simply build and deploy the front-end code to client devices on web, Android and IOS platforms.

Please do take a look at the documentation, as there’s a ton of back-end features I wasn’t able to show you in this tutorial. Given time, you can easily build a full-featured chat application that can rival popular chat products like Slack and Discord.

# Chapter 4: Building a Vue Front End for a Headless CMS

### by Michael Wanyoike

In this guide, we’ll learn how to build a modern blog website using Vue.js and [GraphCMS](https://graphcms.com/), a headless CMS platform.

If you’re looking to start a quick blog today, my recommendation is to go straight to WordPress.

But what if you’re a media powerhouse and you want to deliver your content as fast as possible to multiple devices? You’ll probably also need to integrate your content with ads and other third-party services. Well, you could do that with WordPress, but you’ll come across a few problems with that platform.

1.  You’ll need to install a plugin to implement additional features. The more plugins you install, the slower your website becomes.
2.  PHP is quite slow compared to most JavaScript web frameworks. From a developer’s perspective, it’s much easier and faster to implement custom features on a JavaScript-powered front end.

[JavaScript offers superior performance to PHP in browser loading tests](https://www.hostingadvice.com/blog/comparing-node-js-vs-php-performance/). In addition, modern JavaScript and its ecosystem provides a far more pleasant development experience when it comes to building new web experiences fast.

So there’s been a growth of **headless CMS** solutions—which are simply back ends for managing content. With this approach, developers can focus on building fast and interactive front ends using a JavaScript framework of their choice. Customizing a JavaScript-powered front end is much easier than making changes on a WordPress site.

GraphCMS differs from most Headless CMS platforms in that, instead of delivering content via REST, it does so via GraphQL. This new technology is superior to REST, as it allows us to construct queries that touch on data belonging to multiple models in a single request.

Consider the following model schema:

**Post**

*   id: Number
*   title: String
*   content : String
*   comments : array of Comments

**Comment**

*   id: Number
*   name: String
*   message: String

The above models have a one(Post)-to-many(Comments) relationship. Let’s see how we can fetch a single Post record attached with all linked Comment records.

If the data is in a relational database, you have to construct either one inefficient SLQ statement, or two SQL statements for fetching the data cleanly. If the data is stored in a NoSQL database, you can use a modern ORM like [Vuex ORM](https://vuex-orm.github.io) to fetch the data easily for you, like this:

```
const post = Post.query()
  .with('comments')
  .find(1);
```

Quite simple! You can easily pass this data via REST to the intended client. But here’s the problem: whenever the data requirement changes at the client end, you’ll be forced to go back to your back-end code to either update your existing API endpoint, or create a new one that provides the required data set. This back and forth process is tiring and repetitive.

What if, at the client level, you could just ask for the data you need and the back end will provide it for you, without you doing extra work? Well, that’s what GraphQL is for.

## Prerequisites

Before we begin, I’d like to note that this is a guide for intermediate to advanced users. I won’t be going over the basics, but rather will show you how to quickly build a Vue.js blog using GraphCMS as the back end. You’ll need to be proficient in the following areas:

*   ES6 and ES7 JavaScript
*   Vue.js (using CLI version 3)
*   GraphQL

That’s all you need to know to get started with this tutorial. Also, a background in using REST will be great, as I’ll be referencing this a lot. If you’d like a refresher, this article might help: “[REST 2.0 Is Here and Its Name Is GraphQL](https://www.sitepoint.com/rest-2-0-graphql/)”.

## About the Project

We’ll build a very simple blog application with a basic comment system. Below are the links you can visit to check out the completed project:

*   [CodeSandbox.io demo](https://codesandbox.io/s/01zo6v221p)
*   [GitHub repo](https://github.com/sitepoint-editors/vue-axios-graphcsms)

Please note that a READ-ONLY token has been used in the demo and consequently the comments system won’t work. You’ll need to supply your OPEN permission token and endpoint as per the instructions in this tutorial for it to work.

## Create GraphCMS Project Database

Head over to the [GraphCMS](https://graphcms.com/) website and click the “Start Building for Free” button. You’ll be taken to their signup page.

![Signing up to GraphCMS](Images/graphcms-signup.png) 

Sign up using your preferred method. Once you’ve completed the account authentication and verification process, you should be able to access the main dashboard.

![The GraphCMS main dashboard](Images/graphcms-dashboard.png) 

In the above example, I’ve already created a project called “BlogDB”. Go ahead and create a new one, and call it whatever you want. After you’ve entered the name, you can leave the rest of the fields in their defaults. Click *Create* and you’ll be taken to their project plan.

![GraphCMS plans](Images/graphcms-project-plan.png) 

For the purposes of this tutorial, select the free Developer plan then click *Continue*. You’ll be taken to the project’s dashboard, which looks something like this:

![The GraphCMS project dashboard](Images/graphcms-project-dashboard.png) 

Go to the *Schema* tab. We’re going to create the following models, each with the following fields:

**Category**

*   name: Single line text, required, unique

**Post**

*   slug: Single line text, required, unique
*   title: Single line text, required, unique
*   content: Multi line text

**Comment**

*   name: Single line text, required
*   message: Multi line text, required

Use the *Create Model* button to create models. On the right side, you should find a hidden panel for Fields, which is activated by clicking the *Fields* button. Drag the appropriate field type onto the model’s panel. You will be presented with a form to fill in your field’s attributes. Do note at the bottom there’s a pink button labeled *Advanced*. Clicking it will expand the panel to give you more field attributes you can enable.

![Field attributes in the Advanced tab](Images/graphcms-models-fields.png) 

Next, you’ll need to add the relationship between models as follows:

*   Post > Categories (many-to-many)
*   Post > Comments (one-to-many)

Use the *Reference* field to define this relationship. You can add this field to any side; GraphCMS will automatically create the opposite relation field in the referenced model. When you’ve completed defining the models, you should have something like this:

![GraphCMS models](Images/GraphCMS-fields.jpg) 

You’ve now completed the first part. Let’s now provide some data to our models.

## GraphQL Data Migration

To add content to your models, you can simply click the *Content* tab in the project dashboard where you can create new records for each of your models. However, if you find this to be a slow method, you’ll be happy to know that I’ve created a GraphCMS migration tool that copies data from CSV files and uploads them to your GraphCMS database. You can find the project here in this [GitHub repository](https://github.com/sitepoint-editors/graphcsms-data-migration). To start using the project, simply download it into your workspace like this:

```
git clone git@github.com:sitepoint-editors/graphcsms-data-migration.git
cd graphcsms-data-migration
npm install
```

Next, you’ll need to grab your GraphCMS project’s API endpoint and token from the dashboard’s *Settings* page. You’ll need to create a new token. For the permission level, use OPEN, as this will allow the tool to perform READ and WRITE operations on your GraphCMS database. Create a file called `.env` and put it at the root of the project:

```
ENDPOINT=<Put api endpoint here>
TOKEN=<Put token with OPEN permission here>
```

Next, you may need to populate the CSV files in the data folder with your own. Here’s some sample data that has been used:

```
// Categories.csv
name
Featured
Food
Fashion
Beauty

// Posts.csv
title,slug,content,categories
Food Post 1,food-post-1,Breeze through Thanksgiving by making this Instant Pot orange cranberry sauce,Food|Featured
Food Post 2,food-post-2,This is my second food post,Food
Food Post 3,food-post-3,This is my last and final food post,Food
Fashion Post 1,fashion-post-1,This is truly my very first fashion post,Fashion|Featured
Fashion Post 2,fashion-post-2,This is my second fashion post,Fashion
Fashion Post 3,fashion-post-3,This is my last and final fashion post,Fashion
Beauty Post 1,Beauty-post-1,This is truly my very first Beauty post,Beauty|Featured
Beauty Post 2,Beauty-post-2,This is my second beauty post,Beauty
```

You can change the content if you want. Make sure not to touch the top row, as otherwise you’ll change the field names. Please note, for the column `categories`, I’ve used the pipe `|` character as a delimiter.

To upload the CSV data to your GraphCMS database, execute the following commands in this order:

```
npm run categories
npm run posts
```

Each script will print out records that have uploaded successfully. The reason we uploaded `categories` first is so that the `posts` records can link successfully to existing `category` records.

If you want to clean out your database, you can run the following command:

```
npm run reset
```

This script will delete all your model’s contents. You’ll get a report indicating how many records were deleted for each model.

I hope you find the tool handy. Go back to the dashboard to confirm that data for the `Posts` and `Categories` have successfully been uploaded.

With the back end taken care of, let’s start building our front-end blog interface.

## Building the Blog’s Front End Using Vue.js

As mentioned earlier, we are going to build a very simple blog application powered by a GraphCMS database back end. Launch a terminal and navigate to your workspace.

If you haven’t got Vue CLI installed, do that now:

```
npm install -g @vue/cli
```

Then create a new project:

```
vue create vue-graphcms
```

Choose to manually select features, then select the following options:

*   Features: Babel, Router
*   Router History Mode: Y
*   ESLint with error prevention only
*   Lint on save
*   Config file placement: Dedicated Config Files
*   Save preset: your choice

Once the project creation process is complete, change into the project directory and install the following dependencies:

```
npm install bootstrap-vue axios
```

To set up `Bootstrap-Vue` in our project, simply open `src/main.js` and add the following code:

```
import BootstrapVue from "bootstrap-vue";
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";

Vue.config.productionTip = false;
Vue.use(BootstrapVue);
```

Next, we need to start laying down our project structure. In the `src/components` folder, delete the existing files and create these new ones:

*   `CommentForm.vue`
*   `CommentList.vue`
*   `Post.vue`
*   `PostList.vue`

In the `src/views` folder, delete `About.vue` and create a new file called `PostView.vue`. As seen from the demo, we’ll have several category pages each displaying a list of posts filtered by category. Technically, there will only be one page that will display a different list of posts based on an active route name. The `PostList` component will filter posts based on the current route.

Let’s first set up the routes. Open `src/router.js` and replace the existing code with this:

```
import Vue from "vue";
import Router from "vue-router";
import Home from "./views/Home.vue";
import Post from "./views/PostView.vue";

Vue.use(Router);

export default new Router({
  mode: "history",
  base: process.env.BASE_URL,
  linkActiveClass: "active",
  routes: [
    {
      path: "/",
      name: "Featured",
      component: Home
    },
    {
      path: "/food",
      name: "Food",
      component: Home
    },
    {
      path: "/fashion",
      name: "Fashion",
      component: Home
    },
    {
      path: "/beauty",
      name: "Beauty",
      component: Home
    },
    {
      path: "/post/:slug",
      name: "Post",
      component: Post
    }
  ]
});
```

Now that we have our routes, let’s set up our navigation menu. Open `src/App.vue` and replace the existing code with this:

```
<template>
  <div id="app">
    <b-navbar toggleable="md" type="dark" variant="info">
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand href="#">GraphCMS Vue</b-navbar-brand>
      <b-collapse is-nav id="nav_collapse">
        <b-navbar-nav>
          <router-link  class="nav-link" to="/" exact>Home</router-link>
          <router-link  class="nav-link" to="/food">Food</router-link>
          <router-link  class="nav-link" to="/fashion">Fashion</router-link>
          <router-link  class="nav-link" to="/beauty">Beauty</router-link>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    <b-container>
      <router-view/>
    </b-container>
  </div>
</template>
```

This will add a nav bar to the top of our site with links to our different categories.

Save the file and update the following files accordingly:

**src/views/Home.vue**

```
<template>
  <div class="home">
    <PostList />
  </div>
</template>

<script>
import PostList from "@/components/PostList.vue";

export default {
  name: "home",
  components: {
    PostList
  }
};
</script>
```

**src/components/PostList.vue**

```
<template>
  <section class="post-list">
    <h1>{{ category }} Articles</h1>
    <hr/>
    <p>Put list of posts here!</p>
  </section>
</template>

<script>
export default {
  name: "PostList",
  data() {
    return {
      category: ""
    };
  },
  created() {
    this.category = this.$route.name;
  },
  watch: {
    $route() {
      this.category = this.$route.name;
    }
  }
};
</script>
```

Notice that, in the `PostList` component, we’re using a custom [watcher](https://it.vuejs.org/v2/guide/computed.html#Watchers) to update our `category` data property, based on our current URL.

Now we’re ready to perform a quick test to confirm the routes are working. Spin up the Vue.js server using the command `npm run serve`. Open a browser at [localhost:8080](http://localhost:8080) and test each navigation link. The `category` property should output the same value we defined in route name’s attribute.

![A page view of our app](Images/vue-scaffold.png) 

## Pulling in Data From GraphCMS

Now that we have our routing code working, let’s see how we can pull information from our GraphCMS back end. At the root of your project, create an `env.local` file and populate it with values for the following fields:

```
VUE_APP_ENDPOINT=
VUE_APP_TOKEN=
```

Do note that Vue.js single-page applications only load custom environment variables starting with `VUE_APP`. You can find the API endpoint and token from your GraphCMS dashboard settings page. For the token, make sure to create one with OPEN permission, as that will allow both READ and WRITE operations. Next, create the file `src/graphcms.js` and copy the following code:

```
import axios from "axios";

export const ENDPOINT = process.env.VUE_APP_ENDPOINT;
const TOKEN = process.env.VUE_APP_TOKEN;

const headers = {
  "Content-Type": "application/json",
  Authorization: `Bearer ${TOKEN}`
};

export const apiClient = axios.create({
  headers
});

export const POSTS_BY_CATEGORY_QUERY = `
  query PostsByCategory($category: String!){
    category(where: {
      name: $category
    }
    ){
      name,
      posts {
        id
        slug
        title
        content
        categories {
          name
        }
      }
    }
  }
`;

export const POST_BY_SLUG_QUERY = `
  query PostBySlug($slug: String!){
    post(where: {
      slug: $slug
    })
    {
      id
      title
      content
      categories {
        name
      }
      comments {
        name
        message
      }
    }
  }
`;

export const CREATE_COMMENT_MUTATION = `
  mutation CreateComment($post: PostWhereUniqueInput!, $name: String!, $message: String!){
    createComment(data: {
      name: $name,
      message: $message,
      post: {
        connect: $post
      },
      status: PUBLISHED
    })
    {
      id
      name
      message
    }
  }
`;
```

This helper file we just created provides two main functions:

*   It creates an instance of axios that’s configured to perform authorized requests to your GraphCMS back end.
*   It contains GraphQL queries and mutations used in this project. These are responsible for fetching posts (either by category or by slug), as well as for creating new comments. If you’d like to find out more about GraphQL queries and mutations, [please consult the GraphQL docs](https://graphql.org/learn/queries/).

You can also use the API explorer in your project dashboard to test out these queries and mutations. To do this, copy the query or mutation from the code above and paste it into the top window of the API explorer. Enter any query variables in the window below that, then hit the *Play* button. You should see the results in a new pane on the right.

Here’s a query example:

![A GraphCMS query example](Images/graphms-query-example.png) 

Here’s a mutation example:

![A GraphCMS mutation example](Images/graphcsms-mutation-example.png) 

## Displaying the Data in a Template

Now, let’s create our HTML template in our `src/components/PostList.vue` that will display a list of posts in a neat way. We’ll also add the axios code that will pull in `posts` data from our GraphCMS database:

```
<template>
  <section class="post-list">
    <h1>{{ category }} Articles</h1>
    <hr/>
    <b-row v-if="loading">
      <b-col class="text-center">
        <div class="lds-dual-ring"></div>
      </b-col>
    </b-row>
    <div v-if="!loading" >
      <b-card tag="article" v-for="post in posts" :key="post.id" :title="post.title" :sub-title="post.categories.map(cat => cat.name).toString()">
        <p class="card-text">
          {{ post.content }}
        </p>
        <router-link class="btn btn-primary" :to="'post/' + post.slug">
          Read Post
        </router-link>
      </b-card>
    </div>
  </section>
</template>

<script>
import { ENDPOINT, apiClient, POSTS_BY_CATEGORY_QUERY } from "../graphcms.js";

export default {
  name: "PostList",
  data() {
    return {
      category: "",
      loading: false,
      posts: []
    };
  },
  methods: {
    async fetchPosts() {
      try {
        this.loading = true;
        const response = await apiClient.post(ENDPOINT, {
          query: POSTS_BY_CATEGORY_QUERY,
          variables: {
            category: this.category
          }
        });

        const body = await response.data.data;
        this.posts = await body.category.posts;
        this.loading = false;
      } catch (error) {
        console.log(error);
      }
    }
  },
  created() {
    this.category = this.$route.name;
    this.fetchPosts();
  },
  watch: {
    $route() {
      this.category = this.$route.name;
      this.posts = [];
      this.fetchPosts();
    }
  }
};
</script>

<style>
h1{
  margin-top: 25px !important;
}
.lds-dual-ring {
  display: inline-block;
  width: 64px;
  height: 64px;
}
.lds-dual-ring:after {
  content: " ";
  display: block;
  width: 46px;
  height: 46px;
  margin: 1px;
  border-radius: 50%;
  border: 5px solid #ccc;
  border-color: #ccc transparent #ccc transparent;
  animation: lds-dual-ring 1.2s linear infinite;
}
@keyframes lds-dual-ring {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
```

Let’s quickly go through the code’s main features:

*   **Loading**. When a request is made, a loading spinner is displayed to indicate to the user there’s something in progress. When the request is fulfilled, the loading spinner is replaced with a list of posts.
*   **Query**. In order to get a list of posts by category, I found it easier to query for the category, then use the category-to-posts relationship to get access to the filtered posts.
*   **Created**. When the page is loaded for the first time, the `fetchPosts()` function is called from within the `created` lifecycle hook.
*   **Watch**. When the route URL changes, the `fetchPosts()` function is called each time.

After making those changes, you should now have the following view:

![Our post list](Images/vue-post-list.png) 

## Displaying an Individual Post

Make sure the top main navigation is working as expected. Let’s now work on the `Post` component. It will have its own `fetchPost()` function, where it will query by `slug`. If you’re wondering where the `slug` parameter is coming from, let me remind you of this bit of code we put in `router.js`:

```
//...
{
  path: '/post/:slug',
  name: 'Post',
  component: Post
},
//...
```

This states that anything that comes after `/post/` in the URL is available to us in the component as `this.$route.params.slug`.

The `post` component is a parent of the `CommentForm` and `CommentList` components. The `comments` data will be passed as props to the `CommentList` component from the Posts record. Let’s insert code for `src/components/CommentList.vue` now:

```
<template>
  <section class="comment-list">
    <hr/>
    <h4 class="text-muted">Comments</h4>
    <b-card v-for="comment in comments" :title="comment.name" title-tag="h5" :key="comment.id">
      <p class="card-text text-muted">{{ comment.message }}  </p>
    </b-card>
    <p v-if="comments.length === 0" class="text-center text-muted">No comments posted yet!</p>
  </section>
</template>

<script>
export default {
  name: "CommentsList",
  props: ["comments"]
};
</script>
```

Unless you’ve manually entered comments via the GraphCMS dashboard, don’t expect to see any results just yet. Let’s add code to `src/components/CommentForm.vue` that will enable users to add comments to a blog post:

```
<template>
  <section class="comment-form">
    <h4 class="text-muted">Comment Form</h4>
    <b-form @submit.prevent="onSubmit">
      <b-form-group label="Name">
        <b-form-input id="input-name" type="text" v-model="name" placeholder="Enter your name" required></b-form-input>
      </b-form-group>
       <b-form-group label="Message">
         <b-form-textarea id="input-message" v-model="message" placeholder="Enter your comment" :rows="3" :max-rows="6" required>
         </b-form-textarea>
      </b-form-group>
      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
  </section>
</template>

<script>
import { apiClient, ENDPOINT, CREATE_COMMENT_MUTATION } from "../graphcms.js";

export default {
  name: "CommentForm",
  props: ["post"],
  data() {
    return {
      name: "",
      message: ""
    };
  },
  methods: {
    async onSubmit() {
      const formattedComment = {
        name: this.name,
        message: this.message,
        post: {
          id: this.post.id
        }
      };
      try {
        const response = await apiClient.post(ENDPOINT, {
          query: CREATE_COMMENT_MUTATION,
          variables: formattedComment
        });

        const body = await response.data.data;
        const newComment = body.createComment;
        this.post.comments.push(newComment);
        this.name = "";
        this.message = "";
      } catch (error) {
        console.log(error);
      }
    }
  }
};
</script>

<style>
  .comment-form {
    margin-top: 35px;
  }
</style>
```

We now have a basic comment form capable of submitting a new comment to our GraphQL back-end system. Once the new comment is saved, we’ll take the returned object and add it to the `post.comments` array. This should trigger the `CommentList` component to display the newly added `Comment`.

Let’s now build the `src/components/Post.vue` component:

```
<template>
  <section class="post">
    <b-row v-if="loading">
      <b-col>
        <div class="lds-dual-ring text-center"></div>
      </b-col>
    </b-row>
   <b-row v-if="!loading">
     <b-col>
      <h1>{{post.title}}</h1>
      <h4 class="text-muted">{{post.categories.map(cat => cat.name).toString()}}</h4>
      <hr>
      <p>{{ post.content }}</p>
     </b-col>
   </b-row>
   <!-- List of comments -->
   <b-row v-if="!loading">
     <b-col>
       <CommentList :comments="post.comments" />
     </b-col>
   </b-row>
   <!-- Comment form -->
    <b-row v-if="!loading">
     <b-col>
      <CommentForm :post="post" />
     </b-col>
   </b-row>
  </section>
</template>

<script>
import { ENDPOINT, apiClient, POST_BY_SLUG_QUERY } from "../graphcms.js";
import CommentList from "@/components/CommentList";
import CommentForm from "@/components/CommentForm";

export default {
  name: "Post",
  components: {
    CommentList,
    CommentForm
  },
  data() {
    return {
      loading: false,
      slug: "",
      post: {}
    };
  },
  methods: {
    async fetchPost() {
      try {
        this.loading = true;
        const response = await apiClient.post(ENDPOINT, {
          query: POST_BY_SLUG_QUERY,
          variables: {
            slug: this.slug
          }
        });

        const body = await response.data.data;
        this.post = body.post;
        this.loading = false;
      } catch (error) {
        console.log(error);
      }
    }
  },
  created() {
    this.slug = this.$route.params.slug;
    this.fetchPost();
  }
};
</script>
```

Finally, here’s the code for `src/views/PostView.vue` to tie everything together:

```
<template>
  <div class="post-view">
    <Post/>
  </div>
</template>

<script>
import Post from "@/components/Post.vue";

export default {
  name: "PostView",
  components: {
    Post
  }
};
</script>
```

You should now have the following view for Posts. Take note of the `:slug` at the end of the URL `localhost:8080/post/fashion-post-1`:

![Post comments](Images/vue-post-comments.png) 

In the above example, I’ve added a couple of comments to test out the new feature. Make sure you do the same on yours.

## Summary

I hope you’ve seen how easy it is to build a blog website using Vue.js and GraphQL. If you’d been using plain PHP and MySQL, you’d have written much more code. Even with a PHP framework, you still would have written more code for a simple blog application.

For the sake of this tutorial, I had to keep things as simple as possible. You may note that this blog project is far from even meeting a minimalistic blog setup. There are several things we haven’t tackled, such as error handling, form validation and caching. For the last bit, I recommend [Apollo Client](https://www.npmjs.com/package/apollo-client), as it has mechanisms for caching GraphQL query results. Then of course there needs to be an author model, and a proper comments system that supports authentication and message approval.

If you’re up to it, please go ahead and take this simple Vue.js GraphCMS blog even further.

# Chapter 5: How to Build a Chrome Extension with Vue

### by James Hibbard

Browser extensions are small programs that can modify and enhance the functionality of a web browser. They can be used for a variety of tasks, such as blocking ads, managing passwords, organizing tabs, altering the look and behavior of web pages, and much more.

The good news is that browser extensions aren’t difficult to write. They can be created using the web technologies you’re already familiar with—HTML, CSS and JavaScript—just like a regular web page. However, unlike regular web pages, extensions have access to a number of browser-specific APIs, and this is where the fun begins.

In this tutorial, I’m going to show you how to build a simple extension for Chrome, which alters the behavior of the new tab page. For the JavaScript part of the extension, I’ll be using the Vue.js framework, as [it will allow us to get up and running quickly](https://www.sitepoint.com/replace-jquery-vue/) and is a lot of fun to work with.

#### Tutorial Code

The code for this tutorial can be found on [GitHub](https://github.com/sitepoint-editors/dad-joke-chrome-extension).

## The Basics of a Chrome Extension

The core part of any Chrome extension is a [manifest file](https://developer.chrome.com/extensions/manifest) and a [background script](https://developer.chrome.com/extensions/background_pages). The manifest file is in a JSON format and provides important information about an extension, such as its version, resources, or the permissions it requires. A background script allows the extension to react to specific browser events, such as the creation of a new tab.

To demonstrate these concepts, let’s start by writing a “Hello, World!” Chrome extension.

Make a new folder called `hello-world-chrome` and two files: `manifest.json` and `background.js`:

```
mkdir hello-world-chrome
cd hello-world-chrome
touch manifest.json background.js
```

Open up `manifest.json` and add the following code:

```
{
  "name": "Hello World Extension",
  "version": "0.0.1",
  "manifest_version": 2,
  "background": {
    "scripts": ["background.js"],
    "persistent": false
  }
}
```

The `name`, `version` and `manifest_version` are all required fields. The `name` and `version` fields can be whatever you want; the [manifest version](https://developer.chrome.com/extensions/manifestVersion) should be set to 2 (as of Chrome 18).

The `background` key allows us to register a background script, listed in an array after the `scripts` key. The `persistent` key should be set to `false` unless the extension uses [chrome.webRequest API](https://developer.chrome.com/extensions/webRequest) to block or modify network requests.

Now let’s add the following code to `background.js` to make the browser say hello when the extension is installed:

```
chrome.runtime.onInstalled.addListener(() => {
  alert('Hello, World!');
});
```

Finally, let’s install the extension. Open Chrome and enter `chrome://extensions/` in the address bar. You should see a page displaying the extensions you’ve installed.

As we want to install our extension from a file (and not the Chrome Web Store) we need to activate *Developer mode* using the toggle in the top right-hand corner of the page. This should add an extra menu bar with the option *Load unpacked*. Click this button and select the `hello-world-chrome` folder you created previously. Click *Open* and you should see the extension installed and a “Hello, World!” popup appear.

![Hello World Extension](Images/chrome-ext-1.jpg)

Congratulations! You just made a Chrome extension.

## Overriding Chrome’s New Tab Page

The next step will to have our extension greet us when we open up a new tab. We can do this by making use of the [Override Pages API](https://developer.chrome.com/extensions/override).

#### Disable Other Extensions

Before you progress, please make sure to disable any other extensions which override Chrome’s new tab page. Only one extension at a time may alter this behavior.

We’ll start off by creating a page to display instead of the new tab page. Let’s call it `tab.html`. This should reside in the same folder as your manifest file and background script:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My New Tab Page!</title>
</head>
<body>
  <h1>My New Tab Page!</h1>
  <p>You can put any content here you like</p>
</body>
</html>
```

Next we need to tell the extension about this page. We can do so by specifying a `chrome_url_overrides` key in our manifest file, like so:

```
"chrome_url_overrides": {
  "newtab": "tab.html"
}
```

Finally, you need to reload the extension for the changes to take effect. You can do this by clicking the *reload* icon for the Hello World extension on Chrome’s extensions page.

![Reload the extension](Images/chrome-ext-2.jpg)

Now, when you open a new tab, you should be greeted by your custom message.

## Adding Vue to the Extension

Now we have a very basic implementation of our extension up and running, the time has come to think about what the rest of the desired functionality will look like. When a user opens a new tab, I would like the extension to:

*   Fetch a joke from the wonderful [icanhazdadjoke.com](https://icanhazdadjoke.com/).
*   Display that joke in a nicely formatted manner to the user.
*   Display a button for the user to favorite the joke. This will save the joke to `chrome.storage`.
*   Display a button for the user to list favorited jokes.

You could, of course, do all of this with plain JavaScript, or a library like jQuery—and if that’s your thing, feel free!

For the purposes of this tutorial, however, I’m going to implement this functionality using Vue and the awesome [vue-web-extension](https://github.com/Kocal/vue-web-extension) boilerplate.

Using Vue allows me to write better, more organized code faster. And as we’ll see, the boilerplate provides several scripts that take the pain out of some of the common tasks when building a Chrome extension (such as having to reload the extension whenever you make changes).

### vue-web-extension-boilerplate

This section assumes that you have Node and npm installed on your computer. If this isn’t the case, you can either head to the [project’s home page](https://nodejs.org/en/) and grab the relevant binaries for your system, or you can [use a version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). I would recommend using a version manager.

We’ll also need [Vue CLI](https://cli.vuejs.org/) installed and the [@vue/cli-init package](https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-init#vuecli-init):

```
npm install -g @vue/cli
npm install -g @vue/cli-init
```

With that done, let’s grab a copy of the boilerplate:

```
vue init kocal/vue-web-extension new-tab-page
```

This will open a wizard which asks you a bunch of questions. To keep this tutorial focused, I answered as follows:

```
? Project name new-tab-page
? Project description A Vue.js web extension
? Author James Hibbard <jim@example.com>
? License MIT
? Use Mozilla's web-extension polyfill? No
? Provide an options page? No
? Install vue-router? No
? Install vuex? No
? Install axios? Yes
? Install ESLint? No
? Install Prettier? No
? Automatically install dependencies? npm
```

You can adapt your answers to suit your preferences, but the main thing to be certain of is that you choose to install [axios](https://www.npmjs.com/package/axios). We’ll be using this to fetch the jokes.

Next, change into the project directory and install the dependencies:

```
cd new-tab-page
npm install
```

And then we can build our new extension using one of the scripts the boilerplate provides:

```
npm run watch:dev
```

This will build the extension into a `dist` folder in the project root for development and watch for changes.

To add the extension to Chrome, go through the same process as outlined above, making sure to select the `dist` folder as the extension directory. If all goes according to plan, you should see a “Hello world!” message when the extension initializes.

### Project Setup

Let’s take a minute to look around our new project and see what the boilerplate has given us. The current folder structure should look like this:

```
.
├── dist
│   └── <the built extension>
├── node_modules
│   └── <one or two files and folders>
├── package.json
├── package-lock.json
├── scripts
│   ├── build-zip.js
│   └── remove-evals.js
├── src
│   ├── background.js
│   ├── icons
│   │   ├── icon_128.png
│   │   ├── icon_48.png
│   │   └── icon.xcf
│   ├── manifest.json
│   └── popup
│       ├── App.vue
│       ├── popup.html
│       └── popup.js
└── webpack.config.js
```

As you can see, from the config file in the project root, the boilerplate is using webpack under the hood. This is awesome, as this gives us [Hot Module Reloading](https://webpack.js.org/concepts/hot-module-replacement) for our background script.

The `src` folder contains all of the files we’ll be using for the extension. The manifest file and `background.js` should be familiar, but also notice a `popup` folder containing a Vue component. When the boilerplate builds the extension into the `dist` folder, it will pipe any `.vue` files through the [vue-loader](https://github.com/vuejs/vue-loader) and output a JavaScript bundle which the browser can understand.

Also in the `src` folder is an `icons` folder. If you look in Chrome’s toolbar, you should see a new icon for our extension (also known as the [browser action](https://developer.chrome.com/extensions/browserAction)). This is being pulled from this folder. If you click it, you should see a popup open which displays “Hello world!” This is created by `popup/App.vue`.

Finally, note a `scripts` folder containing two scripts—one to remove `eval` usages to comply with the Content Security Policy of Chrome Web Store and one to package your extension into a .zip file, which is necessary when uploading it to the Chrome Web Store.

There are also various scripts declared in the `package.json` file. We’ll be using `npm run watch:dev` for developing the extension and later on `npm run build-zip` to generate a ZIP file to upload to the Chrome Web Store.

## Using a Vue Component for the New Tab Page

Start off by removing the annoying `alert` statement from `background.js`.

Now let’s make a new `tab` folder in the `src` folder to house the code for our new tab page. We’ll add three files to this new folder—`App.vue`, `tab.html,`, `tab.js`:

```
mkdir src/tab
touch src/tab/{App.vue,tab.html,tab.js}
```

Open up `tab.html` and add the following:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>New Tab Page</title>
  <link rel="stylesheet" href="tab.css">
</head>
<body>
  <div id="app"></div>
  <script src="tab.js"></script>
</body>
</html>
```

Nothing special going on here. This is a simple HTML page which will hold our Vue instance.

Next, in `tab.js` add:

```
import Vue from 'vue';
import App from './App';

new Vue({
  el: '#app',
  render: h => h(App)
});
```

Here we import Vue, pass a selector for the element that we want it to replace with our application, then tell it to render our `App` component.

Finally, in `App.vue`:

```
<template>
  <p>{{ message }}</p>
</template>

<script>
export default {
  data () {
    return {
      message: "My new tab page"
    }
  }
}
</script>

<style scoped>
p {
  font-size: 20px;
}
</style>
```

Before we can use this new tab page, we need to update the manifest file:

```
{
  "name":"new-tab-page",
  ...
  "chrome_url_overrides": {
    "newtab": "tab/tab.html"
  }
}
```

And we also need to have the boilerplate compile our files and copy them over to the `dist` folder, so that they’re available to the extension.

Alter `webpack.config.js` like so, updating both the `entry` and `plugins` keys:

```
entry: {
  'background': './background.js',
  'popup/popup': './popup/popup.js',
  'tab/tab': './tab/tab.js'
},
```

```
plugins: [
  ...
  new CopyWebpackPlugin([
    { from: 'icons', to: 'icons', ignore: ['icon.xcf'] },
    { from: 'popup/popup.html', to: 'popup/popup.html', transform: transformHtml },
    { from: 'tab/tab.html', to: 'tab/tab.html', transform: transformHtml },
    ...
  })
```

You’ll need to restart the `npm run watch:dev` task for these changes to take effect. Once you’ve done this, reload the extension and open a new tab. You should see “My new tab page” displayed.

![My new tab page](Images/chrome-ext-3.jpg)

## Fetching and Displaying Jokes

Okay, so we’ve overriden Chrome’s new tab page and we’ve replaced it with a mini Vue app. Now let’s make it do more than display a message.

Alter the template section in `src/tab/App.vue` as follows:

```
<template>
  <div>
    <div v-if="loading">
      <p>Loading...</p>
    </div>
    <div v-else>
      <p class="joke">{{ joke }}</p>
    </div>
  </div>
</template>
```

Change the `<script>` section to read as follows:

```
<script>
import axios from 'axios';

export default {
  data () {
    return {
      loading: true,
      joke: "",
    }
  },
  mounted() {
    axios.get(
      "https://icanhazdadjoke.com/",
      { 'headers': { 'Accept': 'application/json' } }
    )
      .then(res => {
        this.joke = res.data.joke;
        this.loading = false;
      });
  }
}
</script>
```

And finally, change the `<style>` section to read as follows:

```
<style>
body {
  height: 98vh;
  text-align: center;
  color: #353638;
  font-size: 22px;
  line-height: 30px;
  font-family: Merriweather,Georgia,serif;
  background-size: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.joke {
  max-width: 800px;
}
</style>
```

If you’re running the `npm run watch:dev` task, the extension should automatically reload and you should see a joke displayed whenever you open a new tab page.

![How does a French skeleton say hello? Bone-jour](Images/chrome-ext-4.jpg)

Once you’ve verified it’s working, let’s take a minute to understand what we’ve done.

In the template, we’re using a [v-if](https://vuejs.org/v2/guide/conditional.html) block to either display a loading message or a joke, depending on the state of the `loading` property. Initially, this will be set to `true` (displaying the loading message), then our script will fire off an Ajax request to retrieve the joke. Once the Ajax request completes, the `loading` property will be set to `false`, causing the component to be re-rendered and our joke to be displayed.

In the `<script>` section, we’re importing axios, then declaring a couple of data properties—the aforementioned `loading` property and a `joke` property to hold the joke. We’re then making use of the `mounted` [lifecycle hook](https://vuejs.org/v2/guide/instance.html#Instance-Lifecycle-Hooks), which fires once our Vue instance has been mounted, to make an Ajax request to the [joke API](https://icanhazdadjoke.com/api). Once the request completes, we update both of our data properties to cause the component to re-render.

So far, so good.

## Persisting Jokes to Chrome’s Storage

Next, let’s add some buttons to allow the user to favorite a joke and to list out favorited jokes. As we’ll be using [Chrome’s storage API](https://developer.chrome.com/extensions/storage) to persist the jokes, it might be worth adding a third button to delete all of the favorited jokes from storage.

First, add the following to the bottom of `manifest.json`:

```
"permissions": [ "storage" ]
```

This gives the extension access to the `chrome.storage` API.

Reload the extension, then add the buttons to the `v-else` block:

```
<div v-else>
  <p class="joke">{{ joke }}</p>

  <button @click="likeJoke" :disabled="likeButtonDisabled">Like Joke</button>
  <button @click="logJokes" class="btn">Log Jokes</button>
  <button @click="clearStorage" class="btn">Clear Storage</button>
</div>
```

Nothing too exciting here. Note the way that we are binding the like button’s `disabled` property to a data property on our Vue instance to determine its state. This is because a user shouldn’t be able to like a joke more than once.

Next, add the click handlers and the `likeButtonDisabled` to our script section:

```
export default {
  data () {
    return {
      loading: true,
      joke: "",
      likeButtonDisabled: false
    }
  },
  methods: {
    likeJoke(){
      chrome.storage.local.get("jokes", (res) => {
        if(!res.jokes) res.jokes = [];
        res.jokes.push(this.joke);
        chrome.storage.local.set(res);
        this.likeButtonDisabled = true;
      });
    },
    logJokes(){
      chrome.storage.local.get("jokes", (res) => {
        if(res.jokes) res.jokes.map(joke => console.log(joke));
      });
    },
    clearStorage(){
      chrome.storage.local.clear();
    }
  },
  mounted() { ... }
}
```

Here we’ve declared three new methods to deal with the three new buttons.

The `likeJoke` method looks for a `jokes` property in Chrome’s storage. If it’s missing (that is, the user has yet to like a joke), it initializes it to an empty array. Then it pushes the current joke onto this array and saves it back to storage. Finally it sets the `likeButtonDisabled` data property to `true`, disabling the like button.

The `logJokes` method also looks for a `jokes` property in Chrome’s storage. If it finds one, it loops over all of its entries and logs them to the console.

Hopefully what the `clearStorage` method does is clear.

Go ahead and try this new functionality in the extension and satisfy yourself that it works.

![Listing jokes to the console](Images/chrome-ext-5.jpg)

## Adding Some Polish to the Extension

Okay, so that seems to work, but the buttons are ugly and the page is a little plain. Let’s finish off this section by adding some polish to the extension.

As a next step, install the [vue-awesome](https://www.npmjs.com/package/vue-awesome) library. This will allow us to use some Font Awesome icons in on our page and make those buttons look a bit nicer:

```
npm install vue-awesome
```

Register the library with our Vue app in `src/tab/tab.js`:

```
import Vue from 'vue';
import App from './App';
import "vue-awesome/icons";
import Icon from "vue-awesome/components/Icon";

Vue.component("icon", Icon);

new Vue({
  el: '#app',
  render: h => h(App)
});
```

Now alter the template like so:

```
<template>
  <div>
    <div v-if="loading" class="centered">
      <p>Loading...</p>
    </div>
    <div v-else>
      <p class="joke">{{ joke }}</p>

      <div class="button-container">
        <button @click="likeJoke" :disabled="likeButtonDisabled" class="btn"><icon name="thumbs-up"></icon></button>
        <button @click="logJokes" class="btn"><icon name="list"></icon></button>
        <button @click="clearStorage" class="btn"><icon name="trash"></icon></button>
      </div>
    </div>
  </div>
</template>
```

Finally, let’s add some more styling to the buttons and include a picture of [everyone’s favorite dad](https://knowyourmeme.com/memes/trolldad):

```
<style>
body {
  height: 98vh;
  text-align: center;
  color: #353638;
  font-size: 22px;
  line-height: 30px;
  font-family: Merriweather,Georgia,serif;
  background: url("https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2018/12/1544189726troll-dad.png") no-repeat 1% 99%;
  background-size: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.joke {
  max-width: 800px;
}

.button-container {
  position: absolute;
  right: 0px;
  top: calc(50% - 74px);
}

.btn {
  background-color: #D8D8D8;
  border: none;
  color: white;
  padding: 12px 16px;
  font-size: 16px;
  cursor: pointer;
  display: block;
  margin-bottom: 5px;
  width: 50px;
}

.btn:hover {
  background-color: #C8C8C8;
}

.btn:disabled {
  background-color: #909090;
}
</style>
```

The extension should reload. Try opening a new tab and you should see something like this.

![The finished extension](Images/chrome-ext-6.jpg)

## Uploading the Extension to the Chrome Web Store

Should you want to make your extension available for others to download, you’d do this via the [Chrome Web Store](https://chrome.google.com/webstore/category/extensions).

The first thing you’ll need in order to do this is a Google account, which you can use to sign in to the [Developer Dashboard](https://chrome.google.com/webstore/developer/dashboard). You’ll be prompted for your developer details, and before you publish your first app, you must pay a one-time $5 developer signup fee (via credit card).

Next, you need to create a ZIP file for your app. You can do this locally by running the `npm run build-zip`. This will create a `dist-zip` folder in your project root, containing a ZIP file ready to upload to the Web Store.

For a minimal extension, this is all you’d really need to do. However, before you upload anything, it’s worth reading the official [Publish in the Chrome Web Store](https://developer.chrome.com/webstore/publish) guide.

## Conclusion

And with that, we’re done. In this tutorial, I’ve highlighted the main parts of a Chrome extension and shown how to use the [vue-web-extension](https://github.com/Kocal/vue-web-extension) boilerplate to build an extension using Vue.js. We finished off by looking at how to upload an extension to the Web Store and everything that involves.

I hope you enjoyed this tutorial and can use it to get started building Chrome extensions of your own. [Let me know if you make anything cool](https://twitter.com/jchibbard).

# Chapter 6: Build Your Own Link-sharing Site with Nuxt.js and vue-kindergarten

### by Nilson Jacques

In this tutorial, we’re going to create a our own link-sharing news site, along the lines of [Echo JS](https://echojs.com/) or [Hacker News](https://news.ycombinator.com/), complete with comments and upvoting. The tech stack we’ll be using consists of Vue.js, the Nuxt.js Vue framework, and an access-control/authorization library called vue-kindergarten.

This guide is not intended as a “deep dive” into any of the libraries used. Rather, the aim is to give you some exposure to these tools and how they can be used together to create a real-world application.

#### Node and npm

To follow along, you’ll need to have a recent version of Node.js installed, and your copy of npm needs to be >= 5.2.0.

#### The GitHub Repo

There’s a GitHub repo available with [the finished code](https://github.com/sitepoint-editors/vue-news-site-demo).

## Installing Nuxt.js

We’re going to use [Nuxt.js](https://nuxtjs.org/) for this project. Although it’s well known for its server-side rending (SSR) functionality, we won’t actually be using this part of Nuxt. Instead, we’ll take advantage of Nuxt’s convention-over-configuration approach to reduce the amount of boilerplate we have to write to get a single page application up and running.

Open up a terminal/command prompt and create a new folder. I’ve called mine “yans” for “Yet Another News Site”, but feel free to name yours as you like:

```
mkdir yans && cd yans
```

#### Commands

These commands are for Linux, and will probably work on macOS too. Windows users will have to translate accordingly!

To bootstrap the project, launch the Nuxt.js installer via npm:

```
npx create-nuxt-app client
```

The npx tool will download and run the installer, and you’ll be presented with a series of questions. This isn’t an in-depth tutorial on Nuxt, so I’m not going to go into detail on these.

Here are the selections you’ll need to select to follow along with this guide:

1.  *Project name* (your choice)
2.  *Project description* (your choice)
3.  *Use a custom framework* (“none”)
4.  *Use a custom UI framework* (“bulma”)
5.  *Choose rendering mode* (“Single Page App”)
6.  *Use axios module* (“yes”)
7.  *Use eslint* (your choice)
8.  *Use prettier* (your choice)
9.  *Author name* (your choice)
10.  *Choose a package manager* (your choice)

#### Linting and Coding Styles

If you install ESLint and Prettier (as I did for this tutorial) you’ll need to run `npm run lint -- --fix` after installation, or your Nuxt project won’t compile.

The code formatting used in this guide reflects the default configuration. If this bothers you, feel free to change the settings to your liking (Prettier will even add those semicolons back in for you!) or opt out altogether (**recommended**).

When the installer has finished, it’s time to change into the newly created `client` folder and start building the site!

## Layout and Styling

We’re going to be using the [Bulma CSS framework](https://bulma.io) to style our news site. Nuxt helpfully gave us the option to add this from the installer, but we’ll also need to pull in [Font Awesome](https://fontawesome.com/) for the icons.

The most straightforward way to do this is to edit the Nuxt config file and add a link to the CDN CSS file.

**client/nuxt.config.js**

```
/*
 ** Headers of the page
 */
 head: {
   title: pkg.name,
   meta: [
     { charset: 'utf-8' },
     { name: 'viewport', content: 'width=device-width, initial-scale=1' },
     { hid: 'description', name: 'description', content: pkg.description }
   ],
   link: [
     { rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' },
     {
       rel: 'stylesheet',
       href: 'https://use.fontawesome.com/releases/v5.6.3/css/all.css'
     }
   ]
 },
```

We’re adding a second item to the `link` array, under the `head` property. This will add the CDN link to our SPA’s template.

The next thing we’re going to want to do is customize the basic layout, to add a menu bar that will appear across all the pages on the site.

Open up `layouts/default.vue`, and replace the contents with the following code.

**client/layouts/default.vue**

```
<template>
  <div>
    <nav
      class="navbar is-info"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <nuxt-link
          class="navbar-item"
          to="/"
        >
          YANS!
        </nuxt-link>

        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbarBasicExample"
        >
          <span aria-hidden="true"/>
          <span aria-hidden="true"/>
          <span aria-hidden="true"/>
        </a>
      </div>

      <div class="navbar-menu">
        <div class="navbar-start">
          <nuxt-link
            to="/"
            class="navbar-item"
          >Top</nuxt-link>
          <nuxt-link
            to="/new"
            class="navbar-item"
          >New</nuxt-link>
          <nuxt-link
            to="/submit"
            class="navbar-item"
          >Submit</nuxt-link>
        </div>

        <div class="navbar-end">
          <div class="navbar-item">
            <div class="buttons">
              <nuxt-link
                to="/register"
                class="button is-primary"
              >
                <strong>Register</strong>
              </nuxt-link>
              <nuxt-link
                to="/login"
                class="button is-light"
              >Log in</nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </nav>
    <nuxt/>
  </div>
</template>
```

The basic markup for the navigation bar comes from Bulma’s own documentation, but we’re replacing the anchor tags with Nuxt’s own `<nuxt-link>` components, which allow us to interact with the instance of Vue Router it uses. Also, notice that, down near the bottom of the template, we have the `<nuxt/>` element, so the router knows where to display our content.

As you can see, our menu bar has links for *Top* (posts in order of the most voted), *New* (most recent posts), and *Submit* (a form for submitting new links).

## Faking the Back End

Rather than cover building a back end for the site (a topic best left to a separate guide) we’re going to create a fake API server. Normally for this sort of task I’d reach for [json-server](https://www.sitepoint.com/mock-rest-apis-using-json-server/), which does a great job of turning a JSON file into a RESTful mock API, but we’re also going to need to support authentication.

Fortunately, there’s a module called [json-server-auth](https://github.com/jeremyben/json-server-auth) which builds on json-server to add JWT authentication and access control. Let’s install that and get it set up as our fake back end.

Switch from your `client` folder into the parent directory. Create a new folder called `server` and change into it, and init a new `package.json` file:

```
cd ..
mkdir server && cd server
npm init -y
```

Also install the json-server-auth package:

```
npm i json-server-auth
```

If you’re not familiar with the original json-server package, the way it works is that you create a JSON file which is used as a data store for the mock API. The file contains an object with keys for each of the endpoints you wish your API to have (such as “users”).

Our file will look as follows.

**server/db.json**

```
{
  "users": [],
  "posts": [],
  "comments": []
}
```

This is the basic structure we need for our news site. You can find a copy of `db.json`, prepopulated with sample data [in the project repo](https://github.com/sitepoint-editors/vue-news-site-demo/blob/master/server/db.json).

Under normal circumstances, that would be enough to get a mock back end up and running. However, as we’re going to be using the the Nuxt community’s Auth module, we need to do a little customization first.

After the Auth module makes a successful authentication request, it makes a request to a “user” endpoint, which it expects to return a JSON object representing the logged-in user.

The json-server-auth module doesn’t provide this functionality out of the box, so we’re going to add it ourselves. Create a new file called `index.js`, and add the following code.

**server/index.js**

```
const jsonServer = require('json-server')
const auth = require('json-server-auth')

const app = jsonServer.create()
const router = jsonServer.router('db.json')

const { rewriter } = require('json-server-auth/dist/guards')

const rules = rewriter({
  user: 660
})

app.use(rules)

app.db = router.db

app.use(auth)
app.get('/user', (req, res, next) => {
  const { email } = req.claims
  const { db } = req.app
  const user = Object.assign({}, db.get('users').find({ email }).value())
  delete user.password
  res.json({ user })
})
app.use(router)

app.listen(3001)
console.log('API server started on port 3001')
```

Most of this code comes from the json-server-auth documentation, but this is the code I’ve added:

```
app.get('/user', (req, res, next) => {
  const { email } = req.claims
  const { db } = req.app
  const user = Object.assign({}, db.get('users').find({ email }).value())
  delete user.password
  res.json({ user })
})
```

When a request is made to the `/users` endpoint, this handler gets the user’s email (from the JWT) and fetches the user from the JSON file DB. It removes the password field from the object, before returning it in the response.

Now that’s done, we can spin up an instance of our back end and leave it running as we develop the site itself:

```
node index.js
```

If you’re following along, you’ll also need to start the Nuxt server in the `client` folder with:

```
npm run dev
```

### Proxying with the axios Module

We’re going to take advantage of one of the features of Nuxt’s axios module: proxying. This will allow us to treat our API as if it’s on the same server as the site itself, making requests to `/api/users` instead of something like `http://localhost:3001/users`.

To set this up, all we have to do is add some settings to the Nuxt configuration file.

**client/nuxt.config.js**

```
/*
** axios module configuration
*/
axios: {
  proxy: true
},

proxy: {
  '/api/': { target: 'http://localhost:3001', pathRewrite: { '^/api/': '' } }
},
```

What we’re doing here is telling axios that we want to use a proxy, and then defining a separate `proxy` key with details of the URL we want to map.

In this case, we’re taking any requests to URLs beginning in `/api/` and redirecting them to our mock API server. The `pathRewrite` option strips off the `/api/` segment from the path, as we don’t need it as part of the server URL.

Now that we’ve got our back-end server set up and the proxy configured, let’s start adding some functionality to our site.

## Authentication

As I mentioned before, we’re going to use the [Auth module](https://auth.nuxtjs.org/) plugin for Nuxt. With a little configuration, this module provides us with some helpful methods for authenticating a user with our server, and some Nuxt middleware for restricting routes to logged-in users.

The first thing we need to do is install the module from npm (don’t forget to change back to the `client` folder before this step!):

```
npm i @nuxtjs/auth
```

Once this has downloaded, we need to open the Nuxt config file again, and add some settings.

**client/nuxt.config.js**

```
/*
** Nuxt.js modules
*/
modules: [
  '@nuxtjs/auth',
  // Doc: https://github.com/nuxt-community/axios-module#usage
  '@nuxtjs/axios',
  // Doc:https://github.com/nuxt-community/modules/tree/master/packages/bulma
  '@nuxtjs/bulma'
],
```

First of all, we need to tell Nuxt about the plugin, by adding the module name to the `modules` array as above.

Directly below the `modules` section, let’s add a new key for the auth module’s settings.

**client/nuxt.config.js**

```
auth: {
  strategies: {
    local: {
      endpoints: {
        login: {
          url: '/api/login',
          method: 'post',
          propertyName: 'accessToken'
        },
        logout: false,
        user: { url: '/api/user', method: 'get' }
      }
    }
  }
},
```

The auth module allows you to configure different “strategies” (that is, different authentication methods), and we want to set up the “local” strategy which supports JWT-based authentication.

Within the configuration for the strategy, we need to specify details of “login”, “logout”, and “user” endpoints for the module to make requests to, and how it can retrieve the auth token. Note that we’re setting `logout` to `false` as our authentication API doesn’t support this method. The module will just delete the cached token and revert to a logged out state.

The other thing we need to do to get the module working is have a Vuex store, as it uses this to store the authentication state and the logged-in user. We’ll also be using a Vuex for our application, so let’s go ahead and set this up as an empty store.

**client/store/index.js**

```
import Vuex from 'vuex'

const createStore = () => {
  return new Vuex.Store({
    state: {},
    getters: {},
    actions: {},
    mutations: {}
  })
}

export default createStore
```

Nuxt requires our store to be exported as a factory function due to how the SSR functionality works, but other than that this is a regular Vuex store.

We’ll also need a couple of pages to handle registration and logging in. Let’s create those next.

### Registration

First, create a new file called `register.vue` within the `pages` folder. Let’s look at the template section before we add the script block.

**client/pages/register.vue**

```
<template>
  <section class="section">
    <div class="container">

      <div class="field">
        <label class="label">Username</label>
        <div class="control">
          <input
            v-model="username"
            class="input"
            type="text"
            autofocus
          >
        </div>
      </div>

      <div class="field">
        <label class="label">Email</label>
        <div class="control">
          <input
            v-model="email"
            class="input"
            type="text"
          >
        </div>
      </div>

      <div class="field">
        <label class="label">Password</label>
        <div class="control">
          <input
            v-model="password"
            class="input"
            type="password"
          >
        </div>
      </div>

      <div class="field">
        <div class="control">
          <button
            :disabled="isSaving"
            class="button is-link"
            @click="registerUser"
          >Register</button>
        </div>
      </div>
    </div>
  </section>
</template>
```

Here we’ve just got three basic input fields, all connected via `v-model` to data properties on the component. When the submit button is clicked, it will call the `registerUser` method in the component.

And now the code:

```
<script>
import { mapActions } from 'vuex'

export default {
  data: () => ({
    isSaving: false,
    username: null,
    email: null,
    password: null
  }),
  methods: {
    ...mapActions(['saveUser']),
    async registerUser() {
      this.isSaving = true

      await this.saveUser({
        username: this.username,
        email: this.email,
        password: this.password
      })

      this.$auth.login({
        data: {
          email: this.email,
          password: this.password
        }
      })

      this.$router.push('/')
    }
  }
}
</script>
```

The `registerUser` method is pretty straightforward. We set an `isSaving` flag to `true`, which prevents the form being resubmitted while we’re processing it. We then dispatch a Vuex action, `saveUser`, passing in the three input values and waiting for it to complete. Lastly, we call the auth module’s `login` method with the same values to log the newly registered user in, and redirect to the home page.

One of the benefits to using Nuxt is that we don’t have to manually create routes for the pages. Any component created in the `pages` folder will automatically have a route generated for it with the same name.

We don’t actually have a `saveUser` action in our store yet, so let’s write that now.

**client/store/index.js**

```
actions: {
  async saveUser(context, { username, email, password }) {
    const data = {
      id: uuid(),
      username,
      email,
      password,
      timestamp: new Date().getTime()
    }

    try {
      await this.$axios.post('/api/register', data)
    } catch (error) {
      console.error(error)
    }
  }
}
```

This action takes the email, username, and password data passed into it and builds a new user object. Notice that we’re assigning a UUID as the user ID here. Although json-server-auth will assign an ID for us if we leave it blank, I prefer to use a UUID.

We’ll need to install the module for generating UUIDs via npm, and import it at the top of the store:

```
npm i uuid
```

**client/store/index.js**

```
import Vuex from 'vuex'
import uuid from 'uuid/v4'
```

The axios module makes axios available in the store as `this.$axios`, making it straightforward to send a POST request to our API server. We’re just going to log any errors to the console for now, but you’d probably want to notify the user of the error somehow (for example, with the [Nuxt toast module](https://www.npmjs.com/package/@nuxtjs/toast)).

The finished page should look like this:

![The registration page](Images/yans-register.png)

### Login

Let’s tackle the login page next. Create `login.vue` within the `pages` folder, and add the following template.

**client/pages/login.vue**

```
<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class="column is-4 is-offset-4">
          <h3 class="title has-text-grey">Login</h3>
          <p class="subtitle has-text-grey">Please log in to proceed.</p>
          <div class="box">
            <form @submit.prevent="onSubmit">
              <div class="field">
                <div class="control">
                  <input
                    v-model="email"
                    class="input"
                    type="email"
                    placeholder="Your Email"
                    autofocus
                  >
                </div>
              </div>

              <div class="field">
                <div class="control">
                  <input
                    v-model="password"
                    class="input"
                    type="password"
                    placeholder="Your Password"
                  >
                </div>
              </div>
              <button class="button is-block is-info is-fullwidth">Login</button>
            </form>
          </div>
          <div
            v-if="showError"
            class="notification is-danger"
          >
            <strong>Oops — we couldn't log you in!</strong><br>
            Please check your email and password and try again.
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
```

Most of the markup here is for applying styling, courtesy of Bulma. The important things to note are that we’ve got `v-model` properties set on the inputs, so the component can access the values, and we’ve got an `onSubmit` handler attached to the form (along with a `.prevent` modifier, to prevent the default action). There’s also an error message that will be shown if the `showError` data property is set to true.

Here’s the script section:

```
<script>
export default {
  data: () => ({
    email: '',
    password: '',
    showError: false
  }),
  methods: {
    async onSubmit() {
      try {
        await this.$auth.login({
          data: {
            email: this.email,
            password: this.password
          }
        })
      } catch (error) {
        this.showError = true
      }
    }
  }
}
</script>
```

This should be fairly self-explanatory, but we’re calling the auth module’s `login` method and passing the credentials from the form. If an error is thrown, we set `showError` to true, alerting the user that there was a problem.

Now that we’ve added registration and login functionality, we should go back and tweak our layout slightly, to change the menu based on the current user’s authentication state.

**client/layouts/default.vue**

```
<div class="navbar-end">
  <div class="navbar-item">
    <div class="buttons">
      <nuxt-link
        v-if="!$auth.loggedIn"
        to="/register"
        class="button is-primary"
      >
        <strong>Register</strong>
      </nuxt-link>
      <nuxt-link
        v-if="!$auth.loggedIn"
        to="/login"
        class="button is-light"
      >Log in</nuxt-link>
      <button
        v-else
        class="button is-light"
        @click="$auth.logout()"
      >Log out</button>
    </div>
  </div>
</div>
```

The auth module provides us with a helper (`$auth.loggedIn` from within a template) for checking the logged-in state. We can use it to hide the “register” and “log in” buttons if the current user is authenticated and display a “log out” button instead.

Here’s what the finished page looks like:

![The login screen](Images/yans-login.png)

## Adding New Posts

Now that we have our authentication set up, and a way for users to register and log in, let’s create a page to allow users to submit new links for our news site.

Go to the `pages` folder and create a new file called `submit.vue`.

**client/pages/submit.vue**

```
<template>
  <section class="section">
    <div class="container">

      <div class="field">
        <label class="label">Title</label>
        <div class="control">
          <input
            v-model="title"
            class="input"
            type="text"
            placeholder="Text input"
          >
        </div>
      </div>

      <div class="field">
        <label class="label">Full URL (inc. http(s)://)</label>
        <div class="control">
          <input
            v-model="url"
            class="input"
            type="text"
            placeholder="Text input"
          >
        </div>
      </div>

      <div class="field">
        <div class="control">
          <button
            :disabled="isSaving"
            class="button is-link"
            @click="submitPost"
          >Submit</button>
        </div>
      </div>
    </div>
  </section>
</template>
```

The template here is very similar in structure to our registration form: just a couple of input fields with associated `v-model` properties, and a submit button that triggers a handler on the component.

Here’s the script section:

```
<script>
import { mapActions } from 'vuex'

export default {
  middleware: 'auth',
  data: () => ({
    isSaving: false,
    title: null,
    url: null
  }),
  methods: {
    ...mapActions(['savePost']),
    async submitPost() {
      this.isSaving = true

      await this.savePost({
        title: this.title,
        url: this.url
      })

      this.title = null
      this.url = null
      this.isSaving = false
    }
  }
}
</script>
```

This section is also very similar to what we did before, taking the details and dispatching the `savePost` action to the store. On completion, we’re simply resetting the form to allow further submissions. It would be a good idea to pop up a notification at this point to inform the user their link has been saved, which I’ll leave as an exercise for the reader.

Note that for this component, we’re specifying a `middleware` property of “auth”. This middleware is part of the auth module, and will restrict access to the page to logged-in users. If a guest user tries to access the page, they’ll be redirected to the login form.

The form should look like this:

![The new post form](Images/yans-submit.png)

Let’s go ahead and write the `savePost` action.

**clients/store/index.js**

```
actions: {
  // ...
  async savePost(context, { title, url }) {
    const user = this.$auth.user
    const data = {
      id: uuid(),
      userId: user.id,
      author: user.username,
      title,
      url,
      votes: [],
      timestamp: new Date().getTime()
    }

    try {
        await this.$axios.post('/api/posts', data)
    } catch (error) {
        console.error(error)
    }
  },
},
```

We start off by getting a reference to the current user from the auth module (available within our store as `this.$auth`). We’re then constructing an object literal with the properties for the new post. We’re also adding an empty `votes` array, as this is how we’re going to keep track of the users who’ve upvoted a post.

Once the `data` object is built, we’re using the axios module to submit it via a POST request to our back-end API.

## Fetching and Displaying Posts

Now that we have a way for users to submit links, we’re going to need a way to retrieve those and display them, so let’s build out the “new posts” page.

Before creating the page itself, let’s make the necessary changes to the store.

**client/store/index.js**

```
state: {
  posts: []
},
```

First of all, we need to add a `posts` array to the store state, to hold the posts once we’ve retrieved them from the API.

Next, we’ll need an action to make the API request.

**client/store/index.js**

```
actions: {
  // ...
  async getPosts({ commit }) {
    try {
      const res = await this.$axios.get('/api/posts')
      commit('setPosts', { posts: res.data })
    } catch (error) {
      console.error(error)
    }
  },
},
```

Here we’re just making a GET request to the `posts` endpoint of the API, and passing the result along to the `setPosts` mutation. Let’s add that.

**client/store/index.js**

```
mutations: {
  setPosts(state, { posts }) {
    state.posts = posts
  }
},
```

This is a simple mutation that simply replaces the existing posts array with the one we get back from the API.

For our “new posts” view, we’re going to display the links in descending order of creation. Although this logic could go in the component itself, let’s create a Vuex getter. This will enable us to access the sorted list of posts elsewhere in the app should we want to.

**client/store/index.js**

```
getters: {
  newPosts: state => state.posts.sort((a, b) => a.timestamp - b.timestamp)
},
```

As with computed properties within components, if the `posts` array is modified, the `newPosts` getter will update and be re-rendered by any components using it.

#### Displaying the “Top Posts” Page

The page to display the top voted posts is virtually identical to this one, except that it uses a different getter to return the posts in a different order. You can have a go at building this out yourself, or take a look at this guide’s accompanying [code repo](https://github.com/sitepoint-editors/vue-news-site-demo/blob/master/client/pages/index.vue).

Let’s add the listing page. Create a new file under `pages` called `new.vue`, and add the following code.

**client/pages/new.vue**

```
<template>
  <section class="section">
    <div class="container">
      <h1 class="title">Latest Links</h1>
      <div>
        <news-item
          v-for="post in newPosts"
          :key="post.id"
          :item="post"
        />
      </div>
    </div>
  </section>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'
import NewsItem from '~/components/NewsItem'

export default {
  components: { NewsItem },
  fetch({ store }) {
    store.dispatch('getPosts')
  },
  computed: mapGetters(['newPosts'])
}
</script>
```

I’ve shown the entire file here, as it’s only a relatively small component. It contains the Nuxt-specific `fetch` method, which is called whenever the user tries to navigate to the page. The method receives a [context](https://nuxtjs.org/api/context) object containing the store (among other things), allowing us to dispatch actions before the component is loaded.

Once the `getPosts` action has completed, the `newPosts` getter will be updated, and the component can render the list of posts. We’re delegating the display of each post to the `<NewsItem>` component here, which is actually a custom component. Let’s take a look at that next.

## The NewsItem Component

Displaying a post seems like something we might want to do in multiple places on our news site, so it makes sense to extract this into a separate component. It also encapsulates any markup and display logic, helping to keep the parent components cleaner and focused on the code needed to do their jobs.

Let’s go to the `components` folder and create a new component file called `NewsItem.vue`. As we’ve done previously, we’ll look at the template first.

**client/components/NewsItem.vue**

```
<template>
  <article class="media">
    <figure class="media-left">
      <button class="button is-white">
        <span class="icon is-small">
          <i
            class="fas fa-thumbs-up"
            title="Vote up" />
        </span>
      </button>
    </figure>
    <div class="media-content">
      <div>
        <p>
          <a :href="item.url"><strong>{{ item.title }}</strong></a> <small>({{ item.url | domain }})</small>
        </p>
      </div>
      <nav class="level is-mobile">
        <div class="level-left">
          <span class="level-item">
            <small>{{ votes }} · posted by {{ item.author }} · {{ item.timestamp | timeAgo }}</small>
          </span>
          <nuxt-link
            :to="`/news/${item.id}`"
            class="level-item"
          >
            <span class="icon is-small"><i class="fas fa-comments" /></span>
          </nuxt-link>
        </div>
      </nav>
    </div>
  </article>
</template>
```

A lot of this markup is part of Bulma’s [media object](https://bulma.io/documentation/layout/media-object/), which provides us with a nice structure to build on. You’ll notice we’ve got an upvote button (which we’ll wire up a bit later on), and a couple of output filters: `domain` and `timeAgo`. Let’s look at the JavaScript and see what they’re doing.

**client/components/NewsItem.vue**

```
<script>
import parseDomain from 'parse-domain'
import distanceInWordsStrict from 'date-fns/distance_in_words_strict'

export default {
  filters: {
    domain(value) {
      if (!value) return ''
      const parts = parseDomain(value)
      return parts ? `${parts['domain']}.${parts['tld']}` : ''
    },
    timeAgo(value) {
      if (!value) return ''
      return distanceInWordsStrict(new Date(), new Date(value), {
        addSuffix: true
      })
    }
  },
  props: {
    item: {
      type: Object,
      required: true
    }
  },
  computed: {
    votes() {
      const votes = this.item.votes.length
      const suffix = votes === 1 ? 'vote' : 'votes'
      return `${votes} ${suffix}`
    }
  }
}
</script>
```

As you can see from the component code, we’re importing two third-party modules to help with the formatting: [parse-domain](https://www.npmjs.com/package/parse-domain), and the [date-fns](https://date-fns.org/) function [distanceInWordsStrict](https://date-fns.org/v1.30.1/docs/distanceInWordsStrict).

The parse-domain module takes a URL and returns an array of the constituent parts. Using this, we can display just the domain of the link, so the user knows at a glance which site the content comes from. The `distanceInWordsStrict` function takes two dates and returns a human-friendly description of the time elapsed (such as “5 minutes ago”).

#### Dependencies!

Don’t forget to install the dependencies!

```
npm i parse-domain date-fns
```

Both of these could have been implemented as computed functions, but because their purpose is to *format* output for display, using filters seemed more appropriate. In addition, we could easily re-implement them as global filters, if we needed to use them in other components of the app, without having to change the template.

One place we *are* using a computed property is to display the number of votes and correctly pluralize the text when necessary.

With the page and `NewsItem` component complete, the screen should look something like this with the dummy data:

![The “new links” page, showing dummy data](Images/yans-new.png)

## Handling Comments

Having a list of links is all well and good, but we could do with a way to get users interacting more with the site. Let’s add a comments view to allow our users to discuss the links that get posted.

This page is a little different from the ones we’ve created so far. Since we’re going to be displaying the comments for an individual post, we want the URL to contain the post ID. In this case, we want our URL to conform to the format `/news/6d369e63-da45-4bc3-8853-47106636e256`, where the ID is a dynamic parameter.

To do this in Nuxt, we name our page component `pages/news/_id.vue`. The underscore prefix lets Nuxt know it needs to make this part of the route dynamic, and make the value available to us via a router param.

Let’s create the file, and add in the following code.

**client/pages/news/_id.vue**

```
<template>
  <section class="section">
    <div class="container">
      <news-item :item="selectedPost"/>
      <comment-form
        v-if="$auth.loggedIn"
        @post="saveComment"
      />
      <p v-else>
        Please <nuxt-link to="/register">register</nuxt-link> or
        <nuxt-link to="/login">log in</nuxt-link> to comment.
      </p>
    </div>
  </section>
</template>

<script>
import { mapActions, mapState } from 'vuex'
import NewsItem from '~/components/NewsItem'
import CommentForm from '~/components/CommentForm'

export default {
  fetch({ store, params }) {
    const postId = params.id
    return store.dispatch('getComments', { postId })
  },
  components: { CommentForm, NewsItem },
  computed: mapState(['selectedPost']),
  methods: mapActions(['saveComment'])
}
</script>

<style scoped>
p {
  text-align: center;
  margin: 2em;
}
</style>
```

The `fetch` method here is retrieving the dynamic route parameter `id` from the context object and dispatching the `getComments` action to the store, passing the parameter.

We’re making use of the `NewsItem` component again to display the selected post, and we’re also rendering a `CommentForm` component (that we’ll create in a moment). We’re only going to display the form if the user is authenticated. Otherwise, we’ll prompt them to either log in or register. The form component emits a `post` event, which we’re using to directly trigger the store action `saveComment`.

**client/components/CommentForm.vue**

```
<template>
  <article class="media">
    <div class="media-content">
      <div class="field">
        <p class="control">
          <textarea
            v-model="body"
            class="textarea"
            placeholder="Add a comment..."
          />
        </p>
      </div>
      <div class="field">
        <p class="control">
          <button
            :disabled="!body"
            class="button"
            @click="commentPosted"
          >Post comment</button>
        </p>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  data: () => ({
    body: null
  }),
  methods: {
    commentPosted() {
      this.$emit('post', { body: this.body })
      this.body = null
    }
  }
}
</script>
```

The `CommentForm` component is pretty straightforward, as we’re only dealing with a single input. When the user clicks the button, the component emits a `post` event with the comment text as the payload.

Let’s create the two store actions we need for this page to work.

**client/store/index.js**

```
state: {
  posts: [],
  selectedPost: null
},
```

Firstly, we add a `selectedPost` property to hold the post the user is viewing.

**client/store/index.js**

```
actions: {
  // ...
  async getComments({ commit }, { postId }) {
    try {
      const res = await this.$axios.get(
        `/api/posts/${postId}?_embed=comments`
      )
      commit('setSelectedPost', { post: res.data })
    } catch (error) {
      console.error(error)
    }
  },
  async saveComment({ commit, state }, { body }) {
    const user = this.$auth.user
    const data = {
      id: uuid(),
      postId: state.selectedPost.id,
      userId: user.id,
      author: user.username,
      body,
      timestamp: new Date().getTime()
    }

    try {
      const res = await this.$axios.post('/api/comments', data)
      commit('addComment', { comment: res.data })
    } catch (error) {
      console.error(error)
    }
  }
},
```

Both of these actions are similar to the ones we created previously, so there’s not much to point out about this code. One thing that’s worth mentioning, though, is that we’re re-requesting the selected post from the API, but appending `?_embed=comments` to the URL. This will tell json-server-auth to return the post with all the associated comments attached as an array.

We also need a couple of additional mutations.

**client/store/index.js**

```
mutations: {
  // ...
  addComment(state, { comment }) {
    state.selectedPost.comments.push(comment)
  },
  setSelectedPost(state, { post }) {
    state.selectedPost = post
  },
},
```

Commiting `setSelectPost` assigns the passed `post` object to the `selectedPost` key in the store’s state. The `addComment` mutation takes the comment (having already been persisted by our API) and pushes it into the `comments` array on our current post, allowing the view to update.

### Displaying Posted Comments

You might have noticed we aren’t displaying the comments anywhere in our page! Let’s rectify that by updating the `NewsItem` to display comments if they’re present on the post object. Open up the component and add the following markup to the template, below the closing `</nav>` tag.

**client/components/NewsItem.vue**

```
<article
  v-for="comment in comments"
  :key="comment.id"
  class="media"
>
  <figure class="media-left">
    <p class="image is-48x48">
      <img src="https://bulma.../Images/placeholders/96x96.png">
    </p>
  </figure>
  <div class="media-content">
    <div class="content">
      <p>
        {{ comment.body }}
        <br>
        <small>{{ comment.author }} · {{ comment.timestamp | timeAgo }}</small>
      </p>
    </div>
  </div>
</article>
```

Also add a new computed property to the component object:

```
computed: {
  comments() {
    return this.item.comments || []
  },
  votes() {
    // ...
  }
}
```

And voila! You should now see a nicely formatted list of comments appear beneath the post as you add them!

![A comments page showing the post and a fake comment](Images/yans-comments.png)

## Upvoting Posts

The only thing that’s left to add to our news site is the ability for users to upvote quality posts. Let’s start by adding the necessary action and mutation to the store.

**client/store/index.js**

```
actions: {
  // ...
  async upvotePost({ commit }, { postId }) {
    const postUrl = `/api/posts/${postId}`
    try {
      const { data } = await this.$axios.get(postUrl)
      data.votes.push(this.$auth.user.id)
      const res = await this.$axios.put(postUrl, data)
      commit('updatePost', { post: res.data })
    } catch (error) {
      console.error(error)
    }
  }
},
```

Our `upvotePost` action receives the ID of the post to upvote. Firstly, we re-fetch the post from the API, and push the current user’s ID into the `votes` array. After saving the post back to the server, we commit the `updatePost` mutation, which we’ll write next.

**client/store/index.js**

```
mutations: {
  // ...
  updatePost(state, { post }) {
    const index = state.posts.findIndex(p => p.id === post.id)
    if (index >= 0) {
      state.posts.splice(index, 1, post)
    }
    if (state.selectedPost && state.selectedPost.id === post.id) {
      state.selectedPost.votes = post.votes
    }
  }
},
```

This mutation looks up the index of the post that’s been upvoted, and replaces it with the copy returned from the server. If the user is voting from one of the list views, they’ll see the vote count update dynamically. We also check if `selectedPost` is set and is the same as the upvoted post and updates the `votes` property.

Let’s wire up these new actions to our existing list and comments views, so users can start voting on their favorite links.

First of all, we need to make a small change to the `NewsItem` component, so it can emit an event when the upvote button is clicked.

**client/components/NewsItem.vue**

```
<button
  class="button is-white"
  @click="$emit('upvote')"
>
  <span class="icon is-small">
    <i
      class="fas fa-thumbs-up"
      title="Vote up" />
  </span>
</button>
```

Next, let’s amend the “New Posts” page.

**client/pages/new.vue**

```
<news-item
  v-for="post in newPosts"
  :key="post.id"
  :item="post"
  @upvote="upvotePost(post)"
/>
```

In the template, all that’s required is to add a listener for the `upvote` event. There’s no payload emitted with the event, we’re simply passing the current post in the loop to the component’s `upvotePost` method.

**client/pages/new.vue**

```
methods: {
  ...mapActions(['upvotePost']),
  onUpvote(post) {
    this.upvotePost({ postId: post.id })
  }
},
```

In the component object, we’ve added the `onUpvote` method, which just extracts the ID from the `post` object and dispatches it to the store’s `upvotePost` action.

The comments page is similar.

**client/pages/news/_id.vue**

```
<news-item
  :item="selectedPost"
  @upvote="onUpvote(selectedPost)"
/>
```

The component’s `onUpvote` method is slightly different, as we have to remember to set the `updateSelectedPost` flag.

**client/pages/news/_id.vue**

```
methods: {
  ...mapActions(['saveComment', 'upvotePost']),
  onUpvote(post) {
    this.upvotePost({ postId: post.id })
  }
},
```

## Authorization

One thing you may have noticed while working on the last section is that there’s nothing to stop a user from upvoting a post more than once. In fact, there’s nothing to stop them from upvoting their own posts, either, which seems a little unfair!

Rather than put the logic to check for this into our components, we’re going to make use of an authorization library called [vue-kindergarten](https://github.com/JiriChara/vue-kindergarten). The benefit of using a library like this is that it allows us to separate out the authorization logic from our components, preventing it from bloating them with extra responsibilities, and making that logic easy to re-use across our application.

So, let’s install the package from npm:

```
npm i vue-kindergarten
```

Once it’s downloaded, we need to register it with Vue.js. Normally we’d do this in the file where we create our main Vue instance, but with Nuxt we do this by creating a plugin file.

**client/plugins/vue-kindergarten.js**

```
import Vue from 'vue'
import VueKindergarten from 'vue-kindergarten'

Vue.use(VueKindergarten, {
  child: store => store && store.state.auth.user
})
```

The code is pretty straightforward: we import Vue and the vue-kindergarten library, and register it as we would in a normal Vue app. The plugin takes an `options` object with a `child` property. This should be a function that will be passed an instance of the Vuex store and return the current user.

#### vue-kindergarten Terminology

The library’s terminology revolves around pre-school, with concepts like sandboxes, perimeters, and governesses, so wherever you see “child”, read “user”.

With the plugin file created, we just need to add a reference to it to the `plugins` array in the Nuxt config file.

**client/nuxt.config.js**

```
 plugins: ['~/plugins/vue-kindergarten'],
```

Our next step is to create a **perimeter**. This is a file that contains all the authorization logic for a particular entity or situation. Make a new folder within the Nuxt project called `perimeters`, and add a new file called `postsPerimeter.js` with the following content.

**client/perimeters/postsPerimeter.js**

```
import { createPerimeter } from 'vue-kindergarten'

export default createPerimeter({
  purpose: 'post',

  can: {
    upvote(post) {
      return (
        this.isAuthenticated() &&
        this.isAuthor(post) === false &&
        post.votes.includes(this.child.id) === false
      )
    }
  },

  isAuthenticated() {
    return this.child !== null
  },

  isAuthor(post) {
    return this.child.id === post.userId
  }
})
```

Here we’re importing the `createPerimeter` function from the `vue-kindergarten` module, and using it to define a new perimeter, or set of rules. The `purpose` property lets us define the name of the entity that the rules apply to. When we add the perimeter to a component, its rules become available under the `$post` variable within the template.

The perimeter contains a couple of helper methods for checking if the user is logged in, and if they’re the author of a given post. We also have a `can` property that lets us define actions the current user is allowed to take. Here, we’ve added an `upvote` method, which will return `true` only if the user is authenticated, is *not* the author of the post, and hasn’t already upvoted the post.

Let’s see how we can use this perimeter within our “New Posts” page to control who is allowed to vote on any given post.

**client/pages/new.vue**

```
<script>
import { mapActions, mapGetters } from 'vuex'
import postsPerimeter from '~/perimeters/postsPerimeter'
import NewsItem from '~/components/NewsItem'

export default {
  components: { NewsItem },
  fetch({ store }) {
    store.dispatch('getPosts')
  },
  computed: mapGetters(['newPosts']),
  methods: {
    ...mapActions(['upvotePost']),
    onUpvote(post) {
      if (this.$isAllowed('upvote', post)) {
        this.upvotePost({ postId: post.id })
      }
    }
  },
  perimeters: [postsPerimeter]
}
</script>
```

The sharp-eyed among you will have spotted that we’re importing our new perimeter, and adding it to a new `perimeters` array on the component. The only other change here is to the `onUpvote` method, where we’re using the `this.$isAllowed` helper to check if the vote should be submitted.

As you can see, all the checking logic is neatly encapsulated in the perimeter. If we decide to add an additional requirement in future (for example, that the user must have confirmed their email address, or must have a minimum ranking on the site) we can do that without requiring any changes to our components.

## Summary

And there we have it: you’ve now built your own news site that you can use to start your own version of Reddit! In all seriousness though, I do hope you’ve enjoyed following along and have picked up some useful knowledge that you can apply to future projects of your own.

If you’d like to take a more in-depth look at Nuxt.js, and Vue in general, check out my new SitePoint book called *[Jump Start Vue.js](https://www.sitepoint.com/premium/books/jump-start-vue-js)*.

# Chapter 7: An Introduction to Data Visualization with Vue and D3.js

### by Christopher Vundi

Web applications are normally data-driven and oftentimes the need arises to visualize this data. That’s where charts and graphs come in. They make it easier to convey information, as well as demonstrate correlations or statistical relationships. Information presented in the form of a chart or a graph is also easier for a non-native speaker to understand.

In this tutorial, we’ll learn how to visualize data in a Vue project. For this, we’ll be using the popular D3.js library, which combines powerful visualization components and a data-driven approach to DOM manipulation.

Let’s get started.

#### The GitHub Repo

The code for this tutorial can be found on [GitHub](https://github.com/sitepoint-editors/D3.js).

## What is D3?

As you can read on [the project’s home page](https://d3js.org/), D3.js is a JavaScript library for manipulating documents based on data. D3 helps you bring data to life using HTML, SVG, and CSS. Its emphasis on web standards gives you the full capabilities of modern browsers without tying yourself to a proprietary framework.

Whereas most people will refer to D3.js as a data visualization library, *it’s not*. D3 is more of a framework comprising different parts—such as jQuery parts (which help us select and manipulate DOM elements), Lodash parts, animation parts, data analysis parts, and data visualization parts.

In this tutorial, we’ll be working with the visualization aspect of D3\. The real meat of D3 when visualizing data is:

*   the availability of functions for decorating data with drawing instructions
*   creating new drawable data from source data
*   generating SVG paths
*   creating data visualization elements (like an axis) in the DOM from your data and methods

## What We’ll Be Building

We want to create an app that lets users search for a repo on GitHub, then get a visual representation of issues opened in the past week that are still open. The end result will look like this:

![Final Chart](Images/final-chart.png) 

## Prerequisites

This tutorial assumes you have [a working knowledge of Vue](https://www.sitepoint.com/up-and-running-vue-js-2-0/). Previous knowledge of D3.js isn’t required, but if you’d like to get up to speed quickly, you might want to read our [D3 by example tutorial](https://www.sitepoint.com/d3-js-data-visualizations/).

You’ll also need to have Node installed on your system. You can do this by downloading the binaries for your system from the [official website](https://nodejs.org), or using a [version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

Finally, we’ll be using the following packages to build our app:

*   [Vue CLI](https://cli.vuejs.org/)—to scaffold out the project
*   [D3.js](https://d3js.org/)—to visualize our data
*   [Lodash](https://lodash.com/)—which provides a handful of utility methods
*   [Moment JS](https://momentjs.com/)—for date and time formatting
*   [axios](https://github.com/axios/axios)—an HTTP client to help us make requests to an external API

## New Vue Project

I prefer creating new Vue projects using Vue CLI. (If you’re not familiar with Vue CLI, our beginner’s guide in this Vue series gives a full introduction.) Vue CLI provides a nice folder structure for placing different sections of the code, such as styles, components, and so on.

Make sure that the CLI is installed on your machine:

```
npm install -g @vue/cli
```

Then create a new project with the following command:

```
vue create issues-visualization
```

#### Picking Presets

While creating a new project using Vue CLI, you’ll be prompted to pick a preset. For this particular project, we’ll just stick with the default (Babel + ESLint).

Once our new Vue project has been created, we `cd` into the project folder and add the various node modules we’ll need:

```
npm install lodash d3 axios moment
```

Even though this is a simple app that doesn’t have many running parts, we’ll still take the components approach instead of dumping all the code inside the `App.vue` file. We’re going to have two components, the `App` component and a `Chart` component that we’re yet to create.

The `App` component will handle fetching data from GitHub, then pass this data to the `Chart` component as props. The actual drawing of the chart will happen inside the `Chart` component. Structuring things this way has the advantage that, if you want to use a library other than axios to fetch the data, it’ll be easier to swap it out. Also, if you want to swap D3 for a different charting library, that’ll be easier too.

## Building the Search Interface

We’ll start by building a search interface that lets users enter the name of the repo they want to see visualized.

In `src/App.vue`, get rid of everything inside the `<template>` tag and replace the content with this:

```
<template>
  <div id="app">
    <form action="#" @submit.prevent="getIssues">
      <div class="form-group">
        <input
          type="text"
          placeholder="owner/repo Name"
          v-model="repository"
          class="col-md-2 col-md-offset-5"
        >
      </div>
    </form>
  </div>
</template>
```

Here we have a form which, upon submission, prevents the browser’s default submission action, then calls a `getIssues` method that we’re yet to define. We’re also using a `v-model` directive to bind the input from the form to a `repository` property inside the data model of our Vue instance. Let’s declare that property `repository` as an empty string. We’ll also add a `startDate` property, which we’ll later use as the first date in our time range:

```
import moment from "moment";
import axios from "axios";

export default {
  name: "app",
  data() {
    return {
      issues: [],
      repository: "",
      startDate: null
    };
  },
  methods: {
    getIssues() {
      // code goes in here
    }
  }
};
```

Now on to creating the `getIssues` method:

```
getIssues() {
  this.startDate = moment()
    .subtract(6, "days")
    .format("YYYY-MM-DD");

  axios
    .get(
      `https://api.github.com/search/issues?q=repo:${this.repository}+is:issue+is:open+created:>=${this.startDate}`,
      { params: { per_page: 100 } }
    )
    .then(response => {
      const payload = this.getDateRange();

      response.data.items.forEach(item => {
        const key = moment(item.created_at).format("MMM Do YY");
        const obj = payload.filter(o => o.day === key)[0];
        obj.issues += 1;
      });

      this.issues = payload;
      console.log(this.issues);
    });
}
```

In the above block of code, we start by setting the `startDate` data property to six days ago and formatting it for use with the GitHub API.

We then use axios to make an API request to GitHub to get all issues for a particular repository that were opened in the past week and that are still open. You can refer to [GitHub’s search API](https://help.github.com/articles/searching-for-repositories/) if you need more examples on how to come up with query string parameters.

When making the HTTP request, we set the results count to 100 per page (the max possible). There are hardly any repositories with over 100 new issues per week, so this should be fine for our purposes. By default, the `per_page` value is 30.

If the request completes successfully, we use a custom `getDateRange` method to initialize a `payload` variable that we will be able to pass to the `Chart` component. This payload is an array of objects that will like so:

```
[
  {day: "Dec 7th 18", issues: 0},
  {day: "Dec 8th 18", issues: 0},
  {day: "Dec 9th 18", issues: 0},
  {day: "Dec 10th 18", issues: 0},
  {day: "Dec 11th 18", issues: 0},
  {day: "Dec 12th 18", issues: 0},
  {day: "Dec 13th 18", issues: 0}
]
```

After that, we iterate over the API’s response. The data we’re interested in is in an `items` key on a `data` property on the `response` object. From this, we take the `created_at` key (which is a timestamp) and format it as the `day` property in our objects above. From there, we then look up the corresponding date in the `payload` array and increment the issues count for that date by one.

Finally, we assign the `payload` array to our `issues` data property and log the response.

Next, let’s add in the `getDateRange` method:

```
methods: {
  getDateRange() {
    const startDate = moment().subtract(6, 'days');
    const endDate = moment();
    const dates = [];

    while (startDate.isSameOrBefore(endDate)) {
      dates.push({
        day: startDate.format('MMM Do YY'),
        issues: 0
      });

      startDate.add(1, 'days');
    }

    return dates;
  },
  getIssues() { ... }
}
```

Before we get to the visualization bit, let’s also log any errors we might encounter when making our request to the console (for debugging purposes):

```
axios
  .get( ...)
  .then(response => {
    ...
  })
  .catch(error => {
    console.error(error);
  });
```

We’ll add some UX for informing the user in the case that something went wrong later.

So far, we have an input field that lets the user enter the organization/repository name they wish to search issues for. Upon form submission, all issues opened in the past one week are logged to the console.

Below is an example of what was logged on the console for the `facebook/react` repo:

![Console output](Images/console-output.png) 

If you start up the Vue dev server using `npm run serve` and enter some different repos, you should see something similar. If you’re stuck for inspiration, check out [GitHub’s Trending page](https://github.com/trending).

Next comes the fun bit—visualizing this data.

## Drawing a Bar Chart Using D3

Earlier on, we mentioned that all the drawing will be handled inside a `Chart` component. Let’s create the component:

```
touch src/components/Chart.vue
```

D3 works on SVG elements, and for us to draw anything with D3, we need to have an SVG element on the page. In our newly created component (`src/components/Chart.vue`), let’s create an SVG tag:

```
<template>
  <div>
    <svg></svg>
  </div>
</template>
```

For this particular tutorial, we’ll visualize our data using a bar chart. I picked a bar chart because it represents a low complexity visual element while it teaches the basic application of D3.js itself. The bar chart is also a good intro to the most important D3 concepts, while still having fun!

Before proceeding, let’s update our `App` component to include the newly created `Chart` component below the form:

```
<template>
  <div id="app">
    <form action="#" @submit.prevent="getIssues">
      ...
    </form>

    <chart :issues="issues"></chart>
  </div>
</template>
```

Let’s also register it as a component:

```
import Chart from './components/Chart.vue';

export default {
  name: "app",
  components: {
    Chart
  },
  ...
}
```

Notice how we’re passing the value of the `issues` data property to the `Chart` component as a [prop](https://vuejs.org/v2/guide/components-props.html):

```
<chart :issues="issues"></chart>
```

Let’s now update our `Chart` component to make use of that data:

```
<script>
import * as d3 from "d3";
import _ from "lodash";

export default {
  props: ["issues"],
  data() {
    return {
      chart: null
    };
  },
  watch: {
    issues(val) {
      if (this.chart != null) this.chart.remove();
      this.renderChart(val);
    }
  },
  methods: {
    renderChart(issues_val) {
      // Chart will be drawn here
    }
  }
};
</script>
```

In the above code block, we’re importing D3 and Lodash. We then instantiate a `chart` data property as `null`. We’ll assign a value to this when we start drawing later on.

Since we want to draw the chart every time the value of issues changes, we’ve created a [watcher](https://vuejs.org/v2/guide/computed.html#Watchers) for `issues`. Each time this value changes, we’ll destroy the old chart and then draw a new chart.

Drawing will happen inside the `renderChart` method. Let’s start fleshing that out:

```
renderChart(issues_val) {
  const margin = 60;
  const svg_width = 1000;
  const svg_height = 600;
  const chart_width = 1000 - 2 * margin;
  const chart_height = 600 - 2 * margin;

  const svg = d3
    .select("svg")
    .attr("width", svg_width)
    .attr("height", svg_height);
}
```

Here, we set the height and width of the SVG element we just created. The margin attribute is what we’ll use to give our chart some padding.

D3 comes with DOM selection and manipulation capabilities. Throughout the tutorial, you’ll see lot’s of `d3.select` and `d3.selectAll` statements. The difference is that [select](https://github.com/d3/d3-selection#select) will return the first matching element while [selectAll](https://github.com/d3/d3-selection#selectAll) returns all matching elements.

### The Axes

For bar charts, data can either be represented in a vertical or horizontal format. D3 comes with [axis methods](https://github.com/d3/d3-axis/blob/master/README.md#axisTop), which let us define our axes the way we want:

*   axisLeft
*   axisTop
*   axisBottom
*   axisRight

Today, we’ll be creating a vertical bar chart. For vertical bar charts, we’ll only need the `axisLeft` and `axisBottom` methods:

```
renderChart(issues_val) {
  ...

  this.chart = svg
    .append("g")
    .attr("transform", `translate(${margin}, ${margin})`);

  const yScale = d3
    .scaleLinear()
    .range([chart_height, 0])
    .domain([0, _.maxBy(issues_val, "issues").issues]);

  this.chart
    .append("g")
    .call(d3.axisLeft(yScale).ticks(_.maxBy(issues_val, "issues").issues));

  const xScale = d3
    .scaleBand()
    .range([0, chart_width])
    .domain(issues_val.map(s => s.day))
    .padding(0.2);

  this.chart
    .append("g")
    .attr("transform", `translate(0, ${chart_height})`)
    .call(d3.axisBottom(xScale));
}
```

The above block of code draws axes on the SVG element. Let’s go through it step by step:

```
this.chart = svg.append('g')
  .attr('transform', `translate(${margin}, ${margin})`);
```

We first specify where we want our chart to start within the SVG element. When working with D3, for any element we want to be added to the SVG, we usually call the `append` method, then define attributes for this new element.

To add attributes to an element, we usually call the `attr` method, which takes in two parameters. The first parameter is the attribute we want to apply to the selected DOM element, and the second parameter is the value we want, or a callback function that returns the desired value. Here we’re moving the start of the chart to the `60, 60` position of the SVG:

```
const yScale = d3.scaleLinear()
  .range([chart_height, 0])
  .domain([0, _.maxBy(issues_val, 'issues').issues]);

this.chart.append('g')
  .call(d3.axisLeft(yScale)
  .ticks(_.maxBy(issues_val, 'issues').issues));
```

This codeblock draws the y-axis while making use of D3 [scales](https://github.com/d3/d3-scale) to come up with a y-scale. Scales are functions that will transform our data by either increasing or decreasing its value for better visualization.

The `range` function specifies the length that should be divided between the limits of the input data. You may have noticed I used height as the first parameter and not zero when calling range. This is because the SVG coordinate system starts from the top left corner. You’ll get to understand this better when we get to draw the bar heights.

![SVG scale](Images/svg-scale.png) 

On the other hand, the `domain` function denotes minimum and maximum values of the input data. For this particular data set, we want to start from zero to the highest value in our data set. Think of the domain as the input and range as the output.

After defining a y-scale, we make use of this scale to draw the axis by calling the `axisLeft` method, which takes in the `y-scale` as the argument.

The snippet below draws the x-axis:

```
const xScale = d3.scaleBand()
  .range([0, chart_width])
  .domain(issues_val.map((s) => s.day))
  .padding(0.2)

this.chart.append('g')
  .attr('transform', `translate(0, ${chart_height})`)
  .call(d3.axisBottom(xScale));
```

For the `xScale` we use the `scaleBand` function, which helps to split the range into bands and compute the coordinates and widths of the bars with additional padding. Assuming 3 is the maximum number of issues raised across all dates, the chart output should look like this:

![Axes](Images/axes.png) 

If you test this in your browser with the code we’ve covered so far, you should see something similar.

Now enough with the axes. Let’s spit some bars!

### Drawing Bars

For our bar chart, the bar width will be fixed and the bar height will vary depending on the dataset size:

```
renderChart(issues_val) {
  ...

  const barGroups = this.chart
    .selectAll("rect")
    .data(issues_val)
    .enter();

  barGroups
    .append("rect")
    .attr("class", "bar")
    .attr("x", g => xScale(g.day))
    .attr("y", g => yScale(g.issues))
    .attr("height", g => chart_height - yScale(g.issues))
    .attr("width", xScale.bandwidth());
}
```

Let’s address how we added the bars. First, we created a `barGroups` element:

```
const barGroups = this.chart
  .selectAll('rect')
  .data(issues_val)
  .enter()
```

Calling the `selectAll` method on our chart returns an empty selection/array, since we don’t have any rectangles in our chart so far. We then chain the `data` method, passing in the dataset we want visualized. This puts the data in a waiting state for further processing.

The next step is to chain the `enter` method. The `enter` method looks both at the data set we passed into `data()` and at the selection we get after calling `selectAll()`, and then tries to look for “matches”—more like mapping between our sample data and elements already present in the DOM. In this particular case, no matches were found.

#### Select, Enter and Append

[This article](http://knowledgestockpile.blogspot.no/2012/01/understanding-selectall-data-enter.html) is an excellent guide for understanding the `select`, `enter` and `append` sequence when working with D3 to manipulate the DOM.

Since `selectAll('rect')` returned an empty array, the `enter` method will return a new selection representing the elements in our data set.

Note that, after chaining `enter()`, every item in the returned array is acted upon individually. This means that any method chained onto `barGroups` will define the behavior of individual items.

```
barGroups
  .append('rect')
  .attr('class', 'bar')
  .attr('x', (g) => xScale(g.day))
  .attr('y', (g) => yScale(g.issues))
  .attr('height', (g) => chart_height - yScale(g.issues))
  .attr('width', xScale.bandwidth());
```

The code block above creates a rectangle for each item in our in our data set. We give each of these rectangles a class of `bar`.

To set the x and y coordinates for the rectangles, we use the scaling functions we defined earlier. So far, these rectangles are sitting on top of each other, and we need to give our rectangles some height and width.

The width of our bars would be determined by the `scaleBand` function. Chaining the `bandwidth` function to the `xScale` returns a calculated bandwidth from the range and padding provided to the x-scale.

To set the bar height, we subtract the computed y-coordinate of the bar from the height of the SVG to get the correct representation of the value as a column. Remember that, when working with SVGs, x and y coordinates are always calculated starting from the top-left corner.

### Adding Labels

So far we have a bar chart. But this chart is not really helpful, as it doesn’t tell the user what each axis represents. To give our chart more context, we’ll have to add labels for the axes as well as a chart title.

To add labels, we append text elements to our SVG:

```
svg
  .append('text')
  .attr('class', 'label')
  .attr('x', -(chart_height / 2) - margin)
  .attr('y', margin / 2.4)
  .attr('transform', 'rotate(-90)')
  .attr('text-anchor', 'middle')
  .text('Issues opened')

svg
  .append('text')
  .attr('class', 'label')
  .attr('x', chart_width / 2 + margin)
  .attr('y', chart_height + margin * 1.7)
  .attr('text-anchor', 'middle')
  .text('Days')

svg
  .append('text')
  .attr('class', 'title')
  .attr('x', chart_width / 2 + margin)
  .attr('y', 40)
  .attr('text-anchor', 'middle')
  .text('Issues in the past 1 week')
```

The text elements can be positioned with x and y coordinates while text alignment is done with the `text-anchor` attribute. To add the text itself, we call the `text` method on the text element.

We can test things out by serving our app then searching for a repo. Search for any popular repo—such as `facebook/react`:

![React Issues](Images/facebook-react.png) 

Back in our `App` component, we can now get rid of the console statement inside the `getIssues` method:

```
console.log(this.issues)
```

Even though our chart does an excellent job of visualizing our data, there’s still much to be done in terms of the user experience. In the next section, we’ll look at how to add transitions to D3 charts.

### Adding Transitions

For this particular chart, we want to make it such that, when one hovers over a bar element, its shade changes and the number of issues represented by the bar shows up at the top of the bar.

For this to happen, we have to do some [event handling](https://github.com/d3/d3-selection/blob/master/README.md#handling-events) on `mouseEnter` and `mouseLeave` for the `barGroups`.

Edit the `barGroups` code block above the three `svg` blocks:

```
barGroups
  ...
  .attr("width", xScale.bandwidth())
  .on("mouseenter", function(actual, i) {
    d3.select(this)
      .transition()
      .duration(300)
      .attr("opacity", 0.6)
      .attr("x", a => xScale(a.day) - 5)
      .attr("width", xScale.bandwidth() + 10);
    barGroups
      .append("text")
      .attr("class", "value")
      .attr("x", a => xScale(a.day) + xScale.bandwidth() / 2)
      .attr("y", a => yScale(a.issues) - 20)
      .attr("text-anchor", "middle")
      .text((a, idx) => {
        return idx !== i ? "" : `${a.issues} issues`;
      });
  });
```

We call the [transition method](https://github.com/d3/d3-transition/blob/master/README.md#selection_transition) to add animations to an element when working with D3.

Each time the cursor hovers over a bar, we reduce the opacity of the bar and increase the width by `10px`. We also add text on top of the bar, stating the number of issues the bar represents. This transition takes a duration of 300 milliseconds.

Since we don’t want to leave this bar in the new state when the mouse leaves, let’s define a `mouseleave` event, which removes the selection features we had applied in the `mouseenter` event:

```
barGroups
  ...
  .attr("width", xScale.bandwidth())
  .on("mouseenter", function(actual, i) { ... })
  .on("mouseleave", function() {
    d3.selectAll(".issues").attr("opacity", 1);

    d3.select(this)
      .transition()
      .duration(300)
      .attr("opacity", 1)
      .attr("x", a => xScale(a.day))
      .attr("width", xScale.bandwidth());

    svg.selectAll(".value").remove();
  });
```

What we are doing above is setting the opacity of the bar to the original value and also removing the text from the bar.

```
svg.selectAll('.value').remove();
```

The code above removes any text on the DOM that has a class of `value`.

Here’s the final result:

![Transitions](Images/transitions.png) 

If you try things out in your browser now, you should see something like the above.

## Some Final UI/UX Touches

When making the request to GitHub, we anticipate some loading time before getting a response back from GitHub. For UX purposes, we’ll make the user aware we’re still retrieving results from GitHub by flashing a loading alert on the page. In the `App` component, add this snippet to the HTML section of your code—right above the `Chart` component:

```
<div class="alert alert-info" v-show="loading">Loading...</div>
<chart :issues="issues"></chart>
```

For prototyping purposes, we’ll leverage Bootstrap. Vue has an official Bootstrap package that we’re going to install:

```
npm install bootstrap-vue
```

Once the package has been installed, we’ll have to import Bootstrap’s CSS classes to our `main.js` file to make the alert show up:

```
[...]
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
```

We’re almost done, but we need to add a `loading` attribute to our data model—whose value will determine whether or not to show the loading alert:

```
data() {
  return {
    loading: false,
    ...
  };
},
```

Every time we make a new request, we’ll set the value of `loading` to `true`, so the alert shows up, and then we’ll finally set this value to `false` for successful requests or in the case the app errored:

```
getIssues() {
  this.loading = true;
  ...
  axios.get( ... )
  .then( ... )
  .catch( ... )
  .finally(() => (this.loading = false));
}
```

### Error Handling

As it stands, we’re just logging any errors we might run into on the console—something the user isn’t aware of. To make the user is aware if something goes wrong when making the request, we’ll flash an error alert on the page. Add this snippet below the loading alert we just created:

```
<div class="alert alert-danger" v-show="errored">An error occured</div>
<chart :issues="issues"></chart>
```

We also need to update our data model with the `errored` attribute, which we initialize with a `false` value:

```
data() {
  return {
    loading: false,
    errored: false,
    ...
  };
},
```

We’ll set the `errored` value to `true` every time we run into an error. This should happen inside the catch block:

```
 getIssues() {
  this.loading = true;
  this.errored = false;
  ...
  axios.get( ... )
  .then( ... )
  .catch(error => {
    console.error(error);
    this.errored = true;
  })
  .finally( ... );
}
```

### Some Basic Styling

Eagle-eyed readers will have noticed that in the screen shot at the top of this guide, the color of the bars was blue. Let’s add that as a final touch to our `App` component:

```
<style>
.bar {
  fill: #319bbe;
}
</style>
```

## Conclusion

Congratulations for making it to this point. Even though we have a working bar chart, there’s still more we can do to make the chart more visually appealing. We could, for example, add grid lines, or alternatively visualize this data using a line chart.

What we drew was a simple bar chart, but D3.js has amazing capabilities in terms of what you can do. Any data visualization that you’ve seen anywhere—including powerpoint presentations—can probably be handled by D3\. [This article](https://www.sitepoint.com/d3-js-data-visualizations/) is a good read for some of the things D3 is capable of doing. You can also check out D3 on GitHub to see other [use cases](https://github.com/d3/d3/wiki/Gallery).

# Chapter 8: How to Build a Reusable Component with Vue

### by Deji Atoyebi

Vue is a progressive framework that allows you to build your applications as collections of self-contained, reusable components.

Components are used to create what can be called custom HTML elements. Intrinsically, each element bears similar sets of data and functionalities. For example, say you’re building a Twitter-like social network. For the newsfeed, you’ll require a way to present a list of the latest activities to users. Each activity will have a similar set of data: the name of the creator of the activity, the date the activity was published, the actual content, and so on. Also, you’d want users to carry out actions such as liking, unliking and sharing these activities.

In this scenario, simply creating a card component would cut it. And although the card component will populate different activities, the underlying structure of the data as well as functionalities will remain the same. No need to repeat and modify code. After creating the card component, all we’d need to do is to insert it into the body of our HTML document, as we do every other HTML element:

```
<feed-card v-for=”activity for activities”></feed-card>
```

While building a card component for a news feed would be quite an interesting topic, in this tutorial we’d be touching on something different: how to build a re-usable modal component.

#### Live Code

For the impatient among you, [here’s a demo of the code running on CodePen](https://codepen.io/SitePoint/pen/ZVLaBN).

## But Why a Modal?

Modals are a very important, multi-purpose feature of many websites. Their main function is to bring information to the immediate attention of users. They are particularly useful when crucial information is to be passed or an action must be carried out before users gain access to, say, a resource. A common use case of modals is to present an authentication (login or sign-up) form before a user can carry out a particular action. I assume that you’ll be required to create a modal component at least once during your journey as a web developer—hence the importance of this tutorial.

## What To Consider Before Building Our Component

Before we get our hands dirty with actually building a modal component, it’s important to consider a couple of points.

### Do We Use a Single-file Component or Not?

Don’t be deceived by the name: single-file components (SFCs) are just regular components. The “single-file” part is only meant to denote that, rather than your component being defined in the HTML file in which it’s used, alongside the root Vue instance, it would be defined in a file of its own. This comes with its own advantages, part of which is reusability (if you’re building a non-trivial web app that uses your component in different HTML pages).

In this tutorial, we’ll leverage Vue’s incremental adoptability. We’ll start by building everything in one file and including Vue from a CDN, then in a second step, we’ll look at how to refactor things into an SFC.

### Do We Use ES6 or Not?

If you’re going to be using Vue at all, you need to decide whether or not your code will make use of ES6 features. Using ES6 features comes with cross-browser compatibility issues, often meaning you’ll need to use Babel to transpile it to something older browsers can understand.

For the code in this guide, we’ll use ES6 throughout. It’s a ratified standard, after all, and we’re in the favorable position of not having to support ancient browsers. Note that when we convert the modal to SFCs, the JavaScript will be bundled and transpiled via webpack.

### Important Components and Behavior

What are the important components of a modal and how do we expect our modal to behave?

Every modal has two common components to it: the mask and the container (let’s call them that). The mask is the transparent dark (or white) background that appears with most modals. The modal overlies the rest of the content in the page. Once you click on a mask, the modal exits. The container, on the other hand, is the part of the modal that “contains” the important stuff.

With this knowledge, creating a reusable modal component becomes super easy, as we’ve been able to whittle down its design into its two major parts.

We’ll use [Materialize](https://materializecss.com/) for our design, as we don’t want to get too stuck with writing too much code in CSS.

## Building the Modal Component

Now it’s time for the fun stuff. First, create a file named `modal.html` and add the following code. This pulls in our dependencies from a CDN and defines the HTML structure for our mask and container:

```
<!DOCTYPE html>
<html>
  <head>
  <meta charset="utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <title>Page Title</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
  <style></style>
</head>
<body>
  <div class="container">
    <div class="modal-mask">
      <div class="modal-container"></div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/vue@2.5.21/dist/vue.js"></script>
  <script></script>
</body>
</html>
```

Next, let’s add in some basic styles to the `<style>` block in the `<head>` section:

```
.modal-mask{
  position: fixed;
  z-index: 100;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .3);
  overflow-y:auto;
}
.modal-container {
  width: 80%;
  height: auto;
  margin: 50px auto 0;
  position: relative;
  padding: 16px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
  box-sizing: border-box;
}
```

Open the file in your browser. You’ll see that the modal mask is a transparent dark background. The height and width are set to 100%, as we want it to occupy the whole page while the modal is in focus. The modal’s container is a `<div>` element that occupies 80% of the width of the mask. Feel free to customize yours however you wish.

### Creating a Vue Component

The next step is to make a Vue component out of our modal. Add the following code to the final `<script>` block:

```
new Vue({
  el: ".container",
  data() {
    return {};
  }
});
```

The code for the modal now needs to be wrapped in a `<template>` block so that it can be referenced in the script defining the modal as a component:

```
<div class="container"></div>

<template id="modal-template">
  <div class="modal-mask">
    <div class="modal-container"></div>
  </div>
</template>
```

Now, we can define our modal as a Vue component:

```
Vue.component("modal", {
  template: "#modal-template"
});

new Vue({ ... });
```

Now, when you open up your `modal.html`, you’d find that there’s absolutely nothing shown in the page. This is because the `<template>` block wasn’t rendered when the page was being created.

### Showing and Hiding the Modal

At this point, we should touch on how to call our modal. Let’s model it after a real-word situation: the modal will display when a button is clicked. Thus, insert a button to the container div, along with our modal:

```
<div class="container">
  <button> Show Modal </button>
  <modal></modal>
</div>
```

Since the button does absolutely nothing for now, we need to work on both the root Vue instance and the modal component so that the modal appears when the button is clicked. First, change the code in your root instance:

```
new Vue({
  el: ".container",
  data() {
    return {
      showModal: false
    };
  },
  methods: {
    actShowModal() {
      this.showModal = true;
    }
  }
});
```

In the above, we initialized `showModal` in our root instance to indicate when our modal is being shown to a user and when it’s not. We also added a method to manipulate this data property. As you’ll soon see, calling `actShowModal` will make our modal pop up.

The next task is to enable our `<button>` to call `actShowModal` when it’s clicked:

```
<button v-on:click="actShowModal">Show Modal</button>
```

Unfortunately, clicking the button still makes no difference. This is because we haven’t hooked up our modal component to the data in our root instance. What we want is for our modal to display when `showModal` is `true` and disappear when `showModal` is `false`. The way to achieve this is by using [props](https://vuejs.org/v2/guide/components-props.html). Our code should now be:

```
<modal :show_modal="showModal"></modal>
```

And:

```
Vue.component("modal", {
  template: "modal-template",
  props: ["show_modal"]
});
```

Now that we’ve added the `show_modal` as a prop, we need our modal to appear when `show_modal` is true. This requires a simple change in the template of our modal component:

```
<template id="modal-template">
  <div class="modal-mask" v-if='show_modal'>
    <div class="modal-container"></div>
  </div>
</template>
```

Now, open up `modal.html`. Notice that, when you click the button, the modal pops up. Great! But there’s still a problem: there’s no way to close the modal … yet.

We need the modal to disappear when we click on the mask. To achieve this, `showModal` would have to be `false`, and we need to make this happen from the modal component since it houses the mask.

First, create a method called `closeModal` in the component that emits the change:

```
Vue.component("modal", {
  ...
  methods: {
    closeModal() {
      this.$emit("close_modal");
    }
  }
});
```

And then change the code of your template so it looks like this:

```
<template id="modal-template">
  <div class="modal-mask" v-if="show_modal" @click="closeModal">
    <div class="modal-container"></div>
  </div>
</template>
```

Now when the mask is clicked, the modal component emits a `close_modal` event. Let’s catch that event in our root Vue instance and toggle the modal’s display state to `false`:

```
<modal :show_modal="showModal" @close_modal="actCloseModal"></modal>
```

Also this:

```
methods: {
  actShowModal(){ ... },
  actCloseModal(){
    this.showModal = false;
  }
},
```

Now, our modal should close when the mask is clicked—which is super awesome. But there’s yet another problem: clicking the modal’s container also closes the modal.

A simple explanation for this is that the click event propagates (bubbles up). To stop that, let’s use Vue’s way of stopping such propagation, the [`@click.stop` event modifier](https://vuejs.org/v2/guide/events.html#Event-Modifiers):

```
<template id="modal-template">
  <div class="modal-mask" v-if="show_modal" @click="closeModal">
    <div class="modal-container" @click.stop></div>
  </div>
</template>
```

There, solved! Our modal works the way it should now. Take some time to run the code we have so far and make sure it works correctly.

## Creating an Authentication Modal

Currently, our modal container is empty. Let’s change that and write some code to build a login form to be embedded in this container.

Let’s start off by adding our login form into the mix. Remember, the Materialize framework is to be used, so don’t be too bothered about the HTML class definitions:

```
<template id="modal-template">
  <div class="modal-mask" v-if="show_modal" @click="closeModal">
    <div class="modal-container clearfix" @click.stop>
      <h4 class="blue-text">Login</h4>
      <form class="col s12">
        <div class="input-field col s12">
          <input v-model="email" id="email_address" type="text">
          <label for="email_address">Email Address</label>
        </div>
        <div class="input-field col s12 ">
          <input v-model="password" id="password" type="text" >
          <label for="password">Password</label>
        </div>
        <a class="waves-effect waves-light btn form-btn teal">Sign in</a>
      </form>
    </div>
  </div>
</template>
```

And add the following to style the form’s button:

```
.form-btn {
  float: right;
}
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
```

We aren’t going to implement a back end for the authentication component, so it’s reasonable that our button does nothing. Nonetheless, let’s define the `email` and `password` data properties on our component, as we already have our inputs in the login form pointing to them through the [v-model directive](https://vuejs.org/v2/guide/forms.html). This would be useful for implementing form validation. We won’t do that in this tutorial, but you can read more about this in our tutorial *A Beginner’s Guide to Working with Forms in Vue* in this Vue series:

```
Vue.component("modal", {
  template: "#modal-template",
  props: ["show_modal"],
  data() {
    return {
      email: "",
      password: ""
    };
  },
  methods: { ... }
});
```

Open up your `modal.html`, and … boom! We’ve just created a login modal all by ourselves.

Since everything works nice and smoothly, we’re afforded the opportunity to think of sleeker ways of doing things.

## Making Our Modal Reusable with Slots

Although our modal is now great and usable, there’s still a little problem: the login form is tightly knitted to the modal component. So, at the moment, if we wanted to have different modals in our application—perhaps one for user registration and another for something else—we’d have to repeat our code by creating yet another modal component from scratch.

Is there a way to keep the skeleton of the modal component separate while we plug in whatever content we wish? You bet there is.

With what we have already, it’s easy to separate our login form from the modal component so that we can use the latter for other content when we need to. It all starts with creating a separate login component that would have the data and methods that are required for a login form to operate:

```
Vue.component("login", {
  template: "#login-template",
  data() {
    return {
      email: "",
      password: ""
    };
  }
});
```

Here’s the code defining login template:

```
<template id="login-template">
  <div class="clearfix">
    <h4 class="blue-text">Login</h4>
    <form class="col s12">
      <div class="input-field col s12">
        <input v-model="email" id="email_address" type="text">
        <label for="email_address">Email Address</label>
      </div>
      <div class="input-field col s12 ">
        <input v-model="password" id="password" type="text" >
        <label for="password">Password</label>
      </div>
      <a class="waves-effect waves-light btn form-btn teal">Sign in</a>
    </form>
  </div>
</template>
```

Let’s not forget to rid the modal container of the login form, as we no longer need it. Right now, what we need is to define a [slot](https://vuejs.org/v2/guide/components-slots.html) in the modal container, since that’s where we want any and every content in the modal to live:

```
<template id="modal-template">
  <div class="modal-mask" v-if="show_modal" @click="closeModal">
    <div class="modal-container" @click.stop>
      <slot></slot>
    </div>
  </div>
</template>
```

Also, delete the email and password keys in the modal component; those are now properties of our login component, just as they ought to be. The modal component’s definition should now look something like this:

```
Vue.component("modal", {
  template: "#modal-template",
  props: ["show_modal"],
  methods: {
    closeModal() {
      this.$emit("close_modal", false);
    }
  }
});
```

Inserting our login component into the modal component as provided by our slot takes this simple step:

```
<modal :show_modal="showModal" @close_modal="actCloseModal">
  <login></login>
</modal>
```

Preview your modal and you’ll find that everything works fine: the login component is rendered into the modal component.

### Adding a Registration Component

To go ahead to show how reusable this modal component is now, let’s create a registration component that will also be rendered in the modal component. This will be similar to creating our login component: first, write code for the template and then the component definition.

```
<template id="registration-template">
  <div class="clearfix">
    <h4 class="blue-text">Register</h4>
    <form class="col s12">
      <div class="input-field col s6">
        <input v-model="firstName" placeholder="" id="first_name" type="text">
        <label for="first_name">First Name</label>
      </div>

      <div class="input-field col s6">
        <input v-model="lastName" id="last_name" type="text">
        <label for="last_name">Last Name</label>
      </div>

      <div class="input-field col s12">
        <input v-model="username" id="username" type="text" class="">
        <label for="username">Username</label>
      </div>

      <div class="input-field col s12">
        <input v-model="email" id="email_address" type="text">
        <label for="email_address">Email address</label>
      </div>

      <div class="input-field col s12">
        <input v-model="password" id="password" type="password">
        <label for="password">Password</label>
      </div>

      <a class="waves-effect waves-light btn teal form-btn">Proceed</a>
    </form>
  </div>
</template>
```

The component definition:

```
Vue.component("register", {
  template: "#registration-template",
  data() {
    return {
      firstName: "",
      lastName: "",
      username: "",
      email: "",
      password: ""
    };
  }
});
```

What we’re hoping to do is to render the login or register component into the modal component separately. Say there are two buttons in a web page and while one shows the login modal when clicked, the other shows the registration modal. We should have this as our code:

```
<modal :show_modal="showModal" @close_modal="actCloseModal" choice="choice">
  <login v-if="choice === 'login'"></login>
  <register v-else-if="choice === 'register'"></register>
</modal>
```

As the code suggests, there’s a data property on our root instance named `choice` that could either be “login” or “register”. This is then used in our modal component as a prop, as can be seen in the following code:

```
Vue.component("modal", {
  template: "#modal-template",
  props: ["show_modal", "choice"],
  methods: { ... }
});

Vue.component("login", { ... });
Vue.component("register", { ... });

new Vue({
  el: ".container",
  data() {
    return {
      showModal: false,
      choice: ""
    };
  },
  methods: { ... }
});
```

Next, let’s create the aforementioned two buttons—one to show the login modal, and the other to show the registration modal. So now we have these:

```
<div class="container">
  <button v-on:click="actShowModal('login')"> Login </button>
  <button v-on:click="actShowModal('register')"> Register </button>

  <modal :show_modal="showModal" @close_modal="actCloseModal" choice="choice">
    <login v-if="choice === 'login'"> </login>
    <register v-else-if="choice === 'register'"></register>
  </modal>
</div>
```

Our `actShowModal` method is defined on the root instance will then change to accept a choice as argument:

```
new Vue({
  el: ".container",
  data() { ... },
  methods: {
    actShowModal(choice) {
      this.choice = choice;
      this.showModal = true;
    },
    actCloseModal() {
      this.showModal = false;
    }
  }
});
```

### Some Accessibility Improvements

One thing that we shouldn’t overlook is that people may be using a keyboard to navigate our modal. Let’s make life better for them:

```
<div class="container" @keyup.escape.stop="actCloseModal()">
  ...
</div>
```

This will let the modal be dismissed by pressing the `Esc` key.

When the modal opens, you might also want to focus the first element in the form. This would be done by creating a [custom directive](https://vuejs.org/v2/guide/custom-directive.html) like so:

```
Vue.directive("focus", {
  inserted: el => {
    el.focus();
  }
});
```

You can apply this to any element that should receive focus. In our case, this will be the first input element in either form:

```
<input v-model="email" id="email_address" type="text" v-focus>
<input v-model="firstName" placeholder="" id="first_name" type="text" v-focus>
```

And now, we’re all done! Our modal component nicely renders both the register and login components based on the button we click. Open your `modal.html` to see the outcome.

#### Live Code

![image of code demo](Images/modals.png)

[Here’s a demo of the code running on CodePen](https://codepen.io/SitePoint/pen/ZVLaBN).

What we’ve done is quite valuable, in that it prevents unnecessary code duplication. We’ve ended up creating a somewhat one-size-fits-all modal component. However, to make it perfectly reusable, we need to turn it and other components to SFCs and use webpack to bundle our code as well as transpile it so that it works on all major browsers. We’ll do this in the next part of this tutorial.

## Single-file Components

Single-file components are a clean way to achieve modularity while working with Vue.js. They allow us to create `.vue` files which house our components, and they also come in handy when we’re working on a complex application and would like to avoid the clutter that writing Vue code in an HTML file presents. In our case, turning our `Modal`, `Registration` and `Login` components into SFCs helps prevent the extremely clunky act of copying and pasting code for reuse.

Since your browser cannot read `.vue` files, we’ll be using [Vue CLI](https://cli.vuejs.org/) to scaffold a project. Under the hood, this uses webpack as well as a couple of other dependencies to bundle our code.

Let’s get started.

### Basic Setup

To use the CLI, you’ll need a recent version of Node.js installed on your system. You can do this by downloading the binaries from the [official website](https://nodejs.org/), or by using a [version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). This is probably the easiest way, as it allows you to manage multiple versions of Node on the same machine.

Next, proceed to installing Vue CLI globally on your machine with the following command:

```
npm install -g @vue/cli
```

Create a scaffold for our project with the following command:

```
vue create my-modal
```

Select the default preset, then when the CLI has finished installing all the dependencies, change into this directory:

```
cd my-modal
```

Next, let’s install the Materialize dependency:

```
npm i materialize-css
```

Open up `src/main.js` so that we can include it and make it global to our application:

```
import Vue from "vue";
import App from "./App.vue";
import "materialize-css/dist/css/materialize.min.css";
import "materialize-css/dist/js/materialize.min.js";

Vue.config.productionTip = false;
Vue.directive("focus", {
  inserted: el => {
    el.focus();
  }
});

new Vue({
  render: h => h(App)
}).$mount("#app");
```

While we’re at it, we can add our custom directive, too.

### Creating Our Single-file Components

Open up `src/App.vue` and replace the code with the following:

```
<template>
  <div class="container" @keyup.escape.stop="actCloseModal()">
    <button v-on:click="actShowModal('login')"> Login </button>
    <button v-on:click="actShowModal('register')"> Register </button>

    <modal :show_modal="showModal" @close_modal="actCloseModal" choice="choice">
      <login v-if="choice === 'login'"></login>
      <register v-else-if="choice === 'register'"></register>
    </modal>
  </div>
</template>

<script>
import modal from "./components/modal.vue";
import login from "./components/login.vue";
import register from "./components/register.vue";

export default {
  name: "app",
  components: {
    modal,
    login,
    register
  },
  data() {
    return {
      showModal: false,
      choice: ""
    };
  },
  methods: {
    actShowModal(choice) {
      this.choice = choice;
      this.showModal = true;
    },
    actCloseModal() {
      this.showModal = false;
    }
  }
};
</script>

<style>
body {
  padding: 15px;
}
</style>
```

There’s nothing new going on here in terms of functionality, but notice how much more organized the code is.

Next, create the components we’re going to need in the `src/components` folder:

```
touch src/components/{modal.vue,register.vue,login.vue}
```

When you’re finished, the `src` folder should look like this:

```
.
├── App.vue
├── assets
│   └── logo.png
├── components
│   ├── login.vue
│   ├── modal.vue
│   └── register.vue
└── main.js
```

The final thing that remains to do is to add the code to these components.

In `modal.vue`:

```
<template id="modal-template">
  <div class="modal-mask" v-if="show_modal" @click="closeModal">
    <div class="modal-container" @click.stop>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "modal",
  props: ["show_modal", "choice"],
  methods: {
    closeModal() {
      this.$emit("close_modal", false);
    }
  }
};
</script>

<style>
.modal-mask{
  position: fixed;
  z-index: 100;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .3);
  overflow-y:auto;
}
.modal-container {
  width: 80%;
  height: auto;
  margin: 50px auto 0;
  position: relative;
  padding: 16px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
  box-sizing: border-box;
}
.form-btn {
  float: right;
}
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
</style>
```

Here we’re declaring our CSS, as it pertains more to the modal than the other components. Were we to add a `scoped` attribute, the definitions would only be available to the template in this file.

In `login.vue`:

```
<template id="login-template">
  <div class="clearfix">
    <h4 class="blue-text">Login</h4>
    <form class="col s12">
      <div class="input-field col s12">
        <input v-model="email" id="email_address" type="text" v-focus>
        <label for="email_address">Email Address</label>
      </div>
      <div class="input-field col s12 ">
        <input v-model="password" id="password" type="text" >
        <label for="password">Password</label>
      </div>
      <a class="waves-effect waves-light btn form-btn teal">Sign in</a>
    </form>
  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    return {
      email: "",
      password: ""
    };
  }
};
</script>
```

And in `register.vue`:

```
<template id="registration-template">
  <div class="clearfix">
    <h4 class="blue-text">Register</h4>
    <form class="col s12">
      <div class="input-field col s6">
        <input v-model="firstName" placeholder="" id="first_name" type="text" v-focus>
        <label for="first_name">First Name</label>
      </div>

      <div class="input-field col s6">
        <input v-model="lastName" id="last_name" type="text">
        <label for="last_name">Last Name</label>
      </div>

      <div class="input-field col s12">
        <input v-model="username" id="username" type="text" class="">
        <label for="username">Username</label>
      </div>

      <div class="input-field col s12">
        <input v-model="email" id="email_address" type="text">
        <label for="email_address">Email address</label>
      </div>

      <div class="input-field col s12">
        <input v-model="password" id="password" type="password">
        <label for="password">Password</label>
      </div>

      <a class="waves-effect waves-light btn teal form-btn">Proceed</a>
    </form>
  </div>
</template>

<script>
export default {
  name: "register",
  data() {
    return {
      firstName: "",
      lastName: "",
      username: "",
      email: "",
      password: ""
    };
  }
};
</script>
```

And that’s all there is to it. If you now spin up the dev server using the command `npm run serve`, you’ll be able to see your app running at [http://localhost:8080](http://localhost:8080).

## Conclusion

In this tutorial, I’ve demonstrated how to build a simple modal component. We looked at basic accessibility features, how to design the modal so as to be reusable, and finally how to use Vue CLI to structure our app as single-file components.

I hope I’ve shown how easy it can be to get started building components of your own, as well as how Vue’s component-based approach makes it a joy to build an interface in such a declarative way.

# Chapter 9: How to Build a Game with Vue.js

### by Ivaylo Gerchev

One the reasons I like [Vue.js](https://vuejs.org) so much is that it can be used in a wide variety of scenarios and can be integrated into many different kinds of projects. So to me, Vue is a universal, multipurpose framework. In this aspect, it reminds me of the Python programming language, which is also easy to learn and use, and can be applied in many areas.

In this tutorial, we’ll explore one of the less obvious uses for Vue—game development.

#### This Tutorial’s Code Repository

The code for this tutorial [can be found on GitHub](https://github.com/sitepoint-editors/match-pairs). You can also view [a demo of the finished game here](https://sitepoint-editors.github.io/match-pairs/).

## Why Vue Instead of a Real Game Development Framework

Obviously, Vue is not tailored to game development. So why we would want to choose it instead of a real game development framework/engine? Well, let’s explore two good reasons:

1.  If you’re familiar with Vue and/or you work with it on a daily basis, you already have the necessary skills and knowledge. To create a game with Vue, you just apply what you already know while shifting your mind to a different context—instead of having to learn a whole new game framework.
2.  Vue offers features that make game development easy:
    *   [Vue’s reactivity system](https://vuejs.org/v2/guide/reactivity.html) allows for building highly interactive interfaces with minimum effort.
    *   Transitions and animations are an essential part of most games. Vue has [built-in support for them](https://vuejs.org/v2/guide/transitions.html).
    *   [Vue’s ecosystem](https://github.com/vuejs/awesome-vue) is rich enough to supply you with whatever feature you need for your game project.

## Planning the Game

What we’re going to build today is an electronic variant of the popular [Match Pairs game](https://en.wikipedia.org/wiki/Concentration_(game)). Let’s now lay out the features we want to implement, along with the components we’ll need for that.

The game UI will be composed of four components:

*   A cards board, which will hold the cards.
*   An animated countdown timer, which will display the time remaining for the player to match all the pairs. When the time remaining is 10 seconds or less, the color of the timer will change to red.
*   A status bar, which will display the number of the turns taken and matches found.
*   A splash screen, which will show up when the game is finished—either because the time ran out or because all pairs were discovered. It will display a “You Lose!” or “You Win!” message accordingly, as well as the game’s score.

Here are three screenshots showing the starting, playing, and finishing phases of the game:

![](Images/game_start.png)  ![](Images/game_progress.png)  ![](Images/game_finish.png) 

## Getting Started

Now it’s time for action. To follow along with this, you’ll need to have Node, npm and [Vue CLI](https://cli.vuejs.org/) installed on your system.

To install Node (and by default npm), you can download the binaries for from the [official website](https://nodejs.org/), or use a [version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). This is probably the easiest way, as it allows you to manage multiple versions of Node on the same machine.

To install the CLI run:

```
npm i -g @vue/cli
```

That done, we’ll create a new `match-pairs` project, selecting the “default” preset when prompted:

```
vue create match-pairs
cd match-pairs
```

Next, we add the [Vuetify plugin](https://vuetifyjs.com/en/):

```
vue add vuetify
```

Again, choose the “default” preset, which has the [a la carte system](https://vuetifyjs.com/en/framework/a-la-carte) enabled. To activate it, we need to create a `webpack.config.js` file, in the project’s root, with the following content:

```
const VuetifyLoaderPlugin = require('vuetify-loader/lib/plugin')
module.exports = {
  plugins: [
    new VuetifyLoaderPlugin()
  ]
}
```

Now let’s add two more packages that we’ll need—[Lodash](https://lodash.com/) and [MomentJS](http://momentjs.com/):

```
npm i lodash moment
```

Finally, we can run the app with this command:

```
npm run serve
```

## Preparing the Project Files and Components

Now we need to do some preparation.

First, we need to modify the `src/main.js` file. We swap its content with the following:

```
import Vue from 'vue'
import './plugins/vuetify'
import App from './App.vue'

import _ from 'lodash'

Vue.config.productionTip = false

new Vue({
  render: h => h(App),
}).$mount('#app')
```

Now, in the `src/components` directory, we delete the `HelloWorld.vue` example file and create the necessary components for the game: `CardsBoard.vue`, `Timer.vue`, `StatusBar.vue`, and `Splash.vue`.

Next, we open `src/App.vue`, delete the content and insert the following instead:

```
<template>
  <v-app dark>
    <v-container>
      <v-layout class="font-weight-bold display-3 purple--text" justify-center mb-4>Match Pairs</v-layout>
      <v-layout mb-4>
        <timer></timer>
        <status-bar></status-bar>
      </v-layout>
      <cards-board></cards-board>
    </v-container>
    <splash></splash>
  </v-app>
</template>
```

Here, we construct the game layout using the components we’ve just created.

Next, we populate the script with the following:

```
<script>
const cardsSet = [
  {
    name: "php",
    img: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/74196/php-logo_1.png"
  },
  {
    name: "css3",
    img: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/74196/css3-logo.png"
  },
  ...
];

let shuffleCards = () => {
  let cards = [].concat(_.cloneDeep(cardsSet), _.cloneDeep(cardsSet));
  return _.shuffle(cards);
};

import CardsBoard from "./components/CardsBoard";
import StatusBar from "./components/StatusBar";
import Timer from "./components/Timer";
import Splash from "./components/Splash";
import _ from "lodash";
import moment from "moment";

export default {
  name: "App",
  components: {
    CardsBoard,
    StatusBar,
    Timer,
    Splash
  },
  data() {
    return {
      cards: [],
      started: false,
      duration: 120000,
      progress: 0,
      time: null,
      timer: null,
      flipBackTimer: null,
      turns: 0,
      matches: 0,
      showSplash: false,
      result: "",
      score: 0
    };
  },
  created() {
    this.resetGame();
  },
  methods: {
    resetGame() {
      this.started = false;
      this.progress = 0;
      this.time = null;
      this.turns = 0;
      this.matches = 0;
      this.showSplash = false;
      this.score = 0;

      let cards = shuffleCards();

      _.each(cards, card => {
        card.flipped = false;
        card.found = false;
      });

      this.cards = cards;
    },
  }
};
</script>
```

First, we add the necessary images for the cards. For the sake of brevity, I’ve left many of them out. You can get the [full list from the GitHub repo](https://github.com/sitepoint-editors/match-pairs/blob/master/src/App.vue).

The `shuffleCards()` function doubles the images to make them pairs and shuffles them all.

Next, we import our components and register them in the `components` object. We also import Lodash and Moment.

After that, we define all data properties which we’ll need for the game. We add the `created()` hook, which will invoke the `resetGame()` method on the app’s creation. The `resetGame()` turns back all data properties to their initial states.

Now we can add some helper methods used to manage `flipped` and `found` states of the cards:

```
methods: {
  ...

  flippedCards() {
    return _.filter(this.cards, card => card.flipped);
  },

  sameFlippedCard() {
    let flippedCards = this.flippedCards();
    if (flippedCards.length == 2) {
      if (flippedCards[0].name == flippedCards[1].name) return true;
    }
  },

  setCardFounds() {
    _.each(this.cards, card => {
      if (card.flipped) card.found = true;
    });
  },

  checkAllFound() {
    let foundCards = _.filter(this.cards, card => card.found);
    if (foundCards.length == this.cards.length) return true;
  },

  clearFlips() {
    _.map(this.cards, card => (card.flipped = false));
  },

  clearFlipBackTimer() {
    clearTimeout(this.flipBackTimer);
    this.flipBackTimer = null;
  },
}
```

Here is what the helpers do:

*   `flippedCards()` returns all flipped cards—that is, those having `flipped` property set to true
*   `sameFlippedCard` uses the above helper to check whether two flipped cards are same
*   `setCardFounds()` sets the flipped cards as found
*   `checkAllFound` checks whether all cards are found
*   `clearFlips()` clears all flipped cards
*   `clearFlipBackTimer` resets the timer used when we flip the cards.

Finally, we add methods for starting and finishing the game:

```
methods: {
  ...

  startGame() {
    this.started = true;
    let duration = this.duration;
    this.timer = setInterval(() => {
      if (duration == 1000) {
        this.finishGame();
      }
      duration -= 1000;
      this.time = moment(duration).format("mm:ss");
      this.progress = (duration / this.duration) * 100;
    }, 1000);
  },

  finishGame() {
    this.started = false;
    clearInterval(this.timer);
    this.score = Math.round(this.progress) * 10 * this.matches;

    if (this.matches == cardsSet.length) {
      this.result = "Win";
    } else {
      this.result = "Lose";
    }

    this.showSplash = true;
  }
}
```

As we’ll see a bit later, `startGame()` is called after we flip the first card. It creates the game timer, which is used in the `Timer.vue` component. It also updates the `time` and `progress` props. When one second is left, the `finishGame()` is called. The latter clears the game timer, calculates the `score` and `result` props, and activates the splash screen.

## Building the Game Components

Okay, it’s time to build the components we created earlier.

### The CardsBoard Component

We open the `CardsBoard.vue` and put the following:

```
<template>
  <v-layout>
    <v-flex xs12 sm10 offset-sm1 lg8 offset-lg2>
      <v-card>
        <div class="flex-container">
          <div
            v-for="(card, i) in cards"
            :key="i"
            class="card"
            :class="{ flipped: card.flipped, found: card.found }"
            @click="flipCard(card)"
          >
            <div class="back"></div>
            <div class="front" :style="{ backgroundImage: 'url(' + card.img + ')' }"></div>
          </div>
        </div>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  props: ["cards"],
  methods: {
    flipCard(card) {
      this.$emit("flipcard", card);
    }
  }
};
</script>
```

Here, we use the `v-for` directive to populate the board with the cards by using the passed `cards` prop. For each card we bind `.flipped` and/or `.found` class(es), depending on the states of their `flipped` and `found` props. We create the back and front faces of the cards and populate the front using the `img` prop. And of course, we add a click event listener, which will emit a `flipcard` event.

For the code above to work, we’ll need some CSS. So we put this in the style section:

```
<style>
.flex-container {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
}
.card {
  position: relative;
  width: 100px;
  height: 150px;
  margin: 1px;
  transition: opacity 0.5s;
}
@media only screen and (max-width: 768px) {
  .card {
    width: 50px;
    height: 75px;
  }
}
.card .front,
.card .back {
  border-radius: 5px;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  transition: transform 0.3s;
  transform-style: preserve-3d;
}
.card .back {
  background-image: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/102308/card_backside.jpg");
  background-size: 100%;
  background-repeat: no-repeat;
}
.card .front {
  transform: rotateY(-180deg);
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: center;
  background-color: white;
}
.card.flipped .back,
.card.found .back {
  transform: rotateY(180deg);
}
.card.flipped .front,
.card.found .front {
  transform: rotateY(0deg);
}
.card.found {
  opacity: 0.3;
}
</style>
```

I’m not going into too much detail here. Basically, these styles create correct cards layout and add flipping transitions.

Now, let’s move to the `App.vue` and add the following:

```
<cards-board :cards="cards" @flipcard="flipCard"></cards-board>
```

Here, we bind the `cards` prop and register the `flipcard` event listener. Now, let’s add the `flipCard()` method to the `methods` in the script section:

```
methods: {
  ...

  flipCard(card) {
    if (card.found || card.flipped) return;

    if (!this.started) {
      this.startGame();
    }

    let flipCount = this.flippedCards().length;
    if (flipCount == 0) {
      card.flipped = !card.flipped;
    } else if (flipCount == 1) {
      card.flipped = !card.flipped;
      this.turns += 1;

      if (this.sameFlippedCard()) {
        this.matches += 1;
        this.flipBackTimer = setTimeout(() => {
          this.clearFlipBackTimer();
          this.setCardFounds();
          this.clearFlips();

          if (this.checkAllFound()) {
            this.finishGame();
          }
        }, 1000);
      } else {
        this.flipBackTimer = setTimeout(() => {
          this.clearFlipBackTimer();
          this.clearFlips();
        }, 1000);
      }
    }
  }
}
```

First, if we click on a flipped or found card, the function will terminate. If `started` is `false`, it will start the game. Next, when we open the first card, it will change its `flipped` prop to `true`. When we open the second card, it will change its `flipped` prop to `true` and will increase the `turns` prop. Next, if the cards are the same, it will increase the `matches` prop and set a `flipBackTimer`. It will wait one second and will set the cards `found` props to `true`, and will clear the flipped cards. If all cards are found, the game will finish. If the two opened cards are not same, it will just clear the flipped cards.

### The Timer Component

Open `Timer.vue` and add the following:

```
<template>
  <v-layout justify-end>
    <v-progress-circular
      :rotate="-90"
      :value="progress"
      :size="70"
      :width="9"
      :color="color"
    >{{time}}</v-progress-circular>
  </v-layout>
</template>

<script>
export default {
  props: ["progress", "time"],
  data() {
    return {
      color: "success"
    };
  },
  watch: {
    progress() {
      if (this.progress <= 10) {
        this.color = "red";
      } else {
        this.color = "success";
      }
    }
  }
};
</script>
```

Here, we use the [Vuetify Progress component](https://vuetifyjs.com/en/components/progress). We need to change the timer’s color dynamically depending on the `progress` value. In order to update the `progress` prop constantly, we need to add a [watcher](https://vuejs.org/v2/guide/computed.html#Watchers) for it.

Now we move to `App.vue` and bind the passed props:

```
<timer :progress="progress" :time="time"></timer>
```

### StatusBar

Open `StatusBar.vue` and add the following:

```
<template>
  <v-layout align-center class="headline">
    <span class="mx-3">Turns: {{ turns }}</span>
    <v-divider vertical></v-divider>
    <span class="mx-3">Matches: {{ matches }}</span>
  </v-layout>
</template>

<script>
export default {
  props: ["turns", "matches"]
};
</script>
```

Here, we just pass the `turns` and `matches` props, and use them in the template.

In `App.vue`, we bind the passed props:

```
<status-bar :turns="turns" :matches="matches"></status-bar>
```

### Splash

Finally, open `Splash.vue` and add the following:

```
<template>
  <v-layout row>
    <v-dialog v-model="showSplash" persistent max-width="300">
      <v-card class="text-xs-center">
        <v-card-text>
          <div class="headline mb-4">You {{result}}!</div>
          <div>Score: {{score}}</div>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="green darken-1" flat @click="resetGame">Start New Game</v-btn>
          <v-spacer></v-spacer>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-layout>
</template>

<script>
export default {
  props: ["showSplash", "result", "score"],
  methods: {
    resetGame() {
      this.$emit("resetgame");
    }
  }
};
</script>
```

We use the [Vuetify Dialog component](https://vuetifyjs.com/en/components/dialogs) for the splash screen. The splash will show up when the `showSplash` is `true`.

In `App.vue`, we bind the passed props and register the emitted `resetgame` event:

```
<splash :showSplash="showSplash" :result="result" :score="score" @resetgame="resetGame"></splash>
```

And with that, our journey into the world of game development is at an end. Now, just start the game (`npm run serve`) and enjoy!

## Conclusion

As you saw, building a game with Vue is easy and fun. In many cases, Vue can successfully replace a real game framework. With a little imagination and some effort we can create interesting and creative games with different levels of complexity. Check [this collection](https://madewithvuejs.com/games) for some examples. Happy game development!

# Chapter 10: Build a Shopping List App with Vue, Vuex and Bootstrap Vue

### by Michael Wanyoike

As a Vue app grows, keeping track of state throughout the app can become a tricky process. For example, a given piece of state might need to be used in multiple components. Or maybe it’s needed by a component which is nested several components deeper than the one in which it’s stored.

[Vuex](https://vuex.vuejs.org/) is the official state management solution for Vue and is designed to help you manage state throughout your app as your application grows. In this tutorial, I’ll offer a practical example of how to get up and running with Vuex by building a shopping list app (which is a glorified to-do app, to be honest).

#### Demo and Code

If you’re curious to see what we’ll end up with, you can view [the live version running on CodeSandbox](https://codesandbox.io/s/lp1p0wyv8l). If you’d like to grab a copy of the code, please see [this GitHub repo](https://github.com/sitepoint-editors/vuex-todo).

## Prerequisites

Before we start, I’ll assume that you:

*   have a [basic knowledge of Vue.js](https://www.sitepoint.com/getting-started-with-vue-js/)
*   have a basic knowledge of Vuex and its core concepts (check out “Getting Started with Vuex: a Beginner’s Guide” in this Vue series)
*   are familiar with [ES6](https://www.sitepoint.com/tag/es6/) and [ES7](https://www.sitepoint.com/es2017-whats-new/) language features

To follow along with this tutorial, I recommend you install code highlighting for Vue in your editor of choice. [Vetur for VSCode](https://marketplace.visualstudio.com/items?itemName=octref.vetur) is a popular choice for this, as is [Vue Syntax Highlight for Sublime](https://github.com/vuejs/vue-syntax-highlight).

I also recommend that you install the Vue.js DevTools for your browser, as I’ll be making use of them later on to inspect the state of our application. You can find the [Chrome extension here](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en), or the [Firefox extension here](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools).

In addition, you’ll need to have a recent version of Node.js that’s not older than version 6.0\. At the time of writing, Node.js v10.13.0 (LTS) and npm version 6.4.1 are the most recent. If you don’t have a suitable version of Node installed on your system already, I recommend [using a version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

Finally, you should have the most recent version of [Vue CLI](https://cli.vuejs.org/) installed:

```
npm install -g @vue/cli
```

At the time of writing, this was v3.1.3.

## Create a New Project

Let’s generate a new project using the CLI:

```
vue create vuex-todo
```

A wizard will open up to guide you through the project creation. Select *Manually select features* and ensure that you choose to install Vuex. After you’ve finished selecting your options, Vue CLI will scaffold your project and install the dependencies.

We’re going to use the following dependencies for our Vuex project. They’re not part of Vuex, but they’ll make our web interface pretty and interactive.

*   [Bootstrap Vue](https://bootstrap-vue.js.org/) - Bootstrap CSS framework V4 re-engineered for Vue.js projects
*   [VeeValidate](https://baianat.github.io/vee-validate/), a form validation framework for Vue.js projects

Let’s change into the project directory and install them:

```
cd vuex-todo
npm install bootstrap-vue vee-validate
```

To test everything has run correctly, start up the app using `npm run serve` and visit [http://localhost:8080](http://localhost:8080). You should see a welcome screen.

## Basic Project Setup

Now that we have all our dependencies installed, we can now go ahead and start building our main application structure. Under the `src/components` folder, delete the `HelloWorld.vue` file, then create two new files—`TodoList.vue` and `TodoItem.vue`:

```
rm src/components/HelloWorld.vue
touch src/components/{TodoList.vue,TodoItem.vue}
```

Next, let’s inject `Bootstrap Vue` and `VeeValidate` by adding the following code to `main.js`:

```
...
import BootstrapVue from 'bootstrap-vue'
import VeeValidate from 'vee-validate';
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
...
Vue.config.productionTip = false
Vue.use(BootstrapVue)
Vue.use(VeeValidate);
```

Now open up `src/App.vue` and replace the existing code with the following:

```
<template>
  <div id="app">
   <b-jumbotron  bg-variant="info" text-variant="white">
      <template slot="header">
        <b-container>Vuex ToDo App</b-container>
      </template>
      <template slot="lead">
        <b-container>Built using Bootstrap-Vue.js</b-container>
      </template>
    </b-jumbotron>

    <b-container>
      <div class="todo-page">
        <h2>Shopping List</h2>
        <hr>
        <TodoList />
      </div>
    </b-container>
  </div>
</template>

<script>
  import TodoList from '@/components/TodoList.vue'

  export default {
    name: 'TodoView',
    components: {
      TodoList
    }
  }
</script>
```

Here we’re using Bootstrap components to lay out our application page. It’s easier this way instead of defining Bootstrap class names for each HTML element. You can find the documentation for the components used on the [Bootstrap Vue.js](https://bootstrap-vue.js.org/docs/components/jumbotron) website.

For the components, we’ll just insert some placeholder code. Insert the following code into `components/TodoList.vue`:

```
<template>
    <p>To-do List component under construction</p>
</template>
```

Insert the following code for `components/TodoItem.vue`:

```
<template>
  <p>To-do Item component under construction</p>
</template>
```

Finally, head back to [http://localhost:8080](http://localhost:8080), where you should have the following page view:

![Scaffolding of Vuex app](Images/vuex-todo-01.jpg) 

## Building the To-do List

To build our to-do list, we’ll take a bottom-up approach. In other words, we’ll start by building our Vuex store, then finish by creating the components. We’ll use a very simple `TodoItem` model for our `TodoList` collection that only consists of two properties:

```
{
  name: "Butter",
  done: false
}
```

### Creating the Store

Open `src/store.js` and replace the default export with the following code:

```
export default new Vuex.Store({
  state: {
    items: [
      {
        name: "Milk",
        done: false
      },
      {
        name: "Bread",
        done: true
      },
      {
        name: "Cake",
        done: false
      }
    ]
  },
  mutations: {
    addItem(state, item) {
      state.items.push(item)
    },
    editItem(state, { item, name = item.name, done = item.done }) {
      item.name = name;
      item.done = done;
    },
    removeItem(state, item) {
      state.items.splice(state.items.indexOf(item), 1);
    }
  },
  actions: {
    addItem({ commit }, item) {
      commit("addItem", {
        name: item,
        done: false
      })
    },
    editItem({ commit }, { item, name }) {
      commit("editItem", { item, name });
    },
    toggleItem({ commit }, item) {
      commit("editItem", { item, done: !item.done });
    },
  }
});
```

As you can see, we start off by declaring our items in a `state` object.

We then have three mutations for manipulating the state—`addItem`, `editItem` and `removeItem`. The `addItem` mutation handler takes an item and pushes it on to `state`, and the `removeItem` mutation handler takes an item and uses [Array’s splice method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice) to remove it from state. The `editItem` mutation handler perhaps looks a bit funky, but all it’s doing is accepting an object as an argument with three properties:

*   `item`: the record to be updated.
*   `name`: the new value for `name` field. If none is provided, it uses `item.name`.
*   `done`: the new value for the `done` field. If none is provided, it uses `item.done`.

It then updates the properties accordingly.

This syntax is new to ES6\. You can read more about it in our post “[ES6 in Action: Destructuring Assignment](https://www.sitepoint.com/es6-destructuring-assignment/)”.

Finally come the actions. These will call our mutations to create a new item, to edit an item and to toggle an item’s `done` property. Notice how the `editItem` and `toggleItem` action handlers also take advantage of destructuring to accomplish their tasks.

If you’d like a refresher on these core concepts of Vuex, please refer to “Getting Started with Vuex: a Beginner’s Guide” in this Vue series.

### Building the TodoList Component

Let’s now build out our `src/components/TodoList` component.

Start by adding the following code to `src/comnponents/TodoList.vue`:

```
<template>
  <div class="todo-list">
    <!-- start of to-do form -->
    <b-form class="row" >
      <b-col cols="10">
        <b-form-input
          id="item"
          name="item"
          class="w-100"
          placeholder="What do you want to buy?"
        ></b-form-input>
      </b-col>
      <b-col cols="2">
        <b-button type="submit" variant="primary">Add Item</b-button>
      </b-col>
    </b-form>
    <!-- end of to-do form -->

    <!-- start of to-do list -->
    <b-row>
      <b-col md="10">
        <b-list-group>
          <b-list-group-item v-for="(item, index) in items" :key="index" :item="item">
            {{ item.name }}
          </b-list-group-item>
        </b-list-group>
      </b-col>
    </b-row>
    <!-- end of to-do list -->
  </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
  name: 'TodoList',
  computed: {
    ...mapState([
      'items'
    ])
  },
};
</script>

<style>
form {
  margin-bottom: 25px;
}
.list-group-item {
  display: flex;
}
.list-group-item:hover{
  background-color: aliceblue;
}
.checked {
  font-style: italic;
  text-decoration: line-through !important;
  color: gray;
  background-color: #eeeeee;
}
</style>
```

It’s essentially made up of a form and list group for displaying the shopping list items. There’s a bit of CSS and Bootstrap styling classes to make the layout look right. If there’s anything here you’re not sure of, please consult the [Bootstrap Vue](https://bootstrap-vue.js.org/docs) documentation.

This is what you should have on the to-do page:

![Vuex shopping list app displaying Milk, Bread & Cheese](Images/vuex-todo-02.jpg) 

### Inspect the App’s State Using the Vue DevTools

If you’ve installed the Vue.js browser extension mentioned at the beginning of this guide, you can press `F12` and then click the *Vue* tab. In here, you’ll see another tab called *Vuex*. Click it. You should be able to see the entire store for your application.

![Vue DevTools in action](Images/vuex-todo-03.jpg) 

Once we’ve made the component interactive, you’ll be able to add new items or delete old ones and see the Vuex store update accordingly. You’ll also be able to revert mutations by clicking on the *Revert* button.

### Adding an Item

Let’s now make our shopping list interactive. There are several things we need to do here:

*   Allow users to add items, mark them as `done` and delete them.
*   Add validation to the input form using the [VeeValidate](https://baianat.github.io/vee-validate/) package. The only rule we’re using is `v-validate="'required'"` that will prevent the submission of a blank form.
*   Display validation error messages if present using VeeValidate `errors` object.
*   Create a local state variable called `item` that will bind to the input form.
*   Create an `onSubmit()` function that will handle the form’s `POST` events using Vue.js `@submit.prevent` modifier.

Let’s start enabling the “Add Item” feature. Update the template section in `src/components/TodoList.vue` as follows:

```
<!-- start of to-do form -->
<b-row>
  <b-col>
    <!-- display validation error -->
      <b-alert v-if="errors.has('item')" show dismissible variant="danger">
      {{ errors.first('item') }}
    </b-alert>
  </b-col>
</b-row>
<!-- post to onSubmit function -->
<b-form class="row" @submit.prevent="onSubmit">
  <b-col cols="10">
  <!-- bind to local `item` state -->
    <b-form-input
      id="item"
      class="w-100"
      name="item"
      type="text"
      placeholder="What do you want to buy?"
      v-model="item"
      v-validate="'required'"
      autocomplete="off"
    ></b-form-input>
  </b-col>
  <b-col cols="2">
    <b-button type="submit" variant="primary">Add Task</b-button>
  </b-col>
</b-form>
<!-- end of to-do form -->
```

Let’s now define the local state `item` and `onSubmit()` function in the `<script>` section as follows:

```
import { mapState, mapActions } from 'vuex';

export default {
  name: 'TodoList',
  data() {
    return {
      item:''
    }
  },
  computed: {
    ...mapState([
      'items'
    ])
  },
   methods: {
    ...mapActions([
      'addItem',
    ]),
    async onSubmit() {
      const isvalid = await this.$validator.validateAll();
      if(isvalid) {
        await this.addItem(this.item);
        this.item=''; // Clear form after successful save
        this.$validator.reset();
      }
    },
  }
};
```

In the `onSubmit` method, we first execute a validation method to ensure that the form input value is valid. If it’s not valid, an error message is displayed. If it’s valid, the item is passed to the `addItem` action. The local state `item` is cleared and the validator is reset to prevent incorrect error messages from showing up. After you’ve implemented the changes and tested the form, you should have something similar:

![The item field is required](Images/vuex-todo-04.jpg) 

Remember to check out the Vue DevTools to see how the store reacts to your input events.

### The To-do Item Component

Let’s now work on the `src/components/TodoItem` component. Copy the following code:

```
<template>
  <div class="todo-item">
    <b-list-group-item class="row">
      {{ item.name }}
    </b-list-group-item>
  </div>
</template>

<script>
  export default {
    name: 'TodoItem',
    props: ['item']
  }
</script>
```

Next, go back to `src/components/TodoList`. We need to replace the `<b-list-group-item>` code section with the new component `TodoItem`. Go to the template section and replace the code section with `<b-list-group>` with this:

```
<b-list-group>
  <TodoItem v-for="(item, index) in items" :key="index" :item="item" />
</b-list-group>
```

In order to use the `TodoItem` component in `TodoList`, you’ll need to import it in the `<script>` section like this:

```
import TodoItem from './TodoItem.vue'
//..

export default {
  name: 'TodoList',
  components: {
    TodoItem
  },
  //..
}
```

That’s it. Save your changes and the to-do shopping list should operate as before. Now that we have a dedicated `TodoItem` component, we can now easily add more features:

*   toggle item state (`done` field)
*   edit item names
*   delete items

### Toggling an Item’s State

Let’s start by toggling the item status. In the `todo` store, we already have an action that can do that for us:

```
toggleItem({ commit }, item) {
  commit("editItem", { item, done: !item.done })
}
```

By mapping the action locally using the `mapAction` helper, we can access this function directly from the `TodoItem` component like this:

```
this.toggleItem(item)
```

Let’s add a checkbox input by updating the `<template>` code as follows:

```
<template>
  <div class="todo-item">
    <b-list-group-item v-bind:class="{ checked: item.done }">
      <b-row>
        <b-col cols="1">
          <b-form-checkbox
            :checked="item.done"
            @change="changeItemStatus(item)"
          >
          </b-form-checkbox>
        </b-col>
        <b-col cols="9">
          <span>{{ item.name }}</span>
        </b-col>
      </b-row>
    </b-list-group-item>
  </div>
</template>
```

We now should have the following view:

![Shopping list with toggle](Images/vuex-todo-05.jpg) 

However, do note that we run into an error if we try to toggle any of the checkboxes. This is because we haven’t defined the `changeItemStatus` function.

Let’s do that now:

```
import { mapActions } from 'vuex'

export default {
  name: 'TodoItem',
  props: ['item'],
  methods: {
    ...mapActions([
      'toggleItem'
    ]),
    changeItemStatus(item) {
      this.toggleItem(item);
    }
  }
};
```

Go ahead and test the checkbox. The items should now be toggleable. You can confirm via the DevTools extension that the store is actually reacting to your clicks and that the item’s `done` property is updating in `state`.

### Removing an Item

Next, let’s add a *remove* feature. For this, we won’t dispatch an action, but instead we’ll commit the `removeItem` mutation directly from the `TodoItem` component. This is the code to accomplish that:

```
<template>
  ...
  <b-col cols="10">
    <span>{{ item.name }}</span>
  </b-col>
  <b-col cols="1">
    <b-button-close @click="removeItem(item)"></b-button-close>
  </b-col>
  ...
</template>

<script>
  ...
  methods: {
    ...mapActions([
      'toggleItem'
    ]),
    changeItemStatus(item) {
      this.toggleItem(item);
    },
     removeItem(item) {
      this.$store.commit("removeItem", item)
    },
  }
  ...
</script>
```

After you’ve saved your changes, go ahead and test the delete button to make sure that it’s working properly.

![Removing a to-do item](Images/todo-remove.jpg) 

### Updating an Item

Finally, let’s add the `edit` feature. This one is going to be a bit tricky. This is what we’re going to do:

*   We’ll create a local state called `editing`, which by default will be set to `false`.
*   When it’s false, the item’s name will be displayed via a span element.
*   When it’s true, the item’s name will be displayed via an input text box.
*   We’ll create a custom Vue.js directive for automatically setting focus on the text box when it’s visible.
*   Using events triggered via `@keyup.enter` and `@blur`, we’ll call a custom function `doneEdit`, for handling the edit changes.
*   Using the event triggered via `@keyup.esc`, we’ll call a custom function, `cancelEdit`, for cancelling the edit. This function will also reset the `item.name` state back to its original, and set the `editing` value to false.

Let’s now start implementing the changes. We’ll add the text box by replacing the relevant code in the `template` section in `src/components/TodoItem.vue` with this:

```
<template>
...
<b-col cols="10">
  <span v-if="!editing" @dblclick="editing = true">{{ item.name }}</span>
  <input class="edit"
    v-show="editing"
    v-focus="editing"
    :value="item.name"
    @keyup.enter="doneEdit"
    @keyup.esc="cancelEdit"
    @blur="doneEdit"
  >
</b-col>
...
</template>
```

Next, we’ll add the `editing` Boolean state variable, the `focus` directive, as well as the `doneEdit` and `cancelEdit` functions in the script section.

Update the code as follows:

```
export default {
  //...
  data () {
    return {
      editing: false
    }
  },
  directives: {
    focus (el, { value }, { context }) {
      if (value) {
        context.$nextTick(() => {
          el.focus()
        })
      }
    }
  },
  methods: {
    ...mapActions([
      'toggleItem',
      'editItem'
    ]),
    //..
     doneEdit(event) {
        const value = event.target.value.trim();
        const { item } = this;
        if (!value) {
          this.removeItem(item)
        } else if (this.editing) {
          this.editItem({ item, name:value });
          this.editing = false
        }
      },
      cancelEdit(event){
        event.target.value = this.item.name;
        this.editing = false;
      }
  }
}
```

Save the changes and test the new editing feature. To make a change on an item, simply double click on it. You can press `Return` or click away to save the changes. You can also hit `ESC` if you don’t want to save the change. You should have a similar view as below:

![Editing a to-do item](Images/vuex-todo-06.jpg) 

## Taking it Further

Well done if you made it this far! You’ve grasped the majority of the skills you need to build a Vuex project. I’m going to leave you with a challenge. The project we just built is using a hard-coded list of to-do items. In other words, every time we perform a full browser refresh, the `todo` store is reset back to its hard-coded values:

```
state: {
    items: [
      {
        name: "Milk",
        done: false
      },
      {
        name: "Bread",
        done: true
      },
      {
        name: "Cake",
        done: false
      }
    ]
  },
```

I want you set the initial state for items to an empty array like this:

```
state: {
  items: []
}
```

Then, I want you to use a real database for persisting the `items` collection. You can use any database system you’re comfortable using, such as MongoDB, a ready-made API interface such as [JSON server](https://github.com/typicode/json-server), or a cloud-hosted database such as [mLab](https://mlab.com/). You can then use a library like [axios](https://github.com/axios/axios) to fetch data from your remote API to the application’s store.

Here’s some clues on how you can set it up. You’ll need to create a new mutation for this task in your `todo` store that looks like this:

```
export default {
  state: {
    items: []
  },
  mutations: {
    fetchTodos(state, items) {
      state.items = items
    }
  },
  actions: {
    async fetchTodos({commit}) {
      const response = await axios.get('http://localhost:4000/api/todos');
      commit("fetchItems", response.data)
    }
  }
}
```

Then in your `TodoList` component, you can use Vue’s `created` lifecycle hook to retrieve the data:

```
<script>
import { mapActions } from 'vuex'

export default {
  computed: {
    ...mapActions([
      'fetchTodos'
    ])
  }
  created: function() {
    this.fetchTodos()
  }
}
</script>
```

Note that I haven’t done any error handling. I’ll leave it to you to figure out how to display an appropriate error message in case the `fetchTodos` function fails.

## Summary

On a personal level, I really like Vuex as someone coming from a background in Redux and MobX state management libraries. I find Vuex to be a bit leaner and cleaner. It does a lot of the heavy lifting for you, making it easy to implement your code. The Vue DevTools are a big bonus that allow you to debug your Vuex store easily in the event that something goes wrong.

Vuex is tightly integrated with Vue.js and is maintained by the Vue.js team. I would say that’s a pretty good reason to rely on Vuex for a commercial project. Being open source, you can easily confirm that the project is being actively maintained on [GitHub](https://github.com/vuejs/vuex). You can also confirm that it doesn’t have too many unresolved issues.

With that said, you should note that I haven’t been able to cover 100% of the features available in the Vuex library. I would highly recommend you check out their [current documentation](https://vuex.vuejs.org/) to learn more about its advanced features.

# Chapter 11: How to Develop and Test Vue Components with Storybook

### by Ivaylo Gerchev

In today’s web application development, components play a central role. The complexity in modern apps requires us to split the codebase into small and manageable pieces—components—which then we can use as Lego bricks to build the entire app. To facilitate the building process and make it more automated and interactive, some smart developers have created specialized tools for component development. One such a tool is [Storybook](https://storybook.js.org/).

## What Is Storybook?

Storybook is an interactive environment for developing and testing UI components. It allows developers to build components and play with them in isolation from the actual app. A Storybook project can be exported as a separate, static app, which is ideal for making live and interactive component showcases. Storybook is easy to configure and use, and can be extended via a simple API. It has a bunch of useful add-ons, both official and community made, which enhance the core with lots of different functionality.

## Getting Started

In this tutorial, we’ll learn how to use Storybook to develop [Vue](https://vuejs.org) components.

#### The Finished Result

If you’d like to view the finished result, you can find the Storybook deployed to [GitHub Pages](https://sitepoint-editors.github.io/vue-pomodoro/).

To follow along with this tutorial, you’ll need Git and Node installed on your machine. You can find [instructions on how to install Git here](https://git-scm.com/downloads). To install Node, you can download the binaries from the [official website](https://nodejs.org/), or use a [version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). This is probably the easiest way, as it allows you to manage multiple versions of Node on the same machine.

As a starting point, we’ll use a [vue-pomodoro timer app](https://github.com/sitepoint-editors/vue-pomodoro) that I’ve already written. The [Pomodoro Technique](https://en.wikipedia.org/wiki/Pomodoro_Technique) is a time-management method developed by Francesco Cirillo in the late 1980s, whereby one uses a timer to break down work into intervals, separated by short breaks. I created this app using Vue CLI. (See “A Beginner’s Guide to Vue CLI” in this Vue series if you’re not familiar with it.) I also chose to install the Babel, ESLint and Jest plugins. We’ll need the Jest plugin for testing our components later on.

Clone the app to your local machine, install the dependencies and make sure that it works:

```
git clone git@github.com:sitepoint-editors/vue-pomodoro.git
cd vue-pomodoro
npm i
npm run serve
```

### Installing Storybook

Next we need to install Storybook and some additional dependencies.

#### Checking Your Progress

The repo has a second branch (named `storybook`) which you can check out, should you wish to jump straight to the finished code, or simply check your progress. You can see [the storybook branch on GitHub](https://github.com/sitepoint-editors/vue-pomodoro/tree/storybook), or you can check it out via the terminal:

```
git clone git@github.com:sitepoint-editors/vue-pomodoro.git
  git checkout storybook
```

Install the Storybook itself by running the following:

```
npm i --save-dev @storybook/vue
```

Next, we need to add some dependencies:

```
npm i --save-dev vue-loader
npm i --save-dev babel-preset-vue
```

The next step is to add the `storybook` script in our project’s `package.json` file:

```
{
  "scripts": {
   ...
    "storybook": "start-storybook -p 9001 -c .storybook"
  }
}
```

The script starts the Storybook development server at port `9001` and defines `.storybook` as a config directory. We’ll also need to create a `config.js` file in the `.storybook` directory, in which we import and register our components and load our stories. We’ll learn what stories are and how to create them in the next section.

```
mkdir .storybook
touch .storybook/config.js
```

Add the following to `config.js`:

```
import { configure } from '@storybook/vue';

import Vue from 'vue';

// Import your custom components.
import State from '../src/components/State.vue';
import Countdown from '../src/components/Countdown.vue';
import Controls from '../src/components/Controls.vue';

// Register your custom components.
Vue.component('state', State);
Vue.component('countdown', Countdown);
Vue.component('controls', Controls);

function loadStories() {
  // You can require as many stories as you need.
  require('../src/stories');
}

configure(loadStories, module);
```

## Writing Stories

[Stories](https://storybook.js.org/basics/writing-stories/) are the heart of Storybook. A story represents a particular state of one single component or multiple components grouped together. We can have as many stories for as many components which we need. The great thing is that when we edit the stories the changes are applied and displayed immediately. This gives us a smooth, interactive experience.

The stories are stored in their own directory, which keeps them closer to the app’s components. In our case, we navigate to the `src` directory, and create a new `stories` folder inside. Then add an `index.js` file:

```
mkdir src/stories
touch src/stories/index.js
```

Writing stories is quite simple. Let’s create our first story now in `index.js`:

```
import Vue from "vue";
import { storiesOf } from "@storybook/vue";

storiesOf("State", module).add("state toggle", () => ({
  template: `<state :isworking="false"></state>`
}));
```

The `storiesOf` method wraps a story or set of stories about a particular component or group of components. The first argument defines a name for the wrapper. The individual stories are just different states, which we create by using the `add` method. The first argument defines the state’s name, and the second is a function in which we create the actual state. There are many ways available to render a state. To see them all, check out the [Vue real examples](https://storybooks-vue.netlify.com/?selectedKind=Custom%7CMethod%20for%20rendering%20Vue&selectedStory=render&full=0&addons=1&stories=0&panelRight=0&addonPanel=storybook%2Fstories%2Fstories-panel).

Let’s now see our story in action by running the project:

```
npm run storybook
```

You should see the following in your browser:

![state component](Images/state_toggle.png)

## Installing and Using Add-ons

As we saw, Storybook’s core has limited functionality. To add more useful features, we’ll need to install some add-ons. There are two types of add-ons:

*   **Decorators** wrap a story or stories and transform them in some way. For example, we can create a center text decorator, which will center the text in our story. We’ll see a practical example of this later on.
*   **Native Add-ons** allow for low-level interaction with the Storybook platform. We’ll also see examples of those.

### Installing the Storysource Add-on

The first add-on we’ll install is [Storysource](https://github.com/storybooks/storybook/tree/master/addons/storysource). It adds a “STORY” panel to the storybook, which shows and highlights the source of the selected story. It’s useful because we can see how the story is written without the need to open the story file and search for the story manually. To install the add-on, we run:

```
npm install -D @storybook/addon-storysource
```

Before we can use the add-on, we need to register it in a special `addons.js` file, which we must create in the `.storybook` directory:

```
touch .storybook/addons.js
```

Then add:

```
import '@storybook/addon-storysource/register';
```

And one more thing. The add-on needs some custom webpack configuration. So we create a `webpack.config.js` file in the same `.storybook` directory:

```
touch .storybook/webpack.config.js
```

And add the following content to it:

```
const path = require('path');

module.exports = (storybookBaseConfig, configType, defaultConfig) => {
  defaultConfig.module.rules.push({
    test: [/\.stories\.js$/, /index\.js$/],
    loaders: [require.resolve('@storybook/addon-storysource/loader')],
    include: [path.resolve(__dirname, '../src')],
    enforce: 'pre',
  });

  return defaultConfig;
};
```

#### Restarting the Storybook

After we’ve installed new add-ons, we need to restart the storybook so for the changes to take effects.

Finally, we can see the add-on in action:

![Storysource in action](Images/storysource_preview.png)

### Installing the Options Add-on

The next add-on we’ll install is [Options](https://github.com/storybooks/storybook/tree/master/addons/options). It gives us the ability to use some options for configuring Storybook’s UI.

Install it with this:

```
npm install -D @storybook/addon-options
```

Register it in the `addons.js`:

```
import '@storybook/addon-options/register';
```

Then we can use it in our `config.js` file like this:

```
import { configure, addDecorator } from '@storybook/vue';
import { withOptions } from '@storybook/addon-options';

addDecorator(
  withOptions({
    name: 'Vue Pomodoro',
  })
);
```

We import the `addDecorator` method and set the necessary options via `withOptions` decorator.

Now, the name in the top left corner of our storybook will be “VUE POMODORO”, instead of “STORYBOOK”. You can play with other options as you wish.

### Installing Actions, Links, and Knobs Add-ons

In this section we’ll install three more add-ons: [Actions](https://github.com/storybooks/storybook/tree/master/addons/actions), [Links](https://github.com/storybooks/storybook/tree/master/addons/links), and [Knobs](https://github.com/storybooks/storybook/tree/master/addons/knobs).

You can install them like so:

```
npm install -D @storybook/addon-knobs @storybook/addon-links @storybook/addon-actions
```

And register them in `addons.js`:

```
import '@storybook/addon-knobs/register';
import '@storybook/addon-links/register';
import '@storybook/addon-actions/register';
```

#### Registration Order

The order of registration matters here, because the add-ons will be displayed in the same sequence in the Storybook’s panels section.

### Using the Knobs Add-on

Knobs allow us to edit Vue props dynamically. Let’s see this in action. In the `index.js` file add the following:

```
import { withKnobs, boolean } from '@storybook/addon-knobs';

...

storiesOf("State", module)
  .addDecorator(withKnobs)
  .add("state toggle", () => ({
    props: {
      isworking: {
        type: Boolean,
        default: boolean("isworking", true)
      }
    },
    template: `<state :isworking="isworking"></state>`
  }));
```

Here, we import the `withKnobs` decorator and `boolean` knob. Then, we add the decorator to our story. We define the `isworking` prop and use the `boolean` knob to define the default value. Now, when we go to this story, we’ll see a checkbox in the “KNOBS” panel bound to the `isworking` prop.

![State component with knobs](Images/knobs_preview.png)

### Creating and Using a Custom Decorator

Let’s now see how to create a custom decorator. In the same `index.js` file, add the following:

```
const CenterDecorator = () => ({
  template: '<div style="textAlign: center;"><story/></div>',
});

...

storiesOf("Countdown", module)
  .addDecorator(CenterDecorator)
  .add("work state", () => ({
    template: `<countdown :minute="1" :second="0" :isworking="true"></countdown>`
  }))
  .add("rest state", () => ({
    template: `<countdown :minute="5" :second="0" :isworking="false"></countdown>`
  }));
```

What we do here is define a `CenterDecorator` decorator. We wrap the `<story/>` component with our custom functionality. Then we add it to the two new states we created for the Countdown component.

![State work](Images/work_state.png)

![State rest](Images/rest_state.png)

### Using the Links and Actions Add-ons

In this section, we’ll create stories about the Pomodoro controls buttons, and we’ll use links to simulate the real world behavior when we click them.

In the `index.js` file, add the following:

```
import { linkTo } from '@storybook/addon-links';
import { action } from '@storybook/addon-actions';

...

storiesOf("Controls", module)
  .add("started state", () => ({
    template: `<controls state="started" @paused="linkToPaused()" @stopped="linkToStopped()"></controls>`,
    methods: {
      linkToPaused: linkTo("Controls", "paused state"),
      linkToStopped: linkTo("Controls", "stopped state")
    }
  }))
  .add("paused state", () => ({
    template: `<controls state="paused" @started="linkToStarted()" @stopped="linkToStopped()"></controls>`,
    methods: {
      linkToStarted: linkTo("Controls", "started state"),
      linkToStopped: linkTo("Controls", "stopped state")
    }
  }))
  .add("stopped state", () => ({
    template: `<controls state="stopped" @started="linkToStarted(), action()"></controls>`,
    methods: {
      linkToStarted: linkTo("Controls", "started state"),
      action: action("Starting")
    }
  }));
```

Here, we import the `linkTo` and `action` methods. Then we create stories about the three possible states of the buttons. Next, we create links to navigate between the states according to the pressed button. In the stopped state we use also an action. So when we press the *Start* button, it will log the start action in the “ACTION LOGGER” panel.

![Actions in action](Images/actions_preview.png)

### Combining Multiple Components

In Storybook, we can not only create a story for one single component, but we can combine multiple components into one Story screen. So when we’re done with the single components, we can then combine them to represent different screens of our app. Let’s try this. In `index.js`, add the following:

```
storiesOf("App Screen", module)
  .addDecorator(CenterDecorator)
  .add("all components", () => ({
    template: `
      <div>
        <state :isworking="true"></state>
        <countdown minute="1" second="0" :isworking="true"></countdown>
        <controls state="stopped"></controls>
      </div>`
  }));
```

Here, we use the `CenterDecorator` to center all components. And voilà.

![All components](Images/all_components_preview.png)

## Testing Components

So we have all our components ready. Now it’s time to test them. Testing is too wide a topic to be discussed here entirely. There are many different way to test components. Here, we’ll narrow our exploration to three of them:

*   **Manual testing** relies on developers manually exploring components and making sure they work and behave correctly.
*   **Structural/Snapshot testing** captures the rendered markup of components. At the next run, the new snapshots are compared to the old ones to make sure they match. If they don’t match, we have two choices. We can accept the differences if they’re the result of intentional changes, and update the snapshots. Or we can fix them if they’re the result of incorrect code.
*   **Unit testing** verifies that, with a given input, we’ll get the expected output.

If you’re new to JavaScript testing, you might like to have a quick read of “[How to Test React Components Using Jest](https://www.sitepoint.com/test-react-components-jest/)” to get a handle on the general concepts.

### Implementing Structural Testing with the Storyshots Add-on

The [Storyshots](https://github.com/storybooks/storybook/tree/master/addons/storyshots/storyshots-core) add-on adds automated snapshot testing to our storybook. Let’s see what that looks like.

First, install the add-on:

```
npm install --save-dev @storybook/addon-storyshots
```

Now, we create a `storyshots.spec.js` file in the `tests/unit` directory:

```
touch tests/unit/storyshots.spec.js
```

We then put the following in it:

```
import initStoryshots from '@storybook/addon-storyshots';

initStoryshots();
```

And that’s it. Now we run the test:

```
npm run test:unit
```

And here’s what we should see in the terminal:

![Tests output](Images/snapshots_test_passed.png)

All snapshots will be placed in a `__snapshots__` directory, which is automatically created in the `tests/unit` directory.

Now, to demonstrate the snapshots diffing, let’s change the `isworking` prop, in our very first story, to `false`, and re-run the tests. As we can see in the screenshot below, the change is caught by the add-on, and it tells us that we can update the snapshots by using the `-u` flag.

![Tests output](Images/snapshots_test_failed.png)

To make this easier, we create a `test:update` script in the `package.json`:

```
{
  "scripts": {
    ...
    "test:update": "vue-cli-service test:unit -u"
  }
}
```

Now, if we want to accept the changes, we can run this script and the snapshots will be updated to their new version.

### Unit Testing

As I mentioned at the beginning of this guide, the project has the Jest plugin installed. So we also have the [Vue Test Utils](https://vue-test-utils.vuejs.org/) at our disposal. Given that, let’s explore a practical example of unit testing.

In the `tests/unit` directory we create a `components.spec.js` file:

```
touch tests/unit/components.spec.js
```

And add the following content:

```
import { mount } from "@vue/test-utils";
import State from "../../src/components/State.vue";

describe("State", () => {
  it("has title Work!", () => {
    const wrapper = mount(State, {
      propsData: {
        isworking: true
      }
    });
    const title = wrapper.find("h3");
    expect(title.text()).toBe("Work!");
  });
  it("has title Rest!", () => {
    const wrapper = mount(State, {
      propsData: {
        isworking: false
      }
    });
    const title = wrapper.find("h3");
    expect(title.text()).toBe("Rest!");
  });
});
```

We use the `mount` method to create wrappers for the `State.vue` component with the two possible states of the prop `isworking`. Then we get the title where the prop is used and test whether it has the proper string, depending on the `isworking` state.

Now, let’s run the tests again:

```
npm run test:unit
```

And everything should be correct.

## Exporting Storybook as a Static App

After the hard work is done, we may want to show our components to others. Doing this is easy. We just need to export our storybook as a static app and deploy it. Let’s do it.

First, we need to add a build script to `package.json`:

```
{
  "scripts": {
    ...
    "storybook-static": "build-storybook -c .storybook -o .storybook-static"
  }
}
```

Now, when we run the script, it will output a static Storybook in the `.storybook-static` directory.

### Publishing the Storybook to GitHub

As the storybook is a static app, it’s easy to publish it anywhere on the Web. In this final section, I’ll demonstrate how to add the project to GitHub.

First, we create a new repo `vue-pomodoro-storybook`.

Now, we copy the origin URL of the repo and add it to our local Git project with this command:

```
git remote add origin https://github.com/<USERNAME>/vue-pomodoro-storybook.git
```

Finally, we push the repo to GitHub:

```
git push -u origin master
```

Now, let’s deploy our static app to GitHub Pages.

We navigate to `.storybook-static` folder and run:

```
git init
git add -A
git commit -m 'deploy'
```

Then, we deploy to GitHub Pages with this command:

```
git push -f https://github.com/<USERNAME>/vue-pomodoro-storybook.git master:gh-pages
```

This will create a new branch `gh-pages` and will upload the static app to it.

And that’s it.

#### Github

Don’t forget, you can find the [deployed storybook here](https://sitepoint-editors.github.io/vue-pomodoro/).

## Conclusion

I hope you enjoyed learning Storybook. As you saw, it’s a powerful playground, which we can use to interactively develop and test self-contained UI components. It’s also great for making a live components showcase or documentation. I encourage you to check it out.