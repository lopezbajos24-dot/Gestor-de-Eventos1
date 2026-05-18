classDiagram
    class GestorEventos {
        -List~Evento~ listaEventos
        -List~Usuario~ listaUsuarios
        +iniciarMenu()
        +crearEvento(id, nombre, fecha, max)
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
        +bool comprobarAforo()
        +anadirAsistente(Usuario)
        +quitarAsistente(Usuario)
    }

    class Usuario {
        -int id
        -String nombre
        -String email
        +getDetalles()
    }

    %% Relaciones y Cardinalidades
    GestorEventos "1" --> "*" Evento : gestiona
    GestorEventos "1" --> "*" Usuario : administra
    Evento "0..*" <--> "0..*" Usuario : inscripciones
