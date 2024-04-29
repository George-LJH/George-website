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


<video width="320" height="240" controls>
  <source src="images/dice-sim.webm" type="video/webm">
</video>
