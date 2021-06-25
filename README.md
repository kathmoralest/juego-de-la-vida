Introducción
¿Cuáles son las leyes de la vida? ¿La complejidad de la vida a nuestro alrededor se debe a un gran conjunto de leyes sofisticadas o será que un número pequeño de leyes sencillas puede generar patrones de vida complejos? 

Para intentar responder estas preguntas, en 1970 el matemático John Horton Conway creó un juego de la vida basado en tres reglas sencillas: nacimiento, muerte y supervivencia.

El juego se desarrolla sobre una grilla cuadriculada. Cada cuadrado de la grilla representa un espacio que puede estar vacío u ocupado por una célula (en este caso, el casillero está marcado). A partir de una posición inicial, el juego evoluciona de acuerdo a las siguientes reglas:

Si un cuadrado de la grilla está rodeado por tres células vecinas entonces se crea vida, agregándose una célula en ese sitio.
Si una célula tiene menos de 2 células vecinas, muere por aislamiento y la casilla de la grilla correspondiente queda vacía, y si tiene más de 3 células vecinas, muere por sofocación y también se libera el cuadrado de la grilla que le correspondía.
Una célula que tiene exactamente dos o tres vecinas sobrevive una instancia más en el juego.
Sorprendentemente, mediante estas reglas tan elementales, al dejar evolucionar el juego para diferentes posiciones iniciales, se desarrollan patrones verdaderamente complejos, algunos de ellos estáticos y otros que parecen adquirir movimiento. Más aún, en algunos casos, estos patrones pueden interactuar entre ellos.

COMENTARIOS para evaluar Principios de SOLID

Single Responsability Principle
El tablero pertenece a una misma clase principal.
Solución:
Se debe separar las clases tablero y célula para que los métodos de tablero solo le pertenezcan a la clase tablero.

Open-Closed Principle
No cumple OCP porque no se puede trabajar en más de un tablero y su información es única y vulnerable a modificación.

Solución:
Añadir la clase calculoTablero para que el tablero quede abierto a extensión y se ejecute independientemente de los estados en que se encuentren las celdas.

Interface Segregation Principle
La  interfaz no contiene métodos específicos para mostrar en pantalla las acciones del usuario y que este sepa qué cosas no puede modificar.

Solución:
Crear una interfaz Vida que utilice los métodos mostrarCelulasAdaptadas y mostrarCelulasPeligro.
