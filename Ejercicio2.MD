#   Ejercicio 2

## Caso 1: Mover de una lado del rio a otro a 1 pollo, 1 lechuga y 1 coyote
### secuencia de persepción y medida rendimiento 

** Medida de persepción: 
    Pollo: P, Coyote: C, Lechuga: L, Granjero: G.

    - Lado1: C,P,L,G  Lado2:
    - Lado1: L,P,G  Lado2: C
    - Lado1: P, G   Lado2: C, L  
    - Lado1: P   Lado2: G, C, L  
    - Lado1:   Lado2: G, C, P, L  

** Secuencia de rendimiento: 
    Se tiene 1 pollo, 1 lechuga y 1 coyote, hay dos islas de tierra y en medio
    se tiene un rio que se necesita cruzar, la idea es llevar a los 3 
    de un lado de un rio al otro sin que se coman entre ellos, el pollo se come a la
    lechuga, el coyote se come al pollo. 
    Solo caben 2 elementos en el bote.
    



##  Caso 2: Mover como en el caso anterior, 3 caniblaes y 3 monjes, donde solo
##  se pueden transportar 2 en el bote a la vez 

** Medida de persepción: 
    Monje: M
    Canibal: C

    -- Lado1: M,M,M,C,C,C   Lado2: 
    -- Lado1: M,M,M,C,C     Lado2: C 
    -- Lado1: M,M,M,C       Lado2: C,C 
    -- Lado1: M,M,M         Lado2: C,C,C
    -- Lado1: M,M,M,C       Lado2: C,C
    -- Lado1: M,C           Lado2: M,M,C,C
    -- Lado1: C             Lado2: M,M,M,C,C
    -- Lado1: M,C           Lado2: M,M,C,C
    -- Lado1:               Lado2: M,M,M,C,C,C


** Secuencia de rendimiento: 
    Como en el caso anterior se desea transportar a 3 monjes y 3 canibales de un lado del
    rio al otro. 
    El canibal se puede comer al monje. 
    Si hay mas canibales que monjes, se los pueden comer, en el caso contrario, no.
    En el bote solo caben 2 individuos y uno debe regresar, mientras que el otro se queda
    en el lado 2. La idea es transportar a todos de un lado a otro sin que los canibales
    se coman a los monjes. 

