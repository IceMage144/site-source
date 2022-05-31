---
title: Tetris
date: 2017-08-06T00:00:00-03:00
description: Minha versão do clássico jogo Tetris.
menu:
  sidebar:
    name: Teris
    identifier: tetris
    parent: games
    weight: 2
hero: tetris-cover.png
tags: ["Tetris", "Jogo"]
categories: ["Pessoal"]
---

Minha versão do clássico jogo Tetris.
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
<script type="text/javascript" src="/js/tetris.js"></script>

#### Como jogar
* Setas esquerda e direita: Movem a peça
* Seta para baixo: Aumenta a velocidade da queda da peça
* Z: Rotaciona a peça em sentido anti-horário
* X: Rotaciona a peça em sentido horário
* P: Pausa
* Preencha as linhas para aumentar a pontuação!!