![](Images/default_cover.jpeg)

![](Images/default_cover.jpeg)

## Working with Vue.js

Copyright © 2019 SitePoint Pty. Ltd.

Ebook ISBN: 978-1-925836-26-4

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

If you're an experienced developer looking to make a start with Vue, this book is for you. It provides a rapid introduction to the key topics that you'll need to understand. It contains:

1.  *Getting up and Running with the Vue.js 2.0 Framework* by Jack Franklin
2.  *Getting Started with Vuex: a Beginner’s Guide* by Michael Wanyoike
3.  *A Beginner’s Guide to Vue CLI* by Ahmed Bouchefra
4.  *A Beginner’s Guide to Working With Components in Vue* by Kingsley Silas
5.  *A Beginner’s Guide to Working with Forms in Vue* by Kingsley Silas
6.  *How to Conditionally Apply a CSS Class in Vue.js* by Chad Campbell
7.  *How to Replace jQuery with Vue* by Nilson Jacques
8.  *Nuxt.js: a Minimalist Framework for Creating Universal Vue.js Apps* by Olayinka Omole
9.  *Optimize the Performance of a Vue App with Async Components* by Michiel Mulders

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

# Chapter 1: Getting up and Running with the Vue.js 2.0 Framework

### by Jack Franklin

**As soon as the popular JavaScript framework [Vue.js](https://vuejs.org/) released [v2](https://medium.com/the-vue-point/vue-2-0-is-here-ef1f26acf4b8#.f6sth6njx), I was eager to give it a spin and see what it’s like to work with. As someone who’s pretty familiar with Angular and React, I was looking forward to seeing the similarities and differences between them and Vue.**

Vue 2 sports excellent performance stats, a relatively small payload (the bundled runtime version of Vue weighs in at 30KB once minified and gzipped), along with updates to companion libraries like vue-router and Vuex, the state management library for Vue. There’s far too much to cover in just one article, but keep an eye out for some later articles where we’ll look more closely at various libraries that couple nicely with the core framework.

## Inspiration from Other Libraries

As we go through this tutorial, you’ll see many features that Vue has that are clearly inspired by other frameworks. This is a good thing; it’s great to see new frameworks take some ideas from other libraries and improve on them. In particular, you’ll see Vue’s templating is very close to Angular’s, but its components and component lifecycle methods are closer to React’s (and Angular’s, as well).

One such example of this is that, much like React and nearly every framework in JavaScript land today, Vue uses the idea of a virtual DOM to keep rendering efficient. Vue uses a fork of [snabbdom](https://github.com/snabbdom/snabbdom), one of the more popular virtual DOM libraries. The Vue site includes [documentation on its Virtual DOM rendering](https://vuejs.org/v2/guide/render-function.html#Nodes-Trees-and-the-Virtual-DOM), but as a user all you need to know is that Vue is very good at keeping your rendering fast (in fact, it performs better than React in many cases), meaning you can rest assured you’re building on a solid platform.

## Components, Components, Components

Much like other frameworks these days, Vue’s core building block is the component. Your application should be a series of components that build on top of each other to produce the final application. Vue.js goes one step further by suggesting (although not enforcing) that you define your components in a single `.vue` file, which can then be parsed by build tools (we’ll come onto those shortly). Given that the aim of this article is to fully explore Vue and what it feels like to work with, I’m going to use this convention for my application.

A Vue file looks like so:

```
<template>
  <p>This is my HTML for my component</p>
</template>

<script>
  export default {
    // all code for my component goes here
  }
</script>

<style scoped>
  /* CSS here
   * by including `scoped`, we ensure that all CSS
   * is scoped to this component!
   */
</style>
```

Alternatively, you can give each element a `src` attribute and point to a separate HTML, JS or CSS file respectively if you don’t like having all parts of the component in one file.

## Setting Up a Project

Whilst the excellent [Vue CLI](https://cli.vuejs.org/) exists to make setting up a full project easy, when starting out with a new library I like to do it all from scratch so I get more of an understanding of the tools.

These days, [webpack](https://webpack.js.org/) is my preferred build tool of choice, and we can couple that with the [vue-loader plugin](https://github.com/vuejs/vue-loader) to support the Vue.js component format that I mentioned previously. We’ll also need Babel and the `env` preset, so we can write all our code using modern JavaScript syntax, as well as the [webpack-dev-server](https://github.com/webpack/webpack-dev-server), which will update the browser when it detects a file change.

Let’s initialize a project and install the dependencies:

```
mkdir vue2-demo-project
cd vue2-demo-project
npm init -y
npm i vue
npm i webpack webpack-cli @babel/core @babel/preset-env babel-loader vue-loader vue-template-compiler webpack-dev-server html-webpack-plugin --save-dev
```

Then create the initial folders and files:

```
mkdir src
touch webpack.config.js src/index.html src/index.js
```

The project structure should look like this:

```
.
├── package.json
├── package-lock.json
├── src
│   ├── index.html
│   └── index.js
└── webpack.config.js
```

Now let’s set up the webpack configuration. This boils down to the following:

*   Tell webpack to use the `vue-loader` for any `.vue` files
*   Tell webpack to use Babel and the `env` preset for any `.js` files
*   Tell webpack to generate an HTML file for the dev-server to serve, using `src/index.html` as a template:

```
//webpack.config.js
const VueLoaderPlugin = require('vue-loader/lib/plugin')
const HtmlWebPackPlugin = require("html-webpack-plugin")

module.exports = {
  module: {
    rules: [
      {
        test: /\.vue$/,
        loader: 'vue-loader',
      },
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['@babel/preset-env']
          }
        }
      }
    ]
  },
  plugins: [
    new VueLoaderPlugin(),
    new HtmlWebPackPlugin({
      template: "./src/index.html"
    })
  ]
}
```

Finally, we’ll add some content to the HTML file and we’re ready to go!

```
<!-- src/index.html -->
<!DOCTYPE html>
<html>
  <head>
    <title>My Vue App</title>
  </head>
  <body>
    <div id="app"></div>
  </body>
</html>
```

We create an empty `div` with the ID of `app`, as this is the element that we’re going to place our Vue application in. I always prefer to use a `div`, rather than just the `body` element, as that lets me have control over the rest of the page.

## Writing Our First Vue.js App

We’re going to stay true to every programming tutorial ever and write a Vue application that puts “Hello, World!” onto the screen before we dive into something a bit more complicated.

Each Vue app is created by importing the library and then instantiating a new `Vue` instance:

```
import Vue from 'vue'

const vm = new Vue({
  el: '#app',
})
```

We give Vue an element to render onto the page, and with that, we’ve created a Vue application! We pass a selector for the element that we want Vue to replace with our application. This means when Vue runs it will take the `div#app` that we created and replace it with our application.

The reason we use the variable name `vm` is because it stands for “View Model”. Although not strictly associated with the [“Model View View-Model” (MVVM) pattern](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel), Vue was inspired in part by it, and the convention of using the variable name `vm` for Vue applications has stuck. Of course, you can call the variable whatever you’d like!

So far, our application isn’t doing anything, though, so let’s create our first component, `App.vue`, that will actually render something onto the page.

Vue doesn’t dictate how your application is structured, so this one is up to you. I ended up creating one folder per component, in this case `App` (I like the capital letter, signifying a component), with three files in it:

*   `index.vue`
*   `script.js`
*   `style.css`

```
mkdir src/App
touch src/App/{index.vue,script.js,style.css}
```

The file structure should now be:

```
.
├── package.json
├── package-lock.json
├── src
│   ├── App
│   │   ├── index.vue
│   │   ├── srcipt.js
│   │   └── style.css
│   ├── index.html
│   └── index.js
└── webpack.config.js
```

`App/index.vue` defines the template, then imports the other files. This is in keeping with the structure recommended in the [What About Separation of Concerns?](https://vuejs.org/v2/guide/single-file-components.html#What-About-Separation-of-Concerns) section of Vue’s docs.

```
<!-- src/App/index.vue -->
<template>
  <p>Hello, World!</p>
</template>
<script src="./script.js"></script>
<style scoped src="./style.css"></style>
```

I like calling it `index.vue`, but you might want to call it `app.vue` too so it’s easier to search for. I prefer importing `App/index.vue` in my code versus `App/app.vue`, but again you might disagree, so feel free to pick whatever you and your team like best.

For now, our template is just `<p>Hello, World!</p>`, and I’ll leave the CSS file blank. The main work goes into `script.js`, which looks like so:

```
export default {
  name: 'App',
  data() {
    return {}
  },
}
```

Doing this creates a component which we’ll give the name `App`, primarily for debugging purposes, which I’ll come to later, and then defines the data that this component has and is responsible for. For now, we don’t have any data, so we can just tell Vue that by returning an empty object. Later on, we’ll see an example of a component using data.

Now we can head back into `src/index.js` and tell the Vue instance to render our `App` component:

```
import Vue from 'vue'

import AppComponent from './App/index.vue'

const vm = new Vue({
  el: '#app',
  components: {
    app: AppComponent,
  },
  render: h => h('app'),
})
```

Firstly, we import the component, trusting webpack and the vue-loader to take care of parsing it. We then declare the component. This is an important step: by default, Vue components are not globally available. Each component must have a list of all the components they’re going to use, and the tag that it will be mapped to. In this case, because we register our component like so:

```
components: {
  app: AppComponent,
}
```

This means that in our templates we’ll be able to use the `app` element to refer to our component.

Finally, we define the `render` function. This function is called with a helper — commonly referred to as `h` — that’s able to create elements. It’s not too dissimilar to the `React.createElement` function that React uses. In this case, we give it the string `'app'`, because the component we want to render is registered as having the tag `app`.

More often than not (and for the rest of this tutorial) we won’t use the `render` function on other components, because we’ll define HTML templates. But the [Vue.js guide to the render function](https://vuejs.org/guide/render-function) is worth a read if you’d like more information.

Once we’ve done that, the final step is to create an npm script in `package.json`:

```
"scripts": {
  "start": "webpack-dev-server --mode development --open"
},
```

Now, run `npm run start`. Your default browser should open at [http://localhost:8080/](http://localhost:8080/) and you should see “Hello, World!” on the screen.

Try editing `src/index.vue` to change the message to something else. If all has gone correctly, webpack-dev-server should refresh the page to reflect your changes.

Yay! We’re up and running with Vue.js.

## Vue Devtools

Before we dive into a slightly more complicated app with Vue, now is a good time to mention that you should definitely get the [Vue devtools](https://github.com/vuejs/vue-devtools) installed. These sit within the Chrome developer tools and give you a great way to look through your app and all the properties being passed round, state that each component has, and so on.

![Screenshot of the Vue devtools](Images/screenshot.png)

## Building the App

As an example application, we’re going to be using the GitHub API to build an application that lets us enter a username and see some GitHub stats about that user. I’ve picked the GitHub API here as it’s familiar to most people, usable without authenticating, and gives us a fair amount of information.

Before starting an application I like to have a quick think about what components we’ll need, and I’m thinking that our `App` component will render two further components: `GithubInput`, for taking input from the user, and `GithubOutput`, which will show the user’s information on the screen. We’ll start with the input.

#### Github

You can find all [the code on GitHub](https://github.com/sitepoint-editors/vue2-demo-project) and even check out the [application running online](http://sitepoint-vue2-demo.surge.sh/).

### Initial Setup

Create folders for the `GithubOutput` and `GithubInput` components within the `src` directory:

```
mkdir src/{GithubInput,GithubOutput}
```

Add the necessary files to each:

```
touch src/GithubInput/{index.vue,script.js,style.css}
touch src/GithubOutput/{index.vue,script.js,style.css}
```

The structure of the `src` folder should now look like so:

```
.
├── App
│   ├── index.vue
│   ├── script.js
│   └── style.css
├── GithubInput
│   ├── index.vue
│   ├── script.js
│   └── style.css
├── GithubOutput
│   ├── index.vue
│   ├── script.js
│   └── style.css
├── index.html
└── index.js
```

## Forms in Vue.js

Let’s start with the `GithubInput` component. As with the `App` component, the `index.vue` file should contain the template, as well as loading in the script and CSS file. The template simply contains `<p>github input</p>` for now. We’ll fill it in properly shortly. I like putting in some dummy HTML so I can check I’ve got the template wired up properly when creating a new component:

```
<!-- src/GithubInput/index.vue -->
<template>
  <p>github input</p>
</template>

<script src="./script.js"></script>
<style scoped src="./style.css"></style>
```

When creating this component the one thing we do differently is create a piece of data that’s associated with the component. This is very similar to React’s concept of state:

```
// src/GithubInput/script.js
export default {
  name: 'GithubInput',
  data() {
    return {
      username: '',
    }
  }
}
```

This says that this component has a piece of data, `username`, that it owns and is responsible for. We’ll update this based on the user’s input shortly.

Finally, to get this component onto the screen, I need to register it with the `App` component, as it’s the `App` component that will be rendering it.

To do this, I update `src/App/script.js` and tell it about `GithubInput`:

```
// src/App/script.js
import GithubInput from '../GithubInput/index.vue'

export default {
  name: 'App',
  components: {
    'github-input': GithubInput,
  },
  data() {
    return {}
  },
}
```

And then I can update the `App` component’s template:

```
<!-- src/App/index.vue -->
<div>
  <p>Hello World</p>
  <github-input></github-input>
</div>
```

A restriction of Vue components (which is also true in Angular and React) is that each component must have one root node, so when a component has to render multiple elements, it’s important to remember to wrap them all in something, most commonly a `div`.

## Tracking a Form Input

Our `GithubInput` component will need to do two things:

*   Keep track of the current value of the input
*   Communicate that the value has changed, so that other components can know and therefore update their state.

We can do the first version by creating a `form` with an `input` element in it. We can use Vue’s built-in directives that enable us to keep track of form values. The template for `GithubInput` looks like so:

```
<form v-on:submit.prevent="onSubmit">
  <input type="text" v-model="username" placeholder="Enter a github username here" />
  <button type="submit">Go!</button>
</form>
```

There are two important attributes that you’ll notice: `v-on` and `v-model`.

`v-on` is how we bind to DOM events in Vue and call a function. For example, `<p v-on:click="foo">Click me!</p>` would call the component’s `foo` method every time the paragraph was clicked. If you’d like to go through event handling in greater detail, I highly recommend the [Vue documentation on event handling](https://vuejs.org/v2/guide/events.html).

`v-model` creates a two-way data binding between a form input and a piece of data. Behind the scenes, `v-model` is effectively listening for change events on the form input and updating the data in the Vue component to match.

Taking our template above into consideration, here’s how we’re using `v-on` and `v-model` to deal with the data in the form:

*   `v-on:submit.prevent="onSubmit"` binds the method `onSubmit` to be run when the form is submitted. By adding `.prevent` that means that Vue will automatically prevent the default action from occurring. (If Vue didn’t do this, we could call `event.preventDefault()` in our code, but we might as well take advantage of Vue’s feature.)
*   `v-model:username` binds the input’s value to a value, `username`, in our code. For those of you familiar with Angular you may recognize this as very similar to `ng-model`. When we created `GithubInput` we declared that it had a piece of data, `username`, and here we’ve bound that piece of data to the input field. The two will automatically be kept in sync.

Now, back in our component’s JavaScript, we can declare the `onSubmit` method. Note that the name here is entirely arbitrary — you can choose whatever you’d like — but I like to stick with the convention of naming the function after the event that will trigger it:

```
export default {
  name: 'GithubInput',
  data() {
    return { username: '', }
  },
  methods: {
    onSubmit(event) {
      if (this.username && this.username !== '') {
      }
    }
  }
}
```

We can refer to data directly on `this`, so `this.username` will give us the latest value of the text box. If it’s not empty, we want to let other components know that the data has changed. For this, we’ll use a message bus. These are objects that components can emit events on and use to listen to other events. When your application grows larger you might want to look into a more structured approach, such as [Vuex](https://github.com/vuejs/vuex). For now, a message bus does the job.

The great news is that we can use an empty Vue instance as a message bus. To do so, we’ll create `src/bus.js`, which simply creates a Vue instance and exports it:

```
import Vue from 'vue'
const bus = new Vue()

export default bus
```

In the `GithubInput` component we can then import that module and use it by emitting an event when the username changes:

```
import bus from '../bus'

export default {
  ...,
  methods: {
    onSubmit(event) {
      if (this.username && this.username !== '') {
        bus.$emit('new-username', this.username)
      }
    }
  },
  ...
}
```

With that, our form is done, and we’re ready to start doing something with the resulting data.

## Displaying Results From GitHub

The `GithubOutput` component has the same structure as our other two components. In `GithubOutput/script.js` we also import the `bus` module, as we’ll need it to know when the username changes. The data that this component will be responsible for will be an object that maps GitHub usernames to the data we got from the GitHub API. This means we won’t have to make the request to the API every single time; if we’ve already fetched the data previously we can simply reuse it. We’ll also store the last username we were given, so we know what data to display on screen:

```
// src/GithubOutput/script.js
import bus from '../bus'
import Vue from 'vue'

export default {
  name: 'GithubOutput',
  data() {
    return {
      currentUsername: null,
      githubData: {}
    }
  }
}
```

When the component is created, we want to listen for any `new-username` events that are emitted on the message bus. Thankfully, Vue supports a number of [lifecycle hooks](https://vuejs.org/api/#Options-Lifecycle-Hooks), including `created`. Because we’re responsible developers, let’s also stop listening for events when the component is destroyed by using the `destroyed` event:

```
export default {
  name: 'GithubOutput',
  data: { ... },
  created() {
    bus.$on('new-username', this.onUsernameChange)
  },
  destroyed() {
    bus.$off('new-username', this.onUsernameChange)
  }
}
```

We then define the `onUsernameChange` method, which will be called and will set the `currentUsername` property:

```
methods: {
  onUsernameChange(name) {
    this.currentUsername = name
  }
},
```

Note that we don’t have to explicitly bind the `onUsernameChange` method to the current scope. When you define methods on a Vue component, Vue automatically calls `myMethod.bind(this)` on them, so they’re always bound to the component. This is one of the reasons why you need to define your component’s methods on the `methods` object, so Vue is fully aware of them and can set them up accordingly.

### Conditional Rendering

If we don’t have a username — as we won’t when the component is first created — we want to show a message to the user. Vue has [a number of conditional rendering techniques](https://vuejs.org/guide/conditional.html), but the easiest is the `v-if` directive, which takes a condition and will only render the element if it exists. It also can be paired with `v-else`:

```
<!-- src/GithubOutput/index.vue-->
<template>
  <div>
    <p v-if="currentUsername == null">
      Enter a username above to see their GitHub data
    </p>
    <p v-else>
      Below are the results for {{ currentUsername }}
    </p>
  </div>
</template>
<script src="./script.js"></script>
<style scoped src="./style.css"></style>
```

Once again, this will look very familiar to any Angular developers. We use double equals rather than triple equals here because we want the conditional to be true not only if `currentUsername` is `null` but also if it’s undefined, and `null == undefined` is `true`.

### Fetching from GitHub

Vue.js doesn’t ship with a built-in HTTP library, and for good reason. These days the `fetch` API ships natively in many browsers (although at the time of writing, not IE11, Safari or iOS Safari). For the sake of this tutorial I’m not going to use a polyfill, but you can [easily polyfill the API in browsers](https://github.com/github/fetch) if you need to. If you don’t like the fetch API there are many third-party libraries for HTTP, and the one mentioned in the Vue docs is [Axios](https://github.com/mzabriskie/axios).

I’m a big proponent of frameworks like Vue not shipping with HTTP libraries. It keeps the bundle size of the framework down and leaves it to developers to pick the library that works best for them, and easily customize requests as needed to talk to their API. I’ll stick to the fetch API in this article, but feel free to swap it out for one that you prefer.

If you need an introduction to the fetch API, check out [Ludovico Fischer’s post on SitePoint](https://www.sitepoint.com/introduction-to-the-fetch-api/), which will get you up to speed.

To make the HTTP request, we’ll give the component another method, `fetchGithubData`, that makes a request to the GitHub API and stores the result. It will also first check to see if we already have data for this user, and not make the request if so:

```
methods: {
  ...
  fetchGithubData(name) {
    // if we have data already, don't request again
    if (this.githubData.hasOwnProperty(name)) return

    const url = `https://api.github.com/users/${name}`
    fetch(url)
      .then(r => r.json())
      .then(data => {
        // in here we need to update the githubData object
      })
  }
}
```

We then finally just need to trigger this method when the username changes:

```
methods: {
  onUsernameChange(name) {
    this.currentUsername = name
    this.fetchGithubData(name)
  },
  ...
}
```

There’s one other thing to be aware of, due to the way that Vue keeps track of the data you’re working with so that it knows when to update the view. There is a great [Reactivity guide](https://vuejs.org/guide/reactivity.html) which explains it in detail, but essentially Vue isn’t able to magically know when you’ve added or deleted a property from an object, so if we do:

```
this.githubData[name] = data
```

Vue won’t recognize that and won’t update our view. Instead, we can use the special `Vue.set` method, which explicitly tells Vue that we’ve added a key. The above code would then look like so:

```
Vue.set(this.githubData, name, data)
```

This code will modify `this.githubData`, adding the key and value that we pass it. It also notifies Vue of the change so it can rerender.

Now our code looks like so:

```
const url = `https://api.github.com/users/${name}`
fetch(url)
  .then(r => r.json())
  .then(data => {
    Vue.set(this.githubData, name, data)
  })
```

Finally, we need to register the `GitHubOutput` component with the `App` component:

```
// src/App/script.js
import GithubInput from '../GithubInput/index.vue'
import GithubOutput from '../GithubOutput/index.vue'

export default {
  name: 'App',
  components: {
    'github-input': GithubInput,
    'github-output': GithubOutput,
  },
  data() {
    return {}
  },
}
```

And include it in the template:

```
<!-- src/App/index.vue -->
<template>
  <div>
    <github-input></github-input>
    <github-output></github-output>
  </div>
</template>
```

Although we haven’t yet written the view code to show the fetched data on screen, you should be able to fill in the form with your username and then inspect the Vue devtools to see the data requested from GitHub. This shows how useful and powerful these devtools are; you can inspect the local state of any component and see exactly what’s going on.

### Showing Some Stats in the View

We can now update the template to show some data. Let’s wrap this code in another `v-if` directive so that we only render the data if the request has finished:

```
<!-- src/GithubOutput/index.vue -->
<p v-if="currentUsername == null">
  Enter a username above to see their GitHub data
</p>
<p v-else>
  Below are the results for {{ currentUsername }}
  <div v-if="githubData[currentUsername]">
    <h4>{{ githubData[currentUsername].name }}</h4>
    <p>{{ githubData[currentUsername].company }}</p>
    <p>Number of repos: {{ githubData[currentUsername].public_repos }}</p>
  </div>
</p>
```

With that, we can now render the GitHub details to the screen, and our app is complete!

## Refactors

There are definitely some improvements we can make. The above bit of HTML that renders the GitHub data only needs a small part of it — the data for the current user. This is the perfect case for another component that we can give a user’s data to and it can render it.

Let’s create a `GithubUserData` component, following the same structure as with our other components:

```
mkdir src/GithubUserData
touch src/GithubUserData/{index.vue,script.js,style.css}
```

There’s only one tiny difference with this component: it’s going to take a property, `data`, which will be the data for the user. Properties (or, “props”) are bits of data that a component will be passed by its parent, and they behave in Vue much like they do in React. In Vue, you have to explicitly declare each property that a component needs, so here I’ll say that our component will take one prop, `data`:

```
// src/GithubUserData/script.js
export default {
  name: 'GithubUserData',
  props: ['data'],
  data() {
    return {}
  }
}
```

One thing I really like about Vue is how explicit you have to be; all properties, data, and components that a component will use are explicitly declared. This makes the code much nicer to work with and, I imagine, much easier as projects get bigger and more complex.

In the new template, we have exactly the same HTML as before, although we can refer to `data` rather than `githubData[currentUsername]`:

```
<!-- src/GithubUserData/index.vue -->
<template>
  <div v-if="data">
    <h4>{{ data.name }}</h4>
    <p>{{ data.company }}</p>
    <p>Number of repos: {{ data.public_repos }}</p>
  </div>
</template>
<script src="./script.js"></script>
<style scoped src="./style.css"></style>
```

To use this component we need to update the `GithubOutput` component. Firstly, we import and register `GithubUserData`:

```
// src/GithubOutput/script.js
import bus from '../bus'
import Vue from 'vue'
import GithubUserData from '../GithubUserData/index.vue'

export default {
  name: 'GithubOutput',
  components: {
    'github-user-data': GithubUserData,
  },
  ...
}
```

You can use any name for the component when declaring it, so where I’ve placed `github-user-data`, you could place anything you want. It’s advisable that you stick to components with a dash in them. Vue doesn’t enforce this, but the W3C specification on custom elements states that they must contain a dash to prevent naming collisions with elements added in future versions of HTML.

Once we’ve declared the component, we can use it in our template:

```
<!-- src/GithubOutput/index.vue -->
<p v-else>
  Below are the results for {{ currentUsername }}:
  <github-user-data :data="githubData[currentUsername]"></github-user-data>
</p>
```

The crucial part here is how I pass the `data` property down to the component:

```
:data="githubData[currentUsername]"
```

The colon at the start of that attribute is crucial; it tells Vue that the attribute we’re passing down is dynamic and that the component should be updated every time the data changes. Vue will evaluate the value of `githubData[currentUsername]` and ensure that the `GithubUserData` component is kept up to date as the data changes.

If you find `:data` a bit short and magical, you can also use the longer `v-bind` syntax:

```
v-bind:data="githubData[currentUsername]"
```

The two are equivalent, so use whichever you prefer.

## Conclusion

With that, our GitHub application is in a pretty good state! You can find all [the code on GitHub](https://github.com/sitepoint-editors/vue2-demo-project) and even check out the [application running online](http://sitepoint-vue2-demo.surge.sh/).

I had high hopes when getting started with Vue, as I’d heard only good things, and I’m happy to say it really met my expectations. Working with Vue feels like taking the best parts of React and merging them with the best parts of Angular. Some of the directives (like `v-if`, `v-else`, `v-model` and so on) are really easy to get started with (and easier to immediately understand than doing conditionals in React’s JSX syntax), but Vue’s component system feels very similar to React’s.

You’re encouraged to break your system down into small components, and all in all I found it a very seamless experience. I also can’t commend the Vue team highly enough for their documentation: it’s absolutely brilliant. The guides are excellent, and the API reference is thorough yet easy to navigate to find exactly what you’re after.

# Chapter 2: Getting Started with Vuex: a Beginner’s Guide

### by Michael Wanyoike

In single-page applications, the concept of *state* relates to any piece of data that can change. An example of state could be the details of a logged-in user, or data fetched from an API.

Handling state in single-page apps can be a tricky process. As an application gets larger and more complex, you start to encounter situations where a given piece of state needs to be used in multiple components, or you find yourself passing state through components that don’t need it, just to get it to where it needs to be. This is also known as “prop drilling”, and can lead to some unwieldy code.

[Vuex](https://vuex.vuejs.org/) is the official state management solution for Vue. It works by having a central store for shared state, and providing methods to allow any component in your application to access that state. In essence, Vuex ensures your views remain consistent with your application data, regardless of which function triggers a change to your application data.

In this article, I’ll offer you a high-level overview of Vuex and demonstrate how to implement it into a simple app.

## A Shopping Cart Example

Let’s consider a real-world example to demonstrate the problem that Vuex solves.

When you go to a shopping site, you’ll usually have a list of products. Each product has an *Add to Cart* button and sometimes an *Items Remaining* label indicating the current stock or the maximum number of items you can order for the specified product. Each time a product is purchased, the current stock of that product is reduced. When this happens, the *Items Remaining* label should update with the correct figure. When the product’s stock level reaches 0, the label should read *Out of Stock*. In addition, the *Add to Cart* button should be disabled or hidden to ensure customers can’t order products that are currently not in inventory.

Now ask yourself how you’d implement this logic. It may be trickier than you think. And let me throw in a curve ball. You’ll need another function for updating stock records when new stock comes in. When the depleted product’s stock is updated, both the *Items Remaining* label and the *Add to Cart* button should be updated instantly to reflect the new state of the stock.

Depending on your programming prowess, your solution may start to look a bit like spaghetti. Now, let’s imagine your boss tells you to develop an API that allows third-party sites to sell the products directly from the warehouse. The API needs to ensure that the main shopping website remains in sync with the products’ stock levels. At this point you feel like pulling your hair out and demanding why you weren’t told to implement this earlier. You feel like all your hard work has gone to waste, as you’ll need to completely rework your code to cope with this new requirement.

This is where a state management pattern library can save you from such headaches. It will help you organize the code that handles your front-end data in a way that makes adding new requirements a breeze.

## Prerequisites

Before we start, I’ll assume that you:

*   have a basic knowledge of [Vue.js](https://www.sitepoint.com/getting-started-with-vue-js/)
*   are familiar with [ES6](https://www.sitepoint.com/tag/es6/) and [ES7](https://www.sitepoint.com/es2017-whats-new/) language features

You’ll also need to have a recent version of Node.js that’s not older than version 6.0\. At the time of writing, Node.js v10.13.0 (LTS) and npm version 6.4.1 are the most recent. If you don’t have a suitable version of Node installed on your system already, I recommend [using a version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

Finally, you should have the most recent version of the [Vue CLI](https://cli.vuejs.org/) installed:

```
npm install -g @vue/cli
```

## Build a Counter Using Local State

In this section, we’re going to build a simple counter that keeps track of its state locally. Once we’re done, I’ll go over the fundamental concepts of Vuex, before looking at how to rewrite the counter app to use Vue’s official state management solution.

### Getting Set Up

Let’s generate a new project using the CLI:

```
vue create vuex-counter
```

A wizard will open up to guide you through the project creation. Select *Manually select features* and ensure that you choose to install Vuex.

Next, change into the new directory and in the `src/components` folder, rename `HelloWorld.vue` to `Counter.vue`:

```
cd vuex-counter
mv src/components/HelloWorld.vue src/components/Counter.vue
```

Finally, open up `src/App.vue` and replace the existing code with the following:

```
<template>
  <div id="app">
    <h1>Vuex Counter</h1>
    <Counter/>
  </div>
</template>

<script>
import Counter from './components/Counter.vue'

export default {
  name: 'app',
  components: {
    Counter
  }
}
</script>
```

You can leave the styles as they are.

### Creating the Counter

Let’s start off by initializing a count and outputting it to the page. We’ll also inform the user whether the count is currently even or odd. Open up `src/components/Counter.vue` and replace the code with the following:

```
<template>
  <div>
    <p>Clicked {{ count }} times! Count is {{ parity }}.</p>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  data: function() {
    return {
      count: 0
    };
  },
  computed: {
    parity: function() {
      return this.count % 2 === 0 ? 'even' : 'odd';
    }
  }
}
</script>
```

As you can see, we have one state variable called `count` and a computed function called `parity` which returns the string `even` or `odd` depending on the whether `count` is an odd or even number.

To see what we’ve got so far, start the app from within the root folder by running `npm run serve` and navigate to [http://localhost:8080](http://localhost:8080).

Feel free to change the value of the counter to show that the correct output for both `counter` and `parity` is displayed. When you’re satisfied, make sure to reset it back to 0 before we proceed to the next step.

### Incrementing and Decrementing

Right after the `computed` property in the `<script>` section of `Counter.vue`, add this code:

```
methods: {
  increment: function () {
    this.count++;
  },
  decrement: function () {
    this.count--;
  },
  incrementIfOdd: function () {
    if (this.parity === 'odd') {
      this.increment();
    }
  },
  incrementAsync: function () {
    setTimeout(() => {
      this.increment()
    }, 1000)
  }
}
```

The first two functions, `increment` and `decrement`, are hopefully self-explanatory. The `incrementIfOdd` function only executes if the value of `count` is an odd number, whereas `incrementAsync` is an asynchronous function that performs an increment after one second.

In order to access these new methods from the template, we’ll need to define some buttons. Insert the following after the template code which outputs the count and parity:

```
<button @click="increment" variant="success">Increment</button>
<button @click="decrement" variant="danger">Decrement</button>
<button @click="incrementIfOdd" variant="info">Increment if Odd</button>
<button @click="incrementAsync" variant="warning">Increment Async</button>
```

After you’ve saved, the browser should refresh automatically. Click all of the buttons to ensure everything is working as expected.

#### Live Code

[Vue Counter Using Local State](https://codepen.io/SitePoint/pen/xQXNwm/) shows what you should have ended up with.

The counter example is now complete. Let’s move and examine the fundamentals of Vuex, before looking at how we would rewrite the counter to implement them.

## How Vuex Works

Before we go over the practical implementation, it’s best that we acquire a basic grasp of how Vuex code is organized. If you’re familiar with similar frameworks such as Redux, you shouldn’t find anything too surprising here. If you haven’t dealt with any Flux-based state management frameworks before, please pay close attention.

### The Vuex Store

The store provides a centralized repository for shared state in Vue apps. This is what it looks like in its most basic form:

```
// src/store/index.js

import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

export default new Vuex.Store({
  state: {
    // put variables and collections here
  },
  mutations: {
    // put sychronous functions for changing state e.g. add, edit, delete
  },
  actions: {
    // put asynchronous functions that can call one or more mutation functions
  }
})
```

After defining your store, you need to inject it into your Vue.js application like this:

```
// src/main.js
import store from './store'

new Vue({
  store,
  render: h => h(App)
}).$mount('#app')
```

This will make the injected store instance available to every component in our application as `this.$store`.

### Working with State

Also referred to as the *single state tree*, this is simply an object that contains all front-end application data. Vuex, just like Redux, operates using a single store. Application data is organized in a tree-like structure. Its construction is quite simple. Here’s an example:

```
state: {
  products: [],
  count: 5,
  loggedInUser: {
    name: 'John',
    role: 'Admin'
  }
}
```

Here we have `products` that we’ve initialized with an empty array, and `count`, which is initialized with the value 5\. We also have `loggedInUser`, which is a JavaScript object literal containing multiple fields. State properties can contain any valid datatype from Booleans, to arrays, to other objects.

There are multiple ways to display state in our views. We can reference the store directly in our templates using `$store`:

```
<template>
  <p>{{ $store.state.count }}</p>
</template>
```

Or we can return some store state from within a [computed property](https://vuejs.org/guide/computed.html):

```
<template>
  <p>{{ count }}</p>
</template>

<script>
export default {
  computed: {
    count() {
      return this.$store.state.count;
    }
  }
}
</script>
```

Since Vuex stores are reactive, whenever the value of `$store.state.count` changes, the view will change as well. All this happens behind the scenes, making your code look simple and cleaner.

#### The `mapState` Helper

Now, suppose you have multiple states you want to display in your views. Declaring a long list of computed properties can get verbose, so Vuex provides a [mapState](https://vuex.vuejs.org/api/#mapstate) helper. This can be used to generate multiple computed properties easily. Here’s an example:

```
<template>
  <div>
    <p>Welcome, {{ loggedInUser.name }}.</p>
    <p>Count is {{ count }}.</p>
  </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
  computed: mapState({
    count: state => state.count,
    loggedInUser: state => state.loggedInUser
  })
}
</script>
```

Here’s an even simpler alternative where we can pass an array of strings to the `mapState` helper function:

```
export default {
  computed: mapState([
    'count', 'loggedInUser'
  ])
}
```

This version of the code and the one above it do exactly the same thing. You should note that `mapState` returns an object. If you want to use it with other computed properties, you can use the [spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax). Here’s how:

```
computed: {
  ...mapState([
    'count', 'loggedInUser'
  ]),
  parity: function() {
    return this.count % 2  === 0 ? 'even' : 'odd'
  }
}
```

### Getters

In a Vuex store, getters are the equivalent to Vue’s computed properties. They allow you to create *derived state* that can be shared between different components. Here’s a quick example:

```
getters: {
  depletedProducts: state => {
    return state.products.filter(product => product.stock <= 0)
  }
}
```

Results of `getter` handlers (when accessed as properties) are cached and can be called as many times as you wish. They’re also reactive to state changes. In other words, if the state it depends upon changes, the `getter` function is automatically executed and the new result is cached. Any component that has accessed a `getter` handler will get updated instantly. This is how you can access a `getter` handler from a component:

```
computed: {
  depletedProducts() {
    return this.$store.getters.depletedProducts;
  }
}
```

#### The `mapGetters` Helper

You can simplify the `getters` code by using the `mapGetters` helper:

```
import { mapGetters } from 'vuex'

export default {
  //..
  computed: {
    ...mapGetters([
      'depletedProducts',
      'anotherGetter'
    ])
  }
}
```

There’s an option for passing arguments to a `getter` handler by returning a function. This is useful if you want to perform a query within the `getter`:

```
getters: {
  getProductById: state => id => {
    return state.products.find(product => product.id === id);
  }
}

store.getters.getProductById(5)
```

Do note that each time a `getter` handler is accessed via a method, it will always run and the result won’t be cached.

Compare:

```
// property notation, result cached
store.getters.depletedProducts

// method notation, result not cached
store.getters.getProductById(5)
```

### Changing State with Mutations

An important aspect of the Vuex architecture is that components never alter the state directly. Doing so can lead to odd bugs and inconsistencies in the app’s state.

Instead, the way to change state in a Vuex store is by committing a *mutation*. For those of you familiar with Redux, these are similar to *reducers*.

Here is an example of a mutation that increases a `count` variable stored in `state`:

```
export default new Vuex.Store({
  state:{
    count: 1
  },
  mutations: {
    increment(state) {
      state.count++
    }
  }
})
```

You can’t call a mutation handler directly. Instead, you trigger one by “committing a mutation” like this:

```
methods: {
  updateCount() {
    this.$store.commit('increment');
  }
}
```

You can also pass parameters to a mutation:

```
// store.js
mutations: {
  incrementBy(state, n) {
    state.count += n;
  }
}
```

```
// component
updateCount() {
  this.$store.commit('incrementBy', 25);
}
```

In the above example, we’re passing the mutation an integer by which it should increase the count. You can also pass an object as a parameter. This way, you can include multiple fields easily without overloading your mutation handler:

```
// store.js
mutations: {
  incrementBy(state, payload) {
    state.count += payload.amount;
  }
}
```

```
// component
updateCount() {
  this.$store.commit('incrementBy', { amount: 25 });
}
```

You can also perform an *object-style commit* that looks like this:

```
store.commit({
  type: 'incrementBy',
  amount: 25
})
```

The mutation handler will remain the same.

#### The `mapMutations` Helper

Similar to `mapState` and `mapGetters`, you can also use the `mapMutations` helper to reduce the boilerplate for your mutation handlers:

```
import { mapMutations } from  'vuex'

export default{
  methods: {
    ...mapMutations([
      'increment', // maps to this.increment()
      'incrementBy' // maps to this.incrementBy(amount)
    ])
  }
}
```

On a final note, mutation handlers must be synchronous. You can attempt to write an asynchronous mutation function, but you’ll come to find out later down the road that it causes unnecessary complications. Let’s move on to actions.

### Actions

Actions are functions that don’t change the state themselves. Instead, they commit mutations after performing some logic (which is often asynchronous). Here’s a simple example of an action:

```
//..
actions: {
  increment(context) {
    context.commit('increment');
  }
}
```

Action handlers receive a `context` object as their first argument, which gives us access to store properties and methods. For example:

*   `context.commit`: commit a mutation
*   `context.state`: access state
*   `context.getters`: access getters

You can also use *argument destructing* to extract the store attributes you need for your code. For example:

```
actions: {
  increment({ commit }) {
    commit('increment');
  }
}
```

As mentioned above, actions can be asynchronous. Here’s an example:

```
actions: {
  incrementAsync: async({ commit }) => {
    return await setTimeout(() => { commit('increment') }, 1000);
  }
}
```

In this example, the mutation is committed after 1,000 milliseconds.

Like mutations, action handlers aren’t called directly, but rather via a dedicated `dispatch` method on the store, like so:

```
store.dispatch('incrementAsync')

// dispatch with payload
store.dispatch('incrementBy', { amount: 25})

// dispatch with object
store.dispatch({
  type: 'incrementBy',
  amount: 25
})
```

You can dispatch an action in a component like this:

```
this.$store.dispatch('increment')
```

#### The `mapActions` Helper

Alternatively, you can use the `mapActions` helper to assign action handlers to local methods:

```
import { mapActions } from  'vuex'

export default {
  //..
  methods: {
    ...mapActions([
      'incrementBy', // maps this.increment(amount) to this.$store.dispatch(increment)
      'incrementAsync', // maps this.incrementAsync() to this.$store.dispatch(incrementAsync)
      add: 'increment' // maps this.add() to this.$store.dispatch(increment)
    ])
  }
}
```

## Re-build Counter App Using Vuex

Now that we’ve had a look at the core concepts of Vuex, it’s time to implement what we’ve learned and rewrite our counter to make use of Vue’s official state management solution.

If you fancy a challenge, you might like to have a go at doing this yourself before reading on …

When we generated our project using `Vue CLI`, we selected `Vuex` as one of the features. A couple of things happened:

1.  `Vuex` was installed as a package dependency. Check your `package.json` to confirm this.
2.  A `store.js` file was created and injected into your Vue.js application via `main.js`.

To convert our “local state” counter app to a Vuex application, open `src/store.js` and update the code as follows:

```
import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

export default new Vuex.Store({
  state: {
    count: 0
  },
  getters: {
    parity: state => state.count % 2 === 0 ? 'even' : 'odd'
  },
  mutations: {
    increment(state) {
      state.count++;
    },
    decrement(state) {
      state.count--;
    }
  },
  actions: {
    increment: ({ commit }) => commit('increment'),
    decrement: ({ commit }) => commit('decrement'),
    incrementIfOdd: ({ commit, getters }) => getters.parity === 'odd' ? commit('increment') : false,
    incrementAsync: ({ commit }) => {
      setTimeout(() => { commit('increment') }, 1000);
    }
  }
});
```

Here we can see how a complete Vuex store is structured in practice. Please go back over the theory part of this article if anything here is unclear to you.

Next, update the `src/components/Counter.vue` component by replacing the existing code within the `<script>` block. We’ll switch the local state and functions to the newly created ones in the Vuex store:

```
import { mapState mapGetters, mapActions } from 'vuex'

export default {
  name: 'Counter',
  computed: {
    ...mapState([
      'count'
    ]),
    ...mapGetters([
      'parity'
    ])
  },
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
  ])
}
```

The template code should remain the same, as we’re sticking to the previous variable and function names. See how much cleaner the code now is.

If you don’t want to use the state and getter map helpers, you can access the store data directly from your template like this:

```
<p>
  Clicked {{ $store.state.count }} times! Count is {{ $store.getters.parity }}.
</p>
```

After you’ve saved your changes, make sure to test your application. From an end-user perspective, the counter application should function exactly the same as before. The only difference is that the counter is now operating from a Vuex store.

#### Live Code

See the Pen [Vue Counter Using Vuex](https://codepen.io/SitePoint/pen/ZmaMKO/).

## Conclusion

In this article, we’ve looked at what Vuex is, what problem it solves, how to install it, as well as its core concepts. We then applied these concepts to refactor our counter app to work with Vuex. Hopefully this introduction will serve you well in implementing Vuex in your own projects.

It should also be noted that using Vuex in such a simple app is total overkill. However, in another article—*Build a Shopping List App with Vue, Vuex and Bootstrap Vue*—I’ll build a more complicated app to demonstrate a more real-world scenario, as well as some of Vuex’s more advanced features.

# Chapter 3: A Beginner’s Guide to Vue CLI

### by Ahmed Bouchefra

When building a new Vue app, the best way to get up and running quickly is to use [Vue CLI](https://cli.vuejs.org/). This is a command-line utility that allows you to choose from a range of build tools, which it will then install and configure for you. It will also scaffold out your project, providing you with a pre-configured starting point that you can build on, rather than starting everything from scratch.

The most recent version of Vue CLI is version 3\. It provides a new experience for Vue developers and helps them start developing Vue apps without dealing with the complex configuration of tools like webpack. At the same time, it can be configured and extended with plugins for advanced use cases.

Vue CLI v3 is a complete system for rapid Vue.js development and prototyping. It’s composed of different components, such as the [CLI service](https://cli.vuejs.org/guide/cli-service.html), [CLI plugins](https://cli.vuejs.org/guide/plugins-and-presets.html#plugins) and recently a [web UI](https://cli.vuejs.org/guide/creating-a-project.html#using-the-gui) that allows developers to perform tasks via an easy-to-use interface.

Throughout this article, I’ll introduce the latest version of Vue CLI and its new features. I’ll demonstrate how to install the latest version of Vue CLI and how to create, serve and build an example project.

## Vue CLI v3 Installation and Requirements

In this section, we’ll look at the requirements needed for Vue CLI v3 and how to install it.

### Requirements

Let’s start with the requirements. Vue CLI v3 requires Node.js 8.9+, but v8.11.0+ is recommended.

You can install the latest version of Node.js in various ways:

*   By downloading the binaries for your system from the [official website](https://nodejs.org).
*   By using the official package manager for your system.
*   Using a version manager. This is probably the easiest way, as it allows you to manage multiple versions of Node on the same machine. If you’d like to find out more about this approach, please see our quick tip [Installing Multiple Versions of Node.js Using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

Vue creator, Evan You, described version 3 of the CLI as a “completely different beast” from its predecessor. As such, it’s important to uninstall any previous version of the CLI (that is, 2.x.x) before preceding with this tutorial.

If the `vue-cli` package is installed globally on your system, you can remove it by running the following command:

```
npm uninstall vue-cli -g
```

### Installing Vue CLI v3

You can now install Vue CLI v3 by simply running the following command from your terminal:

```
npm install -g @vue/cli
```

#### Fixing Permissions

If you find yourself needing to add `sudo` before your command in macOS or Debian-based systems, or to use an administrator CMD prompt in Windows in order to install packages globally, then you should fix your permissions. The npm site has [a guide on how to do this](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally), or just use a version manager and you avoid the problem completely.

After successfully installing the CLI, you’ll be able to access the `vue` executable in your terminal.

For example, you can list all the available commands by executing the `vue` command:

```
vue
```

You can check the version you have installed by running:

```
vue --version
$ 3.2.1
```

## Creating a Vue Project

After installing Vue CLI, let’s now look at how we can use it to quickly scaffold complete Vue projects with a modern front-end toolset.

Using Vue CLI, you can create or generate a new Vue app by running the following command in your terminal:

```
vue create example-vue-project
```

#### Naming a Project

`example-vue-project` is the name of the project. You can obviously choose any valid name for your project.

The CLI will prompt you for the preset you want to use for your project. One option is to select the default preset which installs two plugins: Babel for transpiling modern JavaScript, and ESLint for ensuring code quality. Or you can manually select the features needed for your project from a set of official plugins. These include:

*   [Babel](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-babel)
*   [TypeScript](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-typescript)
*   [Progressive Web App support](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-pwa)
*   [Vue Router](https://github.com/vuejs/vue-router)
*   [Vuex](https://github.com/vuejs/vuex) (Vue’s official state management library)
*   CSS Pre-processors ([PostCSS](https://postcss.org/), [CSS modules](https://github.com/css-modules/css-modules), [Sass](https://sass-lang.com/), [Less](http://lesscss.org/) & [Stylus](http://stylus-lang.com/))
*   Linter/ Formatter using [ESLint](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-eslint) and [Prettier](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/eslint-config-prettier)
*   Unit Testing using [Mocha](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-unit-mocha) or [Jest](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-unit-jest)
*   E2E Testing using [Cypress](https://github.com/vuejs/vue-cli/tree/dev/packages/@vue/cli-plugin-e2e-cypress) or [Nightwatch](https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-e2e-nightwatch)

Whatever you choose, the CLI will download the appropriate libraries and configure the project to use them. And if you choose to manually select features, at the end of the prompts you’ll also have the option to save your selections as a preset so that you can reuse it in future projects.

Now let’s look at the other scripts for serving the project (using a webpack development server and hot module reloading) and building the project for production.

Navigate inside your project’s folder:

```
cd example-vue-project
```

Next, run the following command to serve your project locally:

```
npm run serve
```

The command will allow you to run a local development server from the [http://localhost:8080](http://localhost:8080) address. If you use your web browser to navigate to this address, you should see the following page:

![Welcome to Your Vue.js App](Images/vue-cli-1.png) 

The development server supports features like hot code reloading, which means you don’t need to stop and start your server every time you make any changes to your project’s source code. It will even preserve the state of your app!

And when you’ve finished developing your project, you can use the following command to build a production bundle:

```
npm run build
```

This will output everything to a `dist` folder within your project. You can [read more about deployment here](https://cli.vuejs.org/guide/deployment.html).

### What is the Vue CLI Service?

The [Vue CLI Service](https://cli.vuejs.org/guide/cli-service.html) is a run-time dependency (`@vue/cli-service`) that abstracts webpack and provides default configurations. It can be upgraded, configured and extended with plugins.

It provides multiple scripts for working with Vue projects, such as the `serve`, `build` and `inspect` scripts.

We’ve seen the `serve` and `build` scripts in action already. The `inspect` script allows you to inspect the webpack config in a project with `vue-cli-service`. Try it out:

```
vue inspect
```

As you can see, that produces a lot of output. Later on we’ll see how to tweak the webpack config in a Vue CLI project.

### The Project Anatomy

A Vue project generated with the CLI has a predefined structure that adheres to best practices. If you choose to install any extra plugins (such as the Vue router), the CLI will also create the files necessary to use and configure these libraries.

Let’s take a look at the important files and folders in a Vue project when using the default preset.

*   `public`. This folder contains public files like `index.html` and `favicon.ico`. Any static assets placed here will simply be copied and not go through webpack.
*   `src`. This folder contains the source files for your project. Most work will be done here.
*   `src/assets`. This folder contains the project’s assets such as `logo.png`.
*   `src/components`. This folder contains the Vue components.
*   `src/App.vue`. This is the main Vue component of the project.
*   `src/main.js`. This is the main project file which bootstraps the Vue application.
*   `babel.config.js`. This is a configuration file for Babel.
*   `package.json`. This file contains a list of the project’s dependencies, as well as the configuration options for ESLint, PostCSS and supported browsers.
*   `node_modules`. This folder contains the installed npm packages.

This is a screenshot of the project’s anatomy:

![Project anatomy](Images/vue-cli-2.png) 

## Vue CLI Plugins

Vue CLI v3 is designed with a plugin architecture in mind. In this section, we’ll look at what plugins are and how to install them in your projects. We’ll also look at some popular plugins that can help add advanced features by automatically installing the required libraries and making various settings—all of which would otherwise have to be done manually.

### What a Vue Plugin Is

CLI Plugins are just npm packages that provide additional features to your Vue project. The `vue-cli-service` binary automatically resolves and loads all plugins listed in the `package.json` file.

The base configuration for a Vue CLI 3 project is webpack and Babel. All the other features can be added via plugins.

There are official plugins provided by the Vue team and community plugins developed by the community. Official plugin names start with `@vue/cli-plugin-`, and community plugin names start with `vue-cli-plugin-`.

Official Vue CLI 3 plugins include:

*   Typescript
*   PWA
*   Vuex
*   Vue Router
*   ESLint
*   Unit testing etc.

### How to Add a Vue Plugin

Plugins are either automatically installed when creating the project or explicitly installed later by the developer.

You can install many built-in plugins in a project when initializing your project, and install any other additional plugins in the project using the `vue add my-plugin` command at any point of your project.

You can also install plugins with presets, and group your favorite plugins as reusable presets that you can use later as the base for other projects.

### Some Useful Vue Plugins

There are many Vue CLI plugins that you might find useful for your next projects. For example, the [Vuetify UI library is available as a plugin](https://github.com/vuetifyjs/vue-cli-plugin-vuetify), as is [Storybook](https://github.com/storybooks/vue-cli-plugin-storybook). You can also use the [Electron Builder plugin](https://github.com/nklayman/vue-cli-plugin-electron-builder) to quickly scaffold out a Vue project based on Electron.

I’ve also written a couple of plugins which you can make use of:

*   [vue-cli-plugin-nuxt](https://www.npmjs.com/package/vue-cli-plugin-nuxt): a Vue CLI plugin for quickly creating a universal Vue application with Nuxt.js
*   [vue-cli-plugin-bootstrap](https://www.npmjs.com/package/vue-cli-plugin-bootstrap): a Vue CLI plugin for adding Bootstrap 4 to your project

If you’d like to find out more about plugins, check out this great article on Vue Mastery: [5 Vue CLI 3 plugins for your Vue project](https://medium.com/vue-mastery/5-vue-cli-3-plugins-for-your-vue-project-df5af357d076).

## What About webpack?

webpack is abstracted away by the Vue CLI and the different APIs it provides to access and mutate the webpack configuration.

Most project configuration for Vue CLI is abstracted into plugins and is merged into the base configuration at runtime. But in some situations you might want to manually tweak the webpack configuration for your project. In that case, you can either:

*   Create a `vue.config.js` file in your project root and then make any configuration within a `configureWebpack` option:

    ```
     module.exports = {
        configureWebpack: {
          // custom config here
        }
      }
    ```

*   Mutate the webpack configuration using tools like [webpack-chain](https://neutrino.js.org/webpack-chain.html)

You can find out [more about working with Vue CLI and webpack here](https://cli.vuejs.org/guide/webpack.html).

## Vue CLI UI

Let’s now look at the [Vue CLI UI](https://cli.vuejs.org/guide/creating-a-project.html#using-the-gui), covering how to launch it and the different views used to create and manage projects a graphical user interface.

Vue CLI v3 provides a modern web interface that allows you to create and manage projects without using terminal commands. You can launch the UI as follows:

```
vue ui
```

The UI should be available from the [http://localhost:8000](http://localhost:8000) address.

![Vue Project Manager](Images/vue-cli-3.png) 

You create a new project from the *Create* tab. Browse for the location where you want to create your project, then click on the *+ Create a new project here* button.

![Create a new project here](Images/vue-cli-4.png) 

You’ll be taken to a new interface where you need to enter different details about your project such as the name, the project’s location, the package manager and whether or not you want to initialize a Git repository.

![Create a new project](Images/vue-cli-5.png) 

Enter the details and click on the *Next* button. You’ll be taken to the *Presets* tab where you can specify the preset for your project.

You can choose:

*   *Default preset* for a default preset with Babel and ESLint plugins
*   *Manual* for manually selecting plugins
*   *Remote preset* for using a remote preset from a Git repository

Let’s continue with the default preset:

![Select a preset](Images/vue-cli-6.png)

#### Presets

A preset is an association of plugins and configurations.

Next, you can click on the *Create Project* button to start generating your project. You’ll be taken to a new interface that shows you the progress of your project generation.

Next, you’ll be taken to the project dashboard—where your can put widgets, which you can add using the *Customize* button at the top right of the page, after which they’ll be automatically saved.

![Project dashboard](Images/vue-cli-7.png) 

On the left of the dashboard you can find different pages:

*   *Plugins* for adding new Vue CLI plugins
*   *Dependencies* for managing the packages
*   *Configuration* for configuring the tools
*   *Tasks* for running scripts

Switch to the *Tasks* page.

![Project tasks](Images/vue-cli-8.png) 

Next, click on the *serve* button and then on the *Run task* button to serve your project.

![Run task](Images/vue-cli-9.png) 

You can stop serving the project using the *Stop task* button. You can also open the application from this interface and see information about the project, such as the size of assets, modules and dependencies, speed statistics and so on.

![App statistics](Images/vue-cli-10.png)

## Conclusion

In this article we’ve seen an overview of the new Vue CLI version, which provides a whole host of developer-friendly features such interactive project scaffolding, a rich collection of official plugins integrating the best tools in the front-end ecosystem, and a full graphical user interface to create and manage Vue.js projects.

The CLI is a powerful tool in the hands of Vue developers, but in cases when you don’t need all of its features, it might be preferable to use Vue.js in your project without the CLI. You can see how to do this in our tutorial *[Getting up and Running with the Vue.js 2.0 Framework](https://www.sitepoint.com/up-and-running-vue-js-2-0/)*.

# Chapter 4: A Beginner’s Guide to Working With Components in Vue

### by Kingsley Silas

One of the great things about working with Vue is its component-based approach to building user interfaces. This allows you to break your application into smaller, reusable pieces (components) which you can then use to build out a more complicated structure.

In this guide, I’ll offer you a high-level introduction to working with components in Vue. I’ll look at how to create components, how to pass data between components (via both props and an event bus) and how to use Vue’s `<slot>` element to render additional content within a component.

Each example will be accompanied by a runnable CodePen demo.

## How to Create Components in Vue

Components are essentially reusable Vue instances with a name. There are various ways to create components within a Vue application. For example, in a small- to medium-sized project you can use the [Vue.component](https://vuejs.org/v2/api/#Vue-component) method to register a global component, like so:

```
Vue.component('my-counter', {
  data() {
    return {
      count: 0
    }
  },
  template: `<div>{{ count }}</div>`
})

new Vue({ el: '#app' })
```

The name of the component is `my-counter`. It can be used like so:

```
<div id="app">
  <my-counter></my-counter>
</div>
```

When naming your component, you can choose kebab case (`my-custom-component`) or Pascal case (`MyCustomComponent`). You can use either variation when referencing your component from within a template, but when referencing it directly in the DOM (as in the example above), *only* the kebab case tag name is valid.

You might also notice that, in the example above, `data` is a function which returns an object literal (as opposed to being an object literal itself). This is so that each instance of the component receives its own `data` object and doesn’t have to share one global instance with all other instances.

There are several ways to define a component template. Above we are using a template literal, but we could also use a `<script tag>` marked with `text/x-template` or an in-DOM template. You can read more about [the different ways of defining templates here](https://medium.com/js-dojo/7-ways-to-define-a-component-template-in-vuejs-c04e0c72900d).

### Single-file Components

In more complex projects, global components can quickly become unwieldy. In such cases, it makes sense to craft your application to use single-file components. As the name suggests, these are single files with a `.vue` extension, which contain a `<template>`, `<script>` and `<style>` section.

For our example above, an `App` component might look like this:

```
<template>
  <div id="app">
    <my-counter></my-counter>
  </div>
</template>

<script>
import myCounter from './components/myCounter.vue'

export default {
  name: 'app',
  components: { myCounter }
}
</script>

<style></style>
```

And a `MyCounter` component might look like this:

```
<template>
  <div>{{ count }}</div>
</template>

<script>
export default {
  name: 'my-counter',
  data() {
    return {
      count: 0
    }
  }
}
</script>

<style></style>
```

As you can see, when using single-file components, it’s possible to import and use these directly within the components where they’re needed.

In this guide, I’ll present all of the examples using the `Vue.component()` method of registering a component.

Using single-file components generally involves a build step (for example, with Vue CLI). If this is something you’d like to find out more about, please check out “A Beginner’s Guide to Vue CLI” in this Vue series.

## Passing Data to Components Via Props

Props enable us to pass data from a parent component to child component. This makes it possible for our components to be in smaller chunks to handle specific functionalities. For example, if we have a blog component we might want to display information such as the author’s details, post details (title, body and images) and comments.

We can break these into child components, so that each component handles specific data, making the component tree look like this:

```
<BlogPost>
  <AuthorDetails></AuthorDetails>
  <PostDetails></PostDetails>
  <Comments></Comments>
</BlogPost>
```

If you’re still not convinced about the benefits of using components, take a moment to realize how useful this kind of composition can be. If you were to revisit this code in the future, it would be immediately obvious how the page is structured and where (that is, in which component) you should look for which functionality. This declarative way of composing an interface also makes it much easier for someone who isn’t familiar with a codebase to dive in and become productive quickly.

Since all the data will be passed from the parent component, it can look like this:

```
new Vue({
  el: '#app',
  data() {
    return {
      author: {
        name: 'John Doe',
        email: 'jdoe@example.com'
      }
    }
  }
})
```

In the above component, we have the author details and post information defined. Next, we have to create the child component. Let’s call the child component `author-detail`. So our HTML template will look like this:

```
<div id="app">
  <author-detail :owner="author"></author-detail>
</div>
```

We’re passing the child component the `author` object as props with the name `owner`. It’s important to note the difference here. In the child component, `owner` is the name of the prop with which we receive the data from the parent component. The data we want to receive is called `author`, which we’ve defined in our parent component.

To have access to this data, we need to declare the props in the `author-detail` component:

```
Vue.component('author-detail', {
  template: `
    <div>
      <h2>{{ owner.name }}</h2>
      <p>{{ owner.email }}</p>
    </div>
  ´,
  props: ['owner']
})
```

We can also enable validation when passing props, to make sure the right data is being passed. This is similar to [PropTypes](https://reactjs.org/docs/typechecking-with-proptypes.html) in React. To enable validation in the above example, change our component to look like this:

```
Vue.component('author-detail', {
  template: `
    <div>
      <h2>{{ owner.name }}</h2>
      <p>{{ owner.email }}</p>
    </div>
  `,
  props: {
    owner: {
      type: Object,
      required: true
    }
  }
})
```

If we pass the wrong prop type, you’ll see an error in your console that looks like what I have below:

```
"[Vue warn]: Invalid prop: type check failed for prop 'text'. Expected Boolean, got String.
(found in component <>)"
```

There’s an [official guide in the Vue docs](https://vuejs.org/v2/guide/components-props.html#Prop-Validation) that you can use to learn about prop validation.

#### Live Code

See the Pen [Vue Componets - Props](https://codepen.io/SitePoint/pen/NegVgK/).

## Communicating From a Child to Parent Component via an Event Bus

[Events](https://vuejs.org/v2/guide/events.html) are handled by creating wrapper methods that are triggered when the chosen event takes place. By way of a refresher, let’s build on our original counter example, so that it increases each time a button is clicked.

This is what our component should look like:

```
new Vue({
  el: '#app',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++
    }
  }
})
```

And our template:

```
<div id="app">
  {{ count }}
  <div>
    <button @click="increment">+</button>
  </div>
</div>
```

This is hopefully simple enough. As you can see, we’re hooking into the `onClick` event to trigger a custom `increase` method whenever the button is clicked. The `increase` method is then incrementing our `count` data property. Now let’s expand the example to move the counter button into a separate component and display the count in the parent. We can do this using an event bus.

Event buses come in handy when you want to communicate from a child component to parent component. This is contrary to the default method of communication, which happens from parent to child. You can make use of an event bus if your application isn’t big enough to require the use of Vuex. (You can read more about that in “Getting Started with Vuex: a Beginner’s Guide” in this Vue series.)

So here’s what we want to do: the `count` will be declared in the parent component and passed down to a child component. Then in the child component, we want to increment the value of count and also ensure that the value is updated in the parent component.

The App component will look like this:

```
new Vue({
  el: '#app',
  data() {
    return {
      count: 0
    }
  }
```

Then in the child component, we want to receive the count via props and have a method to increment it. We don’t want to display the value of count in the child component. We only want to do the increment from the child component and have it reflected in the parent component:

```
Vue.component('counter', {
  template: `
    <div>
      <button @click="increment">+</button>
    </div>
  `,
  props: {
    value: {
      type: Number,
      required: true
    }
  },
  methods: {
    increment() {
      this.count++
    }
  }
})
```

Then our template will look like this:

```
<div id="app">
  <h3>
    {{ count }}
  </h3>
  <counter :count="count" />
</div>
```

If you try incrementing the value like that, it won’t work. To make it work, we have to emit an event from the child component, send the new value of `count` and also listen for this event in the parent component.

First, we create a new instance of Vue and set it to `eventBus`:

```
const eventBus = new Vue();
```

We can now make use of the event bus in our component. The child component will look like this:

```
Vue.component('counter', {
  props: {
    count: {
      type: Number,
      required: true
    }
  },
  methods: {
    increment() {
      this.count++
      eventBus.$emit('count-incremented', this.count)
    }
  },
  template: `
  <div>
    <button @click="increment">+</button>
  </div>
  `
})
```

The event is emitted each time the `increment` method is called. We have to listen for the event in the main component and then set `count` to the value we obtained through the event that was emitted:

```
new Vue({
  el: '#app',
  data() {
    return {
      count: 0
    }
  },
  created() {
    eventBus.$on('count-incremented', (count) => {
      this.count = count
    })
  }
})
```

Note that we’re making use of [Vue’s created lifecycle method](https://vuejs.org/v2/api/#created) to hook into the component before it’s mounted and to set up the event bus.

Using an event bus is good if your application isn’t complex, but please remember that, as your application grows, you may need to make use of Vuex instead.

#### Live Code

See the Pen [Vue Components - Event Bus](https://codepen.io/SitePoint/pen/qLjzZL/)

## Nesting Content in Components Using Slots

In all the examples we’ve seen so far, the components have been self-closing elements. However, in order to make components that can be composed together in useful ways, we need to be able to nest them inside one another as we do with HTML elements.

If you try using a component with a closing tag and putting some content inside, you’ll see that Vue just swallows this up. Anything within the component’s opening and closing tags is replaced with the rendered output from the component itself:

```
<div id="app">
  <author-detail :owner="author">
    <p>This will be replaced</p>
  </author-detail>
</div>
```

Luckily, [Vue’s slots](https://vuejs.org/v2/guide/components-slots.html) make it possible to pass an arbitrary value to a component. This can be anything from DOM elements from a parent component to a child component. Let’s see how they work.

The script part of our components will look like this:

```
Vue.component('list', {
  template: '#list'
})

new Vue({
  el: "#app"
})
```

Then the templates will look like this:

```
<div id="app">
  <h2>Slots</h2>
  <list>
    <h4>I am the first slot</h4>
  </list>
  <list>
    <h4>I am the second slot</h4>
  </list>
</div>

<script type="text/x-template" id="list">
  <div>
    <h3>Child Component</h3>
    <slot></slot>
  </div>
</script>
```

The content inside our `<list>` component gets rendered between the `<slot></slot>` element tag. We can also make use of fallback content, for cases where the parent doesn’t inject any.

```
<div id="app">
  <h2>Slots</h2>
  <list>
    <h4>I am the first slot</h4>
  </list>
  <list></list>
</div>

<script type="text/x-template" id="list">
  <div>
    <h3>Child Component</h3>
    <slot>This is fallback content</slot>
  </div>
</script>
```

The fallback content will render in cases where there’s no content from the parent component.

#### Live Code

See the Pen [Vue Components - Slots](https://codepen.io/SitePoint/pen/zyzQgR/).

## Conclusion

This has been a high-level introduction to working with components in Vue. We looked at how to create components in Vue, how to communicate from a parent to a child component via props and from a child to a parent via an event bus. We then finished off by looking at slots, a handy method for composing components in useful ways. I hope you’ve found the tutorial useful.

# Chapter 5: A Beginner’s Guide to Working with Forms in Vue

### by Kingsley Silas

Forms are an integral part of modern web applications. They allow us to receive input from users which we can then validate and act upon.

In this tutorial, I’m going to demonstrate how to work with forms in Vue. We’ll start off by creating a simple form and look at how to use two-way data binding to keep user input in sync with our data model. We’ll then take a look at modifiers, which allow us to change the browser’s default form-handling behavior, and filters, which allow us to format the output the user sees. We’ll finish off by implementing form validation using the [VeeValidate](https://baianat.github.io/vee-validate/) plugin. Each section will be accompanied by a runnable CodePen demo.

By the time you’ve finished reading, you’ll have seen how easy Vue makes it to work with forms, and you’ll be able to implement all of these techniques in your own apps.

Let’s get to it.

## Two-way Data Binding with v-model

Vue provides a two-way binding feature that keeps the inputs entered by your user in sync with the data model. This is made possible by using the [v-model](https://vuejs.org/v2/api/#v-model) directive like so: `v-model="entry"`.

In the data model, you’ll need to have the following:

```
data() {
  return {
    entry: 3
  }
}
```

Then our template will look like this:

```
<div id="app">
  <h2>Vue Form</h2>
  <h2>{{ entry }}</h2>
  <input type="text" v-model="entry" />
</div>
```

By default, the input field will have a value of `3`, which is the initial state for our entry. However, that doesn’t stop us from changing the state by entering another value in our input field. The value automatically changes as we do this. Underneath the hood, the `v-model` directive is shorthand for this:

```
<div id="app">
  <h2>Vue Form</h2>
  <h2>Input: {{ entry }}</h2>
  <input type="text"
     v-bind:value="entry"
     v-on:input="entry=$event.target.value"
  />
</div>
```

The `v-model` directive combines the power of [v-bind](https://vuejs.org/v2/api/#v-bind) and [v-on:input](https://vuejs.org/v2/api/#v-on) to provide you with the two-way data binding for form inputs. The above snippet can also be written like this:

```
<div id="app">
  <h2>Vue Form</h2>
  <h2>Input: {{ entry }}</h2>
  <input type="text"
    :value="entry"
    @input="entry=$event.target.value"
  />
</div>
```

Now let’s take a look at an example. If you’d like to follow along at home, do one of two things. You could create a new app using Vue CLI (which you can read about in “A Beginner’s Guide to Vue CLI” in this Vue series). The other option is to use the following template, which includes Vue from a CDN, and which you can open directly in your browser:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.1.3/css/bootstrap.min.css">
  <style>
    /* Styles here */
  </style>
</head>
<body>
  <!-- Template here -->

  <script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.5.17/vue.min.js"></script>
  <script>
    // Script here
  </script>
</body>
</html>
```

We’ll start off by adding a template that includes four types of form inputs—namely a text input, a select element, radio buttons and check boxes. You can use `v-model` with all of these inputs to keep their values in sync with a Vue instance’s data model:

```
<div id="app" class="container">
  <h2>Vue Form</h2>

  <div class="output">
    <p>Name: {{ name }}</p>
    <p>Genre: {{ genre}}</p>
    <p>Gender: {{ gender }}</p>
    <p>
      Languages:
      <span v-for="(language, index) in languages" :key="index">
        {{ language }}
        <span v-if="index + 1 < languages.length">, </span>
      </span>
    </p>
    <p>Terms Agreement: {{ agreeToTerms }}</p>
  </div>

  <form>
    <div>
      <label for="name">Name:</label>
      <input type="text" v-model="name" id="name" />
    </div>

    <div class="gender">
      <input type="radio" id="male" value="Male" v-model="gender">
      <label for="male">Male</label>
      <br>
      <input type="radio" id="female" value="Female" v-model="gender">
      <label for="female">Female</label>
    </div>

    <div>
      <select v-model="genre">
        <option disabled value="">Please select a genre</option>
        <option>Rap</option>
        <option>Indie Pop</option>
        <option>Soul</option>
      </select>
    </div>

    <div class="languages">
      <input type="checkbox" id="javascript" value="JavaScript" v-model="languages">
      <label for="javascript">Javascript</label>
      <input type="checkbox" id="ruby" value="Ruby" v-model="languages">
      <label for="ruby">Ruby</label>
      <input type="checkbox" id="python" value="Python" v-model="languages">
      <label for="python">Python</label>
    </div>

    <div>
      <label>
        <input type="checkbox" v-model="agreeToTerms"/>
        Yes, I agree to everything
      </label>
    </div>
  </form>
</div>
```

Notice that, at the top of the template, we’re doing some basic interpolation to output the values of our form fields. We’ll need to declare these as data properties on our Vue instance:

```
new Vue({
  el: '#app',
  data() {
    return {
      name: "John Doe",
      agreeToTerms: false,
      genre: '',
      gender: '',
      languages: []
    }
  }
})
```

We can finish off with some basic styling:

```
h2 {
  margin: 30px 0;
  text-align: center;
  font-size: 3em;
  color: tomato;
}

.output {
  text-align: center;
  margin: 30px;
}

form {
  width: 40%;
  max-width: 350px;
  margin: 0 auto 30px;
  border-radius: 4px;
  border: none;
  border-top: 2px solid tomato;
}

input[type="text"], select {
  background: rgba(255, 255, 255, 0.1);
  border: none;
  font-size: 16px;
  height: auto;
  margin: 0;
  outline: 0;
  padding: 10px;
  width: 100%;
  background-color: #e8eeef;
  color: #2E4049;
  box-shadow: 0 1px 0 rgba(0, 0, 0, 0.03) inset;
  margin-bottom: 20px;
}

label {
  display: inline-block;
  margin: 5px 0 10px 0;
}

input[type="checkbox"] {  margin: 0 2px 8px 0; }
input[type="radio"] {  margin: 0 2px 0 15px; }
.gender label {  margin: 0 0 10px 0; }
.languages label {  margin: 0 15px 0 0; }
p {  margin-bottom: 3px; }
```

#### Live Code

![-](Images/forms1.png)

And [here’s the demo running on CodePen](https://codepen.io/SitePoint/pen/KbpYoj/). Try altering any of the fields. You should see the updated value reflected in the UI.

## Altering the Browser’s Default Behavior with Modifiers

Events are handled in Vue using the `v-on` directive. However, there are modifiers that allow us to change the behaviors of these events.

Let’s say we have a counter that can be increased or decreased depending on the button that’s clicked. We can modify the click event to ensure that it’s only clicked once, like so:

```
<button class="incrementButton" @click.once="handleIncrement">
  Increment
</button>
```

#### Live Code

![-](Images/forms2.png)

It becomes impossible to increment the counter multiple times. [Here’s a demo that demonstrates this](https://codepen.io/SitePoint/pen/wRabgw/).

Another modifier you’ll use frequently is the `.prevent` modifier—which prevents the default behavior of an event. Let’s redo the demo above to include a form.

The template part will look like this:

```
<div id="app">
  <h2>Counter</h2>
  <form>
    <h2>{{ count }}</h2>
    <div class="div__buttons">
      <button class="incrementButton" type="submit">
        Increment
      </button>
    </div>
  </form>
</div>
```

The form will submit each time you click the button, causing the value of `count` to change to `0`. To avoid that, we have to add the `.prevent` modifier, like so:

```
<div id="app">
  <h2>Counter</h2>
  <form @submit.prevent="handleIncrement">
    ...
  </form>
</div>
```

The script section should look like this:

```
new Vue({
  el: '#app',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    handleIncrement() {
      this.count += 1;
    }
  }
})
```

That will alter the default behavior of the button. You can also use this if on anchor and form elements.

#### Live Code

![-](Images/forms3.png)

[Here’s a working demo of the technique](https://codepen.io/SitePoint/pen/WLvBMw/)

Other [event modifiers](https://vuejs.org/v2/guide/events.html#Event-Modifiers) include these:

*   `.capture`: This is used for handling an event.
*   `.self`: This will be triggered if the event’s target is the element itself.
*   `.stop`: This will stop the propagating of the event up the DOM tree.

And there are [some modifiers you can apply to `v-model` itself](https://vuejs.org/v2/guide/forms.html#Modifiers):

*   `.lazy`: This syncs the input with the data model after a `change` event. By default, `v-model` syncs after each `input` event.
*   `.number`: This typecasts user input as a number.
*   `.trim`: This automatically trims the user input.

## Formatting Output with Filters

Filters make it possible for you to transform data. They only change the displayed data, but don’t actually transform the data itself. You apply a filter to an expression using the pipe `|` symbol.

To see filters at work, let’s create a filter to capitalize text entered through an input:

```
new Vue({
  el: '#app',
  data() {
    return {
      entry: "John"
    }
  },
  filters: {
    capitalize(value) {
      return value.toUpperCase()
    }
  }
})
```

Our filter takes a parameter and returns the result of calling `.toUpperCase()` on the parameter. This is how we make use of it on our template:

```
<div id="app">
  <h2>Filters</h2>
  <p>Input: {{ entry }}</p>
  <p>Filtered Text: {{ entry | capitalize }}</p>
  <input type="text" v-model="entry" />
</div>
```

Note that the fact that the filter is a function doesn’t mean we call it with `capitalize(entry)`. In the template, we display two versions of the input—the transformed text and the original text.

Let’s say you’re working with an API that returns some posts and displays the date the posts were created. You may want to display a user-friendly date to the users. This is one of the scenarios where filter comes in handy. Using [Momentjs](http://momentjs.com/), you can create a filter for the date.

Your filter will look like this:

```
date(value) {
  return moment(value).fromNow()
}
```

Nothing special is happening here: we only call moment’s `.fromNow()` method on the parameter, which is then returned. To display the filtered date, we use `{{ created_at | date }}`.

#### Live Code

![-](Images/forms4.png)

See the Pen [Formatting Data With Filters](https://codepen.io/SitePoint/pen/bOdXXy/).

## VeeValidate

[VeeValidate](https://baianat.github.io/vee-validate/) simplifies validation for forms in Vue. In this final section, we’ll build a registration form and use VeeValidate to implement some basic validation checks.

If you’re following along using the CLI, you’ll need to install VeeValidate using npm:

```
npm install vee-validate --save
```

You’ll also need to register the plugin in `main.js`:

```
import  VeeValidate  from  "vee-validate";
Vue.use(VeeValidate);
```

Alternatively, you can pull it into your application using a CDN:

```
<script src="https://unpkg.com/vee-validate@latest"></script>
```

You’ll then need to amend your template like so:

```
<!DOCTYPE html>
<html lang="en">
<head> ... </head>
<body>
  <!-- Template here -->

  <script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.5.17/vue.min.js"></script>
  <script src="https://unpkg.com/vee-validate@latest"></script>
  <script>
    Vue.use(VeeValidate);
    new Vue({ .. })
  </script>
</body>
</html>
```

Next up, let’s create our form. We’re going to have `name`, `gender`, `phone`, `email` and `password` fields, which we’ll bind to our data model using `v-model`:

```
<div id="app">
  <h2>Register</h2>

  <form @submit.prevent="register" method="post" class="form">
    <div>
      <label for="name">Name:</label>
      <input id="name" name="name" v-validate="'required'" type="text" v-model="user.name" class="form-control" />
      <span v-show="errors.has('name')" class="text-danger">{{ errors.first('name') }}</span>
    </div>
    <div>
      <label for="gender">Gender:</label>
      <select id="gender" name="gender" v-model="user.gender" class="form-control" v-validate="'required'">
        <option>Female</option>
        <option>Male</option>
      </select>
      <span v-show="errors.has('gender')" class="text-danger">
        {{ errors.first('gender') }}
      </span>
    </div>
    <div>
      <label for="phone">Phone:</label>
      <input id="phone" name="phone" v-validate="'required'" type="text" v-model="user.phone" class="form-control" />
      <span v-show="errors.has('phone')" class="text-danger">
        {{ errors.first('phone') }}
      </span>
    </div>
    <div>
      <label for="email">Email:</label>
      <input id="email" name="email" v-validate="'required|email'" type="text" v-model="user.email" class="form-control" />
      <span v-show="errors.has('email')" class="text-danger">
        {{ errors.first('email') }}
      </span>
    </div>
    <div>
      <label for="password">Password:</label>
      <input id="password" name="password" v-validate="'required'" type="password" v-model="user.password" class="form-control" />
      <span v-show="errors.has('password')" class="text-danger">
        {{ errors.first('password') }}
      </span>
    </div>
    <div>
      <button class="btn btn-lg btn-primary btn-block" type="submit">Submit</button>
    </div>
  </form>
</div>
```

To ensure that the required fields are filled, we pass the value `required` to a `v-validate` attribute in our template. This signifies that a value must be provided for the input. We won’t do much more than that in our example, but please be aware that [VeeValidate comes with a bunch of validation rules out of the box](https://baianat.github.io/vee-validate/guide/rules.html), which are all localized and cover most validation needs. And if you don’t find what you’re looking for there, it’s possible to [create custom rules](https://baianat.github.io/vee-validate/guide/custom-rules.html#creating-a-custom-rule), too.

Once the form is submitted, we prevent the browser’s default submit action using the `.prevent` modifier. Then we call a custom `register` method. Any errors from the form will be in the `errors` object, and we can use one of the built-in helper methods to display each error for a particular field.

Next, let’s implement the form’s logic:

```
Vue.use(VeeValidate);

new Vue({
  el: '#app',
  data() {
    return {
      user: {
        email: '',
        password: '',
        name: '',
        phone: '',
        gender: ''
      }
    }
  },
  methods: {
    register() {
      this.$validator.validateAll().then((result) => {
        if (result) {
          alert('Form Submitted!');
          return;
        }

        alert('Form is invalid!');
      });
    }
  }
})
```

Within our `register` method, the `validateAll` method is used to validate each value against the corresponding field validations. We’re also displaying two different alerts depending on the validity of the form. In your application, you’ll want to replace the first alert with your POST request to the server.

And finally, the styles:

```
h2 {
  margin: 20px 0;
  text-align: center;
}
.form {
  max-width: 380px;
  padding: 15px 35px 45px;
  margin: 0 auto;
  background-color: #fff;
  border: 1px solid rgba(0,0,0,0.1);
}
label {
  margin: 12px 0 2px 0;
}
button {
  margin: 15px 0 0 0;
}
```

#### Live Code

![-](Images/forms5.png)

See the Pen [vue form - VeeValidate](https://codepen.io/SitePoint/pen/aPvzRB/).

## Conclusion

In this guide, I’ve demonstrated how easy it can be to work with forms in Vue. We looked at how to use two-way data binding to keep user input in sync with a data model, how to change the browser’s default form-handling behavior, and how to implement form validation using the [VeeValidate](https://baianat.github.io/vee-validate/) plugin.

At this point, you can go on to build simple to complicated forms in Vue, without the need to write long lines of code to handle validation.

# Chapter 6: How to Conditionally Apply a CSS Class in Vue.js

### by Chad Campbell

**There are times you need to change an element’s CSS classes at runtime. But when changing classes, it’s sometimes best to apply style details conditionally. For example, imagine your view has a pager. Pagers are often used to navigate larger sets of items. When navigating, it can be helpful to show the user the page they’re currently on. The style of the item is conditionally set, based on the current page that’s being viewed.**

A pager in this case may look something like this:

![Pager](Images/1501161191pager.png)

In this example, there are five pages. Only one of these pages is selected at a time. If you built this pager with Bootstrap, the selected page would have a CSS class named `active` applied. You’d want this class applied only if the page was the currently viewed page. In other words, you’d want to *conditionally* apply the `active` CSS class. Luckily, Vue provides a way to conditionally apply a CSS class to an element, which I’m going to demonstrate in this article.

To conditionally apply a CSS class at runtime, you can bind to a JavaScript object. To successfully complete this task, you must complete two steps. First, you must ensure that your CSS class is defined. Then, you create the class bindings in your template. I’m going to explain each of these steps in detail in the rest of this article.

## Step 1: Define Your CSS Classes

Imagine, for a moment, that the five page items shown in the image above were defined using the following HTML:

```
<div id="myApp">
  <nav aria-label="Page navigation example">
    <ul class="pagination">
      <li class="page-item"><a class="page-link" href="#">1</a></li>
      <li class="page-item"><a class="page-link" href="#">2</a></li>
      <li class="page-item active"><a class="page-link" href="#">3</a></li>
      <li class="page-item"><a class="page-link" href="#">4</a></li>
      <li class="page-item"><a class="page-link" href="#">5</a></li>
    </ul>
  </nav>
</div>
```

Notice that each page in this code snippet has a list-item element (`<li …`). That element references the `page-item` CSS class. In the code for this article, this class is defined in the Bootstrap CSS framework. However, if it weren’t defined there, it would be your responsibility to ensure that it was defined somewhere. The second CSS class is the one that’s most relevant to this article, though.

The `active` CSS class is used to identify the currently selected page. For this article, this CSS class is also defined in the Bootstrap CSS. As shown in the snippet above, the `active` class is only used in the *third* list item element. As you can probably guess, this is the CSS class that you want to apply conditionally. To do that, you need to add a JavaScript object.

## Step 2: Create Your Class Bindings

Let’s build on the code snippet shown in step 1\. When creating class bindings in your template, there are two primary choices: using the object syntax or using the array syntax. I’m going to show you how to use both approaches in the remainder of this article.

### Binding using object syntax

To create a class binding using the object syntax, you have to use a JavaScript **expression**. The expression we’ll be using can be seen in the code associated with this article [here](https://codepen.io/SitePoint/pen/RqbBdK). That relevant code looks like this:

```
<div id="myApp">
  <nav aria-label="An example with pagination">
    <ul class="pagination">
      <li v-for="page in totalPages" v-bind:class="{'page-item':true, 'active':(page === currentPage)}">
        <a class="page-link" href="#">{{ page }}</a>
      </li>
    </ul>
  </nav>
</div>
```

I’ve reduced the amount of code by using Vue’s baked-in `v-for` directive. This directive is used to render items in a loop. The items in this example are the pages themselves. Beyond the use of the `v-for` directive, notice the use of the `v-bind` directive.

The `v-bind` directive connects the element’s `class` attribute to the Vue instance. That instance of Vue is defined like this:

```
var app = new Vue({
  el: '#myApp',
  data: {
    totalPages: 5,
    currentPage: 3
  }
});
```

This Vue instance is straight to the point. The `data` object above includes a property named `currentPage`. If you revisit the HTML template defined above, you’ll notice that this property is being referenced. In fact, the JavaScript object associated with each class binding looks something like this:

```
{'page-item':true, 'active':(page === currentPage)}
```

This object defines two properties: `page-item` and `active`. Notably, these are the names of the two CSS classes discussed in Step 1\. In Step 2, these two class references have become property names in a JavaScript object. The values associated with these property names are JavaScript expressions. If the expression evaluates as truthy, the CSS class will be included. If the expression evaluates to `false`, the CSS class will *not* be included. With these rules in mind, let’s look at each property.

The first property, `page-item`, has a value of `true`. This hard-coded value is used because we always want to include the `page-item` class. The second property, `active`, uses a JavaScript expression. When this expression is `true`, the `active` class will be applied. This empowers us to conditionally apply the `active` class based on the value of `currentPage`. Another way to conditionally apply the `active` class is by binding to an `Array`.

### Binding using array syntax

Vue lets you apply a list of CSS classes by binding to an `Array`. If you wanted to use the `Array` syntax, the HTML shown in Step 1 would become this:

```
<div id="myApp">
  <nav aria-label="An example with pagination">
    <ul class="pagination">
        <li v-for="page in totalPages" v-bind:class="[pageItemClass, (page === currentPage) ? activeClass : '']">
          <a class="page-link" href="#">{{ page }}</a>
        </li>
    </ul>
  </nav>
</div>
```

A running version with the `Array` syntax can be seen [here](https://codepen.io/SitePoint/pen/dQbjxX). The only difference is the use of an `Array` on the class binding. This alternative approach expects two additional properties to exist in your Vue’s `data` object. Those two properties are: `pageItemClass` and `activeClass`. The updated Vue initialization code with these properties looks like this:

```
var app = new Vue({
  el: '#myApp',
  data: {
    totalPages: 5,
    currentPage: 3,
    pageItemClass: 'page-item',
    activeClass: 'active'
  }
});
```

As you can see, the `data` object has grown in size, but the code in the template is slightly cleaner when using the `Array` syntax. The object syntax is a little bit more compact. The choice between the object syntax and the `Array` syntax comes down to personal preference.

Both approaches may seem to make your HTML template more complicated. However, there’s actually more going on here. In reality, we’re separating concerns. We’re creating a template that is driven by data. This makes the view easier to test and easier to maintain as the app grows.

# Chapter 7: How to Replace jQuery with Vue

### by Nilson Jacques

**I’m willing to bet that there are a lot of developers out there who still reach for [jQuery](https://jquery.com/) when tasked with building simple apps. There are often times when we need to add some interactivity to a page, but reaching for a JavaScript framework seems like overkill — with all the extra kilobytes, the boilerplate, the build tools and module bundlers. Including jQuery from a CDN seems like a no-brainer.**

In this article, I’d like to take a shot at convincing you that using [Vue.js](https://vuejs.org/) (referred to as Vue from here on), even for relatively basic projects, doesn’t have to be a headache, and will help you write better code faster. We’ll take a simple example, code it up in jQuery, and then recreate it in Vue step by step.

## What We’re Building

For this article, we’re going to be building a basic online invoice, using this [open-source template from Sparksuite](https://github.com/sparksuite/simple-html-invoice-template). Hopefully, this should make a refreshing change from yet another to-do list, and provide enough complexity to demonstrate the advantages of using something like Vue while still being easy to follow.

![Screenshot of template](Images/1523363247sparksuite-template.png)

We’re going to make this interactive by providing item, unit price, and quantity inputs, and having the *Price* column automatically recalculated when one of the values changes. We’ll also add a button, to insert new empty rows into the invoice, and a *Total* field that will automatically update as we edit the data.

I’ve modified the template so that the HTML for a single (empty) row now looks like this:

```
<tr class="item">
  <td><input value="" /></td>
  <td>$<input type="number" value="0" /></td>
  <td><input type="number" value="1" /></td>
  <td>$0.00</td>
</tr>
```

## jQuery

So, first of all, let’s take a look at how we might do this with jQuery.

```
$('table').on('mouseup keyup', 'input[type=number]', calculateTotals);
```

We’re attaching a listener to the table itself, which will execute the `calculateTotals` function when either the *Unit Cost* or *Quantity* values are changed:

```
function calculateTotals()  {
  const subtotals = $('.item').map((idx, val)  => calculateSubtotal(val)).get();
  const total = subtotals.reduce((a, v)  => a + Number(v),  0);
  $('.total td:eq(1)').text(formatAsCurrency(total));
}
```

This function looks for all item rows in the table and loops over them, passing each row to a `calculateSubtotal` function, and then summing the results. This `total` is then inserted into the relevant spot on the invoice.

```
function calculateSubtotal(row) {
  const $row = $(row);
  const inputs = $row.find('input');
  const subtotal = inputs[1].value * inputs[2].value;

  $row.find('td:last').text(formatAsCurrency(subtotal));

  return subtotal;
}
```

In the code above, we’re grabbing a reference to all the `<input>`s in the row and multiplying the second and third together to get the subtotal. This value is then inserted into the last cell in the row.

```
function formatAsCurrency(amount) {
  return `$${Number(amount).toFixed(2)}`;
}
```

We’ve also got a little helper function that we use to make sure both the subtotals and the total are formatted to two decimal places and prefixed with a currency symbol.

```
$('.btn-add-row').on('click', () => {
  const $lastRow = $('.item:last');
  const $newRow = $lastRow.clone();

  $newRow.find('input').val('');
  $newRow.find('td:last').text('$0.00');
  $newRow.insertAfter($lastRow);

  $newRow.find('input:first').focus();
});
```

Lastly, we have a click handler for our *Add row* button. What we’re doing here is selecting the last item row and creating a duplicate. The inputs of the cloned row are set to default values, and it’s inserted as the new last row. We can also be nice to our users and set the focus to the first input, ready for them to start typing.

#### Live Code

See the Pen [jQuery Invoice](https://codepen.io/SitePoint/pen/YaBwJQ/).

### Downsides

So what’s wrong with this code as it stands, or rather, what could be better?

You may have heard some of these newer libraries, like Vue and React, claim to be declarative rather than imperative. Certainly looking at this jQuery code, the majority of it reads as a list of instructions on how to manipulate the DOM. The purpose of each section of code — the “what” — is often hard to make out through the details of “how” it’s being done. Sure, we can clarify the intent of the code by breaking it up into well-named functions, but this code is still going to take some effort to mentally parse if you come back to it after a while.

The other issue with code like this is that we’re keeping our application state in the DOM itself. Information about the items ordered exists only as part of the HTML making up the UI. This might not seem like a big problem when we’re only displaying the information in a single location, but as soon as we start needing to display the same data in multiple places in our app, it becomes increasingly complex to ensure that each piece is kept in sync. There’s no single source of truth.

Although nothing about jQuery prevents us from keeping our state outside the DOM and avoiding these problems, libraries such as Vue provide functionality and structure that facilitate creating a good architecture and writing cleaner, more modular code.

## Converting to Vue

So how would we go about recreating this functionality using Vue?

As I mentioned earlier, Vue doesn’t require us to use a module bundler, or a transpiler, or to opt in to their single file components (`.vue` files) in order to get started. Like jQuery, we can simply include the library from a CDN. Let’s start by swapping out the script tag:

```
<script src="https://cdn.jsdelivr.net/npm/vue@2.5.17/dist/vue.js"></script>
```

The next thing we need to do is create a new Vue instance:

```
const app = new Vue({
  el: 'table'
});
```

The only option we need to provide here is `el`, which is a selector (like we would use with jQuery) identifying which part of the document we want Vue to manage.

We can put Vue in charge of anything from the entire page (for a single page application, for example) or a single `<div>`. For our invoice example, we’ll give Vue control of the HTML table.

### Data

Let’s also add the data for the three example rows to our Vue instance:

```
const app = new Vue({
  el: 'table',
  data: {
    items: [
      { description: 'Website design', quantity: 1, price: 300 },
      { description: 'Hosting (3 months)', quantity: 1, price: 75 },
      { description: 'Domain name (1 year)', quantity: 1, price: 10 },
    ]
  }
});
```

The `data` property is where we store the state of our application. This includes not only any data we want our app to work with, but also information about the state of the UI (for example, which section is currently active in a tab group, or whether an accordion is expanded or contracted).

Vue encourages us to keep our app’s state separate from its presentation (that is, the DOM) and centralized in one place — a single source of truth.

### Modifying the template

Now let’s set up our template to display the items from our data object. As we’ve told Vue we want it to control the table, we can use its template syntax in the HTML to tell Vue how to render and manipulate it.

Using the `v-for` attribute, we can render a block of HTML for each item in our `items` array:

```
<tr class="item" v-for="item in items">

</tr>
```

Vue will repeat this markup for each element of the array (or object) that you pass to the `v-for` construct, allowing you to reference each element inside the loop — in this case, as `item`. As Vue is observing all the properties of the `data` object, it will dynamically re-render the markup as the contents of `items` change. All we have to do is add or remove items to our app state, and Vue takes care of updating the UI.

We’ll also need to add `<input>`s for the user to fill out the description, unit price, and quantity of the item:

```
<td><input v-model="item.description" /></td>
<td>$<input type="number" v-model="item.price" /></td>
<td><input type="number" v-model="item.quantity" /></td>
<td>${{ item.price * item.quantity }}</td>
```

Here we’re using the `v-model` attribute to set up a two-way binding between the inputs and properties on our data model. This means any change to the inputs will update the corresponding properties on the item model, and vice versa.

In the last cell, we’re using double curly braces `{{ }}` to output some text. We can use any valid JavaScript expression within the braces, so we’re multiplying two of our item properties together and outputting the result. Again, as Vue is observing our data model, a change to either property will cause the expression to be re-evaluated automatically.

### Events and methods

Now we have our template set up to render out our `items` collection, but how do we go about adding new rows? As Vue will render whatever is in `items`, to render an empty row we just need to push an object with whatever default values we want into the `items` array.

To create functions that we can access from within our template, we need to pass them to our Vue instance as properties of a `methods` object:

```
const app = new Vue({
  // ...
  methods: {
    myMethod() {}
  },
  // ...
})
```

Let’s define an `addRow` method that we can call to add a new item to our `items` array:

```
methods: {
  addRow() {
    this.items.push({ description: '', quantity: 1, price: 0 });
  },
},
```

Note that any methods we create are automatically bound to the Vue instance itself, so we can access properties from our `data` object, and other methods, as properties of `this`.

So, now that we have our method, how do we call it when the *Add row* button is clicked? The syntax for adding event listeners to an element in the template is `v-on:event-name`:

```
<button class="btn-add-row" @click="addRow">Add row</button>
```

Vue also provides a shortcut for us so we can use `@` in place of `v-on:`, as I’ve shown in the code above. For the handler, we can specify any method from our Vue instance.

### Computed properties

Now all we need to do is display the grand total at the bottom of the invoice. Potentially we could do this within the template itself: as I mentioned earlier, Vue allows us to put any JavaScript statement between curly brackets. However, it’s much better to keep anything more than very basic logic out of our templates; it’s cleaner and easier to test if we keep that logic separate.

We could use another method for this, but I think a [computed property](https://vuejs.org/v2/guide/computed.html#Computed-Properties) is a better fit. Similar to creating methods, we pass our Vue instance a `computed` object containing functions whose results we want to use in our template:

```
const app = new Vue({
  // ...
  computed: {
    total() {
      return this.items.reduce((acc, item) => acc + (item.price * item.quantity), 0);
    }
  }
});
```

Now we can reference this computed property within our template:

```
<tr class="total">
  <td colspan="3"></td>
  <td>Total: ${{ total }}</td>
</tr>
```

As you might already have noticed, computed properties can be treated as if they were data; we don’t have to call them with parentheses. But using computed properties has another benefit: Vue is smart enough to cache the returned value and only re-evaluate the function if one of the data properties it depends upon changes.

If we were using a method to sum up the grand total, the calculation would be performed each and every time the template was re-rendered. Because we’re using a computed property, the total is only recalculated if one of the item’s `quantity` or `price` fields are changed.

### Filters

You might have spotted we have a small bug in our implementation. While the unit costs are whole numbers, our total and subtotals are displayed without the cents. What we really want is for these figures to always be displayed to two decimal places.

Rather than modify both the code that calculates the subtotals and the code that calculates the grand total, Vue provides us with a nice way to deal with common formatting tasks like this: filters.

As you might have already guessed, to create a filter we just pass an object with that key to our Vue instance:

```
const app = new Vue({
  // ...
  filters: {
    currency(value) {
      return value.toFixed(2);
    }
  }
});
```

Here we’ve created a very simple filter called `currency`, which calls `toFixed(2)` on the value it receives and returns the result. We can apply it to any output in our template like so:

```
<td>Total: ${{ total | currency }}</td>
```

#### Live Code

See the Pen [Vue Invoice](https://codepen.io/SitePoint/pen/MVLVmv/).

## Summing Up

Comparing the two versions of the code side by side, a couple things stand out about the Vue app:

*   **The clear separation between the UI, and the logic/data that drives it**: the code is much easier to understand, and lends itself to easier testing
*   **The UI is declarative**: you only need concern yourself with what you want to see, not how to manipulate the DOM to achieve it.

The size (in KB) of both libraries is almost identical. Sure, you could slim down jQuery a bit with a custom build, but even with a relatively simple project such as our invoice example, I think the ease of development and the readability of the code justifies the difference.

Vue can also do a lot more than we’ve covered here. Its strength lies in allowing you to create modular, reusable UI components that can be composed into sophisticated front-end applications. If you’re interested in delving deeper into Vue, I’d recommend checking out [Getting Up and Running with the Vue.js 2.0 Framework](https://www.sitepoint.com/up-and-running-vue-js-2-0/).

# Chapter 8: Nuxt.js: a Minimalist Framework for Creating Universal Vue.js Apps

### by Olayinka Omole

**Universal (or Isomorphic) JavaScript is a term that has become very common in the JavaScript community. It’s used to describe JavaScript code that can execute both on the client and the server.**

Many modern JavaScript frameworks, like [Vue.js](https://vuejs.org/), are aimed at building single-page applications (SPAs). This is done to improve the user experience and make the app seem faster, since users can see updates to pages instantaneously. While this has a lot of advantages, it also has a couple of disadvantages, such as long “time to content” when initially loading the app as the browser retrieves the JavaScript bundle, and some search engine web crawlers or social network robots won’t see the entire loaded app when they crawl your web pages.

Server-side rendering of JavaScript is about preloading JavaScript applications on a web server and sending rendered HTML as the response to a browser request for a page.

Building server-side rendered JavaScript apps can be a bit tedious, as a lot of configuration needs to be done before you even start coding. This is the problem [Nuxt.js](https://nuxtjs.org) aims to solve for Vue.js applications.

## What Nuxt.js Is

Simply put, Nuxt.js is a framework that helps you build server-rendered Vue.js applications easily. It abstracts most of the complex configuration involved in managing things like asynchronous data, middleware, and routing. It’s similar to [Angular Universal](https://universal.angular.io/) for [Angular](https://angular.io/), and [Next.js](https://zeit.co/blog/next6) for [React](https://facebook.github.io/react/).

According to [the Nuxt.js docs](https://nuxtjs.org/guide), “its main scope is UI rendering while abstracting away the client/server distribution.”

### Static Generation

Another great feature of Nuxt.js is its ability to generate static websites with the `generate` command. It’s pretty cool, and provides features similar to popular static generation tools like [Jekyll](https://jekyllrb.com/).

### Under the Hood of Nuxt.js

In addition to Vue.js 2.0, Nuxt.js includes the following: [Vue-Router](https://github.com/vuejs/vue-router), [Vuex](https://github.com/vuejs/vuex) (only included when using the [store option](https://nuxtjs.org/guide/vuex-store)), [Vue Server Renderer](https://ssr.vuejs.org/) and [vue-meta](https://github.com/declandewet/vue-meta). This is great, as it takes away the burden of manually including and configuring different libraries needed for developing a server-rendered Vue.js application. Nuxt.js does all this out of the box, while still maintaining a total size of **57kB min+gzip** (60KB with vuex).

Nuxt.js also uses [webpack](https://github.com/webpack/webpack) with [vue-loader](https://github.com/vuejs/vue-loader) and [babel-loader](https://github.com/babel/babel-loader) to bundle, code-split and minify code.

### How it works

This is what happens when a user visits a Nuxt.js app or navigates to one of its pages via `<nuxt-link>`:

1.  When the user initially visits the app, if the [`nuxtServerInit` action](https://nuxtjs.org/guide/vuex-store/#the-nuxtserverinit-action) is defined in the store, Nuxt.js will call it and update the store.
2.  Next, it executes any existing [middleware](https://nuxtjs.org/guide/routing/#middleware) for the page being visited. Nuxt checks the `nuxt.config.js` file first for global middleware, then checks the matching [layout file](https://nuxtjs.org/guide/views#layouts) (for the requested page), and finally checks the page and its children for middleware. Middleware are prioritized in that order.
3.  If the route being visited is a dynamic route, and a `validate()` method exists for it, [the route is validated](https://nuxtjs.org/api/pages-validate).
4.  Then, Nuxt.js calls the `asyncData()` and `fetch()` methods to load data before rendering the page. The [`asyncData()` method](https://nuxtjs.org/guide/async-data/) is used for fetching data and rendering it on the server-side, while the [`fetch()` method](https://nuxtjs.org/api/pages-fetch/) is used to fill the store before rendering the page.
5.  At the final step, the page (containing all the proper data) is rendered.

These actions are portrayed properly in this schema, gotten from the Nuxt docs:

![Nuxt.js Schema](Images/1498691466nuxt-schema.png "Nuxt.js Schema")

## Creating A Serverless Static Site With Nuxt.js

Let’s get our hands dirty with some code and create a simple static generated blog with Nuxt.js. We’ll assume our posts are fetched from an API and will mock the response with a static JSON file.

To follow along properly, a working knowledge of Vue.js is needed. You can check out Jack Franklin’s great [getting started guide](https://www.sitepoint.com/up-and-running-vue-js-2-0/) for Vue.js 2.0 if you’re new to the framework. I’ll also be using ES6 Syntax, and you can get a refresher on that here: [sitepoint.com/tag/es6/](https://www.sitepoint.com/tag/es6/).

Our final app will look like this:

![Nuxt SSR Blog](Images/nuxt1.png "Nuxt SSR Blog")

#### Github

The entire code for this tutorial can be seen [here on GitHub](https://github.com/sitepoint-editors/nuxt-ssr-blog/), and you can check out the demo [here](https://nuxt-ssr-blog.firebaseapp.com/).

### Application Setup and Configuration

The easiest way to get started with Nuxt.js is to use the template created by the Nuxt team. We can install it to our project (`ssr-blog`) quickly using the [vue-cli](https://cli.vuejs.org/):

```
vue init nuxt/starter ssr-blog
```

Once you’ve run this command, a prompt will open and ask you a couple of questions. You can press `Return` to accept the default answers, or enter values of your own.

#### Install vue-cli

If you don’t have vue-cli installed, you have to run `npm install -g @vue/cli` first, to install it.

Next, we install the project’s dependencies:

```
cd ssr-blog
npm install
```

Now we can launch the app:

```
npm run dev
```

If all goes well, you should be able to visit [http://localhost:3000](http://localhost:3000) to see the Nuxt.js template starter page. You can even view the page’s source, to see that all content generated on the page was rendered on the server and sent as HTML to the browser.

Next, we can make some simple configurations in the `nuxt.config.js` file. We’ll add a few options:

```
// ./nuxt.config.js

module.exports = {
  /*
   * Headers of the page
   */
  head: {
    titleTemplate: '%s | Awesome JS SSR Blog',
    // ...
    link: [
      // ...
      {
        rel: 'stylesheet',
        href: 'https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.2/css/bulma.min.css'
      }
    ]
  },
  // ...
}
```

In the above config file, we simply specify the title template to be used for the application via the `titleTemplate` option. Setting the `title` option in the individual pages or layouts will inject the `title` value into the `%s` placeholder in `titleTemplate` before being rendered.

We also pulled in my current CSS framework of choice, [Bulma](http://bulma.io/), to take advantage of some preset styling. This was done via the `link` option.

#### Understanding the Headers

Nuxt.js uses [vue-meta](https://github.com/declandewet/vue-meta) to update the headers and HTML attributes of our apps. So you can take a look at it for a better understanding of how the headers are being set.

Now we can take the next couple of steps by adding our blog’s pages and functionalities.

### Working with Page Layouts

First, we’ll define a custom base layout for all our pages. We can extend the main Nuxt.js layout by updating the `layouts/default.vue` file:

```
<!-- ./layouts/default.vue -->

<template>
  <div>
    <!-- navigation -->
    <nav class="navbar has-shadow" role="navigation" aria-label="main navigation">
      <div class="container">
        <div class="navbar-start">
          <nuxt-link to="/" class="navbar-item">
            Awesome JS SSR Blog!
          </nuxt-link>
          <nuxt-link active-class="is-active" to="/" class="navbar-item is-tab" exact>Home</nuxt-link>
          <nuxt-link active-class="is-active" to="/about" class="navbar-item is-tab" exact>About</nuxt-link>
        </div>
      </div>
    </nav>
    <!-- /navigation -->

    <!-- displays the page component -->
    <nuxt/>

  </div>
</template>

<style>
  .main-content {
    margin: 30px 0;
  }
</style>
```

In our custom base layout, we add the site’s navigation header. We use the `<nuxt-link>` component to generate links to the routes we want to have on our blog. You can check out the [docs on `<nuxt-link>`](https://nuxtjs.org/api/components-nuxt-link) to see how it works.

The `<nuxt>` component is really important when creating a layout, as it displays the page component.

It’s also possible to do a couple of more things — like define custom document templates and error layouts — but we don’t need those for our simple blog. I urge you to check out the [Nuxt.js documentation on views](https://nuxtjs.org/guide/views) to see all the possibilities.

### Simple Pages and Routes

Pages in Nuxt.js are created as [single file components](https://vuejs.org/v2/guide/single-file-components.html) in the `pages` directory. Nuxt.js automatically transforms every `.vue` file in this directory into an application route.

### Building the Blog Homepage

We can add our blog homepage by updating the `index.vue` file generated by the Nuxt.js template in the pages directory:

```
<!-- ./pages/index.vue -->
<template>
  <div>
    <section class="hero is-medium is-primary is-bold">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            Welcome to the JavaScript SSR Blog.
          </h1>
          <h2 class="subtitle">
            Hope you find something you like.
          </h2>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    head: {
      title: 'Home'
    }
  }
</script>

<!-- Remove the CSS styles -->
```

As stated earlier, specifying the `title` option here automatically injects its value into the `titleTemplate` value before rendering the page.

We can now reload our app to see the changes to the homepage.

### Building the About page

Another great thing about Nuxt.js is that it will listen to file changes inside the `pages` directory, so there’s no need to restart the application when adding new pages.

We can test this, by adding a simple `about.vue` page:

```
<!-- ./pages/about.vue -->
<template>
  <div class="main-content">
    <div class="container">
      <h2 class="title is-2">About this website.</h2>
      <p>Curabitur accumsan turpis pharetra <strong>augue tincidunt</strong> blandit. Quisque condimentum maximus mi, sit amet commodo arcu rutrum id. Proin pretium urna vel cursus venenatis. Suspendisse potenti. Etiam mattis sem rhoncus lacus dapibus facilisis. Donec at dignissim dui. Ut et neque nisl.</p>
      <br>
      <h4 class="title is-4">What we hope to achieve:</h4>
      <ul>
        <li>In fermentum leo eu lectus mollis, quis dictum mi aliquet.</li>
        <li>Morbi eu nulla lobortis, lobortis est in, fringilla felis.</li>
        <li>Aliquam nec felis in sapien venenatis viverra fermentum nec lectus.</li>
        <li>Ut non enim metus.</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'About'
  }
}
</script>
```

Now, we can visit [http://localhost:3000/about](http://localhost:3000/about) to see the about page, without having to restart the app, which is awesome.

### Showing Blog Posts on the Homepage

Our current homepage is pretty bare as it is, so we can make it better by showing the recent blog posts from the blog. We’ll do this by creating a `<posts>` component and displaying it in the `index.vue` page.

But first, we have to get our saved JSON blog posts and place them in a file in the app root folder. [The file can be downloaded from here](https://github.com/sitepoint-editors/nuxt-ssr-blog/blob/master/posts.json), or you can just copy the JSON below and save in the root folder as `posts.json`:

```
[
    {
        "id": 4,
        "title": "Building universal JS apps with Nuxt.js",
        "summary": "Get introduced to Nuxt.js, and build great SSR Apps with Vue.js.",
        "content": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>",
        "author": "Jane Doe",
        "published": "08:00 - 07/06/2017"
    },
    {
        "id": 3,
        "title": "Great SSR Use cases",
        "summary": "See simple and rich server-rendered JavaScript apps.",
        "content": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>",
        "author": "Jane Doe",
        "published": "17:00 - 06/06/2017"
    },
    {
        "id": 2,
        "title": "SSR in Vue.js",
        "summary": "Learn about SSR in Vue.js, and where Nuxt.js can make it all faster.",
        "content": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>",
        "author": "Jane Doe",
        "published": "13:00 - 06/06/2017"
    },
    {
        "id": 1,
        "title": "Introduction to SSR",
        "summary": "Learn about SSR in JavaScript and how it can be super cool.",
        "content": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>",
        "author": "John Doe",
        "published": "11:00 - 06/06/2017"
    }
]
```

#### Where to Retreive the Content

Ideally the posts should be retrieved from an API or resource. For example, [Contentful](https://www.contentful.com/) is a service that can be used for this.

Components live in the `components` directory. We’ll create the `<posts>` single file component in there:

```
<!-- ./components/Posts.vue -->
<template>
  <section class="main-content">
    <div class="container">
      <h1 class="title has-text-centered">
        Recent Posts.
      </h1>
      <div class="columns is-multiline">
        <div class="column is-half" v-for="post in posts" :key="post.id">
          <div class="card">
           <header class="card-header">
            <p class="card-header-title">
              {{ post.title }}
            </p>
          </header>
          <div class="card-content">
            <div class="content">
              {{ post.summary }}
              <br>
              <small>
                by <strong>{{ post.author}}</strong>
                \\ {{ post.published }}
              </small>
            </div>
          </div>
          <footer class="card-footer">
            <nuxt-link :to="`/post/${post.id}`"
              class="card-footer-item">
              Read More
            </nuxt-link>
          </footer>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<script>
  import posts from '~/posts.json'

  export default {
    name: 'posts',
    data () {
      return { posts }
    }
  }
</script>
```

We import the posts data from the saved JSON file and assign it to the `posts` value in our component. We then loop through all the posts in the component template with the `v-for` directive and display the post attributes we want.

#### The `~` Symbol

The `~` symbol is an alias for the `/` directory. You can check out the docs [here](https://nuxtjs.org/guide/directory-structure/#aliases) to see the different aliases Nuxt.js provides, and what directories they’re linked to.

Next, we add the `<posts>` component to the homepage:

```
<!-- ./pages/index.vue -->
<template>
<div>
    <!-- ... -->
    <posts />
</div>
</template>

<script>
import Posts from '~/components/Posts.vue'

export default {
  components: {
    Posts
  },
  // ...
}
</script>
```

### Adding Dynamic Routes

Now we’ll add dynamic routes for the posts, so we can access a post for example with this URL: `/post/1`.

To achieve this, we add the `post` directory to the `pages` directory and structure it like this:

```
pages
└── post
    └── _id
        └── index.vue
```

This generates the corresponding dynamic routes for the application like this:

```
router: {
  routes: [
    // ...
    {
      name: 'post-id',
      path: '/post/:id',
      component: 'pages/post/_id/index.vue'
    }
  ]
}
```

Updating the single post file:

```
<!-- ./pages/post/_id/index.vue -->
<template>
  <div class="main-content">
    <div class="container">
      <h2 class="title is-2">{{ post.title }}</h2>
      <div v-html="post.content"></div>
      <br>
      <h4 class="title is-5 is-marginless">by <strong>{{ post.author }}</strong> at <strong>{{ post.published }}</strong></h4>
    </div>
  </div>
</template>

<script>
  // import posts saved JSON data
  import posts from '~/posts.json'

  export default {
    validate ({ params }) {
      return /^\d+$/.test(params.id)
    },
    asyncData ({ params }, callback) {
      let post = posts.find(post => post.id === parseInt(params.id))
      if (post) {
        callback(null, { post })
      } else {
        callback({ statusCode: 404, message: 'Post not found' })
      }
    },
    head () {
      return {
        title: this.post.title,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: this.post.summary
          }
        ]
      }
    }
  }
</script>
```

Nuxt.js adds some custom methods to our page components to help make the development process easier. See how we use some of them on the single post page:

*   Validate the route parameter with the `validate` method. Our validate method checks if the route parameter passed is a number. If it returns `false`, Nuxt.js will automatically load the 404 error page. You can read more on it [here](https://nuxtjs.org/api/pages-validate).
*   The `asyncData` method is used to fetch data and render it on the server side before sending a response to the browser. It can return data via different methods. In our case, we use a callback function to return the post that has the same `id` attribute as the route `id` parameter. You can see the various ways of using this function [here](https://nuxtjs.org/guide/async-data).
*   As we’ve seen before, we use the `head` method to set the page’s headers. In this case, we’re changing the page title to the title of the post, and adding the post summary as a meta description for the page.

Great, now we can visit our blog again to see all routes and pages working properly, and also view the page source to see the HTML being generated. We have a functional server-rendered JavaScript application.

### Generating Static Files

Next, we can generate the static HTML files for our pages.

We’ll need to make a minor tweak though, as by default Nuxt.js ignores dynamic routes. To generate the static files for dynamic routes, we need to specify them explicitly in the `./nuxt.config.js` file.

We’ll use a callback function to return the list of our dynamic routes:

```
// ./nuxt.config.js

module.exports = {
  // ...
  generate: {
    routes(callback) {
      const posts = require('./posts.json')
      let routes = posts.map(post => `/post/${post.id}`)
      callback(null, routes)
    }
  }
}
```

You can check [here](https://nuxtjs.org/api/configuration-generate/) for the full documentation on using the `generate` property.

To generate all the routes, we can now run this command:

```
npm run generate
```

Nuxt saves all generated static files to a `dist` folder.

### Deployment on Firebase Hosting

As a final step, we can take advantage of [hosting by Firebase](https://firebase.google.com/products/hosting/) to make our static website live in a couple of minutes. This step assumes that you have a Google account.

First, install the Firebase CLI, if you don’t already have it:

```
npm install -g firebase-tools
```

To connect your local machine to your Firebase account and obtain access to your Firebase projects, run the following command:

```
firebase login
```

This should open a browser window and prompt you to sign in. Once you’re signed in, visit [https://console.firebase.google.com](https://console.firebase.google.com) and click *Add project*. Make the relevant choices in the wizard that opens.

Once the project is created, go to the project’s hosting page at `https://console.firebase.google.com/project/<project name>/hosting` and complete the *Get started* wizard.

Then, on your PC, from the root of your project directory, run the following command:

```
firebase init
```

In the wizard that appears, select “Hosting”. Then select your newly created project from the list of options. Next choose the `dist` directory as the public directory. Select to configure the page as a single-page app and finally select “No” when asked if you want to overwrite `dist/index.html`.

Firebase will write a couple of configuration files to your project, then put the website live at `https://<project name>.firebaseapp.com`. The demo app for this article can be seen at [nuxt-ssr-blog.firebaseapp.com](https://nuxt-ssr-blog.firebaseapp.com/).

If you run into problems, you can find full instructions on [Firebase’s quickstart page](https://firebase.google.com/docs/hosting/quickstart).

## Conclusion

In this article, we’ve learned how we can take advantage of Nuxt.js to build server-rendered JavaScript applications with Vue.js. We also learned how to use its `generate` command to generate static files for our pages, and deploy them quickly via a service like Firebase Hosting.

The Nuxt.js framework is really great. It’s even [recommended in the official Vue.js SSR GitBook](https://ssr.vuejs.org/en/#about-this-guide). I really look forward to using it in more SSR projects and exploring all of its capabilities.

# Chapter 9: Optimize the Performance of a Vue App with Async Components

### by Michiel Mulders

**Single-page applications sometimes cop a little flack for their slow initial load. This is because traditionally, the server will send a large bundle of JavaScript to the client, which must be downloaded and parsed before anything is displayed on the screen. As you can imagine, as your app grows in size, this can become more and more problematic.**

Luckily, when building a Vue application using Vue CLI (which uses webpack under the hood), there are a number of measures one can take to counteract this. In this article, I’ll demonstrate how make use of both asynchronous components and webpack’s code-splitting functionality to load in parts of the page after the app’s initial render. This will keep the initial load time to a minimum and give your app a snappier feel.

To follow this tutorial, you need a basic understanding of Vue.js and optionally Node.js.

## Async Components

Before we dive into creating asynchronous components, let’s take a look at how we normally load a component. To do so, we’ll use a very simple message component:

```
<!-- Message.vue -->
<template>
  <h1>New message!</h1>
</template>
```

Now that we’ve created our component, let’s load it into our `App.vue` file and display it. We can just import the component and add it to the components option so we can use it in our template:

```
<!-- App.vue -->
<template>
  <div>
    <message></message>
  </div>
</template>

<script>
import Message from "./Message";
export default {
  components: {
    Message
  }
};
</script>
```

But what happens now? The `Message` component will be loaded whenever the application is loaded, so it’s included in the initial load.

This might not sound like a huge problem for a simple app, but consider something more complex like a web store. Imagine that a user adds items to a basket, then wants to check out, so clicks the checkout button which renders a box with all details of the selected items. Using the above method, this checkout box will be included in the initial bundle, although we only need the component when the user clicks the checkout button. It’s even possible that the user navigates through the website without ever clicking the checkout button, meaning that it doesn’t make sense to waste resources on loading this potentially unused component.

To improve the efficiency of the application, we can combine both lazy loading and code splitting techniques.

Lazy loading is all about delaying the initial load of a component. You can see lazy loading in action on sites like medium.com, where the images are loaded in just before they’re required. This is useful, as we don’t have to waste resources loading all the images for a particular post up front, as the reader might skip the article halfway down.

The code splitting feature webpack provides allows you to split your code into various bundles that can then be loaded on demand or in parallel at a later point in time. It can be used to load specific pieces of code only when they’re required or used.

## Dynamic Imports

Luckily, Vue caters for this scenario using something called **dynamic imports**. This feature introduces a new function-like form of import that will return a Promise containing the requested (Vue) component. As the import is a function receiving a string, we can do powerful things like loading modules using expressions. Dynamic imports have been available in Chrome since version 61\. More information about them can be found on the [Google Developers website](https://developers.google.com/web/updates/2017/11/dynamic-import).

The code splitting is taken care of by bundlers like webpack, Rollup or Parcel, which understand the dynamic import syntax and create a separate file for each dynamically imported module. We’ll see this later on in our console’s network tab. But first, let’s take a look at the difference between a static and dynamic import:

```
// static import
import Message from "./Message";

// dynamic import
import("./Message").then(Message => {
  // Message module is available here...
});
```

Now, let’s apply this knowledge to our `Message` component, and we’ll get an `App.vue` component that looks like this:

```
<!-- App.vue -->
<template>
  <div>
    <message></message>
  </div>
</template>

<script>
import Message from "./Message";
export default {
  components: {
    Message: () => import("./Message")
  }
};
</script>
```

As you can see, the `import()` function will resolve a Promise that returns the component, meaning that we’ve successfully loaded our component asynchronously. If you take a look in your devtools’ network tab, you’ll notice a file called `0.js` that contains your asynchronous component.

![Code splitting webpack](Images/15431553231-network-tab-output.png "Async Component Code Splitting")

## Conditionally Loading Async Components

Now that we have a handle on asynchronous components, let’s truly harvest their power by only loading them when they’re really needed. In the previous section of this article, I explained the use case of a checkout box that’s only loaded when the user hits the checkout button. Let’s build that out.

### Project Setup

If you don’t have Vue CLI installed, you should grab that now:

```
npm i -g @vue/cli
```

Next, use the CLI to create a new project, selecting the default preset when prompted:

```
vue create my-store
```

Change into the project directory, then install the [ant-design-vue](https://www.npmjs.com/package/ant-design-vue) library, which we’ll be using for styling:

```
cd my-store
npm i ant-design-vue
```

Next, import the Ant Design library in `src/main.js`:

```
import 'ant-design-vue/dist/antd.css'
```

Finally, create two new components in `src/comonents`, `Checkout.vue` and `Items.vue`:

```
touch src/components/{Checkout.vue,Items.vue}
```

### Making the Store View

Open up `src/App.vue` and replace the code there with the following:

```
<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <items></items>
  </div>
</template>

<script>
import items from "./components/Items"

export default {
  components: {
    items
  },
  name: 'app',
  data () {
    return {
      msg: 'My Fancy T-Shirt Store'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
```

There’s nothing fancy going on here. All we’re doing is displaying a message and rendering an `<items>` component.

Next, open up `src/components/Items.vue` and add the following code:

```
<template>
  <div>
    <div style="padding: 20px;">
      <Row :gutter="16">
        <Col :span="24" style="padding:5px">
          <Icon type="shopping-cart" style="margin-right:5px"/>{{shoppingList.length}} item(s)
          <Button @click="show = true" id="checkout">Checkout</Button>
        </Col>
      </Row>
    </div>
    <div v-if="show">
      <Row :gutter="16" style="margin:0 400px 50px 400px">
        <checkout v-bind:shoppingList="shoppingList"></checkout>
      </Row>
    </div>
    <div style="background-color: #ececec; padding: 20px;">
      <Row :gutter="16">
        <Col :span="6" v-for="(item, key) in items" v-bind:key="key" style="padding:5px">
          <Card v-bind:title="item.msg" v-bind:key="key">
            <Button type="primary" @click="addItem(key)">Buy ${{item.price}}</Button>
          </Card>
        </Col>
      </Row>
    </div>
  </div>
</template>

<script>
import { Card, Col, Row, Button, Icon } from 'ant-design-vue';

export default {
  methods: {
    addItem (key) {
      if(!this.shoppingList.includes(key)) {
        this.shoppingList.push(key);
      }
    }
  },
  components: {
    Card, Col, Row, Button, Icon,
    checkout: () => import('./Checkout')
  },
  data: () => ({
    items: [
      { msg: 'First Product', price: 9.99 },
      { msg: 'Second Product', price: 19.99 },
      { msg: 'Third Product', price: 15.00 },
      { msg: 'Fancy Shirt', price: 137.00 },
      { msg: 'More Fancy', price: 109.99 },
      { msg: 'Extreme', price: 3.00 },
      { msg: 'Super Shirt', price: 109.99 },
      { msg: 'Epic Shirt', price: 3.00 },
    ],
    shoppingList: [],
    show: false
  })
}
</script>
<style>
#checkout {
  background-color:#e55242;
  color:white;
  margin-left: 10px;
}
</style>
```

In this file, we’re displaying a shopping cart icon with the current amount of purchased items. The items themselves are pulled from an `items` array, declared as a data property. If you click on an item’s *Buy* button, the `addItem` method is called, which will push the item in question to a `shoppingList` array. In turn, this will increment the cart’s total.

We’ve also added a *Checkout* button to the page, and this is where things start to get interesting:

```
<Button @click="show = true" id="checkout">Checkout</Button>
```

When a user clicks on this button, we’re setting a parameter `show` to be `true`. This `true` value is very important for the purpose of conditionally loading our async component.

A few lines below, you can find a `v-if` statement, which only displays the content of the `<div>` when `show` is set to `true`. This `<div>` tag contains the checkout component, which we only want to load when the user has hit the checkout button.

The checkout component is loaded asynchronously in the `components` option in the `<script>` section. The cool thing here is that we can even pass arguments to the component via the `v-bind` statement. As you can see, it’s relatively easy to create conditional asynchronous components:

```
<div v-if="show">
  <checkout v-bind:shoppingList="shoppingList"></checkout>
</div>
```

Let’s quickly add the code for the `Checkout` component in `src/components/Checkout.vue`:

```
<template>
  <Card title="Checkout Items" key="checkout">
    <p v-for="(k, i) in this.shoppingList" :key="i">
      Item: {{items[Number(k)].msg}} for ${{items[Number(k)].price}}
    </p>
  </Card>
</template>

<script>
import { Card } from 'ant-design-vue';

export default {
  props: ['shoppingList'],
  components: {
    Card
  },
  data: () => ({
    items: [
      { msg: 'First Product', price: 9.99 },
      { msg: 'Second Product', price: 19.99 },
      { msg: 'Third Product', price: 15.00 },
      { msg: 'Fancy Shirt', price: 137.00 },
      { msg: 'More Fancy', price: 109.99 },
      { msg: 'Extreme', price: 3.00 },
      { msg: 'Super Shirt', price: 109.99 },
      { msg: 'Epic Shirt', price: 3.00 },
    ]
  })
}
</script>
```

Here we’re looping over the props we receive as `shoppingList` and outputting them to the screen.

You can run the app using the `npm run serve` command. Then navigate to [http://localhost:8080/](http://localhost:8080/). If all has gone according to plan, you should see something like what’s shown in the image below.

![Vue Webshop Demo](Images/15431556012-Webshop-example.png "Vue.js Webshop example")

Try clicking around the store with your network tab open to assure yourself that the `Checkout` component is only loaded when you click the *Checkout* button.

You can also find [the code for this demo on GitHub](https://github.com/sitepoint-editors/shopping-cart-async).

## Async with Loading and Error Component

It’s even possible to define a loading and/or error component for when the async component takes some time to load or fails to load. It can be useful to show a loading animation, but bear in mind this again slows down your application. An asynchronous component should be small and fast to load. Here’s an example:

```
const Message = () => ({
  component: import("./Message"),
  loading: LoadingAnimation,
  error: ErrorComponent
});
```

## Conclusion

Creating and implementing asynchronous components is very easy and should be part of your standard development routine. From a UX perspective, it’s important to reduce the initial load time as much as possible to maintain the user’s attention. Hopefully this tutorial has assisted you with loading your own components asynchronously and applying conditions to them to delay (lazy load) the load of the component.