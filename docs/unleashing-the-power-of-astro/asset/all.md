![](Images/astro1.jpg)

## Unleashing the Power of Astro

Copyright © 2024 SitePoint Pty. Ltd.

Ebook ISBN: 978-1-925836-60-8

*   **Author:** Tamas Piros
*   **Cover Design:** Volodymyr Boyarinov
*   **Technical editor:** Joan León
*   **Series editor:** Oliver Lindberg

## Notice of Rights

All rights reserved. No part of this book may be reproduced, stored in a retrieval system or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical articles or reviews.

## Notice of Liability

The author and publisher have made every effort to ensure the accuracy of the information herein. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors and SitePoint Pty. Ltd., nor its dealers or distributors will be held liable for any damages to be caused either directly or indirectly by the instructions contained in this book, or by the software or hardware products described herein.

## Trademark Notice

Rather than indicating every occurrence of a trademarked name as such, this book uses the names only in an editorial fashion and to the benefit of the trademark owner with no intention of infringement of the trademark.

![SitePoint logo](Images/sitepoint-logo-2012.png)
Published by SitePoint Pty. Ltd.

71 Balmain Street, Cremorne, VIC, 3121
Australia
Web: www.sitepoint.com
Email: books@sitepoint.com

## About SitePoint

SitePoint specializes in publishing fun, practical, and easy-to-understand content for web professionals. Visit [http://www.sitepoint.com/](http://www.sitepoint.com/) to access our blogs, books, newsletters, articles, and community forums. You’ll find a stack of information on JavaScript, PHP, design, and more.

## About the Author

Tamas is a Google Developer Expert in Web Technologies and a seasoned Developer Evangelist. He is a passionate advocate for modern web technologies, helping people understand and unlock the latest & greatest features of web development.

# Preface

## Who Should Read This Book?

This book is for developers who are interested in learning to use Astro to build websites. It assumes familiarity with JavaScript, HTML, and CSS. Some familiarity with other front-end frameworks will be beneficial but is not required.

## Conventions Used

### Code Samples

Code in this book is displayed using a fixed-width font, like so:

```
 <h1>A Perfect Summer's Day</h1>
<p>It was a lovely day for a walk in the park.
The birds were singing and the kids were all back at school.</p> 
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

## Supplementary Materials

*   [https://www.sitepoint.com/community/](https://www.sitepoint.com/community/) are SitePoint’s forums, for help on any tricky problems.
*   **books@sitepoint.com** is our email address, should you need to contact us to report a problem, or for any other reason.

# Chapter 1: Getting Started with the Basics of Astro

[Astro](https://astro.build) is a modern static site generator that allows developers to build fast, optimized websites—a critical requirement in today’s rapidly evolving ecosystem, where user demands are high. Astro’s story goes back to 2021, when Fred K. Schott released the first version of the framework. At the time of writing this tutorial, Astro is already at version 4 and has seen many amazing features added to it.

Astro has [gained popularity](https://2022.stateofjs.com/en-US/libraries/rendering-frameworks/) over its brief existence, due to:

*   its innovative approach to creating websites, which emphasizes performance
*   its smooth developer experience
*   its ability to blend various other frameworks seamlessly

Due in part to a [new monthly sponsorship from Vercel](https://astro.build/blog/vercel-official-hosting-partner/), and because it’s the first framework to [implement the View Transitions API](https://thenewstack.io/dev-news-astro-3-0-state-of-css-and-react-opinions/), Astro is a force to be reckoned with.

This tutorial is the first in a series that will introduce Astro and walk through some its basics—such as rendering, content collections, data fetching, and image optimization.

## Key Concepts of Astro

How can one framework stand out in terms of performance? Let’s start by discussing one of the key concepts of Astro, called Astro Islands (or Component Islands). To better understand this web architecture style, let’s take a step back and discuss purely component-based development. If you’ve worked with React, Vue or Angular before, you likely have created components. **Components** encapsulate functionality: a React application is just a set of components put together in a logical way. My favorite analogy is that components are like Lego blocks: we use them to build our project.

There’s a striking problem with how components work under the hood in frameworks such as React and Angular. Usually, when a project is created, some components don’t necessarily require JavaScript, as the component isn’t interactive. For example, think about a navigation bar. Built out as a component, it may contain little apart from text, HTML and some styling. However, due to the nature of a framework such as React, we must load all the JavaScript. Otherwise, the component will fail to function.

When speaking of an Astro **island**, we refer to an interactive piece of UI element—“interactive” in the sense that it requires some JavaScript code to be run in order for it to be fully functional. Still, at the same time, Astro can also work with static (that is, non-interactive) components. Returning to our previous example, we could have a non-interactive navbar requiring zero bytes of JavaScript, while at the same time another interactive component loads some JavaScript.

![Astro islands in a typical web page](Images/1_1.png)

This architectural pattern technique may also be called partial or selective **hydration**, which pertains to optimizing how web apps load and render content. Both of these techniques involve the deliberate loading and rendering of only essential parts, deferring less critical components until they’re needed by the app. The main purpose of this is to strike a balance between providing a speedy initial page load and allowing for a responsive user experience.

To sum up, Astro uses interactive and non-interactive components to create a site. This approach means that much less JavaScript is loaded, and only when it’s needed.

Astro’s default behavior is to ship zero client-side JavaScript. That doesn’t mean we can’t use JavaScript in an Astro project. Far from it. But its island architecture means that client-side JavaScript will only be loaded where necessary.

## Getting Started with Astro

What better way to explore Astro than to create a project? And it couldn’t be easier: all we need to do is execute `npm create astro@latest`, which will allow the creation of a brand new project.

#### npm

The command above refers to npm, the Node Package Manager. Make sure you have an up-to-date version of Node.js and npm on your computer before working with Astro. Check out this [comprehensive tutorial on installing and working with npm](https://www.sitepoint.com/npm-guide/) if you need help with this.

The above command will ask multiple questions, such as the project’s location and how to start a project. This includes a choice of sample templates such as “blog”. For the purposes of this tutorial, just choose an empty project.

#### Starter Templates

Astro offers a wide range of [starter templates](https://docs.astro.build/en/install/auto/#starter-templates), which you may like to check out, as well as an extensive range of [themes](https://astro.build/themes/).

The next step in the process is to make sure that the dependencies are installed. Astro also supports TypeScript by default, and the installer will prompt us to select whether we plan to write TypeScript or just JavaScript.

Let’s next look at some of the key folders and files. The good news is that there’s only a small number of these within an empty project installation.

## Project Structure

The `src` folder is where the entire application will be built. By default, the `src` folder contains a `pages` folder and an `env.d.ts` file. As stated earlier, Astro has TypeScript support out of the box, and the `env.d.ts` file has a [triple slash directive](https://www.typescriptlang.org/docs/handbook/triple-slash-directives.html) that points to the appropriate Astro typings.

Astro uses file system-based routing. This essentially means that every folder and file placed in the `pages` folder will act as a route. Therefore, adding `about.astro` to `src/pages` will create the `/about` page. Adding a new `countries` folder, along with a `singapore.astro` file, will create the route `/countries/singapore`—and so on.

What’s really amazing about Astro is that linking between these pages doesn’t require a third-party dependency or a dedicated component. Instead, a standard `<a href="/about">` element can be used.

#### File Extensions

We don’t need to use the `.astro` extension. Astro can also use `.md`, `.mdx`, and `.html` extensions, as well as `.js` and `.ts` (for API endpoints, but more on this later). For this tutorial, we’ll stick to creating `.astro` files and components.

The last file that needs mentioning is `astro.config.mjs`, where we can specify some of Astro’s behavior or add plugins. We’ll return to this file later in the series and explore some of the options available.

It’s also important to discuss some naming conventions Astro suggests. Some of these are just suggestions. However, Astro reserves some folder names. Similarly to building a project with React, an Astro project comprises multiple components (either `.astro` or others). Therefore, it makes sense to store these in a centralized location. Astro’s documentation suggests storing these in `src/components`.

In the following chapter, we’ll talk about layouts in Astro, which can be used to define the UI structure of the entire application. Astro again suggests using `src/layouts` for files related to UI structures.

Styling is an important part of modern web applications, and `src/styles` could be used to store CSS or even Sass files.

The `public` folder can store assets such as images and fonts.

Last but not least, apart from `src/pages`, the other folder name that’s reserved by Astro is `src/content`. This location is to be used by content collections, which we’ll explore later.

Now that we’ve discussed the folder structure, let’s also discuss what files go into some folders. We’ll start by looking at how an Astro file is constructed. (An Astro file has a `.astro` extension, referring to an “Astro component”.)

## Anatomy of an Astro File

An `.astro` component has two parts: a script and a template. The component script usually goes on top, and it’s separated by what’s called a **code fence**—three dashed lines at the top and the bottom of the “script” section: `---`. (If you’ve used `frontmatter` in Markdown, the syntax is exactly the same.)

The component script is basically JavaScript code executed using a Node.js runtime during build time. Typically, we can import other components in here (either other Astro components or React components as well!), do data imports, execute Fetch API requests, create variables that would be used in the template, and even safely use API keys or write to a database. The key thing to understand here is that the JavaScript (or TypeScript) code written in this part of an Astro component will never make it to the client.

Any variable created in the script section can be referenced in the template section by using curly braces. (We’ll see an example of this later.)

The second part of an Astro component is the **template**. This is where the HTML tags should be added, and based on this, Astro will generate its final output during the build process. Apart from standard HTML elements, in this part of the template we can use JavaScript expressions, Astro components (or components from any other [supported framework](https://docs.astro.build/en/guides/integrations-guide/#official-integrations)), and special Astro directives. The template can also naturally accept a `<script>` element if client-side JavaScript is required.

This is how a sample `.astro` file might look, showing both the script and the HTML template parts:

```
---
const name = 'Jack'
---
<h1>Hello there, {name}</h1>
```

#### Placing JavaScript

By default, any JavaScript added to the `<script>` element will be bundled and added to the `<head>` of the statically generated page using the `type="module"` attribute. Add `<script is:inline>` if you want your JavaScript to be inline instead. See the next section for more details.

## Client-side JavaScript vs Build-time JavaScript

Let’s check quickly to ensure we understand the concept of JavaScript added in the script part of an Astro component versus adding JavaScript in a `<script>` element in the template.

Here’s one option:

```
---
const copyrightYear = new Date().getFullYear();
---
<small>Copyright, {copyrightYear}</small>
```

Here’s another option:

```
<small>Copyright</small>
<script>
document.querySelector('small').insertAdjacentText('beforeend',` ${new Date().getFullYear()}`);
</script>
```

Which option would we use to display the copyright year in Astro? Both of them work (seemingly) correctly, and both of them will display the current year.

However, there’s a crucial difference. Imagine we end up using the first solution and build our project on December 29, 2024 and deploy it. Then we don’t do another build for two years. Opening the page will still display 2024 once that year has expired. Why? Because the JavaScript code placed between the code fence (`---`) executes during build time. The second solution, however, will always display the correct year, as that code executes at the request time. That is, every time someone views the page, that piece of JavaScript code will run.

## Styling an Astro Component

Now that we have a good idea of what an Astro component looks like, let’s also discuss styling these components. Astro, out of the box, supports CSS, Sass and Less. Similar to how adding a `<script>` element is possible in a component, adding a `<style>` element is also possible. And the good news? CSS rules are scoped by default to the component where they’re defined. This means that the styles defined at the individual page or component level don’t pollute the rest of the application and the CSS rules will only apply to the necessary pages/components. That said, global styles can also be created by adding the `is:global` attribute to the `<style>` element.

Take this example:

```
<style is:global>
p {
  font-weight: bold;
}
</style>
```

In the code sample above, all paragraphs will be bold in the *entire* project because of the `is:global` directive.

These two approaches can also be combined by using the `<style>` element and the `:global()` CSS selector.

Furthermore, CSS variables can be used from the script part of an Astro component by utilizing the `define:vars` attribute on the `<style>` element:

```
---
const important = `#f00`;
---
<style define:vars={{ important }}>
p {
  color: var(--important);
}
</style>
<p>Important message</p>
```

In the code above, we’re defining a variable in JavaScript (`important`) and then reusing it as a CSS variable within the Astro template by way of the `define:vars` directive on the `<style>` element.

Lastly, if we have external stylesheets and we’ve placed them in our `public` folder, we can easily import them from within the component using the standard ESM `import` syntax:

```
---
import '../path/to/style.css'
---
<p>some html...</p>
```

Let’s also talk about Astro in the context of a larger ecosystem. Astro integrates with tools such as [Tailwind](https://tailwindcss.com) (a utility-first CSS framework) and [Partytown](https://partytown.builder.io) (a library designed to assist moving resource intensive scripts—such as third-party scripts—to a web worker, therefore relieving the main thread to process app specific JavaScript instead).

#### Custom Integrations

It’s worth noting that we can build a custom integration as well via Astro’s [Integrations API](https://docs.astro.build/en/reference/integrations-reference/).

The easiest way to use Tailwind (and other officially supported integrations) is by using the `npx astro add [integration]` command: `npx astro add tailwind`. This command automatically installs a compatible version of Tailwind, generates a custom `tailwind.config.cjs` file, and updates the `astro.config.mjs` to look like this, making it really easy to add Tailwind to a project:

```
import { defineConfig } from 'astro/config';

import tailwind from "@astrojs/tailwind";

// https://astro.build/config
export default defineConfig({
  integrations: [tailwind()]
});
```

## Demo

Throughout this book, we’ll be referencing a sample app, which you can also take a look at by visiting [stackblitz.com](https://stackblitz.com/github/tpiros/sitepoint-astro). For the purposes of consolidating what you’ve learned in this first chapter, it would be good to review the file and folder structure as well as the Tailwind setup in this demo.

## Conclusion

In this chapter, we got an introduction to Astro, a modern frontend framework. Astro’s rising popularity is attributed to its innovative approach to web development, prioritizing performance, seamless developer experience, and the ability to integrate with other frameworks and tools.

Some of the key takeaways from this chapter are:

*   **Islands**. Astro’s island architecture allows us to create islands of interactivity—loading JavaScript where and when needed in our app.
*   **Project structure**. Our overview of the project structure of an Astro project showed the key files and folders found in an Astro project.
*   **File anatomy**. We explored the anatomy of a `.astro` file, discussing what the script and template sections of a typical `.astro` file look like.
*   **Styling**. We briefly touched on how to use styles in Astro.

And that’s it for the first chapter in this Astro series. Now that we’ve covered the basic concepts, we’ll next take a look at Astro’s options for rendering and layouts.

# Chapter 2: Rendering Options in Astro: Building a Layout

In the previous tutorial, we looked at the basics of Astro: its folder structure, how components work, and how styling works.

This tutorial will focus on layouts and the various rendering options available at our disposal with Astro. Rendering plays a critical part in any web application, since its goal is to display the final output to the end user. With Astro, we have the flexibility to choose between two primary rendering modes: **static site generation** (SSG) and **server-side rendering** (SSR). The former is ideal for generating highly optimized, pre-built HTML during the build process, resulting in lightning-fast load times and SEO-friendly websites. The latter enables dynamic content generation on the server, striking a balance between performance and flexibility.

## Layouts in Astro

While each `.astro` page (route) has the potential to contain a fully-fledged HTML document, it’s inefficient to duplicate that structure, especially when certain elements—such as `<meta>` and `<title>` elements—may vary depending on the currently viewed page. (The inefficiency comes from the fact that we would have to potentially add the same HTML structure to each `.astro` page.)

Therefore, it’s advisable to establish an overarching layout that can be used across all pages. Although not mandatory, organizing the layout files within the `src/layouts` folder makes sense, enabling the addition of multiple layout files—such as one for navigation and another for a footer, or even splitting up the layout for parts of the page (for example, a separate layout for the overall page and for the blog).

Consider the following as an example of a basic website that would encompass common UI elements:

*   `layouts/Layout.astro`: the primary layout file
*   `layouts/Head.astro`: a section for custom `<head>` elements, potentially unique for each page
*   `layouts/Nav.astro`: a navigation bar
*   `layouts/Footer.astro`: a footer section

![Common UI elements on a page](Images/2_4.png)

Here’s a glimpse of the `layouts/Layout.astro` file:

```
---
import Head from './Head.astro';
import Nav from './Nav.astro';
const {
  title = 'Footie is the best',
  description = 'An online football magazine',
} = Astro.props;

import Footer from './Footer.astro';
---

<html lang="en">
  <title>{title}</title>
  <meta name="description" content={description}>
  <body>
    <Nav />
    <div>
      <main>
        <slot />
      </main>
    </div>
    <Footer />
  </body>
</html>
```

#### Mixing HTML Elements and Astro Components

Note that, in the example above, we’re mixing standard HTML elements with Astro components. The ones that are capitalized (`Nav` and `Footer`) are Astro components that are imported in the top part of this sample layout file.

### Astro.props

There are a few key takeaways here. Take note of the `import` function and the usage of `Astro.props`. We can easily import any other component by using the `import` keyword. The special built-in `Astro.props` object allows us to send properties to components and access them. In the code above, default values are set if `Astro.props` lacks the `title` or `description` keys (the default values are `Footie is the best` and `An online football magazine`). This is good practice, and we’re leveraging JavaScript’s default params feature intermixed with object destructuring. However, if there are `props` sent, Astro will pick them up. Let’s take a look at this by examining the code below:

```
<!-- Uses the defaults -->
<Layout />

<!-- Sets title to "My Title," while description retains its default value -->
<Layout title="My Title" />
```

The first `<Layout />` component doesn’t have any `props` attached to it, so it will resort to using the previously mentioned default values. In the second scenario, however, the `title` prop is sent with the value of `My Title`, which means that the page will display the appropriate title.

#### Global Object Properties

Multiple properties are available from the built-in global object [Astro](https://docs.astro.build/en/reference/api-reference/#astro-global).

Lastly, take note of the `<slot />` element, which serves as the insertion point for content from individual `.astro` pages. More on this shortly.

Please also pay attention to the `<Head>` Astro component. Suppose the property and variable holding the value we wish to send to the property share the same name. In that case, we can employ a simpler syntax:

```
const title = 'my title';

<Head title={title} />
<!-- Can be simplified to 👇 -->
<Head {title} />
```

### Slot

Let’s talk a bit more about the built-in `<slot />` element. Once the layouts are ready, the content from Astro files in the `src/pages` folder will be injected where the element mentioned above is placed.

To apply a layout to an Astro file, we need to import it and use it as we’d use any other component:

```
---
import Layout from '../layouts/Layout.astro';
---
<Layout title="Welcome">
  <p>Some content that will be injected into the "slot"</p>
</Layout>
```

## Components

Apart from layout components, a recommended practice is to create a `src/components` folder for storing various components. In Astro, we can include components of any “type”—including both `.astro` and `.jsx` components, for example. One of the powerful features of Astro is that a component created in another framework can be added.

To do this, we first need to install the appropriate integration. (For React, it would be `@astrojs/react`, as explained [in the docs](https://docs.astro.build/en/guides/integrations-guide/react/).) After the installation, we can take a look at an example of adding a React component to Astro:

```
import { useState } from 'react';

const Counter = () => {
  const [counter, setCounter] = useState(0);

  const increment = () => {
    setCounter(counter + 1);
  };

  const decrement = () => {
    setCounter(counter - 1);
  };

  return (
    <div>
      <h1>Counter: {counter}</h1>
      <button onClick={increment}> + </button>
      <button onClick={decrement}> - </button>
    </div>
  );
};

export default Counter;
```

The code above is a React component with a counter that can be incremented and decremented. Let’s add this to Astro now:

```
---
import Counter from '../components/Counter.jsx';
---
<Counter client:only="react" />
```

Notice `client:only="react"`, which is one of the [client directives](https://docs.astro.build/en/reference/directives-reference/). There are multiple ways to use these, and we’ll get back to them at the end of this chapter.

## Routing

As previously discussed, Astro routing revolves around files in the `src/pages` folder. In this chapter, we’ll cover three types of routes: static routes, dynamic routes, and server endpoints (API routes).

### Static Routes

Static routes are pretty straightforward: `.astro` files become routes in the `src/pages` folder. For example:

*   `src/pages/about.astro` becomes `example.com/about`
*   `src/pages/destinations/london.astro` becomes `example.com/destinations/london`

Please recall from the previous chapter that `.md`, `.mdx`, and `.html` files can also generate routes. For instance, `/src/pages/hello.md` becomes `example.com/hello`.

### Dynamic Routes

Dynamic routes are helpful when it’s impractical to manually create routes due to dynamic changes. For example, what if we’re working on a page that lists destinations, and there are over 100 destinations (or an unknown number of them)? Creating individual `.astro` files for each possible route combination isn’t viable.

Instead, we can instruct Astro to use dynamic routes: `src/pages/[destination]` would then become `src/pages/*`, effectively handling all potential variations such as `example.com/london`, `example.com/singapore` and so on. (Note that the route actually requires the `[]` characters.)

To facilitate dynamic routes, Astro requires some information on how to generate files for dynamic routes. This is achieved through the built-in `getStaticPaths()` method. It returns an array of objects, each containing a mandatory `params` object. This object should match the dynamic route definition (such as `destination` in our case):

```
---
const { destination } = Astro.params;

export function getStaticPaths() {
  const destinations = [
    'london',
    'rome',
    'sanfrancisco',
    'singapore',
    'cairo',
    'medellin',
  ];
  // ☝🏼 remember, since this JavaScript is executed on the server, we could pull this data from a REST API endpoint as well
  return destinations.map((destination) => ({ params: { destination } }));
}
---
<h1>Welcome to: {destination}</h1>
```

For situations where multiple parameters need to be handled (such as `/src/pages/[city]-[country].astro`), we can pass multiple props to the params object:

```
return [{ params: { city: 'london', country: 'uk' } }];
```

#### 404 Pages

If there’s a page that doesn’t match a route, Astro will generate a 404 page. Customizing the content of this page is possible by creating a `404.astro` page in the `src/pages` folder.

### Rest Params

Astro also supports rest parameters in dynamic URL routing, as seen in `src/pages/destinations/[...path].astro`. This offers greater flexibility. For example, we could match a path with any combination such as `example.com/destinations/london` and `example.com/london` as well as `example.com/destinations/favourites/rome`.

#### Path Undefined

Returning `{params: { path: undefined }}` in `getSTaticPaths()` effectively matches `example.com/destinations/`.

## Server-side Rendering

Before we continue with our discussion on routing, let’s divert a little bit to discuss another very important aspect of Astro: server-side rendering.

To recap, the default behavior of Astro is static site generation. This means that all the pages are built during build time. However, there can be situations when this isn’t the right approach; things that are dynamic in nature require server-side rendering. Imagine we had a small ecommerce site, and after each successful purchase we had to rebuild our entire site to show a modified stock count for a product. This wouldn’t only be unviable, but there would be times when incorrect stock information would be shown. Server-side rendering solves this problem, because the page content is rendered at the request time, which means that the most up-to-date information can arrive from the server.

Earlier we talked about the `astro.config.mjs` file before. This is the place where we can switch on server-side rendering:

```
import { defineConfig } from 'astro/config';
import nodejs from '@astrojs/node';

export default defineConfig({
  output: 'server',
  adapter: nodejs(),
});
```

`output: 'server'` is the key here, but also take note of the `adapter` setting. An adapter is needed because server-side rendering requires a runtime where our server-side code is going to be executed. For development purposes, using the `nodejs()` adapter is fine, but Astro can be configured with [many other adapters](https://astro.build/integrations/?search=&categories%5B%5D=adapters), including but not limited to Netlify, Vercel and Cloudflare.

#### Adding the Node Adapter

We also need to run the `npx astro add node` command to install and let Astro automatically configure the `nodejs()` adapter for our project.

The key takeaway here is that, with this setting, we’re now switching off Astro’s default static site rendering mechanism and swapping it out for server-side rendering—for all the pages.

But what if we have pages where we don’t want to utilize SSR? Luckily, Astro allows us to selectively turn off SSR and re-enable the default rendering behavior on a per-route basis. Make sure the following is added on the top of any such page route:

```
---
export const prerender = true;
---
<p>This page is pre-rendered at build time<p>
```

### Hybrid Rendering

Even better, we can do the same, but in reverse, so to speak: as opposed to setting the `output: 'server'` option, we can set `output: 'hybrid'`, which means that the default behavior is kept (static site generation at build time), and then we can add the following to page routes where we explicitly want to have SSR enabled:

```
---
export const prerender = false;
---
<p>This is now server-rendered</p>
```

## Server-side Rendering Routes

Now let’s continue our discussion on routes. For server-side rendered pages, `getStaticPaths()` shouldn’t be used, as the content is rendered at request time, not at build time.

### Endpoints

There are two types of endpoints in Astro: Static and API/Server. Static endpoints can be created by adding `.js` or `.ts` files to the `src/pages` directory, which will be called at build time to produce static files. It should also be noted that, during the build process, the extensions are removed. So, for example, `src/pages/destinations.json.js` will become `/destinations.json`.

Endpoints have access to both the `request` and `params` objects, and they should export a `GET` function. Furthermore, dynamic routes are also supported (via the `[]` file naming notation). Recreating an earlier example to be an endpoint using `getStaticPaths()` would look like this:

```
// src/pages/api/[destination].json.js
const destinations = [
  'london',
  'rome',
  'sanfrancisco',
  'singapore',
  'cairo',
  'medellin',
];

export const GET = ({ params }) => {
  const { destination } = params;
  const [myDestination] = destinations.filter(
    (destination) => destination === destination
  );
  return new Response(
    JSON.stringify({
      destination: myDestination,
    })
  );
};

export function getStaticPaths() {
  return destinations.map((destination) => {
    return {
      params: {
        destination,
      },
    };
  });
}
```

#### Using the api Folder

Note that using the `api` folder isn’t mandatory, but it also provides a good separation of concerns, and it’s highly recommended that we use it for storing API endpoints.

#### Accessing the request Object

The endpoint also has access to the `request` object, but in static mode `request.url` is the only available property from that object.

#### Server Endpoints

To create server endpoints (API routes), we need to enable SSR mode in Astro’s configuration file.

Adding a `.js` or `.ts` file to the pages directory creates REST API endpoints that can not only operate with `GET` methods but also have access to all other CRUD methods (`POST`, `PUT`, `DELETE`).

#### Handling GET, POST and DELETE Requests

For handling HTTP delete requests, use `del` in Astro, as `delete` is a JavaScript built-in keyword.

Here’s an example illustrating how to handle HTTP `GET`, `POST` and `DELETE` requests in Astro. The `GET` method accepts parameters (note how the route is defined: `src/pages/api/[id].json.js`). Since we have `[id]` in the route, we can destructure the `params` object and retrieve the value of `id`. The rest of the code in the `GET` method makes a hypothetical database lookup and returns a response with the queried data.

The `POST` method checks if the `Authorization` header was sent as part of the request. If it wasn’t, we return an HTTP status code of 401 (Unauthorized). (Note that we’re simplifying the code here and authentication/authorization requires more steps). If everything’s fine, we parse the data sent as part of the request and do a hypothetical database insert and return a success 201 message:

```
// src/pages/api/[id].json.js
import { getCityData, addCity } from './fake-db.js';

export const GET = async ({ params }) => {
  const { id } = params;
  const cityData = await getCityData(id);
  return new Response(JSON.stringify(cityData), {
    status: 200,
    headers: {
      'Content-Type': 'application/json',
    },
  });
};

export const POST = async ({ request }) => {
  if (!request.headers.get('Authorization')) {
    return new Response(null, { status: 401 });
  }
  const body = await request.json();
  const city = body.city;
  await addCity(city);
  return new Response(
    JSON.stringify({
      message: 'City added',
    }),
    {
      status: 201,
    }
  );
};

export const DEL = ({ request }) => {
  // Handle HTTP delete
};
```

#### Using the request Object

Note that it’s important to use the `request` object to its fullest to achieve authorization and to accept incoming data—which could come from a form.

## Hydration of Interactive Components

In the previous chapter we talked about Astro’s island architecture, which basically is a way to break down a web application into isolated islands that are each responsible for rendering specific parts of the page. Furthermore, this architecture can also dictate which elements require JavaScript to be loaded.

The last thing we’ll discuss in this chapter is how Astro hydrates interactive components. With Astro, we can control when and how client-side JavaScript is loaded for our components. The following options can be used:

*   `client:load`. This option has a high priority and is suitable for crucial elements that require immediate interactivity. The JavaScript code for the component is loaded during the initial page load.

*   `client:idle`. With a medium priority, this option is perfect for components that can afford to wait. The JavaScript code for the component is loaded either after the browser fires the `requestIdleCallback` or the `load` event.

*   `client:visible`. With low priority, this option is ideal for components initially hidden from view and not immediately visible above the fold. The component’s JavaScript is loaded when it becomes visible in the viewport, utilizing the [`IntersectionObserver`](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API).

*   `client:media`. This low-priority choice is best suited for components visible only under specific screen sizes. The JavaScript is loaded when the specified CSS media query triggers, such as `client:media="(min-width: 400px)"`.

*   `client:only`. This attribute bypasses HTML server rendering and exclusively renders on the client. However, we must specify the framework to load, because Astro doesn’t have this information by default. For instance, use `<MyReactComponent client:only="react" />`.

## Demo

Please take a look at the [demo app for this chapter](https://stackblitz.com/github/tpiros/sitepoint-astro) and see if you can determine whether static site rendering of server-side rendering is being used!

## Conclusion

In this chapter, we shifted our focus to layouts and explored the diverse rendering options that Astro has to offer. Rendering is critical for any web app, as it determines the final presentation of content to end users. We explored how to create layouts in Astro and how to work with routes to create a compelling web application. We also looked at how to create and work with static site generation and server-side rendering in Astro.

In the next chapter, we’ll explore how to fetch data using Astro.

# Chapter 3: Fetching and Using Data with Astro

In this third part of our Astro series, we’ll explore how to retrieve data in Astro. Data fetching is a fundamental aspect of web applications, as it allows for the creation of dynamic content—such as data coming from a content management system (CMS). It also caters for personalization, where applications retrieve user-specific information such as preferences or profile information.

In this series so far we’ve learned quite a few things about Astro, such as how its project structure works, how to create routes and components, and how to work with both static site generation and server-side rendering.

In this chapter, we’ll examine how Astro’s capabilities extend beyond rendering web content to efficiently handling the retrieval and integration of dynamic data, enhancing the overall user experience and functionality of web applications. You’ll be happy to hear that this is also incredibly straightforward.

Remember that we have a code fence (the content enclosed between `---` lines at the top of each `.astro` page). Inside it, we can write JavaScript or TypeScript code, and this opens up a lot of possibilities.

What’s even better news is the fact that, out of the box, Astro supports [top-level `await`](https://v8.dev/features/top-level-await) and all modern web APIs. This allows us to effortlessly use the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) to request data. And having zero third-party dependencies is always a good thing!

#### Fetch Execution

With server-side rendering enabled, fetch calls are executed at request time, while without SSR (Astro’s normal operation of static site rendering), fetch calls are executed at build time.

Let’s take a look at how this works in action. In any `.astro` page, we can simply use code similar to this to fetch data:

```
---
const response = await fetch('an-api-endpoint');
const data = await response.json();
---
<pre>{JSON.stringify(data)}</pre>
```

The code above makes a Fetch API request to an endpoint, parses the data to a JSON object, and then uses a simple `JSON.stringify` method to display the data.

Let’s create another example where we fetch real data to see how to iterate through the results. While there are plenty of free REST APIs available out there, my choice is to use the [Star Wars API](https://swapi.dev):

```
---
const response = await fetch('https://swapi.dev/api/people');
const data = await response.json();
const characters = data.results;
---
<h1>Star Wars Characters</h1>
<ul>
  {characters.map(({name}) => (
    <li>{name}</li>
  ))}
</ul>
```

The code above makes the request to the aforementioned REST API, processes the data, and iterates through the results by using the standard JavaScript `map()` method.

Note that we can also consume an API endpoint created as part of the project. (We covered server endpoints in the previous chapter.) To do this, we need to reference the full URL, but luckily Astro exposes that via a built-in global object: `Astro.url`. This is how the code looks when referencing a custom-built API call:

```
---
const response = await fetch(`${Astro.url.origin}/api/endpoint`);
const data = await response.json();
---
<pre>{JSON.stringify(data)}</pre>
```

This makes it incredibly easy to retrieve data.

## Working with GraphQL

Sometimes there may be a requirement in a project to use GraphQL instead of a REST API. (GraphQL is a query language for APIs that enables clients to request precisely the data they need, facilitating more efficient and flexible data retrieval compared to traditional REST APIs, which typically expose a set of fixed endpoints with pre-defined data structures.)

Astro can also seamlessly interact with GraphQL endpoints and utilize the Fetch API, so again, we can execute GraphQL queries with no additional dependencies added to a project:

```
---
const method = 'POST';
const query = `{
  query getDestination($id: ID) {
      destination($id) {
        capital,
        flag
      }
    }
  }
}`;
const variables = {
  id: 'italy'
}

const options = {
  method,
  body: {
    query,
    variables
  }
}
const response = await fetch('/graphql/endpoint', options);
const data = await response.json();
---
<pre>{JSON.stringify(data)}</pre>
```

In the code above, we’re constructing a GraphQL query to get information from a GraphQL service about a destination. As part of the query, we’re requesting the capital and the flag. Since this is a parameterized GraphQL query, we’re also specifying what the `id` should be.

Next, we create an `options` object, which will make sure that our Fetch API request is using the HTTP method of `POST`, and that the GraphQL query and its variable are sent as part of the request body. The rest of the code is pretty self explanatory: we make the request, process the response, and display that using `JSON.stringify()`.

## Data Retrieval from a Server Endpoint

As discussed in the previous chapter, Astro can create server API endpoints, and it’s possible to consume data returned from these server endpoints as well.

Suppose we’ve added `src/pages/api/products.json.js` (a server API endpoint). In that case, we can easily access it on any `src/pages/` page by adding something similar to a `.astro` file, like so:

```
---
const response = await fetch(`${Astro.url.origin}/api/products.json`);
const products = await response.json();
---
<ul>
  {products.map((data) => <li>{data.name}</li>)}
</ul>
```

In this block of code, we’re making a request against an Astro server endpoint, grabbing the results, and storing them in a `products` variable. Since the data we get back is an array, we can iterate through that using the `map()` method.

#### Sensitive Data Protected by Fences

Remember that, since the code between the `---` fences is executed at build time, it’s safe to use API keys and other methods even for data fetching.

## Forms

Though working with form data isn’t necessarily directly related to data retrieval, it’s still worth mentioning it here. With Astro, we can rely on `Astro.request` not only to check if the incoming method (via the `.method` property) is a `POST` method, but we can also access `formData` sent from the UI interface.

#### formData and SSR

Note that `formData` is only available if we have server-side rendering enabled.

You can access any form of data in the script section of `.astro` files:

```
---
if (Astro.request.method === 'POST') {
  const data = await Astro.request.formData();
  const name = data.get('name');
  // Process 'data' or 'name,' e.g., send it to a server via `fetch()`
}
---
<h1>Form</h1>
  <form method="post">
  <input type="text" name="name" />
  <button>Submit</button>
</form>
```

The code above first checks if the request method is using the HTTP `POST` method. Since we’re using `method="post"` on the form in the HTML template, the `if` clause will trigger and we’ll be able to access the data from the form by using `Astro.request.formData()`. Once we have that data, we can use the `get()` method to grab the value from `<input type="text" name="name" />`. Please note that the input’s `name` attribute matches the value passed to the `get()` method.

## Headless CMS

Often data will be coming from a CMS of some sort. The good news (yet again!) is that Astro can also be [integrated with various Headless CMS providers](https://docs.astro.build/en/guides/cms/).

It’s worth noting that these out-of-the-box integrations are great, but we can also work with a CMS that isn’t on the list. One prominent example is [Strapi](https://strapi.io), which exposes its data via API endpoints (as well as GraphQL queries)—meaning that we can simply use that CMS by utilizing the Fetch API in Astro for even greater flexibility.

## Demo

The demo for this tutorial series on [stackblitz.com](https://stackblitz.com/github/tpiros/sitepoint-astro). Take a look at `characters.astro` to see how a Fetch API request is done.

## Conclusion

In this chapter, we dived deep into the realm of data retrieval with Astro. Data fetching—a fundamental pillar of web applications—opens the door to dynamic content, enabling the integration of data from sources like content management systems and providing the means for personalization by fetching user-specific information.

The beauty of Astro lies in its native support for modern web APIs and top-level `await`, allowing effortless use of the Fetch API without any third-party dependencies. With server-side rendering, fetch calls occur at request time, whereas in Astro’s default static site rendering mode they take place at build time.

We also delved into the world of GraphQL, demonstrating how Astro seamlessly interacts with GraphQL endpoints, utilizing the Fetch API to execute GraphQL queries as well.

Lastly, we highlighted Astro’s versatility in working with headless content management systems. Whether through out-of-the-box integrations or custom interactions with CMS providers like Strapi, Astro offers flexibility and ease in integrating external data sources, further expanding its capabilities in data retrieval for web applications.

In the next chapter, we’ll learn how to work with content collections in Astro.

# Chapter 4: Getting Started with Content Collections and View Transitions in Astro

In this chapter, we’ll take a look at content collections and view transitions.

One of the notable additions in Astro version 2 was the introduction of content collections. This feature proves particularly valuable when working with `.md` or `.mdx` files. Content collections empower us to effectively manage our content while also enabling data validation and TypeScript type safety for all the content within an Astro project.

Since Astro version 3, and with added features in version 4, view transitions are also part of Astro. In fact, Astro was the first framework to implement this new web feature. **View transitions** serve as a user navigation aid: they enable the seamless redirection of user attention towards the core message of a web page, allowing for a rich user experience. With view transitions, the user experience can be improved with no cost to performance.

## Getting Started with Content Collections

To make use of content collections, Astro designates a special folder: `src/content`. Subsequently, we can create subfolders within this location, each generating individual content collections. For instance, we could create collections such as `src/content/dev-blog` and `src/content/corporate-blog`.

![The architecture of our collections](Images/4.png)

Each content collection can be configured in a config file—`/src/content/config.js` (or `.ts`)—where we have the option to employ collection schemas using [Zod](https://zod.dev).

Zod is a “TypeScript-first schema validation with static type inference” that’s integrated into Astro. Here’s an example of how this would take shape:

```
// src/content/config.js
import { z, defineCollection } from 'astro:content';

const devBlogCollection = defineCollection({
  schema: z.object({
    title: z.string(),
    author: z.string().default('The Dev Team'),
    tags: z.array(z.string()),
    date: z.date(),
    draft: z.boolean().default(true),
    description: z.string(),
  }),
});

const corporateBlogCollection = defineCollection({
  schema: z.object({
    title: z.string(),
    author: z.string(),
    date: z.date(),
    featured: z.boolean(),
    language: z.enum(['en', 'es']),
  }),
});

export const collections = {
  devblog: devBlogCollection,
  corporateblog: corporateBlogCollection,
};
```

In the code above, we’re defining two content collections—one for a “developer blog” and one for a “corporate blog”. The `defineCollection` method allows us to create a `schema` for any given collection. For the “developer blog”, we’re creating a schema where the articles for this blog category must have a title (string), author (string defaulting to “The Dev Team”), tags (array of strings), date (date type), draft (Boolean defaulting to `true`) and a description (string).

For the “corporate blog”, our schema is a little bit different: we have a string for both the title and the author. Date (data type) is also going to be required by the content, as well as the featured (Boolean) flag and a language (enum), which can either be set to `en` or `es`.

Lastly, we’re exporting a `collections` object with two properties, `devblog` and `corporateblog`. These will be used later on.

#### Markdown Files and Frontmatter

The examples in this tutorial about content collection assume that the `.md` files also include `frontmatter` matching the schema specified above in the configuration file. As an example, this is what a sample “corporate blog” post would look like:

```
---
title: 'Buy!!'
author: 'Jack from Marketing'
date: 2023-07-19
featured: true
language: 'en'
---

# Some Marketing Promo

This is the best product!
```

### Slug Creation

Astro will automatically generate slugs for posts based on the file name. For example, the slug for `first-post.md` will be `first-post`. However, if we provide a `slug` entry in our `frontmatter`, Astro will respect that and use our custom slug.

Bear in mind that the properties specified in the `export const collections` object must match the folder names where the content is going to live. (Also note that they’re case sensitive!)

### Querying Data

Once we have all the Markdown files in place (in our case, that would be under `src/content/devblog` and `src/content/corporateblog`) and our `config.js` file ready, we can start to query data from the collections, which is a straightforward process:

```
---
import { getCollection } from 'astro:content';
const allDevPosts = await getCollection('devblog');
const allCorporatePosts = await getCollection('corporateblog');
---
<pre>{JSON.stringify(allDevPosts)}</pre>
<pre>{JSON.stringify(allCorporatePosts)}</pre>
```

As seen above, the `getCollection` method can be used to retrieve all the entries from a given collection (again, referencing the exported collection names from earlier). In the example above, we retrieve all the posts from both the “developer blog” (`devblog`) and from the “corporate blog” (`corporateblog`). In the template, we simply return the raw data using `JSON.stringify()`.

We should also examine the data that’s being displayed via `JSON.stringify()`, and we should take note that, other than the `frontmatter` data, we also get an `id`, a `slug`, and a `body` property returned to use where the latter contains the post’s content.

We can also filter for drafts or posts written in a particular language in the `frontmatter` section by iterating through all articles like this:

```
import { getCollection } from 'astro:content';

const spanishEntries = await getCollection('corporateblog', ({ data }) => {
  return data.language === 'es';
});
```

`getCollection` returns all the posts, but we can also use `getEntry` to return a single entry from within a collection:

```
import { getEntry } from 'astro:content';

const singleEntry = await getEntry('corporateblog', 'pr-article-1');
```

### getCollection vs getEntries

While there are two ways to return multiple posts from collections, there’s a subtle difference between the two of them. `getCollection()` retrieves a list of content collection entries by collection name, while `getEntries()` retrieves multiple collection entries from the same collection.

The Astro documentation gives the example of `getEntries()` being used to retrieve content when using reference entities (for example, a list of related posts).

The concept of related posts is where we can reference an array of posts from a collection. This can be achieved by adding the following to the schema when using the `defineCollection` method:

```
import { defineCollection, reference, z } from 'astro:content';

const devblog = defineCollection({
  schema: z.object({
    title: z.string(),
    relatedPosts: z.array(reference('blog')),
  }),
});
```

In the code above, we’re also importing `reference` and using that when adding `relatedPosts` to our schema. (Note that we can call this whatever we want, such as `recommendedPosts` or `followupPosts`.)

To use these `relatedPosts`, the appropriate slug values should be added to the `frontmatter` part of the Markdown:

```
title: "This is a post"
relatedPosts:

- A related post # `src/content/devblog/a-related-post.md
```

Reference entities are defined in the `config.js` file for the content collection and use the `reference` method from Zod:

```
const blog = defineCollection({
  type: 'content',
  schema: z.object({
    title: z.string(),
    relatedPosts: z.array(reference('blog')).optional(),
    author: reference('author'),
  }),
});

const author = defineCollection({
  type: 'data',
  schema: z.object({
    name: z.string(),
  }),
});
```

Also, notice the usage of `type: 'content'` and `type: 'data'`. In this case, the collection encompasses both content authoring formats such as Markdown (`type: 'content'`) and data formats like JSON or YAML (`type: 'data'`).

### Displaying the Content

Now that we know how to query data, let’s discuss how to actually display it in a formatted way. Astro provides a convenient method called `render()` to render the entire content of the Markdown into a built-in Astro component called `<Content />`. How we build and display the content is also going to be driven by whether we have static site generation or server-side rendering mode.

For pre-rendering, we can use the `getStaticPaths()` method:

```
// /src/pages/posts/[...slug].astro
---
import { getCollection } from 'astro:content';

export async function getStaticPaths() {
  const blogEntries = await getCollection('blog');
  return blogEntries.map(entry => ({
    params: { slug: entry.slug }, props: { entry },
  }));
}

const { entry } = Astro.props;
const { Content } = await entry.render();
---
<h1>{entry.data.title}</h1>
<Content />
```

In the code above, we’re using `getStaticPaths()`. (We covered this method in the second chapter of this book as a way to cater for dynamic routes.) We then rely on `Astro.props` to capture the `entry`, which is going to be an object that contains the metadata about the entry, an `id`, a `slug`, and a `render()` method. This method is responsible for rendering the Markdown entry to HTML in the Astro template, and it does so by creating a `<Content />` component. What’s amazing about this is that all we need to do now is add the `<Content />` component to our template and we’ll be able to see the Markdown content rendered into HTML.

#### Rendering Options

As a refresher, or in case you missed it, the second chapter of this book discusses the various rendering options available.

For SSR, a slightly different approach needs to be followed. Instead of using `getStaticPaths()`, `Astro.params` can be utilized, as the content will be pulled and rendered at request time:

```
---
import { getEntry } from 'astro:content';

const { slug } = Astro.params;
const entry = await getEntry('blog', slug);
const { Content } = await entry.render();
---
<h1>{entry.data.title}</h1>
<Content />
```

#### Integrating Tailwind CSS with Astro

In the introductory tutorial, we talked about integrating Tailwind CSS with Astro. Tailwind has a [typography plugin](https://tailwindcss.com/docs/typography-plugin) (`@tailwindcss/typography`) that can be used to add styling to HTML rendered from Markdown. I recommend that you check it out if you haven’t already. Please take a look at the screenshot below. On the left is the rendered template from Markdown without the typography plugin, and on the right is the rendered template with it.

![The rendered template with and without the typography plugin](Images/typography.png)

## View Transitions

The [View Transitions API](https://developer.mozilla.org/en-US/docs/Web/API/View_Transitions_API) offers a convenient way to generate animated transitions between various DOM states while simultaneously updating the DOM content in a single operation. Achieving this has traditionally been difficult on the Web, but with this new API, transitions can be handled in a rather easy way. [Studies](https://developer.chrome.com/blog/view-transitions-case-studies/#redbus) have shown that using the View Transitions API leads to a faster perceived site performance.

Astro supports view transitions out of the box, with a built-in fallback mechanism for browsers that don’t currently support the API.

The out-of-the-box solution supports built-in animations, animations for forward and backward navigation, and automatic support for accessibility (via `prefers-reduced-motion`), amongst many other things.

#### Prefers Reduced Motion

The `prefers-reduced-motion` media query is important, as it allows web developers to create more inclusive and accessible user experiences by respecting user preferences for reduced motion, benefiting individuals with motion sensitivity or vestibular disorders.

#### Browser Support for View Transitions

While the View Transition API is a great innovation and is worth trying out, keep in mind that it’s still experimental and currently has [only partial browser support](https://caniuse.com/view-transitions).

One of the best ways to demonstrate view transitions is to utilize a video element that will maintain its state between page transitions. (Do note that we can also persist state between components that utilize the `client:*` directives as well.) An example of this is shown in [this video](https://player.vimeo.com/video/884466855?h=fdaebb6dba&badge=0&autopause=0&quality_selector=1&player_id=0&app_id=58479).

Let’s assume that we have a `<Video />` component with this content:

```
---
// src/components/Video
const src = 'https://res.cloudinary.com/tamas-demo/video/upload/f_auto,q_auto/imagecon/ship.mp4';
const {
  autoplay = false,
  controls = true,
  loop = false
} = Astro.props;
---

<video {controls} {autoplay} {loop} transition:persist>
  <source {src} />
</video>
```

In the code above, we’re grabbing a video from Cloudinary. Additionally, we’re allowing the video to automatically play and loop (start over) when it finishes, and we’re providing control buttons for the user. These settings are determined by properties sent to this video component, and if these properties aren’t provided, default values are used. These variables are then added to the HTML `<video>` and `<source>` elements.

Please take note of the `transition:persist` directive. With this directive, we’ll maintain the state of the video player between transitions: while navigating to the next page, the video will keep on playing, while other parts of the page will show the updated content. We can use this component on both the `index.astro` and `about.astro` pages:

```
// src/pages/index.astro
---
import Video from '../components/Video.astro';
---
<!-- some other HTML -->
<Video />
```

Lastly, we need to enable page transitions, which we can either do per page or globally for the entire project. Assuming that we have a layout file of some sort, we can easily enable it, by importing `ViewTransitions` from `astro:transitions`:

```
// src/layouts/Layout.astro
---
import { ViewTransitions } from 'astro:transitions';
---
<html lang="en">
  <head>
    <title>My site!</title>
    <ViewTransitions />
  </head>
  <body>
    <slot />
  </body>
</html>
```

In summary, the experimental View Transitions API simplifies visual transitions between various pages or elements through CSS pseudo-elements, JavaScript, and snapshots of the previous and current DOM states. It presents a fresh chance to enhance the perceived performance of a page, minimizing reliance on intricate custom JavaScript and CSS.

## Demo

The [demo that we’ve deployed on StackBlitz](https://stackblitz.com/github/tpiros/sitepoint-astro) for this tutorial utilizes content collections. Take a look at `src/pages/posts.astro`, the `src/content` folder and `src/pages/posts/[...slug].astro` to check out the implementation details.

## Conclusion

In this chapter, we delved into two essential features in Astro: content collections and view transitions. Content collection allows for efficient content management and data validation, particularly when working with `.md` or `.mdx` files. View transitions, on the other hand, provide a seamless way to enhance user navigation, all while maintaining excellent performance.

In the next chapter in this series, we’ll take a look at the built-in `Image` component in Astro, which allows for creating performant image assets.

# Chapter 5: Image Optimization and Deploying Our First Astro Site

In this final chapter, we’ll look at the image optimization options offered by Astro, and we’ll learn how to deploy a production-ready site built with Astro.

Image optimization is (or rather, should be) an important discussion point, as the heaviest resources on a web page are generally image (or video) assets. Therefore, optimizing images plays a crucial part in web development. Today, there are multiple image formats. There are also many tools for converting images between formats so that they become smaller in terms of kilobytes, resulting in better experiences for users. This result is measured by the [Largest Contentful Paint](https://web.dev/articles/lcp) metric, which is part of [Core Web Vitals](https://web.dev/explore/learn-core-web-vitals).

Fortunately, Astro provides us with some incredibly handy tools right out of the box that make image optimization a snap. Let’s take a look!

## The Image component

Astro provides a built-in `<Image />` component that utilizes the [Sharp](https://www.npmjs.com/package/sharp) library or [Squoosh](https://www.npmjs.com/package/@squoosh/lib) behind the scenes to optimize images (the default is Sharp). This is an excellent starting point if you want to achieve quick improvements in your image performance. The component takes an image (which is an unoptimized image asset) and produces an optimized version of it. The good news is that, even without changing any defaults, you can get a lot of savings right out of the box.

#### Switching from Sharp to Squoosh

To change from `sharp` to `squoosh`, you need to edit your `astro.config.mjs` file:

```
import { defineConfig, squooshImageService } from 'astro/config';

export default defineConfig({
  image: {
    service: squooshImageService(),
  },
});
```

#### Squoosh CLI

While we could choose the Squoosh CLI as an alternative to the default Sharp library, unfortunately Squoosh CLI is no longer actively maintained.

To use the `<Image />` component, we first simply place our image assets in the `src` folder (subfolders can be created as needed). Then, in any of our `.astro` files, we import them—along with the `<Image />` component—like this:

```
import { Image } from 'astro:assets';
import spain from '~/assets/spain.jpeg';
```

In the code above, we’re importing both the `Image` component as well as an image (`spain.jpeg`).

#### Storing Images in the public Folder

We can also store images in the `public` folder, but that’s always going to be served from the `build` folder without any processing.

When we’re ready to display the image(s), we can add the following code:

```
<Image src={spain} width={400} alt="Some Text" />
```

In the code above, we’re using the previously imported `Image` component and setting its source (`src`) attribute to be equal to the image we’ve also imported earlier. We’re also adding a `width` and `alt` attribute to the component.

#### Cumulative Layout Shift

Always add a `width` or `height` property to your image to reduce your Cumulative Layout Shift (which is measured by the Core Web Vitals).

**Cumulative Layout Shift** measures the visual stability of a page by quantifying the unexpected layout shifts that occur during the page’s loading time.

As an additional exercise, we can run `console.log(spain)` to see the properties accessible from the imported image object. Also, inspect the network panel in the browser’s developer tools to observe the new image weight, as well as the image headers, which should now be set to a so-called “next-gen” image format such as `.webp`.

During the production build of our Astro project, we’ll find details about image optimization in the build log for all our image assets, highlighting the savings as well as the time it took for the tool to optimize the image:

```
 generating optimized images
  ▶ /_astro/spain.9abbae23_ZpzbJG.webp (before: 2724kB, after: 24kB) (+78ms) (1/1)
```

#### getImage

Astro also has a [`getImage()` method](https://docs.astro.build/en/reference/api-reference/#getimage) that can do on-demand image optimization without using the `<Image />` component. But remember that this method only works with server-only APIs.

## Performance

Changing the width of the image via the image component actually generates an image with the given width (as opposed to just shrinking the original image down with CSS in the browser), which therefore yields further bandwidth savings. Generally speaking, it’s bad practice to transfer the image at its original size over the network and shrink it down using CSS only on the client side.

#### Don’t Be Lazy

By default, the `<Image />` component will generate an `<img>` element that has the `loading="lazy"` attribute added to it. In my opinion, this is really dangerous, as it can cause performance issues related to the Largest Contentful Paint Core Web Vital metric. If an image element is being considered for the LCP calculation—in other words, if the image is the largest element that loads for the page and it’s “above the fold”—we shouldn’t set the image to load lazily. Be careful!

For more advanced image manipulation—such as generating thumbnails, cropping, or adding overlays—we may need to use a service like [Cloudinary](https://cloudinary.com). In fact, since Cloudinary provides a Node.js SDK that has the capacity to generate a fully optimized image and render it via the `<img>` element, it works charmingly with an Astro project as well. Here’s how this would look:

```
---
import { Image } from 'astro:assets';
import { v2 as cloudinary, config } from 'cloudinary';

config({
  cloud_name: 'tamas-demo',
  api_key: import.meta.env.CLOUDINARY_API_KEY,
  api_secret: import.meta.env.CLOUDINARY_API_SECRET,
  secure: true
});

const cloudinaryImage = cloudinary.image("r6bswlzed6oisy4bu4sb", {
  transformation: [
    { width: 800, crop: "scale" },
    { color: "#ff0", overlay: {font_family: "Roboto", font_size: 70, font_weight: "bold", text: "Munich, Germany" } },
    { flags: "layer_apply", gravity: "south", y: 20 }
  ]
})
---

<div class="py-6" set:html={cloudinaryImage}></div>
```

In the code above, we’re importing Astro’s `Image` component, as well as the Cloudinary Node.js SDK. Since this is a third-party service, we need to configure it by adding our Cloudinary username (`cloud_name`), the API key, and the secret—all of which can all be found in our Cloudinary account’s dashboard.

Using the Cloudinary Node.js SDK, we’re creating an image transformation. Each object in the `transformation` array modifies the image. The first object crops the image to a width of `800`. The second object overlays the image with text, using the Roboto font face at a size of `70px`. The overlay text is “Munich, Germany”. The last object places the text overlay at the bottom part of the image (`south`), `20px` from the bottom (`y: 20`).

The code above generates an actual `<img>` element, and from this point usage of the `set:html` directive is required. Also note that the code is using environment variables that live in a `.env` file. The resulting image will have a text overlay (where the text overlay has a few separate settings such as color and font face) carefully placed within the image. All of this is generated at build time, so the result will be an image with the text already overlaid.

#### Environment Variable Rules

It’s worth noting here that the rules governing environment variables are consistent with those outlined in the [Vite documentation](https://vitejs.dev/guide/env-and-mode.html).

## Deployment

Now that we’ve gone through the steps of preparing our Astro site, we come to the topic of deployment, as we get ready to show our project to the world. Astro deployment couldn’t be easier: we simply run the `npm run dev` command, which will result in the creation of a folder called `dist` in the root project folder.

### Local Preview

If we want to see what our site looks like after a build, we can run `npx http-server dist/` (or use any other way) to serve the content of the `dist` folder. I also recommend opening up a few files in that folder to see what the Astro build has produced.

Depending on whether we have static site generation mode or server-side rendering mode switched on, the type of deployment provider that we can use changes. For example, a static site can be easily deployed to GitHub Pages or Cloudflare Pages, while a site utilizing SSR can be deployed to Netlify or Vercel. For a full, filterable list of the various deployment options on offer, [refer to the Astro documentation](https://docs.astro.build/en/guides/deploy/).

Also, bear in mind that, when using SSR mode with Astro, we need to [install an adapter and configure it](https://docs.astro.build/en/guides/server-side-rendering/#adding-an-adapter) appropriately.

## Conclusion

Since this is the last chapter, let’s summarize what we’ve learned.

Astro is a modern frontend framework allowing developers to create performant websites. It combines the benefits of static site generation with dynamic interactivity, making it a powerful choice for building fast and efficient web applications. Astro’s focus on performance and developer experience has led to a framework that’s gaining popularity among developers looking for a fresh approach to web development.

In this book, we looked at Astro’s versatile rendering model, which blends static site generation and server-side rendering. It allows developers to choose how and when content is rendered, providing excellent flexibility.

We also looked at Astro’s data fetching features. Astro supports top-level `await`, making it easy to fetch data from APIs or other sources. Developers can use the Fetch API and modern web APIs without the need for third-party dependencies.

We also talked about content collections, a valuable feature for managing content, especially when working with Markdown (`.md` or `.mdx`) files. This empowers developers to maintain and validate content easily within an Astro project while ensuring TypeScript type safety. In that chapter, we also explored the View Transition API—an experimental feature in browsers that simplifies visual transitions between pages or elements by combining CSS pseudo-elements, JavaScript, and DOM state snapshots.

In this final chapter, we looked at Astro’s capabilities for image optimization, minimizing the performance impact of images on web apps. Astro’s built-in image optimization capabilities enable developers to create visually appealing websites without compromising load times.

I hope you’ve enjoyed reading this series on Astro, and that you’re as enthusiastic about Astro as I am. The last step in your learning process is to get your hands dirty. Go and try out Astro today!