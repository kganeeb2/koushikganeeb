---
layout: post
title:  "Html Web Component vs Javascript Web Component"
summary: "Html Web Component vs Javascript Web Component"
author: spradeep
date: '2023-11-24 14:35:23 +0530'
category: Web Component, HTML Web Component, Javascript Web Component
keywords: web component, create web component, javascript, Web component 
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

https://meyerweb.com/eric/thoughts/2023/11/01/blinded-by-the-light-dom/
https://codepen.io/davatron5000/pen/rNoRdex?editors=1010
https://blog.jim-nielsen.com/2023/html-web-components/
https://adactio.com/journal/20618
https://news.ycombinator.com/item?id=19640226
https://github.com/wisercoder/uibuilder
https://news.ycombinator.com/item?id=21585774
https://briangrinstead.com/blog/firefox-webcomponents/
https://dev.to/andreslopezrm/wordpress-web-components-awesome-na8