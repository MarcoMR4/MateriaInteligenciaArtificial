#   Ejercicio 1: Juego de gato en 3D  
## Se necesita una IA capaz de ganar un juego de gato en 3 dimensiones 

### Medida de persepción: 
    - Se tenen 3 niveles en 2d del juego gato.
    - cada nivel tiene 9 espacios para rellenar.
    - se forma un total de 27 espacios con posibles combinaciones. 
    - Se tienen líneas horizontales que se forman en cada nivel. 
    - Se tienen líneas verticales que se forman conectando los niveles entre sí. 
    - Se tienen diagonales horizontales y verticales. 


### Secuencia de rendimiento: 
    - Buscar una esquina. 
    - Buscar esquina en otro extremo para poder formar una diagonal horizontal. 
    - Buscar esquina en otro extremo para formar una diagonal vertical  
    - si el oponente no ocupa el centro horizontal o vertical, es decir,
    cualquiera de los dos centros (horizontal o vertical), el juego se gana. 




