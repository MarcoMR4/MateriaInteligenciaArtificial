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


