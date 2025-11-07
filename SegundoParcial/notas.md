# Notas 

---

## Diferentes formas de comparar:
### 1. Comparable
    Es una interfaz que implementás dentro de la clase del objeto
    que querés comparar.

    Aplica una comparación 'natural'.

    public class Persona implements Comparable<Persona> { ... }
    
### 2. Comparator
    También es una interfaz, pero externa a la clase que comparás.
    Le decís explícitamente cómo querés comparar dos objetos en 
    cada caso.

    Aplica una comparación configurable.

    public class ComparadorPorDni implements Comparator<Persona> 
    { ... }

### 3. compareTo()
    Acopla la lógica de comparación a la clase.
    No sirve para código genérico.

    Exige el uso de comparable.
---

### Resumen
En síntesis, el ideal para trabajar con código genérico y tener más 
flexibilidad es Comparator<T> porque esta es una interfaz externa a la clase 
que quiero comparar.

---