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

# List of outcomes
outcomes_list = [one, two, three, four, five, six]

print("🎲 This is a Dice Simulator 🎲")

x = "y"
while x.lower() == "y":
    # Roll two dice
    random_outcome = random.choices(outcomes_list, k=2)
    for outcome in random_outcome:
        print(outcome)
    x = input("Press 'y' to roll again, any other key to quit: ")

print("Thanks for playing!")
