# Diseño del Sistema - Gestor de Eventos

## 1. Estructura del Sistema (Diagrama de Clases)
A continuación, se muestra la estructura principal de los elementos que componen la aplicación:

```mermaid
classDiagram
    class GestorEventos {
        -listaEventos
        -listaUsuarios
        +iniciarMenu()
        +gestionarInscripcion()
    }

    class Evento {
        -int id
        -String nombre
        -String fecha
        -int maxAsistentes
        -List~Usuario~ asistentes
        +comprobarAforo()
        +anadirAsistente()
        +eliminarAsistente()
    }

    class Usuario {
        -int id
        -String nombre
        -String email
        -List~Evento~ misInscripciones
    }

    GestorEventos "1" --> "*" Evento : gestiona
    GestorEventos "1" --> "*" Usuario : administra
    Evento "*" <--> "*" Usuario : inscripciones
