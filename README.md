# Entrega25

Repositorio del proyecto: [Entrega25](https://github.com/Encina33/Entrega25.git)

## Descripción

Este proyecto implementa tres problemas clásicos de programación utilizando una arquitectura **Modelo-Vista-Controlador (MVC)**. Los tres juegos comparten un objeto base que se adapta a las necesidades específicas de cada problema, como funcionalidad, color y tamaño. Los juegos implementados son:

1. **Torres de Hanói**
2. **Problema de las 8 Reinas**
3. **Problema del Caballo de Ajedrez**

Cada juego está diseñado para ser interactivo y educativo, mostrando soluciones a problemas típicos de programación mediante algoritmos eficientes. Este proyecto busca no solo resolver los problemas, sino también proporcionar una base sólida para comprender los algoritmos y su implementación en un entorno estructurado.

---

## Juegos Implementados

### 1. Torres de Hanói

**Descripción**:  
El objetivo del juego es mover todos los discos de una torre inicial a una torre destino, siguiendo estas reglas:
- Solo se puede mover un disco a la vez.
- Un disco más grande no puede colocarse sobre uno más pequeño.
- Se utilizan tres torres (pilas) para realizar los movimientos.

**Algoritmo**:  
El algoritmo utilizado es **recursivo** y se basa en dividir el problema en subproblemas más pequeños. La fórmula matemática para calcular el número mínimo de movimientos necesarios para resolver el problema es:

\[
T(n) = 2^n - 1
\]

Donde:
- \( T(n) \) es el número mínimo de movimientos.
- \( n \) es el número de discos.

**Pasos del Algoritmo**:
1. Mover \( n-1 \) discos de la torre origen a la torre auxiliar.
2. Mover el disco más grande a la torre destino.
3. Mover los \( n-1 \) discos de la torre auxiliar a la torre destino.

**Discusión Lógica**:  
El problema de las Torres de Hanói es un ejemplo clásico de recursión. Cada llamada recursiva reduce el problema en tamaño hasta llegar al caso base (un solo disco). Este enfoque divide el problema en tres pasos principales, asegurando que las reglas del juego se respeten en cada movimiento.

---

### 2. Problema de las 8 Reinas

**Descripción**:  
El objetivo es colocar 8 reinas en un tablero de ajedrez de 8x8 de manera que ninguna reina pueda atacar a otra. Esto significa que no puede haber dos reinas en la misma fila, columna o diagonal.

**Algoritmo**:  
Se utiliza un enfoque de **backtracking** (vuelta atrás) para encontrar todas las soluciones posibles. El algoritmo verifica todas las combinaciones posibles y retrocede cuando encuentra una posición inválida.

**Pasos del Algoritmo**:
1. Colocar una reina en una fila.
2. Verificar si la posición es válida (no hay conflictos en filas, columnas o diagonales).
3. Si es válida, proceder a la siguiente fila; si no, retroceder y probar otra posición.

**Discusión Lógica**:  
El problema de las 8 Reinas es un ejemplo clásico de búsqueda con restricciones. El algoritmo explora todas las configuraciones posibles del tablero y utiliza la técnica de backtracking para descartar configuraciones inválidas. Esto asegura que se encuentren todas las soluciones posibles de manera eficiente.

**Fórmula Matemática**:  
El número total de soluciones para el problema de las 8 Reinas es 92 (sin considerar simetrías). Este número se obtiene mediante la exploración exhaustiva de todas las configuraciones válidas.

---

### 3. Problema del Caballo de Ajedrez

**Descripción**:  
El objetivo es mover un caballo de ajedrez por un tablero de \( N \times N \) de manera que visite cada casilla exactamente una vez. Este problema también se conoce como el **Problema del Paseo del Caballo**.

**Algoritmo**:  
Se utiliza un enfoque de **backtracking** para encontrar una solución. El algoritmo intenta todos los movimientos posibles del caballo y retrocede si no puede continuar.

**Pasos del Algoritmo**:
1. Comenzar desde una casilla inicial.
2. Mover el caballo según las reglas del ajedrez (en forma de "L").
3. Verificar si la casilla es válida y no ha sido visitada.
4. Continuar hasta que todas las casillas hayan sido visitadas o retroceder si no hay movimientos válidos.

**Discusión Lógica**:  
El problema del Caballo de Ajedrez es un ejemplo de un problema de recorrido en grafos. Cada casilla del tablero puede considerarse un nodo, y los movimientos válidos del caballo representan las aristas. El algoritmo de backtracking explora todas las rutas posibles hasta encontrar una solución válida.

**Fórmula Matemática**:  
El problema no tiene una fórmula cerrada para tableros de tamaño arbitrario, pero para tableros pequeños, se pueden calcular soluciones exactas mediante simulación.

---

## Estructura del Proyecto

El proyecto sigue la arquitectura **Modelo-Vista-Controlador (MVC)**:
- **Modelo**: Contiene la lógica y los datos de cada juego. Por ejemplo, las pilas para las Torres de Hanói o el tablero para los problemas de ajedrez.
- **Vista**: Proporciona la interfaz gráfica o textual para interactuar con el usuario.
- **Controlador**: Gestiona la interacción entre el modelo y la vista, asegurando que las reglas del juego se respeten y que las acciones del usuario se reflejen correctamente.

---

## Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/Encina33/Entrega25.git









# Proyecto: Juegos Clásicos de Programación

Este proyecto implementa tres problemas clásicos de programación utilizando una arquitectura **Modelo-Vista-Controlador (MVC)**. Los juegos disponibles son:

1. **Torres de Hanói**
2. **Problema de las 8 Reinas**
3. **Problema del Caballo de Ajedrez**

---

## **Estructura del Programa**

El programa sigue el patrón **Modelo-Vista-Controlador (MVC)**:
- **Modelo**: Contiene la lógica de los juegos (`TowersOfHanoi`, `EightQueens`, `KnightTour`).
- **Vista**: En este caso, la salida se muestra en la consola.
- **Controlador**: La clase `GameController` gestiona la interacción entre el usuario y los juegos.

---

## **Flujo del Programa**

1. **Inicio**:
   - El programa comienza en la clase `Main`, que llama al método `start()` del `GameController`.

2. **Menú**:
   - El controlador muestra un menú en la consola con las opciones de los juegos:
     ```
     Selecciona un juego:
     1. Torres de Hanói
     2. Problema de las 8 Reinas
     3. Problema del Caballo de Ajedrez
     ```

3. **Selección del Juego**:
   - Según la elección del usuario, el controlador crea una instancia del juego correspondiente.

4. **Ejecución del Juego**:
   - El método `play()` del juego seleccionado ejecuta la lógica específica y muestra los resultados en la consola.

---

## **Explicación de las Clases**

### **1. Clase `GameController`**
La clase `GameController` es el controlador del programa. Su función principal es gestionar la interacción entre el usuario y los juegos. 

#### **Método `start()`**
- **Mostrar el Menú**: Muestra las opciones de los juegos disponibles.
- **Leer la Elección del Usuario**: Utiliza un objeto `Scanner` para leer la entrada del usuario desde la consola.
- **Seleccionar el Juego**: Usa un `switch` para determinar qué juego ejecutar según la elección del usuario.
- **Ejecutar el Juego**: Llama al método `play()` del juego seleccionado, que contiene la lógica específica de cada juego.

### **2. Clase `GameObject`**
- Es una clase abstracta que define el método `play()`:
  ```java
  public abstract class GameObject {
      public abstract void play();
  }



   


Entrega25/
├── src/

│   ├── model/

│   │   ├── GameObject.java

│   │   ├── TowersOfHanoi.java

│   │   ├── EightQueens.java

│   │   └── KnightTour.java

│   ├── view/

│   │   ├── GameView.java

│   │   ├── TowersOfHanoiView.java

│   │   ├── EightQueensView.java

│   │   └── KnightTourView.java

│   ├── controller/

│   │   ├── GameController.java

│   │   ├── TowersOfHanoiController.java

│   │   ├── EightQueensController.java

│   │   └── KnightTourController.java

│   └── Main.java





   
