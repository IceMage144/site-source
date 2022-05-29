---
title: Snake
date: 2017-07-16T00:00:00-03:00
description: My version of the classic Snake game.
menu:
  sidebar:
    name: Snake
    identifier: snake
    parent: games
    weight: 1
hero: snake-cover.png
tags: ["Snake", "Game"]
categories: ["Personal"]
---

My version of the classic Snake game.
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

#### How to play
* Arrow keys: Move the snake
* P: Pause
* Eat apples to increase your score!!