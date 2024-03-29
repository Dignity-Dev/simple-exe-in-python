# simple-exe-in-python
In this guide, you’ll see how create an executable of a Python script using PyInstaller?
## Steps to Create an Executable using PyInstaller
### Step 1: Add Python to Windows Path
To start, you need to add Python to Windows path.

An easy way to add Python to the path is by downloading a recent version of Python, and then checking the box to ‘Add Python to PATH’ at the beginning of the installation.

Finish the installation, and you should be good to go.

### Step 2: Install the PyInstaller Package
Next, open the Windows Command Prompt, and then type the following command to install the PyInstaller package:
> `pip install pyinstaller`

### Step 3: Save your Python Script
Now save your Python script at your desired location.

For illustration purposes, let’s create a simple Python script that displays ‘Hello World!’ when clicking a button:
`
import tkinter as tk

root= tk.Tk()

canvas1 = tk.Canvas(root, width = 300, height = 300)
canvas1.pack()

def hello ():  
    label1 = tk.Label(root, text= 'Hello World!', fg='blue', font=('helvetica', 12, 'bold'))
    canvas1.create_window(150, 200, window=label1)
    
button1 = tk.Button(text='Click Me', command=hello, bg='brown',fg='white')
canvas1.create_window(150, 150, window=button1)

root.mainloop()
`

For demonstration purposes, let’s say that the Python script is stored in the following folder:

C:\Users\HTC\Desktop\Test

Where Python script is called ‘hello‘ and the file extension is '.py'

###Step 4: Create the Executable using PyInstaller
Now you’ll be able to create the executable of the Python script using PyInstaller.

Simply go to the Command Prompt, and then type:

cd followed by the location where your Python script is stored

Here is the command for our example:

> C:\Users\Ron>cd C:\Users\Ron\Desktop\Test

Press Enter (after you typed the location where the Python script is stored on your computer).

Then, refer to the following template to create the executable:

`pyinstaller --onefile pythonScriptName.py`
Since for our example, the pythonScriptName is 'hello' (and the file extension is .py), then the command to create the executable is:

`pyinstaller --onefile hello.py`

Press Enter for the last time.

###Step 5: Run the Executable
Your executable will be created at the location that you specified.

For our example, it will be under the same folder where the ‘hello’ script was originally stored:

C:\Users\HTC\Desktop\Test
You’ll notice that few additional files were created at that location.

To find the executable file, open the dist folder. You’ll then see the executable file:

>> hello

Double click on the file, and you should be able to launch your program (if you get an error message, you may need to install Visual C++ Redistributable).

In our case, once you click on the ‘hello’ executable, you’ll get a display with a single button.

And if you click on that button, you’ll see the following expression:

>> Hello World!