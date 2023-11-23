🔙 [Volver](README.MD)

## Practica 4 Introducción a la inteligencia artificial Introspección: Contar islas en una matriz.

### Introducción. 
El siguiente ensayo es el planteamiento de cómo resolver un problema, que consiste en contar el número de islas dentro de una matriz de elementos rectangulares o cuadrados, según la perspectiva que se note. El objetivo del mismo es poner en práctica la autopercepción de mi mente para encontrar la metodología para resolver este problema.
Es importante conocer la forma en que nuestra mente trabaja y como asociando diferentes conocimientos previos, podemos encontrar la forma más óptima de encontrar una solución para poder implementar las diferentes técnicas de la inteligencia artificial.

### Desarrollo 
#### Percepción y análisis del problema. 
Lo primero que observamos en este problema es una matriz de 14 x 22 cuadros, que más bien tienen formas rectangulares, dentro del cual la mayoría de los cuadros son blancos y se tienen 6 islas conformadas por cuadros grises oscuro, ese es el color que marca la diferencia y del cual se tienen que contar los cuadros para las islas. 
Al pedirse resolver el problema de contar los cuadros de diferente color, que serían los que contiene cada isla se toman en cuenta dos métodos, uno iterativo y uno recursivo en forma de algoritmos. Tomando esto en cuenta podríamos asignar un valor numérico a los elementos de color gris oscuro como un 1 y los de color blanco como un cero. 

#### Método iterativo. 
En la parte iterativa se utilizaría una función que pueda recorrer la matriz en el sentido de las filas y en cada fila una columna, se puede pasar un color como referencia numérica, en el caso de querer contar los elementos de color gris oscuro solo se haría referencia al número 1. Al recorrer cada posición, si el cuadro es blanco la referencia sería un 0, por lo que un contador auxiliar que utilicemos podría regresar un valor de 0, referenciando que no encontramos nada. 
Teniendo como referencia el tamaño de la matriz, esto me hace asociarlo con un ciclo iterativo como por ejemplo el ciclo for, en el que podríamos recorrer fila y las columnas en otro for anidado. Sin embargo, para poder contar las islas que se tendrían en la matriz, debería de haber varios elementos con valor 1 conectados de forma vertical u horizontal, en cualquiera de las dos formas. Si en un dado caso se encuentra un valor de 1, se debería activar una variable que indique que se están contando los elementos dentro de una isla por lo que se debería de guardar la referencia de las columnas en las que se encuentran los elementos  1 en dicha fila y luego continuar en la siguiente fila en el momento que se dejen de encontrar elementos 1, lo que se me ocurre es que después se recorre la siguiente fila específicamente en las columnas referenciadas para así ver si también hay elementos con valor 1. Aunque si hay otros elementos consecutivos en la misma fila, entonces estos también formarían parte de la isla, este proceso se haría hasta llegar a un momento en el que ya no haya elementos 1 consecutivos y se contaría como una isla. Después se repetiría el proceso principal para encontrar más islas. 

#### Ejemplo iterativo: 
def contarElementosIterativo(matriz, fila, columna, color):
	if matriz[fila][columna] != color:
        		return 0
	contador = 0
	referencia = [(fila, columna)]
 	while referencia:
      		  f, c = referencia.pop()
if 0 <= f < len(matriz) and 0 <= c < len(matriz[0]) and matriz[f][c] == color:
            contador += 1
            matriz[f][c] = None  
            stack.append((f + 1, c))
            stack.append((f - 1, c))
            stack.append((f, c + 1))
            stack.append((f, c - 1))
    return contador
Donde el color a contar sería 1.

#### Método recursivo. 
Para una forma recursiva el método sería similar en su declaración pero tendría que mandarse a llamar dentro pero indicando las diferentes direcciones en las que podría moverse la posición en la que estemos, tomando en cuenta claro, que si estamos en la posición 0, no podemos ir a un número negativo y el límite sería ya sea el ancho o el alto de la matriz, además si devolvemos un valor de 1 cuando vamos encontrando una isla cuando se sume el contador podemos usar como referencia la recursividad del método utilizado. 

#### Ejemplo recursivo: 
def contarElementosRecursivo(matriz, fila, columna, color):
if not (0 <= fila < len(matriz)) or not (0 <= columna < len(matriz[0])) or matriz[fila][columna] != color:
        		return 0
	contador = 1
	matriz[fila][columna] = None
contador += contarElementosRecursivo (matriz, fila + 1, columna, color)
    	contador += contarElementosRecursivo (matriz, fila - 1, columna, color)
    	contador += contarElementosRecursivo (matriz, fila, columna + 1, color)
    	contador += contarElementosRecursivo (matriz, fila, columna - 1, color)

### Conclusión 
En conclusión, vemos que el método recursivo parece ser más óptimo que el iterativo, aunque pueden adaptarse características del otro según se necesite, en este caso creo que incluso solo con aplicar el segundo es suficiente, sobre todo por la naturaleza del problema, en donde la conexión de los elementos que conforman una isla puede ser tanto de forma horizontal como vertical. 
Lo que pude observar en este ejercicio, es que yo tenía asociado los métodos que vimos en las primeras clases con los ejercicios que estábamos resolviendo para encontrar islas también, creo que, entrando en contexto con la inteligencia artificial, estas características también podrían ser aprendidas y aprovechadas para resolver el problema. 



