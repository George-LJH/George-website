+++
chapter = false
title = "Dice Rolling Simulator"
tags = ["Coding","Python"]
weight = 0
+++


## Dice Rolling Simulator
```python
import random
again = True
while again:
    
    print(random.randint(1,6))
    another_roll = input("Want to roll the dice again? (y/n):")
    if another_roll.lower() == "y":
        continue
    else:
        break

```

Explanation of code:
Line 1 import the module random,
The Line 
