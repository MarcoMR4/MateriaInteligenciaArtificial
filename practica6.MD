## Prática 6. Introducción a la Inteligencia Artificial: El proceso de razonamiento según la lógica

**Problema de Josephus**

Con respecto al problema de Flavius Josephus podemos comenzar con un análisis de patrones utilizando como referencia un número de prisioneros más pequeños. donde en las suseciones el número de prisionero se convierte en una "x" al ser asesinado.

1.  1, 2
    1, x --pos 1

2.  1, 2, 3
    1, x, 3
    x, x, 3 --pos 3

3.  1, 2, 3, 4
    1, x, 3, x
    1, x, x, x --pos 1

4.  1, 2, 3, 4, 5
    x, x, 3, x, 5
    x, x, 3, x, x  --pos 3

5.  1, 2, 3, 4, 5, 6
    1, x, 3, x, 5, x
    x, x, x, x, 5, x --pos 5

6.  1, 2, 3, 4, 5, 6, 7
    1, x, 3, x, 4, x, 7
    x, x, 3, x, x, x, 7
    x, x, x, x, x, x, 7 --pos 7

7.  1, 2, 3, 4, 5, 6, 7, 8
    1, x, 3, x, 5, x, 7, x
    1, x, x, x, 5, x, x, x
    1, x, x, x, x, x, x, x --pos 1 

Para este punto podemos darnos cuenta de que la posicion vuelve a ser 1, otro aspecto a considerar es que números como 2, 4 y 8 se han descartado de las posiciones seguras. 

8.  1, 2, 3, 4, 5, 6, 7, 8, 9
    1, x, 3, x, 5, x, 7, x, 9
    x, x, 3, x, x, x, 7, x, x
    x, x, 3, x, x, x, x, x, x --pos 3 

9.  1, 2, 3, 4, 5, 6, 7, 8, 9, 10 
    1, x, 3, x, 5, x, 7, x, 9, x 
    x, x, x, x, 5, x, 7, x, 9, x
    x, x, x, x, 5, x, x, x, 9, x
    x, x, x, x, x, x, x, x, 9, x --pos 9

10. 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11
    1, x, 3, x, 5, x, 7, x, 9, x, 11
    x, x, 3, x, x, x, 7, x, x, x, 11
    x, x, x, x, x, x, 7, x, x, x, x --pos7 

11. 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15 
    1, x, 3, x, 5, x, 7, x, 9, x, 11, x, 13, x, 15 
    x, x, 3, x, x, x, 7, x, x, x, 11, x, x, x, 15
    x, x, x, x, x, x, x, x, x, x, x, x, x, x, 15  --pos 15

12. 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16 
    1, x, 3, x, 5, x, 7, x, 9, x, 11, x, 13, x, 15, x
    1, x, x, x, 5, x, x, x, 9, x, x, x, 13, x, x, x
    1, x, x, x, x, x, x, x, x, x, x, x, x, x, x, x --pos 1 

    En este caso vemos que antes de llegar a 16, la posición vuele a ser 1, el número 15 es un número impar, pero además vemos que cuando el número de posición va a tomar un valor de potencia de 2, se regresa a 1, por lo que podemos deducir que la posición no debe ser par ni tampoco potencia del número 2. 

    Ejemplo de algoritmo: 

    


