---
title: Derivative Calculator
date: 2016-11-15T00:00:00-03:00
description: A derivative calculator.
menu:
  sidebar:
    name: Derivative Calculator
    identifier: derivative-calculator
    parent: apps
    weight: 1
hero: derivative-calculator-cover.png
tags: ["Derivative", "Calculator", "App"]
categories: ["Personal"]
---

This app calculates the derivative of a function for you. It parses the input into a tree of operators, numbers and variables, passes through the tree deriving the functions and then transforms it back to LaTeX, so the result can be shown.

It is not optmized, so you may have to do some algebraic manipulations to simplify the result.

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
* Write the function at the first line
* Put the variable you want to derivate in at the second line
* Click on the "Calculate" button and see the derivative!

## Valid functions and variables
* Variables can be an upper or lower case letter (excluding "e"), and can have a subscript character using "_". Ex.: x_i
* For unary "-" use "~" instead, or it will not read correctly the input
* You can use the constants e, pi and gr (golden ratio)
* Power was implemented as x^y and square root was implemeted as sqrt(x)
* Logarithm is implemented as log(b, x) (base b) and ln(x) (base e)
* Trigonometric functions are implemented (sin, cos, tan), moreover, their reciprocals (sec, csc, cot), inverses (arcsec, arccos, arctan, arcsec, arccsc, arccot) and hyperbolic versions (sinh, cosh, tanh, sech, csch, coth) are implemented too
* sum(a, b, x_i) = summation of x_i's, with i going from a to b (a and b can be almost anything) (Obs.: when using this notation, the derivation at the iteration variable x_i is not available)
* Factorial is NOT implemented