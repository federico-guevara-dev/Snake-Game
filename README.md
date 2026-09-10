# Trabajo Práctico de Laboratorio N°2: Snake Game con GUI y Envío de Correos

Este proyecto es una bifurcación (fork) del repositorio de [Snake-Game](https://github.com/Degef/Snake-Game). El objetivo principal del laboratorio consiste en tomar una aplicación con interfaz gráfica existente en Python (Tkinter), adaptarla con nuevos requerimientos de diseño funcional y preparar el entorno para la posterior exportación a ejecutable.

---

## 📌 Modificaciones Realizadas en la Versión Inicial (Commit 1)

En esta primera etapa se intervino la estructura base del juego sin alterar la lógica de movimiento ni el sistema de colisiones de la viborita:

1. **Reestructuración del Layout de la Interfaz (GUI)**:
   * **Separación de áreas**: El juego original renderizaba únicamente un `Canvas` centrado. En esta modificación se dividió la ventana principal en dos columnas.
   * **Área de juego (`Canvas`)**: Se configuró con empaquetado a la izquierda (`side=LEFT`) manteniendo la resolución clásica de 700x700 px.
   * **Panel Lateral de Control (`panel_lateral`)**: Se incorporó un contenedor `Frame` vertical a la derecha (`side=RIGHT, fill=Y`) de 280 px de ancho con un fondo contrastante `#2c3e50`.

2. **Reubicación de Componentes**:
   * El marcador de puntaje (`label`), que antes flotaba en la parte superior general de la ventana, se reubicó de manera fija dentro del nuevo panel lateral derecho.
   * El botón de inicio (`Start Game`) se reajustó proporcionalmente sobre el eje horizontal para centrarse en el área visual del lienzo de juego y no en el ancho total de la ventana combinada.

3. **Correcciones de Código y Tipado**:
   * Se envolvieron los cálculos de posición de la comida dentro de `int()` en la función `Food.__init__` para evitar advertencias de valores flotantes en versiones recientes de Tkinter/Python al calcular `random.randint()`.

---

## 🎯 Próximas Implementaciones Planificadas
* **Menú Desplegable (`OptionMenu`)**: Selección rápida de correos electrónicos de docentes y compañeros, sumado a un campo `Entry` para entrada manual.
* **Integración de Identidad Visual**: Inclusión de logotipo/imagen personalizada en la barra lateral.
* **Módulo SMTP**: Envío automatizado de puntajes por correo electrónico al finalizar la partida.
* **Generación de Ejecutable**: Compilación a `.exe` en carpeta `/output` mediante `auto-py-to-exe`.

---

## 🚀 Instrucciones de Ejecución Local

1. Clonar el fork del repositorio:
   ```bash
   git clone https://github.com/federico-guevara-dev/Snake-Game.git
   cd Snake-Game
   ```
2. Ejecutar el script principal:
   ```bash
   python Snake.py
   ```
