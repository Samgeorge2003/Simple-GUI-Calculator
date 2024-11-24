# Simple-GUI-Calculator
 A simple calculator GUI built with Tkinter in Python. It supports basic arithmetic operations such as addition, subtraction, multiplication, and division.

# Python Code

import tkinter as tk
def button_click(number):
    current = entry.get()
    entry.delete(0, tk.END)
    entry.insert(0, current + str(number))
def clear():
    entry.delete(0, tk.END)
def add():
    global first_number
    global math_operation
    math_operation = "addition"
    first_number = float(entry.get())
    entry.delete(0, tk.END)
def subtract():
    global first_number
    global math_operation
    math_operation = "subtraction"
    first_number = float(entry.get())
    entry.delete(0, tk.END)
def multiply():
    global first_number
    global math_operation
    math_operation = "multiplication"
    first_number = float(entry.get())
    entry.delete(0, tk.END)
def divide():
    global first_number
    global math_operation
    math_operation = "division"
    first_number = float(entry.get())
    entry.delete(0, tk.END)
def equals():
    second_number = float(entry.get())
    entry.delete(0, tk.END)
    if math_operation == "addition":
        entry.insert(0, first_number + second_number)
    elif math_operation == "subtraction":
        entry.insert(0, first_number - second_number)
    elif math_operation == "multiplication":
        entry.insert(0, first_number * second_number)
    elif math_operation == "division":
        if second_number == 0:
            entry.insert(0, "Error")
        else:
            entry.insert(0, first_number / second_number)
# Create main window
root = tk.Tk()
root.title("Simple Calculator")
# Entry widget for displaying input and result
entry = tk.Entry(root, width=35, borderwidth=5, justify='right')
entry.grid(row=0, column=0, columnspan=4, padx=10, pady=10)
# Define buttons
button_1 = tk.Button(root, text="1", padx=20, pady=20, command=lambda: button_click(1))
button_2 = tk.Button(root, text="2", padx=20, pady=20, command=lambda: button_click(2))
button_3 = tk.Button(root, text="3", padx=20, pady=20, command=lambda: button_click(3))
button_4 = tk.Button(root, text="4", padx=20, pady=20, command=lambda: button_click(4))
button_5 = tk.Button(root, text="5", padx=20, pady=20, command=lambda: button_click(5))
button_6 = tk.Button(root, text="6", padx=20, pady=20, command=lambda: button_click(6))
button_7 = tk.Button(root, text="7", padx=20, pady=20, command=lambda: button_click(7))
button_8 = tk.Button(root, text="8", padx=20, pady=20, command=lambda: button_click(8))
button_9 = tk.Button(root, text="9", padx=20, pady=20, command=lambda: button_click(9))
button_0 = tk.Button(root, text="0", padx=20, pady=20, command=lambda: button_click(0))
button_add = tk.Button(root, text="+", padx=20, pady=20, command=add)
button_subtract = tk.Button(root, text="-", padx=20, pady=20, command=subtract)
button_multiply = tk.Button(root, text="*", padx=20, pady=20, command=multiply)
button_divide = tk.Button(root, text="/", padx=20, pady=20, command=divide)
button_equals = tk.Button(root, text="=", padx=20, pady=20, command=equals)
button_clear = tk.Button(root, text="C", padx=20, pady=20, command=clear)
# Place buttons on the grid
button_1.grid(row=3, column=0)
button_2.grid(row=3, column=1)
button_3.grid(row=3, column=2)
button_4.grid(row=2, column=0)
button_5.grid(row=2, column=1)
button_6.grid(row=2, column=2)
button_7.grid(row=1, column=0)
button_8.grid(row=1, column=1)
button_9.grid(row=1, column=2)
button_0.grid(row=4, column=0)
button_add.grid(row=1, column=3)
button_subtract.grid(row=2, column=3)
button_multiply.grid(row=3, column=3)
button_divide.grid(row=4, column=3)
button_equals.grid(row=4, column=2)
button_clear.grid(row=4, column=1)
# Run the application
root.mainloop()


# Features:
Numeric Buttons: For entering numbers.
Operation Buttons: +, -, *, /
Equals Button: To calculate the result.
Clear Button: To reset the input field.
