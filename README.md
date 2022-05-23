# Permanente2a
Ruleta de casino
El programa consiste en que el juego es una ruleta en el cual la ruleta gira y te da 3 valores distintos si consigues que esos números coincidan con los que tu piensas has ganado.

#Datos personales
import random
def Bienv():
    print ('Hola usuario quieres jugar')
def main():
    Bienv() #Saludar al usuario
    print('Comenzando la ruleta')
    repite='S' #Si quieres iniciar a jugar
    acumula=0
    jugadas=0  #Lejos del ciclo, inicia variables
    while (repite.upper()=='S'): #Nuevo comando cualquier valor de repite
        empieza=raw_input ('Presiona cualquier tecla para comenzar la ruleta')
        x1= x2= x3= 0
        veces=random.randint(5,30) #Simula el giro de cada variable generando numeros
        jugadas=jugadas+1 #Acumulador de jugadas
        for i in range(veces):  #For para la var 1
            x1=random.randint(1,10)
            print(x1)
        for i in range(veces):  #For para la var 2
            x2=random.randint(1,10)
            print(x1, ' - ',x2)
        for i in range(veces):  #For para la var 3
            x3=random.randint(1,10)
            print(x1, ' - ', x2, ' - ', x3)
        print('Los resultados son:') #Que se note el tabulador
        print(x1, ' - ',x2,' - ', x3) #Aca ya salen los 3 valores 
        if (x1==x2 and x1==x3):  #Doble igual parentesis dos puntos
            print('\tGanador por Tercias, \tPuntos = 3')
            acumula=acumula+3 
        elif (x1==x2 or x1==x3):
            print('\tGanador por Pares, \tPuntos = 2')
            acumula=acumula+2
        else:
            print('\tNo hay Tercias ni pares, \tPuntos = 0') #Puede salir -1
        repite=raw_input ('\tDeseas jugar otra vez? ') #Notese el tabulador hacia atras
        print('\tReuniste en esta sesion %i puntos, hiciste %i jugadas' %(acumula, jugadas)) 
        #Fin del main
    main() #LLamada al main 
