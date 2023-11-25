🔙 [Volver](README.MD)

## Practica 3 Introducción a la inteligencia artificial Introspección

### Introducción 
Este ensayo aborda el tema sobre resolver un desafío, el cual consiste en intercambiar la posición de 4 alfiles blancos y 4 negros que se encuentran en la primera y última fila respectivamente en un tablero de ajedrez de 5 x 4, la idea es interpretar la solución desde el punto de vista introspectivo. 
La importancia de este ensayo radica en conocer o tener un mejor entendimiento del proceso cognitivo y de resolución de problemas que tiene la inteligencia artificial conociendo el que tenemos los seres humanos, la misma mencionada pretende funcionar de la misma manera que la inteligencia natural del ser humano, que hasta el momento es el ser vivo con la máxima capacidad de utilizar la misma y además ser consciente. 

### Desarrollo 
#### Percepción y análisis del problema. 
El problema que se presenta es un tablero similar al del ajedrez, pero en una versión más pequeña. En primer lugar, lo que hago es observar el tablero que tiene 5 filas y 4 columnas, la primera y la última fila son las únicas que tienen alfiles, la primera tiene 4 ejemplares blancos y la segundo a su vez tiene 4 ejemplares negros. 
Después de observar el tablero lo que hago es deducir que al alfil solo puede realizar movimientos en forma diagonales como en el juego tradicional de ajedrez, por lo que la única manera de cambiarlos de posición es llevándolos en pasos con forma de diagonal. Las diagonales como en el juego tradicional, pueden ser de 2 a n cuadros, claro que tomando en cuenta la medida del tablero, ese es otro detalle que también comienzo a tomar en cuenta. 
En primer lugar, observo que los afiles no se pueden mover en una diagonal más grande de 3 cuadros, puesto que si exceden esta medida entonces quedarían en los posibles caminos de los que están en el extremo opuesto.  

#### Estrategia inicial 
Desde el punto de vista más fácil lo primero que se me vino a la mente fue mover los alfiles de forma que no importase que quedaran en los posibles caminos de los del otro color, viéndolo con esa lógica el primer movimiento que pensé fue en mover al segundo alfil blanco hacia la fila siguiente, pero en el extremo izquierdo, después hacer el mismo movimiento con el alfil negro de hasta el otro lado, lo que observe en este punto es que se formó una cierta simetría, el campo vacío que dejo el alfil negro lo pudo ocupar el alfil blanco y viceversa. 
Al notar que, al mantener cierta simetría, lo siguiente que hice mover de la misma manera los alfiles de la primera fila de la misma forma, pero del lado opuesto, es decir, simétricamente con respecto a la fila. 
Llegue a un punto en el que había que regresar a la primera fila el alfil blanco y el negro para poder repetir otro patrón de simetría y que quedara el camino libre para los demás alfiles y llegaran lo más rápido posible hacia el otro lado. 

#### Movimientos 
Si se mantenía la simetría se podían mover los alfiles alternadamente entre los dos colores, había por ejemplo ocasiones en las que había que moverse un solo cuadro y otras en las que se movían tres, note que este patrón también se repetía mucho. 
En los últimos movimientos quedaban diagonales en los extremos del tablero, por ejemplo, en la fila de hasta abajo (donde inicialmente se encontraban los alfiles blancos), quedaban dos diagonales de alfiles negros y en el otro lado el mismo caso, pero del color contrario. Al ver esto me percaté que solo faltaban 2 movimientos respectivamente para cada color, es decir, 4 movimientos en total y se llegaba a la solución. 
Movimientos para la solución
Cada vez que simulaba un movimiento dibujándolo en la libreta iba contando cada uno, otro detalle aquí es que cada vez que un alfil blanco hacia un movimiento, la mejor estrategia era hacer que el siguiente alfil negro hiciera un movimiento similar, pero de forma simétrica, fue así como llegué a la solución. El número total de movimientos fue de 36, si es que no me comí alguno. 

***Descripción de movimientos***
1. 
>| ♝₁ | ♝₁ | ♝₁ | ♝₁ |
>|---|---|---|---|
>| * | * | * | * |
>| * | * | * | * |
>| * | * | * | * |
>| ♝₂ | ♝₂ | ♝₂ | ♝₂ |



2. 
>| ♝₁ | ♝₁ | ♝₁ | ♝₁ |
>|---|---|---|---|
>| * | * | * | * |
>| * | * | * | * |
>| * | * | ♝₂ | * |
>| ♝₂ | * | ♝₂ | ♝₂ |

3. 
>| ♝₁ | ♝₁ | * | ♝₁ |
>|---|---|---|---|
>| * | ♝₁ | * | * |
>| * | * | * | * |
>| * | * | ♝₂ | * |
>| ♝₂ | * | ♝₂ | ♝₂ |

4. 
>| ♝₁ | ♝₁ | * | ♝₁ |
>|---|---|---|---|
>| * | ♝₁ | * | ♝₂ |
>| * | * | * | * |
>| * | * | ♝₂ | * |
>| * | * | ♝₂ | ♝₂ |

5. 
>| ♝₁ | ♝₁ | * | * |
>|---|---|---|---|
>| * | ♝₁ | * | ♝₂ |
>| * | * | * | * |
>| ♝₁ | * | ♝₂ | * |
>| * | * | ♝₂ | ♝₂ |


6. 
>| ♝₁ | ♝₁ | * | * |
>|---|---|---|---|
>| * | ♝₁ | * | ♝₂ |
>| * | * | * | * |
>| ♝₁ | ♝₂ | ♝₂ | * |
>| * | * | * | ♝₂ |

7. 
>| ♝₁ | * | * | * |
>|---|---|---|---|
>| * | ♝₁ | ♝₁ | ♝₂ |
>| * | * | * | * |
>| ♝₁ | ♝₂ | ♝₂ | * |
>| * | * | * | ♝₂ |

8. 
>| ♝₁ | * | * | * |
>|---|---|---|---|
>| ♝₂ | ♝₁ | ♝₁ | ♝₂ |
>| * | * | * | * |
>| ♝₁ | ♝₂ | * | * |
>| * | * | * | ♝₂ |

9. 
>| ♝₁ | * | * | * |
>|---|---|---|---|
>| ♝₂ | * | ♝₁ | ♝₂ |
>| * | * | * | * |
>| ♝₁ | ♝₂ | * | ♝₁ |
>| * | * | * | ♝₂ |

10. 
>| ♝₁ | * | ♝₂ | * |
>|---|---|---|---|
>| ♝₂ | * | ♝₁ | * |
>| * | * | * | * |
>| ♝₁ | ♝₂ | * | ♝₁ |
>| * | * | * | ♝₂ |

11. 
>| ♝₁ | * | ♝₂ | * |
>|---|---|---|---|
>| ♝₂ | * | ♝₁ | * |
>| * | * | * | * |
>| * | ♝₂ | * | ♝₁ |
>| * | ♝₁ | * | ♝₂ |

12. 
>| ♝₁ | * | ♝₂ | * |
>|---|---|---|---|
>| ♝₂ | * | ♝₁ | * |
>| ♝₂ | * | * | * |
>| * | * | * | ♝₁ |
>| * | ♝₁ | * | ♝₂ |


13. 
>| ♝₁ | * | ♝₂ | * |
>|---|---|---|---|
>| ♝₂ | * | * | * |
>| ♝₂ | * | * | ♝₁ |
>| * | * | * | ♝₁ |
>| * | ♝₁ | * | ♝₂ |

14. 
>| ♝₁ | * | ♝₂ | * |
>|---|---|---|---|
>| * | * | * | * |
>| ♝₂ | ♝₂ | ♝₁ | ♝₁ |
>| * | * | * | * |
>| * | ♝₁ | * | ♝₂ |



15. 
>| ♝₁ | * | ♝₂ | * |
>|---|---|---|---|
>| * | * | * | * |
>| * | ♝₂ | ♝₁ | ♝₁ |
>| * | * | * | * |
>| * | ♝₁ | ♝₂ | ♝₂ |

16. 
>| ♝₁ | ♝₁ | ♝₂ | * |
>|---|---|---|---|
>| * | * | * | * |
>| * | ♝₂ | ♝₁ | * |
>| * | * | * | * |
>| * | ♝₁ | ♝₂ | ♝₂ |

17. 
>| ♝₁ | ♝₁ | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| * | * | ♝₁ | * |
>| * | * | * | * |
>| * | ♝₁ | ♝₂ | ♝₂ |

18. 
>| ♝₁ | ♝₁ | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| * | * | * | * |
>| * | * | * | * |
>| ♝₁ | ♝₁ | ♝₂ | ♝₂ |

19. 
>| ♝₁ | ♝₁ | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| * | ♝₂ | * | * |
>| * | * | * | * |
>| ♝₁ | ♝₁ | ♝₂ | * |
 
20. 
>| * | ♝₁ | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| * | ♝₂ | ♝₁ | * |
>| * | * | * | * |
>| ♝₁ | ♝₁ | ♝₂ | * |

21. 
>| * | ♝₁ | * | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| ♝₂ | ♝₂ | ♝₁ | * |
>| * | * | * | * |
>| ♝₁ | ♝₁ | ♝₂ | * |

22. 
>| * | ♝₁ | * | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| ♝₂ | ♝₂ | ♝₁ | ♝₁ |
>| * | * | * | * |
>| ♝₁ | * | ♝₂ | * |

23. 
>| * | ♝₁ | * | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| ♝₂ | * | ♝₁ | ♝₁ |
>| ♝₂ | * | * | * |
>| ♝₁ | * | ♝₂ | * |

24. 
>| * | ♝₁ | * | ♝₂ |
>|---|---|---|---|
>| * | * | * | ♝₁ |
>| ♝₂ | * | * | ♝₁ |
>| ♝₂ | * | * | * |
>| ♝₁ | * | ♝₂ | * |

25. 
>| * | ♝₁ | * | ♝₂ |
>|---|---|---|---|
>| * | * | * | ♝₁ |
>| ♝₂ | * | * | ♝₁ |
>| ♝₂ | * | * |♝₂ |
>| ♝₁ | * | * | * |
 
26. 
>| * | * | * | ♝₂ |
>|---|---|---|---|
>| ♝₁ | * | * | ♝₁ |
>| ♝₂ | * | * | ♝₁ |
>| ♝₂ | * | * |♝₂ |
>| ♝₁ | * | * | * |

27. 
>| ♝₂ | * | * | ♝₂ |
>|---|---|---|---|
>| ♝₁ | * | * | ♝₁ |
>| ♝₂ | * | * | ♝₁ |
>| ♝₂ | * | * |* |
>| ♝₁ | * | * | * |

28. 
>| ♝₂ | * | * | ♝₂ |
>|---|---|---|---|
>| * | * | * | ♝₁ |
>| ♝₂ | * | * | ♝₁ |
>| ♝₂ | * | * |* |
>| ♝₁ | * | * | ♝₁ |
 
29. 
>| ♝₂ | * | * | ♝₂ |
>|---|---|---|---|
>| * | ♝₂ | * | ♝₁ |
>| * | * | * | ♝₁ |
>| ♝₂ | * | * |* |
>| ♝₁ | * | * | ♝₁ |

30. 
>| ♝₂ | * | * | ♝₂ |
>|---|---|---|---|
>| * | ♝₂ | * | ♝₁ |
>| * | * | * | * |
>| ♝₂ | * | ♝₁ |* |
>| ♝₁ | * | * | ♝₁ |

31. 
>| ♝₂ | * | * | ♝₂ |
>|---|---|---|---|
>| * | ♝₂ | ♝₂ | ♝₁ |
>| * | * | * | * |
>| * | * | ♝₁ |* |
>| ♝₁ | * | * | ♝₁ |
 
32. 
>| ♝₂ | * | * | ♝₂ |
>|---|---|---|---|
>| * | ♝₂ | ♝₂ | * |
>| * | * | * | * |
>| * | ♝₁ | ♝₁ |* |
>| ♝₁ | * | * | ♝₁ |

33. 
>| ♝₂ | * | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | ♝₂ | * |
>| * | * | * | * |
>| * | ♝₁ | ♝₁ |* |
>| ♝₁ | * | * | ♝₁ |

34. 
>| ♝₂ | * | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | ♝₂ | * |
>| * | * | * | * |
>| * | ♝₁ | * |* |
>| ♝₁ | ♝₁ | * | ♝₁ |

35. 
>| ♝₂ | ♝₂ | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| * | * | * | * |
>| * | ♝₁ | * |* |
>| ♝₁ | ♝₁ | * | ♝₁ |

36. 
>| ♝₂ | ♝₂ | ♝₂ | ♝₂ |
>|---|---|---|---|
>| * | * | * | * |
>| * | * | * | * |
>| * | * | * |* |
>| ♝₁ | ♝₁ | ♝₁ | ♝₁ |
 
 
 

 
### Conclusión 
La resolución exitosa de este problema requiere de una estrategia con un enfoque cuidadoso que se pueda utilizar para respetar las limitaciones del juego, una de ellas es que cada color tenía que tomar un turno en cada movimiento. Si lo vemos desde ese punto de vista los alfiles blancos tenían que llegar al otro extremo, pero a la vez que los negros necesitaban hacer lo mismo. 
En lo personal a mí me cuesta trabajo interpretar las estrategias que sigo en mi mente o incluso plasmar la secuencia de pasos que tengo que seguir, más bien la forma en la que llego a la solución de algún problema es, ya sea simulándolo o haciendo los movimientos y necesito apoyarme de alguna bitácora o lista para poder recordar los pasos a seguir, como lo fué en este caso anotar en una hoja de papel y despues en digital, hay personas que tienen mayor facilidad para plasmar su metodología pero en mi caso he notado que me es más sencillo poniéndolo en práctica, quizá desde un enfoque kinestésico, pero a la vez, visual. 

En conclusión, puedo decir que para solucionar un problema de esta naturaleza lo primero es observar detenidamente el tablero del juego y las piezas que hay, cuáles son sus dimensiones, observar cuales son las reglas y las limitaciones para hacer los movimientos, en base a ello pude deducir que si los movimientos eran alternados tenían que tener cierta coordinación y simetría al asociarlo con un numero par, además de que el número de piezas al ser 4 seguía esta lógica, también es importante tomar en cuenta los patrones que se van construyendo ya poniendo en práctica la solución del problema, creo que teniendo en cuenta estas características puede ser una herramienta útil para resolver otro problemas con características similares.  








