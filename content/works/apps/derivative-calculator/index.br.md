---
title: Calculadora de derivada
date: 2016-11-15T00:00:00-03:00
description: Uma calculadora de derivada
menu:
  sidebar:
    name: Calculadora de derivada
    identifier: derivative-calculator
    parent: apps
    weight: 1
hero: derivative-calculator-cover.png
tags: ["Derivada", "Calculadora", "App"]
categories: ["Pessoal"]
---

Esse app calcula a derivada de uma função. Ele transforma o texto da função em uma árvore contendo operadores, números e variáveis, percorre a árvore derivando as funções e depois a transforma texto LaTeX, para que o resultado possa ser mostrado.

Ele não é muito otimizado, então pode ser necessário fazer alguma manipulação algébrica no resultado.

<link rel="stylesheet" type="text/css" href="/css/derivative.css" />

## Função
<div class="inputBorder">
  <input type="text" id="formInput"/>
</div>

## Variável
<div class="inputBorder">
  <input type="text" id="varInput"/>
</div>

<input id="calc" type="submit" value="Calcular" onclick="main()"/>
<script>
  var a = function(e) {
    if (e.keyCode == 13)
      document.getElementById('calc').click();
  }
  document.getElementById('formInput').onkeypress = a
  document.getElementById('varInput').onkeypress = a
</script>

<p id="result" class="output">..........</p>
<p id="errorLog" class="output"></p>

<script type="text/javascript" src="/js/derivative_script.js"></script>
<script type="text/javascript" async
    src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_HTMLorMML">
</script>

## Como usar
* Escreva a função na primeira linha
* Coloque a variável na qual você deseja derivar a função na segunda liha
* Clique em "Calcular" e veja a derivada!

## Funções e variáveis válidas
* Variáveis podem ser letras maiúsculas ou minúsculas (exceto "e"), e podem ter um caractere subscrito usando "_". Ex.: x_i
* Para "-" unário use "~", ou a entrada não poderá ser lida corretamente
* Constantes e, pi e gr (razão de ouro) estão disponíveis
* Potênciação foi implementada como x^y e raiz quadrada como sqrt(x)
* Logarítmo foi implementado como log(b, x) (base b) e ln(x) (base e)
* Funções trigonométricas estão implementadas (sin, cos, tan), além de suas recíprocas (sec, csc, cot), inversas (arcsec, arccos, arctan, arcsec, arccsc, arccot) e versões hiperbólicas (sinh, cosh, tanh, sech, csch, coth)
* sum(a, b, x_i) é a soma dos x_i's, com i indo de a até b (a e b podem ser quase tudo) (Obs.: quando estiver usando esse recurso a derivada na variável de iteração x_i não fica disponível)
* Fatorial NÃO está implementado