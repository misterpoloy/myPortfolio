<h1 align="center">Juan Pablo Ortíz</h1>

<div align="center">
  <strong>Software Engineer</strong>
</div>
<div align="center">
  <code>janpoloy@gmail.com</code> 📍Mexico City 🇲🇽
</div>
<br />

<div align="center">

  <!-- Github -->
  <img alt="GitHub followers" src="https://img.shields.io/github/followers/misterpoloy?logo=github&style=for-the-badge">
  <!-- Twitter -->
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/janpoloy?label=%40janpoloy&logo=twitter&style=for-the-badge">
</div>

<div align="center">
  <h3>
    <a href="#">
      Twitter
    </a>
    <span> | </span>
    <a href="#">
      Youtube
    </a>
    <span> | </span>
    <a href="#">
      Medium
    </a>
    <span> | </span>
    <a href="#">
      Stack Overflow
    </a>
  </h3>
</div>

<div align="center">
  <sub>As Seen on
  <a href="https://twitter.com/yoshuawuyts">Forbes</a> and
  <a href="https://github.com/choojs/choo/graphs/contributors">
    Microsoft
  </a>
</div>

## Languages
[![Generic badge](https://img.shields.io/badge/C++-advanced-green.svg)](https://shields.io/)

[![Generic badge](https://img.shields.io/badge/Javascript-advanced-green.svg)](https://shields.io/)

[![Generic badge](https://img.shields.io/badge/Python-learning-yellow.svg)](https://shields.io/)

## Table of Contents
- [Data estructures](#features)
- [Algorithms](#example)
- [Mobile](#philosophy)
- [Frontend](#events)
- [Backend](#state)
- [Original articles](#state)

## Data estrucures
- __minimal size:__ weighing `4kb`, Choo is a tiny little framework
- __event based:__ our performant event system makes writing apps easy
- __small api:__ with only 6 methods there's not much to learn
- __minimal tooling:__ built for the cutting edge `browserify` compiler
- __isomorphic:__ renders seamlessly in both Node and browsers
- __very cute:__ choo choo!

## Example
```js
var html = require('choo/html')
var devtools = require('choo-devtools')
var choo = require('choo')

var app = choo()
app.use(devtools())
app.use(countStore)
app.route('/', mainView)
app.mount('body')

function mainView (state, emit) {
  return html`
    <body>
      <h1>count is ${state.count}</h1>
      <button onclick=${onclick}>Increment</button>
    </body>
  `

  function onclick () {
    emit('increment', 1)
  }
}

function countStore (state, emitter) {
  state.count = 0
  emitter.on('increment', function (count) {
    state.count += count
    emitter.emit('render')
  })
}
```
Want to see more examples? Check out the 
