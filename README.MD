# Materia: Inteligencia Artificial 


# Práctica 8: Reglas y búsquedas

# ********Ejercicio 1: Juego de gato en 3D********

## Se necesita una IA capaz de ganar un juego de gato en 3 dimensiones

### Medida de percepción:
- Se tienen 3 niveles en 2D del juego gato.
- Cada nivel tiene 9 espacios para rellenar.
- Se forman un total de 27 espacios con posibles combinaciones.
- Se tienen líneas horizontales que se forman en cada nivel.
- Se tienen líneas verticales que se forman conectando los niveles entre sí.
- Se tienen diagonales horizontales y verticales.

### Secuencia de rendimiento:
- Buscar una esquina.
- Buscar esquina en otro extremo para poder formar una diagonal horizontal.
- Buscar esquina en otro extremo para formar una diagonal vertical.
- Si el oponente no ocupa el centro horizontal o vertical, es decir, cualquiera de los dos centros (horizontal o vertical), el juego se gana.


# ********Ejercicio 2********

## Caso 1: Mover de un lado del río a otro a 1 pollo, 1 lechuga y 1 coyote
### Secuencia de percepción y medida de rendimiento

**Medida de percepción:**
Pollo: P, Coyote: C, Lechuga: L, Granjero: G.

- Lado1: C, P, L, G    Lado2:
- Lado1: L, P, G        Lado2: C
- Lado1: P, G           Lado2: C, L
- Lado1: P              Lado2: G, C, L
- Lado1:                Lado2: G, C, P, L

**Secuencia de rendimiento:**
Se tiene 1 pollo, 1 lechuga y 1 coyote. Hay dos islas de tierra y en medio se tiene un río que se necesita cruzar. La idea es llevar a los 3 de un lado de un río al otro sin que se coman entre ellos. El pollo se come a la lechuga, el coyote se come al pollo. Solo caben 2 elementos en el bote.

## Caso 2: Mover como en el caso anterior, 3 caníbales y 3 monjes, donde solo se pueden transportar 2 en el bote a la vez

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


# ********Ejercicio 3: 3 ranas azules y tres rojas********

## Medida de percepción
Se tienen 7 posiciones.
Las 3 de cada extremo se ocupan por cada grupo de ranas.
Una rana solo puede saltar a 1 posición.
Una rana puede saltar 2 posiciones siempre y cuando haya una rana al lado y la segunda posición esté libre.
Ranas azules: A
Rana roja: R

## Secuencia de rendimiento
Se desea comenzar desde un estado inicial de A, A, A, _, R, R, R a un estado R, R, R, _, A, A, A de la forma más óptima posible.

## Espacio de estados

- A A A _ R R R
- A A _ A R R R



# ******** Obtener las variables de las personas que votan en las elecciones ********

## Secuencias de percepción:
- Personas en un país en el que se va a elegir un presidente.
- País con 32 estados.
- Cada estado tiene un número estimado de personas.

## Medida de rendimiento:

**Realizar encuestas que soliciten datos:**
- Edad
- Género
- Candidato preferido
- Entidad Federativa
- Municipio






# Actividades Agosto Diciembre 2023

## Práctica 1. Introducción a la Inteligencia Artificial Actividad 1


### Ensayo: Inteligencia Artificial, un enfoque moderno

#### Introducción 
El presente ensayo abarca el tema de la inteligencia artificial basado en el libro “Inteligencia Artificial, un enfoque moderno”, por Stuart Rusell, este es un campo de la computación y la tecnología muy importante que ha tomado auge en los últimos años, la industria, la globalización y la manera en que la velocidad del trabajo que las personas han necesitado recientemente lleva a necesitar la tecnología como un asistente capaz de ayudar a resolver problemas para la reducción de tiempos y costes de recursos. Este ensayo habla sobre los capítulos 1 y 2 donde se habla de los fundamentos de la inteligencia artificial y el concepto del agente, el cual es el que hace uso de la misma. También se mencionan los capítulos 26 y 27 donde se habla de los fundamentos filosóficos, como es que la inteligencia artificial ha existido desde hace mucho tiempo y como en el futuro esta tendrá crecimiento.


#### Desarrollo
Capítulo 1. La inteligencia Artificial. 
Cuando estamos hablando de inteligencia artificial comúnmente nos imaginamos un tema interesante e incluso lleno de fantasía, sin embargo, es una realidad, y una que ha estado muy presente en las últimas décadas. Tal como describe el libro “Inteligencia Artificial: un enfoque moderno” de Stuart Rusell, es una disciplina que conlleva muchísimo trasfondo y aplicación de conocimientos que se mencionan en algunos de sus capítulos. 
Un tema muy importante que se menciona en el primer capítulo es la racionalidad, la cual relaciono mucho con la acción de tomar las mejores decisiones en base a la experiencia que un individuo va tomando, como sabemos, el ser humano ha sido el ser vivo más racional conocido hasta el momento, y por otro lado, sabemos que las computadoras tienen la capacidad de realizar todo tipo de tareas y pueden procesar la información de una forma similar a como el cerebro humano lo hace, sin embargo, necesitan ser programadas, esta es una de las bases que comienzan con el concepto de la inteligencia artificial. 
Un tema interesante mencionado en el primer capítulo es la prueba de Turing, que en pocas palabras ayudó a determinado si una máquina realmente tenía inteligencia propia pasando una prueba en la que una persona no se daba cuenta si quien le contestaba era una. Además, se menciona que hay 4 puntos muy importantes que una computadora inteligente debería poseer, estas son: procesamiento de lenguaje natural, representación del conocimiento, razonamiento automático y aprendizaje automático. 
Al ver esas 4 características que necesita una máquina para ser inteligente pienso que tiene mucho sentido, porque de alguna manera se vuelve independiente, cuando una persona nace, aprende, pero también aprende a comunicarse para poder expresar sus conocimientos, por otro lado tiene que darles forma, tiene que asociar las cosas y de alguna manera poder expresarlas, a su vez, otra persona pasa por lo mismo y son conocimiento que se comparten mutuamente, siempre y cuando una persona tenga un cerebro sano, se puede apreciar que de alguna manera adquiere, procesa y comparte la información de forma independiente. 
Entre los temas que se ven dentro del primer capítulo también se tiene el enfoque cognitivo, este también se relacionado con lo mencionado anteriormente, para que una persona pueda aprender, necesita entradas de información, en el caso de estas, se tienen los 5 sentidos, vista, oído, tacto, gusto y olfato, y es a través de estos que toda la información del mundo que nos rodea puede entrar al cerebro para generar un conocimiento, entonces, viéndolo en el enfoque de la inteligencia artificial, una máquina también necesita fuentes de entrada similares para poder procesar la información con la que puede generar conocimiento. 
Un tema que cabe destacar es el concepto del agente racional, que tal como nos lo menciona este capítulo es una entidad que existe meramente con la finalidad de resolver problemas que se le presentan, pero necesita tener la capacidad de percibir su entorno y adaptarse a este, esto cobra mucho sentido porque es como si por ejemplo le pides a una persona invidente que te replique el dibujo de tu personaje favorito, el sería como un gente incapaz de percibir su entorno, pero solo desde el punto de vista de la imagen que tiene enfrente, ese entorno de alguna manera le permite al agente recibir las entradas de información para que este encuentre una solución y resuelva el problema, que en el ejemplo mencionado sería poder replicar una imagen o dibujo, además esta característica de resolver problemas es intrínseca para el agente. 
Cuando hablamos de la inteligencia artificial probablemente nos preguntamos, de hecho, en mi caso si llegue a hacerlo, ¿Desde cuándo existe? Comúnmente podemos pensar que es algo muy reciente, quizá sin tener más de in siglo de existencia, pero la realidad es que sus principios, o al menos el principio de sus fundamentos existe desde hace miles de años, desde la antigua Grecia, cuando estaban los grandes filósofos como Aristóteles, que tal como menciona el libro, dio los primeros aportes para entender cómo funcionaba el razonamiento por medio de silogismos, en donde a partir de premisas que uno iba dando se iban teniendo conclusiones. 
Las matemáticas también han sido otro factor que ha nutrido el desarrollo de la inteligencia artificial, el capítulo 1 nos menciona que existen 3 campos importantes en los que le ha aportado como lo son: lógica, probabilidad y computación. Ciertamente podemos relacionar la computación con la matemática, puesto que el procesador, que es el cerebro de la misma y su núcleo, siempre realiza operaciones matemáticas y lógicas dentro de su funcionamiento. 
Otro de los aspectos básicos que vale la pena tomar en cuenta es la lógica de primer orden que planteo Gottlob Frege en base a la matemática booleana que aportó George Boole, esta rama de la mátematica está muy apegada a la forma en que los procesadores trabajan, y por otro lado la lógica de primer orden se considera una base para entender la forma en que funciona el conocimiento. Por otra parte, la probabilidad ha aportado mucho para la inteligencia artificial, e incluso hoy en día sigue siendo un recurso muy importante, y es que el mundo que vivimos es completamente impredecible y con esta disciplina podemos tener un apoyo a través de mediciones en las que existe incertidumbre, como mencioné anteriormente, un agente puede tener un entorno y resolver problemas que claro existan en ese contexto, pero ya viéndolo de forma realista, el mundo es algo completamente impredecible. 
El agente puede ser dotado con la inteligencia artificial y gracias a esto puede tomar decisiones, gracias al uso de las ciencias que mencionamos, y no solamente son estas ciencias, la inteligencia artificial también se ha nutrido de campos como investigación de operaciones, la teoría de la decisión, de juegos. 
Como vemos es un campo bastante interesante y demasiado complejo, pero este también está basado en cómo funciona la mente humana, esta se encuentra físicamente en el cerebro y a su vez, está conformado por neuronas, las cuales tienen su propia estructura y se conectan entre sí para poder compartir pulsos nerviosos e información, luego también pueden haber salidas que serían órdenes para el resto del cuerpo, pues ciertamente es otro aspecto importante para la inteligencia artificial, puesto que esta también utiliza neuronas artificiales, algo que se parece mucho al cerebro humano es el procesador de una computadora que contiene miles de transistores que a su vez, tratan la información, pulsos de energía eléctrica a muy pequeña escala, realmente este tema a mí me parece fascinante y me impresiona como los seres humanos podemos llegar a ser tan conscientes al grado de poder replicar la forma de funcionar de nuestro cerebro en una máquina. La introspección es esa habilidad de la que hablo, la capacidad de ser conscientes de nosotros mismos, procesar esa información y luego poder plasmarla en otra entidad, es extraño mencionarlo así, pero incluso queremos ser conscientes de lo que nos hace consientes y llegar a un nivel todavía más alto de conciencia del que como tal no existen evidencias físicas, pero si metafóricas e incluso metafísicas. 
Como vemos, un robot puede llegar a ser muy similar a un ser humano, mientras que su cerebro puede ser una computadora muy compleja, su cuerpo pueden ser sistemas mecánicos o electromecánicos que teniendo la señales adecuadas pueden simular el sistema nervioso humano, los sensores serían como los sentidos y los actuadores como las extremidades o los mecanismos necesarios para realizar alguna tarea y bueno, a su vez, esa tarea pudiera solucionar algún problema, incluso el habla se consideraría un mecanismo. 
Una persona muy importante en todo este ámbito es John McCarthy, uno de los iniciadores de la inteligencia artificial que comenzaron con temas como las redes neuronales, estas podríamos verlas como la representación de un cerebro, o al menos una parte de uno, en la que se pretende generar conocimiento y aprender con la información que entra y luego en base al conocimiento poder dar soluciones, nos mencionan que en un principio no se les pudo dar una consolidación muy buena pero en los últimos años ha retomado mucha importancia en este tema y además ha ido creciendo su desarrollo. Con ayuda de la inteligencia artificial muchas áreas en las que el ser humano trabaja hoy día pueden tener mucho apoyo, pues se reduce el tiempo para la consulta de soluciones, y esto es importante destacarlo porque la velocidad de procesamiento de una computadora es mucho más alta que la del cerebro humano. Además, esta disciplina se ha convertido en una ciencia con un gran campo de investigación y ramas como lo es la ciencia de datos, que permiten hacer el uso de sus herramientas para diferentes aplicaciones, industrias y contextos. 
Capítulo 2. El agente inteligente 
En este capítulo se mencionan las bases de lo que es un agente racional, como se mencionó previamente, su finalidad es la de resolver problemas, teniendo un objetivo en base a un entorno que este debe conocer, incluso puede haber varios de ellos, estos de hecho podrían ser un robot inteligente, con sus propios sensores y actuadores,  un concepto importante en este tema es que el agente usa una secuencia de percepción para conocer dicho entorno y usa una medida de rendimiento para encontrar la forma más rápido de resolver el problema que le sea planteado, el agente tiene dentro lo que se conoce como el programa del agente que es toda la parte con la que procesa información y llega a las conclusiones, además si este busca la mejor manera de hacer las cosas se le considera un agente racional, pues usa su conocimiento para tomar sus decisiones. 
Hay muchas maneras en que el agente puede interpretar su entorno, ya cuando se aplica en la inteligencia artificial en un computador podemos darnos cuenta de la complejidad que esto conlleva, desde solo pasar datos numéricos hasta pasar una matriz completa para poder representar a una imagen. 

Capítulo 26. Fundamentos filosóficos 
Este es meramente teórico, pero maneja conceptos importantes que hay que conocer relacionado a la inteligencia artificial, como a inteligencia artificial débil que nos dice que es posible que las máquinas puedan actuar con inteligencia, pero solo es posible, mientras que la inteligencia artificial fuerte nos dice que esto no es solo posible, sino es un hecho. Hasta la fecha lo más realista que he podido observar es que la inteligencia artificial débil puede estar más presente pero no es algo completamente definido, de hecho, para que la máquina pueda pensar tiene que existir una cierta programación para que esta aprenda, pero al menos yo no he visto alguna que ya de fábrica tenga la capacidad de aprender de forma independiente, este haría que el conocimiento pudiera compartirse incluso entre máquinas. La teoría de la incapacidad es un tema que nos menciona precisamente que las máquinas nos son en primera instancia como personas y mucho menos actuarían en base a pensamientos subjetivos. El aprendizaje no supervisado es un tema en el que se menciona que las máquinas si van aumentando su conocimiento de forma independiente utilizando el aprendizaje por refuerzo y el supervisado es en el que se le necesita proporcionar información para su conocimiento. 
Entender las emociones humanas y sus propios pensamientos es algo que sería difícil para la inteligencia artificial, tendría que cumplirse la idea de la inteligencia artificial fuerte en la que esta sería consciente incluso de la forma en que ha sido creada, pero es un tema complejo, porque ni siquiera el ser humano sabe que es lo que origino a su capacidad de razonar o que hay más arriba de esa conciencia. 
Capitulo 27. Ia en el presente y el futuro
En este tema se abarca lo que es la estructura de un agente y los conceptos que pueden aplicarse para mejorarlo y además se hace mención de que si un agente fuera totalmente consciente esto podría no ser del todo conveniente para los seres humanos. 
Al ser construido un agente puede tener una racionalidad perfecta caludadora, limitada o una optimalidad limitada, en la que la segunda y la tercera tienen un enfoque más realista en cuestión del tiempo que llevaría llegar a una decisión y la optimalidad limitada toma en cuenta el uso de los recursos computacionales 

#### Conclusión 
Las máquinas han existido en concepto desde siempre, comenzaron como simples herramientas y se desarrollaron hasta convertirse en cosas muy complejas a las que ahora se les puede dar la capacidad de aprender y tomar sus propias acciones para llevar a cabo una tarea, es muy importante entender que la inteligencia artificial debe ser solo eso una herramienta y no podemos permitir completamente de la misma, ciertamente será un gran apoyo para el avance de la especie humana en cuestión tecnológica e incluso quizá algún día llegar a lugares inexplorados pero esto debe ser con su debida medida y equilibrio. 
Entender los conceptos más básicos de la inteligencia artificial, como desde donde se concibe su idea, en que está basado su funcionamiento, todas las formas en que se puede aplicar en la computación, las ramas que maneja y como puede hacer uso de otras disciplinas como la matemática es muy importante para poder trabajar dentro de este ámbito si somos personas especializadas en tecnologías de información y comunicación. 





