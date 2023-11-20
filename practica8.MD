- [Volver](README.md)

## Práctica 8: Reglas y búsquedas

### ********Ejercicio 1: Juego de gato en 3D********

#### Se necesita una IA capaz de ganar un juego de gato en 3 dimensiones

#### Medida de percepción:
- Se tienen 3 niveles en 2D del juego gato.
- Cada nivel tiene 9 espacios para rellenar.
- Se forman un total de 27 espacios con posibles combinaciones.
- Se tienen líneas horizontales que se forman en cada nivel.
- Se tienen líneas verticales que se forman conectando los niveles entre sí.
- Se tienen diagonales horizontales y verticales.

#### Secuencia de rendimiento:
- Buscar una esquina.
- Buscar esquina en otro extremo para poder formar una diagonal horizontal.
- Buscar esquina en otro extremo para formar una diagonal vertical.
- Si el oponente no ocupa el centro horizontal o vertical, es decir, cualquiera de los dos centros (horizontal o vertical), el juego se gana.


### ********Ejercicio 2********

#### Caso 1: Mover de un lado del río a otro a 1 pollo, 1 lechuga y 1 coyote
#### Secuencia de percepción y medida de rendimiento

**Medida de percepción:**
Pollo: P, Coyote: C, Lechuga: L, Granjero: G.

- Lado1: C, P, L, G    Lado2:
- Lado1: L, P, G        Lado2: C
- Lado1: P, G           Lado2: C, L
- Lado1: P              Lado2: G, C, L
- Lado1:                Lado2: G, C, P, L

**Secuencia de rendimiento:**
Se tiene 1 pollo, 1 lechuga y 1 coyote. Hay dos islas de tierra y en medio se tiene un río que se necesita cruzar. La idea es llevar a los 3 de un lado de un río al otro sin que se coman entre ellos. El pollo se come a la lechuga, el coyote se come al pollo. Solo caben 2 elementos en el bote.

### Caso 2: Mover como en el caso anterior, 3 caníbales y 3 monjes, donde solo se pueden transportar 2 en el bote a la vez

**Medida de percepción:**
Monje: M, Caníbal: C

- Lado1: M, M, M, C, C, C    Lado2:
- Lado1: M, M, M, C, C       Lado2: C
- Lado1: M, M, M, C         Lado2: C, C
- Lado1: M, M, M            Lado2: C, C, C
- Lado1: M, M, M, C         Lado2: C, C
- Lado1: M, C                Lado2: M, M, C, C
- Lado1: C                  Lado2: M, M, M, C, C
- Lado1: M, C                Lado2: M, M, C, C
- Lado1:                    Lado2: M, M, M, C, C, C

**Secuencia de rendimiento:**
Como en el caso anterior, se desea transportar a 3 monjes y 3 caníbales de un lado del río al otro. El caníbal se puede comer al monje. Si hay más caníbales que monjes, se los pueden comer, en el caso contrario, no. En el bote solo caben 2 individuos y uno debe regresar, mientras que el otro se queda en el lado 2. La idea es transportar a todos de un lado a otro sin que los caníbales se coman a los monjes.


## ********Ejercicio 3: 3 ranas azules y tres rojas********

### Medida de percepción
Se tienen 7 posiciones.
Las 3 de cada extremo se ocupan por cada grupo de ranas.
Una rana solo puede saltar a 1 posición.
Una rana puede saltar 2 posiciones siempre y cuando haya una rana al lado y la segunda posición esté libre.
Ranas azules: A
Rana roja: R

### Secuencia de rendimiento
Se desea comenzar desde un estado inicial de A, A, A, _, R, R, R a un estado R, R, R, _, A, A, A de la forma más óptima posible.

### Espacio de estados

- A A A _ R R R
- A A _ A R R R



## ******** Obtener las variables de las personas que votan en las elecciones ********

### Secuencias de percepción:
- Personas en un país en el que se va a elegir un presidente.
- País con 32 estados.
- Cada estado tiene un número estimado de personas.

### Medida de rendimiento:

**Realizar encuestas que soliciten datos:**
- Edad
- Género
- Candidato preferido
- Entidad Federativa
- Municipio
