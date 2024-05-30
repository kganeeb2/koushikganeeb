---
layout: post
title:  "Creating Web Component and deploying to github page!"
summary: "Creating Web Component and deploying to github page"
author: spradeep
date: '2023-11-12 14:35:23 +0530'
category: Web Component, UI, github page
keywords: web component, create web component, javascript, Web component , github, static page
permalink: /blog/creating-web-component-github-page/
usemathjax: true
---

Web Components is a suite of different technologies allowing you to create reusable custom elements — with their functionality encapsulated away from the rest of your code — and utilize them in your web apps.

Here is an example of web component, The web component can be deployed in github page and source code is available for fork.

1. Create a Javascript file and define a class 


```javascript
class MyFirstWebComponent extends HTMLElement {
    connectedCallback() {
      this.innerHTML = `<h1>Hi Koushik Kumar Ganeeb</h1>`;
    }
  }
customElements.define('my-first-web-component', MyFirstWebComponent);
```

2. Create a html file to incluide JS code that creates a web component

```javascript
<!doctype html>
<html>
  <head>
    <title>This is my first web component!</title>
    <script src="MyFirstWebComponent.js"></script>
  </head>
  <body>
    <my-first-web-component></my-first-web-component>
  </body>
</html>
```

3. If you want to try online fork [this repo](https://github.com/pradeepin2/create-web-component/tree/main).  and deploy it as a github page

[https://github.com/pradeepin2/create-web-component/tree/main](https://github.com/pradeepin2/create-web-component/tree/main)




