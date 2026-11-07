>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
tiempo compartido / timesharing

Según Silberschatz et al. (2018), el tiempo compartido (_timesharing_) es una evolución interactiva de la multiprogramación donde la CPU conmuta con tanta frecuencia entre múltiples tareas de distintos usuarios que estos perciben una interacción directa y simultánea con el sistema. el tiempo compartido permite usar una computadora por diferentes usuarios simultaneamente

- C
    
    ```
    #include <stdio.h>
    
    struct Proceso {
        int id;
        int tiempo_restante;
    };
    
    int main() {
        struct Proceso p1 = {1, 5};
        struct Proceso p2 = {2, 3};
        int quantum = 2;
    
        printf("Simulando Tiempo Compartido con Quantum = %d\n", quantum);
        printf("Proceso %d ejecuta %d unidades de tiempo.\n", p1.id, quantum);
        printf("Proceso %d ejecuta %d unidades de tiempo.\n", p2.id, quantum);
        return 0;
    }
    ```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 1