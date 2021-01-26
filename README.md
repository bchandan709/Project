



class project:
    def __init__(self):
        
        import tkinter as tk
        from tkinter import ttk

    def WindowFunc(self):
        an=[]
        ap=[]
        ab=[]
        cu=[]
        au=[]

        b=tk.Tk()
        b.title('BANK')
        b.geometry('1000x400')

        was4=ttk.Label(b,text='                           ',font=('arial',33,'bold'))
        was4.grid(row=0,column=1)

        w=ttk.Label(b,text='PLEASE ENTER BANK DATABASE',font=('arial',24,'bold'))
        w.grid(row=1,column=1)
        was=ttk.Label(b,text='                               ',font=('arial',18,'bold'))
        was.grid(row=2,column=0)


        e=ttk.Label(b,text='ENTER ACCOUNT NUMBER :-',font=('arial',12))
        e.grid(row=3,column=1,sticky=tk.W)
        r=ttk.Entry(b,width=40)
        r.grid(row=3,column=1,sticky=tk.E)


        t=ttk.Label(b,text='ENTER ACCOUNT PASSWORD :-',font=('arial',12))
        t.grid(row=4,column=1,sticky=tk.W)
        y=ttk.Entry(b,width=40)
        y.grid(row=4,column=1,sticky=tk.E)

        qw=ttk.Label(b,text='ENTER ACCOUNT BALANCE :-',font=('arial',12))
        qw.grid(row=5,column=1,sticky=tk.W)
        qe=ttk.Entry(b,width=40)
        qe.grid(row=5,column=1,sticky=tk.E)

        def i():
            o=r.get()
            p=y.get()
            m=qe.get()

            an.append(o)
            ap.append(p)
            ab.append(int(m))

            r.delete(0,tk.END)
            y.delete(0,tk.END)
            qe.delete(0,tk.END)


        croc=ttk.Label(b,text='                ',font=('arial',20,'bold'))
        croc.grid(row=6,column=1)    
        u=ttk.Button(b,text='SUBMIT',command=i)
        u.grid(row=7,column=1,sticky=tk.W)
        def s():

            b.destroy()

            atm=tk.Tk()
            atm.title('ATM')
            atm.geometry('1000x400')

            was2=ttk.Label(atm,text='                           ',font=('arial',18,'bold'))
            was2.grid(row=0,column=0)

            f=ttk.Label(atm,text='-------------WELCOME TO ATM------------',font=('arial',24,'bold'))
            f.grid(row=1,column=1)


            was1=ttk.Label(atm,text='       ',font=('arial',22,'bold'))
            was1.grid(row=2,column=0)

            was3=ttk.Label(atm,text='       ',font=('arial',22,'bold'))
            was3.grid(row=3,column=1)


            g=ttk.Label(atm,text='ENTER ACCOUNT NUMBER :-   ',font=('arial',12))
            g.grid(row=4,column=1,sticky=tk.W)
            hh=ttk.Entry(atm,width=40)
            hh.grid(row=4,column=1,sticky=tk.E)


            j=ttk.Label(atm,text='ENTER ACCOUNT PASSWORD :-  ',font=('arial',12))
            j.grid(row=5,column=1,sticky=tk.W)
            kk=ttk.Entry(atm,width=40)
            kk.grid(row=5,column=1,sticky=tk.E)


            def c():
                    ok1=hh.get()
                    ok2=kk.get()
                    if ok1 in an and ok2 in ap:

                        ok3=an.index(ok1)
                        cu.append(ok3)
                        if ok1 in an and ok2==ap[ok3]:
                            atm.destroy()


                            atm2=tk.Tk()

                            atm2.geometry('1000x400')

                            was5=ttk.Label(atm2,text='           ',font=('arial',45,'bold'))
                            was5.grid(row=0,column=1)

                            fx=ttk.Label(atm2,text='-------------------ATM-----------------',font=('arial',24,'bold'))
                            fx.grid(row=1,column=1)

                            was6=ttk.Label(atm2,text='                               ',font=('arial',18,'bold'))
                            was6.grid(row=2,column=0)

                            fbb=tk.IntVar()
                            e=ttk.Radiobutton(atm2,text='WITHDRAWAL',value=1,variable=fbb)
                            e.grid(row=3,column=1,sticky=tk.W)
                            g=ttk.Radiobutton(atm2,text='DEPOSITE',value=2,variable=fbb)
                            g.grid(row=4,column=1,sticky=tk.W)
                            h=ttk.Radiobutton(atm2,text='CHECK BALANCE',value=3,variable=fbb)
                            h.grid(row=5,column=1,sticky=tk.W)
                            def ll():


                                    if fbb.get()==1:

                                        atm2.destroy()
                                        wdb=tk.Tk()
                                        wdb.title('MONEY WITHDRAWAL')
                                        wdb.geometry('1000x400')

                                        was10=ttk.Label(wdb,text='           ',font=('arial',45,'bold'))
                                        was10.pack()


                                        wdb3=ttk.Label(wdb,text='-------------------ATM-----------------',font=('arial',24,'bold'))
                                        wdb3.pack()

                                        was11=ttk.Label(wdb,text='           ',font=('arial',45,'bold'))
                                        was11.pack()


                                        wdb1=ttk.Label(wdb,text='ENTER WITHDRAWAL AMOUNT',font='Times')
                                        wdb1.pack()

                                        wdb2=ttk.Entry(wdb,width=30)
                                        wdb2.pack()


                                        def press1():


                                            au.append(int(wdb2.get()))
                                            aff=cu[0]



                                            if ab[aff]>=au[0]:
                                                acc=ab[aff]-au[0]

                                                ab.pop(aff)
                                                ab.insert(aff,acc)
                                                wdb.destroy()
                                                disp=tk.Tk()

                                                disp.geometry('1000x400')

                                                was20=ttk.Label(disp,text='           ',font=('arial',45,'bold'))
                                                was20.pack()

                                                disp1=ttk.Label(disp,text='-------------------ATM-----------------',font=('arial',24,'bold'))
                                                disp1.pack()

                                                was21=ttk.Label(disp,text='           ',font=('arial',20,'bold'))
                                                was21.pack()

                                                disp2=ttk.Label(disp,text='YOUR BALANCE LEFT IS  ',font='Times')
                                                disp2.pack()

                                                was22=ttk.Label(disp,text='           ',font=('arial',20,'bold'))
                                                was22.pack()

                                                disp3=ttk.Label(disp,text=f'{acc} Rupees',font='Times')
                                                disp3.pack()


                                                def exit1():
                                                    disp.destroy()

                                                was23=ttk.Label(disp,text='           ',font=('arial',20,'bold'))
                                                was23.pack()

                                                disp4=ttk.Button(disp,text='Exit',command=exit1)
                                                disp4.pack()

                                                disp.mainloop()

                                            else:
                                                ror=tk.Tk()
                                                ror.title('ERROR')
                                                ror.geometry('1000x400')

                                                was8=ttk.Label(ror,text='           ',font=('arial',45,'bold'))
                                                was8.pack()


                                                was9=ttk.Label(ror,text='                               ',font=('arial',18,'bold'))
                                                was9.pack()


                                                ttk.Label(ror,text='INSUFFICIENT BALANCE',font=('arial',15)).pack()

                                                def final():
                                                    ror.destroy()
                                                    wdb.destroy()
                                                was9=ttk.Label(ror,text='                               ',font=('arial',18,'bold'))
                                                was9.pack()

                                                ttk.Button(ror,text='OK',command=final).pack()    
                                                ror.mainloop()

                                        was12=ttk.Label(wdb,text='           ',font=('arial',20,'bold'))
                                        was12.pack()
                                        wdb4=ttk.Button(wdb,text='Press Here',command=press1)
                                        wdb4.pack()

                                        wdb.mainloop()
                                    if fbb.get()==2:



                                        atm2.destroy()
                                        depo=tk.Tk()

                                        depo.title('MONEY DEPOSITE')
                                        depo.geometry('1000x400')

                                        was13=ttk.Label(depo,text='           ',font=('arial',45,'bold'))
                                        was13.pack()

                                        depo1=ttk.Label(depo,text='-------------------ATM-----------------',font=('arial',24,'bold'))
                                        depo1.pack()

                                        was14=ttk.Label(depo,text='           ',font=('arial',20,'bold'))
                                        was14.pack()

                                        depo2=ttk.Label(depo,text='ENTER AMOUNT TO BE DEPOSITED :-',font='Times')
                                        depo2.pack()

                                        depo3=ttk.Entry(depo,width=30)
                                        depo3.pack()

                                        def press2():

                                            au.append(int(depo3.get()))
                                            aff=cu[0]
                                            acc=ab[aff]+au[0]

                                            ab.pop(aff)
                                            ab.insert(aff,acc)
                                            depo.destroy()
                                            hope=tk.Tk()
                                            hope.geometry('1000x400')

                                            was29=ttk.Label(hope,text='           ',font=('arial',45,'bold'))
                                            was29.pack()

                                            hope1=ttk.Label(hope,text='-------------------ATM-----------------',font=('arial',24,'bold'))
                                            hope1.pack()

                                            was24=ttk.Label(hope,text='           ',font=('arial',20,'bold'))
                                            was24.pack()


                                            hope2=ttk.Label(hope,text='YOUR BALANCE LEFT IS  ',font='Times')
                                            hope2.pack()

                                            was25=ttk.Label(hope,text='           ',font=('arial',20,'bold'))
                                            was25.pack()

                                            hope3=ttk.Label(hope,text=f'{acc} Rupees',font='Times')
                                            hope3.pack()

                                            def exit2():
                                                hope.destroy()

                                            was26=ttk.Label(hope,text='           ',font=('arial',20,'bold'))
                                            was26.pack()
                                            hope4=ttk.Button(hope,text='Exit',command=exit2)
                                            hope4.pack()

                                            hope.mainloop()

                                        was23=ttk.Label(depo,text='           ',font=('arial',20,'bold'))
                                        was23.pack()    
                                        depo4=ttk.Button(depo,text='Press Here',command=press2)
                                        depo4.pack()
                                        depo.mainloop()

                                    if fbb.get()==3:

                                        aff=cu[0]
                                        acc=ab[aff]

                                        atm2.destroy()

                                        check=tk.Tk()
                                        check.geometry('1000x400')

                                        check.title('CHECK BALANCE')

                                        was16=ttk.Label(check,text='           ',font=('arial',45,'bold'))
                                        was16.pack()

                                        check1=ttk.Label(check,text='-------------------ATM-----------------',font=('arial',24,'bold'))
                                        check1.pack()

                                        was17=ttk.Label(check,text='           ',font=('arial',20,'bold'))
                                        was17.pack()

                                        check2=ttk.Label(check,text='YOUR BALANCE IS  ',font='Times')
                                        check2.pack()

                                        was18=ttk.Label(check,text='           ',font=('arial',20,'bold'))
                                        was18.pack()

                                        check3=ttk.Label(check,text=f'{acc} Rupees',font='Times')
                                        check3.pack()

                                        def exit3():
                                            check.destroy()

                                        was19=ttk.Label(check,text='           ',font=('arial',20,'bold'))
                                        was19.pack()
                                        check4=ttk.Button(check,text='Exit',command=exit3)
                                        check4.pack()

                                        check.mainloop()

                            was7=ttk.Label(atm2,text='                               ',font=('arial',18,'bold'))
                            was7.grid(row=6,column=1)
                            ss=ttk.Button(atm2,text='Submit',command=ll)
                            ss.grid(row=7,column=1,sticky=tk.W)

                            atm2.mainloop()
                    else:
                        error=tk.Tk()
                        err1=ttk.Label(error,text='PLEASE CHECK YOUR ACCOUNT NUMBER OR PASSWORD',font='Times')
                        err1.grid(row=0,column=0)
                        def erbox():
                            error.destroy()
                        err2=ttk.Button(error,text='OK',command=erbox)
                        err2.grid(row=1,column=0)
                        error.mainloop()

            croc1=ttk.Label(atm,text='       ',font=('arial',23,'bold'))
            croc1.grid(row=6,column=1)             
            x=ttk.Button(atm,text='SUBMIT',command=c)
            x.grid(row=7,column=1,sticky=tk.E)


            atm.mainloop()
        a=ttk.Button(b,text='EXIT',command=s)
        a.grid(row=7,column=1,sticky=tk.E)


        b.mainloop()
obj=project()
obj.WindowFunc()
