---
title: Snake
date: 2017-07-16T00:00:00-03:00
description: Minha versão do clássico jogo Snake.
menu:
  sidebar:
    name: Snake
    identifier: snake
    parent: games
    weight: 1
hero: snake-cover.png
tags: ["Snake", "Jogo"]
categories: ["Pessoal"]
---

Minha versão do clássico jogo Snake.
<!--more-->

<link rel="stylesheet" href="/css/game.css">

<!--
<input type="button" value="+" onclick="resize(1)">
<input type="button" value="-" onclick="resize(-1)">
-->
<div id="gamediv">
  <canvas id="game"></canvas>
</div>

<script type="text/javascript" src="/js/game_engine.js"></script>
<script type="text/javascript" src="/js/snake.js"></script>

#### Como jogar
* Setad: Movem a cobra
* P: Pausa
* Coma maçãs para aumentar sua pontuação