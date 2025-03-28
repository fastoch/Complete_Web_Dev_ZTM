# Browsing the Web

When we enter "google.com" in our web browser, we send a **request** to our **ISP** (Internet Service Provider).  
That request is then relayed to a Domain Name Service (**DNS**), which knows the **IP address** corresponding to "google.com".  

Once we have the IP address for the "google.com" **URL** (Uniform Resource Locator), we can communicate with Google servers.  
Our browser sends an HTTP request to Google servers and, in response, these servers send (serve) many files to our browser.  

These files are necessary to display the web page, and to allow us to interact with the website/web application.  
These files contain HTML code, CSS code, and JavaScript code, the 3 main components that make up the Web.  

All of that happens crazy fast! And that is thanks to the Internet, the underlying infrastructure that makes Web browsing possible.  
40 maps that explain the Internet: https://www.vox.com/a/internet-maps

---

# What does a developer do?

A **frontend** developer works with **HTML**, **CSS**, and **JavaScript** (JS). We sometimes refer to this part of web development as the "**client-side**".  
It's responsible for the visible part of websites and web applications, for what the user can see, and is called the "UI" (**user interface**).  

Modern frontend developers also use tools like **TypeScript** and **React**, but these are just built from JavaScript, or on top of it.  
React is a JS library, and TypeScript is a superset of JavaScript that adds strong typing to JS.  

A **backend** developer works on the "**server-side**", it makes sure that when a web browser speaks to the servers, they serve up the 
requested files. This job requires the use of technologies such as **Node**.js, **Express**.js, and **databases**.  

A **full-stack** developer knows both sides of Web Development, it works with frontend and backend technologies, and knows how to connect them.  

---

# History of the Web

Timothy Berners-Lee invented the World Wide Web - WWW or W3 - in 1989, making him the first Web Developer.  
The Web relies essentially upon a common language that all computers can speak: the **TCP/IP** protocol.  

TCP/IP stands for Transmission Control Protocol/Internet Protocol.  

Timothy Berners-Lee created the first Web browser, the first Web site, and the first Web server.  
First website ever: https://info.cern.ch/hypertext/WWW/TheProject.html

---

# HTML, CSS, JavaScript (JS)

In this course, we're going to learn HTML5, CSS3, and JavaScript + React. That is for the **frontend** part.

## HyperText Markup Language

HTML 1.0 was released in 1993.  

HTML is the fundamental building block of the World Wide Web, used primarily for the following purposes: 
- Displaying content in Web browsers
- Structuring and formatting this content
- Creating **hyperlinks**
- Creating **forms**: HTML allows developers to create interactive forms for **user input** and **data collection**
- Embedding media: **HTML5** introduced enhanced capabilities for embedding audio, video, and other multimedia elements
- Improving **accessibility**: Proper use of HTML elements helps make web content accessible to users with disabilities, and improves search engine optimization (SEO)

HTML works in conjunction with CSS for styling and JavaScript for functionality, forming the core trio of web technologies.  
JavaScript was created in 1995, while CSS first version was released in 1996.  

## Cascading Style Sheets

CSS is used to control the visual presentation and layout of web pages.  
CSS essentially solves the problem of having to include styling information within HTML tags, which became cumbersome and inefficient as web design grew more complex.   
By using CSS, web developers can create more visually appealing and user-friendly websites while maintaining cleaner, more organized code.  

## JavaScript

JavaScript is a versatile programming language primarily used for creating **dynamic** and **interactive** web content.  
JavaScript's widespread adoption and versatility make it an essential tool for modern web development, enabling developers to create rich, interactive experiences across various platforms and devices.  

---

# Different web browsers & screen sizes

It is still a pain point for developers when it comes to making sure our web application will look and behave exactly the same on any web browsers.  
And not only that, we also have mobile phones and tablets now, which makes us having to think about **responsiveness** and compatibility with all screen sizes.  

---

# HTML5 

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My first webpage</title>
  </head>
  <body>
    <h1>Hellooooo!</h1>
    <h2>Hellooooo!</h2>
    <h6>Hellooooo!</h6>

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto tempora molestias ipsum dicta. 
      Ratione dolores quibusdam facere cum rerum, voluptatibus veniam autem nemo repellat libero sed optio.
      Natus, suscipit magni?
    </p>

    <ol>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ol>

    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </body>
</html>
```

This basic HTML page only shows a few of the most commonly used elements:  
- different sizes of headers
- paragraph
- Ordered list
- unordered list

Note that lists and list items can be **nested**.  

## Self-closing HTML Tags

Up until now, we've only used HTML elements that have an opening tag and a closing tag, such as `<h1>Big header</h1>`.  

Self-closing tags include:
- line break: `<br>`
- horizontal line: `<hr>`
- image: `<img>`

Generally, an image element goes with the following **attributes**:
```html
<img src="path-to-image" alt="txt-describing-img" width="42" height="42">
```
And each attribute has a value associated to it. The width and height values are expressed in pixels.  

## Anchor tag

The power of HTML resides in its ability to link to other documents, via something called "**hyperlinks**".  
Hyperlinks are **clickable** elements that can:
- take the user to another webpage within the same website, or to a completely different website
- take the user to another part of the same page
- trigger a file download

Hyperlinks are also crucial for search engine optimization (SEO), more on that later on.  

Example anchor tag:
```html
<a href="newpage.html">new page</a>
```
The `href` attribute stands for 'hypertext reference'.  
The href value is the destination, but we need something between the opening and closing tags, something we can click on.  

We can nest any element inside an anchor tag:
```html
<a href="index.html">
  <h2>back to previous page</h2>
</a>
```

---

# Advanced HTML5

Last time, we created 2 files: index.html and newpage.html to demonstrate the power of anchor tags, also called hyperlinks.  
Now, let's see another very important feature: HTML Forms. Forms are useful for collecting data, or authenticating to a website.

## HTML Forms


