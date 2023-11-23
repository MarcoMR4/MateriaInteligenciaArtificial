🔙 [Volver](README.MD)

## Practica 5 Introducción a la inteligencia artificial Introspección: Elementos de color en una imagen. 

### Introducción 
El siguiente ensayo es una redacción relacionada a cómo resolver un problema muy similar al problema anterior, en el que se contaban islas en una matriz definida, en este caso el problema consiste en contar el número de elementos que abarcan la gama de colores rojos. 
La importancia de este problema radica en que este ejemplo es una aplicación mucho más realista de como contar el número de elementos dentro de una imagen con una característica en común, la cual es el color de los mismos. 

### Desarrollo 
#### Percepción y análisis del problema 
La primera impresión que tengo de este problema es que veo una imagen con muchos objetos distribuidos y que además hay una gran variedad de colores. La mayoría de estos son alimentos que tienen tamaños, formas y colores distintos. 
Lo primero que se me viene a la mente en esta situación es que en un concepto muy básico una imagen puede ser considerada como una matriz, una matriz de pixeles, a fin de cuentas, en donde cada uno tiene un color distinto. 
Otra característica que observo es que la imagen es una matriz muy grande que, de hecho, su tamaño puede no siempre estar definido como lo es el caso de una matriz pequeña, pero a fin de cuentas si tomamos las medidas del número de filas y columnas entonces el ejercicio se puede resolver de manera muy similar al anterior, que es el de las islas, a fin de cuentas, en este caso es como si contáramos islas, pero ahora manejando un color como referencia. 
Para tener una referencia más clara y limitar los colores podríamos utilizar los rangos numéricos en que los colores se acercan a los tonos rojos y tener una sola referencia para detectar todos los objetos que puedan considerarse “rojos”. 
Los colores que normalmente hemos manejado en estos rangos son los RGB que son los tres colores primarios que forman a los demás, aunque solo es un formato de muchos que se manejan para el color digital. 
El primer paso sería poder procesar la imagen para convertirla en una matriz, esto utilizando una librería que permita el manejo de imágenes y colores como el caso de open cv del lenguaje Python, luego definir los colores. Además se debería definir un contador para guardar el número de elementos, objetos o islas encontrados con la característica que se solicita. 
Ejemplo de algoritmo 

```python
r1 = 100, g1 = 0, b1 = 0
r2 = 255, g2 = 100, b2 = 100
islas = 0

mapa = cv.imread('atividad5.png', 1)  #leer los 3 canales con 1
w =mapa.shape[0]
h =mapa.shape[1]   #w y h para el ancho y alto de la imagen (filas y columnas)
#funcion para evaluar el color 
def rojo(i, j):
    if(mapa[i, j][2] >= r1 and mapa[i, j][2] <= r2):
        if(mapa[i, j][1] >= g1 and mapa[i, j][1] <= g2):
            if(mapa [i, j][0] >= b1 and mapa[i, j][0] <= b2):
                return True;
    return False;

Método recursivo. 
def metodoRecursivo(i, j):
    if not(i < 0 or i >= w or j < 0 or j >= h):
        if(rojo(i,j)):
            mapa[i,j][2] = 0
            mapa[i,j][1] = 0
            mapa[i,j][0] = 0
            metodoRecursivo(i - 1, j)
            metodoRecursivo(i + 1, j)
            metodoRecursivo(i, j - 1)
            metodoRecursivo(i, j + 1)
    return

Ejemplo iterativo: 
for i in range(w):
    for j in range(h):
        if(rojo(i, j)):
            islas += 1
            metodoRecursivo(i, j);
Mostrar resultados 
cv.imshow('Original',mapa)
print('islas:',islas)
cv.waitKey(0)
cv.destroyAllWindows()
```

### Conclusión 
El ejemplo tratado es muy similar al anterior, donde solo se contaban islas, de hecho, entre más pequeños son los pixeles, más curveadas pueden apreciarse esas islas, pero viéndolos desde la perspectiva de una matriz, sabemos que también son cuadradas como el caso de una matriz que es más pequeña. 
Para el cerebro humano es más fácil detectar los objetos con colores porque no necesita hacer un análisis tan profundo del mismo, solo observa un todo en el que hay formas, colores, tamaños y diseños. En el caso de una computadora, esta tiene que aprender a procesar las imágenes como en este ejemplo, como si estas fueran una matriz y existen algunas librerías, como lo es open cv de Python que resultan muy útiles para el desarrollo de inteligencias artificial enfocada a la visión. 

