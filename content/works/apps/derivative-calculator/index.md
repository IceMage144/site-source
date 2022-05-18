---
title: Derivative Calculator
date: 2016-11-15T00:00:00+03:00
description: A derivative calculator.
menu:
  sidebar:
    name: Derivative Calculator
    identifier: derivative-calculator
    parent: apps
    weight: 1
# hero: images/forest.jpg
tags: ["Derivative", "Calculator", "App"]
categories: ["Personal"]
---

<link rel="stylesheet" type="text/css" href="/css/derivative.css" />

## Function
<div class="inputBorder">
  <input type="text" id="formInput"/>
</div>

## Variable
<div class="inputBorder">
  <input type="text" id="varInput"/>
</div>

<input id="calc" type="submit" value="Calculate" onclick="main()"/>
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

## How to use
* Put the function in the first line
* Put the variable you want to derivate in at the second line
* Click on the "Calculate" button and see the derivative!

## Valid functions and variables
* Variables can be an upper or lower case letter (excluding "e"), and can have subscript using "_", ex.: x_i
* To use unary "-", use "~" or it will show an error message
* You can use the constants e, pi and gr (golden ratio)
* Power was implemented as a^b and square root was implemeted as sqrt(a)
* log and ln were implemented too
* Every trigonometric function were implemented (reciprocals, inverses and hiperbolics too)
* sum(a, b, x_i) = summation of x_i's, with i going from a to b (a and b can be almost anything) (Obs.: don't try to derivate it in x_i!)
* Factorial is not implemented
* You may have to do some algebraic manipulations to simplify the result :)