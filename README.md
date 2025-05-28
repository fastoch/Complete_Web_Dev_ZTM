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

A **Content Delivery Network** (CDN) is a system of geographically distributed servers designed to deliver web content efficiently and quickly to users based on their location. By caching data on servers closer to the end user, CDNs reduce latency, improve loading speeds, and enhance the overall user experience (UX).  

## Flexbox

Flexbox is a layout model that allows us to create flexible and responsive layouts.  

In this chapter, we will be building an image gallery that is fully responsive.  
This means that the layout will adapt to different screen sizes and resolutions.  

Useful resources:
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- https://darekkay.com/flexbox-cheatsheet/
- https://flexboxfroggy.com/

For this lesson, see the `flexbox` folder.  

We start by reducing the size of the images:
```css
img {
  width: 50%;
  height: auto;
}
```

We defined a div with a `container` class that will be the parent of all the images.  
Then, in our CSS file, we use the `display: flex;` rule to make the div a flex container.  

After adding this rule, the images are now displayed in a row, instead of being stacked vertically.  
But we don't want to scroll horizontally to see them all, so we need to add the `flex-wrap: wrap;` rule.  

### Flexbox properties - global

The `justify-content`property aligns items **horizontally** and accepts the following values:
- `flex-start`: Items align to the left side of the container.
- `flex-end`: Items align to the right side of the container.
- `center`: Items align at the center of the container.
- `space-between`: Items display with equal spacing between them.
- `space-around`: Items display with equal spacing around them.

The `align-items` property aligns items **vertically** and accepts the following values:
- `flex-start`: Items align to the top of the container.
- `flex-end`: Items align to the bottom of the container.
- `center`: Items align at the vertical center of the container.
- `baseline`: Items display at the baseline of the container.
- `stretch`: Items are stretched to fit the container.

The `flex-direction` property defines the direction of the flex items and accepts the following values:
- `row`: Items are displayed horizontally from left to right.
- `row-reverse`: Items are displayed horizontally from right to left.
- `column`: Items are displayed vertically from top to bottom.
- `column-reverse`: Items are displayed vertically from bottom to top.

**IMPORTANT**:  
Note that when `flex-direction` is set to `column`, `justify-content` changes to the vertical and `align-items` to the horizontal.  

### Flexbox properties - individual items

Sometimes **reversing** the row or column order of a container **is not enough**.  
In these cases, we can apply the `order` property to individual items.  
By default, items have a value of 0, but we can set the order property to a positive or negative integer value.  

Another property you can apply to individual items is `align-self`, it accepts the same values as `align-items`.  

### Flexbox properties - flex-wrap

If items are squeezed onto a single row, we can spread them out using the `flex-wrap` property, which accepts the following values:
- `nowrap`: Every item is fit to a single line.
- `wrap`: Items wrap around to additional lines.
- `wrap-reverse`: Items wrap around to additional lines in reverse.

### Flexbox properties - flex-flow

The two properties `flex-direction` and `flex-wrap` are used so often together that the shorthand property `flex-flow` was created to combine them. This shorthand property accepts the value of the two properties separated by a space.  

For example, you can use `flex-flow: row wrap;` to set rows and wrap them.  

### Flexbox properties - align-content

You can use `align-content` to set how multiple lines are spaced apart from each other.  
This property takes the following values:
- `flex-start`: Lines are packed at the top of the container.
- `flex-end`: Lines are packed at the bottom of the container.
- `center`: Lines are packed at the vertical center of the container.
- `space-between`: Lines display with equal spacing between them.
- `space-around`: Lines display with equal spacing around them.
- `stretch`: Lines are stretched to fit the container.

This can be confusing, but `align-content` determines the spacing between **lines**,  
while `align-items` determines how the items as a whole are aligned within the container.  
When there is only one line, `align-content` has no effect.  

## Transition & Transform (basic example)

Going back to our image gallery, we can add a hover effect to the images:
```css
img {
  width: 50%;
  height: auto;
  transition: all 1s;
}

img:hover {
  transform: scale(1.1);
}
```
The above code will make the images grow by 10% when hovered over.  
The `transition` property is used to specify the duration of the transformation.  

The `all` keyword specifies that the transition should apply to all animatable CSS properties of the element (color, background-color, transform, opacity, etc.).  
If you want to target specific properties, you can replace `all` with the property names.  

---

## CSS newest features

To know if a CSS property is supported by a browser, you can check this website:  
https://www.w3schools.com/cssref/css3_browsersupport.php

### Browser prefixes

Sometimes, we need to use a **browser prefix** before the property name to make it work:  
![browser_prefix](/assets/prefix.png)  

That happens when a new CSS property is introduced, and the browser vendors haven't implemented it yet.  
For such experimental properties, the browser vendors add a prefix to the property name to indicate that it's still in development.  

Example:
```css
-moz-box-shadow: 4px 4px 5px #888; /* Firefox */
-ms-box-shadow: 4px 4px 5px #888; /* Edge */
-webkit-box-shadow: 4px 4px 5px #888; /* Chrome, Safari, Opera */
```

A useful resource for checking a browser's compatibility with a specific feature:    
https://caniuse.com/

---

## Mastering Transitions and Transforms

resource: https://thoughtbot.com/blog/transitions-and-transforms  

When used together, the `transition` and `transform` properties allow us to create simple animations and add valuable interaction and visual feedback for our users.  

Transforms move or change the appearance of an element, while Transitions make the element smoothly and gradually change from one state to another.  

### CSS Transitions

Without a transition, an element being transformed would change abruptly from one state to another.   
By applying a transition you can control the change, making it smooth and gradual.  

There are 2 properties that are **required** in order for the transition to take effect:
- `transition-property`
- `transition-duration`

Each transition property can be defined individually, but for cleaner and faster code, it’s **recommended** that you use the `transition` shorthand.  

Here’s the full shorthand sequence. Once again, only the first two properties are required:
```css
selector {
  transition: [property] [duration] [timing-function] [delay];
}
```  

The `transition-property` specifies the CSS property where the transition will be applied.   
You may apply a transition to an individual property (e.g., `background-color` or `transform`) or to all properties in the rule-set (i.e., `all`).  

The `transition-duration` property specifies the time span of the transition.  
You can specify a value in seconds or milliseconds.  

The `transition-timing-function` property allows you to define the speed of the transition over the duration.  
The default timing is `ease`, which starts out slow, quickly speeds up, and then slows down at the end.  
The other timing options are: `linear`, `ease-in`, `ease-out`, and `ease-in-out`.  
For more advanced timing options, you can define a custom timing function with a `cubic-bezier`.  

The `transition-delay` property allows you to specify when the transform will start.  
By default, it starts as soon as it is triggered (e.g., on mouse hover).  
However, if you want it to start after a certain time, you can use the `transition-delay` property.

### CSS Transforms

Now that we reviewed how to make smooth and gradual transitions, let’s see how to make an element change from one state to another. 
With the CSS `transform` property you can rotate, move, skew, and scale elements.  

Transforms are triggered when an element changes states, such as on mouse-hover or mouse-click.  

---

The **scale** value allows you to increase or decrease the size of an element.  
For example, the value 2 would transform the size to be 2 times its original size.   
The value 0.5 would transform the size to be half its original size.  

You can scale an element by setting parameters for the width (X-axis) or height (Y-axis).  
For example, `transform: scaleX(2);`.  

Or, use the scale() shorthand to scale both axes at the same time: `transform: scale(2);`.  
Or define them independently of each other: `transform: scale(2, 4);`  

**Don’t forget to add a transition!**  
Without applying transition, the element would abruptly change sizes.  
Add the transition to the parent selector (not the hover selector).  

---

With the **rotate** value, the element rotates clockwise or counterclockwise by a specified number of degrees.  
A positive value, such as 90deg, rotates the element clockwise, while a negative value rotates it counterclockwise.  
You can rotate more than a full rotation with numbers over than 360, such as 1080deg, for three full rotations.  

---

The **translate** value moves an element left/right and up/down.  
The movement is based on the parameters given for the X (horizontal) Y (vertical) axes.  

A positive X value moves the element to the right, while a negative X moves the element to the left.  
A positive Y value moves the element downwards and a negative Y value, upwards.  

---

With the **skew** value, the element skews (or tilts) one direction or the other based on the values given for the X and Y axes.  

A positive X value tilts the element left, while a negative X value tilts it right.  
A positive Y value tilts the element down, and a negative Y value tilts is up.  
Or use a shorthand to include both X and Y properties.  

**Note**:  
Skewing an element will also skew all of the children inside of the element as well (which may make text content unreadable).  
If you need to maintain the original angle of a child element, you can use the opposite value of skew to bring it back.  

---
The `transform-origin` property is separate from the `transform` property but works in tandem with it.  
It allows you to specify the location origin of the transform. By default, the origin is in the center of the element.  

For example, if you are using the `transform: rotate();` property but want it to rotate not from the center, but from the top left corner, you’d use the value `left top`. For the bottom right corner, you would use `right bottom`, etc.  

Make sure to add the `transform-origin` property to the parent element, not with the transform property in the hover selector.  
```css
div {
  transform-origin: left top;
  transition: transform 1s;
}

div:hover {
  transform: rotate(720deg);
}
```

---

We can **combine** multiple transforms by using the `transform` shorthand:
```css
div {
  transform: rotate(90deg) scale(2) translateY(-50%) translateX(50%);
}
```

---

## Robot Animation

TO DO

---

# Bootstrap & CDNs 

Bootstrap is a popular CSS framework that provides a set of pre-designed CSS styles and components.  
These styles and components are hosted on a **CDN**, which prevents devs from having to download and host the files themselves.  

CDN stands for **Content Delivery Network**.  
A CDN is a network of servers that delivers content to users based on their geographic location.  

All we need to do to use Bootstrap is to add the Bootstrap CDN link to our HTML file, inside the `<head>` tag.  
The link needs to be added before any other stylesheets.  
For example:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.3.0/dist/css/bootstrap.min.css">
```  

Once we have added the CDN link, we can use Bootstrap classes in our HTML code.  
For example, if we want to add a nav bar to our page, we can simply copy the Bootstrap code for it and paste it into our HTML file.  
We copy the code inside our `<body>` tag, of course.

Bootstrap is **fully responsive**, meaning that it will automatically adjust its layout and styling to fit the screen size of the device it is being viewed on.  

If we want to customize our Bootstrap styles, we can do so by adding our own CSS stylesheet after the Bootstrap CDN link.  
And according to Cascading Style Sheets (CSS), the last stylesheet added will override the previous ones.  
Then we use the same class name as the Bootstrap class name, and we define our custom styling.  

---

# Changing versions

As a developer, you may want to update the version of the packages you are using.  
It's important to note that updating packages can sometimes cause issues, so it's important to test your code thoroughly before deploying it to production.  
Maintaining the latest version of your packages is important for security and performance reasons.  

If you want, for example, to update the Bootstrap version, you can do so by changing the version number in the CDN link.  
For example, if you want to use Bootstrap 5.3.0, you can change the link to:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
```

You would also need to update the Bootstrap JavaScript files if you want to use Bootstrap's JavaScript features: 
```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

---

# Fast and the Furious Bootstrap

We're going to build a Bootstrap website in record time.  

- First, go to https://getbootstrap.com/docs/5.3/getting-started/download/
- copy the following lines of code:
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.6/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-4Q6Gf2aSP4eDXB8Miphtr37CMZZQ5oXLH2yaXMJ2w8e2ZtHTl7GptT4jmndRuHDT" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.6/dist/js/bootstrap.bundle.min.js" integrity="sha384-j1CDi7MgGQ12Z7Qab0qlWQ/Qqz24Gc6BM0thvEMVjHnfYGF0rmFCozFSxQBxwHKO" crossorigin="anonymous" defer></script>
```
- paste the code into the `head` section of your HTML file
- add the `defer` attribute to the script tag to make sure the page loads before the script runs
- in the `body` section, 
  - add the navbar from this page: https://getbootstrap.com/docs/5.3/components/navbar/
  - add the carousel from this page: https://getbootstrap.com/docs/5.3/components/carousel/
  - add a modal and a button that triggers it from https://getbootstrap.com/docs/5.3/components/modal/

---

# Bootstrap Grid Layout

https://getbootstrap.com/docs/5.3/layout/grid/  

The primary reason why Bootstrap was so popular is that we didn't have **Flexbox** back in the day.  
Bootstrap allows us to create very responsive websites using a grid system.  

see the `Bootstrap_grid` folder for an example of a Bootstrap grid layout  

In Bootstrap, you always want to wrap everything in a container.  
```html
<div class="container">
  ...
</div>
```

The container is a special class that Bootstrap provides, among other numerous classes.  
https://getbootstrap.com/docs/5.3/layout/containers/  


The Bootstrap grid system is based on a **12-column** grid.  

---

# Building a startup landing page

We will build a startup landing page from scratch using Bootstrap.  
See the `Bootstrap_grid` folder for the final result.  

@Startup Landing Page 3

## What is the `<meta>` tag?

The `<meta>` tag is used to provide **metadata** about the HTML document. Metadata is data (information) about data.  

`<meta>` tags always go inside the `<head>` tag, and are typically used to specify:
- **character set**, 
- page description, 
- **keywords**, 
- author of the document, 
- and **viewport** settings.

Metadata will not be displayed on the page, but is machine-parsable.  
Metadata is used by browsers (how to display content or reload page), search engines (keywords), and other web services.  

### Setting the Viewport

The viewport is the user's visible area of a web page.  
It varies with the device - it will be smaller on a mobile phone than on a computer screen.  

You should **ALWAYS** include the following <meta> element in all your web pages:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

The `width=device-width` part sets the width of the page to follow the screen-width of the device.  
The `initial-scale=1.0` part sets the initial zoom level when the page is first loaded by the browser.  

More here: https://www.w3schools.com/tags/tag_meta.asp  

## Perfect Full Page Background Image

https://css-tricks.com/perfect-full-page-background-image/  

Add the following to the html selector inside your .css file:
```css
background: url(../assets/startup_landing_page.jpg) no-repeat center center fixed;
background-size: cover;
```

## Startup Landing Page 4

We apply a Bootstrap class to our h1 element so the text is uppercase:  
`<h1 class="text-uppercase"><strong>The Biggest Startup Event of the Year</strong></h1>`  

We also use a Bootstrap class to style the "Find out more" button:
`<button type="button" class="btn btn-danger">Find out more</button>`

Then, we can change the color of the button by adding our own custom class:
`<button type="button" class="btn btn-danger btn-custom">Find out more</button>`

And we define this custom class in our .css file:
```css
.btn-custom {
  padding: 1rem;
  font-weight: 500;
  border-radius: 16px;
  background-color: #F05F44;
}
``` 

We can also add a hover effect to the button:
```css
.btn-custom:hover {
  background-color: #ee4b08;
  border-color: #ee4b08;
  border-width: 2px;
}
```

We can add a horizontal line `<hr>` between the h1 and the button, and we can add some style to it:
```css
hr {
    margin: 20px auto;
    color: #F05F44;
    border: 3px solid #F05F44;
    max-width: 82px;
    opacity: 1;  
}
```

## Startup Landing Page 5

Let's see how Bootstrap does **layout**.  

### Make a Bootstrap Container

First of all, inside our body tag, let's create a `<div>` with a class of `container`.  
Inside that div, we create another `<div>` with a class of `row`.  

Inside the `row` div, we'll put all the code already written in the body tag:
```html
<body>
  <div class="container">
    <div class="row">
      <h1 class="text-uppercase"><strong>The Biggest Startup Event of the Year</strong></h1>
      <hr>
      <button type="button" class="btn btn-danger btn-custom">Find Out More</button>
    </div>
  </div>
</body>
```

### Divide & Center (horizontally)

Now, let's divide this row into different sections:  

- the first section will be the `<header>`, so we'll put the h1 element into a header that has a Bootstrap class of 'text-center':
```html
<header class="text-center">
  <h1 class="text-uppercase"><strong>The Biggest Startup Event of the Year</strong></h1>
</header>
```

- the second section will include the `<button>` and the horizontal line, and will also have a Bootstrap class of 'text-center':
```html
<section class="text-center">
  <hr>
  <button type="button" class="btn btn-danger btn-custom">Find Out More</button>
</section>
```

### Positioning the Elements Vertically

Now that our 3 elements are horizontally centered and included in a Bootstrap container, we can position them vertically.  
The `d-flex` class is a Bootstrap class that allows us to use Flexbox. We need to apply this class to the `container` div.  
Then, to position the elements at the bottom of the page, we need to use the `align-items-end` class.  

```html
<div class="container d-flex align-items-end">
```

At first, the above won't work, and that is because we the container does not fill the entire viewport height.  
We'll use another Bootstrap class, `vh-100`, to set the height of the container to 100% of the viewport height.  
```html
<div class="container d-flex align-items-end vh-100">
```

## Mailchimp

We can use a service called **Mailchimp** to collect email addresses from our users.  
When they'll click the "Find Out More" button, they'll be redirected to a form where they can enter their email address.  

First of all, we need to create a new account on Mailchimp. You can choose the free plan.  


---

# CSS Grid + CSS Layout



