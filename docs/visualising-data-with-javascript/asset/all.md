![](images/jacket/front-cover.png)

# Table of Contents

Visualising Data with JavaScript

Copyright © 2025 Peter Cook. All rights reserved.

This version was published on 7th February 2025.

# 1. Introduction

Visualising Data with Javascript teaches you how to make maps, charts and data stories with JavaScript. You’ll learn about:

*   JavaScript’s role in data visualisation
*   how to create charts and maps using JavaScript libraries such as Chart.js, D3.js and Leaflet
*   how to combine maps and charts to create and publish data stories

You’ll learn how to make charts using Chart.js (Figure 1), maps using Leaflet (Figure 2), custom data visualisations using D3.js (Figure 3) and data stories using HTML, CSS, JavaScript, Chart.js and Leaflet (Figure 4).

![chartjs styled 1](images/chartjs-styled-1.png)

Figure 1\. Chart.js bar chart

![leaflet](images/leaflet.png)

Figure 2\. Leaflet map

![d3 timeline](images/d3-timeline.png)

Figure 3\. D3.js timeline

![data story](images/data-story.png)

Figure 4\. Data story

* * *

## 1.1\. Prerequisites

To get the most out of this book you need:

*   access to a computer with Node.js installed and a code editor (such as VS Code)
*   moderate experience with HTML, CSS and JavaScript
*   moderate experience with the command line, Node.js and npm

If you’ve built (or worked on) a web application you should be fine. Knowledge of JavaScript arrow functions, callback functions and promises is useful for this book. If you need to get up to speed with HTML, CSS, SVG and/or JavaScript I recommend reading [Fundamentals of HTML, SVG, CSS and JavaScript for Data Visualisation](https://leanpub.com/html-svg-css-js-for-data-visualisation) (also by myself). This contains all the necessary background knowledge for this book.

## 1.2\. Setting expectations

This book aims to get you up and running with Chart.js, D3, Leaflet and shows you how to make a data story.

It covers the fundamentals of making maps and charts as well as how to get started using each of these libraries. It doesn’t go into great detail about the libraries but seeks to motivate you to learn more about them and empower you to make your own data visualisations.

## 1.3\. The code

This book covers several example projects. Download a zip of the code from [app.createwithdata.com/downloads/visualising-data-with-js-book-code.zip](https://app.createwithdata.com/downloads/visualising-data-with-js-book-code.zip). Unzip the file and move the directory to your usual development directory.

Contact me at [help@createwithdata.com](mailto:help@createwithdata.com) if you have any issues downloading the code.

* * *

## 1.4\. The data

This book uses a single dataset from the UK government’s Renewable Energy Planning Database ([https://www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract](https://www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract)). It tracks UK renewable energy projects through the planning system from 1990 onwards.

We use a snapshot of the dataset published in January 2023 that contains just over 8000 rows. Each row represents a planning application and has fields including name, technology (the type of technology such as solar or wind), capacity (the output capacity in megawatts), location (latitude and longitude), region, status (e.g. operational, refused, under construction) and year submitted.

We use this data because:

*   it’s real data that’s published by a reputable source
*   it has a mix of categorical and numeric data
*   it has a geographic element to it (the location of each project)
*   it’s a good size for educational purposes (it’s not tiny nor is it massive)

The original data looks like:

![repd data sheet](images/repd-data-sheet.png)

Figure 5\. REPD data (some rows and columns omitted)

For the purposes of this book I’ve transformed the data into a JSON file. A subset of the original data’s columns are used and the columns are renamed. Some new properties `yearSubmitted`, `yearGranted` and `daysUntilGranted` have also been added:

* * *

```
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  {
    "id": "3",
    "name": "Ferrybridge Multifuel 2 (FM2)",
    "technology": "EfW Incineration",
    "capacity": 70,
    "lon": -1.282,
    "lat": 53.716,
    "region": "Yorkshire and Humber",
    "status": "Operational",
    "operator": "Scottish and Southern Energy (SSE)",
    "yearSubmitted": 2014,
    "dateSubmitted": "2014-08-20T00:00:00.000Z",
    "yearGranted": 2015,
    "daysUntilGranted": 434
  },
  ...
]
```

Listing 1\. First few items in the JSON file

You can inspect the data for yourself in the code download at `load-data/public/repd.json`.

For more information about converting the REPD CSV file into `repd.json` visit the Data Wrangling section in the Appendix at the end of this book.

* * *

## 1.5\. Book Structure

The book is organised into the following chapters:

*   JavaScript and Data Visualisation
*   Make a Chart with Chart.js
*   Styling and Customising Chart.js
*   Custom Charts with D3.js
*   Data-driven Maps with Leaflet
*   Data Stories

The **JavaScript and Data Visualisation** chapter gives a brief overview of data visualisation and JavaScript’s role in data visualisation. It also covers how to create a web application using the build tool Vite and walks through an example application that loads some data and displays it as a table.

The **Make a Chart with Chart.js** chapter introduces Chart.js and shows how to make a simple bar chart. It introduces the tidy.js JavaScript library which is used for processing and analysing data. The chapter closes by walking through a Chart.js example.

The **Styling and Customising Chart.js** chapter shows how to style Chart.js charts. It also shows how to create multi-series charts such as multi-line charts and stacked bar charts.

The **Custom Charts with D3.js** gives a brief introduction to the D3.js JavaScript library. D3.js helps you create custom charts and is useful if you have a specific requirement that cannot be met by the likes of Chart.js. However, it comes at a cost. D3.js has a steeper learning curve than Chart.js and requires much more effort to create a production ready chart.

The **Data-driven Maps with Leaflet** chapter introduces the mapping library Leaflet and shows how to draw data points on a map.

The **Data Stories** chapter shows how you can create and publish a web page that incorporates text, maps and charts. This is useful if you want to present your data as a story (or report).

# 2\. Data Visualisation and JavaScript

This chapter gives an overview of JavaScript’s role in data visualisation. It also shows how to create a web application using the build tool Vite and walks through an example application that loads some data and displays it as a table.

## 2.1\. Data Visualisation

Data visualisation is the process of representing data using graphics (rather than numbers).

For example, suppose you have a table of sales data:

![simple table of numbers](images/simple-table-of-numbers.png)

Figure 6\. A table of sales data

It’s hard to spot any trends in the data just by looking at the numbers. A data analyst might run a regression test to see if there’s a trend but you can also visualise the data by plotting a line chart:

![simple table of numbers as chart](images/simple-table-of-numbers-as-chart.png)

Figure 7\. The sales data represented with a line chart

We can immediately see there’s an upward trend and that there was a peak in August. This is the power of data visualisation. It reveals patterns that aren’t apparent in a table of numbers.

### 2.1.1\. Why visualise data?

There’s plenty of reasons to visualise data such as:

*   it’s an effective approach to understanding and communicating data
*   it can offer increased visual variety that helps engage the reader
*   it can be a visually appealing work in its own right (good for content, SEO etc.)

### 2.1.2\. Best practice

There’s plenty of books about data visualisation best practice. One that springs to mind is Alberto Cairo’s [The Functional Art](https://www.oreilly.com/library/view/the-functional-art/9780133041187/). This has a handy chapter that explains which charts are most effective at conveying data based on academic understanding of human perception. In short it’s best to use position and length to represent data (rather than direction, area and/or shade) because we are able to perceive differences in position and length better than other encodings. This is one of the reasons bar, line and scatter charts are so prevalent.

That’s not to say non-standard charts are ineffective. So long as the important quantities are represented using position and length custom charts can also be effective at conveying data.

## 2.2\. JavaScript

JavaScript is the programming language of the web and is implemented in all major web browsers. It has a similar syntax to C-style programming languages such as C, C++, Java, PHP and is commonly used to add interactivity to web sites and applications.

It’s also used to add and modify content within a web page. For example it can be used to add interactive charts to a web page.

### 2.2.1\. Why visualise data using JavaScript?

There’s several reasons why JavaScript is one of the leading (if not the leading) language for visualising data:

*   it’s the only language implemented in major web browsers
*   it’s well suited to working with data
*   it has plenty of data visualisation libraries including Chart.js, Leaflet and D3.js.

* * *

### 2.2.2\. History of JavaScript and Data Visualisation

JavaScript charting libraries have existed almost as long as JavaScript itself (which was introduced in 1995)^([[¹](#fn1)]). As far as I can tell the earliest ones that are still maintained are [Google Charts](https://developers.google.com/chart) and [Flot](https://www.flotcharts.org/) which were both introduced around 2007 and support standard charts such as bar charts, line charts and pie charts.

![flot](images/flot.png)

Figure 8\. A line chart created with Flot

In 2009 [Highcharts](https://www.highcharts.com) and [Protovis](https://mbostock.github.io/protovis/) were launched. Highcharts is still one of the leading JavaScript charting libraries (and is free for non-commercial use) and provides standard charts. Protovis took a different approach. Rather than providing standard charts it provided graphical elements (such as bars, lines and dots) with which you can encode your data. You can combine these elements to create custom charts. Protovis was led by Mike Bostock and Jeff Heer who went on to create D3.js.

![protovis](images/protovis.png)

Figure 9\. Custom chart created with Protovis

* * *

In the mid-2000s Adobe’s Flash was the dominant platform for creating rich interactive applications for the web. Its popularity declined towards the end of the 2000s as web standards such as SVG and Canvas started to be supported by the major browsers.

2011 saw the launch of [D3.js](https://d3js.org/) which embraced the growing support for the SVG web standard. Like Protovis it provides building blocks for making charts and it became the dominant JavaScript library for creating custom visualisations.

In 2014 [Chart.js](https://www.chartjs.org/) launched and is currently one of the leading free and open-source standard charting libraries.

### 2.2.3\. JavaScript and Data Visualisation today

The most popular data visualisation projects on Github are currently D3.js (105,000 stars) and Chart.js (60,300 stars). My personal opinion is that D3.js and Chart.js are able to cover most visualisation cases. In general I recommend using Chart.js for standard charts (bar, line, pie and scatter) and D3.js for custom visualisations.

* * *

## 2.3\. Creating a Web Application with JavaScript

This section shows how to create a JavaScript web application. It starts by showing the fundamental components of a web application then introduces the tool Vite which helps you join all the pieces together.

Fundamentally a web application consists of HTML, CSS and JavaScript. This is true whether the application is a simple website or a fully featured e-commerce store or social media platform. If you’re not familiar with HTML, CSS or JavaScript I recommend finding a tutorial on the web such as [this tutorial at mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web) or reading my book [Fundamentals of HTML, SVG, CSS and JavaScript for Data Visualisation](https://leanpub.com/html-svg-css-js-for-data-visualisation).

### 2.3.1\. HTML

HTML (Hypertext Markup Language) describes the static content of the application. Typically this is content that is always visible on the webpage or container elements for JavaScript generated content (such as charts).

Here’s some sample HTML:

```
<!DOCTYPE html>
<html lang="en">
<head>...</head>
<body>
  <h1>My app</h1> ①
  <div id="menu"></div>
  <div class="content">
    <div id="chart"></div> ②
  </div>
</body>
</html>
```

1.  *①* Some static content
2.  *②* A container element for a chart that’ll be generated by JavaScript

* * *

### 2.3.2\. CSS

CSS (Cascading Style Sheets) describes the layout and style of the app. For example:

```
body {
  background-color: #eee;
}

h1 {
  color: blue;
}

.content {
  padding: 1rem;
}

...
```

### 2.3.3\. JavaScript

JavaScript code manages interaction and dynamic content. Dynamic content is content that’s generated after the web page has loaded. It augments the static content in the main HTML file.

Here’s a basic example that populates the `<div id="chart">` container element in the HTML file with a Chart.js chart (there’s no need to understand this code at this stage):

```
let chart = new Chart('chart', {
  type: 'bar',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [10, 20, 30]
      }
    ]
  }
});
```

This code results in Chart.js drawing a bar chart inside the `<div id="chart">` element.

If these HTML, CSS or JavaScript snippets look totally alien to you I recommend getting up to speed using [Fundamentals of HTML, SVG, CSS and JavaScript for Data Visualisation](https://leanpub.com/html-svg-css-js-for-data-visualisation).

### 2.3.4\. Joining the pieces

It’s possible to link to each a project’s CSS and JavaScript files using `link` and `script` tags in the HTML file but the usual approach (especially with medium and large projects) is to use a **bundler**. A bundler is a tool that combines multiple JavaScript files into a single bundle.

One of the main advantages is your JavaScript can be modularised meaning that you can split your application into smaller files, each of which has a single purpose. This makes your application code much easier to understand and navigate.

There’s several bundlers available such as [Webpack](https://webpack.js.org/), [Rollup](https://rollupjs.org/), [Parcel](https://parceljs.org/) and [Vite](https://vitejs.dev/). In this book we use Vite because:

*   you can create a project with minimal configuration
*   it has a built-in web-server for when you’re developing your application
*   it’s fast
*   its web-server serves static files (which is useful for loading in CSV and JSON files)

In general I recommend using Vite for any size web application.

All of the projects in this book are created using Vite. Creating a project with Vite is relatively straightforward but there’s no need to do this yourself for the purposes of this book. However if you’d like to know how to create a project with Vite refer to Appendix A.

* * *

### 2.3.5\. Example web application

Our first project loads the REPD data, filters it then displays it as a list:

![load data](images/load-data.png)

To run the project, open your command line and navigate to `load-data` of the code download. Type `npm install` to download the project dependencies then `npm run dev` to start the project’s web server:

```
cd load-data
npm install
npm run dev
```

When `npm run dev` is run the command line will respond with a message containing a URL to visit (usually [`http://localhost:5173/`](http://localhost:5173/)). Copy the URL and paste in your browser and you should see the list of battery planning applications from the REPD data (see previous figure).

#### Project overview

The project has the following file structure:

```
load-data/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

Listing 2\. load-data project files

The main files are `index.html`, `main.js`, `style.css` and `repd.json`. This project has lots in common with the other projects in this book so it’s worth getting to know this project well. I recommend viewing this project in your favourite code editor (e.g. VS Code).

* * *

Here’s a brief description of the files:

| File | Description |
| --- | --- |
| `index.html` | The main HTML file. This contains static content and container elements for JavaScript generated content |
| `main.js` | The main JavaScript file. This loads the REPD data, filters it and constructs a list. |
| `node_modules` | Directory containing 3rd party modules (such as Chart.js or D3). This is a standard directory that’s created by `npm install`. You don’t usually need to concern yourself with this directory so we won’t pay it any more attention. |
| `package-lock.json` | File created by `npm install` which logs the exact versions of the installed 3rd party modules. You don’t usually need to concern yourself with this file so we won’t pay it any more attention. |
| `package.json` | File created by `npm init` that contains the project configuration. For example it lists the installed 3rd party modules (such as Chart.js and D3). You don’t usually need to concern yourself with this file so we won’t pay it any more attention. |
| `public` | Directory that acts as the server root directory. You can put static files (such as CSV files) here which the application can request. |
| `style.css` | The main CSS file. |

`load-data` is a project that’s derived from Vite’s default counter project (see Appendix A). Let’s examine the files in more detail.

* * *

##### index.html

This is the main HTML file and is the first file that’s loaded by the web browser when the site loads. Most of this file is the same as the Vite’s default HTML file. Generally speaking the only changes we make to `index.html` in this book are:

*   changing the content of `<title>`
*   adding, removing or modifying HTML in the `<body>` section.

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>REPD battery applications</title> ①
  </head>
  <body>
    <div id="output"></div> ②
    <script type="module" src="/main.js"></script> ③
  </body>
</html>
```

Listing 3\. index.html

1.  *①* The title that appears in the browser’s tab is set using a `<title>` tag.
2.  *②* The `<div>` element that acts as a container for the list. We populate this element in `main.js`.
3.  *③* The main JavaScript file `main.js` is included using a `<script>` tag. This line is generated by Vite and in general we don’t need to touch it.

* * *

##### main.js

`main.js` is the only JavaScript file in this project. It loads the data and generates a list. To load the data it uses a JavaScript promise which is a fairly advanced technique. If you’re not familiar with promises don’t worry about them too much as they’re only used to load the data and this code is largely the same throughout the book.

Here’s an outline of `main.js`:

```
import './style.css'; ①

function makeList(data) { ... }

fetch('./repd.json') ②
  .then(res => res.json()) ③
  .then(data => makeList(data)); ④
```

Listing 4\. main.js

1.  *①* Import `style.css`. This is non-standard JavaScript (you can’t import CSS files in standard JavaScript) but is supported by Vite. We’ll see later that this approach is handy for keeping CSS files alongside related JavaScript files.
2.  *②* When `main.js` runs the first command to execute is `fetch`. This requests the file `./repd.json` and returns a **promise**. A promise is an object that represents an operation (such as a data request) that will complete at some time in the future (typically this is a few hundred milliseconds in the future).
3.  *③* Call the promise’s `then` method and pass in a **callback** function that runs when the promise fulfils. (The promise is said to be fulfilled when the data has arrived.) The callback function’s first parameter `res` is an object that represents the response. We call its `json` method which converts the data into a JavaScript array and returns a new promise.
4.  *④* Call the second promise’s `then` method and pass in another callback function. This function’s first parameter `data` is the array of data. In the function body call `makeList` and pass the array in.

Don’t worry too much about the detail of this code as JavaScript promises are quite an advanced concept and it can take a while to understand them. Basically this code requests data from a URL, converts the file content into an array and calls a function that renders the data. This is pretty standard code and remains fairly similar throughout this book.

* * *

* * *

The array that’s passed into `makeList` contains the REPD data:

```
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

Listing 5\. First few items in the JSON file (data/repd.json)

* * *

Now let’s look at the `makeList` function which filters the data (using JavaScript’s built in [`filter`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) method), constructs a list and displays it:

```
function makeList(data) {
  // Filter
  data = data.filter(d => d.technology === "Battery" && d.capacity > 100); ①

  // Build a list from the data
  let list = ''; ②
  data.forEach(d => { ③
    list += '<div>' + d.name + ' (' + d.region + ') ' + d.capacity + 'MW</div>'; ④
  });

  document.querySelector('#output').innerHTML = list; ⑤
}
```

Listing 6\. main.js

1.  *①* Use JavaScript’s built-in [array filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) method to filter the data for Battery applications where the capacity is over 100.
2.  *②* Initialise a variable named `list` and assign an empty string to it.
3.  *③* Iterate through each element of `data`.
4.  *④* Append a `div` element to `list` containing the name, region and capacity. (The `+=` operator is shorthand for `list = list + '<div>' + …​`.)
5.  *⑤* Select the `<div id="output">` element defined in `index.html` and set its content to `list`. The browser will parse the string and create the necessary `div` elements to reflect the string `list`.

##### style.css

`style.css` contains typography settings that were retained from Vite’s default `style.css` file. (`style.css` is imported at the top of `main.js`.)

```
body {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
  font-size: 16px;
  line-height: 24px;
  font-weight: 400;
}
```

* * *

## 2.4\. Wrapping up

This chapter discussed the role of JavaScript when visualising data. It presented an overview of JavaScript charting libraries and divided them into two categories: those that provide a selection of standard charts and those that provide more flexibility at the cost of a steeper learning curve.

We also looked at a simple project built using Vite. The project loads the REPD data and presents a subset of it as a list. This forms the foundation for the remaining content in this book.

## 2.5\. Ideas for further study

I recommend playing around with the project by exploring, modifying and adding code. Here are some ideas:

*   display different fields (for example operator or status)
*   change the filter to display a different technology type (or change the capacity threshold)
*   try displaying your own data (make sure the dataset isn’t too large, perhaps don’t go over 10Mb).

Visit the Appendix for solutions.

# 3\. Make a Chart with Chart.js

This chapter introduces the JavaScript charting library [Chart.js](https://www.chartjs.org/). This is one of the most popular free and open source JavaScript charting libraries. It lets you add bar, line, pie and other charts to a web page with relative ease.

![chartjs basic](images/chartjs-basic.png)

Figure 10\. Bar chart created with Chart.js

Although it’s relatively easy to create a chart using Chart.js there’s more to Chart.js than meets the eye. Some of the benefits of Chart.js are:

*   the charts are very stylable. You can set the style of individual elements and adjust the spacing between elements which means you can satisfy most styling requirements.
*   the charts are responsive to device width meaning that the charts work equally well on larger screens and mobile devices.
*   the charts have a built-in tooltip that shows information on data points that are hovered by the mouse (or touched on mobile devices). The tooltip can be configured to show exactly the information that you’d like to show.
*   Chart.js is surprisingly performant. I’ve ran tests where it handles hundreds, if not thousands, of data points with ease (see [Chart.js performance test](https://codepen.io/createwithdata/pen/mvdQjg)).

![chartjs tennis](images/chartjs-tennis.png)

Figure 11\. Example of a styled Chart.js chart ([https://www.createwithdata.com/chartjs-and-csv/](https://www.createwithdata.com/chartjs-and-csv/))

This chapter shows how to create a simple bar chart using Chart.js. We load the REPD data, perform some data basic analysis and create a bar chart to display the result.

We also use the [tidy.js](https://pbeshai.github.io/tidy/) JavaScript library which facilitates common data processing operations such as filtering, sorting and aggregation. We use tidy.js to aggregate the REPD data before visualising it.

* * *

## 3.1\. Introducing Chart.js

Chart.js is a free, open-source JavaScript library that draws bar, line, scatter, pie and radar charts. It produces attractive charts and is reliable, performant, relatively easy to use, well documented and well supported. This book uses version 4 of Chart.js.

This section starts by showing how to make a chart with Chart.js. Following this an example that uses tidy.js and Chart.js to visualise the REPD data is presented.

### 3.1.1\. Making a chart

There are three steps to creating a chart with Chart.js:

*   include Chart.js in your project
*   create an HTML element to contain your chart
*   create a new Chart using Chart.js’s constructor function

#### Including Chart.js in your project

If you’re using a bundler such as Webpack, Parcel or Vite, Chart.js is installed using:

```
cd your-project
npm install chart.js
```

#### Creating a container for a chart

Each chart requires a `<canvas>` element (a `<canvas>` element is a rectangular area on which you can draw shapes using JavaScript):

```
<body>
  ...
  <canvas id="chart"></canvas> ①
  ...
</body>
```

1.  *①* The `<canvas>` element needs an `id` attribute so you can reference it in your JavaScript code.

* * *

#### Creating the chart

Each JavaScript file that uses Chart.js must import the library at the top of the file:

```
import Chart from 'chart.js/auto';

...
```

Chart.js provides a constructor function named `Chart`. To create a chart call `Chart` using the `new` operator and pass in:

*   the id of the Canvas element
*   a chart configuration object.

```
let chart = new Chart('chart', { ①
  type: 'bar', ②
  data: { ③
    labels: ['A', 'B', 'C'], ④
    datasets: [ ⑤
      {
        data: [10, 20, 30] ⑥
      }
    ]
  }
});
```

Listing 7\. Creating a bar chart with Chart.js

1.  *①* The constructor function `Chart` draws the chart and returns an object that represents the chart (which we assign to the `chart` variable). The first argument is the id of the `<canvas>` container element. The second argument is an object that configures the chart.
2.  *②* The configuration object must include two properties `type` and `data`. The `type` property defines the chart type (see later).
3.  *③* The `data` property describes the chart’s data. For bar and line charts two properties `labels` and `datasets` are required.
4.  *④* `labels` defines the axis labels of each bar (or each line point in the case of line charts).
5.  *⑤* `datasets` describes the data values and is an array of objects.
6.  *⑥* Each object in `datasets` represents a data series and must contain a property named `data` whose value is an array of numbers. This is the data itself and determines the length of each bar.

![chartjs single series](images/chartjs-single-series.png)

Figure 12\. A bar chart created with Chart.js

If `datasets` contains a single series (as in our example) we get a normal bar chart where each label corresponds to a single bar. If `datasets` contains more than one series we get a grouped bar chart where each label corresponds to multiple bars.

* * *

### 3.1.2\. Chart configuration

Chart.js charts can be configured in many ways. We won’t cover all the possible options but will cover some of the more useful ones.

#### Chart type

The configuration object’s `type` property can be `'bar'`, `'line'`, `'scatter'`, `'bubble'`, `'pie'`, `'doughnut'`, `'polarArea'` or `'radar'`.

`'bar'` is used for bar charts, `'line'` for line charts and `'scatter'` for scatter plots. `'bubble'` is for scatter plots where the radius of each circle is used to represent an additional variable. `'pie'` is for pie charts and `'doughnut'` is for pie charts with a hole in the center. `'polarArea'` is similar to a bar chart except the bars fit inside a circle. `'radar'` is for radar charts which are similar to line charts but transformed to fit inside a circle.

For `'bar'`, `'line'`, `'pie'`, `'doughnut'`, `'polarArea'` and `'radar'` types the `datasets` property uses a similar structure. Each series object in `datasets` has a `data` property which is an array of numbers:

```
let chart = new Chart('chart', {
  type: 'bar', // bar, line, pie, doughnut, polarArea or radar
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [10, 20, 30]
      }
    ]
  }
});
```

For `scatter` charts each series object has a `data` property which is an array of objects where each object has `x` and `y` properties:

```
let chart = new Chart('chart', {
  type: 'scatter',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [
          {x: 10, y: 50},
          {x: 30, y: 10},
          {x: 50, y: 20}
        ]
      }
    ]
  }
});
```

For `bubble` charts each series object has a `data` property which is an array of objects where each object has `x`, `y` and `r` properties:

```
let chart = new Chart('chart', {
  type: 'bubble',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [
          {x: 10, y: 50, r: 20},
          {x: 30, y: 10, r: 30},
          {x: 50, y: 20, r: 70}
        ]
      }
    ]
  }
});
```

* * *

#### Multi-series charts

If `datasets` has more than one series a multi-series chart is created. For bar charts this means a grouped bar chart and for line charts a multi-line chart.

You can also name a series using the `label` property and colour a series using the `backgroundColor` property:

```
let chart = new Chart('chart', {
  type: 'bar',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        label: 'My series 1',
        backgroundColor: '#2E86AB', // blue
        data: [10, 20, 30]
      },
      {
        label: 'My series 2',
        backgroundColor: '#F18F01', // orange
        data: [15, 40, 20]
      }
    ]
  }
})
```

![chartjs multi series options](images/chartjs-multi-series-options.png)

Figure 13\. Multi-series (or grouped) bar chart

* * *

#### Chart options

The chart configuration object has an optional property `options` for additional configuration. The `options` object has lots of properties, all of which are optional. We cover some of the more useful ones in this book.

Broadly speaking there are options that affect:

*   the whole chart
*   the x and y axes
*   other components such as the title and legend.

Chart.js treats some components, namely the title and legend, as plugins which is why they appear under the `plugins` property.

* * *

Let’s look at an options object containing the options I often use:

```
let chart = new Chart('chart', {
  type: 'bar',
  data: { ... },
  options: {
    maintainAspectRatio: false, ①
    indexAxis: 'x', ②
    scales: { ③
      x: { ④
        title: { ⑤
          display: true,
          text: 'My x-axis title',
          color: '#333',
          font: {
            size: 12
          }
        },
        ticks: {
          color: '#aaa'
        },
        grid: {
          color: '#aaa'
        },
        stacked: false ⑥
      },
      y: {...}
    },
    plugins: { ⑦
      title: { ⑧
        display: true,
        text: 'My chart title',
        color: '#333',
        font: {
          size: 12
        }
      },
      legend: { ⑨
        display: true,
        position: 'top'
      }
    }
  }
});
```

Listing 8\. Chart.js options object

Each of these options is optional so if you’re happy with an option’s default value there’s no need to set it. We sometimes refer to an option by its full path relative to the configuration object. For example, the legend’s `display` option can be referenced using `options.plugins.legend.display`. This is consistent with Chart.js’s documentation.

1.  *①* `options.maintainAspectRatio` determines whether the chart’s aspect ratio is fixed regardless of chart width. It’s default is `true` but I often set this to `false` in order to create a fixed-height chart whose width adapts to the device width.
2.  *②* `options.indexAxis` specifies which axis the labels are on. Its default value is `'x'`. If it’s set to `'y'` the labels appear along the y axis and if type is `'bar'` you’ll get a horizontal bar chart.
3.  *③* `options.scales` accepts an object with two optional properties `x` and `y`. `options.scales.x` configures the x axis and `options.scales.y` configures the y axis.
4.  *④* Each axis configuration object has a number of optional properties. `title` configures the x-axis title, `ticks` configures the x-axis tick marks and `grid` configures the axis grid lines. The grid lines of an axis are the feint lines that extend from the axis ticks to the opposite side of the chart. `stacked` determines whether a multi-series bar chart should be stacked rather than grouped.
5.  *⑤* The `title` property has a number of optional properties including `display` (determines whether the title is visible), `text` (the title text), `color` (the title colour) and `font` (an object that configures the title font). The title’s `font` property has several optional properties including `family` (for the font family), `size` (the font size in pixels), `weight` (for the font weight) and `lineHeight` for the text line height. These properties are similar to CSS properties. See [https://www.chartjs.org/docs/latest/general/fonts.html](https://www.chartjs.org/docs/latest/general/fonts.html) for more detail.
6.  *⑥* For stacked bar charts set both `scales.x.stacked` and `scales.y.stacked` to `true`. For more information on axis options see [https://www.chartjs.org/docs/latest/axes/cartesian/](https://www.chartjs.org/docs/latest/axes/cartesian/).
7.  *⑦* `options.plugins` contains options for any installed plugins. Chart.js treats the chart title and legend as plugins.
8.  *⑧* `options.plugins.title` configures the chart title. It has the similar configuration to `options.scales.x.title`. See [https://www.chartjs.org/docs/latest/configuration/title.html](https://www.chartjs.org/docs/latest/configuration/title.html) for more detail.
9.  *⑨* `options.plugins.legend` configures the chart legend. Two of the most useful properties are `display` (determines if the legend is visible) and `position` (determines the legend position and can be set to `'top'`, `'bottom'`, `'left'` or `'right'`). For more detail on legend options visit [https://www.chartjs.org/docs/latest/configuration/legend.html](https://www.chartjs.org/docs/latest/configuration/legend.html).

* * *

## 3.2\. tidy.js

[tidy.js](https://pbeshai.github.io/tidy/) is one of my favourite JavaScript libraries. It’s a JavaScript data transformation library that lets you reshape your data with relative ease. (It’s inspired by R’s dplyr library so it should feel familiar if you’re from the R community.) It also lets you perform basic data analysis. It has a really well designed API so is a pleasure to use.

Some things that tidy.js can do are filtering, sorting, renaming columns, deriving new columns, summarising data, joins and pivoting. It can be used in a web application or in server-side code. We use it later to summarise the REPD data prior to creating a bar chart.

### 3.2.1\. Including tidy.js in your project

If you’re using a bundler such as Webpack, Parcel or Vite install tidy.js using:

```
npm install @tidyjs/tidy
```

To use any of tidy.js’s function’s within a JavaScript file use `import` to import each function. Here we import `tidy`, `filter` and `count`:

```
import { tidy, filter, count } from '@tidyjs/tidy';
```

### 3.2.2\. Tidy data

A common convention used in the data community is 'tidy data'. This is where a table of data is structured such that:

*   every column is a variable (e.g. name, technology, capacity)
*   every row is an item (e.g. a planning application)

This is also known as 'long format' (rather than 'wide format') and is the format required by tidy.js.

In the JavaScript world, tidy data is represented by an array of objects where each object represents a single item (e.g. a planning application). Each object has properties representing the variables (e.g. name, technology and capacity).

* * *

For example:

```
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

An example of non-tidy (or 'wide format') data is where a data table has column headers containing years (e.g. 2000, 2001, 2002 etc.):

| Category | 2020 | 2021 | 2022 |
| --- | --- | --- | --- |
| Food | 1234 | 1343 | 1542 |
| Clothes | 431 | 522 | 467 |

2020, 2021 and 2022 aren’t variables. They’re actually values of the variable 'year'. Furthermore each row represents 3 observations rather than a single observation.

A tidy (or 'long format') version of this data is:

| Category | Year | Amount |
| --- | --- | --- |
| Food | 2020 | 1234 |
| Food | 2021 | 1343 |
| Food | 2022 | 1542 |
| Clothes | 2020 | 431 |
| Clothes | 2021 | 522 |
| Clothes | 2022 | 467 |

Now each column is a variable and each row is a single observation (for example the first row is an observation that in 2020 the food category’s amount was 1234).

* * *

### 3.2.3\. How to use tidy.js

To process data using tidy.js call the function `tidy` and pass in a data array as the first argument. The array needs to be in tidy format, so each observation is represented by a single array element.

The processing operations (such as `filter`, `sort`, `rename` and `count`) are passed to `tidy` as additional arguments. For example let’s filter the REPD data (`data`) by status then count the number of applications for each technology:

```
import { tidy, filter, count } from '@tidyjs/tidy';

let summary = tidy(
  data,
  filter(d => d.status === 'Operational'),
  count('technology')
);
```

The `tidy` function returns a new array. In this case, it’s a summary array:

```
[
  {
    "technology": "Biomass (co-firing)",
    "n": 3
  },
  {
    "technology": "EfW Incineration",
    "n": 56
  },
  {
    "technology": "Biomass (dedicated)",
    "n": 78
  },
  {
    "technology": "Advanced Conversion Technologies",
    "n": 18
  },
  ...
]
```

It’s important to understand that tidy creates a new array (it doesn’t modify the original array).

* * *

### 3.2.4\. Common tidy.js operations

tidy.js has a large number of functions that carry out various data processing or analysis tasks. The ones used in this book are: `filter`, `rename`, `mutate`, `sort`, `count` and `groupBy`.

#### filter

The `filter` function filters the data according to a function that’s passed in. It’s similar to JavaScript’s array method `filter`.

Here’s a couple of examples:

```
import { tidy, filter } from '@tidyjs/tidy';

// Get all operational applications:
tidy(
  data,
  filter(d => d.status === 'Operational')
)

// Get applications with a capacity greater than 100:
tidy(
  data,
  filter(d => d.capacity > 100)
)
```

* * *

#### rename

`rename` renames a property in each item of the array. (In tabular terms this is equivalent to renaming a column.) You pass in an object where each property’s key is the current name and each value is the new name.

The following example renames the `'status'` property to `'Application status'`:

```
import { tidy, rename } from '@tidyjs/tidy';

tidy(
  data,
  rename({status: 'Application status'})
);

returns:
[
  {
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "Application status": "Operational", ①
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  ...
]
```

1.  *①* `'status'` has been renamed to `'Application status'`.

* * *

#### mutate

The `mutate` function creates a new property for each item of the array. (In tabular terms, this is equivalent to adding a new column.) You pass in an object where each property name defines a new data property and each value is a function that returns the value of the new data property.

Here’s a couple of examples:

```
import { tidy, mutate } from '@tidyjs/tidy';

// Add a new field isHighCapacity
tidy(
  data,
  mutate({
    isHighCapacity: d => d.capacity > 1000
  })
);

// Convert the dateSubmitted string into a date object
tidy(
  data,
  mutate({
    dateSubmitted: d => new Date(d.dateSubmitted)
  })
);
```

The first example adds a new property `isHighCapacity` which is `true` if the capacity is over 1000\. The second example converts the `dateSubmitted` string into a date object. `dateSubmitted` already exists as a data property so tidy overwrites the existing value (the date string) with the new value (the date object).

* * *

#### sort

The `sort` function sorts the data by a given property name. By default it sorts in ascending order. To sort in descending order wrap the property name with tidy’s `desc` function. You can sort by more than one property by passing in an array of property names.

Here’s a couple of examples:

```
import { tidy, sort, desc } from '@tidyjs/tidy';

// Sort by capacity (ascending)
tidy(
  data,
  sort('capacity')
)

// Sort by capacity (descending)
tidy(
  data,
  sort(desc('capacity'))
)
```

* * *

#### count

The `count` function is an aggregation operation that groups the data according to the specified property and computes the size of each group. It reaturns an array of objects where each object has the group name and a property `n` for the count.

To sort the result in descending order pass an object `{sort: true}` as the second argument.

```
import { tidy, count } from '@tidyjs/tidy';

// Count the number of applications of each technology
tidy(
  data,
  count('technology', {sort: true})
)

// returns:
[
  {
    "technology": "Solar Photovoltaics",
    "n": 2630
  },
  {
    "technology": "Wind Onshore",
    "n": 2241
  },
  {
    "technology": "Battery",
    "n": 623
  },
  ...
]
```

We use `count` later to create a summary bar chart of the REPD data.

* * *

#### groupBy

The `groupBy` function groups the data by a given property and performs operations on the groups. This is useful for performing aggregation operations such as sum, mean, median, min and max over the dataset.

For example, you can compute the count and average (mean) capacity for each technology type:

```
import { tidy, groupBy, n, mean, desc } from '@tidyjs/tidy';

// Group by technology and count the number of applications and the mean capacity in each group
tidy(
  data,
  groupBy('technology', [
    summarize({
      count: n(),
      meanCapacity: mean('capacity')
    })
  ]),
  sort(desc('meanCapacity'))
)

returns:
[
  {
    "technology": "Pumped Storage Hydroelectricity",
    "count": 10,
    "meanCapacity": 573.78
  },
  {
    "technology": "Wind Offshore",
    "count": 74,
    "meanCapacity": 456.25479452054793
  },
  {
    "technology": "Flywheels",
    "count": 1,
    "meanCapacity": 400
  },
  ...
]
```

The first argument of `groupBy` is the property name you want to group by. The second argument is an array of tidy.js functions. Usually this array just has a single call to tidy’s `summarize` function.

`summarize` accepts an object whose property names (`count` and `meanCapacity` in our example) are properties that’ll be added to each group in the result array. The property values are tidy.js summary functions such as `n`, `min`, `max`, `mean`, `median` and `deviation`. Each summary function is called on each group and the return value is written to the result array.

Thus in the example above, the 'Pumped Storage Hydroelectricity' group has 10 members and a mean capacity of 573.78.

### 3.2.5\. tidy.js examples

`tidyjs-examples` is a Vite project that demonstrates tidy.js. It loads the REPD data, performs a tidy.js transformation and displays the result in the browser.

To run:

```
# Make sure you're in the visualising-data-with-js-code directory

cd tidyjs-examples

npm install

npm run dev
```

If you’ve a Vite server running, use `ctrl-c` to stop the server.

There’s a number of individual examples. Uncomment the one you’d like to try (and make sure the others are commented out).

* * *

## 3.3\. Chart.js example application

In this section we look at an application that loads the REPD data, uses tidy.js to summarise the data then visualises the result using Chart.js. This project is built using Vite so follows a similar structure to the `load-data` project.

![chartjs app bar chart](images/chartjs-app-bar-chart.png)

Figure 14\. Bar chart created by chart-js project

To run the project navigate to the `chart-js` project directory and call `npm install`. Call `npm run dev` to start the application server. This gives you a url (usually [http://localhost:5173](http://localhost:5173)) to visit. You should see a bar chart when you visit this URL.

```
cd chart-js

npm install

npm run dev
```

* * *

### 3.3.1\. File structure

The project directory looks like:

```
chart-js/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

Listing 9\. chart-js project files

The project was built using Vite so has the standard Vite file structure. The REPD data is in the `public` directory. All our JavaScript code is in `main.js`.

The main project files are `index.html`, `main.js` and the data `public/repd.json`. Let’s look at the first two.

### 3.3.2\. index.html

Here’s the main HTML file `index.html`:

```
<!DOCTYPE html>
<html lang="en">
  <head>
  <meta charset="UTF-8" />
  <link rel="icon" type="image/svg+xml" href="#" />
  <meta name="viewport" content="..." />
  <title>Vite App</title>
  </head>
  <body>
  <canvas id="chart"></canvas> ①
  <script type="module" src="/main.js"></script>
  </body>
</html>
```

Listing 10\. chart-js/index.html

1.  *①* The only change from the `index.html` that Vite generates is the inclusion of a `<canvas>` element for the chart.

* * *

### 3.3.3\. main.js

Here’s the main JavaScript file:

```
import { tidy, count } from '@tidyjs/tidy';
import Chart from 'chart.js/auto';

function draw(data) {
  let summary = tidy(
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n)
      }]
    },
    options: {
      plugins: { ... }
    }
  });
}

fetch('./repd.json') ①
  .then(res => res.json())
  .then(data => draw(data));
```

Listing 11\. chart-js/main.js

1.  *①* The REPD data is requested using `fetch` and when it loads it’s converted to an array of objects and sent to the `draw` function. This is similar to the code used to load data in the `load-data` project.

* * *

Let’s step through `draw`:

```
function draw(data) {
  let summary = tidy(
    data,
    count('technology', {sort: true})
  );

  ...
}
```

Listing 12\. chart-js/main.js

`draw` starts by creating a summary array of the data. `summary` looks something like:

```
[
  {
    "technology": "Solar Photovoltaics",
    "n": 3593
  },
  {
    "technology": "Wind Onshore",
    "n": 2196
  },
  {
    "technology": "Battery",
    "n": 948
  },
  ...
]
```

* * *

Next a Chart.js chart is created:

```
function draw(data) {
  ...

  const myChart = new Chart('chart', { ①
    type: 'bar', ②
    data: {
      labels: summary.map(d => d.technology), ③
      datasets: [{
        data: summary.map(d => d.n) ④
      }]
    },
    options: { ... }
  });
}
```

Listing 13\. chart-js/main.js

1.  *①* Create a chart by calling Chart.js’s constructor function and passing in the id of the chart’s `<canvas>` element.
2.  *②* The `type` property of the configuration object is set to `bar`.
3.  *③* The `labels` array is generated by using the `map` method to extract the `technology` property from `summary`. This generates an array of technology names `["Solar Photovoltaics", "Wind Onshore", "Battery", …​]`.
4.  *④* Likewise the `data` array is generated by using the `map` method to extract the `n` property from `summary`. This generates an array of counts `[3593, 2196, 948, …​]`.

* * *

Now let’s look at the `options` object:

```
function draw(data) {
  ...

  const myChart = new Chart('chart', {
    type: 'bar',
    data: { ... },
    options: {
      plugins: {
        title: {
          display: true, ①
          text: 'Number of planning submissions (by technology) 1990-2022', ②
          font: {
            size: 18 ③
          }
        },
        legend: {
          display: false ④
        }
      }
    }
  });
}
```

Listing 14\. chart-js/main.js

1.  *①* Make the chart title visible.
2.  *②* Set the chart title.
3.  *③* Set the font size of the chart title.
4.  *④* Hide the legend.

* * *

This example creates the following bar chart:

![chartjs app bar chart](images/chartjs-app-bar-chart.png)

Figure 15\. Bar chart created by chart-js project

## 3.4\. Wrapping up

This chapter introduced Chart.js and tidy.js. We looked at how a simple bar chart is created using Chart.js and how to transform data using tidy.js. We used both libraries to create a summary bar chart.

In the next chapter we cover styling Chart.js charts and how to create multi-series charts.

## 3.5\. Ideas for further study

I recommend playing around with the project by exploring, modifying and adding code. Here are some ideas:

*   show the number of applications per region (instead of technology)
*   sort the bars alphabetically
*   change the bar colour to `'steelblue'`.

Visit the Appendix for solutions.

# 4\. Styling and Customising Chart.js

In this chapter I show:

*   how to style Chart.js charts
*   how to create a Chart.js chart with a dark theme
*   how to create multi-line charts from long format data
*   how to create stacked bar charts from long format data

![chartjs styled 1](images/chartjs-styled-1.png)

Figure 16\. Styled Chart.js bar chart

![chartjs styled 2](images/chartjs-styled-2.png)

Figure 17\. Dark theme Chart.js bar chart

![chartjs styled 3](images/chartjs-styled-3.png)

Figure 18\. Multi-line chart

![chartjs styled 4](images/chartjs-styled-4.png)

Figure 19\. Stacked bar chart

This knowledge is used later in the Data Stories chapter.

* * *

## 4.1\. The project

The `chartjs-various` project contains this chapter’s examples.

To run the project navigate to `chartjs-various` and call `npm install`. Then call `npm run dev` to start the application server. This gives you a URL to visit.

```
cd chartjs-various

npm install

npm run dev
```

When you visit the provided URL (usually [`http://localhost:5173`](http://localhost:5173)) you should see a page containing all four charts.

This project uses `tidy.js` and `Chart.js`. It also uses `lodash` which is a JavaScript library that provides a large number of helper functions for processing arrays and objects. We use its `uniq` method that takes an array and returns a copy of the array with duplicates removed.

### 4.1.1\. File structure

The project directory looks like:

```
chartjs-various/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

Listing 15\. chartjs-various project files

The project was built using Vite so has the standard Vite file structure. The main project files are `index.html`, `main.js`, `style.css` and the data `public/repd.json`.

### 4.1.2\. index.html

The main HTML file is `index.html`:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="#" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite App</title>
  </head>
  <body>
    <div class="chart-wrapper"> ①
      <canvas id="chart-1"></canvas> ②
    </div>
    <div class="chart-wrapper dark"> ①
      <canvas id="chart-2"></canvas> ③
    </div>
    <div class="chart-wrapper"> ①
      <canvas id="chart-3"></canvas> ④
      </div>
    <div class="chart-wrapper"> ①
      <canvas id="chart-4"></canvas> ⑤
    </div>
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

Listing 16\. chartjs-various/index.html

1.  *①* Each `<canvas>` element is placed inside a wrapper to help size the chart.
2.  *②* `<canvas>` element for the styled bar chart.
3.  *③* `<canvas>` element for the dark theme chart.
4.  *④* `<canvas>` element for the multi-line chart.
5.  *⑤* `<canvas>` element for the stacked bar chart.

Each chart has its own `<canvas>` element with a unique id.

To control the size of a Chart.js chart the recommended approach is to wrap the chart’s `<canvas>` element with a `<div>` element and to size the `<div>` element ([see documentation](https://www.chartjs.org/docs/latest/configuration/responsive.html#important-note)). You also need to set the chart’s `maintainAspectRatio` option to `false` so that the chart can adapt to both width and height of the wrapper.

In this project we add a class name of `chart-wrapper` to each `<div>` wrapper so that it can be styled in `style.css`.

### 4.1.3\. style.css

`style.css` mostly contains rules for styling and sizing the chart wrapper elements:

```
body {
  margin: 0; ①
}

.chart-wrapper {
  height: 600px; ②
  background-color: #F9F7EB; ③
  padding: 2rem; ④
}

.chart-wrapper.dark {
  background-color: #222; ⑤
}
```

Listing 17\. chartjs-various/style.css

1.  *①* Remove the default margin around the whole page.
2.  *②* The chart wrapper height is set to 600px so that the charts have a fixed height. The chart wrapper width (which we haven’t set) will be 100% which is the default width for a `<div>` element. This means each chart will span the full width of the page and be 600px high. (It’s important that we set the Chart.js `maintainAspectRatio` option to `false` so that the each chart can fill its wrapper vertically and horizontally.)
3.  *③* Each chart wrapper’s background colour is set to off-white.
4.  *④* We also add some padding between the wrapper border and the chart.
5.  *⑤* If the wrapper has a `dark` class attribute set the background colour to dark grey.

* * *

### 4.1.4. main.js

`main.js` is quite long so let’s start with an outline:

```
import { tidy, count, filter } from '@tidyjs/tidy';
import Chart from 'chart.js/auto';
import uniq from 'lodash-es/uniq';

import './style.css';

Chart.defaults.plugins.legend.display = false; ④
Chart.defaults.scale.title.font = {size: 14};
Chart.defaults.plugins.title.display = true;
Chart.defaults.plugins.title.font.size = 18;
Chart.defaults.maintainAspectRatio = false;

const technologyPalette = { ⑤
  'Advanced Conversion Technologies': '#FF9999',
  'Anaerobic Digestion': '#C58882',
  'Battery': '#B6A6CA',
  ...
};

function getMultiSeriesChartData(data, seriesProp, labelProp) { ... } ③

function drawChart1(data) { ... }
function drawChart2(data) { ... }
function drawChart3(data) { ... }
function drawChart4(data) { ... }

function draw(data) { ②
  drawChart1(data);
  drawChart2(data);
  drawChart3(data);
  drawChart4(data);
}

fetch('./repd.json') ①
  .then(res => res.json())
  .then(data => draw(data));
```

Listing 18\. chartjs-various/main.js

1.  *①* `main.js` loads the data in the same manner as `load-data`. When the data arrives call `draw`.
2.  *②* The `draw` function calls the draw functions (such as `drawChart1`) for each of the four charts.
3.  *③* A helper function used by charts 3 and 4 to transform the data into multiple series.
4.  *④* Set Chart.js options that apply to all the charts (see later).
5.  *⑤* `technologyPalette` is a lookup object that defines a colour for each technology type. I used the website [coolors.co](https://coolors.co) to find colours. (I cycle through the different palettes and pick out colours that catch my eye!)

Near the top of `main.js` we set some Chart.js options that apply to all charts. This is done by assigning values to `Chart.defaults.*` where `*` is the path of the option being set. For example to make the chart title visible by default, use:

```
Chart.defaults.plugins.title.display = true;
```

You can still override these options on a particular chart:

```
const myChart = new Chart('chart', {
  type: 'bar',
  data: { ... },
  options: {
    scales: { ... },
    plugins: {
      title: {
        display: false
      }
    }
  }
});
```

We’ll now look at the individual charts.

* * *

## 4.2\. Chart 1 (Styled horizontal bar chart)

Chart 1 is a horizontal bar chart that shows the number of submissions for each technology type. It’s styled with an off-white background, blue/green bars, an x-axis title, no y-axis title and a chart title.

![chartjs styled 1](images/chartjs-styled-1.png)

Figure 20\. Styled Chart.js bar chart

* * *

`drawChart1` is the function that draws this chart:

```
function drawChart1(data) {
  let summary = tidy( ①
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart-1', {
    type: 'bar',
    data: { ②
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n),
        backgroundColor: '#19A0AA' ③
      }]
    },
    options: {
      indexAxis: 'y', ④
      scales: {
        x: {
          title: { ⑤
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of planning applications (by technology) 1990-2022' ⑥
        }
      }
    }
  });
}
```

Listing 19\. chartjs-various/main.js

1.  *①* Create a summary of the data using tidy.js. We count the number of planning applications for each technology.
2.  *②* The chart’s `data` property is defined in a similar manner to the `chart-js` project.
3.  *③* Set the series `backgroundColor` to define the bar colour.
4.  *④* Set `indexAxis` to `y` to make the axis labels appear along the y-axis. This creates a horizontal bar chart.
5.  *⑤* Set the x-axis’s title. Its size is set using `Chart.defaults` at the top of the file.
6.  *⑥* Set the chart title. The title’s visibility and size is set at the top of the file.

* * *

## 4.3\. Chart 2 (Dark theme horizontal bar chart)

Chart 2 is identical to Chart 1 but with a dark theme. The main changes are to make the background dark and the titles, labels and grid lines light.

![chartjs styled 2](images/chartjs-styled-2.png)

Figure 21\. Dark theme Chart.js bar chart

* * *

`drawChart2` is the same as `drawChart1` except for changes to make the labels, ticks and grid lines show up against the dark background.

```
function drawChart2(data) {
  let summary = tidy(...); ①

  const myChart = new Chart('chart-2', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n),
        backgroundColor: '#19A0AA' ②
      }]
    },
    options: { ... } ③
  });
}
```

Listing 20\. chartjs-various/main.js

1.  *①* Summarise the data in the same manner as Chart 1.
2.  *②* The bar colour remains the same as in Chart 1.
3.  *③* The `options` object (see later).

We look at the `options` object on the following page.

* * *

```
{
  indexAxis: 'y',
  scales: {
    x: {
      title: {
        display: true,
        text: 'Number of applications',
        color: '#eee' ①
      },
      ticks: {
        color: '#ccc' ②
      },
      grid: {
        color: '#555' ③
      }
    },
    y: {
      ticks: {
        color: '#ccc' ②
      },
      grid: {
        color: '#333' ③
      }
    }
  },
  plugins: {
    title: {
      text: 'Number of planning applications (by technology) 1990-2022',
      color: '#ccc' ④
    }
  }
}
```

Listing 21\. chartjs-various/main.js

1.  *①* Set the x-axis title to light grey so it shows up against the dark background.
2.  *②* Set the axis ticks to light grey so they show up against the dark background.
3.  *③* Set the grid lines to light grey so they show up against the dark background.
4.  *④* Set the chart title to light grey so it shows up against the dark background.

* * *

## 4.4\. Chart 3 (Multi-line chart)

Chart 3 is a multi-line chart. For each technology type a line shows the number of planning applications over time. The x-axis represents year and the y-axis represents the number of applications.

![chartjs styled 3](images/chartjs-styled-3.png)

Figure 22\. Multi-line chart

The function `drawChart3` draws this chart. The chart itself is similar to previous ones. However the challenge is transforming the REPD data into an array of series.

* * *

We use a helper function `getMultiSeriesChartData` (which is defined near the top of `main.js`) that takes three arguments:

1.  The REPD data array
2.  The data property that defines the names of each series.
3.  The data property that defines the axis labels.

For this chart, where each series is a technology and the x-axis represents year submitted we call:

```
getMultiSeriesChartData(data, 'technology', 'yearSubmitted');
```

This returns an object that looks like:

```
{
  labels: [1990, 1991, 1992, ... 2020, 2021, 2022], ①
  datasets: [ ②
    {
      label: "Advanced Conversion Technologies",
      data: [0, 0, 0, ... 0, 0, 0] ③
    },
    {
      label: "Anaerobic Digestion",
      data: [0, 0, 0, ... 10, 17, 22] ③
    }
    ,
    ...
  ]
}
```

1.  *①* Each value in `labels` represents a name along the main axis.
2.  *②* Each object in `datasets` represents a series for a particular technology type.
3.  *③* The values in the `data` array of a series are the number of planning applications for the given technology type and corresponding year. For instance for Anaerobic Digestion there are 10 planning applications from 2020, 17 from 2021 and 22 from 2022\. If the chart’s type is `line` this data results in a multi-line chart where the years appear along the main axis and each technology type is represented by a line.

* * *

We assign the output of `getMultiSeriesChartData` to `chartData` and use it as the value of the `data` property in the Chart.js configuration object:

```
function drawChart3(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted'); ①

  ...

  const myChart = new Chart('chart-3', {
    type: 'line',
    data: chartData, ②
    options: { ... }
  });

  ...
}
```

Listing 22\. chartjs-various/main.js

1.  *①* Assign the return value of `getMultiSeriesChartData` to `chartData`.
2.  *②* Set the chart’s `data` property to `chartData`.

For the purposes of this book you don’t need to understand `getMultiSeriesChartData` but if you’re interested in seeing how it works visit 'getMultiSeriesChartData' in the Appendices at the back of the book.

* * *

Let’s look at `drawChart3` in its entirety:

```
function drawChart3(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted'); ①

  // Add style to each series
  chartData.datasets.forEach(series => { ②
    let color = technologyPalette[series.label] || '#aaa'; ③
    series.borderColor = color; ④
    series.borderWidth = 1.5; ④
    series.backgroundColor = color; ⑤
    series.radius = 2; ⑥
  });

  const myChart = new Chart('chart-3', { ⑦
    type: 'line', ⑧
    data: chartData, ⑨
    options: { ⑩
      scales: {
        x: {
          title: {
            display: true,
            text: 'Year'
          }
        },
        y: {
          title: {
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of applications (by technology) 1990-2022',
        },
        legend: {
          display: true
        }
      }
    }
  });
}
```

Listing 23\. chartjs-various/main.js

1.  *①* Call `getMultiSeriesChartData` to construct the chart data object. The second argument defines which property is used for series (`'technology'`) and the third argument defines which property is used for the main axis labels (`'yearSubmitted'`).
2.  *②* Iterate through each series in `chartData.datasets` and add style properties so that each line in the chart is coloured according to the technology type.
3.  *③* Use the `technologyPalette` lookup to get the technology’s colour. Fall back to grey if the colour isn’t defined.
4.  *④* `borderColor` sets the line colour and `borderWidth` sets the line width.
5.  *⑤* `backgroundColor` sets the colour of the data point circles.
6.  *⑥* `radius` sets the radius of the data point circles.
7.  *⑦* Call `new Chart()` to construct the chart and pass in the id of the `<canvas>` element and the configuration object.
8.  *⑧* In the configuration object set type to `'line'`.
9.  *⑨* Set the `data` property to the data object `chartData`. This is the object that was created using `getMultiSeriesChartData`.
10.  *⑩* Finally set options for the axis titles, the chart title and the legend.

Each series in `chartData.datasets` is represented by a line in the chart.

![chartjs styled 3](images/chartjs-styled-3.png)

Figure 23\. Multi-line chart

* * *

## 4.5\. Chart 4 (Stacked bar chart)

Chart 4 is a stacked bar chart which shows the number of planning applications for each region. Each bar is subdivided by technology type. This allows the reader to view the distribution of planning applications by technology type for each region. For instance it’s immediately apparent that Scotland has many more wind related applications than any other region.

![chartjs styled 4](images/chartjs-styled-4.png)

Figure 24\. Stacked bar chart

The function `drawChart4` draws this chart and works in a similar way to `drawChart3` but now each data series corresonds to a set of same-color horizontal slices through the bars. For example the series representing Solar Photovoltaics is represented by the yellow slices through each bar.

* * *

As with `drawChart3` it calls `getMultiSeriesChartData` but this time the axis label property is `region`:

```
let chartData = getMultiSeriesChartData(data, 'technology', 'region');
```

This returns the object:

```
{
  labels: ["East Midlands", "Eastern", "London", "North East", "North West", ... ],
  datasets: [
    {
      label: "Advanced Conversion Technologies",
      data: [14, 6, 8, 8, 10, ...]
    },
    {
      label: "Anaerobic Digestion",
      data: [31, 47, 11, 14, 25, ...]
    }
    ,
    ...
  ]
}
```

* * *

```
function drawChart4(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'region'); ①

  // Add colour to each series
  chartData.datasets.forEach(series => { ②
    let color = technologyPalette[series.label] || '#aaa';
    series.backgroundColor = color;
  });

  const myChart = new Chart('chart-4', { ③
    type: 'bar', ④
    data: chartData, ⑤
    options: {
      scales: {
        x: {
          stacked: true, ⑥
        },
        y: {
          stacked: true, ⑥
          title: {
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of applications (by region and technology) 1990-2022',
        },
        legend: {
          display: true
        }
      }
    }
  });
}
```

Listing 24\. chartjs-various/main.js

1.  *①* Call `getMultiSeriesChartData` to construct the chart data object. The second argument defines which property is used for series (`'technology'`) and the third argument defines which property is used for the main axis labels (`'region'`).
2.  *②* Iterate through each series in `chartData.datasets` and add style properties so that each bar slice is coloured according to the technology type. `backgroundColor` sets the colour of a bar slice.
3.  *③* Construct the chart by calling `new Chart()` and passing in the id of the `<canvas>` element and the configuration object.
4.  *④* In the configuration object set the type to `'bar'`.
5.  *⑤* Set the `data` property to the data object `chartData`. This is the object that was created using `getMultiSeriesChartData`.
6.  *⑥* To create a stacked bar chart set the `stacked` property of the x and y scales to `true`. If we leave these at their default value of `false` we get a grouped bar chart.

## 4.6\. Wrapping up

This chapter showed a few ways in which Chart.js charts can be styled. We changed the colour scheme of a simple bar chart to give it a cleaner look and showed how to achieve a dark themed chart.

I also showed how to create multi-line and stacked bar charts and walked through a helper function that transforms an array of data into the multi-series structure required by Chart.js.

This concludes the introduction to Chart.js. I haven’t covered everything there is to know about Chart.js but enough to enable you to create useful and attractive charts. We’ll use this knowledge later in the book when creating data stories.

# 5\. Custom Charts with D3.js

This chapter introduces [D3.js](https://d3js.org) which is a free and open-source JavaScript library. Rather than providing ready made charts D3 provides building blocks for making custom data visualisations.

![d3 timeline](images/d3-timeline.png)

Figure 25\. A custom chart created using D3.js. Each circle represents an REPD planning application

In this chapter I:

*   introduce D3
*   learn about D3’s philosophy
*   learn about D3 selections, joins and scale functions
*   learn about the Tippy.js tooltip module
*   walk through a D3 example that visualises the REPD data

* * *

## 5.1\. Introduction to D3

D3 is a free, open-source JavaScript library that helps you create custom data visualisations. Unlike Chart.js which provides a selection of ready made charts, D3 provides a selection of functions that help you make any chart you can imagine. In culinary terms Chart.js is like a ready meal (fast and convenient) and D3 is like cooking from raw ingredients (which takes more time and skill but with superior results).

D3 does require more skill and usually requires more coding. For instance to create a bar chart with Chart.js requires a few lines of code but with D3 this could run into hundreds of lines (if you want to cover all features and cases).

I cover D3 in this book because it’s one of the most popular JavaScript data visualisation libraries and is a very powerful tool. However it’s beyond this book’s scope to cover D3 comprehensively but I show enough to give you an idea of how D3 works and what it can do.

If you’re interested in learning more I suggest reading [D3 Start to Finish](https://www.createwithdata.com/d3-start-to-finish-book/) which takes you through a full example step by step.

Don’t worry if this chapter proves challenging. We don’t use D3 elsewhere in this book so you can skip this chapter if you wish.

* * *

## 5.2\. Principles of D3

### 5.2.1\. The data join

One of the key principles of D3 is the data join. This is where an array of data is associated with a group of DOM elements. (A DOM element is the browser’s internal representation of an HTML or SVG element.) This means that each data item is associated with a DOM element. We then associate data variables (such as year, technology type or capacity) with style and attributes of the DOM elements (such as position, size and colour).

For instance we could represent each REPD planning application with a circle. This results in 8000 or so circles. Now let’s associate the submission year (`yearSubmitted`) with the circle’s position along the x-axis. This results in a line of circles where the right-most circles are the most recent applications:

![d3 dot 1](images/d3-dot-1.png)

Figure 26\. Dot plot where the x coordinate represents submission date

This isn’t the most useful (nor impressive) data visualisation. But rest assured, each dot represents a planning application. If we make each circle transparent (by lowering it’s `opacity` value) we can see more of a trend over time (the darker the line, the more applications there were):

![d3 dot 2](images/d3-dot-2.png)

Figure 27\. Reducing the opacity of each circle reveals a trend

Now let’s position each circle along the y-axis according to its technology type:

![d3 dot 3](images/d3-dot-3.png)

Figure 28\. Positioning each circle along the y coordinate according to technology

Now we can see patterns in the data. We can see that some technologies have become more prevalent in later years while one technology (the one just below the middle of the chart) was more prevalent in earlier years but subsequently waned. The bottom row (which represents onshore wind) has had a strong stream of applications across all years. (There’s no labels to tell us which row belongs to which technology. Unfortunately this is where D3 requires more effort as we have to add them using more code!)

Now let’s colour each circle according to it’s application status:

![d3 dot 4](images/d3-dot-4.png)

Figure 29\. Colouring each circle according to its status

Green means the site is operational, yellow means the site is awaiting or under construction, purple means the planning application is in progress and grey means the planning application has been abandoned, withdrawn or refused. Now let’s size each circle according to the power output (or capacity) of each proposed installation:

![d3 dot 5](images/d3-dot-5.png)

Figure 30\. Sizing each circle according to its capacity

The bottom row represent onshore wind and the one above offshore wind. Not surprisingly these have the largest power outputs.

This example gives a flavour of how D3 works. We represent data with shapes and modify each shape’s 'visual variables' according to its data values. (A shape’s visual variable is a quantity such as x coordinate, y coordinate, length, width, radius and colour.)

In this chapter I show you how to create the example we’ve just stepped through. We also add an x-axis that shows the years and a y-axis that shows the technology types.

![d3 timeline](images/d3-timeline.png)

Figure 31\. REPD timeline (d3-dot project)

### 5.2.2\. Modules

D3 consists of a number of modules each of which contains functions that help you build visualisations. (You can picture D3 as a toolkit for building visualisations.)

The modules include:

*   `d3-selection` (functions to add, remove and modify DOM elements and perform data joins)
*   `d3-scale` (functions for transforming data values into visual values such as position and colour)
*   `d3-axis` (functions for drawing x and y axes)
*   `d3-hierarchy` (functions to help build hierarchical charts such as treemaps and circle packing)
*   `d3-force` (a physics-based engine for positioning elements)
*   `d3-geo` (for drawing maps)
*   `d3-array` (array manipulation functions)

Each module contains tools for building visualisations, ranging from simple functions that compute the minimum or maximum value in an array, through to functions that help you build an interactive, zoomable treemap. The skill in using D3 is knowing how to piece these elements together.

I introduce a few essential modules in this book, namely `d3-selection`, `d3-scale`, `d3-axes` and `d3-array`. This combination is sufficent to build a custom visualisation.

For more information on the the other modules I suggest visiting the [official documentation](https://d3js.org/api) or [D3 in Depth](https://d3indepth.com).

## 5.3\. Using D3

In this section we look at a few of D3’s core modules (`d3-selection`, `d3-scale`, `d3-axes` and `d3-array`). Most visualisations I’ve built using D3 use these modules and I recommend getting to know these ones first. We use all four in the REPD timeline example later on.

### 5.3.1\. Installation

You can either install the entire D3 library using `npm install d3` or individual modules using (for example) `npm install d3-selection`. In this chapter we install individual d3 modules.

* * *

### 5.3.2\. Selections

The `d3-selection` module lets you add, remove and modify DOM elements. It also lets you perform data joins (where you associate an array of data with DOM elements).

A core concept in `d3-selection` is a 'selection' which is basically an array of DOM elements. In order to modify DOM elements and to join data you need to create a selection.

Supposing you have the following snippet of HTML in your `index.html` file (it’s an `<svg>` element containing three circles):

```
<svg>
  <circle></circle>
  <circle></circle>
  <circle></circle>
</svg>
```

You can create a selection containing a **single element** using `select`. This accepts a single argument containing a CSS selector string:

```
import { select } from 'd3-selection';

// select the svg element
select('svg');

// select the first circle
select('circle');
```

You can also create a selection containing **multiple elements** using `selectAll`. This finds all matching elements:

```
import { selectAll } from 'd3-selection';

// select all the circles
selectAll('circle');
```

* * *

You can select child elements of a selection by **chaining** `select` or `selectAll`. Here’s an example where we make a single selection of the `<svg>` element then select all the `<circle>` elements within it:

```
import { select } from 'd3-selection';

// select all circles that are children of the svg element
select('svg')
  .selectAll('circle');
```

This is known as a **nested selection** and is important when joining data (see later).

A selection is basically an array of DOM elements but selections have a number of methods that let you modify the selection’s elements. Two of the most common methods are `.style` and `.attr` which let you modify the style and attributes of the elements:

```
import { select } from 'd3-selection';

select('svg') ①
  .selectAll('circle') ②
  .attr('cx', 200) ③
  .attr('cy', 100) ④
  .attr('r', 10) ⑤
  .style('fill', 'blue') ⑥
  .style('stroke', '#aaa'); ⑦
```

1.  *①* Select the `<svg>` element.
2.  *②* Select all the `<circle>` elements within the `<svg>` element of the prior selection.
3.  *③* Add a `cx` attribute with value `200` to each circle. This sets the x coordinate of each circle.
4.  *④* Add a `cy` attribute with value `100` to each circle. This sets the y coordinate of each circle.
5.  *⑤* Add a `r` attribute with value `10` to each circle. This sets the radius of each circle.
6.  *⑥* Sets the `fill` CSS property on each circle to `'blue'`.
7.  *⑦* Sets the `stroke` CSS property on each circle to `'#aaa'`.

You can view this example on [Codepen](https://codepen.io/createwithdata/pen/KKrNzXy). Note that the Codepen example imports the whole D3 library as `d3` so we use `d3.select` rather than `select`. Also note that all three circles have the same position and radius so you only see one circle.

### 5.3.3\. Data joins

You can create a correspondence between an array of data and a selection using a **join**. This lets you add, remove and modify DOM elements in a data-driven fashion.

Let’s start by looking at a simple example where we join a short array of data to `<circle>` elements. Suppose we have the following HTML:

```
<svg></svg>
```

The HTML consists of a single, empty `<svg>` element. This element will act as the container of the `<circle>` elements. The container element is usually empty (the data join will populate it).

The data join consists of four steps:

*   call `select` to select a single container element
*   call `selectAll` and pass in the type of element you wish to join
*   call `data` and pass in the data array
*   call `join` and pass in the type of element you wish to join

```
let data = [
  { age: 20, height: 170 },
  { age: 34, height: 165 },
  { age: 26, height: 178 }
];

select('svg') ①
  .selectAll('circle') ②
  .data(data) ③
  .join('circle'); ④
```

1.  *①* The first step selects the element that act as a container.
2.  *②* The second step calls `selectAll` to make a selection of the elements you wish to join. The container is usually empty, so this is usually an empty selection. (This can be confusing because it can feel strange to select elements that don’t exist!)
3.  *③* The third step calls `data` to create an association between the data array `data` and the selection. This allows us to modify each element’s attributes and style according to its associated data (see later).
4.  *④* The fourth step calls `join` to add or remove DOM elements (`<circle>` elements in this example) such that each array element has an associated DOM element.

This data join code ensures that each array element has an associated `<circle>` element.

You can modify the style and attributes of joined DOM elements based on their joined data by passing **a function** into `.style` or `.attr`. The DOM element’s associated array item (its **joined data**) is passed into the function and the return value is used to set the style or attribute’s value. In our case each array item is an object such as `{ age: 34, height: 165 }`.

Let’s add some `.style` and `.attr` calls to our example:

```
let data = [
  { time: 50, value: 15 },
  { time: 150, value: 40 },
  { time: 250, value: 30 }
];

select('svg')
  .selectAll('circle')
  .data(data)
  .join('circle')
  .style('fill', 'orange') ①
  .attr('cx', d => d.time) ②
  .attr('cy', 100) ③
  .attr('r', d => d.value); ④
```

1.  *①* Each circle’s `fill` value is set to `orange` using the approach covered in the [Selections](#_custom_charts_with_d3_js.xhtml__selections) section.
2.  *②* Each circle’s `cx` attribute is set in a data driven fashion by passing in a function. The function returns the `time` property of the joined data so the first circle’s `cx` value will be 50, the second circle’s `cx` will be `150` and the last circle’s `cx` will be `250`.
3.  *③* Each circle’s `cy` attribute is set to 100.
4.  *④* Each circle’s `r` attribute is set in a data driven fashion by passing a function in. The function returns the `value` property of the joined data so the first circle’s `r` value will be `15` etc.

The result looks like:

![d3 join circles](images/d3-join-circles.png)

Figure 32\. Joining an array of data to circle elements

Each array element corresponds to a `<circle>` element. Each circle’s x coordinate and radius is set according to the joined data.

Here’s the example on Codepen: [https://codepen.io/createwithdata/pen/OJwpVbG](https://codepen.io/createwithdata/pen/OJwpVbG).

### 5.3.4\. Scale functions

Scale functions let you transform data variables into visual variables such as position and colour. For example the REPD data has years varying between 1990 and 2021\. If you’d like to build a timeline that’s 1000 pixels long you can create a scale function that accepts a year and outputs a value between 0 and 1000.

D3 has several scale types, the most common of which are `scaleLinear`, `scaleSqrt`, `scaleTime` and `scalePoint`. For each scale type D3 provides a constructor function. The typical usage pattern is:

*   call the scale constructor. This returns a scale function.
*   set the scale’s domain by calling the scale function’s `domain` method. The domain is the scale function’s minimum and maximum input value.
*   set the scale’s range by calling the scale function’s `range` method. The range is the scale function’s minimum and maximum output value.

Here’s an example where we create a linear scale:

```
import { scaleLinear } from 'd3-scale';

let myScale = scaleLinear() ①
  .domain([0, 100]) ②
  .range([0, 500]); ③
```

1.  *①* Call a scale constructor to create and return a scale function.
2.  *②* Call the scale’s `domain` method to set its domain (its minimum and maximum input).
3.  *③* Call the scale’s `range` method to set its range (its minimum and maximum output).

`myScale` is linear scale function that accepts values between 0 and 100 and outputs values between 0 and 500. It linearly maps between the domain and range. This means that an input value that’s a proportion `u` along the domain is mapped to the value that’s a proportion `u` along the range.

For example:

```
myScale(0); // returns 0
myScale(100); // returns 500
myScale(50); // returns 250
```

`scaleTime` is similar to scaleLinear but its domain is an array of dates:

```
import { scaleTime } from 'd3-scale';

let timeScale = scaleTime()
  .domain([new Date(2016, 0, 1), new Date(2017, 0, 1)])
  .range([0, 700]);

timeScale(new Date(2016, 0, 1));   // returns 0
timeScale(new Date(2016, 6, 1));   // returns 348.00...
timeScale(new Date(2017, 0, 1));   // returns 700
```

We use `scaleTime` in the REPD dot plot example to compute the x-coordinate of each circle.

`scalePoint` accepts an array of categorical values as its domain and distributes the values across the range:

```
let pointScale = scalePoint()
  .domain(['Mon', 'Tue', 'Wed', 'Thu', 'Fri'])
  .range([0, 500]);

pointScale('Mon');  // returns 0
pointScale('Tue');  // returns 125
pointScale('Fri');  // returns 500
```

We use `scalePoint` in the REPD dot plot example to compute the y-coordinate of each circle.

* * *

`scaleSqrt` is useful when sizing circles proportionally to a variable:

```
let sqrtScale = scaleSqrt()
  .domain([0, 100])
  .range([0, 30]);

sqrtScale(0);   // returns 0
sqrtScale(50);  // returns 21.21...
sqrtScale(100); // returns 30
```

We use `scaleSqrt` in the REPD dot plot example to compute the radius of each circle.

### 5.3.5\. Axes

The `d3-axis` module helps you draw axes. To draw an axis:

*   create an SVG `<g>` element to act as a container for the axis. You also need to position it appropriately using a `transform` attribute
*   create an **axis generator** by calling `axisLeft`, `axisRight`, `axisBottom` or `axisTop` and passing in a scale function
*   select the axis container and use the selection’s `.call` method to call the axis generator.

There are four types of axis depending on which side of a chart it’s for. For example `axisLeft` is used for a y axis on the left side of a chart.

As an example let’s make an x axis. First add an SVG `<g>` element to act as a container for the axis. Notice we’ve translated it so the axis isn’t clipped against the top and left boundaries of the viewport:

```
<svg>
  <g class="x-axis" transform="translate(100,100)"></g>
</svg>
```

* * *

In JavaScript we create a scale function and pass it into `axisBottom`:

```
import { select } from 'd3-selection';
import { scaleLinear } from 'd3-scale';
import { axisBottom } from 'd3-axis';

let scale = scaleLinear() ①
  .domain([-100, 100])
  .range([0, 500]);

let axis = axisBottom(scale); ②

select('.x-axis') ③
  .call(axis); ④
```

1.  *①* Create a linear scale function
2.  *②* Create an axis generator and pass in the scale function.
3.  *③* Select the axis container.
4.  *④* Call the selection’s `call` method and pass in the axis generator.

The axis generator creates the appropriate lines, ticks and labels within the container. The axis spans between the scale function’s range values, so in this example its x coordinate spans between the 0 and 500.

![d3 axis](images/d3-axis.png)

Figure 33\. Axis created using d3-axis

Here’s the example on Codepen: [https://codepen.io/createwithdata/pen/XWPXRqe](https://codepen.io/createwithdata/pen/XWPXRqe)

### 5.3.6\. Events

You can attach event handlers to a selection using the `.on` method. This method accepts two arguments:

*   the event type (e.g. `'click'`, `'mouseover'`, `'mouseout'`)
*   a function whose first parameter (typically named `e`) is the browser event object and whose second parameter `d` is the joined value.

As an example let’s add an event handler to the data join example that responds to click events. When a circle is clicked an alert message appears containing the `value` property of the joined data:

```
let data = [
  { time: 50, value: 15 },
  { time: 150, value: 40 },
  { time: 250, value: 30 }
];

select('svg')
  .selectAll('circle')
  .data(data)
  .join('circle')
  .style('fill', 'orange')
  .attr('cx', d => d.time)
  .attr('cy', 100)
  .attr('r', d => d.value)
  .on('click', (e, d) => { ①
    alert('Value is: ' + d.value); ②
  });
```

1.  *①* Add an event handler to the selection that responds to click events.
2.  *②* When a circle is clicked an alert is activated that displays the `value` property of the joined data.

The element’s joined data is passed into the callback function (as the second argument). Thus if the second circle is clicked, the alert’s message is 'Value is: 40'.

![d3 event](images/d3-event.png)

Figure 34\. Alert triggered by an event added using D3’s .on method

Here’s the example on Codepen: [https://codepen.io/createwithdata/pen/xxaZdaj](https://codepen.io/createwithdata/pen/xxaZdaj).

You can add more than one event handler to a selection using additional calls to the `on` method.

* * *

### 5.3.7\. Array helpers

D3’s `d3-array` module provides a number of array utility functions. For example it has functions for computing the minimum, maximum, sum and mean of an array. (See [https://github.com/d3/d3-array#api-reference](https://github.com/d3/d3-array#api-reference) for a full guide.)

`min` and `max` compute the minimum and maximum values in an array. `extent` computes the min and max values and returns the result as an array `[min, max]`.

If the data’s an array of objects you must also pass in an accessor function to specify which property to use.

```
import { max, extent } from 'd3-array';

// return the maximum value
max([10, 60, 30, 20]);

let data = [
  { time: 50, value: 15 },
  { time: 150, value: 40 },
  { time: 250, value: 30 }
];

// return the maximum of the value property in data (returns 40)
max(data, d => d.value); ①

// return the extent of the time property in data (returns [50, 250])
extent(data, d => d.time);
```

1.  *①* The second argument of `max` is an accessor function whose input is an array element (an object in this example) and the output is the value we’re comparing.

* * *

## 5.4\. Tippy.js tooltip

A tooltip reveals more information about a data point when it’s hovered by the mouse pointer. They’re non-trivial to implement well so I recommend using a library such as the [Tippy.js tooltip library](https://atomiks.github.io/tippyjs/). This library is relatively straightforward to use, looks nice and works well. You can populate the tooltip with whatever content you like and it even adapts so that it doesn’t get clipped when it’s close to the edge of its container.

![tippyjs](images/tippyjs.png)

Figure 35\. Tippy.js tooltip

To use Tippy.js:

*   install using `npm install tippy.js` on the command line
*   import into a JavaScript file using `import tippy from 'tippy.js'`
*   import Tippy’s style file using `import 'tippy.js/dist/tippy.css'`
*   add a tooltip to each element by calling `tippy()`. The first argument specifies the element and the second argument is a configuration object.

* * *

Let’s add tooltips to our ongoing example:

```
import { select } from 'd3-selection';
import tippy from 'tippy.js'; ①
import 'tippy.js/dist/tippy.css'; ②

let data = [
  { time: 50, value: 15 },
  { time: 150, value: 40 },
  { time: 250, value: 30 }
];

select('svg')
  .selectAll('circle')
  .data(data)
  .join('circle')
  .style('fill', 'orange')
  .attr('cx', d => d.time)
  .attr('cy', 100)
  .attr('r', d => d.value)
  .each(function(d) { ③
    tippy(this, { ④
      content: 'The value is ' + d.value ⑤
    });
  });
```

1.  *①* Import Tippy’s constructor function `tippy`.
2.  *②* Import Tippy’s style file. (Vite allows you to import CSS files within a JavaScript file.)
3.  *③* D3’s `each` method lets you iterate through each element in a selection. For each element in the selection, the specified callback function is called and the element’s joined data is assigned to the `d` parameter.
4.  *④* A tooltip is added to the current element by calling `tippy` and passing in the current element as the first argument. (In the callback function D3 assigns the current DOM element to the `this` keyword, so long as the function is defined using the `function` keyword, rather than the arrow operator.)
5.  *⑤* A configuration object is passed in as the second argument. We set the content using the `content` property. `d` represents the joined data of the current element and we display its value property.

* * *

Now when a circle is hovered a toolip is displayed:

![tippyjs simple](images/tippyjs-simple.png)

Figure 36\. Tippy.js tooltip on circles example

Here’s the example on Codepen: [https://codepen.io/createwithdata/pen/pvzqwLM](https://codepen.io/createwithdata/pen/pvzqwLM)

* * *

## 5.5\. D3 example application

In this section we look at an application that loads the REPD data and creates a custom visualisation using D3\. This project is built using Vite so follows a similar structure to the `load-data` project.

The visualisation is a dot plot where the horizontal position is determined by the `yearSubmitted` property and the vertical position by the `technology` property. The size of each circle is related to the `capacity` property and the colour to the `status` property.

There’s two axes: one on the left that shows the technology types and one at the bottom that shows the year.

![d3 timeline](images/d3-timeline.png)

Figure 37\. Dot plot created by d3-dot project

To run the project navigate to the `d3-dot` project directory and call `npm install`. Call `npm run dev` to start the application server. This will give you a url (usually [http://localhost:5173](http://localhost:5173)) to visit. You should see a dot plot when you visit this URL.

```
cd d3-dot

npm install

npm run dev
```

### 5.5.1\. File structure

The project directory looks like:

```
d3-dot/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

Listing 25\. d3-dot project files

The project was built using Vite so has the standard Vite file structure. The REPD data is in the `public` directory. All the JavaScript code is in `main.js`.

The main project files are `index.html`, `main.js` and `style.css`.

* * *

### 5.5.2\. index.html

The main HTML file is `index.html`:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>REPD Timeline</title> ①
  </head>
  <body>
    <h1>Timeline of REPD applications 1990-2022</h1> ②
    <svg> ③
      <g class="inner"> ④
        <g class="x-axis"></g> ⑤
        <g class="y-axis"></g> ⑤
        <g class="points"></g> ⑥
      </g>
    </svg>
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

Listing 26\. d3-dot/index.html

1.  *①* As usual we’ve taken the `index.html` generated by Vite and modified it. A minor change is to update the content of the `<title>` element.
2.  *②* Add a heading for the chart.
3.  *③* The body content is more substantial than previous projects. An `<svg>` element is added for the chart.
4.  *④* We place a `<g class="inner">` element inside the `<svg>` element so that we can position the chart within the `<svg>` element.
5.  *⑤* Add container elements for the axes.
6.  *⑥* Add a container for the dots.

* * *

### 5.5.3\. main.js

Here’s an outline of `main.js`:

```
import { select } from 'd3-selection'; ①
import { scaleTime, scalePoint, scaleSqrt } from 'd3-scale';
import { max, extent } from 'd3-array';
import { axisBottom, axisLeft } from 'd3-axis';
import { tidy, count, filter, mutate, sort, desc } from '@tidyjs/tidy';
import tippy from 'tippy.js';
import 'tippy.js/dist/tippy.css';
import 'tippy.js/themes/light.css';

import './style.css';

let green = '#358600';
let grey = '#aaa';
let purple = '#A675A1';
let yellow = '#F5CF29';

let statusColors = { ②
  'Abandoned': grey,
  'Appeal Withdrawn': grey,
  'Application Refused': grey,
  'Application Submitted': purple,
  ...
};

function update(data) { ... }

function init(data) { ③
  ...

  update(data);
}

fetch('./repd.json') ④
  .then(res => res.json())
  .then(data => init(data));
```

Listing 27\. d3-dot/main.js

1.  *①* The structure of `main.js` is fairly similar to previous projects. We import functions from D3, tidy.js and tippy.js.
2.  *②* Define a colour lookup object `statusColors`. (We define a few colours (`green`, `grey`, `purple` and `yellow`) so we can reuse them in the `statusColors` object).
3.  *③* `init` carries out some data processing then calls `update`.
4.  *④* The data is requested using `fetch` at the bottom of the file. When the data loads the `init` function is called.

`init` does some data processing then calls `update`:

```
function init(data) {
  data = tidy(
    data,
    filter(d => d.dateSubmitted !== null), ①
    mutate({
      dateSubmitted: d => new Date(d.dateSubmitted) ②
    }),
    sort(desc('capacity')) ③
  );

  update(data); ④
}
```

Listing 28\. d3-dot/main.js

1.  *①* Filter out planning applications with a `null` value (which indicates a missing value) because there isn’t an obvious way of placing them along a timeline.
2.  *②* Convert the `dateSubmitted` property from a string into a date object because scale functions generated by D3’s `scaleTime` require date objects as input rather than strings.
3.  *③* Sort the items by `capacity` in descending order. This means that the `<circle>` elements will be ordered within their parent element from large to small. This means the largest circles are drawn first so smaller circles aren’t hidden behind larger ones.
4.  *④* At the end of `init` call `update` which draws the chart.

* * *

Before looking at `update` lets look at the chart layout:

![d3 dot layout](images/d3-dot-layout.png)

Figure 38\. d3-dot chart layout

The `<svg>` element is depicted in grey and it contains the `<g class="inner">` element which contains all the chart elements (including the axes). The x and y axes meet at the origin of the `<g class="inner">` element (depicted by a small circle where the two axes meet).

In order to create sufficient space for the axis labels we introduce margins around the `<g class="inner">` element and these are specified using the variables `leftMargin`, `rightMargin`, `topMargin` and `bottomMargin`. We define these at the beginning of `update`:

```
function update(data) {
  let width = 1200, height = 600; ①
  let leftMargin = 210, rightMargin = 20, topMargin = 20, bottomMargin = 40; ②

  ...
}
```

Listing 29\. d3-dot/main.js

1.  *①* Define the overall width and height of the `<svg>` element.
2.  *②* Define the left, right, top and bottom margins.

Although the screenshots of the REPD dot plot show the x-axis at the bottom of the chart, it does actually live at the top. We set the tick length to the full height of the chart which causes the tick marks to look like grid-lines and the tick labels get pushed to the bottom of the chart (see later).

Next in `update` we create the x, y, and radius scale functions:

```
function update(data) {
  ...

  // x scale
  let dateSubmittedExtent = extent(data, d => d.dateSubmitted);
  let xLength = width - leftMargin - rightMargin;
  let xScale = scaleTime() ①
      .domain(dateSubmittedExtent)
      .range([0, xLength]);

  // y scale
  let technologyValues = tidy(
    data,
    count('technology'),
    sort('technology')
  ).map(d => d.technology);
  let yLength = height - topMargin - bottomMargin;
  let yScale = scalePoint() ②
      .domain(technologyValues)
      .range([0, yLength]);

  // radius scale
  let maxCapacity = max(data, d => d.capacity);
  let maxRadius = 20;
  let rScale = scaleSqrt() ③
      .domain([0, maxCapacity])
      .range([0, maxRadius]);

  ...
}
```

Listing 30\. d3-dot/main.js

1.  *①* The scale function `xScale` is used to determine the x location of the dots. Its input is a `dateSubmitted` value (a JavaScript date object) and its output is an x coordinate. The input domain is the extent of the `dateSubmitted` property and the output range is the overall width minus the left and right margins (refer to the chart layout diagram). The x location is driven by `dateSubmitted` so we use `scaleTime` to generate a scale function that accepts date objects as input.
2.  *②* The scale function `yScale` is used to determine the y location of the dots. Its input is a technology value such as `'Battery'` and its output is a y coordinate. The input domain is `technologyValues`, a sorted, unique array of technology names (created using tidy.js) and the output range is the overall height minus the top and bottom margins. The y location is driven by discrete values and we wish the output values to be evenly spaced so we use D3’s `scalePoint`.
3.  *③* The scale function `rScale` is used to determine the radius of the dots. Its input is a `capacity` value (a number) and its output is a radius in pixels. The input domain is `[0, maxCapacity]` where `maxCapacity` is the maximum capacity. The output range is `[0, 20]` where 20 is the upper radius limit in pixels. We want to set the circle’s **area** (rather than its radius) proportionally to the capacity (as this is best practice) so we use D3’s `scaleSqrt`.

```
function update(data) {
  ...

  select('svg')
    .attr('width', width)
    .attr('height', height);

  select('svg .inner')
    .attr('transform', 'translate(' + leftMargin + ',' + topMargin + ')');

    ...
}
```

Listing 31\. d3-dot/main.js

This code sets the width and height of the `<svg>` element using the `width` and `height` variables. This ensures that the `<svg>` element is large enough to contain the entire chart.

`<g class="inner">` is then translated by `(leftMargin, topMargin)` to create space for the y-axis labels and introduce a bit of space at the top (refer to the chart layout diagram).

* * *

Now let’s look at the code that draws the visualisation:

```
function update(data) {
  ...

  // Points
  select('svg .points') ①
    .selectAll('circle') ②
    .data(data) ③
    .join('circle') ④
    .attr('cx', d => xScale(d.dateSubmitted)) ⑤
    .attr('cy', d => yScale(d.technology)) ⑤
    .attr('r', d => rScale(d.capacity)) ⑤
    .style('fill', d => statusColors[d.status]) ⑤
    .style('stroke', d => statusColors[d.status]) ⑤
    .style('fill-opacity', 0.5)
    .each(function(d) { ⑥
      let html = ''; ⑦
      html += '<div>Name: ' + d.name + '</div>';
      html += '<div>Technology: ' + d.technology + '</div>';
      html += '<div>Capacity: ' + d.capacity + ' MW</div>';
      html += '<div>Date submitted: ' + d.dateSubmitted.toDateString() + '</div>';
      html += '<div>Status: ' + d.status + '</div>';
      tippy(this, { ⑧
        content: html, ⑨
        allowHTML: true, ⑩
        theme: 'light', ⑪
        duration: 0 ⑫
      });
    });

    ...
}
```

Listing 32\. d3-dot/main.js

1.  *①* The first four lines join the `data` array to `circle` elements. The data join follows the four step procedure that we presented in the [Data joins](#_custom_charts_with_d3_js.xhtml__data_joins) section. This step selects the element that contains the circles.
2.  *②* Call `selectAll` and pass in the element type being joined.
3.  *③* Associate the `data` array with the selection using the `data` method.
4.  *④* Call `join` and pass in the element type being joined. This adds or removes `<circle>` elements so that each element in `data` has a corresponding `<circle>` element. (In this case it adds over 8000 circles.)
5.  *⑤* Call `.attr` and `.style` to set the position, size and colour of the circle elements. By passing in a function as the second argument we can set these attributes and style according to the joined data (see the [Data joins](#_custom_charts_with_d3_js.xhtml__data_joins) section). Notice that we use the `xScale`, `yScale` and `rScale` functions to compute a position or radius from the data values. For example each circles' `cx` attribute is set by passing the `dateSubmitted` property of its joined data into `xScale`.
6.  *⑥* Call D3’s `each` method to iterate through the selection. The callback function is called on each element in the selection and the element’s joined data is assigned to the `d` parameter.
7.  *⑦* Define a variable `html` that specifies the tooltip’s content. This is defined as a string of HTML code.
8.  *⑧* Call the Tippy.js constructor and pass in `this` (which represents the current DOM element of the selection).
9.  *⑨* Set the tooltip content to the string of HTML.
10.  *⑩* Set `allowHTML` to `true` so that Tippy interprets the content as HTML code.
11.  *⑪* Set the theme to `light`. Tippy supports different themes. We imported the light theme near the top of this file.
12.  *⑫* Set the show and hide duration to zero so that the tooltip appears and disappears instantly.

Finally in `update` we draw the axes:

```
function update(data) {
  ...

  // y-axis
  let yAxis = axisLeft(yScale) ①
      .tickSize(0); ②

  select('svg .y-axis') ③
    .call(yAxis);

  // x-axis
  let xAxis = axisBottom(xScale) ④
      .tickSize(yLength + 20); ⑤

  select('svg .x-axis') ⑥
    .call(xAxis);
}
```

Listing 33\. d3-dot/main.js

1.  *①* The axis creation is similar to the examples in the [Axes](#_custom_charts_with_d3_js.xhtml__axes) section. We start by creating an axis generator for the y-axis using `axisLeft` and passing in `yScale`.
2.  *②* The y axis doesn’t require tick marks so we set the tick size to zero by calling `tickSize` and passing in 0.
3.  *③* Select the y-axis container and use the `call` method to run the generator. The y-axis starts at the origin of `<g class="inner">` and proceeds downwards. (The origin of `<g class="inner">` is at `(leftMargin, topMargin)` relative to the `<svg>` element and is depicted by the small circle in the chart layout diagram.) By default the labels of an `axisLeft` axis appear to the left of the axis line.
4.  *④* Create an axis generator for the x-axis using `axisBottom` and pass in `xScale`.
5.  *⑤* Set the tick size to `yLength + 20` which means the ticks span the entire height of the chart. This also pushes the tick labels all the way to the bottom of the chart. This is a clever trick to create gridlines.
6.  *⑥* Select the x-axis container and use the `call` method to run the generator. The x-axis starts at the origin of `<g class="inner">` and proceeds to the right.

There’s also a few CSS rules in `style.css` that hide the the x-axis' primary line so that only the ticks are visible.

### 5.5.4\. style.css

`style.css` mainly contains a few CSS rules to style the axes:

```
body {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif; ①
  background-color: #eee; ②
}

g.x-axis path, g.y-axis path {
  display: none; ③
}

g.x-axis line {
  stroke-dasharray: 1 1; ④
  stroke: #ccc; ④
}

g.x-axis text, g.y-axis text {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif; ⑤
  font-size: 12px;
}
```

Listing 34\. d3-dot/style.css

1.  *①* Set the font family for the whole page. This rule remains from Vite’s default project.
2.  *②* Set the page background colour to off white.
3.  *③* The primary line of the axis (the line that connects the tick marks) is hidden by selecting the `path` element that represents the line and setting its `display` to `none`. (It’s not obvious how to style an axis generated by D3\. I usually inspect the axis using the browser’s inspect element tool, find the element I’m interested in and figure out what selector string to use.)
4.  *④* The vertical grid lines (made up of the full height x-axis ticks) are given a feint, dotted style.
5.  *⑤* For reasons unknown to me the font family of the `body` element doesn’t cascade to the axes so I’ve added a rule for this.

## 5.6\. Wrapping up

This chapter introduced D3.js and showed how to create a custom chart using it. Ceating a chart using D3 is a lot more involved than with Chart.js but the advantage is you can fully customise the chart.

Whether or not you think you’ll use D3 in the future I hope this chapter helps you understand D3 better.

## 5.7\. Ideas for further study

I recommend playing around with the project by exploring, modifying and adding code. Here are some ideas:

*   show regions along the y-axis (instead of technology).
*   change the colour scheme so that Battery applications are coloured in purple and everything else in grey.
*   change the information displayed in the tooltip.

Visit the Appendix for solutions.

# 6\. Data-driven Maps with Leaflet

This chapter introduces [Leaflet](https://leafletjs.com/) which is a free, open-source JavaScript library for making maps. Leaflet creates tile-based maps meaning the maps are made up of small images tiled together. (This is the same method that Google Maps uses.) The user can zoom in and out and scroll around the map.

You can also draw shapes on the map which means you can create data-driven maps.

Here’s a map generated using Leaflet that visualises the REPD data (we’ll step through this project in this chapter):

![leaflet](images/leaflet.png)

Figure 39\. Leaflet map showing REPD planning applications

In this chapter I:

*   introduce Leaflet
*   show how to use Leaflet
*   walk through a Leaflet example that visualises the REPD data.

* * *

## 6.1\. Introduction to Leaflet

Leaflet is a free, open-source JavaScript library that draws tile-based maps. It’s relatively easy to use, very configurable and you can draw shapes such as circles on top of the map.

A Leaflet map is made up of small JPG or PNG images placed in a grid formation. When the map first loads, and when the map is panned or zoomed, new tiles are loaded.

![leaflet tiles](images/leaflet-tiles.png)

Figure 40\. Map tiles

Leaflet relies on a tile server to provide the map tiles. There’s lots of options but few of them are free. In this book we use [Stadia’s tiles](https://stadiamaps.com/products/map-tiles/) which are free for non-commercial use but if you publish your map on the web you’ll need a Stadia account. If you were really serious you could consider hosting your own tile server but this isn’t something I’ve done myself.

You can browse a large selection of tile sets [here](https://leaflet-extras.github.io/leaflet-providers/preview/). Other options are Stamen, Thunderforest and Mapbox.

* * *

## 6.2\. How to use Leaflet

### 6.2.1\. Installation

Install Leaflet by navigating to your project and calling `npm install leaflet`.

### 6.2.2\. Creating a map

There are a few steps to creating a map with Leaflet:

*   add a `<div>` container for the map to `index.html`
*   add a CSS rule to set the height of the container
*   make sure Leaflet’s CSS file is imported
*   in the relevant JavaScript files import Leaflet
*   create a map using Leaflet’s `map` method
*   specify the tile server and set the map’s view center.

Each of these steps is important and missing one of them out can result in no map (or a scrambled map!).

#### Add a container

A `<div>` container for the map must be added to the HTML. For example:

```
<div id="map"></div>
```

I recommend adding an `id` attribute to the container as this makes it easier to identify the container in your JavaScript.

#### Set the height of the container

The height of the container must be set. This can be done using CSS. (I’ve often forgotten this step and wondered why my map is invisible.)

```
#map {
  height: 600px;
}
```

#### Import Leaflet’s stylesheet

Leaflet has a CSS stylesheet that must be included in your project. For a Vite project, this can be done by adding an `@import` statement in `style.css`. (You can read more about this feature in [Vite’s documentation](https://vitejs.dev/guide/features.html#import-inlining-and-rebasing).)

```
@import 'leaflet/dist/leaflet.css';
```

If this step is omitted the map may appear scrambled.

#### Create a map

In the JavaScript code a map is created by importing the Leaflet library, calling the `map` method, specifying the tile server and setting the view center:

```
import L from 'leaflet'; ①

let map = L.map('map'); ②

L.tileLayer('https://tiles.stadiamaps.com/tiles/alidade_smooth/{z}/{x}/{y}{r}.png', { ③
  maxZoom: 20,
  attribution: '&copy; <a href="https://stadiamaps.com/">Stadia Maps</a>...',
}).addTo(map); ④

map.setView([55, -2], 6); ⑤
```

1.  *①* The first line of `main.js` imports the main Leaflet object. This object is exported as an unnamed object, so we have to name it. The convention is to name it `L`.
2.  *②* Next a map object is created by calling `L.map` and passing in the id of the `<div>` container. This creates a map object but doesn’t draw the map yet. We still need to add a tile layer to the map.
3.  *③* The next step is to create a tile layer using `L.tileLayer`. Pass in two arguments, the tile layer’s URL and a configuration object. Both arguments are usually supplied by the tile server provider. If you browse the Leaflet providers gallery ([https://leaflet-extras.github.io/leaflet-providers/preview/](https://leaflet-extras.github.io/leaflet-providers/preview/)) each tile set has this information.
4.  *④* The tile layer is then added to the map object using `addTo`. (`addTo` is a layer method that adds the layer to an existing map object.)
5.  *⑤* Finally the map’s view center and zoom level is specified using the `setView` method. The first argument is an array containing the latitude and longitude (`[latitude, longitude]`) and the second is a zoom level (where 0 is fully zoomed out). The maximum zoom level is determined by the tile server. In this example the maximum zoom level is 20.

This example results in a basic map centered on the UK:

![leaflet basic map](images/leaflet-basic-map.png)

Figure 41\. Basic Leaflet map centered on the UK

* * *

#### Add a marker

A circle marker can be created using Leaflet’s `circleMarker` method and added to the map using the `addTo` method. When the marker is created we pass in an array containing the marker’s latitude and longitude. The circle marker’s style can also be set using the `setStyle` method and passing in an object containing CSS properties:

```
import L from 'leaflet';

let map = L.map('map');

...

let marker = L.circleMarker([50.8229, -0.1363]); ①

marker.setStyle({ ②
  radius: 10, ③
  fillColor: '#FFB30F', // inner colour
  fillOpacity: 0.75,    // inner opacity
  color: '#FFB30F',     // border colour
  weight: 1             // border width
});

marker.addTo(map); ④
```

1.  *①* Create a circle marker object by calling Leaflet’s `circleMarker` method and passing in its location.
2.  *②* Use the marker’s `setStyle` method to style the marker.
3.  *③* Set the marker’s radius (in pixels).
4.  *④* Add the marker to the map.

* * *

This example places a circle marker over Brighton, UK:

![leaflet circle marker](images/leaflet-circle-marker.png)

Figure 42\. Leaflet circle marker

* * *

## 6.3\. Leaflet example application

In this section we look at an application that loads the REPD data and creates a data driven map using Leaflet. This project is built using Vite so follows a similar structure to the `load-data` project.

The map displays each REPD planning applications as a circle. Each circle is located using latitude and longitude values in the data, sized according to its output capacity and coloured according to its technology type.

![leaflet](images/leaflet.png)

Figure 43\. Leaflet map showing REPD planning applications

To run the project navigate to the `leaflet-map` project directory and call `npm install`. Call `npm run dev` to start the application server. This will give you a url (usually [http://localhost:5173](http://localhost:5173)) to visit. You should see a map covered in circles when you visit this URL.

```
cd leaflet-map

npm install (or npm i)

npm run dev
```

* * *

### 6.3.1\. File structure

The project directory looks like:

```
leaflet-map/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

Listing 35\. leaflet-map project files

The project was built using Vite so has the standard Vite file structure. The REPD data is in the `public` directory. All the JavaScript code is in `main.js`.

The main project files are `index.html`, `main.js` and `style.css`.

### 6.3.2\. index.html

Here’s the main HTML file `index.html`:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>REPD Planning applications</title> ①
  </head>
  <body>
    <div id="map"></div> ②
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

Listing 36\. leaflet-map/index.html

1.  *①* As usual we’ve taken the `index.html` generated by Vite and modified it. Here the content of the `<title>` element has been updated.
2.  *②* The body content just contains a `<div>` container for the map.

### 6.3.3\. main.js

`main.js` loads the data then calls `draw` which creates the map. Here’s an outline:

```
import L from 'leaflet'; ①
import { scaleSqrt } from 'd3-scale';
import { max } from 'd3-array';

import './style.css'; ②

const technologyColors = { ③
  'Advanced Conversion Technologies': '#FF9999',
  'Anaerobic Digestion': '#C58882',
  'Battery': '#B6A6CA',
  ...
};

function getTooltipContent(d) { ... } ④

function draw(data) { ... } ⑤

fetch('./repd.json') ⑥
  .then(res => res.json())
  .then(data => draw(data));
```

Listing 37\. leaflet-map/main.js

1.  *①* At the top of the file import Leaflet and two functions `scaleSqrt` and `max` from D3 that help size the circles.
2.  *②* Import `style.css`. (This isn’t standard JavaScript but is supported by Vite.)
3.  *③* Define a colour lookup object so that each circle can be coloured according to its technology type. We only define colours for the more common technology types.
4.  *④* Leaflet has a built in tooltip and we define a function `getTooltipContent` that creates the tooltip’s content.
5.  *⑤* Next the `draw` function is defined. This is where the map is created and the circle markers added.
6.  *⑥* At the bottom of `main.js` is the usual code to request the REPD data and we call `draw` when the data arrives.

* * *

Let’s look at the first few lines of the `draw` function:

```
function draw(data) {
  let map = L.map('map'); ①

  L.tileLayer('https://tiles.stadiamaps.com/tiles/alidade_smooth/{z}/{x}/{y}{r}.png', {
    maxZoom: 20,
    attribution: '...',
  }).addTo(map);

  map.setView([55, -2], 6);

  let maxCapacity = max(data, d => d.capacity); ②
  let maxRadius = 20;
  let radiusScale = scaleSqrt().domain([0, maxCapacity]).range([3, maxRadius]);

  ...
}
```

Listing 38\. leaflet-map/main.js

1.  *①* The first few lines of `draw` create a map in the same manner as previously described in this chapter.
2.  *②* Compute the data’s maximum `capacity` property and create a `radiusScale` function. Note we set the minimum range to be 3 so that installations with a very low capacity are visible.

* * *

Now that we’ve set up the map and radius scale function we can draw the points:

```
function draw(data) {
  ...

  data.forEach(d => { ①
    if (d.lat === null || d.lon === null) return;
    let marker = L.circleMarker([d.lat, d.lon]); ②
    let radius = radiusScale(d.capacity || 0); ③
    let color = technologyColors[d.technology] || '#aaa'; ④

    marker.setStyle({ ⑤
      radius: radius,
      fillColor: color,
      fillOpacity: 0.75,
      color: color,
      weight: 1
    });

    marker.bindTooltip(getTooltipContent(d)); ⑥
    marker.addTo(map); ⑦
  });
}
```

Listing 39\. leaflet-map/main.js

1.  *①* Iterate through `data`. If the item has a `null` latitude or longitude we return early.
2.  *②* Create a circle marker and set its position.
3.  *③* Compute the circle’s radius by passing item’s `capacity` property into `radiusScale`. If the item has a `null` value fallback to zero, meaning the circle will have a radius of 3.
4.  *④* Compute the circle colour using the `technologyColors` lookup. Fallback to grey if the lookup doesn’t have a value for a particular technology type.
5.  *⑤* Set the circle marker’s radius and style. `fillColor` and `fillOpacity` set the colour and opacity of the circle’s inside. `color` sets the colour of the circle’s border and `weight` sets the thickness of the circle’s border. This results in a slightly transparent circle with a slightly darker border.
6.  *⑥* Leaflet has a built in tooltip but its approach is unusual. We set each marker’s tooltip content upfront rather than computing it on the fly then attach it to the marker using `bindTooltip`. The tooltip content is computed by calling `getTooltipContent` and passing in the item’s data (see later).
7.  *⑦* Add the marker to the map using `addTo`.

* * *

The `getTooltipContent` function accepts a single data object and it returns an HTML string containing information about a data item:

```
function getTooltipContent(d) {
  var content = '';
  content += '<h4>' + d.name + '</h4>';
  content += '<div>Technology: ' + d.technology + '</div>';
  content += '<div>Capacity: ' + (d.capacity ? d.capacity + 'Mw' : 'Unknown ') + '</div>';
  content += '<div>Operator: ' + d.operator + '</div>';
  content += '<div>Status: ' + d.status + '</div>';
  return content;
}
```

Listing 40\. leaflet-map/main.js

When a circle is hovered Leaflet displays the circle’s tooltip content:

![leaflet tooltip](images/leaflet-tooltip.png)

Figure 44\. Leaflet tooltip

* * *

### 6.3.4\. style.css

The `style.css` file contains a small amount of CSS:

```
@import 'leaflet/dist/leaflet.css'; ①

body {
  margin: 0; ②
}

#map {
  height: 100vh; ③
}

h4 {
  margin: 0; ④
}
```

Listing 41\. leaflet-map/style.css

1.  *①* Import Leaflet’s CSS file (this way of importing a CSS file is supported by Vite).
2.  *②* Remove space around the map by setting the body margin to zero.
3.  *③* Set the map’s height to the full height of the browser window.
4.  *④* Set the margin of `<h4>` elements to zero. This is to reduce space around the tooltip’s heading.

* * *

## 6.4\. Wrapping up

This chapter introduced the Leaflet mapping library. It showed how to create a map, how to add circles to the map and showed a complete example of a data-driven map.

Leaflet’s a fantastic library for creating maps and one of the easiest libraries I know of for quickly making a map. It’s more powerful than it appears at first glance. As well as circle markers you can add other shapes including ones based on GeoJSON data. You can also programmatically set the view point and zoom and even get the map to 'fly to' a particular location. I recommend visiting the [official documentation](https://leafletjs.com/reference.html) to explore what Leaflet has to offer.

## 6.5\. Ideas for further study

I recommend playing around with the project by exploring, modifying and adding code. Here are some ideas:

*   colour the markers according to status instead of technology type (you might want to use the colour palette from `d3-dot`)
*   only show Solar photovoltaic applications.

Visit the Appendix for solutions.

# 7\. Data Stories

A data story is a document that presents data using a mix of narrative and data visualisation. It aims to present findings and conclusions in a memorable and compelling manner.

In this chapter I show how to build a data story using HTML, CSS, JavaScript, Chart.js and Leaflet. These techniques can also be used to build data reports (which focus more on providing objective and detailed information).

I step through the code of a data story 'Battery Storage Charging Ahead' which explores the growth of battery storage installations (which store electricity from intermittent sources such as wind and solar).

You can visit a live version of the data story at [http://jsvis-data-story.surge.sh](http://jsvis-data-story.surge.sh).

![data story](images/data-story.png)

Figure 45\. Battery Storage data story

The data story shows a number of charts and a map showing the locations of the battery installations. Each chart has explanatory text and the piece as a whole reads like a story. The data story is styled using alternating background colours to give the piece more visual variety. Most of the content has left and right margins except for the map which is full width.

This data story is built in a similar manner to the `chartjs-various` project where several Chart.js charts were added to a single HTML page. We also add a map and explanatory text and we pay additional attention to the layout and styling.

At the end of this chapter I show how to publish the data story onto the web for free using [surge.sh](https://surge.sh/).

## 7.1\. 'Battery Storage Charging Ahead' data story project

The data story project is built using Vite and follows a similar structure to the `chartjs-various` project. The data story consists of four Chart.js charts (a bar chart, a multi-line chart, a doughnut chart and another bar chart) and a Leaflet map.

To run the project navigate to the `data-story` project directory and call `npm install`. Call `npm run dev` to start the application server. This will give you a url (usually [http://localhost:5173](http://localhost:5173)) to visit. You should see the data story when you visit this URL.

```
cd data-story

npm install

npm run dev
```

### 7.1.1\. File structure

The project directory has the following structure:

```
data-story/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

Listing 42\. data-story project files

The project was built using Vite so has the standard Vite file structure. The REPD data is in the `public` directory. All the JavaScript code is in `main.js`.

The main project files are `index.html`, `main.js` and `style.css`. Most of the content is in `index.html` which contains the explanatory text and containers for the charts and map. The main job of the JavaScript file `main.js` is to create the four charts and the map.

### 7.1.2\. index.html

`index.html` contains the explanatory text and containers for the charts and map. It’s a big file so let’s start by looking at an outline:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="#" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Battery Storage Charging Ahead</title>
  </head>
  <body> ①
    <div id="content">
      <section> ②
          ...
      </section>
      <section class="dark"> ③
          ...
      </section>
      <section> ④
          ...
      </section>
      <section class="map"> ⑤
          ...
      </section>
      <section> ⑥
          ...
      </section>
      <section class="dark"> ⑦
          ...
      </section>
    </div>
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

Listing 43\. data-story/index.html

1.  *①* The `<body>` tag of `index.html` contains multiple sections. Each section contains text and a chart or map.
2.  *②* The first section contains text and a bar chart.
3.  *③* The second section contains some text and a line chart. It has a class attribute with value `'dark'` to give this section a dark theme.
4.  *④* This section contains a small amount of text.
5.  *⑤* This section contains the map and its class attribute of `'map'` causes it to be full width.
6.  *⑥* This section contains text and the doughnut chart.
7.  *⑦* The last section also uses a dark theme and contains text and a bar chart.

Each section contains a `<div class="inner">` element which wraps the text and chart content:

```
<section>
  <div class="inner"> ①
    <h1>Battery storage charging ahead</h1>
    <p>The need to switch to low-carbon energy production...</p>
    ...
    <div class="chart-wrapper">
      <canvas id="chart-1"></canvas>
    </div>
  </div>
</section>
```

1.  *①* This wrapper element lets us set the width of a section’s text and charts.

Let’s look at each section in turn.

* * *

#### Section 1 (Text and bar chart)

```
<section>
  <div class="inner">
    <h1>Battery storage charging ahead</h1>
    <p>The need to switch to low-carbon energy production...</p>
    <p>Typically electricity needs to be produced on demand...</p>
    <p>This is where battery storage technology can help.</p>
    <h3>Battery storage technology</h3>
    <p>If solar panel and wind turbine production exceeds demand...</p>
    <p>The UK's Renewable Energy Planning Database (REPD) records...</p>
    <div class="chart-wrapper">
      <canvas id="chart-1"></canvas>
    </div>
  </div>
</section>
```

Listing 44\. data-story/index.html

This section contains the main title, introductory text and the first bar chart. As usual for a Chart.js chart we wrap the `<canvas>` element in a `<div>` wrapper so that we can fix its height.

![data story section 1](images/data-story-section-1.png)

Figure 46\. Data story section 1 (text and bar chart)

* * *

#### Section 2 (Text and line chart, dark theme)

```
<section class="dark">
  <div class="inner">
    <p>Battery storage ranks third in terms of the number of planning...</p>
    <div class="chart-wrapper">
      <canvas id="chart-2"></canvas>
    </div>
    <p>While most technologies saw a plateau or decline in applications...</p>
  </div>
</section>
```

Listing 45\. data-story/index.html

This section contains more text and the container for the line chart. This section has a dark background so it has a class attribute of `'dark'`.

![data story section 2](images/data-story-section-2.png)

Figure 47\. Data story section 2 (text and line chart with dark theme)

* * *

#### Section 3 (Text)

```
<section>
  <div class="inner">
    <p>Battery storage technology is scattered throughout the UK. Teal indicates battery installations in operation. ...</p>
  </div>
</section>
```

Listing 46\. data-story/index.html

This is just a short section that introduces the map.

![data story section 3](images/data-story-section-3.png)

Figure 48\. Data story section 3 (just some text)

* * *

#### Section 4 (Map)

```
<section class="map">
  <div class="inner">
    <div id="map"></div>
  </div>
</section>
```

Listing 47\. data-story/index.html

This section is for the map. A `<div>` container with an id of `'map'` is added for the Leaflet map. The section has a class attribute of `'map'` (and associated CSS in `style.css` to make the map span the full width of the page).

![data story section 4](images/data-story-section-4.png)

Figure 49\. Data story section 4 (map)

* * *

#### Section 5 (Text and doughnut chart)

```
<section>
  <div class="inner">
    <p>Although there's been an marked increase in applications for battery installations...</p>
    <div class="chart-wrapper">
      <canvas id="chart-3"></canvas>
    </div>
  </div>
</section>
```

Listing 48\. data-story/index.html

This section contains some text and a container for the doughnut chart.

![data story section 5](images/data-story-section-5.png)

Figure 50\. Data story section 5 (text and doughnut chart)

* * *

#### Section 6 (Text and bar chart)

```
<section class="dark">
  <div class="inner">
    <p>According to the REPD, granting an application can take over 11 years...</p>
    <div class="chart-wrapper">
      <canvas id="chart-4"></canvas>
    </div>
  </div>
</section>
```

Listing 49\. data-story/index.html

The final section contains some text and a container for the final bar chart. The section has a dark background so has a class attribute of `'dark'`.

![data story section 6](images/data-story-section-6.png)

Figure 51\. Data story section 6 (text and bar chart with dark theme)

* * *

### 7.1.3\. style.css

Most of `style.css` is concerned with sizing each section. Let’s look at the first few lines:

```
@import 'leaflet/dist/leaflet.css'; ①

body {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
  background-color: #F9F7EB; ②
  margin: 0;
}

section { ③
  display: flex;
  justify-content: center;
}

section div.inner {
  width: 100%; ④
  max-width: 1000px; ④
  padding: 2rem 1rem; ⑤
  box-sizing: border-box; ⑤

/* ... */
}
```

Listing 50\. data-story/style.css

1.  *①* Import Leaflet’s CSS file (this way of importing a CSS file is supported by Vite).
2.  *②* Set the background colour of the whole document.
3.  *③* Set each section’s display to `flex` and its `justify-content` to `center` so that the section’s content is horizontally centered. You can learn more about CSS’s Flexbox model in the Fundamentals of HTML, SVG, CSS and JavaScript for Data Visualisation book.
4.  *④* Set the width of each section’s `<div class="inner">` element to 100% so that the section content fills the page width. The maximum width is set to 1000px so that the content doesn’t become too wide on wider screens.
5.  *⑤* Add some padding around the section’s content and set the `box-sizing` to `border-box` so that the padding is included in the width measurement.

* * *

Here’s the remainder of `style.css`:

```
/* ... */

section.dark {
  background-color: #222; ①
  color: white; ①
}

.chart-wrapper {
  height: 700px; ②
  padding: 2rem 0; ③
}

section.map div.inner {
  max-width: none; ④
  padding: 0;
}

#map {
  height: 50rem; ⑤
}
```

Listing 51\. data-story/style.css

1.  *①* Set the background colour of sections with class attribute of `dark` to a dark grey and the text colour to white.
2.  *②* Set the height of the Chart.js wrapper elements. This sets the height of each Chart.js chart.
3.  *③* Add vertical padding to the chart wrappers.
4.  *④* Earlier on we set the `max-width` property of the inner elements to `1000px`. We want the map to be full width so we set `max-width` to `none`.
5.  *⑤* Set the height of the map to `50rem`.

* * *

### 7.1.4\. main.js

`main.js` loads the data and draws the charts and map. It has a similar form to `main.js` in the `chartjs-various` project.

Let’s look at the first few lines:

```
import { tidy, count, filter, sort, desc, groupBy, summarize, mean } from '@tidyjs/tidy'; ①
import Chart from 'chart.js/auto';
import L from 'leaflet';
import uniq from 'lodash-es/uniq';
import { min, max } from 'd3-array';
import { scaleSqrt } from 'd3-scale';

import './style.css'; ②

Chart.defaults.maintainAspectRatio = false; ③
Chart.defaults.plugins.legend.display = false;
Chart.defaults.scale.title.font = {size: 16};
Chart.defaults.plugins.title.display = true;
Chart.defaults.plugins.title.font.size = 20;

let grey = '#999'; ④
let lightGrey = '#CCC';
let yellow = '#F5CF29';
let teal = '#19A0AA';

let statusPalette = {
  'Operational': teal,
  'Application Withdrawn': lightGrey,
  'Application Refused': lightGrey,
  ...
};
```

Listing 52\. data-story/main.js

1.  *①* At the top of `main.js` are the module imports. We import functions from tidy.js for data transformation and statistical calculations, the chart constructor from Chart.js, the Leaflet main object, the `uniq` function from Lodash and functions from D3 for creating a square root scale (for sizing the map’s circle markers).
2.  *②* Import `style.css`. This is non-standard JavaScript (you can’t import CSS files in standard JavaScript) but is supported by Vite.
3.  *③* Set various Chart.js global default options to save us having to set the same options on each chart. The first one `maintainAspectRatio` lets the charts adapt to the width of the content area while keeping the height fixed.
4.  *④* Create a colour palette object `statusPalette` for the map and doughnut colour scheme.

* * *

Now that the defaults and colour palette have been defined we define the main functions:

```
...

function getMultiSeriesChartData(data, seriesProp, labelProp) { ... } ①

function drawChart1(data) { ... } ②
function drawChart2(data) { ... } ③
function getMapTooltipContent(d) { ... } ④
function drawMap(data) { ... } ⑤
function drawChart3(data) { ... } ⑥
function drawChart4(data) { ... } ⑦

function draw(data) { ⑧
  drawChart1(data);
  drawChart2(data);
  drawMap(data);
  drawChart3(data);
  drawChart4(data);
}

fetch('./repd.json') ⑨
  .then(res => res.json())
  .then(data => draw(data));
```

Listing 53\. data-story/main.js

1.  *①* `getMultiSeriesChartData` (copied from the `chartjs-various` project) generates a multi-series `data` object that we can pass to Chart.js. It’s used by `drawChart2` to generate the data object for the multi-line chart.
2.  *②* `drawChart1` draws the first bar chart.
3.  *③* `drawChart2` draws the multi-line chart.
4.  *④* `getMapTooltipContent` is used by `drawMap` to populate the map tooltips.
5.  *⑤* `drawMap` draws the Leaflet map.
6.  *⑥* `drawChart3` draws the doughnut chart.
7.  *⑦* `drawChart4` draws the final bar chart.
8.  *⑧* `draw` is the main draw function that calls the draw functions for each chart.
9.  *⑨* Request the REPD data and when it arrives convert it into a JavaScript object and call `draw`.

* * *

#### drawChart1

`drawChart1` draws the first bar chart which shows the number of planning applications by technology type:

![data story chart 1](images/data-story-chart-1.png)

Figure 52\. Bar chart (number of planning applications by technology)

* * *

Here’s the function:

```
function drawChart1(data) {
  let summary = tidy( ①
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart-1', { ②
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology), ③
      datasets: [{
        data: summary.map(d => d.n), ④
        backgroundColor: summary.map(d => d.technology === 'Battery' ? teal : '#999') ⑤
      }]
    },
    options: {
      indexAxis: 'y', ⑥
      scales: {
        x: {
          title: {
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of planning applications (by technology) 1990-2022',
        }
      }
    }
  });
}
```

Listing 54\. data-story/main.js

1.  *①* Create a count (by technology) summary of the REPD data.
2.  *②* Create the chart, using the `<div>` element with id `chart-1` as the container.
3.  *③* Use the `technology` property of the summary data as the chart labels (these are the technology names).
4.  *④* Use the `n` property of the summary data as the data values (these are the counts).
5.  *⑤* Set the bar colour to grey, except for Battery technology for which we use `teal` (which is defined near the top of the file).
6.  *⑥* Set `indexAxis` to `y` for a horizontal bar chart.

`drawChart1` is very similar to `drawChart1` in the `chartjs-various` project. The main difference is that the bar colours are set to grey except for Battery which is set to `teal` which we define near the top of the file. Using a variable to represent a colour is a handy technique because it ensures colour consistency and if we did want to change the colour we only need to change a single hex code.

#### drawChart2

`drawChart2` draws the multi-line chart which shows the number of planning application submissions across time, broken down by technology type.

![data story chart 2](images/data-story-chart-2.png)

Figure 53\. Multi-line chart (planning applications over time)

`drawChart2` is similar to `drawChart3` in the `chartjs-various` project. The main differences are the style of the chart’s lines (which highlight Battery technology) and the axis style (which adapts to the dark theme).

* * *

Here’s `drawChart2` with the options object truncated:

```
function drawChart2(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted'); ①

  // Add style to each series
  chartData.datasets.forEach(series => { ②
    let color = series.label === 'Battery' ? teal : '#999'; ③
    series.backgroundColor = color;
    series.radius = 2;
    series.borderColor = color;
    series.borderWidth = 1.5;
    series.borderDash = series.label === 'Battery' ? [] : [1,1]; ④
  });

  const myChart = new Chart('chart-2', {
    type: 'line',
    data: chartData, ⑤
    options: { ... }
  });
}
```

Listing 55\. data-story/main.js

1.  *①* Call `getMultiSeriesChartData` and pass in the data, `technology` as the series property and `yearSubmitted` as the axis label property.
2.  *②* This loop sets the style of each series.
3.  *③* Set the line colour to grey unless the technology type is Battery.
4.  *④* `borderDash` defines whether the line is solid, dotted or dashed. An empty array specifies a solid line. Otherwise the array’s first value sets the length of the dots or dashes and the second value sets the length of the gaps between the dots and dashes. If the technology type is Battery draw a solid line otherwise draw a dotted line.
5.  *⑤* Use the `chartData` object returned by `getMultiSeriesChartData` as the `data` value of the chart’s configuration object.

* * *

Here’s the options object of `drawChart2`:

```
{
  scales: {
    x: {
      title: {
        display: true,
        text: 'Year',
        color: '#eee'
      },
      ticks: {
        color: '#ccc' ①
      },
      grid: {
        color: '#555' ①
      }
    },
    y: {
      title: {
        display: true,
        text: 'Number of applications',
        color: '#eee' ①
      },
      ticks: {
        color: '#ccc' ①
      },
      grid: {
        color: '#333' ①
      }
    }
  },
  plugins: {
    title: {
      text: 'Battery applications compared with other renewables 1990-2022',
      color: '#eee' ①
    },
    legend: {
      display: false
    }
  }
}
```

Listing 56\. data-story/main.js

1.  *①* This chart uses a dark theme so we need to set the axis ticks and labels to lighter colours and grid lines to darker colours.

* * *

#### drawMap

`drawMap` draws the map. Circle markers are added to represent each battery application.

![data story map](images/data-story-map.png)

Figure 54\. Map showing battery application locations

* * *

Here’s the first few lines of the function:

```
function drawMap(data) {
  let filteredData = tidy( ①
    data,
    filter(d => d.technology === 'Battery'),
    sort(desc('capacity'))
  );

  let map = L.map('map', { ②
    scrollWheelZoom: false ③
  });

  L.tileLayer('https://tiles.stadiamaps.com/tiles/alidade_smooth/{z}/{x}/{y}{r}.png', { ④
    maxZoom: 20,
    attribution: '...',
  }).addTo(map);

  map.setView([55, -2], 6); ⑤

  let maxCapacity = max(filteredData, d => d.capacity); ⑥
  let maxRadius = 30;
  let radiusScale = scaleSqrt().domain([0, maxCapacity]).range([5, maxRadius]); ⑦

  ...
}
```

Listing 57\. data-story/main.js

1.  *①* Start by filtering the REPD data so only battery applications are included.
2.  *②* Create a map by calling Leaflet’s `map` method and passing in the id of the map container.
3.  *③* Disable the scroll wheel zoom (to make it easier for the user to scroll up and down the page).
4.  *④* Add the tile layer and add it to the map.
5.  *⑤* Set the map’s view.
6.  *⑥* Compute the maximum of the capacity property within the filtered data.
7.  *⑦* Create a square root scale function using D3.

* * *

Next in `drawMap` we add the circle markers:

```
function drawMap(data) {
  ...

  filteredData.forEach(d => { ①
    if (d.lat === null || d.lon === null) return; ②
    let marker = L.circleMarker([d.lat, d.lon]); ③
    let radius = radiusScale(d.capacity || 0); ④
    let color = statusPalette[d.status] || '#aaa'; ⑤

    marker.setStyle({ ⑥
      radius: radius,
      fillColor: color,
      fillOpacity: 0.75,
      weight: 1,
      opacity : 1,
      color: color
    });

    marker.bindTooltip(getMapTooltipContent(d)); ⑦
    marker.addTo(map); ⑧
  });
}
```

Listing 58\. data-story/main.js

1.  *①* Loop through the filtered data.
2.  *②* If the current item doesn’t have a latitude or longitude return early.
3.  *③* Create a circle marker.
4.  *④* Compute the radius of the circle marker.
5.  *⑤* Compute the colour of the circle marker using `statusPalette` defined near the top of the file.
6.  *⑥* Set the marker’s style.
7.  *⑦* Add tooltip content to the marker.
8.  *⑧* Add the marker to the map.

This function is similar to the `draw` function in the `leaflet-map` project. The main difference is that the data is filtered to include only Battery planning applications.

The `getMapTooltipContent` is similar to the one in the `leaflet-map` project. Consult the 'Data-driven maps with Leaflet' chapter for a walk through of this and the `draw` function.

* * *

#### drawChart3

`drawChart3` draws a doughnut chart that shows the number of battery planning applications broken down by status.

![data story chart 3](images/data-story-chart-3.png)

Figure 55\. Doughnut chart showing battery applications by status

* * *

The function looks like:

```
function drawChart3(data) {
  let summary = tidy( ①
    data,
    filter(d => d.technology === 'Battery'),
    count('status', {sort: true})
  );

  const myChart = new Chart('chart-3', {
    type: 'doughnut', ②
    data: { ③
      labels: summary.map(d => d.status),
      datasets: [{
        data: summary.map(d => d.n),
        backgroundColor: summary.map(d => statusPalette[d.status]) ④
      }],
    },
    options: {
      plugins: {
        title: {
          text: 'Status of battery planning applications in 2022',
        },
        legend: {
          display: true
        }
      }
    }
  });
}
```

Listing 59\. data-story/main.js

1.  *①* Use tidy.js to filter by technology type (to include only Battery applications) then count the number of applications for each status code.
2.  *②* Set the chart type to `'doughnut'`.
3.  *③* The data structures are the same as for bar charts. Chart.js automatically calculates the percentages for the doughnut chart.
4.  *④* Use the `statusPalette` colour object to set the segment colours.

By now this function should feel quite familiar. We use tidy.js to extract the data we require then create a chart using Chart.js. The main difference with this chart is its type is `'doughnut'`. One of the great things about Chart.js is that we only needed to change the chart’s type to create a doughnut chart. (The `data` configuration object remains the same.)

* * *

#### drawChart5

The final chart is a bar chart that shows the average time to grant a planning application, broken down by technology type.

![data story chart 4](images/data-story-chart-4.png)

Figure 56\. Bar chart showing average time to grant a planning application

The REPD data contains a property `daysUntilGranted` which is the number of days between the `dateSubmitted` and `dateGranted` dates. (This property was added by the script that converted the original REPD CSV file into a JSON file. See the `wrangling` project.) We use tidy.js to compute the mean number of days for each technology type.

The chart itself is straightforward, the main difference being its dark theme and the bar representing Battery technology is highlighted.

* * *

Here’s the code (with the options object truncated):

```
function drawChart4(data) {
  let summary = tidy(
    data,
    filter(d => d.daysUntilGranted !== null), ①
    groupBy('technology', [ ②
      summarize({
        meanDaysUntilGranted: mean('daysUntilGranted')
      })
    ]),
    sort('meanDaysUntilGranted') ③
  );

  const myChart = new Chart('chart-4', { ④
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.meanDaysUntilGranted), ⑤
        backgroundColor: summary.map(d => d.technology === 'Battery' ? teal: '#777') ⑥
      }]
    },
    options: { ... }
  });
}
```

Listing 60\. data-story/main.js

1.  *①* Use tidy.js to filter out applications whose `daysUntilGranted` equals `null`. (These are mostly applications that haven’t been granted yet.)
2.  *②* Use tidy.js’s `groupBy` function to group the filtered applications by technology type and compute the mean `daysUntilGranted` for each group. (We covered `groupBy` in the 'Make a Chart with Chart.js' chapter.)
3.  *③* Sort the applications by `meanDaysUntilGranted`.
4.  *④* Create a chart in the usual manner.
5.  *⑤* The data values are based on the `meanDaysUntilGranted` property in `summary`.
6.  *⑥* Set the bar colour to grey, unless the technology type is Battery.

* * *

The option objects looks like:

```
{
  scales: {
    y: {
      title: {
        display: true,
        text: 'Days until application granted',
        color: '#eee'
      },
      ticks: {
        color: '#ccc'
      },
      grid: {
        color: '#555'
      }
    },
    x: {
      ticks: {
        color: '#ccc'
      },
      grid: {
        color: '#333'
      }
    }
  },
  plugins: {
    title: {
      text: 'Average time to grant applications (by technology) 1990-2022',
      color: '#eee'
    }
  }
}
```

Listing 61\. data-story/main.js

Most of the options are to make the axis ticks and gridlines light against the dark background.

* * *

The biggest difference in `drawChart4` is the data transformation at the beginning of the function. This uses tidy.js to filter out applications without a valid `daysUntilGranted` value and to group by technology. The mean `daysUntilGranted` is then computed on each group and then the groups are sorted by `meanDaysUntilGranted.`

The output of this transformation looks like:

```
[
  {
    "technology": "Compressed Air Energy Storage",
    "meanDaysUntilGranted": 71
  },
  {
    "technology": "Liquid Air Energy Storage",
    "meanDaysUntilGranted": 138.5
  },
  {
    "technology": "Biomass (co-firing)",
    "meanDaysUntilGranted": 140
  },
  ...
]
```

Each technology type is represented by an object that has a `meanDaysUntilGranted` property. This is a similar data structure to the one used for previous summary charts, the main difference is that we have a `meanDaysUntilGranted` property instead of an `n` property.

The remainder of the function should by now be fairly familiar. If not, have another read through the 'Styling and Customising Chart.js' chapter, in particular functions `drawChart1` and `drawChart2`.

We’ve now covered all the data story code.

* * *

## 7.2\. Publishing the Data Story

This section shows how the data story can be published to the web using [surge.sh](https://surge.sh/). This is a free service that copies a static website (a website that doesn’t rely on a web server to dynamically generate files) onto a server so that anyone can visit the URL and see the data story.

There’s three steps to publishing the data story:

1.  Install surge if it isn’t already installed.
2.  Build a production version of the data story.
3.  Deploy the data story using surge.

To install surge use:

```
npm install --global surge
```

To build a production version of a Vite application navigate to the project directory on the command line (`cd data-story`) and type:

```
npm run build
```

This creates a new directory `dist` and adds the production version of the application to it. (The production version is an optimised version of your application that’s suitable for uploading to a static web server.)

Next navigate to the `dist` directory and type `surge`:

```
cd dist
surge
```

Surge prompts you with a few questions. Usually it asks you for the project’s location. It uses the current directory as the default location, so just press enter here.

It then asks for the URL of the data story. It usually provides one for you (usually a funny name) but you can rename the part before `.surge.sh` to whatever you like. Surge then copies your data story to its servers and gives you its URL. Click on the URL (or copy it and paste into a web browser) and you should see the published version of the data story. (I’ve published my version to [http://jsvis-data-story.surge.sh/](http://jsvis-data-story.surge.sh/))

* * *

If you’ve tried to publish your own version you’ll probably find the map doesn’t have map tiles.

![data story no map tiles](images/data-story-no-map-tiles.png)

Figure 57\. Unregistered Stadia map

This is because the map tile provider Stadia requires you to register the URL of any site that’s using their map tiles. This is so that they can keep track of how many times the tiles are being served. If it exceeds the free-tier limits they’ll start charging.

To register your own URL with Stadia create an account at [https://client.stadiamaps.com/signup/](https://client.stadiamaps.com/signup/) then use the `Create a Property` button to add your URL. I found that I had to put the full domain in the 'Domain' section rather than splitting the subdomain and domain. I don’t know why!

![stadia prop](images/stadia-prop.png)

Figure 58\. Stadia dashboard property

## 7.3\. Wrapping up

This chapter showed how to create a data story containing text, charts and a map. The approach is deliberately simple so that you can create your own data story with a reasonable understanding of HTML, CSS and JavaScript.

The chapter also showed how to deploy the data story to the web using surge.sh. This means you’re able to create and publish a data story for free. (Although bear in mind the map tiles might have a cost.)

# Appendix A: Creating a project with Vite

Creating a project using Vite is relatively straightforward. You do need to have Node installed on your computer. You can check this by running the following on the command line:

```
node -v
```

It should return the Node version that’s installed on your computer. Vite requires Node version 14.18 or 16 upwards so ensure one of these is installed.

In the command line navigate to a directory where you save your projects and type:

```
npm create vite@latest
```

If you’re asked whether to install `create-vite@latest` answer yes.

Vite will ask a few questions about your new project such as the project name.

When it asks you to select a framework answer Vanilla unless you’re wanting to use a framework such as Vue or React. When it asks which variant, select JavaScript, unless you’re specifically wanting to use TypeScript. (This book doesn’t use TypeScript.)

Vite creates a new project directory and gives you the instructions of how to navigate to the new directory. For example:

```
cd my-project
```

Once you’re in your new project directory type `npm install` to download the project’s dependencies then `npm run dev` to build the project and start the development server.

* * *

Vite will display a URL where you can visit your application. This is usually `localhost:5173`. If you visit this URL in your web browser you should see:

![vite](images/vite.png)

Figure 59\. The Vite default project

The default project is a simple counter application. When you click the button the counter increments.

The project has the following file structure:

```
my-project/
  counter.js
  index.html
  javascript.svg
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    vite.svg
  style.css
```

* * *

It’s nice that Vite creates a working application for you but it does mean there’s a few files that you probably don’t need when you start developing your own application. These are:

*   `counter.js`
*   `javascript.svg`
*   `public/vite.svg`

Generally I delete these files and any code that imports them (in `index.html` and `main.js`). Most of `main.js` can also be removed.

The files that are usually retained are:

| Filename | Description |
| --- | --- |
| `index.html` | The main HTML file. This contains static content and container elements for JavaScript generated content. |
| `main.js` | The JavaScript entry point. This is the first file to run when the application loads. |
| `style.css` | The main CSS file. It can either be included in `index.html` using a `link` tag or imported by a JavaScript file. (Importing CSS files from a JavaScript file isn’t standard JavaScript but Vite supports this.) |
| `public` | A directory that acts as the root directory (`/`) on the web server. This enables your own files to be included by `index.html` or files (such as a CSV or JSON file) to be loaded using JavaScript. |
| `package.json` | The main project configuration file. One of the main things this file does is specify any third party packages (such as Chart.js and D3) the the project depends on. |

`node_modules` is a standard directory that contains third party packages (such as Chart.js or D3) that are listed as dependencies in `package.json`.

`package-lock.json` is a file that’s created by `npm` that lists exactly what’s been installed in the project and is used to ensure anyone working on the project has exactly the same package versions installed. You don’t need to think about this file at all for the purposes of this book.

Unfortunately Vite doesn’t seem to let you create a barebones project. The closest is the Vanilla option which creates the counter application. This means we need to strip away code that we don’t need. For each of the projects in this book we:

*   remove `counter.js`
*   in `main.js` just retain the first line (the `style.css` import)
*   remove `javascript.svg` and `public\vite.svg` files
*   remove the line containing `vite.svg` in `index.html`
*   remove all the CSS in `style.css` except for `body` element rule

This leaves us with a barebones application.

# Appendix B: getMultiSeriesChartData

This section explains how the function `getMultiSeriesChartData` works. It’s used in the `chartjs-various` and `data-story` projects.

The purpose of the function is to create a Chart.js data object for a multi-series chart given an array of data.

It takes three arguments:

1.  The REPD data array
2.  The data property that defines the names of each series.
3.  The data property that defines the axis labels.

If called with the following arguments:

```
getMultiSeriesChartData(data, 'technology', 'yearSubmitted');
```

it returns an object that looks like:

```
{
  labels: [1990, 1991, 1992, ... 2020, 2021, 2022],
  datasets: [
    {
      label: "Advanced Conversion Technologies",
      data: [0, 0, 0, ... 0, 0, 0]
    },
    {
      label: "Anaerobic Digestion",
      data: [0, 0, 0, ... 10, 17, 22]
    }
    ,
    ...
  ]
}
```

* * *

We assign the output of `getMultiSeriesChartData` to the `data` property in the Chart.js configuration object. For example:

```
let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted');

const myChart = new Chart('my-chart', {
  type: 'line',
  data: chartData,
  options: { ... }
});
```

Here’s the function:

```
function getMultiSeriesChartData(data, seriesProp, labelProp) { ①
  let seriesNames = uniq(data.map(d => d[seriesProp])) ②
      .filter(d => d !== '')
      .sort();

  let labelNames = uniq(data.map(d => d[labelProp])) ③
      .filter(d => d !== '')
      .sort();

  let chartData = { ④
    labels: labelNames,
    datasets: seriesNames.map(series => { ⑤
      return {
        label: series,
        data: []
      };
    })
  };

  // Add data to each series
  chartData.datasets.forEach(series => { ⑥
    series.data = labelNames.map(label => { ⑦
      let items = data.filter(d => { ⑧
        return d[seriesProp] === series.label && d[labelProp] === label;
      });
      return items.length;
    });
  });

  return chartData;
}
```

1.  *①* `getMultiSeriesChartData` accepts three arguments: `data` (the data array), `seriesProp` (the property e.g. `'technology'` from which we derive the series names) and `labelProp` (the property e.g. `'yearSubmitted'` from which we derive the labels along the main axis).
2.  *②* Create an array of the series names. We use lodash’s `uniq` function that takes an array and outputs a copy of the array with duplicates removed. We also filter the arrays to remove blanks and sort the arrays in ascending order.
3.  *③* Create an array of the label names in a similar manner to `seriesNames`.
4.  *④* Create and initialise the chart data object.
5.  *⑤* Create the `datasets` array by calling the `map` method on `seriesNames`. Each element of this array represents a data series. Each series has two properties `label` (the series name) and `data` (an array of numbers).
6.  *⑥* Iterate through each series.
7.  *⑦* For each series call the `map` method on the `labelNames` array to create an array where each element is the number of planning applications for this series and a particular label name.
8.  *⑧* To count the number of items filter the data for items that match `series` and `label` and return the array length.

# Appendix C: Data Wrangling

This appendix shows how the REPD data was converted from the original CSV download into the `repd.json` JSON file. This section isn’t intended as a full tutorial on data wrangling, but you’ll pick up plenty of tips that will help you transform your own data.

The `wrangling` directory contains a Node.js project that converts the original REPD CSV file into a JSON file.

To run the script, navigate to the `wrangling` directory, install the Node modules and run the script:

```
cd wrangling
npm install
node index.js
```

The `wrangling` directory contains `repd-january-2023.csv` which was downloaded from [www.gov.uk](https://www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract).

The steps the script performs are:

1.  Loads the CSV file.
2.  Converts it into a JavaScript array using D3.
3.  Carries out some data processing.
4.  Saves the data as a JSON file.

* * *

Let’s look the first few lines where the script loads the CSV file and turns it into a JavaScript array:

```
const fs = require('fs'); ①
const d3 = require('d3'); ②
const OSPoint = require('ospoint'); ③

let f = fs.readFileSync('repd-january-2023.csv', 'utf8'); ④
let data = d3.csvParse(f); ⑤
```

Listing 62\. wrangling/index.js

1.  *①* Import the `fs` module. This contains the methods `readFileSync` for reading in files and `writeFileSync` for saving files. Note that unlike the other projects in this book we using the CommonJS module system to import modules which means we use `require` instead of `import`.
2.  *②* Import D3.js so that we can use its `csvParse` method. This converts a CSV text string into an array of objects.
3.  *③* Import the [`ospoint`](https://www.npmjs.com/package/ospoint) library which converts Ordnance Survey grid points (northings and eastings) into latitude and longitude. The REPD CSV file specifies the location of each planning application using Ordnance Survey eastings and northings and this library helps us convert them into longitude and latitude.
4.  *④* Load the REPD CSV file using `readFileSync`. This method returns a string containing the CSV and it’s assigned to the variable `f`.
5.  *⑤* Use D3’s `csvParse` method to convert the CSV string into a JavaScript array of objects. `csvParse` is a handy function that takes a CSV string and converts it into an array of objects. Each column in the CSV file maps to a property in each object.

* * *

The array `data` is an array of objects where each object represents a single planning application (or a single row in the CSV file). Each object has properties, each of which corresponds to a column in the CSV file. `data` looks something like:

```
[
  {
    'Old Ref ID': 'N00053B',
    'Ref ID': '1',
    'Record Last Updated (dd/mm/yyyy)': '07/07/2009',
    'Operator (or Applicant)': 'RWE npower',
    'Site Name': 'Aberthaw Power Station Biomass',
    'Technology Type': 'Biomass (co-firing)',
    'Storage Type': '',
    'Storage Co-location REPD Ref ID': '',
    'Installed Capacity (MWelec)': '35',
    'CHP Enabled': 'No',
    'RO Banding (ROC/MWh)': '',
    'FiT Tariff (p/kWh)': '',
    'CfD Capacity (MW)': '',
    ...
  },
 {
    'Old Ref ID': 'AA110',
    'Ref ID': '2',
    'Record Last Updated (dd/mm/yyyy)': '20/11/2017',
    'Operator (or Applicant)': 'Orsted (formerly Dong Energy) / Peel Energy',
    'Site Name': 'Hunterston - cofiring',
    'Technology Type': 'Biomass (co-firing)',
    'Storage Type': '',
    'Storage Co-location REPD Ref ID': '',
    'Installed Capacity (MWelec)': '170',
    'CHP Enabled': 'No',
    'RO Banding (ROC/MWh)': '',
    'FiT Tariff (p/kWh)': '',
    'CfD Capacity (MW)': '',
    ...
  }
  ...
]
```

We don’t use all of these properties so the script will pick out the properties that we require for the charts in this book. Each planning application has a location but it’s specified in Ordnance Survey eastings and northings. It’s much more common to use latitude and longitude (for example, that’s what Leaflet uses) so we’ll convert each easting/northing pair into latitude and longitude. We also rename the properties to use shorter names as this makes our project code a bit clearer and easier to write.

* * *

Note that numbers are represented by strings. For example look at the `'Installed Capacity (MWelec)'` property whose values are `'35'` and `'170'` in the above snippet. Therefore there’ll be an additional step to convert these strings into numbers.

Now that we’ve converted the CSV data into an array of objects we’ll iterate through it using JavaScript’s `map` method to create a new, transformed array of data. Let’s look at the first few lines:

```
let output = data.map((d, i) => { ①
  let ret = {}; ②

  ret.id = d['Ref ID']; ③
  ret.name = d['Site Name']; ④
  ret.technology = d['Technology Type']; ⑤
  ret.capacity = parseFloat(d['Installed Capacity (MWelec)']); ⑥

  ...

  return ret;
});
```

Listing 63\. wrangling/index.js

1.  *①* Use JavaScript’s `map` method to create a new array of data. For each iteration `d` is an object representing a single planning application.
2.  *②* Create an empty object. We’ll populate this object with the properties we require in our charts and will return it at the end of this function.
3.  *③* Set the id. This is a good example why we’re renaming the properties. It’s much easier to write `d.id` instead of `d['Ref ID']`.
4.  *④* Set the name of the planning application.
5.  *⑤* Set the technology type.
6.  *⑥* Set the capacity. Numbers are represented by strings so we need to convert the capacity into a number using JavaScript’s built-in `parseFloat`.

* * *

The next step is to convert the location (represented by the `'Y-coordinate'` and `'X-coordinate'` properties) into latitude and longitude:

```
let output = data.map((d, i) => {
  ...

  let point = new OSPoint(d['Y-coordinate'], d['X-coordinate']); ①
  let lonLat = point.toWGS84(); ②

  ret.lon = parseFloat(lonLat.longitude.toFixed(3)); ③
  ret.lat = parseFloat(lonLat.latitude.toFixed(3)); ④

  ...
});
```

Listing 64\. wrangling/index.js

1.  *①* Create a new OSPoint instance by passing the northing (`d['Y-coordinate']`) and easting (`d['X-coordinate']`) into the `OSPoint` constructor function.
2.  *②* Convert the location into a longitude/latitude object and assign to `lonLat`.
3.  *③* The longitude value is referenced by `lonLat.longitude`. To reduce the size of the JSON file, we’ll just retain 3 decimal places using JavaScript’s built-in `toFixed` method. This returns a string so we convert it back into a number using `parseFloat`.
4.  *④* Get the latitude value in a similar manner to longitude.

We then create properties for region, status and operator:

```
let output = data.map((d, i) => {
  ...

  ret.region = d.Region;

  ret.status = d['Development Status (short)']; ①
  ret.operator = d['Operator (or Applicant)']; ①

  ...
});
```

Listing 65\. wrangling/index.js

1.  *①* This property contains spaces, so we use the square bracket syntax to access the property.

* * *

Next we create the temporal (time-related) properties:

```
let output = data.map((d, i) => {
  ...

  let dateParser = d3.utcParse('%d/%m/%Y'); ①

  let dateSubmitted = dateParser(d['Planning Application Submitted']); ②
  ret.yearSubmitted = dateSubmitted ? dateSubmitted.getFullYear() : null; ③
  ret.dateSubmitted = dateSubmitted ? dateSubmitted.toISOString() : null; ④

  let dateGranted = dateParser(d['Planning Permission Granted']); ⑤
  ret.yearGranted = dateGranted ? dateGranted.getFullYear() : null; ⑥

  ret.daysUntilGranted = dateSubmitted && dateGranted && dateSubmitted < dateGranted ? d3.timeDay.count(dateSubmitted, dateGranted) : null; ⑦

  return ret;
});
```

Listing 66\. wrangling/index.js

1.  *①* Create a date parser using D3’s `utcParse` method. We pass in the format of dates in the CSV data (e.g. `28/10/2015`). `utcParse` returns a function that accepts a date string in the specified format and returns a JavaScript date object. We use `utcParse` instead of D3’s `timeParse` so that the parsing is independent of daylight saving time. (The date doesn’t have a time, so 12am is assumed.)
2.  *②* Parse the application submission date and assign it to the `dateSubmitted` variable.
3.  *③* If it’s a valid date, assign its year to the `yearSubmitted` property.
4.  *④* If it’s a valid date, assign its ISO representation to the `dateSubmitted` property.
5.  *⑤* Parse the application granted date and assign it to the `dateGranted` variable.
6.  *⑥* If it’s a valid date, assign its year to the `yearGranted` property.
7.  *⑦* Compute the number of days between 'dateSubmitted' and 'dateGranted' and assign to the `daysUntilGranted` property. We use D3’s `timeDay.count` method to compute the number of days between two date objects. (There are cases where the granted date is before the submission date. If this is the case we don’t do this computation.)

* * *

Some applications don’t have a valid submission date. It’s not obvious what to do in these cases and in order to keep things simple for teaching purposes I exclude them:

```
// Exclude applications w/out a submission date
output = output.filter(d => d.dateSubmitted !== null); ①

// Just keep year submitted up to and including Dec 2022
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

Listing 67\. wrangling/index.js

1.  *①* Exclude applications without a submission date.
2.  *②* The visualisations only display data up until the end of 2022 so exclude applications that were submitted after 2022.
3.  *③* Use `JSON.stringify` to convert the array of data `output` into a JSON string representation and save it to `repd.json` using the `writeFileSync` method. `JSON.stringify` takes one argument plus two optional arguments. The first argument is the array and the third argument is the number of indentation spaces. We set the indentation to 2 to make the file human readable. Setting it to zero (or omitting the optional arguments) eliminates whitespace in the JSON string and results in a smaller file size. `writeFileSync` takes two arguments, a filename and a string. It opens or creates the file and writes the string to it.

* * *

When the script is run using `node index.js` it processes the data and writes to `repd.json`. `repd.json` looks like:

```
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

Listing 68\. wrangling/index.js

# Appendix D: Exercise hints and solution ideas

This appendix contains hints and solution ideas for the 'Ideas for Further Study' sections.

## D.1\. JavaScript and Data Visualisation

### D.1.1\. Display different fields (for example operator and/or status)

To add the `operator` property to the table:

```
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

Listing 69\. load-data/main.js

### D.1.2\. Change the filter to display a different technology type and change the capacity threshold

To show solar applications with a capacity over 50 MW:

```
// Filter
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

Listing 70\. load-data/main.js

### D.1.3\. Try displaying your own data (make sure the dataset isn’t too large, perhaps don’t go over 10Mb)

Make sure your data is in long format and saved as JSON. Also make sure numeric data are numbers (rather than strings with quote marks) in the JSON. The Data Wrangling section in the Appendix shows how the REPD CSV file was transformed into `repd.json` and it contains some handy tips on data transformation.

* * *

## D.2\. Make a Chart with Chart.js

### D.2.1\. Show the number of applications per region (instead of technology) and sort the bars alphabetically

Modify the tidy.js code to count regions instead of technology types:

```
import { tidy, count, sort } from '@tidyjs/tidy';

  ...

  let summary = tidy(
    data,
    count('region'), ①
    sort('region') ②
  );

  const myChart = new Chart('chart', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.region), ③
      datasets: [{ ... }]
    },
    options: { ... }
  });
```

Listing 71\. chart-js/main.js

1.  *①* Change the property name to `'region'` and remove the sort option (which sorts by value)
2.  *②* Add a sort command and pass in `'region'` to sort alphabetically by region. You also need to add `sort` to the `import` statement at the top of the file.
3.  *③* Use the `region` property for the labels.

* * *

### D.2.2\. Change the bar colour to `'steelblue'`

```
data: {
    labels: summary.map(d => d.region),
    datasets: [{
      data: summary.map(d => d.n),
      backgroundColor: 'steelblue' ①
    }]
},
```

Listing 72\. chart-js/main.js

1.  *①* To set the bar colour use the `backgroundColor` option in the series object.

* * *

## D.3\. Custom Charts with D3.js

### D.3.1\. Show regions along the y-axis

Create an array `regionValues` of unique region names and pass it into `yScale` as the domain:

```
// y scale
let regionValues = tidy( ①
  data,
  count('region'), ②
  sort('region') ③
).map(d => d.region); ④

let yLength = height - topMargin - bottomMargin;

let yScale = scalePoint()
    .domain(regionValues) ⑤
    .range([0, yLength]);
```

Listing 73\. d3-dot/main.js

1.  *①* Change `technologyValues` to `regionValues`.
2.  *②* Count regions instead of technologies.
3.  *③* Sort by region instead of technology.
4.  *④* Extract the region name instead of technology.
5.  *⑤* Use `regionValues` for the `yScale` domain.

Set each circle’s `cy` attribute according to the `region` property:

```
.attr('cx', d => xScale(d.dateSubmitted))
.attr('cy', d => yScale(d.region)) ①
.attr('r', d => rScale(d.capacity))
```

Listing 74\. d3-dot/main.js

1.  *①* Use region instead of technology to determine the `cy` attribute.

* * *

### D.3.2\. Change the colour scheme so that Battery applications are coloured in purple and everything else in grey

Set the circle fill and stroke according to the technology property:

```
.attr('r', d => rScale(d.capacity))
.style('fill', d => d.technology === 'Battery' ? 'purple' : '#aaa') ①
.style('stroke', d => d.technology === 'Battery' ? 'purple' : '#aaa') ①
```

Listing 75\. d3-dot/main.js

1.  *①* If technology is Battery, use purple otherwise use grey.

### D.3.3\. Add more information to the toolip

Add the operator and region to the tooltip:

```
.each(function(d) {
  let html = '';
  html += '<div>Name: ' + d.name + '</div>';
  html += '<div>Technology: ' + d.technology + '</div>';
  html += '<div>Capacity: ' + d.capacity + ' MW</div>';
  html += '<div>Operator: ' + d.operator + '</div>'; ①
  html += '<div>Region: ' + d.region + '</div>'; ②
  html += '<div>Date submitted: ' + d.dateSubmitted.toDateString() + '</div>';
  html += '<div>Status: ' + d.status + '</div>';
  tippy(this, {
    content: html,
    allowHTML: true,
    theme: 'light',
    duration: 0
  });
});
```

Listing 76\. d3-dot/main.js

1.  *①* Add the operator property to the tooltip’s HTML string.
2.  *②* Add the region property to the tooltip’s HTML string.

* * *

## D.4\. Data-driven maps with Leaflet

### D.4.1\. Colour the markers according to status instead of technology type

Add a colour palette for the status property (copied from the `d3-dot` project):

```
...
import './style.css';

let green = '#358600';
let grey = '#aaa';
let purple = '#A675A1';
let yellow = '#F5CF29';

let statusColors = {
  'Abandoned': grey,
  'Appeal Withdrawn': grey,
  'Application Refused': grey,
  'Application Submitted': purple,
  'Application Withdrawn': grey,
  'Awaiting Construction': yellow,
  'Decommissioned': grey,
  'No Application Required': yellow,
  'Operational': green,
  'Planning Permission Expired': grey,
  'Under Construction': yellow
};

function getTooltipContent(d) { ... }
```

Listing 77\. leaflet-map/main.js

Set the marker colour according to status:

```
data.forEach(d => {
  if (d.lat === null || d.lon === null) return;
  let marker = L.circleMarker([d.lat, d.lon]);
  let radius = radiusScale(d.capacity || 0);
  let color = statusColors[d.status] || '#aaa'; ①

  ...
});
```

Listing 78\. leaflet-map/main.js

1.  *①* Set the colour using the `status` property and the `statusColors` colour lookup object.

### D.4.2\. Only show Solar photovoltaic applications

Filter the data for `'Solar Photovoltaics'`:

```
map.setView([55, -2], 6);

data = data.filter(d => d.technology === "Solar Photovoltaics"); ①

let maxCapacity = max(data, d => d.capacity); ②
let maxRadius = 20;
let radiusScale = scaleSqrt().domain([0, maxCapacity]).range([3, maxRadius]);
```

Listing 79\. leaflet-map/main.js

1.  *①* Filter the data for `'Solar Photovoltaics'`.
2.  *②* `maxCapacity` will adapt to the filtered data so the maximum circle size will still be 20 even though the maximum capacity is lower.

* * *

1.  According to ChatGPT one of the earliest JavaScript charting libraries was Netscape Livewire Charts which was developed in the mid-1990s.[↩︎](#fnref1)