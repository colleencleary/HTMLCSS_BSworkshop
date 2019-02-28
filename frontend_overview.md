# Front End Web Development
_"Front End Web Development" refers to the languages that run in a web browser_


<hr />


## Task 1: File Setup with Github
  1. Log in to your [Github](https://github.com/) account.

  2. Create a new repository named _yourusernamehere_.github.io

      - it **must** be your username or it won't work.

  3. Open Terminal and make a new directory called dev (from your home directory). Navigate into your new directory

      `cd ~`

      `mkdir dev`

      `cd dev`

  4. Clone your github repository and enter the project folder (replace `username` with _your_ username)

      `git clone https://github.com/username/username.github.io`

      `cd username.github.io`

  5. Create a file called index.html

      `touch index.html`

  6. Add some text to your index.html file

      `echo "Hello World" > index.html`

  7. Add, commit, and push your changes

      `git add .`

      `git commit -m "Initial commit"`

      `git push origin master`


  8. Go to your website at https://_username_.github.io

      - the first commit might take a few minutes, but future changes should show up pretty quickly

<hr />


## HTML
###### Or **Hypertext Markup Language**

 - HTML is a coding language that defines the structure/layout of a webpage

 - It allows you to add content to the browser and give it meaning

 - HTML uses `<tags>` to create elements and format content

      See some examples in the [tags.html](/tags.html) file.




#### Example Index

Open up [example_index.html](/example_index.html) in your text editor _and_ your browser.


Find more tags at [W3 Schools](https://www.w3schools.com/tags/)




<hr />




## Task 2: Add some content to your website
  1. open index.html in a text editor

  2. use [example_index.html](/example_index.html) to add elements to _your_ index.html file

  3. Add, commit, and push your changes with a descriptive commit message

      `git add .`

      `git commit -m "added content to index.html"`

      `git push origin master`


  _Save time by using https://meettheipsums.com/ for text blocks_




<hr />





## CSS
###### Or **Cascading Style Sheets**

  - CSS controls the style(fonts, colors, layout, etc) of the HTML content

  - Different language from HTML (and has its own syntax rules!)

  - Style can be added in a `<style>` tag in your html file, but we'll be creating an external `styles.css` file

  - CSS is called in the `<head>` element using a new tag

      `<link rel="stylesheet" href="css/styles.css">`



  <hr />





## Task 3: Add some style to your website
  1. add the `<link>` relation tag under the `<title>` in your `<head>` element

  2. make two new directories called `css` and `images`

  3. move your profile image into the `images` directory

  4. create your CSS file in terminal and open it in your text editor

      `touch css/styles.css`

  5. change the background color of your webpage and refresh in the browser to make sure index.html and styles.css are connected

  6. Add, commit, and push your changes with a descriptive commit message


<hr />


### CSS terminology and syntax

`p {`

`color: green;`

`font-weight: bold;`

`}`

**Selectors** are the HTML element that you want to apply styles to.

**Declaration blocks** are all the style rules for the element surrounded by {}.

**Declarations** are style rules, written as:
  property: value;
    _always end with a semicolon!_

**Properties** are the type of style.

**Values** are specific to the property.

##### Find more properties at [codrops](https://tympanus.net/codrops/css_reference/) and [W3 Schools](https://www.w3schools.com/css/default.asp).

### W3 Schools examples https://www.w3schools.com/css/css_intro.asp



  <hr />



## Task 4: Pick a color palette
  1. go to https://coolors.co/ and pick a color palette

  2. add your colors as comments at the top of your styles.css file

  3. using colors from your palette, change the color of your background and the color of your `<h2>` font

  4. Add, commit, and push your changes with a descriptive commit message


<hr />


### CSS Selectors

#### **Type Selectors** apply styles to _all_ of those elements.

`h2 {`

  `color: #17303F;`

`}`

_This changes the color for **all** the h2 elements, but nothing else._


#### **Class and ID attributes** can be used to attach extra information to HTML elements.

  index.html:

      `<tag attribute="value"></tag>`
      `<p class="highlighted"></p>`
      `<div id="social"></div>`


- What you call your classes and IDs are up to you, but always be descriptive.
- The same class can be used for multiple elements, but you should only use IDs for _one_ element.


##### Class Selector

In styles.css, the class name is your selector (instead of the element) and it starts with a period.

`.highlighted {`

  `background: yellow;`

`}`

##### ID Selector

In styles.css, the id name is your selector and it starts with a # symbol.

`#social {`

  `background: black;`

  `color: white;`

`}`


##### Multiple Classes

You can assign multiple classes to an element in your HTML by separating them with a space.

`<p class="highlighted education"></p>`

You can apply different styles to each class separately.

`.highlighted {`

  `background: yellow;`

`}`

`.education {`

  `font-size: 16px;`

`}`

You can also combine them to assign styles to elements that have both classes.

`.highlighted.education {`

  `color: blue;`

`}`

_multiple IDs can NOT be used_


##### Descendent Selectors

Elements are _nested_ and we can use this to add style to specific elements!

![nested elements](http://www.openbookproject.net/tutorials/getdown/css/images/lesson4/HTMLDOMTree.png)

Instead of changing the color of all the h2 elements, we can target just the ones in the header:

`header h2 {`

  `color: blue;`

`}`

`.education h3 {`

  `color: purple;`

`}`

##### Grouping multiple Selectors

We can apply the same styles to multiple elements at once!

`h1, .education h2 {`

  `color: blue;`

`}`

is the same as:

`h1 {`

  `color: blue;`

`}`


`.education h2 {`

  `color: blue;`

`}`

##### Pseudo-class Selectors

- Pseudo-class selectors are keywords used to specify the state of the element.
- Keywords are combined with selectors using a colon (no spaces!).

`a:hover {`

  `background: yellow;`

`}`




  <hr />



## Task 5: Add style to specific elements
  1. In index.html, add a "work" class to your work section and an "education" class to your education section

  2. In styles.css, add different background and font colors to your "work" and "education" classes

  3. Give a different background and font color to your header and footer using one declaration block

  4. Give a different font color to the h1 and h2 elements in your header and footer using one declaration block

  5. Give your links a different color when the mouse hovers over them by using a pseudo-class selector

  6. Add, commit, and push your changes with a descriptive commit message



<hr />


### Web Fonts

We can link web fonts the same way we linked our css in index.html:

`<link href="https://fonts.googleapis.com/css?family=Caveat|Open+Sans" rel="stylesheet">`

- Fonts need to be called _before_ linking your css file.



Fonts are applied in styles.css with the "font-family" property:

`body {`

  `font-family: 'Open Sans', sans-serif;`

`}`


`h1, h2 {`

`  font-family: 'Caveat', cursive;`

`}`

And we can change font styles with "font-size" and "font-weight":

`h2 {`

`  font-size: 40px;`

`  font-weight: bold;`

`}`

`h1 {`

`  font-size: 80px;`

`}`






<hr />


## Task 6: Change the font of your page
  1. Pick one or two fonts from https://fonts.google.com/

  2. Link them in your index.html file

  3. Apply them in your styles.css file

  4. Add, commit, and push your changes with a descriptive commit message



<hr />




### Layout

#### Block Elements VS Inline Elements

- block elements have the height of their content, but their width is 100% of their container (which is why each element starts on a new line)
- inline elements have the height _and_ width of their content (they align left)

We can set the height and width of an element in styles.css:

`h1 {`

  `width: 300px;`

`}`


You can use the css property "float" to allow elements to float to the right or left.

`img  {`

`float: right;`

`}`




<hr />


## Task 7: Fix the layout of your website
  1. In index.html, add a new class called "narrow-column" to your header image

  2. Wrap the h1, h2, and p elements in your header in a `<div>` element that is assigned the class "wide-column"

  3. In styles.css, give your "narrow-column" class a width of "35%" and your "wide-column" class a width of "62%"

  4. Use `float: left` to make them inline elements and give them the same height.

  5. Add, commit, and push your changes with a descriptive commit message



<hr />

#### Spacing

![spacing](http://mattryall.net/image/css-box-model.gif)

We can set the height and width of an element in styles.css:

`h1 {`

  `width: 300px;`

`}`


You can use the css property "float" to allow elements to float to the right or left. Also add padding and remove margins!

`img  {`

`float: right;`

`padding: 10px;`

`margin: 0;`

`}`




<hr />


## Task 7: Fix the layout of your website
  1. In index.html, add a new class called "narrow-column" to your header image

  2. Wrap the h1, h2, and p elements in your header in a `<div>` element that is assigned the class "wide-column"

  3. In styles.css, give your "narrow-column" class a width of "35%" and your "wide-column" class a width of "62%"

  4. Use `float: left` to make them inline elements and give them the same height.

  5. Add, commit, and push your changes with a descriptive commit message



<hr />
