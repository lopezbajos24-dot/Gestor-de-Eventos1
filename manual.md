# Manual de Usuario: Gestor de Eventos

Este manual describe el funcionamiento de la aplicación **Gestor de Eventos** desde la perspectiva del usuario final. Explica cómo navegar por el menú interactivo de la consola y cómo realizar las acciones de gestión de eventos, usuarios e inscripciones.

---

## 1. Cómo usar la aplicación

La aplicación se ejecuta a través de la consola de comandos. El sistema funciona mediante un ciclo continuo que muestra un menú de opciones numeradas. 

Para interactuar con la aplicación:
1. **Visualizar el menú:** Seleccione mentalmente la acción que desea realizar.
2. **Introducir opción:** Escriba el número de la opción correspondiente en la consola y pulse `Intro`.
3. **Completar datos:** Si la opción requiere información (como un nombre, ID o email), la aplicación le irá solicitando los datos uno a uno por pantalla.
4. **Confirmación:** El sistema mostrará un mensaje indicando si la operación se realizó con éxito o si ocurrió algún error (por ejemplo, aforo completo o ID duplicado).

---

## 2. Menú Principal

Al iniciar el programa, se desplegará la interfaz gráfica textual en la terminal. El menú está dividido en bloques temáticos para facilitar su uso:

```text
==================================================
                GESTOR DE EVENTOS
==================================================
 [MÓDULO DE EVENTOS]
   1. Crear evento
   2. Listar eventos
   3. Buscar evento por nombre
   4. Eliminar evento
 ------------------------------------------------
 [MÓDULO DE USUARIOS]
   5. Crear usuario
   6. Listar usuarios
   7. Buscar usuario
   8. Eliminar usuario
 ------------------------------------------------
 [MÓDULO DE INSCRIPCIONES]
   9. Inscribir usuario en evento
  10. Cancelar inscripción
  11. Mostrar asistentes de un evento
 ------------------------------------------------
   0. Salir de la aplicación
==================================================
Seleccione una opción (0-11): _
