### 1
Intento 1 es el mas simple, las caracteristas son: Circuito simple (no ackerman), colores RGB (no HSV), PD
Para el filtrado de la imagen era necesario tener en cuenta que hay colores que tambien tienen parte roja aunque no sean de color rojo, por ello es importante hacer el filtrado de ellos tambien.

Al usar un controlado P nada mas, en las curvas tambaleaba muchismo el coche, y tardaba mucho en estabilizarse en las rectas, por ello añadi un controlador D, el cual suavizaba mucho estos balanceos.

Para coger el centro de la linea, cuando empieza el progama, el coche debe de estar alineado con la linea y asi antes de empezar a seguir la linea, toma ese punto de refencia como centro.

Intenté realizar otros casos como que empiece y el coche no vea la linea, lo progamé y luego me di cuenta que no podia mover el coche porque en las granjas no va el gazebo :) asique esas comprobaciones se dejarán para mas adelate.

