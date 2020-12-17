# **Unit Convertor**  
### A series of codes for converting units of measurements.
## **Motivation**
##### 
In the UK both imperial and metric measurements are still used, often measurments are interchanged to whatever is suitable at the time. 
For example, distance for car journeys will be in imperial miles, whereas the length of a swimming pool is in metres. The efficiency of a vehicle's engine is deteremined by mpg (miles per gallon) for engine sizes based on cc (cubic centimetres).
#### 
Therefore the need for a unit converter may find many uses.
##### 
This project aims at developing a user friendly application for converting units of measurement.
##### 
This project provides a learning platform for developing my coding skills. Notably the use of the tkinter library for input via a Graphic User Interface, GUI. 
## **Build status:** Under Development. 
#### 
The first convertor is that of length, metric to imperial (UK) and is functioning today (17/12/2020)
##### 
Currently the GUI accepts input units in metre format and returns their equivalent (UK) imperial lengths by selecting the relevent button.
Possible unit conversion is from metre to inch, feet, yards and miles.

[![length.jpg](https://i.postimg.cc/tRLX0fqK/length.jpg)](https://postimg.cc/Hj9GX67z)
## **Tech**
#####
Coded with Python in Jupyter notebook
Library List:
pip install python-math
tkinter should be included in Python3 onwards, if not follow this link
(https://docs.python.org/3/library/tkinter.html#module-tkinter)

Libaries initiated with code as:
```
import math as m
import tkinter as tk
```

## **Code**
```
import math as m
import tkinter as tk
root =tk.Tk()

canvas1 =tk.Canvas(root, width = 300, height=200)
canvas1.pack()

label1 = tk.Label(root,text='Metres:')
label1.config(font=('helvetica',14))
canvas1.create_window(50, 25, window=label1)
entry1= tk.Entry(root)
canvas1.create_window(150, 25 , window=entry1)

def getinches():
    x1 = entry1.get()
    label3=tk.Label(root,text=round(float(x1)*39.37,2),font=('helvetica',12,'bold'))
    canvas1.create_window(150,80, window=label3)

def getfeet():
    x2 = entry1.get()
    label4=tk.Label(root,text=round(float(x2)/0.3,2),font=('helvetica',12,'bold'))
    canvas1.create_window(150,110, window=label4)

def getyards():
    x3 = entry1.get()
    label5=tk.Label(root,text=round(float(x3)/0.9,2),font=('helvetica',12,'bold'))
    canvas1.create_window(150,140,window=label5)

def getmiles():
    x4 = entry1.get()
    label6=tk.Label(root,text=round(float(x4)/1600,5),font=('helvetica',12,'bold'))
    canvas1.create_window(150,170,window=label6)      

button1 = tk.Button(text='Inches', command=getinches)
canvas1.create_window(70, 80, window=button1)
button2 = tk.Button(text='Feet',command=getfeet)
canvas1.create_window(70,110,window=button2)

button3 = tk.Button(text='Yards', command=getyards)
canvas1.create_window(70,140,window=button3)
button4 = tk.Button(text='Miles', command=getmiles)
canvas1.create_window(70,170,window=button4)

root.mainloop()
```
## **Instructions**
Paste the code into a Jupyter notebook window.
Press SHIFT ENTER.
Wait for the GUI to generate. 
Input length in metres, click on respective box to convert to UK imperial unit.
