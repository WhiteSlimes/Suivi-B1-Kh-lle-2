```
from tkinter import *
#Définition des positions initiales des barres
refreshrate=50
flag = 0
v,dx,dy=0,-10,15
####Initialisation des raquettes
PosXG=30
PosYG=140
PosXD=450
PosYD=140
x=42
y=152
dx=10
dy=10
def move():
    global x,y,dx,dy,flag,PosXD,PosYD,PosXG,PosYG,balle
    xp, yp = x+dx, y+dy
    print (xp,yp)
    if xp >= PosXD + 5 and yp < PosYD+50 and yp > PosYD-10:
        dx = -dx
    if xp <= PosXG - 5 and yp < PosYG+50 and yp > PosYG-10:
        dx = -dx
    if yp> Hauteur -15 or yp < 15:
        dy = -dy
    x, y = x+dx, y+dy
    Canevas.coords(balle,x,y,x+16,y+16)
  
    if flag > 0:
        Mafenetre.after(50,move)
#####################################    FONCTION START    #################################
  
def start():
    global flag
    flag=flag+1
    if flag==1:
        move()
    "Start"
 
######################################  FONCTION CLAVIER   #################################
 
     
def Clavier(event):
    #Gestion de l'événement Appui sur une touche du clavier
    global PosXD, PosYD,PosXG,PosYG
    touche=event.keysym
    print("Touche :", touche)
     
     
 
    #déplacement vers le haut
    if touche == 'Up':
        PosYD=PosYD-20
    #déplacement vers le bas
    if touche == 'Down':
        PosYD=PosYD+20
         
    Canevas.coords(raquettedroite,PosXD-10,PosYD-10,PosXD+10,PosYD+50)
 
    if touche == 'a':
        PosYG=PosYG-20
    #déplacement vers le bas
    if touche == 'q':
        PosYG=PosYG+20
    Canevas.coords(raquettegauche,PosXG-10,PosYG-10,PosXG+10,PosYG+50)
     
     
     
Mafenetre = Tk() 
Mafenetre.title('PONG') #Définition d'un titre pour la fenetre
largeur = 480 #Définition de la variable largeur à 480 pxl
Hauteur = 320 #Définition de la variable Hauter à 320 pxl
#Indique les normes du Canevas
Canevas = Canvas(Mafenetre, width = largeur, height = Hauteur, bg='#333333')
Canevas.pack()
#Définition du boutton "Start"
Button(Mafenetre, text='Start',command=start).pack(side=LEFT, padx=10)
#Définition du boutton "Quitter"
Button(Mafenetre, text='Quitter',command=Mafenetre.destroy).pack(side=LEFT,padx=5,pady=5)
raquettedroite = Canevas.create_rectangle(PosXD-10,PosYD-10,PosXD+10,PosYD+50,width=2,outline='white',fill='#01B0F0')
raquettegauche = Canevas.create_rectangle(PosXG-10,PosYG-10,PosXG+10,PosYG+50,width=2,outline='white',fill='#01B0F0')
balle = Canevas.create_oval(x,y,x+16,y+16,width=1,outline='white',fill='#FF358B')
 
 
Canevas.focus_set()
 
Canevas.bind('<Key>', Clavier) # Flèche haut
#Créer une boucle
Mafenetre.mainloop()
```
