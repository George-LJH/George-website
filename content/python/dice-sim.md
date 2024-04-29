+++
chapter = false
title = "Dice Rolling Simulator"
tags = ["theme"]
weight = 0
+++


# Dice Rolling Simulator
```python
import random


again = True
while again:
   rolled_number = random.randint(1,6)
   print(f"ROLLED{rolled_number}")
   roll_again = input("Want to roll again?")
   if roll_again.lower == "y":
      continue
   else:
      break
```
