# kakao_clone

## 1. Web Developer Tools

### VS code

- Prettier
- Material Theme
- Material Icon Theme

<br/>

### Git

- repository
- commit
- branch

<br/>

### Git vs Github

- Git

  - system of keeping track of code

- Github
  - webside, provides cloud storage for code using git

<br/>

### HTML, CSS

- Markup language
  - highlight parts in the document to tell browser what is important
- CSS
  - how elements should look like

<br/>

<br/>

## 2. HTML5

### Anatomy of a HTML Tag

- `index.html`
  - Web servers are configured to look for `index.html` first as a **default**

<br/>

### First HTML Document

- ```html
  <!DOCTYPE html>
  ```

  - the `tag` tells browser that the document is `html`
  - **self-contained** or **self-closing** tag - gives information itself

- ```html
  <html>
    <head> </head>
    <body></body>
  </html>
  ```

  - `<head>`
    - invisible to the user
    - gives information to the browser

<br/>

### Add meta Information to Document

- ```html
  <meta charset="UTF-8" />
  ```

  - encoding

- ```html
  <meta name="description" content="Welcome to Kakao Clone" />
  ```

  - the grey paragraph on every searched element

- ```html
  <meta name="author" content="sejoonkim" />
  ```

<br/>

### Semantic vs. non-Semantic tags

- semantic = contains **meaning**
  - `<h1>`
  - `<article>`
  - `<header>`
- non-semantic
  - `<div>`
    - block-level element
    - like a container, box
    - put more `<tags>` inside
  - `<span>`
    - inline element
    - container for text other than `<title>`, `<p>`

<br/>

### id & class

- `id`

  - **ONE** `id` per element
  - unique identifier

- `class`
  - can be more than 1 **in a tag**
  - can be shared in **multiple tags**

<br/>

<br/>

## 3. CSS3

### CSS Syntax

- ```css
  div {
    display: block;
  }

  #id_name {
  }

  .className {
  }
  ```

1. selector
2. property

<br/>

### Connect CSS to HTML

1. inline

2. external

   - ```html
     <link rel="stylesheet" href="style.css" />
     ```

<br/>

### Box Model

- 4 components

  1. Margin

     - ```css
       body {
           margin: 20px;
           margin: 20px 10px; up-down left-right
           margin: 20px 10px 5px 2px; clock-wise
       }
       ```

  2. Border

     - ```css
       body {
         border-width: 5px;
         border-color: red;
         border-style: dashed;
         border: 10px dashed red;
       }
       ```

     - width, style, color

  3. Padding

     - ```cs
       body {
           padding: 20px;
           padding: 20px 10px; up-down left-right
           padding: 20px 10px 5px 2px; clock-wise
       }
       ```

  4. Content

<br/>

### Block, Inline Block, Inline

- `block`
  - takes up the whole line
- `display: inline-block;`
  - a box can only be `block` or`inline-block`
- `display: inline;`
  - removes every box property
    - `width: 200px;`
    - `height:30px;`
  - consider the content a text
  - when applied to `<span>`
    - CSS only applied around text content

<br/>

### Position

- Remove default styles by browser

  - ```css
    body,
    html {
      height: 100%;
      margin: 0;
      padding: 0;
    }
    ```

- 4 properties

  1. `position: static;`

     - default property

     - > statically created in the page

  2. `position: fixed;`

     - > fixed on the screen, it hangs

     - unlocks 4 properties = location determined by the `screen`

       1. `top: 10px;`
       2. `bottom: 10px;`
       3. `left: 30px;`
       4. `right: 50px`

  3. `position: absolute`

     - ```html
       <div class="abs-box">
         <div class="abs-child"></div>
       </div>
       ```

     - > position: absolute to the position: relative

     - when a tag's `position: absolute`

       - looks for `position: relative` on the parent
       - if fails -> absolute position relative to the `<body>`

  4. `position: relative`
     - works with `position: absolute`
     - if set, it works as the base `position` for the `child elements`
