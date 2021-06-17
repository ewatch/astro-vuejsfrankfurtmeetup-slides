---
theme: seriph
class: text-center
fonts:
  sans: Arial
  serif: Arial
  mono: Fira Code
layout: cover
background: ./images/slide-title.png
title: Using Astro
---

# Using Astro

<div class="flex justify-center items-center">
  <twemoji-rocket class="m-8 text-3xl text-orange-400 animate-pulse" />
  <img class="w-16 m-8" src="/images/astro.png">
  <img class="w-16 m-8" src="/images/vuejsfrankfurt-logo.png">
</div>

<!--
Welcome to the Astro Universe.
This is a page rendered with the Astro dev server.
With Astro you can travel to the Planet Svelte.
From Svelte we can also travel to React.
So let's now travel to our homebase Vue :-).

This was already one of the features I was totally caught of.
Sure at first there might be nothing special of rendering three JavaScript frameworks on the same page.
But how it's done in Astro is really different.
-->

---

# Who am I

- I am Jan, 36 years old
- currently DevOps Engineer, doing web development since a long time
- passionate about new technologies and learning


---

# What are we talking about today

- What is Astro ?
- Goals of Astro
- Mechanisms (Project Structure, Routing, ...)
- Things I'd like you to know about
- Future outlook
- Feedback, Questions & Open Discussion

<!--


I will write down all the questions that I can't respond in detail and add them to the meetup event
-->

---

# What is Astro ?

- Static Site Generator
- Bring your own JavaScript Framework
- Islands Architecture
- HTML first build tool
- Based on Snowpack (Module Bundler, heavily relies on ES Modules)


<!-- 
ZERO Configuration JavaScript
HTML First => only renders HTML, the goal is less JavaScript

The repository was made public last week.
Astro is currently in early beta version. So there are still bugs here in there.
So bear with me if I run into an error and have to skip something.

BYOF Svelte, React / Preact, VueJS

HTML first build tool
Building pages with no or low amount of JavaScript
and only add as much as you need

What are ES Modules ? 
CommonJS — the module.exports and require syntax used in Node.js
Asynchronous Module Definition (AMD)
Universal Module Definition (UMD).

Scoping
Isolating javascript
explicitly exporting variables / functions

Supported by Node 14.16.1

https://caniuse.com/es6-module
https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/

-->

---

# Goals

- make better and faster webpages
  - power web applications
  - expression and possibilities of JavaScript
  - ship as less as possible through the browser (Simplicity of Webpages / Speed of Static HTML)
- have a nice developer experience

---

# Mechanisms

- Project Structure
- Astro files (pages / components without runtime)
- Markdown OOB
- Hydration
- Routing

---

# Initializing a new project

```bash
# create your project
mkdir new-project-directory
cd new-project-directory
npm init astro

# install your dependencies
npm install

# start the dev server and open your browser
npm start
```

---
layout: cover
background: './images/folder-structure.jpg'
---

# Project Structure

<!--
1. npm init astro
2. code .
3. show
- public folder
- src folder
    - pages (Entrypoint)
    - components
    - data
    - layouts
- astro.config.mjs

What are mjs files ?
-->

---

# Astro files

- have the `.astro` extension
- can be pages 
- can be components
- consist of HTML
    - add frontmatter script section for server side rendering
    - add JSX for templating

<!-- 
1. Create a astro file with HTML (meetup landingpage)
2. Add frontmatter 
  variable 
  Array
3. Show JSX rendering
4. create components for showing a meetup with title / time / description
5. import json data and render meetup data


What is frontmatter ? 
limitations in the block
Currently no node modules can be imported => Keep the processing runtime agnostic (it's discussed)

Limits of JSX ? 
-->

---
layout: cover
background: './images/markdown-cutted.png'
---

# Markdown Support

<!--
1. Create a markdown Example file
    - with GFM (todo list)
    - syntax highlighting
    - footnotes (remark-footnotes)
2. Create a layout
3. Show rendering of the markdown files
-->

---

# Islands architecture & Partial Hydration

<div class="block bg-contain w-md h-sm bg-light-50" style="background-image: url('./images/islands.png')"></div>

<!--

termin is coined by Jason Miller the Creator of Preact 

Astro generates static pages by default

- render HTML pages on the server
- inject placeholders or slots around highly dynamic regions
- These placeholders/slots contain the server-rendered HTML output from their corresponding widget"

seperated islands which don't influence the rest of the page


astro provides modifiers only for JavaScript Framework Components that influence when the component is actually hydrated
-->

---


# Where is Vue ?

Let's integrate Vue in our project...

<!--
1. Create a Vue component to render a Meetup with thumbs up / down
2. Replace Astro component with vue
3. render the first three components without modifier, the other ones with visible
3. Show no interactivity with network tab
5. Show load modifier, Show visible modifier (IntersectionObserver), Show idle modifier

requestIdleCallback
This enables developers to perform background and low priority work on the main event loop, without impacting latency-critical events such as animation and input response

8. Create an MDX example with a Vue component

-->

---
layout: image-right
image: './images/astro-routing-rendering.png'
---

# Routing

---

# Other features I want you to know about

- Collections API
- Tailwind support
- Generation of sitemap.xml
- State libraries (Vuex)
- Styling


| Framework        | Global CSS | Scoped CSS | CSS Modules |
| :--------------- | :--------: | :--------: | :---------: |
| Astro (`.astro`) |     ✅     |     ✅     |    N/A      |
| React / Preact   |     ✅     |     ❌     |     ✅      |
| Vue              |     ✅     |     ✅     |     ✅      |
| Svelte           |     ✅     |     ✅     |     ❌      |

<!--
Collections API is about having multiple markdown files in a folder (as an example post) and generating a variable for the page holding a pagination urls of the next / previous page total number of posts and so on

Tailwind
npm install it
create a tailwind config and add it to the astro config

-->

---

# Future Outlook

- Currently positioned as Static Site Generator
- support of more frameworks (possible)
- mixture between static and dynamic sites (possible)
- Named Slots
- Image Support

<!--
Frameworks: Renderer interface (Feature Requests for: Angular, Lit SSR, Ember)
  - OOB <=> Plugins
For Utility CSS: WindiCSS
Modifiers: Can theoretically be added to the framework two
-->

---

# Resources

- https://astro.build
- https://github.com/snowpackjs/astro
- https://twitter.com/astrodotbuild
- https://css-tricks.com/astro/


## Join Discord

- https://astro.build/chat

## Show Cases

- https://divriots.com
- https://navillus.dev
- https://aseemtaneja.com/why-i-built-my-blog-with-astro/

---
layout: center
---

# Thank you for listening

## Feedback, Questions & Open Discussion

<!--
did you like the presentation ?
do you want to try astro ?
do you have questions ?
any topics / ideas to discuss ?
what would you like to see ?
-->
