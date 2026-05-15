# Documento de Requisitos: Gestor de Eventos

## 1. Descripción general de la aplicación
"Gestor de Eventos" es una aplicación de consola diseñada para administrar la organización de eventos, el registro de usuarios y el control de aforos. Permite vincular a los asistentes con los eventos deseados de forma rápida y sin superar el número máximo de plazas permitidas.

## 2. Funcionalidades
El sistema cuenta con tres bloques principales de funciones:

### Gestión de Eventos
* Crear un evento nuevo (requiere ID, Nombre, Fecha y Número máximo de asistentes).
* Listar todos los eventos registrados.
* Buscar un evento concreto por su nombre.
* Eliminar un evento del sistema.

### Gestión de Usuarios
* Crear un usuario nuevo (requiere ID, Nombre y Email).
* Listar todos los usuarios.
* Buscar un usuario por su nombre.
* Eliminar un usuario.

### Gestión de Inscripciones
* Inscribir a un usuario en un evento.
* Cancelar la inscripción de un usuario.
* Mostrar la lista completa de asistentes de un evento.

## 3. Tipos de usuarios
* *Usuario Administrador:* Es el único tipo de usuario del sistema. Operará la consola y tendrá permisos totales para crear, modificar, borrar y gestionar tanto los eventos como los asistentes y las inscripciones.

## 4. Casos de uso principales
* *UC1 - Registrar nuevo evento:* El administrador introduce los datos de un evento (ej. ID: 01, Nombre: "Concierto", Fecha: "20/12/2026", Aforo: 100). El sistema guarda el evento.
* *UC2 - Inscribir usuario con éxito:* El administrador selecciona un usuario y un evento. Si el evento tiene plazas libres, el sistema registra la inscripción.
* *UC3 - Error por aforo completo:* El administrador intenta inscribir a un usuario en un evento que ya ha alcanzado su "Número máximo de asistentes". El sistema bloquea la acción y muestra un error.
