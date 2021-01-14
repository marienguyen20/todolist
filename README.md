# Create a To Do List Application

It is a simple desktop project system created using the Python Programming Language, it is design using tkinter and the project file contains(todolist.py).
Python gives TKinter toolkit to increase graphical user interface packages.

Before you start to create a To Do List Project in Python, make sure that you have Pycharm IDE installed in your computer.

## Steps to create a To Do List Application in Python:

Step 1: Create a Project Name.
First step open the PyCharm IDE and click “File” and select “New Project” and then create a project name after that click the “create” button.

Step 2: Create a Python File.
Second step after creating a project name, “right” click the project name and the click “New” after that choose “Python File“.

Step 3: Name the Python File.
Third step after choose Python File name the file “todolist” and then click “Enter“.

Step 4: The actual code.
Now you can start coding, you are free to copy the code that being provided below.

## Importing Tkinter Module

Tkinter is the standard GUI library for Python. Python when combined with Tkinter provides a fast and easy way to create GUI applications.

import tkinter
from tkinter import messagebox

## Module for the Design Main Screen Window
root = tkinter.Tk()
root.geometry("460x480")
root.title("Students to do List Reminder")
root.rowconfigure(0, weight=1)
root.config(bg="blue")


frame = tkinter.Frame(root)
frame.pack()


lbl = tkinter.Label(root, text="Enter Tasks To Do:", fg="white", bg="blue",
                    font=('Arial', 14), wraplength=200)
lbl_hrs = tkinter.Label(root, text="Enter time (Seconds)", fg="white",
                        bg="blue", font=('Arial', 14), wraplength=200)
todo = tkinter.Entry(root, width=30, font=('Arial', 14))
time = tkinter.Entry(root, width=15, font=('Arial', 14))
post = tkinter.Button(root, text='Add task', fg="white", bg='green',
                      font=('Arial', 16), relief="ridge", bd=5, height=3,
                      width=30, command=getting_tasks)
Exit = tkinter.Button(root, text='Exit', fg="white", bg='red', height=3,
                      font=('Arial Bold', 14), relief="ridge", bd=5, width=30, command=root.destroy)
WorkingList = tkinter.Listbox(root, font=('Arial', 12

                                          ))
if tasks != "":
    actual_time()

root.bind('&lt;Return&gt;', getting_tasks)


lbl.place(x=0, y=10, width=200, height=25)
lbl_hrs.place(x=235, y=10, width=200, height=25)
todo.place(x=20, y=40, width=160, height=25)
time.place(x=245, y=40, width=170, height=25)
post.place(x=62, y=80, width=100, height=25)
Exit.place(x=302, y=80, width=50, height=25)
WorkingList.place(x=20, y=120, width=395, height=300)

## Module for the Popup Message

def proceed_time(task):
tkinter.messagebox.showinfo("Notification", "Its Now the Time for : " + task)

In the code above, which is for showing a popup message after the time seconds is finished off.
