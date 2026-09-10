# Trabajo Práctico de Laboratorio N°2: Interfaz Gráfica de Usuario (GUI) y GitHub Fork

**Materia:** Programación / Laboratorio de Computación  
**Estudiante:** Federico Guevara  
**Repositorio Fork:** [https://github.com/federico-guevara-dev/Snake-Game](https://github.com/federico-guevara-dev/Snake-Game)  
**Repositorio Original:** [https://github.com/Degef/Snake-Game](https://github.com/Degef/Snake-Game)  

---

## 📖 Descripción del Proyecto
El objetivo del trabajo práctico consiste en realizar una bifurcación (fork) de un proyecto público de Python con interfaz gráfica de usuario (GUI), incorporar modificaciones estructurales y funcionales a gusto personal cumpliendo consignas técnicas específicas, y generar la documentación correspondiente junto al archivo ejecutable final.

Para este laboratorio se seleccionó el clásico juego de la viborita (**Snake Game**), implementado originalmente con la biblioteca nativa **Tkinter**, expandiéndolo para permitir el registro y notificación de puntajes por correo electrónico.

---

## 🛠️ Modificaciones y Añadidos a la Interfaz Gráfica

Conforme a los requerimientos del Trabajo Práctico, se rediseñó la ventana principal y se sumaron los siguientes componentes:

1. **Reestructuración del Layout (División en dos sectores)**:
   * **Área de Juego (`Canvas`)**: Se empaquetó hacia el sector izquierdo (`side=LEFT`), conservando las dimensiones originales de 700x700 px y el fondo negro.
   * **Panel Lateral de Control (`Frame`)**: Se construyó un panel lateral a la derecha (`side=RIGHT, fill=Y`) de 280 px de ancho con estética oscura (`#2c3e50`) para nuclear las interacciones del laboratorio sin entorpecer la jugabilidad.
   * **Reubicación de Elementos**: El marcador de puntajes (`Score`) se trasladó al panel lateral y el botón de inicio de partida (`Start Game`) fue recalibrado sobre el eje horizontal (`relx=0.36`) para centrarse con respecto al lienzo jugable.

2. **Menú de Selección de Destinatarios (`OptionMenu`) - Requisito 4.c**:
   * Se incorporó una lista desplegable con las direcciones de los docentes del área:
     * `fjcoronati@gmail.com`
     * `mfedullo@gmail.com`
   * Permite escoger el destinatario del reporte con un clic.

3. **Entrada Manual de Correo (`Entry`) - Requisito 4.c**:
   * Se integró una caja de entrada de texto manual justo debajo del menú desplegable para que el usuario pueda escribir cualquier otra dirección alternativa en caso de no seleccionarla del listado.

4. **Correcciones de Código**:
   * Se envolvieron los cálculos de coordenadas de la comida dentro de `int()` en la clase `Food` (`int((GAME_WIDTH / SPACE_SIZE) - 1)`), subsanando problemas de tipos de datos en `random.randint` presentes en versiones actualizadas de Python.


---

## 🚀 Historial de Commits Realizados

En cumplimiento del mínimo de 4 commits descriptivos en el repositorio:

1. `Modificacion de la estructura de la interfaz agregando panel lateral`: Separación del lienzo de juego a la izquierda y creación del contenedor `panel_lateral`.
2. `Agregado OptionMenu de correos y entrada de texto manual en panel lateral`: Incorporación de `OptionMenu` con correos docentes (`fjcoronati@gmail.com`, `mfedullo@gmail.com`) y caja `Entry`.
3. `Implementacion de envio por SMTP y boton de despacho`: Lógica de conexión con servidor de correo para remitir el puntaje obtenido al perder.
4. `Inclusion de identidad visual e informe final`: Ajustes estéticos con imagen personalizada y documentación del proyecto.

---

## 📦 Instrucciones de Ejecución

### Desde Código Fuente:
1. Clonar el repositorio localmente:
   ```bash
   git clone https://github.com/federico-guevara-dev/Snake-Game.git
   cd Snake-Game
   ```
2. Ejecutar el script:
   ```bash
   python Snake.py
   ```

### Desde el Ejecutable (.exe):
* El binario compilado se encuentra dentro del directorio `/output` listo para ser ejecutado en entornos Windows sin requerir instalación previa de Python.
