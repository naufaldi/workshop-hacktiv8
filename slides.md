---
theme: dracula
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  Workshop Web Fundamental
drawings:
  persist: false
defaults:
  foo: true
transition: slide-left
title: Workshop Web Fundamental
mdc: true
monaco: true
monacoTypesSource: local # or cdn or none
monacoTypesAdditionalPackages:
  - '@slidev/types'
---

# Workshop Web Fundamental

HTML,CSS and JS - Data Fetching

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>


---
layout: author
---

![image of naufaldi](https://github.com/naufaldi.png?size=100)

# Naufaldi Rafif S

I'm a passionate about creating and contributing to open source projects. I am a ReactJS enthusiast and python lover ❤️ Mainly working on [eFishery](https://efishery.com/id/) ⚛️

<footer>

<iconoir-twitter /> [@f2aldi](https://twitter.com/f2aldi)

<iconoir-github /> [@naufaldi](https://github.com/naufaldi)

<iconoir-profile-circle/> [faldi.xyz](https://faldi.xyz)

</footer>


---
layout: default
transition: fade-out
---

# Table of contents

<Toc maxDepth="1"></Toc>

---
layout: section
transition: fade-out
---

# Introduction to Web Development

---
layout: default
transition: fade-out
---

## Objectives
- Understand the basics of web development.
- Learn about HTML, CSS, and JavaScript and their roles in creating websites.
- Set up a development environment for building web applications.
- Data Fetching from API

---
layout: default
transition: fade-out
---


# Agenda

## Introduction to Web Technologies
- Brief history of the web.
- Overview of web development.
- Understanding the role of HTML, CSS, and JavaScript.

---
layout: default
transition: fade-out
---

# Brief History of the Web
- **1960s-1970s:** Development of early computer networks like ARPANET.
- **1989:** Tim Berners-Lee proposes the World Wide Web while working at CERN.
- **1991:** First website goes live.
- **1993:** Introduction of Mosaic, the first widely-used web browser.
- **Web 1.0 (1990s):** Primarily static web pages with limited user interaction. Information was presented in a one-way communication manner.
- **Web 2.0 (2000s):** Emergence of dynamic and interactive web applications. Users could participate in content creation, social networking, and collaboration.
- **Web 3.0 (present-future):** Envisioned as the semantic web, where data is interconnected and machine-readable, enabling more intelligent and context-aware applications.
- **2000s-present:** Rapid growth of the web with the creation of browsers like Netscape Navigator and Internet Explorer, leading to the emergence of dynamic web applications, social media, and mobile web.

---
layout: default
transition: fade-out
---

# Overview of Web Development
- **Frontend Development:** Concerned with what users interact with directly in their web browsers.
  - Involves HTML (structure), CSS (presentation), and JavaScript (behavior).
- **Backend Development:** Deals with server-side logic and database interactions.
  - Utilizes languages like Python, Ruby, Node.js, etc., along with databases like MySQL, PostgreSQL, MongoDB, etc.
- **Full Stack Development:** Involves both frontend and backend development.
  - Requires proficiency in multiple technologies and frameworks.

---
layout: default
transition: fade-out
---

# Understanding the Role of HTML, CSS, and JavaScript
- **HTML (Hypertext Markup Language):**
  - Defines the structure of web pages using elements like `<html>`, `<head>`, `<body>`, `<div>`, etc.
  - Elements are organized in a hierarchical manner, forming the DOM (Document Object Model).
- **CSS (Cascading Style Sheets):**
  - Controls the presentation and layout of HTML elements.
  - Used for styling elements with properties like color, font-size, margin, etc.
- **JavaScript:**
  - Adds interactivity and dynamic behavior to web pages.
  - Allows manipulation of DOM elements, handling events, making AJAX requests, etc.
  - Widely used in frontend and backend development with Node.js.

---
layout: section
transition: fade-out
---

# Setting Up Your Development Environment

---
layout: default
transition: fade-out
---


## Choosing a Text Editor
- **Visual Studio Code:** A popular, feature-rich code editor developed by Microsoft.
- **Sublime Text:** Lightweight yet powerful, Sublime Text offers a smooth editing experience with extensive plugin support.
- **Atom:** Known for its hackability, Atom is an open-source text editor developed by GitHub.

---
layout: default
transition: fade-out
---


# Installing a Modern Web Browser
- **Chrome:** Google Chrome is widely used, offering fast performance and robust developer tools.
- **Firefox:** Mozilla Firefox provides a customizable browsing experience with excellent privacy features.
- **Edge:** Microsoft Edge is built on Chromium, offering compatibility with Chrome extensions and developer tools.

---
layout: default
transition: fade-out
---


# Introduction to Browser Developer Tools
- **Inspect Element:** Allows you to view and modify the HTML and CSS of a web page in real-time.
- **Console:** Provides a JavaScript console for debugging, logging, and executing code snippets.
- **Network:** Displays network requests made by the browser, helping optimize web performance.
- **Debugger:** Allows you to set breakpoints and step through JavaScript code for debugging purposes.
- **Performance:** Offers insights into page load times and resource utilization, aiding in optimization efforts.


---
layout: default
transition: fade-out
---

# Introduction to HTML

HTML (Hypertext Markup Language) is the standard markup language for creating web pages. It provides the structure and content of a web page, defining elements such as headings, paragraphs, images, links, and more. Here's a basic overview of HTML:

- **Elements:** HTML documents are made up of elements, which are enclosed in tags. Tags are composed of an opening tag, content, and a closing tag. For example, `<p>` is the opening tag for a paragraph, and `</p>` is the closing tag.
- **Attributes:** Elements can have attributes that provide additional information about them. Attributes are placed within the opening tag and are typically in name-value pairs. For example, the `src` attribute in the `<img>` tag specifies the URL of the image to be displayed.
- **Document Structure:** HTML documents follow a hierarchical structure defined by nested elements. The root element is `<html>`, which contains two main sections: `<head>` (metadata and document settings) and `<body>` (content visible to users).

---
layout: default
transition: fade-out
---

- **Semantic Markup:** HTML5 introduced semantic elements like `<header>`, `<footer>`, `<nav>`, `<article>`, `<section>`, etc., which provide meaning to the content and improve accessibility and SEO.
- **Validation:** HTML should be well-formed and adhere to the standards set by the W3C (World Wide Web Consortium). Validators can be used to ensure compliance with HTML specifications.


---
layout: default
transition: fade-out
---

Now, let's create the HTML structure for our Weather App:

<div class="overflow-y-auto h-[80%] ">

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather App</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link to external CSS file -->
</head>
<body>
    <header>
        <h1>Weather App</h1>
    </header>
    <main>
        <section id="location">
            <h2>Location</h2>
            <form id="location-form">
                <input type="text" id="search-input" placeholder="Enter city name...">
                <button type="submit">Search</button>
            </form>
        </section>
        <section id="current-weather">
            <h2>Current Weather</h2>
            <div id="weather-details">
                <!-- Weather details will be dynamically populated here -->
            </div>
        </section>
        <section id="forecast">
            <h2>5-Day Forecast</h2>
            <div id="forecast-details">
                <!-- Forecast details will be dynamically populated here -->
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Weather App. All rights reserved.</p>
    </footer>
    <script src="app.js"></script> <!-- Link to external JavaScript file -->
</body>
</html>
```


</div>



---
layout: section
transition: fade-out
---

# Introduction to CSS

---
layout: default
transition: fade-out
---


CSS (Cascading Style Sheets) is a stylesheet language used to control the presentation and layout of HTML documents. It allows you to style elements such as text, colors, fonts, margins, padding, and more. Here's a brief overview of CSS:

- **Selectors:** CSS selectors are used to target HTML elements for styling. They can be based on element types, classes, IDs, attributes, or pseudo-classes.
- **Properties and Values:** CSS properties define the appearance of elements, while values specify the desired styles. For example, the `color` property sets the text color, and the `font-size` property determines the size of the font.

---
layout: default
transition: fade-out
---

- **Cascade and Specificity:** CSS follows a cascading hierarchy, where styles can be inherited from parent elements and overridden by more specific selectors. Specificity rules determine which styles take precedence when multiple conflicting styles are applied.
- **Box Model:** Elements in CSS are represented as rectangular boxes with content, padding, border, and margin areas. Understanding the box model is essential for layout design and positioning.
- **Responsive Design:** CSS allows you to create responsive layouts that adapt to different screen sizes and devices using techniques like media queries and flexible units (e.g., percentages, viewport units).

---
layout: default
transition: fade-out
---

# Now Lets Style our Weather App

<div class="overflow-y-auto h-[80%] ">



```css
/* styles.css */

/* Reset default browser styles */
body, h1, h2, p, form, input, button {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f5f5f5;
    color: #333;
}

header {
    background-color: #007bff;
    color: #fff;
    padding: 1rem;
    text-align: center;
}

main {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
}

section {
    margin-bottom: 2rem;
}

h2 {
    margin-bottom: 1rem;
}

form {
    margin-bottom: 1rem;
}

input[type="text"] {
    padding: 0.5rem;
    width: 70%;
}

button {
    padding: 0.5rem 1rem;
    background-color: #007bff;
    color: #fff;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

footer {
    text-align: center;
    padding: 1rem;
    background-color: #007bff;
    color: #fff;
    position: fixed;
    bottom: 0;
    width: 100%;
}
```
</div>


---
layout: section
transition: fade-out
---


# Introduction to JavaScript


---
layout: default
transition: fade-out
---

JavaScript is a high-level programming language primarily used for adding interactivity and dynamic behavior to web pages. It allows you to manipulate the DOM (Document Object Model), handle events, make asynchronous requests, and much more. Here's a brief overview of JavaScript:

- **Syntax:** JavaScript syntax is similar to other programming languages like Java and C. It supports variables, data types, operators, control structures (e.g., if statements, loops), functions, and objects.
- **DOM Manipulation:** JavaScript can modify the structure, content, and style of HTML elements in real-time. This enables dynamic updates and interactive user interfaces.

---
layout: default
transition: fade-out
---

- **Event Handling:** JavaScript allows you to respond to user actions (e.g., clicks, keystrokes, mouse movements) by attaching event listeners to HTML elements.
- **Asynchronous Programming:** JavaScript supports asynchronous operations using callbacks, promises, and async/await syntax. This enables non-blocking behavior, making it suitable for tasks like AJAX requests and timeouts.
- **Browser Compatibility:** JavaScript is supported by all modern web browsers and can be executed both on the client-side (in the browser) and server-side (with Node.js).




---
layout: default
transition: fade-out
---

# Now Lets Dynamic our Weather App

<div class="overflow-y-auto h-[80%] ">


```js
// app.js
document.getElementById('location-form').addEventListener('submit', function(event) {
    event.preventDefault();
    const cityName = document.getElementById('search-input').value;
    getWeather(cityName);
});

function getWeather(cityName) {
    // Fake API call (replace with real API later)
    const fakeWeatherData = {
        current: {
            temperature: 20,
            description: 'Partly cloudy'
        },
        forecast: [
            { date: '2024-03-20', temperature: 22, description: 'Sunny' },
            { date: '2024-03-21', temperature: 24, description: 'Clear skies' },
            { date: '2024-03-22', temperature: 18, description: 'Rain showers' },
            { date: '2024-03-23', temperature: 16, description: 'Thunderstorms' },
            { date: '2024-03-24', temperature: 20, description: 'Partly cloudy' }
        ]
    };

    // Update UI with fake weather data
    displayCurrentWeather(fakeWeatherData.current);
    displayForecast(fakeWeatherData.forecast);
}

function displayCurrentWeather(weather) {
    const weatherDetails = document.getElementById('weather-details');
    weatherDetails.innerHTML = `
        <p>Temperature: ${weather.temperature}°C</p>
        <p>Description: ${weather.description}</p>
    `;
}

function displayForecast(forecast) {
    const forecastDetails = document.getElementById('forecast-details');
    forecastDetails.innerHTML = '';
    forecast.forEach(day => {
        const forecastItem = document.createElement('div');
        forecastItem.classList.add('forecast-item');
        forecastItem.innerHTML = `
            <p>Date: ${day.date}</p>
            <p>Temperature: ${day.temperature}°C</p>
            <p>Description: ${day.description}</p>
        `;
        forecastDetails.appendChild(forecastItem);
    });
}

```
</div>


---
layout: section
transition: fade-out
---

# Introduction to APIs

---
layout: default
transition: fade-out
---

An API (Application Programming Interface) is a set of rules and protocols that allows different software applications to communicate with each other. It defines how requests and responses should be structured, enabling developers to access and interact with external services, databases, or libraries. Here's a brief overview of APIs:

- **Types of APIs:** APIs can be classified into several types, including:
  - **Web APIs:** Exposed over the internet using standard web protocols like HTTP. Common examples include RESTful APIs and SOAP APIs.
  - **Library APIs:** Provided by software libraries or frameworks to enable functionality within an application.
  - **Operating System APIs:** Offered by operating systems to interact with hardware, file systems, and other system resources.
- **HTTP Methods:** APIs typically use HTTP methods (e.g., GET, POST, PUT, DELETE) to perform operations like fetching data, creating resources, updating information, and deleting records.

---
layout: default
transition: fade-out
---

- **Request and Response Formats:** APIs define the structure of requests and responses using formats like JSON (JavaScript Object Notation), XML (eXtensible Markup Language), or HTML.
- **Authentication and Authorization:** APIs may require authentication to access protected resources, using mechanisms like API keys, OAuth tokens, or JWT (JSON Web Tokens).
- **Rate Limiting:** To prevent abuse and ensure fair usage, APIs often enforce rate limits to restrict the number of requests a client can make within a certain time period.

---
layout: default
transition: fade-out
---

# Now, let's transition from our fake API to a real API for fetching weather data:

<div class="overflow-y-auto h-[80%] ">


```javascript
// app.js
document.getElementById('location-form').addEventListener('submit', function(event) {
    event.preventDefault();
    const cityName = document.getElementById('search-input').value;
    getWeather(cityName);
});

async function getWeather(cityName) {
    try {
        const apiKey = 'YOUR_API_KEY'; // Replace with your actual API key
        const response = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${cityName}&appid=${apiKey}&units=metric`);
        const data = await response.json();
        
        const currentWeather = {
            temperature: data.main.temp,
            description: data.weather[0].description
        };

        const forecastResponse = await fetch(`https://api.openweathermap.org/data/2.5/forecast?q=${cityName}&appid=${apiKey}&units=metric`);
        const forecastData = await forecastResponse.json();
        
        const forecast = forecastData.list.map(item => ({
            date: item.dt_txt,
            temperature: item.main.temp,
            description: item.weather[0].description
        })).filter((item, index) => index % 8 === 0); // Filter to get one forecast per day

        displayCurrentWeather(currentWeather);
        displayForecast(forecast);
    } catch (error) {
        console.error('Error fetching weather data:', error);
    }
}

function displayCurrentWeather(weather) {
    const weatherDetails = document.getElementById('weather-details');
    weatherDetails.innerHTML = `
        <p>Temperature: ${weather.temperature}°C</p>
        <p>Description: ${weather.description}</p>
    `;
}

function displayForecast(forecast) {
    const forecastDetails = document.getElementById('forecast-details');
    forecastDetails.innerHTML = '';
    forecast.forEach(day => {
        const forecastItem = document.createElement('div');
        forecastItem.classList.add('forecast-item');
        forecastItem.innerHTML = `
            <p>Date: ${day.date}</p>
            <p>Temperature: ${day.temperature}°C</p>
            <p>Description: ${day.description}</p>
        `;
        forecastDetails.appendChild(forecastItem);
    });
}
```
</div>

---
layout: default
transition: fade-out
---

# Thank You
# Q&A
