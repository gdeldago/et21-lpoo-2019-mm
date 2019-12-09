# et21-lpoo-2019-mm
Escuela técnica N°21 - Laboratorio de programación orientda a objetos - 2019 
## Examen - Laboratorio de programación orientada a objetos. 

### Importante.
Antes de comenzar resolver leer atentamente el enunciado completo (Domino y consignas). En cada consigna se indican los puntos con los que ésta contribuye a la nota final en caso de estar resueltos de manera correcta y completa. 

Para la evaluación se consideraran los avances según el siguiente calendario de revisiones:
1. Martes 10/12 17:30
2. Jueves 12/12 17:30
3. Martes 17/17 12:00

### Dominio.
Se trata de modelar algunos aspectos del juego Dominó. No hace falta conocer las reglas del juego pero es fundamental atender a las consideraciones y características que se detallan a continuación:
Se trata de un juego en el que se utiliza un conjunto de 28 fichas.
Cada ficha tiene dos números con valores entre el 0 (cero) y el 6 (seis). A estos valores o puntos se los llama palos.
Las fichas corresponden al conjunto de todas las combinaciones de palos sin repeticiones. A continuación se detallan las 28 fichas indicando sus valores separados por un guión:
0-0 
1-0, 1-1
2-0, 2-1, 2-2
3-0, 3-1, 3-2, 3-3
4-0, 4-1, 4-2, 4-3, 4-4
5-0, 5-1, 5-2, 5-3, 5-4, 5-5
6-0, 6-1, 6-2, 6-3, 6-4, 6-5, 6-6
A las fichas con números repetidos se las llama dobles.
Aquí nos ocuparemos de una versión simplificada en la que participan sólo 2 jugadores.
Se reparten 7 fichas a cada jugador escogidas al azar.
El objetivo del juego es deshacerse de las fichas recibidas.
Cada jugador en su turno podrá bajar a la mesa una ficha siempre que se cumplan las siguientes condiciones:
Si no hay fichas en la mesa podrá bajar la ficha de su preferencia.
Las fichas de la mesa conforman una cadena donde siempre los valores de dos fichas contiguas deben ser iguales. La cadena tendrá siempre dos extremos que son las posiciones donde se pueden agregar fichas. 
Veamos un ejemplo de cadena:
6-5 5-4 4-4 4-2
se trata de una cadena de longitud 4 (cuatro fichas)
los extremos son las fichas 6-5 y 4-2
Se podrán agregar a la cadena (bajar fichas) con valores 6 o 2 
Cuando no se tengan fichas para sumar a la cadena, se deberá pasar el turno.
Una mano termina cuando suceda una de las siguientes condiciones:
Un jugador bajó su última ficha.
Ningún jugador tiene fichas para bajar.  
Al final de cada mano se realiza la cuenta de puntos de cada jugador sumando la totalidad de los valores (2 por ficha) de las fichas que tenga en su poder al termina la mano.
El juego termina cuando el primer jugador alcance el puntaje convenido. Es frecuente pactar partidas a 100 tantos y, en ese caso, el juego terminará cuando un jugador alcance o supere dicho los 100 puntos perdiendo la partida.
En la mano de un jugador, se llama palo largo al que tenga la mayor cantidad de fichas (incluyendo las que estén en la mesa).
Se llama fallo de un palo cuando un jugador no tiene fichas de ése palo. Por ejemplo si no tenemos ninguna ficha con palo 4, diremos que tenemos un fallo en el palo 4.
Se llama cerrar cuando se coloca la última ficha de un palo en la cadena. Una situación que impide seguir bajando fichas por ese extremo de la cadena.
Se llama ahorcar un doble cuando se han colocado en una cadena todos las fichas de un palo a excepción del palo del doble ahorcado.
 
Consignas.
Diseñar una solución que permita modelar el problema y responder a los siguientes requerimientos.
Jugar una partida completa entre dos jugadores (uno estará controlado por el programa). Las funcionalidades principales son:
Repartir las fichas de cada mano.
Mostrar las fichas que están sobre la mesa conformando una cadena y las que están en poder de cada jugador. Las fichas se deberán mostrar en el formato palo-palo por ejemplo el seis doble se mostrará 6-6
Determinar si una jugada es válida (puede bajarse una ficha o puede pasar).
Determinar el final de una mano (jugador sin fichas o ambos jugadores pasan).
Determinar el puntaje obtenido por cada jugador al final de una ronda indicando el nombre del jugador y los puntos obtenidos.
El jugador controlado por la máquina deberá realizar, cómo mínimo, jugadas válidas (bajar fichas o pasar). 
Con el propósito de analizar el desarrollo del juego se desea conocer:
Si un jugador tiene dobles.
Si se trata de un doble solitario (el jugador no tiene más fichas de ese palo) o acompañado (el jugador tiene por lo menos una ficha del mismo palo.
Los fallos que tenga un jugador en cualquier momento.
Si la cadena está cerrada por algún extremo (o por ambos)
Si, en cualquier momento, existe algún doble ahorcado.

Diagrama de clases y objetos. (1 puntos)
Utilizar nomenclatura UML.
Indicar métodos principales de cada objeto, relaciones entre clases y objetos, jerarquía de clases (cuando se emplee herencia) colecciones previstas durante la implementación.
Código de programa necesario de acuerdo a los requerimientos. (5 puntos)
Se debe realizar en lenguaje Wollok.
Casos de prueba. (4 puntos)
Suficientes para validar el funcionamiento de los métodos principales y de todos los métodos relacionados con el análisis del desarrollo de una partida.  
