[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vTkcPn0-)
# 2.-Dise-o-Orientado-a-Objetos
Primer acercamiento y prácticas guiadas e individuales de POO
# Diagrama de Clases - Sistema de Biblioteca

```mermaid
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
```
# Relaciones y cardinalidad de los elementos
Libro-Préstamo

Un libro puede estar involucrado en varios préstamos en bastante tiempo.
Cada préstamo se asocia a un solo libro.
Cardinalidad: 1 a muchos (Un libro puede tener varios préstamos, pero cada préstamo pertenece a un solo libro).
Lector-Préstamo

Un lector puede realizar varios préstamos.
Cada préstamo está asociado a un solo lector.
Cardinalidad: 1 a muchos (Un lector puede hacer muchos préstamos, pero cada préstamo pertenece a un solo lector).
Préstamo-libro y lector

Cada préstamo vincula exactamente un libro y un lector en una fecha específica,lo que significa que sin un libro y un lector juntos no existe un prestamo.
Cardinalidad: muchos a 1 en ambas relaciones (muchos préstamos pueden referirse a un solo libro o a un solo lector)


