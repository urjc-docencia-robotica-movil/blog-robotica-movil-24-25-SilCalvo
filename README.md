# blog-robotica-movil-24-25-SilCalvo
blog-robotica-movil-24-25-SilCalvo created by GitHub Classroom

Practica 1

# INTRODUCCION
La siguiente practica consiste en crear un programa para un robot aspiradora que solo consta de los siguientes sensores: Bumper, Laser (180º)

Para el control de la logica se usara una Maquina de EStados Finitos

# PRUEBAS
### ALGORITMO Nº1 SALA VACIA
Para crear el algoritmo de exploracion mi primer intento fue crear uno simple, que recoriese sin problemas una sala vacia mediante el siguiente patron: 
Avanzar hasta obstaculo, girar 90 grados, avanzar 2 segundos, girar 90 grados (cada vez girando hacia un lado distinto creando el siguiente patron de dibujo)


ADJUNTAR DIBUJO
**Problemas:** 

1. Como no sabemos la disposicion del robot no podemos calcular correctamente que gire 90 grados siempre. 
2. Solo funciona bien asegurado en salas vacias sin obstaculos

