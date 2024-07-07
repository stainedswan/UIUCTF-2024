---
layout: default
description: there is actually a trace
title: Without a Trace
id: notrace
---

<link rel="stylesheet" href="writeupcss.css">

<h2>
{{ site.subtitle }}
</h2>

[Home](https://stainedswan.github.io/UIUCTF-2024)
[OSINT](https://stainedswan.github.io/UIUCTF-2024/OSINT)
[Crypto](https://stainedswan.github.io/UIUCTF-2024/Crypto)
[Miscellaneous](https://stainedswan.github.io/UIUCTF-2024/Miscellaneous)

The first thing we had to do was figure out how the code worked. We realized that the inputs() function would be used to create a matrix where only the diagonal elements would be filled based on user input, and that the handler() and check() functions were used to check the validity of the matrix. Then, We figured out that the fun() function would return the trace (sum of the elements on the diagonal) of the product of the inputted matrix and a matrix where the diagonal elements were filled with pieces of the flag. We figured out that the way to solve this challenge would be to create 5 valid matrices and then use the trace to set up a system of equations and solve for each piece of the flag. To make this easy, we inputted 11111, 12111, 11211, 11121, and 11112. From there, we set up a system of equations using each coefficient we entered and the corresponding traces, solved for the decimal values of the flag, converted those decimals to hex and the hex to ascii, and retrieved the flag.

Written by @cornguy.