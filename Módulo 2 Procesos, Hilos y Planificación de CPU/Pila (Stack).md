>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Pila / Stack 

Según Silberschatz et al. (2018), la pila es una estructura de datos de tipo LIFO (último en entrar, primero en salir) dentro de la memoria del proceso, empleada para almacenar datos temporales como parámetros de funciones, direcciones de retorno y variables locales. es una estructura que almacena datos temporales donde el ultimo en entrar es el primero en salir


```
 [ Llamada a Función ] ──> [ Pila (Stack LIFO) ] ──> [ Asignación de Variables Locales y Retorno ]
```
C

```
#include <stdio.h>

void funcion_recursiva(int nivel) {
    int variable_local_stack = nivel; // Almacenada en la Pila
    printf("Nivel %d - Dirección en Stack (Pila): %p\n", nivel, (void *)&variable_local_stack);

    if (nivel > 1) {
        funcion_recursiva(nivel - 1);
    }
}

int main() {
    printf("Demostración de crecimiento de la Pila (Stack):\n");
    funcion_recursiva(3);
    return 0;
}
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3