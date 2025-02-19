Integrantes:Santiago Robles Castro
código de diagrama


classDiagram
class Libro {
        +String titulo
        +String isbn
        +int yearPublicacion}
class Lector {
        +String nombre
        +String numerosocio
        +String fecharegistro
    }

class Prestamo {
        +String fechaPrestamo
        +String fechaDevolucion
        +devolverLibro()
    }

    Libro "1" -- "*" Prestamo : es prestado en
    Lector "1" -- "*" Prestamo : realiza