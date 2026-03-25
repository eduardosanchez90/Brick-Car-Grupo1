# Aporte de Diego Antonio Guerrero Castellanos

## Descripción
Mi aporte al proyecto consistió en mejorar la experiencia del jugador al momento de perder, agregando un sistema de reinicio del juego y mostrando la distancia recorrida.

## Funcionalidades implementadas

###  Sistema de reinicio con tecla R
Se implementó la opción de reiniciar el juego presionando la tecla **R** después de que el jugador pierde.

Esto permite que el usuario no tenga que cerrar y volver a ejecutar el programa, haciendo el juego más dinámico y fácil de volver a intentar.

if (e.getKeyCode() == KeyEvent.VK_R) ctrl.resetGame();.

funcion de **R**

   public void resetGame() {
 
    // Reiniciar estado
    state = new modelGameState();

    // Reiniciar jugador
    player = new modelPlayerCar();

    // Limpiar obstáculos
    obstacles.clear();

    // Reiniciar contador
    spawnTick = 0;

    // Reiniciar tiempo
    timer.stop();
    timer = new Timer(16, e -> tick());
    timer.start();

    panel.repaint();
###  Mostrar distancia recorrida (Game Over)
Se agregó un sistema que calcula y muestra la distancia total recorrida por el jugador al momento de perder.

Esta distancia se muestra en la pantalla de **Game Over**, permitiendo al jugador ver su desempeño en cada partida.

private void drawGameOver(Graphics g) {

        g.setColor(new Color(0,0,0,160));
        
        g.fillRect(0,0,W,H);
        
        g.setColor(Color.WHITE);
        
        g.setFont(new Font("Arial", Font.BOLD, 30));
        
        g.drawString("GAME OVER :)", 100, 300);
        
         g.setFont(new Font("Arial", Font.PLAIN, 20));
    
    g.drawString("Presiona R para reiniciar crack ", 80, 500);
    
     g.drawString("Distancia: " + ctrl.getState().getDistance(), 130, 400);
    }.

## Funcionamiento

- Mientras el juego está activo, se va acumulando la distancia recorrida.
- Al perder (cuando las vidas llegan a 0), se muestra:
  - Mensaje de **Game Over**
  - Distancia total recorrida
- El jugador puede presionar la tecla **R** para reiniciar:
  - Se reinicia la distancia
  - Se restablecen las variables del juego
  - El jugador vuelve a iniciar desde el comienzo

## Objetivo
Estas mejoras se realizaron con el objetivo de hacer el juego más interactivo, brindar retroalimentación al jugador y permitir múltiples intentos sin necesidad de reiniciar manualmente el programa.
