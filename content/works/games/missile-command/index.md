---
title: Missile Command
date: 2017-08-18T00:00:00-03:00
description: My version of the classic Missile Command game.
menu:
  sidebar:
    name: Missile Command
    identifier: missile-command
    parent: games
    weight: 4
# hero: images/forest.jpg
tags: ["Missile", "Command", "Game"]
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
<script type="text/javascript" src="/js/missile_command.js"></script>

# How to play
* Arrow keys: Move cursor
* Z: Shoot
* P: Pause
* Destroy enemy's missiles to protect your cities!!