import tkinter as tk
import random

# Dice faces as ASCII art
dice_faces = [
    """+-----------+
|           |
|     O     |
|           |
+-----------+""",
    """+-----------+
| O         |
|           |
|         O |
+-----------+""",
    """+-----------+
| O         |
|     O     |
|         O |
+-----------+""",
    """+-----------+
| O       O |
|           |
| O       O |
+-----------+""",
    """+-----------+
| O       O |
|     O     |
| O       O |
+-----------+""",
    """+-----------+
| O       O |
| O       O |
| O       O |
+-----------+"""
]

def roll_dice():
    # Randomly choose two dice
    dice = random.choices(dice_faces, k=2)
    label1.config(text=dice[0])
    label2.config(text=dice[1])
root = tk.Tk()
root.title("🎲 Dice Simulator")
root.geometry("400x300")
root.config(bg="#202020")
title = tk.Label(root, text="Dice Simulator", font=("Courier", 18, "bold"), fg="white", bg="#202020")
title.pack(pady=10)
frame = tk.Frame(root, bg="#202020")
frame.pack(pady=10)
label1 = tk.Label(frame, text=dice_faces[0], font=("Courier", 10), fg="white", bg="#202020", justify="left")
label1.grid(row=0, column=0, padx=10)
label2 = tk.Label(frame, text=dice_faces[0], font=("Courier", 10), fg="white", bg="#202020", justify="left")
label2.grid(row=0, column=1, padx=10)
roll_button = tk.Button(root, text="🎲 Roll Dice", command=roll_dice, font=("Arial", 12, "bold"), bg="#28a745", fg="white", relief="raised")
roll_button.pack(pady=10)
exit_button = tk.Button(root, text="Exit", command=root.destroy, font=("Arial", 10, "bold"), bg="#dc3545", fg="white")
exit_button.pack(pady=5)
root.mainloop()
