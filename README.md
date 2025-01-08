Rainbow Text Generator 🌈

Description

Welcome to the Rainbow Text Generator, a fun and creative Python program that adds colors to your text based on specific characters. This tool is simple, interactive, and demonstrates how to use ANSI escape codes to create vibrant outputs in the terminal. Whether you're a Python beginner or a coding enthusiast, this project is a delightful way to explore colorful possibilities!

Features

🎨 Dynamic Coloring: Assigns specific colors to letters (r, g, b, p, y) using ANSI escape codes.

✨ Interactive Experience: Colors your text in real-time as you type.

🐍 Beginner-Friendly: Ideal for Python learners and hobbyists.

Table of Contents

Features

Demo

Installation

Usage

Code Explanation

Code

Contributing

License

Demo

Enter a sentence and watch as the script transforms it into a rainbow masterpiece! 🌈

Example

If you type:

This is a rgby test!

The output will display the colors:

r as Red

g as Green

b as Blue

y as Yellow

Characters that don't match any specific colors will remain in the default terminal color.

Installation

Clone the repository:

git clone https://github.com/YourUsername/rainbow-text-generator.git

Navigate to the project directory:

cd rainbow-text-generator

(Optional) Set up a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Usage

Run the script:

python rainbow_text.py

Enter a sentence: Follow the prompt and type a sentence to see it transformed into vibrant colors.

Screenshot

Coming soon! Add your screenshots here to showcase the colorful output. 🌟

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

Contributing

Contributions are welcome! Here's how you can help:

🔧 Add support for additional colors.

🌟 Introduce bold, italic, or gradient effects.

🎉 Add features like random color cycling or multi-line support.

Feel free to fork the project and submit a pull request with your improvements.

License

This project is licensed under the MIT License. See the LICENSE file for more information.

Enjoy making your text colorful and fun! 🌈💻

