# Brick-Car-Grupo1
## Nombres de integrantes
-Javier Isidro Durán Villanueva
-Eduardo Benjamin Sanchez Mejia
-Diego Antonio Guerrero castellanos
-Cesar Ulises Campos
-Ariel Urias Urias

## Descripción del Proyecto

Brick-Car es un videojuego desarrollado en Java que simula una experiencia de conducción en carretera, donde el jugador controla un automóvil que debe esquivar obstáculos mientras avanza continuamente.

El objetivo principal del juego es sobrevivir el mayor tiempo posible evitando colisiones con otros vehículos que aparecen en la vía. A medida que el juego progresa, la dificultad aumenta, lo que exige mayor rapidez de reacción y precisión por parte del jugador.

El sistema del juego incluye mecánicas como detección de colisiones, control de vidas, movimiento constante del entorno, lo que genera una sensación dinámica de desplazamiento, se ha implementado el reposicionamiento del vehículo tras un impacto, mejorando la experiencia del usuario. El jugador cuenta con un número limitado de vidas en este caso que es una, y cada colisión reduce este contador. La lógica implementada, el vehículo puede reiniciarse en una posición centrica para continuar la partida hasta que choquemos, momento en el cual se muestra una pantalla de "Game Over".

Este proyecto fue desarrollado aplicando conceptos fundamentales de la programación orientada a objetos, tales como encapsulamiento, modularidad y separación de responsabilidades mediante el uso de controladores, modelos y vistas. También se hace uso de herramientas gráficas de Java como JPanel para la representación visual del juego.

## Características principales

- Movimiento del vehículo controlado por el jugador
- Generación de obstáculos dinámicos
- Sistema de colisiones
- Contador de vidas
- Incremento progresivo de dificultad
- incremento de velocidad a medida avance
- Interfaz gráfica basada en Java Swing

## Tecnologías utilizadas
- Java
- Java Swing (JPanel, Graphics)
- Programación Orientada a Objetos (POO)

## Objetivo del juego
El objetivo es simple y el cual es sobrevivir el mayor tiempo posible evitando chocar con otros autos y lograr la mayor puntuación posible.


# Javier Durán
## Vida extra cuando el vehiculo choque 
En el juego se implementó un sistema de vidas para evitar que el jugador pierda inmediatamente al primer choque y así mejorar la experiencia de juego,el jugador inicia con 2 vidas (`vidas = 2`). Cada vez que ocurre una colisión con un obstáculo, se reduce una vida: vidas--;

Esto permite que el jugador tenga una oportunidad adicional para continuar jugando después de cometer un error, cuando el jugador choca y aún le queda al menos una vida, el juego no termina. En lugar de eso:

- Se muestra cuántas vidas le quedan
- El carro se reposiciona en un carril seguro
- Se eliminan los obstáculos actuales para evitar choques inmediatos
- Se activa una pequeña invulnerabilidad temporal

Esto se hizo para darle al jugador un momento de recuperación y evitar que pierda otra vida de forma instantánea, sin embargo, cuando las vidas llegan a ser menores a 1, el juego termina (Game Over), ya que el jugador ha agotado todas sus oportunidades , el sistema de vidas se implementó para hacer el juego más justo, menos frustrante y permitir que el jugador pueda continuar después de un error.
