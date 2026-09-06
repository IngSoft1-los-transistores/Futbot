# **ALCANCE DEL PROYECTO**

El objetivo principal del proyecto es desarrollar un juego de fútbol web multijugador en donde los usuarios pueden crear sus clubes, jugadores (y sus comportamientos) y ligas para jugar entre clubes. Habrá un sistema de ranking global y a parte partidos amistosos que no contarán para el puntaje del ranking, las ligas pueden ser tanto públicas como privadas pero estas últimas no contarán para el puntaje tampoco.

Para lograr esto, primeramente el sistema identifica al usuario autenticado como un único club. El sistema incluirá un buscador de liga por nombre y un buscador de partidos por id, por lo cual no habrá friend list, el sistema contará con un fixture y un ranking global, por lo que tendrá sistema de registro de usuario obligatorio. una vez un partido amistoso o liga haya sido creado, la cantidad de usuarios mínima/máxima (definidas por el club creador de la liga) sea alcanzada  y él/los otros usuarios en la sala den listo o transcurra un tiempo determinado (30seg), el creador de la sala podrá iniciar el amistoso/liga, a partir de que se inicie, ningún usuario que participe en la sala podrá abandonarla, en caso de abandono, el usuario simplemente no interactuara con el juego manteniendo los últimos cambios. Al finalizar un partido se mostrará los resultados del mismo, y al finalizar una liga se mostrará el fixture de la misma, tras esto la sala se cierra y se deberá crear una nueva para poder jugar nuevamente. 


En cuanto a las mecánicas de juego:
- Todo usuario deberá tener una cuenta creada para poder jugar y la creación de sus jugadores requerirá distribuir exactamente 300 puntos entre los atributos PACSS, los cuales son power (fuerza de pateo), agility (tiempo para volver a patear), control (distancia para el control con la pelota), speed (velocidad y aceleración) y strength (imposición a los choques).
- Al entrar a una liga o partido deberá seleccionar 6 jugadores (3 titulares y 3 suplentes) a los cuales les tendrá que asignar un comportamiento programado previamente en código Python.
- Las ligas requieren de un mínimo de 3 usuarios y pueden tener un máximo de 30, al momento de crearla se le pedirá contraseña al creador y si este deja el campo vacío será una liga pública.
- Todo jugador deberá tener una cuenta creada y logueada para poder jugar .
- Una vez creada la liga y que todos sus cupos hayan sido ocupados, el creador podrá dar a inicio si todos los participantes tienen el estado de listo.
- Los partidos se elegirán de forma aleatoria y se jugará una cantidad de partidos que se asegure que todos jueguen contra todos y se puede jugar un máximo de una vez contra cada rival.
- El partido estará separado en 3 tiempos (un medio tiempo y dos pausas de hidratación en cada mitad del medio tiempo).
- Al empezar el partido el usuario debe elegir la posición para cada uno de sus jugadores.
Durante el partido el usuario puede hacer cambios de jugadores que impactaran en las pausas del partido.
Se puede cambiar el comportamiento asignado a cada jugador lo cual tiene un impacto en el próximo tick.

En cuanto a requerimientos no funcionales el proyecto se centrará en mostrar partidos en 2D de forma fluida y en tiempo real, principalmente computado o calculado en el servidor y que sea accesible desde cualquier navegador. El sistema se construirá obligatoriamente bajo una arquitectura con backend en FastAPI y frontend en React, respetando la prohibición estricta de utilizar técnicas de polling para la comunicación cliente-servidor.

Que NO incluirá el proyecto:
No habrá friend list, no se incluirá un editor de código IDE python, no habrá animaciones 3D, no habrá persistencia de sesión
