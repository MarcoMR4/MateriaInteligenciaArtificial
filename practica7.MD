🔙 [Volver](README.MD)

##  Introducción a la Inteligencia Artificial: El papel de la heurística

**Descripción del problema**

***La heurística.***


Según lo que vimos en clase de inteligencia artificial, recuerdo que el profesor comentó que la heurística es el camino más corto y directo para llegar de un punto a otro, más específicamente tomando en cuenta de la cantidad de cuadros o costo del camino que este tiene, esto sin importar o tomar en cuenta los obstáculos que se encuentren entre ambos con la finalidad de alcanzar la meta de la forma más rápida. 


***Método recursivo.***
```python

# Método recursivo

matriz = [
    [1,1,1,1,1,1,1,1,1],
    [0,0,0,0,0,0,1,0,1],
    [1,1,1,0,1,1,1,0,1],
    [1,0,0,0,1,0,1,0,1],
    [1,0,1,1,1,0,1,0,1],
    [1,0,0,0,0,0,0,0,1],
    [1,0,1,1,1,0,1,0,1],
    [3,0,1,0,0,0,1,0,1],
    [1,1,1,1,1,1,1,1,1]
]

ya = False

def buscar(x,y):
    global ya
    if(ya):
        return
    if(matriz[x][y] == 3):
        ya = True
        print("salida encontrada ")
    if(x<0 or x>8 or y<0 or y>8 ):
        return 
    else: 
        matriz[x][y] = 2
        buscar(x+1,y)
        buscar(x-1,y)
        buscar(x,y+1)
        buscar(x,y-1)

buscar(1,0)

```

***Solución propuesta.***
Manejando una referencia como un número distinto, en este caso, 3, se puede implementar un algoritmo en el que se busque en las direcciones más cercanas los vecinos que se tengan.

Lo primero sería usar una función para verificar la coordenada en donde nos vayamos moviendo a través del laberinto, asegurándonos de que no nos salgamos del tablero ni nos movamos hacia un muro, que en este caso lo manejaríamos como un "1". 

Teniendo esa función de referencia lo siguiente sería tener una referencia de hacia que dirección movernos, dependiendo de si la función de verificación devuelve un resultado verdadero se guadaría como referencia para el camino que se puede tomar, un método muy similar a lo recursivo pero haciendo comporbaciones en los posiciones que se puedan recorrer, y en este caso solo se recorrerían las que lleven como referencia el 0, sin necesidad de pasar por las casillas marcadas en 1. 

``` python

to = 'r'
laberinto = [
    [1,1,1,1,1,1,1,1,1],
    [0,0,0,0,0,0,1,0,1],
    [1,1,1,0,1,1,1,0,1],
    [1,0,0,0,1,0,1,0,1],
    [1,0,1,1,1,0,1,0,1],
    [1,0,0,0,0,0,0,0,1],
    [1,0,1,1,1,0,1,0,1],
    [3,0,1,0,0,0,1,0,1],
    [1,1,1,1,1,1,1,1,1]
]

def verify(x, y):
    if(x < 0 or x > 8 or y < 0 or y > 8 or laberinto[x][y] == 1):
        return False
    else:
        return True

def right(x, y):
    global to
    if(to == 'r'):
        if(verify(x + 1, y)):
            to = 'd'
            return x + 1, y
        elif(verify(x, y + 1)):
            return x, y + 1
        elif(verify(x - 1, y)):
            to = 'u'
            return x - 1, y
        elif(verify(x, y - 1)):
            to = 'l'
            return x, y - 1
    elif(to == 'd'):
        if(verify(x, y - 1)):
            to = 'l'
            return x, y - 1
        elif(verify(x + 1, y)):
            return x + 1, y
        elif(verify(x, y + 1)):
            to = 'r'
            return x, y + 1
        elif(verify(x - 1, y)):
            to = 'u'
            return x - 1, y
    elif(to == 'l'):
        if(verify(x - 1, y)):
            to = 'u'
            return x - 1, y
        elif(verify(x, y - 1)):
            return x, y - 1
        elif(verify(x + 1, y)):
            to = 'd'
            return x + 1, y
        elif(verifica(x, y + 1)):
            to = 'r'
            return x, y + 1
    elif(to == 'u'):
        if(verify(x, y + 1)):
            to = 'r'
            return x, y + 1
        elif(verify(x - 1, y)):
            return x - 1, y
        elif(verify(x, y - 1)):
            to = 'l'
            return x, y - 1
        elif(verify(x + 1, y)):
            to = 'd'
            return x + 1, y

def to_right(x, y):
    global to
    if(laberinto[x][y] == 3):
        print('salida encontrada en: (',x,',', y,')')
        return
    else:
        print('casilla: (',x, y,')')
        xs, ys = right(x, y)
        to_right(xs, ys)

to_right(1, 0)

```

