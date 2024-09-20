
# P1 INTRODUCCION
La siguiente practica consiste en crear un programa para un robot aspiradora que solo consta de los siguientes sensores: Bumper, Laser (180º)

Para el control de la logica se usara una Maquina de EStados Finitos

# PRUEBAS
### ALGORITMO Nº1 SALA VACIA
Para crear el algoritmo de exploracion mi primer intento fue crear uno simple, que recoriese sin problemas una sala vacia mediante el siguiente patron: 
Avanzar hasta obstaculo, girar 90 grados, avanzar 2 segundos, girar 90 grados (cada vez girando hacia un lado distinto creando el siguiente ![patron de dibujo](Photo1.jpeg))


**Problemas:** 

1. Como no sabemos la disposicion del robot no podemos calcular correctamente que gire 90 grados siempre. 
2. Solo funciona bien asegurado en salas vacias sin obstaculos


### ALGORITMO Nº2 ESTADO RECUPERACION
Para solucionar el problema de los obstaculos añadimos un estado que consista en que cuando se choque con alguno, de marcha atras y gire ciertos grados, para intentar alejarse de este. Permitiendo cubrir gran parte del mapa.  ![Foto del mapa](Photo2.png)) 

**Problemas:** 
1. Cuando es un obstaculo funciona, pero no cuando es una esquina, ya que al girar y luego volver a avanzar se vuelve a dar, con la posibilidad de salir pero siendo poco óptimo.


### ALGORITMO Nº3 ESTADO SCAPE
Para solucionar el problema de las esquinas añadimos un estado llamado SCAPE el cual intenta salir de las esquinas usando el laser para medir las distancias a las paredes a saber por donde hay huecos. 



