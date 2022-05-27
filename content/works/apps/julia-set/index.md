---
title: Julia Set Visualizer
date: 2018-02-01T00:00:00-03:00
description: An online tool for visualizing Julia Sets.
menu:
  sidebar:
    name: Julia Set Visualizer
    identifier: julia-set
    parent: apps
    weight: 2
hero: julia-set-cover.png
tags: ["Julia", "Set", "App"]
categories: ["Personal"]
math: true
---

The Julia set of a complex point c is defined to be the set of complex points z such that the following sequence does not diverge.

$$a_0 = z$$
$$a_n = a_{n-1}^2 + c$$

This app generates a picture coloring each point of the complex plane with a different color depending on how "quickly" the sequence diverges when it starts at that point.

Since the Mandelbrot set is deeply linked with the Julia set (if c is a point of the Mandelbrot set, then the Julia set of that point is not empty) the app displays a picture of the Mandelbrot set to guide the choice of c.

<link rel="stylesheet" href="/css/julia.css">

<div id="gamediv">
  <div class="julia-row">
    <div class="julia-column">
      <h2>Julia</h2>
      <canvas id="julia"></canvas>
    </div>
    <div class="julia-column">
      <h2>Mandelbrot</h2>
      <canvas id="mand"></canvas>
    </div>
  </div>
</div>

<div class="input-group">
  <p class="row-el" style="font-size: 20px"> c = </p>
  <div class="row-el">
    <div class="inputBorder">
      <input type="text" id="real"/>
    </div>
  </div>
  <p class="row-el" style="font-size: 20px"> + i </p>
  <div class="row-el">
    <div class="inputBorder">
      <input type="text" id="imaginary"/>
    </div>
  </div>
  <input id="sub" class="row-el" type="submit" value="Submit" onClick="sub()"/>
</div>

<div class="res-group">
  <p id="res" class="row-el">Resolution: 200</p>
  <input class="row-el" type="submit" value="+" onClick="increaseResol()"/>
  <input class="row-el" type="submit" value="-" onClick="decreaseResol()"/>
</div>
<script>
  var onKeyPress = function(event)
  {
    if (event.keyCode == 13)
    {
      document.getElementById('sub').click();
    }
  }
  document.getElementById('real').onkeypress = onKeyPress
  document.getElementById('imaginary').onkeypress = onKeyPress
</script>

<script type="text/javascript" src="/js/game_engine.js"></script>
<script type="text/javascript" src="/js/julia_script.js"></script>

## How to use
* Enter an imaginary number at the fields to see the corresponding Julia set on the left canvas
* You can hold the Z key and point with the mouse to the Mandelbrot set, so you can see the Julia set of that point on the left canvas
* You can increase or decrease the resolution using the "+" and "-" buttons