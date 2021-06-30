# Shravani Aravat
from tkinter import*

bs= Tk()
bs.title('calculator')
bs.geometry('450x400+200+200')
bs.config(bg="grey25")

operator=""
input=StringVar()

def numinp(numbers):
    global operator
    operator=operator+str(numbers)
    input.set(operator)

def btnclr():
    global operator
    operator=""
    input.set("")

def btneql():
    global operator
    sumop =str(eval(operator))
    input.set(sumop)
    operator=""

frame0=Frame(bs,bg='wheat1',relief=GROOVE,borderwidth=10)
frame0.place(x=10,y=30,width=430,height=100)
entry=Entry(frame0,text=input,font=('arial',27,'bold'),bd=6,justify="right",bg='wheat1').grid(columnspan=10)

frame1 =Frame(bs,bg='grey53',relief=GROOVE)
frame1.place(x=10,y=150,width=420,height=240)

bt1=Button(frame1,text='9',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(9)).grid(row=1,column=0)

bt2=Button(frame1,text='8',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(8)).grid(row=1,column=1)

bt3=Button(frame1,text='7',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(7)).grid(row=1,column=2)

bt4=Button(frame1,text='6',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(6)).grid(row=2,column=0)

bt5=Button(frame1,text='5',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(5)).grid(row=2,column=1)

bt6=Button(frame1,text='4',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(4)).grid(row=2,column=2)

bt7=Button(frame1,text='3',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(3)).grid(row=3,column=0)

bt8=Button(frame1,text='2',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(2)).grid(row=3,column=1)

bt9=Button(frame1,text='1',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(1)).grid(row=3,column=2)

bt10=Button(frame1,text='CLEAR',height=3,width=13,bg='wheat1',borderwidth=4,command=btnclr).grid(row=4,column=0)

bt11=Button(frame1,text='0',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp(0)).grid(row=4,column=1)

bt12=Button(frame1,text='=',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :btneql()).grid(row=4,column=2)

btn13=Button(frame1,text='+',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp('+')).grid(row=1,column=3)

btn14=Button(frame1,text='-',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp('-')).grid(row=2,column=3)

btn15=Button(frame1,text='*',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp('*')).grid(row=3,column=3)

btn16=Button(frame1,text='/',height=3,width=13,bg='wheat1',borderwidth=4,command=lambda :numinp('/')).grid(row=4,column=3)

bs.mainloop()
