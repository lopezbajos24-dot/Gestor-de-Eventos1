# Diseño del Sistema - Gestor de Eventos

## 1. Estructura del Sistema (Diagrama de Clases)
A continuación, se muestra la estructura principal de los elementos que componen la aplicación:

```mermaid
classDiagram
    class GestorEventos {
        -listaEventos
        -listaUsuarios
        +iniciarMenu()
        +crearEvento(id,nombre,fecha,max)
        +listarEventos()
        +buscarEventoPorNombre(nombre)
        +eliminarEvento(id)
        +crearUsuario(id, nombre, email)
        +listarUsuarios()
        +buscarUsuarioPorNombre(nombre)
        +eliminarUsuario(id)
        +inscribirUsuarioEnEvento(idUsuario, idEvento)
        +cancelarInscripcion(idUsuario, idEvento)
        +mostrarAsistentesEvento(idEvento)
    }

    class Evento {
        -int id
        -String nombre
        -String fecha
        -int maxAsistentes
        -List~Usuario~ asistentes
        +comprobarAforo()
        +anadirAsistente(Usuario)
        +eliminarAsistente(Usuario)
    }

    class Usuario {
        -int id
        -String nombre
        -String email
        +getDetalles()
    }
    %%Relaciones y Cardinalidad 
    GestorEventos "1" --> "*" Evento : gestiona
    GestorEventos "1" --> "*" Usuario : administra
    Evento "*" <--> "*" Usuario : inscripciones
