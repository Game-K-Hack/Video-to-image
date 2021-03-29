[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg?logo=paypal&style=flat-square)](https://paypal.me/pools/c/8y8KpBnTjJ)

# Video-to-image

CODE

    from tkinter import *
    from tkinter import filedialog
    from tkinter.messagebox import *

    fen = Tk()
    fen.title("Changeur d'extention")
    filename_intput = StringVar()
    chemin = ""

    def Input_P():
        filename_intput.set(filedialog.askopenfilename())

    def prog():
        if entree1.get() != "":
            if entree2.get() != "":
                fichier = open(str(entree1.get()),"r")
                text = fichier.read()
                print(text)
                fichier.close()
                liste = list(str(entree1.get()).split("."))
                nb = len(liste)
                liste.remove(str(liste[int(nb-1)]))
                chemin = str(liste)
                chemin = chemin.replace("['","")
                chemin = chemin.replace("']","")
                fichier = open(chemin + str(entree2.get()),"a")
                fichier.write(str(text))
                fichier.close()
            else:
                showerror('ERREUR',"Aucune extention").lift()
        else:
            showerror('ERREUR',"Aucun fichier").lift()

    canvas1 = Canvas(fen, width=10, height=10)
    canvas1.grid(row=0, column=1)
    canvas2 = Canvas(fen, width=20, height=10)
    canvas2.grid(row=0, column=5)
    label1 = Label(fen, text = '        Fichier       ')
    label1.grid(row=1, column=1)
    label3 = Label(fen, text = '        Exention       ')
    label3.grid(row=2, column=1)
    entree1 = Entry(fen, textvariable=filename_intput, width=50, bg ='bisque')
    entree1.grid(row=1, column=2)
    entree2 = Entry(fen, width=50, bg ='bisque')
    entree2.grid(row=2, column=2)
    label2 = Label(fen, text = '        ')
    label2.grid(row=1, column=3)
    parcourir1 = Button(fen, text='Parcourir', borderwidth=1, command=Input_P)
    parcourir1.grid(row=1, column=4)
    canvas1 = Canvas(fen, width=10, height=10)
    canvas1.grid(row=3, column=1)
    Start = Button(fen, text='    CONVERTION    ', borderwidth=1, command=prog)
    Start.grid(row=4, column=2)
    canvas1 = Canvas(fen, width=10, height=10)
    canvas1.grid(row=5, column=1)

    fen.mainloop()
    from tkinter import *
    from tkinter import filedialog
    from tkinter.messagebox import *

    fen = Tk()
    fen.title("Changeur d'extention")
    filename_intput = StringVar()
    chemin = ""

    def Input_P():
        filename_intput.set(filedialog.askopenfilename())

    def prog():
        if entree1.get() != "":
            if entree2.get() != "":
                fichier = open(str(entree1.get()),"r")
                text = fichier.read()
                print(text)
                fichier.close()
                liste = list(str(entree1.get()).split("."))
                nb = len(liste)
                liste.remove(str(liste[int(nb-1)]))
                chemin = str(liste)
                chemin = chemin.replace("['","")
                chemin = chemin.replace("']","")
                fichier = open(chemin + str(entree2.get()),"a")
                fichier.write(str(text))
                fichier.close()
            else:
                showerror('ERREUR',"Aucune extention").lift()
        else:
            showerror('ERREUR',"Aucun fichier").lift()

    canvas1 = Canvas(fen, width=10, height=10)
    canvas1.grid(row=0, column=1)
    canvas2 = Canvas(fen, width=20, height=10)
    canvas2.grid(row=0, column=5)
    label1 = Label(fen, text = '        Fichier       ')
    label1.grid(row=1, column=1)
    label3 = Label(fen, text = '        Exention       ')
    label3.grid(row=2, column=1)
    entree1 = Entry(fen, textvariable=filename_intput, width=50, bg ='bisque')
    entree1.grid(row=1, column=2)
    entree2 = Entry(fen, width=50, bg ='bisque')
    entree2.grid(row=2, column=2)
    label2 = Label(fen, text = '        ')
    label2.grid(row=1, column=3)
    parcourir1 = Button(fen, text='Parcourir', borderwidth=1, command=Input_P)
    parcourir1.grid(row=1, column=4)
    canvas1 = Canvas(fen, width=10, height=10)
    canvas1.grid(row=3, column=1)
    Start = Button(fen, text='    CONVERTION    ', borderwidth=1, command=prog)
    Start.grid(row=4, column=2)
    canvas1 = Canvas(fen, width=10, height=10)
    canvas1.grid(row=5, column=1)

    fen.mainloop()
