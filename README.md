import random

# Dice faces as ASCII art
one = """\
+-----------+
|           |
|     O     |
|           |
+-----------+"""

two = """\
+-----------+
| O         |
|           |
|         O |
+-----------+"""

three = """\
+-----------+
| O         |
|     O     |
|         O |
+-----------+"""

four = """\
+-----------+
| O       O |
|           |
| O       O |
+-----------+"""

five = """\
+-----------+
| O       O |
|     O     |
| O       O |
+-----------+"""

six = """\
+-----------+
| O       O |
| O       O |
| O       O |
+-----------+"""

outcomes_list = [one, two, three, four, five, six]
print("This is a dice stimulator")
x = "y"
while x == "y":
    randon_outcome = random.sample(outcomes_list, 2)
    for outcome in randon_outcome:
        print(outcome)
    
    x =  input("Press y to roll again ") 
    
