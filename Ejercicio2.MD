#   Ejercicio 2

## Caso 1: Mover de una lado del rio a otro a 1 pollo, 1 lechuga y 1 coyote
### secuencia de persepción y medida rendimiento 

** Medida de persepción: 
    Se tiene 1 pollo, 1 lechuga y 1 coyote, hay dos islas de tierra y en medio
    se tiene un rio que se necesita cruzar, la idea es llevar a los 3 
    de una isla a la otra sin que se coman entre ellos, el pollo se come a la
    lechuga, el coyote se come al pollo. 
    Solo caben 2 elementos en el bote.
    Pollo: P, Coyote: C, Lechuga: L, Granjero: G.

** Secuencia de rendimiento: 
    - Lado1: C,P,L,G  Lado2:
    - Lado1: L,P,G  Lado2: C
    - Lado1: P, G   Lado2: C, L  
    - Lado1: P   Lado2: G, C, L  
    - Lado1:   Lado2: G, C, P, L  

    


##  Caso 2: Mover como en el caso anterior, 3 caniblaes y 3 monjes, donde solo
##  se pueden transportar 2 en el bote a la vez 

** Medida de persepción: 
    Como en el caso anterior se desea transportar a 3 monjes y 3 canibales de una 
    isla a la otra. 
    El canibal se puede comer al monje. 
    Si hay mas canibales que monjes, se los pueden comer, en el caso contrario, no.
    Monje: M
    Canibal: C


** Secuencia de rendimiento: 
    -- Lado1: M,M,M,C,C,C    Lado2:
    -- Lado1: M,M,C,C    Lado2: M,C
    -- Lado1:    Lado2: 
    -- Lado1:     Lado2: 