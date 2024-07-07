---
layout: default
description: treasure?
title: X Marked the Spot
id: xmark
---

<link rel="stylesheet" href="../writeupcss.css">
<link rel="stylesheet" href="../code.css">

<h2>
{{ site.subtitle }}
</h2>

[Home](https://stainedswan.github.io/UIUCTF-2024)
[OSINT](https://stainedswan.github.io/UIUCTF-2024/OSINT)
[Crypto](https://stainedswan.github.io/UIUCTF-2024/Crypto)
[Miscellaneous](https://stainedswan.github.io/UIUCTF-2024/Miscellaneous)

# X Marked the Spot Writeup

<div style="text-align:center" markdown="1">
<h2>

Description
</h2>
</div>

<div style="text-align:center"><img src="image.png" width=700/></div>

## Information gained from prompt
- public.py file
- ct file (contains the ciphertext)

### public.py file contents

```python
from itertools import cycle

flag = b"uiuctf{????????????????????????????????????????}"
# len(flag) = 48
key  = b"????????"
# len(key) = 8
ct = bytes(x ^ y for x, y in zip(flag, cycle(key)))

with open("ct", "wb") as ct_file:
    ct_file.write(ct)
```

## Information Gathering Stage
The first thing we had to do was figure out how the `zip()` and `cycle()` functions worked. We figured out that the zip function takes two elements and groups their corresponding pairs into tuples. This is also explained in the [Python functions docs](https://docs.python.org/3/library/functions.html#zip). 

Then we move to the cycle function, it iterates over an element until it is exhausted (not to say that it is tired, but that there is nothing more to iterate over), as described in [Python iterator docs](https://docs.python.org/3/library/itertools.html#itertools.cycle). 


## Thinking Stage
With this, we understood that the program was taking the 8 letter key and XOR'ing it against the 48 letter flag in groups of 8 since the key had 8 letters. From there, we took the ciphertext and plugged it into VSCode's hex editor to get the ciphertext's binary. We then grouped it into 6 elements, each of which would be the key XOR'ed with a piece of the plaintext. 

![alt text](image-3.png)

## The Solve
We figured out that the first 7 elements of the ciphertext had to correspond to uiuctf{ and that the last element of the ciphertext had to correspond to }. So, to figure out the key, we need to XOR uiuctf{} with the appropriate elements of the ciphertext to retrieve the key. *From there, we just XOR'ed the key with the ciphertext to get the flag.*

### Manual Key Calculation
```
key[0] = 0x1D ^ 117 = 0x1D ^ 0x75 = 0x68 = 104
key[1] = 0x0D ^ 105 = 0x0D ^ 0x69 = 0x64 = 100
key[2] = 0x1C ^ 117 = 0x1C ^ 0x75 = 0x69 = 105
key[3] = 0x12 ^ 99 = 0x12 ^ 0x63 = 0x71 = 113
key[4] = 0x16 ^ 116 = 0x16 ^ 0x74 = 0x62 = 98
key[5] = 0x00 ^ 102 = 0x00 ^ 0x66 = 0x66 = 102
key[6] = 0x11 ^ 123 = 0x11 ^ 0x7B = 0x6A = 106
key[7] = 0x0C ^ 0x7D = 0x71
```

```txt
The flag for X Marked the Spot is uiuctf{n0t_ju5t_th3_st4rt_but_4l50_th3_3nd!!!!!}
```

Written by @cornguy.

Formatted by @goldenscience