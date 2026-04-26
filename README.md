# ⚡ Aegleseeker
Aegleseeker es un buscaminas de consola escrito en C++. Genera un tablero aleatorio, lo muestra en pantalla y te permite revelar casillas y marcar/desmarcar minas hasta ganar o perder.
1. Ejecuta el programa.
2. Selecciona una dificultad.
3. Ingresa las coordenadas de una casilla e indica qué acción realizar.
4. Ganas cuando todas las minas están marcadas y no quedan casillas sin explorar. Si revelas una mina, pierdes.
---
## 💣 Dificultad
La dificultad controla dos cosas: el tamaño del tablero y la probabilidad de aparición de minas en cada casilla.
| Tecla | Dificultad | Tamaño del tablero     | Probabilidad de minas |
|-------|------------|------------------------|-----------------------|
| `E`   | Easy       | 25% – 50% del máximo   | 10% – 15%             |
| `N`   | Normal     | 50% – 75% del máximo   | 15% – 20%             |
| `H`   | Hard       | 75% – 100% del máximo  | 20% – 25%             |
| Otro  | Random     | 25% – 100% del máximo  | 10% – 25%             |
---
## 🎮 Acciones
En cada turno se ingresa la posición `X Y` de una casilla y luego una acción:
| Tecla         | Acción         | Efecto |
|---------------|----------------|--------|
| `1`           | Minar          | Revela la casilla. Si tiene una mina, la partida termina. Si está vacía, se expanden automáticamente las casillas adyacentes sin riesgo. |
| `2`           | Marcar         | Coloca una bandera `X` sobre la casilla. Consume un marcador disponible. |
| `3`           | Desmarcar      | Retira la bandera y devuelve el marcador. |
| `Otro número` | Reseleccionar  | Te regresa a la fase de elección de casilla. |
| Letra         | Rendirse       | Ingresa cualquier letra cuando el juego espere un número para abandonar la partida. |
---
## 📊 Tablero
El tablero tiene dos capas: una interna con los valores reales, y una visible con el estado actual de exploración. Cada casilla puede encontrarse en uno de los siguientes estados:
| Símbolo | Significado |
|---------|-------------|
| `?`     | Sin explorar |
| `X`     | Marcada como mina |
| ` `     | Revelada — Ninguna mina adyacente |
| `1`–`8` | Revelada — Número de minas adyacentes |
| `*`     | Explosión de mina |
---
## 🛠️ Recursos
- 🖥️ **NetBeans** — IDE utilizado para escribir y compilar el proyecto en C++.
