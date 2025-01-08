Rainbow Text Generator 🌈

Description

Welcome to the Rainbow Text Generator, a fun and creative Python program that adds colors to your text based on specific characters. This tool is simple, interactive, and demonstrates how to use ANSI escape codes to create vibrant outputs in the terminal.

Features

🎨 Assigns specific colors to letters (r, g, b, p, y) using ANSI escape codes.

✨ Dynamically colors text as you type.

🐍 Easy-to-use and beginner-friendly Python script.

Table of Contents

Features

Demo

Code Explanation

Code

How to Run

Contributing

License

Demo

Enter a sentence and watch as the script transforms it into a rainbow masterpiece! Here is how it works:

Enter any sentence.

Letters like r, g, b, p, and y change to Red, Green, Blue, Purple, and Yellow, respectively.

All other characters are displayed in the default terminal color.

Example:

If you type:

This is a rgby test!

The output will display the colors:

r as Red

g as Green

b as Blue

y as Yellow

Code Explanation

Functions

setColor(color)

This function accepts a character and sets the terminal text color based on:

r = Red

g = Green

b = Blue

p = Purple

y = Yellow

Default or other characters = White (default terminal color)

Workflow

The program prompts the user for a sentence.

It loops through each character in the input:

If the character matches one of the predefined color keys, it sets the corresponding color.

Otherwise, it uses the default color.

It prints the sentence with the appropriate colors applied.

Code

Here is the Python script:

# Function for adding colors.
def setColor(color):
    if color == "r":
        print("\033[31m", end='')  # Red
    elif color == "g":
        print("\033[32m", end='')  # Green
    elif color == "b":
        print("\033[34m", end='')  # Blue
    elif color == "p":
        print("\033[35m", end='')  # Purple
    elif color == "y":
        print("\033[33m", end='')  # Yellow
    elif color == "":
        print("\033[0m", end='')  # Default or White

print("What sentence do you want rainbow-ising?")
sentence = input()
print()

# Loop through each character in the sentence.
for letter in sentence:
    if letter.lower() in ['r', 'g', 'b', 'p', 'y']:
        setColor(letter.lower())
    else:
        setColor("")
    print(letter, end='')

# Reset the terminal color to default.
setColor("")
print()

How to Run

Install Python: Make sure Python is installed on your computer (Python 3.x recommended).

Download the Script: Copy the script to a .py file, e.g., rainbow_text.py.

Run the Script:

python rainbow_text.py

Enter a sentence when prompted and see the colorful magic!

Contributing

Contributions are welcome! Here's how you can help:

Add support for additional colors.

Enhance styling options like bold or italic text.

Introduce color gradients or patterns.

Feel free to fork the project and submit a pull request with your improvements.

License

This project is licensed under the MIT License. See the LICENSE file for more information.

Enjoy making your text colorful and fun! 🌈

