#Front End Web Development
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

  `<h1>Colleen Cleary</h1>`

Some Common Tags:
  - header (goes up to h6!)

  `<h1></h1>`
  - normal paragraph

  `<p></p>`
  - link

  `<a></a>`
  - image

  `<img />`
  - line break

  `<br />`

Find more tags at [W3 Schools](https://www.w3schools.com/tags/)




<hr />




## Task 2: Add some content to your website
  1. open index.html in a text editor
  2. use [example_index.html](/example_index.html) to add elements to _your_ index.html file

  _Save time by using https://meettheipsums.com/ for text blocks_




<hr />





## CSS
###### Or **Cascading Style Sheets**

  - CSS controls the style(fonts, colors, layout, etc) of the HTML content
  - Different language from HTML (and has its own syntax rules!)
  - Style can be added in a `<style>` tag in your html file, but we'll be creating an external `styles.css` file
  - CSS is called in the `<head>` element using a new tag
  `<link rel="stylesheet" href="styles.css">`



  <hr />





## Task 3: Add some style to your website
  1. add the new `<link>` relation tag to your `<head>` element
  2. create your CSS file in terminal and open it in your text editor

  `touch styles.css`
  3. change the background color of your webpage to make sure they are connected


<hr />


### CSS terminology and syntax

`p {
color: green;
font-weight: bold;
}`

**Selectors** are the HTML element that you want to apply styles to.

**Declaration blocks** are all the style rules for the element surrounded by {}.

**Declarations** are style rules, written as:
  property: value;
_always end with a semicolon!_

**Properties** are the type of style.

**Values** are specific to the property.

##### Find more properties at [codrops](https://tympanus.net/codrops/css_reference/)
