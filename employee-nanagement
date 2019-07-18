from tkinter import *

employee = {1: {'name': 'John', 'age': '27','salary': '60000', 'gender': 'Male'},
          2: {'name': 'Marie', 'age': '22','salary': '80000',  'gender': 'Female'}}

x=2	  
def insertinfo():
     global x
     x=x+1
     employee[x]={}
     employee[x]['name']=name.get()
     employee[x]['age']=age.get()
     employee[x]['salary']=salary.get()
	 
    
     
     if var_gender.get()==1:
         employee[x]['gender']='Male'
     if var_gender.get()==2: 
         employee[x]['gender']='Female'	 
     
   
     showinfo()
 
	
def deleteinfo():
    y=employeeid.get()
    del employee[y]
    showinfo()
	

def editinfo():
    
    y=employeeid.get()
    employee[y]['name']=name.get()
    employee[y]['age']=age.get()
    employee[y]['salary']=salary.get()
    showinfo()
	 

def clear():
    list.delete(0,"end")
			  
		  
def showinfo():
    list.delete(0,"end")
    entry_name.delete(0,"end")
    entry_age.delete(0,"end")
    entry_salary.delete(0,"end")    
    entry_id.delete(0,"end")	
    for i,j in employee.items():
       msg=("                   "+str(i)+"                                              "+employee[i]['name']+"                                                                     "+employee[i]['age']+"                                                       "+employee[i]['salary']+"                                        "+employee[i]['gender'] )
       list.insert("end",msg)
	
root= Tk()

lbl1= Label(root,text="")
lbl1.grid(row=0,column=0)

#name
lbl_name= Label(root,text="Name")
lbl_name.grid(row=1,column=0)
name=StringVar()
entry_name= Entry(root,textvariable=name)
entry_name.grid(row=1,column=1)


lbl2= Label(root,text="")
lbl2.grid(row=2,column=0)

#Age
lbl_age= Label(root,text="Age")
lbl_age.grid(row=3,column=0)
age=StringVar()
entry_age= Entry(root,textvariable=age)
entry_age.grid(row=3,column=1)

lbl3= Label(root,text="")
lbl3.grid(row=4,column=0)

#Salary
lbl_salary=Label(root,text="Salary")
lbl_salary.grid(row=5,column=0)
salary=StringVar()
entry_salary= Entry(root,textvariable=salary)
entry_salary.grid(row=5,column=1)

lbl4= Label(root,text="")
lbl4.grid(row=6,column=0)

lbl_gender=Label(root,text="Gender")
lbl_gender.grid(row=7,column=0)
var_gender=IntVar()
CheckMale= Radiobutton(root,text="Male",height=5,width = 20,value=1,variable=var_gender)
CheckMale.grid(row=7,column=1)

CheckFemale= Radiobutton(root,text="Female",height=5,width = 20,value=2,variable=var_gender)
CheckFemale.grid(row=7,column=2)


Btn_insert=Button(root,text="Insert",command=insertinfo)
Btn_insert.grid(row=9,column=1)

Btn_show=Button(root,text="Show All",command=showinfo)
Btn_show.grid(row=9,column=3)


Btn_delete=Button(root,text="Delete",command=deleteinfo)
Btn_delete.grid(row=9,column=2)

lbl_edit= Label(root,text="To edit and delete Write employee id")
lbl_edit.grid(row=9,column=4)

employeeid=IntVar()
entry_id= Entry(root,textvariable=employeeid)
entry_id.grid(row=10,column=4)

lbl5= Label(root,text="")
lbl5.grid(row=10,column=0)

Btn_edit=Button(root,text="Edit",command=editinfo)
Btn_edit.grid(row=11,column=1)

Btn_clear=Button(root,text="Clear",command=clear)
Btn_clear.grid(row=11,column=2)

lbl5= Label(root,text="")
lbl5.grid(row=12,column=0)

lbl_id2= Label(root,text="    Employee Id")
lbl_id2.grid(row=13,column=0)
lbl_name2= Label(root,text="Name")
lbl_name2.grid(row=13,column=1)
lbl_age2= Label(root,text="Age")
lbl_age2.grid(row=13,column=2)
lbl_salary2= Label(root,text="Salary")
lbl_salary2.grid(row=13,column=3)
lbl_gender2= Label(root,text="Gender")
lbl_gender2.grid(row=13,column=4)


list =Listbox(root,height=10,width=150)
list.grid(row=14,column=0,columnspan=5)


root.mainloop()
