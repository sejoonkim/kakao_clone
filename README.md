# kakao_clone

Contents

Theory

1. [Web Developer Tools](#1-web-developer-tools)
2. [HTML5](#2-html5)
3. [CSS3](#3-css3)
4. [Advanced CSS](#4-advanced-css)

Practice

1. [HTML](#1-html)
2. [CSS](#2-css)
3. [Animations](#3-animations)

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

<br/>

### Fluid Layouts with Flexbox

- Before: problems with grid layouts, columns, boxes

  - no **perfectly aligned** grids

  - ```html
    <div class="box">1</div>
    <div class="box">2</div>
    <div class="box">3</div>
    <div class="box">4</div>
    <div class="box">5</div>
    <div class="box">6</div>
    <div class="box">7</div>
    <div class="box">8</div>
    <div class="box">9</div>
    ...
    ```

  - will automatically move to the next line

- After

  - fix with `display: flex`

    - make `parent` container a `flex` container

    - do not need to talk to `child`

    - > "Hey parent, your children should look like this"

    - ```css
      .parent {
        display: flex;
        justify-content: space-around;
        align-items: flex-start;
        height: 100%;
      }
      ```

    - ```html
      <div class="parent">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
        <div class="box">4</div>
        <div class="box">5</div>
        <div class="box">6</div>
        <div class="box">7</div>
        <div class="box">8</div>
        <div class="box">9</div>
      </div>
      ```

  - `flex-direction: row`, `flex-direction:column`

    - how elements inside are shown
    - `justify-content`
      - horizontal -> vertical
    - `align-items`
      - vertical -> horizontal

  - `flex-wrap`

    - when find the end of the page, automatically move to the next line
    - `flex-wrap: nowrap;` = default

  - examples

    - ```css
      .parent {
        flex-direction: row-reverse; // column-reverse
        flex-wrap: reverse; // wrap-reverse
      }
      ```

<br/>

### CSS Selectors and Pseudo Selectors

- Situation

  1. do not know class name or id selector

- Pseudo Selector = selector that is not element

  - ```css
    input[type="submit"] {
      background-color: red;
    }
    ```

  - ```css
    .box:last-child {
      // first-child, nth-child(2), nth-child(2n), nth-child(2n+1) // from 1st element select 2n
      background-color: maroon;
    }
    ```

  - ```css
    input + .box {
      // brother
      border: 1px solid yellow;
    }
    ```

  - ```css
    input > .box {
      // direct child
      border: 1px solid yellow;
    }
    ```

<br/>

### CSS States

1. `:active`
   - mouse clicked
2. `:focus`
   - have higher priority compared to `:hover`
3. `:visited`
4. `:hover`
   - mouse on

<br/>

<br/>

## 4. Advanced CSS

### Transitions

- Link - [Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)

- Transitions appear when changes to `state`(**hover**, **active**, **focus**, visited)

- ```css
  transition: background-color 0.5s ease-in-out;
  ```

  - name of the property to change, duration, method

- ```css
  transition: all 0.5s ease-in-out;
  ```

  - change all properties

### Transformations

- Link - [Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)

- combined with `transitions`

  - ```css
    .box {
      width: 500px;
      height: 500px;
      background-color: red;
      transition: transform 0.5s ease-in-out;
    }

    .box:hover {
      transform: rotate(5turn) scale(0.5, 0.5);
    }
    ```

<br/>

### Animations

- syntax

  - `@keyframes ANIMATION_NAME` - stating the animation
  - 2 steps
    1. `from~to`
    2. `0% ~ 50% ~ 100%`

- example

  - ```css
    .box {
      animation: 1.5s scaleAndRotateSquare infinite ease-in-out;
    }

    @keyframes scaleAndRotateSquare {
      /* from {
            transform: none;
        }
        to {
            transform: rotate(1turn) scale(.5, .5);
        } */
      0% {
        transform: none;
      }
      50% {
        transform: rotate(1turn) scale(0.5, 0.5);
      }
      100% {
        transform: none;
      }
    }
    ```

  - `from~to` is one way, 2 stages

  - `0% ~ 50% ~ 100%` can be both ways

<br/>

### Media Queries

- example

  - ```css
    @media screen and (min-width: 320px) and (max-width: 640px) {
      body {
        background-color: red;
      }
    }
    ```

    - CSS applied when the screen's min and max width are set accordingly

<br/>

<br/>

## 1. HTML

### Status Bar, Header

- BEM model

  - used when two or more states are used for a tag/component

  - `block--modifier-value`

    ```html
    <button class="button">
      Normal button
    </button>
    <button class="button button--state-success">
      Success button
    </button>
    <button class="button button--state-danger">
      Danger button
    </button>
    ```

    ```css
    .button {
      display: inline-block;
      border-radius: 3px;
      padding: 7px 12px;
      border: 1px solid #d5d5d5;
      background-image: linear-gradient(#eee, #ddd);
      font: 700 13px/18px Helvetica, arial;
    }
    .button--state-success {
      color: #fff;
      background: #569e3d linear-gradient(#79d858, #569e3d) repeat-x;
      border-color: #4a993e;
    }
    .button--state-danger {
      color: #900;
    }
    ```

  - parent-chlid relationship

    ```html
    <div class="button">
      <div class="button__child">
        Child Div
      </div>
    </div>
    ```

* Icons

  - fontawesome

  - add `<script>` tag to `<header>`

    ```html
    <script src="URL" crossorigin="anonymous"></script>
    ```

  - use with `<i>` tag

    ```html
    <i class="fas fa-clock"></i>
    ```

<br/>

### Navigation Bar

- change icon to simulate selected

<br/>

### Chat Screen

- Structuring classes
  - chats
    - chats\_\_list
      - chat\_\_column
      - chat\_\_column

<br/>

### Friends Screen

- create a `global class` for repeated elements

  - `g-avatar`

- BEM model
  - `__` = parent\_\_child
  - `--` = element--NewTrait

<br/>

### Find Screen

- copy HTML structure from Friends Screen
