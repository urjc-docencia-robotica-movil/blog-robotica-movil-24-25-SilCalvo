# blog-robotica-movil-24-25-SilCalvo
blog-robotica-movil-24-25-SilCalvo created by GitHub Classroom

Practica 1
primer aproach - HAcer que el robot recorra los espacios mediante el siguiente patron: Avanzar hasta obstaculo, girar 90 grados, avanzar 2 segundos, girar 90 grados, de esta forma en una sala vacia recorreria toda la sala

ADJUNTAR DIBUJO
Problemas: Como no sabemos la disposicion del robot no podemos calcular correctamente que gire 90 grados siempre.
Intento 1 de ese codigo

'''python


import GUI
import HAL
import math
from enum import Enum
import time

class States(Enum):
    INIT = 0
    FORWARD = 1
    RIGTH = 2
    TURN = 3
  
#Turn 90º aprox, move forward and turn again to complete a 180º turn  
def turn(direction, time_turn):
    turn_complete = False
    actual_time = time.time()
    vel = 0.5
    
    if(actual_time - time_turn < 3):
      HAL.setW(vel * direction)
      HAL.setV(0.0)
      
    elif(actual_time - time_turn < 5):
      HAL.setW(0.0)
      HAL.setV(vel)
      
    elif (actual_time - time_turn < 8):
      HAL.setW(vel * direction)
      HAL.setV(0.0)
    else:
      turn_complete = True
      
    return turn_complete
  
  
state = States.INIT
bumper = False
turn_complete=False
direction = 1

while True:
  
    #Conditions to change STATES 
    if(state == States.INIT):
      state=States.FORWARD
      
    elif(state== States.FORWARD and HAL.getBumperData().state == 1): #Move forward untill crush
      state = States.TURN
      time_turn = time.time()
      print(state)
      
    elif(state == States.TURN and turn_complete):
      state = States.FORWARD
      direction = direction * -1 #Change the turn direction 
      turn_complete = False
      print(state) 
    
    #Actions taken in each STATE
    if(state == States.FORWARD):
      HAL.setV(0.5)
      HAL.setW(0.0)
      
    elif(state == States.TURN):
      turn_complete = turn(direction,time_turn)
     
'''

