classDiagram
    class GestorEventos {
        -List~Evento~ listaEventos
        -List~Usuario~ listaUsuarios
        +iniciarMenu()
        
        %% Gestión de Eventos
        +crearEvento(id, nombre, fecha, max)
        +listarEventos()
        +buscarEventoPorNombre(nombre)
        +eliminarEvento(id)
        
        %% Gestión de Usuarios
        +crearUsuario(id, nombre, email)
        +listarUsuarios()
        +buscarUsuarioPorNombre(nombre)
        +eliminarUsuario(id)
        
        %% Gestión de Inscripciones
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

    GestorEventos "1" --> "*" Evento : gestiona
    GestorEventos "1" --> "*" Usuario : administra
    Evento "0..*" <--> "0..*" Usuario : inscripciones
