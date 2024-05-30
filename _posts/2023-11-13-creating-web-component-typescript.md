---
layout: post
title:  "Creating Web Component in Typescript and deploying to github page!"
summary: "Creating Web Component in Typescript and deploying to github page"
author: spradeep
date: '2023-11-13 14:35:23 +0530'
category: Web Component, UI, github page, Typescript
keywords: web component, create web component, javascript, Web component , github, static page, Typescript
permalink: /blog/creating-web-component-typescript-github-page/
usemathjax: true
---

Web Components is a suite of different technologies allowing you to create reusable custom elements — with their functionality encapsulated away from the rest of your code — and utilize them in your web apps.

TypeScript is a free and open-source high-level programming language that adds static typing with optional type annotations to JavaScript. It is designed for the development of large applications and transpiles to JavaScript

Here is an example of web component in Typescript, The web component can be deployed in github page and source code is available for fork.

1. Create a Typescript file and define a class 


```Typescript
class MyFirstWebComponent extends HTMLElement {
    connectedCallback() {
      this.innerHTML = `<h1>Hi Koushik Kumar Ganeeb</h1> `;
    }
  }
customElements.define('my-first-web-component', MyFirstWebComponent);

document.body.innerHTML = `<my-first-web-component></my-first-web-component>`
```

2. Create a html file to incluide Typescript code that creates a web component

```javascript
<!doctype html>
<html>
  <head>
    <title>This is my first web component!</title>
    <script type="text/typescript" src="script.ts"></script>
  </head>
  <body>
    
  </body>
</html>
```

3. Doing this will not work. As Typescript needs to be compiled into Javascript.

4. So load the library that compiles the typescript and loads Javascript. [Code is here](https://github.com/pradeepin2/create-web-component-typescript)

5. So try online fork [this repo](https://github.com/pradeepin2/create-web-component-typescript) and deploy it as a github page to see web component created in Typescript

[https://github.com/pradeepin2/create-web-component-typescript](https://github.com/pradeepin2/create-web-component-typescript)

