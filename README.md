# Tic-Tac-Toe
Tic-Tac-toe Game Using Python

from tkinter import *

import tkinter.messagebox

app=Tk()

#Giving Title

app.title("Tic-Tac-Toe")

#Giving Geometry

app.geometry('400x400')

#Setting Default Value this Helps to use the X in game

click = 9

def check(button):
    
    global click
    
    if button["text"] == " " and click == 9:
        button["text"] = "X"
        click = 8 #This will chnage The Value of click and now it will use O in game

    elif button["text"] == " " and click == 8:
        button["text"] = "O"
        click = 9 #This will change it to X in the game

#Giving Condition When X wins
    
    elif(q["text"] == "X" and w["text"] == "X" and e["text"] == "X" or
         f["text"] == "X" and r["text"] == "X" and t["text"] == "X" or
         y["text"] == "X" and u["text"] == "X" and i["text"] == "X" or
         q["text"] == "X" and r["text"] == "X" and i["text"] == "X" or
         e["text"] == "X" and r["text"] == "X" and y["text"] == "X" or
         q["text"] == "X" and f["text"] == "X" and y["text"] == "X" or
         w["text"] == "X" and r["text"] == "X" and u["text"] == "X" or
         e["text"] == "X" and t["text"] == "X" and i["text"] == "X"):
        tkinter.messagebox.showinfo("Winner X, You Have just Won The Game")

#Giving Condition When O wins
    
    elif(q["text"] == "0" and w["text"] == "0" and e["text"] == "0" or
         f["text"] == "0" and r["text"] == "0" and t["text"] == "0" or
         y["text"] == "0" and u["text"] == "0" and i["text"] == "0" or
         q["text"] == "0" and r["text"] == "0" and i["text"] == "0" or
         e["text"] == "0" and r["text"] == "0" and y["text"] == "0" or
         q["text"] == "0" and f["text"] == "0" and y["text"] == "0" or
         w["text"] == "0" and r["text"] == "0" and u["text"] == "0" or
         e["text"] == "0" and t["text"] == "0" and i["text"] == "0"):
        tkinter.messagebox.showinfo("Winner 0, You Have Just Won The Game")

button=StringVar()

#Creating Buttons

q=Button(app,text=" ",command=lambda:check(q),height=5,width=8)

q.grid(row=1,column=1)

w=Button(app,text=" ",command=lambda:check(w),height=5,width=8)

w.grid(row=1,column=2)

e=Button(app,text=" ",command=lambda:check(e),height=5,width=8)

e.grid(row=1,column=3)

f=Button(app,text=" ",command=lambda:check(f),height=5,width=8)

f.grid(row=2,column=1)

r=Button(app,text=" ",command=lambda:check(r),height=5,width=8)

r.grid(row=2,column=2)

t=Button(app,text=" ",command=lambda:check(t),height=5,width=8)

t.grid(row=2,column=3)

y=Button(app,text=" ",command=lambda:check(y),height=5,width=8)

y.grid(row=3,column=1)

u=Button(app,text=" ",command=lambda:check(u),height=5,width=8)

u.grid(row=3,column=2)

i=Button(app,text=" ",command=lambda:check(i),height=5,width=8)

i.grid(row=3,column=3)

app.mainloop()
