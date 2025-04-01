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

# HTML, CSS, and JavaScript (JS)

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

The following file is in the HTML folder.    

Let's create our first HTML page by creating a file called `index.html` in VS Code:
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

### Image tag

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

Let's create an anchor tag that links to a new page:
```html
<a href="newpage.html">new page</a>
```
The `href` attribute stands for 'hypertext reference'.  
The href value is the destination, but we need something between the opening and closing tags, something we can click on.  

Now we need to create a `newpage.html` file with some basic contents.  
In VS Code, we can just type `!` and hit enter to generate a basic HTML template.  

We can nest any HTML element inside an anchor tag.   
For example, we can create an h2 element that allows us to go back to the previous page:
```html
<a href="index.html">
  <h2>back to previous page</h2>
</a>
```

---

# Advanced HTML5

All files for this section are in the HTML folder.  

Last time, we created 2 files: `index.html` and `newpage.html` to demonstrate the power of **anchor tags**, or **hyperlinks**.  
Now, let's see another very important feature: HTML **Forms**. Forms are useful for collecting data, or authenticating to a website.

## HTML Forms

Let's create a new file in VS Code called `register.html`. Use the Emmet abbreviation `!` to generate a basic HTML template.  
Then, add the following link to our index.html file: `<a href="register.html">Register</a>`  
Note that we can insert a line break `<br>` between our new page anchor tag and this Register link.  

See `register.html` for the form example.  

To make an input field required, we need to add the `required` attribute.  
To make all **radio buttons** part of the same group, we need to add the `name` attribute to each of them.  

## Submitting a form

Check the `register.html` file for more details.  

### The 'name' attribute for the input fields

In order to submit a form, we first need to add the `name` attribute to all the fields that require user input.  

### The 'method' attribute for the form tag

Then, we need to add the `method` attribute to the form tag.  

The `method` attribute defines the **HTTP method** used to send form data, it can be set to `GET` or `POST`.  
- **GET**:
  - Appends form data as query parameters in the URL (see example below) 
  - Suitable for non-sensitive data, like search queries.
  - Limited by URL length restrictions.

Example query string generated when using the GET method:   
```
?firstname=fast
&lastname=furious
&email=fake%40gmail.com
&password=12345678
&birthday=2025-03-12
&gender=male
&dog=on
&cars=Mercedes
```

- **POST**:
  - Sends form data in the request body, making it more secure.
  - Suitable for sensitive data or when the form data should not be visible in the URL.
  - Supports larger data payloads.

## HTML comments

HTML comments are used to add notes or explanations within the HTML code. They are not displayed on the webpage.  
To add a comment, we use the `<!-- my comment -->` syntax.  

In VS Code, the keyboard shortcut to comment/uncomment is `Ctrl + :` (AZERTY french keyboard layout).  
With a QWERTY keyboard layout, the shortcut is `Ctrl + /`.  

## The <div> and <span> elements

These tags are used to group elements together in an invisible container, to divide the page into sections.  
But it's recommended to use semantic HTML elements instead.  

More on **semantic** HTML elements: https://www.w3schools.com/html/html5_semantic_elements.asp  
Using semantic HTML elements is a good practice because it makes the code more readable and understandable.  
It also helps search engines understand the content of the page better, so it's good for **SEO**.  

Dividing your html page into sections is very useful for styling purposes.  
More on that when we get to learning **CSS**.  

The difference between `<div>` and `<span>` is that `<div>` is a **block-level** element, while `<span>` is an **inline** element.  

---

# CSS

All files for this section are in the CSS folder.  

## External stylesheet

Let's create our first CSS file called `style.css`.  

The basic syntax of a CSS rule is:
```css
selector {
  property: value;
}
```

Let's say we want the "Home" heading inside the index.html to be in red:
```css
h2 {
  color: red;
}
```

But this won't apply until we add a link to our CSS file in the index.html file:
```html
<link rel="stylesheet" href="style.css">
```

And if we want to apply the same styles to other .html files, we need to add the same link to them.  
We can also have a different CSS file for each .html file, but that's not very efficient.  
Instead, we should use classes and IDs, more on that topic later on.

## Cascading Style Sheets - a word about specificity

"**Cascading**" means that it follows a specific order when applying styles to HTML elements.  

>[!impoortant]
>When two rules have the same specificity, the one defined later in the CSS file takes precedence.  

CSS uses a **scoring system** to determine which rule is more specific and should be applied:  
- https://specificity.keegan.st/
- https://www.w3schools.com/css/css_specificity.asp

The order of precedence is:
1. Inline styles (cf. next section)
2. IDs 
3. Classes and pseudo-classes (e.g. :hover, :active, :focus, etc.)
4. Element (body, h1, p, nav, etc.) and pseudo-elements (e.g. ::before, ::after, etc.)
5. Universal selectors (*) and inherited styles (from parent elements)

## Inline styles

Using an external stylesheet is the best and most common practice.  
However, there might be some cases where we need to use inline styles.  

Inline styles are applied directly to the HTML elements using the `style` attribute.  
This was the original way of applying styles to HTML elements, until CSS was invented.  

Here's an example:
```html
<header style="color: blue; background-color: yellow;">Hello World</h1>
```

## The style tag

We saw how to use an external stylesheet, then we learnt how to apply inline styles.  
There's a third way to apply styles to HTML elements: by adding a `<style>` tag inside the `<head>` tag.  

**Example**:
```html
<!DOCTYPE html>
<html>
<head>
  <!--- ... -->
  <style>
    h1 {
      color: red;
      background-color: yellow;
    }
  </style>
</head>
<body>
  <!-- ... -->
</body>
</html>
```

### SEPARATION OF CONCERNS

Using inline styles or the `<style>` tag is not recommended, because it can make the HTML code harder to read and maintain.  
The **best practice** is to use an external stylesheet, or multiple external stylesheets.  

As a general rule, try and keep your HTML code separated from your CSS code. The same applies to JavaScript.  
This principle is called **separation of concerns**. It helps keep your code organized and easier to maintain.

## CSS Properties

Useful resources: 
- https://css-tricks.com/almanac/
- https://www.w3schools.com/cssref/
- https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

See the `style.css` file inside the `CSS` folder for the most common properties.  

### Colors

Useful resource: https://coolors.co/  

Colors in CSS can be specified in different ways:
- RGB values (red, green, blue)
- RGBA values (red, green, blue, alpha)
  - alpha is the opacity of the color (0 = transparent, 1 = opaque)
- Hexadecimal values (#RRGGBB)
- HSL values
- Predefined color names

## CSS Selectors

In order of precedence:
- `#id`
- `.class`
- `element:pseudo-class`: :hover, :first-child, : last-child, etc. 
  - `:hover`: apply style to an element when the user hovers over it with the mouse
  - `:first-child`: apply style to the first child element of a parent element
  - `:last-child`: apply style to the last child element of a parent element
  - `:nth-child(n)`: apply style to the nth child element of a parent element
- `element`: apply style to all elements of a certain type
- `element, element`: apply style to multiple elements at once
- `element element`: apply style to nested elements (no need to be a direct child)
- `element > element`: apply style to direct child elements
- `element + element`: apply style to an element that immediately follows another element
- `element::pseudo-element`: apply style to a pseudo-element
- `*`: universal selector, apply style to all elements 

To override any of the above styling, we have 2 options (but they're **not recommended**):
- use the `!important` keyword right before the semicolon at the end of the rule
- use inline styles (directly on the HTML element)

>[!important]
>Train yourself to use the right selector for the job: https://css-diner.netlify.app/

## Text and Font

Here are some useful properties for text:
- to space out lines: `line-height`
- to change text boldness: `font-weight`
- to change text alignment: `text-align`
- to change text decoration: `text-decoration`
- to modify font size: `font-size`
- to set font family: `font-family`

### Font Family

For the font family, we can use a list of font names, separated by commas.  
Font names must be in **quotes** if they contain **spaces**.  

The browser will try to use the first font name in the list that is available on the user's computer.  
If the font is not available, the browser will use the next font in the list.  

When selecting the font for you website/web app, it's best to use a **web-safe font** (a font that is available on most computers).  

What if we have a super cool font that we want to use? How do we make sure that any user can enjoy it?  
We can use a **web font**, which is a font that is hosted on a server and can be loaded by the browser.  

Google Fonts are the most popular option when it comes to web fontss: https://fonts.google.com/

## Images in CSS

about.html
```html
<img 
  src="https://www.ipnoze.com/wordpress/wp-content/uploads/2019/01/alpagas-droles-mignons-007.jpg" 
  alt="cute alpaga"
  width="200px" height="auto"
>
```

style.css
```css
img {
  float: left;
  padding: 1rem;
}

footer {
  clear: both;
  text-align: center;
}
```

**IMPORTANT NOTE**:   
`float` is a property that is often used for images, and that allows us to position an element to the left or right of its container.  
When using this property, the element will be removed from the normal flow of the page, and other elements will wrap around it.  
To prevent that "wrapping around" behavior, we need to use `clear` on adjacent elements.  
In our example, using the `clear` property on the footer allows it to be displayed correctly.

## Box Model

![box_model](/assets/box_model.png)  

- `padding`: space between the content and the border
- `border`: the border around the content
- `margin`: space between the border and the other elements

To change the content size, we can use the `width` and `height` properties.

## CSS units

- `px`: pixels, fixed size, not responsive
- `em`: relative to the font size of the parent element, **responsive**
- `rem`: relative to the font size of the root element (html), usually 16px, **responsive**
- `%`: relative to the parent element, **responsive**
- `vw`: relative to the viewport width, **responsive**
- `vh`: relative to the viewport height, **responsive**

More info: https://elementor.com/help/whats-the-difference-between-px-em-rem-vw-and-vh/

---

# Advanced CSS

## Critical Rendering Path

The Critical Rendering Path (CRP) is the sequence of steps browsers use to convert HTML, CSS, and JavaScript into visible pixels on screen.  

Optimizing this process reduces initial page load times and improves perceived performance, directly impacting user experience and SEO rankings.  

To optimize loading times, we can use the following techniques:
- **Minify CSS and JS files**: remove unnecessary whitespace and comments 
- Remove unused CSS rules
- Use **media queries** to load conditional CSS
- Defer non-critical JavaScript with `async/defer`
- Having our asset files hosted on a **CDN**: font files, images, etc.

### Content Delivery Network (CDN)

A **Content Delivery Network** (CDN) is a system of geographically distributed servers designed to deliver web content efficiently and quickly to users based on their location.  

By caching data on servers closer to the end user, CDNs reduce latency, improve loading speeds, and enhance the overall user experience (UX).  

## Flexbox

Flexbox is a layout model that allows us to create flexible and responsive layouts.  

In this chapter, we will be building an image gallery that is fully responsive.  
This means that the layout will adapt to different screen sizes and resolutions.  

Here are the links to the images used:  
- https://static.pexels.com/photos/52500/horse-herd-fog-nature-52500.jpeg
- https://static.pexels.com/photos/66898/elephant-cub-tsavo-kenya-66898.jpeg
- https://static.pexels.com/photos/213399/pexels-photo-213399.jpeg
- https://static.pexels.com/photos/158471/ibis-bird-red-animals-158471.jpeg
- https://static.pexels.com/photos/133459/pexels-photo-133459.jpeg
- https://static.pexels.com/photos/50988/ape-berber-monkeys-mammal-affchen-50988.jpeg
