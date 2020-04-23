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
