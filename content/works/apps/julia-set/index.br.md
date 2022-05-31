---
title: Visualizador de conjuntos de Julia
date: 2018-02-01T00:00:00-03:00
description: Uma ferramenta para visualizar os conjuntos de Julia
menu:
  sidebar:
    name: Visualizador de conjuntos de Julia
    identifier: julia-set
    parent: apps
    weight: 2
hero: julia-set-cover.png
tags: ["Julia", "Conjunto", "App"]
categories: ["Pessoal"]
math: true
---

Esse app gera imagens dos conjuntos de Julia.
<!--more-->

O conjunto de Julia de um ponto c no plano complexo é definido como sendo o conjunto de pontos complexos z tais que a sequência abaixo não diverge.

$$a_0 = z$$
$$a_n = a_{n-1}^2 + c$$

Esse app gera uma imagem colorindo cada ponto do plano complexo com uma cor diferente dependendo do quão "rápido" a sequência divergiu quando ela começa naquele ponto.

Dado que o conjunto de Mandelbrot está profundamente ligado com os conjuntos de Julia (c é um ponto do conjunto de Mandelbrot se, e somente se, o conjunto de Julia daquele ponto não é vazio) o app também mostra uma imagem do conjunto de Mandelbrot para ajudar na escolha do ponto c.

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
  <input id="sub" class="row-el" type="submit" value="Enviar" onClick="sub()"/>
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

## Como usar
* Coloque um número complexo nos campos e clique em "Enviar" para ver o conjunto de Julia correspondente na tela da esquerda
* Você pode segurar a tecla Z e apontar com o mouse no conjunto de Mandelbrot na tela direita, assim o conjunto de Julia daquele ponto será gerado
* Você pode aumentar ou diminuir a resolução usando os botões "+" e "-"