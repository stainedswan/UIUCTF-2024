---
layout: default
description: we were, in fact, determined
title: Determined
id: determined
---

<link rel="stylesheet" href="../writeupcss.css">

<h2>
{{ site.subtitle }}
</h2>

[Home](https://stainedswan.github.io/UIUCTF-2024)
[OSINT](https://stainedswan.github.io/UIUCTF-2024/OSINT)
[Crypto](https://stainedswan.github.io/UIUCTF-2024/Crypto)
[Miscellaneous](https://stainedswan.github.io/UIUCTF-2024/Miscellaneous)

# Determined Writeup

## Description

![alt text](image-2.png)

Looking at gen.txt, we realized that this challenge involved RSA encryption. Then, looking at server.py, we realized that we would somehow have to get the values for p and q out of the M matrix. Unlike the Without a Trace challenge, the sign() function would come into play as it was a factor in the return value. The return value would be a summation, and a good chunk of the operands would be 0 due to all of the 0’s in the matrix, so we wrote a sample script where the non zero values in the matrix would be 1 and figured out which permutations of the matrix would be non zero and what the corresponding signs would be. Once we had that, we figured that the way to solve this challenge would be to input a series of values that could result in the script outputting p or q. We figured out that the input sequence 100101110 would result in an output of -q. Given this, finding q was trivial. We then used a big numbers division calculator to find p, and then we plugged in our values to an rsa calculator to find the plaintext, which we then converted to hex and the subsequent hex to ascii to retrieve the flag.

Written by @cornguy.