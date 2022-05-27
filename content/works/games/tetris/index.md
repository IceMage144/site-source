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
# hero: images/forest.jpg
tags: ["Tetris", "Game"]
categories: ["Personal"]
---

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

## How to play
* Left and right keys: Move the piece</li>
* Down key: Increases piece's falling speed</li>
* Z: Rotate the piece anticlockwise</li>
* X: Rotate the piece clockwise</li>
* P: Pause</li>
* Fill the rows to increase your score!!</li>