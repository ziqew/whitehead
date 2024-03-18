

## AstroWind

npm run dev



python3 -m http.server 8080
./caddy run --config ./whitehead/Caddyfile

## Components

Component Template


Component props

slot

named slot

<div id="content-wrapper">
  <Header />
  <slot name="after-header" />  <!--  children with the `slot="after-header"` attribute will go here -->
  <Logo />
  <h1>{title}</h1>
  <slot />  <!--  children without a `slot`, or with `slot="default"` attribute will go here -->
  <Footer />
  <slot name="after-footer" />  <!--  children with the `slot="after-footer"` attribute will go here -->
</div>

## Pages
Pages are files that live in the src/pages/ subdirectory of your Astro project. They are responsible for handling routing, data loading, and overall page layout for every page in your website.

Astro supports the following file types in the src/pages/ directory:

.astro
.md
.mdx (with the MDX Integration installed)
.html
.js/.ts (as endpoints)


Using with a library
htmx


## Astro Syntax

JSX-like expressions
define local javascript in code fence ---

---
const name = "Astro";
---

variables

 <h1>Hello {name}!</h1>


Dynamic Attributes
 <h1 class={name}>Attribute expressions are supported</h1>

<MyComponent templateLiteralNameAttribute={`MyNameIs${name}`} />

---
function handleClick () {
    console.log("button clicked!");
}
---
<!-- not work-->
<button onClick={handleClick}>Nothing will happen when you click me!</button>

<!-- do like this-->
<button id="button">Click Me</button>
<script>
  function handleClick () {
    console.log("button clicked!");
  }
  document.getElementById("button").addEventListener("click", handleClick);
</script>


Dynamic HTML

---
const items = ["Dog", "Cat", "Platypus"];
---
<ul>
  {items.map((item) => (
    <li>{item}</li>
  ))}
</ul>


Fragments


Differences between Astro and JSX




node.js http server

export TZ='Asia/Shanghai'
http-server 
日志时间显示UTC时间