# Canicas Game Simulator

Pequeña simulación de un juego cooperativo con canicas.

## Instrucciones del juego

### Preparación

Se colocan las canicas en una cesta con un total de canicas igual al número de jugadores multiplicado por un factor entre 1,2 y 1,5. La escasez de canicas determina lo rápido que acaba.

Los jugadores pasan por la cesta y recogen entre 0 y 3 canicas, las que cada uno quiera sin saber el objetivo del juego. Y pasan a la sala de intercambios.

### Objetivo

El objetivo de cada ronda es no ser eliminado para poder pasar a la siguiente ronda. Para ello se debe conseguir poseer el número de canicas que indica el dado, ya sea individualmente o sumando con otros jugadores.

### Reglas

* Los jugadores no pueden tirar o esconder las canicas.
* Solo es admisible modificar el número de canicas que posee un jugador intercambiando canicas con otros jugadores.
* Todos los jugadores parte de un equipo deben aportar al menos una canica al equipo, los equipos pueden ser de un único jugador.
* Los equipos que logren el número necesario de canicas abandonan la sala de intercambios con sus canicas, con las que volverán a entrar en la sala de intercambios para la siguiente ronda.
* Los jugadores que queden en la sala de intercambio pasado un tiempo sin lograr el número necesario son eliminados y retiran del juego las canicas que posean al salir de la sala.

### Ronda

La ronda empieza lanzando uno o dos dados para determinar el número objetivo a conseguir por los equipos en dicha ronda y termina eliminando a los jugadores que no lo consiguen y lanzando un dado para eliminar todas las canicas de un color de entre los jugadores que quedan.

### Final

El juego acaba cuando en una ronda NO se elimina a nadie (todos sobreviven), o en la sexta ronda (ya que se eliminaría el último color de cara a la ronda 7). También puede acabar en la ronda en la que sobrevivan un número muy reducido de jugadores y de entre ellos ganan aquellos que posean el mayor número de canicas en su poder.


## IA Prompt Utilizado

Eres un experto desarrollador en HTML5 JavaScript y CSS y quiero que hagas un HTML de una simulación de un juego participativo con las siguientes reglas básicas.

Para iniciar el juego los jugadores eligen a su criterio un número de canicas entre 0 y 3 de un cesto de canicas de varios colores. 

En cada ronda se lanza un dado y los jugadores deben formar equipos de entre 1 y 6 miembros de forma que sumen entre todos el número exacto de canicas indicado por el dado. Los jugadores pueden hacer intercambios (entregando o recibiendo canicas de otros usuarios) con objeto de conseguir formar un equipo con el número exacto de canicas. No está permitido esconder, destruir o tirar canicas, solo es posible modificar el número de canicas que posee un jugador usando intercambios con otros jugadores. Sólo pueden formar parte de un equipo jugadores con una o más canicas, y los jugadores durante las rondas pueden acumular un número de canicas superior al máximo inicial de tres que tienen al iniciar el juego.

Los jugadores que no logran formar parte de un equipo con el número de canicas requerido por el dado son eliminados del juego (desapareciendo del juego las canicas que posean), y sobreviven aquellos jugadores que sí lo logran. Una vez acaba la ronda se eliminan todas las canicas de un color seleccionado al azar (se puede forzar a que sea de los colores que quedan vivos o dejar al azar que haya una posibilidad de no eliminar ningún color de los restantes). Los jugadores supervivientes que posean canicas del color eliminado si lo hay las pierden pasando a la siguiente ronda sin ellas, sin importar el número de canicas que mantengan en su poder (incluso si no les queda ninguna). 

El juego acaba cuando se juega la última ronda en la que todas las canicas serían del mismo color y ganan los jugadores no eliminados en esa ronda los que logran sobrevivir a todas las rondas. El juego también acaba si quedan un número reducido de supervivientes y ganan los que tienen más canicas en su poder.

El HTML debe permitir probar simulaciones del juego ajustando diferentes valores: Número de jugadores iniciales (por defecto 50), Número de colores de canicas (6 por defecto), Número de canicas por color (determinará el total de canicas, 14 por defecto), Máximo de canicas con las que puede iniciar el juego un jugador, (3, entre 0 y 3), Número de datos para seleccionar el número a conseguir (1 ó 2, por defecto 1), Número de simulaciones a ejecutar (200 por defecto), Estrategia de intercambios o agrupamiento (puede ser maximizar el número de supervivientes, o aleatorio sin importar cuántos sobreviven, o humana favoreciendo intercambios simples para formar parejas o trios donde no sea necesario ceder canicas), Criterio de eliminación de color en cada ronda (aleatorio de entre los restantes (siempre se elimina un color presente en cada ronda), el menos abundante entre las canicas restantes, el más abundante entre las canicas restantes, no eliminar nunca ningún color, aleatorio pudiendo no eliminar ningún color...), debe incluir gráficos con histograma de jugadores supervivientes al finalizar todas las rondas, promedio de jugadores eliminados y supervivientes por ronda y debe permitir un modo de ejecución de una partida individual con el detalle de lo sucedido en cada ronda con una visualización ronda por ronda que indique, las canicas que hay en juego en la ronda, los jugadores que sobreviven (y cómo se agrupan en equipos o no para entregar el número exacto de canicas requeridas, cuántas canicas aporta cada uno), los eliminados y las canicas que tiene cada uno, el color eliminado (y el número de canicas eliminadas).

Cuando se aplica el criterio de no eliminar color el juego se puede extender por un número de rondas superior al de colores, en ese caso el juego acaba cuando en una ronda se eliminan a todos los jugadores restantes y los ganadores son todos los jugadores que hayan participado en esa última ronda que más canicas posean.
