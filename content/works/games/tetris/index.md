---
title: Tetris
date: 2017-08-06T00:00:00-03:00
description: My version of the classic Tetris game.
menu:
  sidebar:
    name: Teris
    identifier: tetris
    parent: games
    weight: 2
hero: tetris-cover.png
tags: ["Tetris", "Game"]
categories: ["Personal"]
---

My version of the classic Tetris game.
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

#### How to play
* Left and right keys: Move the piece
* Down key: Increases piece's falling speed
* Z: Rotate the piece anticlockwise
* X: Rotate the piece clockwise
* P: Pause
* Fill the rows to increase your score!!