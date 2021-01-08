from tkinter import *
from tkinter import ttk

t = Tk()

e = ttk.Entry(t)
e.pack()

def click():
    if e.get() == "x":
        print("Will Close !!")
        t.destroy()

    try:
        get = e.get()
        get = int(get)
        if get %2 == 0:
            print("You put even number !!")
        else:
            print("You put odd number !!")
    except ValueError :
        print("please enter a number !!")

b = ttk.Button(t,text="Start",command=click)
b.pack()

t.mainloop()
