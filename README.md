import tkinter as tk
import random

# List of symbols
symbols = ['🍒', '⭐', '🍋', '🔔', '💎', '7']

def spin():
    reel1.config(text=random.choice(symbols))
    reel2.config(text=random.choice(symbols))
    reel3.config(text=random.choice(symbols))

# Set up window
root = tk.Tk()
root.title("Slot Machine")

# Reels
reel1 = tk.Label(root, text='?', font=('Helvetica', 48))
reel2 = tk.Label(root, text='?', font=('Helvetica', 48))
reel3 = tk.Label(root, text='?', font=('Helvetica', 48))

# Layout
reel1.pack(side='left', padx=10)
reel2.pack(side='left', padx=10)
reel3.pack(side='left', padx=10)

# Spin button
spin_button = tk.Button(root, text="Spin!", command=spin)
spin_button.pack(pady=20)

root.mainloop()
