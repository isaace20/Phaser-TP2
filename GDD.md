# GDD — Explorador TP2

**Versión:** 0.1  
**Motor:** Phaser 3  
**Plataforma:** Navegador web  
**Género:** Aventura  
**Modo de juego:** Un jugador local  
**Público objetivo:** Niños  
**Estilo visual:** Pixel Art

---

## 1. Concepto

El jugador controla a un explorador que debe recorrer distintos laberintos, recolectar objetos y encontrar la salida para avanzar a través de una antigua mazmorra.

## 2. Premisa

Un joven explorador, cuyo sueño es convertirse en el mejor explorador del mundo, decide aventurarse en una legendaria y peligrosa mazmorra para demostrar su valentía y conseguir los tesoros que allí se ocultan.

Durante su aventura deberá orientarse dentro de los laberintos, recolectar objetos y evitar los peligros que custodian la mazmorra.

## 3. Objetivo del juego

Completar tres niveles de laberintos. Para avanzar al siguiente nivel, el jugador deberá recolectar al menos cinco objetos y alcanzar el punto de llegada.

Al finalizar el tercer nivel, se mostrará una escena de victoria con el puntaje acumulado.

## 4. Descripción general

Explorador TP2 es un videojuego de aventura desarrollado con Phaser 3. Los laberintos se construyen mediante mapas de mosaicos (*tilemaps*), que definen los caminos y las paredes por los que puede desplazarse el personaje.

El jugador deberá explorar cada mapa, recoger objetos y encontrar la salida. La dificultad principal consiste en orientarse y recorrer el escenario sin quedar bloqueado por las paredes o los posibles enemigos.

El juego contará con tres niveles. El tercero tendrá dimensiones superiores a las de la pantalla y utilizará una cámara que seguirá al personaje durante la exploración.

## 5. Mecánicas principales

### 5.1 Movimiento del personaje

El jugador podrá desplazarse por el laberinto mediante las flechas del teclado. Las paredes impedirán el paso por las zonas bloqueadas.

### 5.2 Recolección de objetos

Los objetos recolectables estarán distribuidos por el mapa. Al entrar en contacto con uno, el personaje lo recogerá y se actualizarán los contadores correspondientes.

### 5.3 Condición de llegada

Cada nivel tendrá un punto de llegada. Al entrar en contacto con él, el juego comprobará cuántos objetos se han recolectado en el nivel actual.

- Si el jugador recolectó menos de cinco objetos, no podrá completar el nivel.
- Si recolectó cinco objetos o más, podrá avanzar al siguiente nivel.

### 5.4 Puntaje

El juego mostrará el puntaje durante la partida. Los puntos obtenidos se conservarán al cambiar de nivel y se acumularán hasta finalizar el juego.

La cantidad de puntos otorgada por cada objeto se definirá durante la implementación.

### 5.5 Progresión de niveles

La partida estará compuesta por tres niveles diferentes.

- **Nivel 1:** Laberinto inicial para familiarizarse con el movimiento y la recolección.
- **Nivel 2:** Nuevo mapa que continúa la exploración de la mazmorra.
- **Nivel 3:** Laberinto de dimensiones superiores a la pantalla, con desplazamiento de cámara.

Al completar un nivel, se cargará el mapa siguiente y se conservará el puntaje acumulado.

### 5.6 Cámara

En el tercer nivel se implementará una cámara que seguirá al personaje y permitirá explorar las zonas del mapa que no estén visibles inicialmente en pantalla.

## 6. Enemigos (opcional)

Se podrán incorporar enemigos que representen un peligro durante la exploración.

Los enemigos podrán tener dos patrones de movimiento:

- **Horizontal:** desplazamiento de izquierda a derecha.
- **Vertical:** desplazamiento de arriba hacia abajo.

El patrón de movimiento dependerá de la ubicación inicial del enemigo dentro del mapa.

Esta mecánica es opcional y se implementará únicamente después de completar los requisitos obligatorios.

## 7. Interfaz

La interfaz mostrará:

- **Contador de objetos:** cantidad de objetos recolectados en el nivel actual.
- **Puntaje acumulado:** total de puntos obtenidos durante la partida.
- **Escena de victoria:** mensaje que indica que se completaron los tres niveles y muestra el puntaje final.

Si el jugador intenta alcanzar la salida sin cumplir la condición de recolección, se deberá informar que necesita recoger más objetos.

## 8. Controles

| Tecla | Acción |
|---|---|
| Flecha arriba | Mover hacia arriba |
| Flecha abajo | Mover hacia abajo |
| Flecha izquierda | Mover hacia la izquierda |
| Flecha derecha | Mover hacia la derecha |

## 9. Elementos del juego

- **Personaje:** explorador controlado por el jugador.
- **Paredes:** obstáculos sólidos que delimitan el recorrido.
- **Caminos:** espacios transitables del laberinto.
- **Objetos recolectables:** elementos que permiten cumplir la condición de llegada.
- **Punto de llegada:** destino que permite avanzar de nivel.
- **Enemigos (opcional):** obstáculos móviles que el jugador deberá evitar.
- **Interfaz:** indicadores de recolección y puntaje.

## 10. Requisitos técnicos

- Phaser 3.
- JavaScript con módulos ES.
- Mapas de mosaicos (*tilemaps*) para construir los laberintos.
- Colisiones entre el personaje y las paredes.
- Detección de contacto entre el personaje, los objetos y la llegada.
- Gestión de escenas o mapas para la progresión entre niveles.
- Conservación del puntaje entre niveles.
- Cámara de seguimiento para el tercer nivel.

## 11. Condiciones de victoria

El jugador gana al completar el tercer nivel, habiendo cumplido la condición de recolectar al menos cinco objetos en cada nivel.

La escena final mostrará un mensaje de victoria y el puntaje total acumulado.

## 12. Alcance del proyecto

El objetivo principal es cumplir los requisitos obligatorios de la Propuesta 2 de la actividad de Phaser 3.

El desarrollo se priorizará en el siguiente orden:

1. Verificar el funcionamiento del personaje, el mapa y las colisiones.
2. Implementar la recolección y la validación de la llegada.
3. Crear los tres niveles y sus transiciones.
4. Conservar el puntaje acumulado entre niveles.
5. Implementar la cámara del tercer nivel.
6. Incorporar enemigos opcionales y mejoras visuales si el tiempo lo permite.
