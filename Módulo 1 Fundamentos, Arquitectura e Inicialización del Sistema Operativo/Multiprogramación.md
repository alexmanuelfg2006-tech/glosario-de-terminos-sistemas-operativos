>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Multiprogramación / Multiprogramming

Según Silberschatz et al. (2018), la multiprogramación es la técnica operativa mediante la cual el sistema operativo mantiene múltiples trabajos cargados simultáneamente en la memoria principal, con el objetivo de alternar la CPU entre ellos cuando un proceso queda a la espera de operaciones de E/S. Permite mantener procesos cargados en la memoria y se alternan entre ellos para hacer un mejor uso de la cpu

C

```
#include <stdio.h>
#include <unistd.h>
#include <sys/types.h>

int main() {
    pid_t pid = fork(); // Crea un nuevo flujo de ejecución residente en memoria
    if (pid == 0) {
        printf("[Programa B en RAM] Ejecutando tareas secundarias concurrentes...\n");
    } else {
        printf("[Programa A en RAM] Ejecutando tareas principales concurrentes...\n");
    }
    return 0;
}
```


```
 [ Múltiples Trabajos en RAM ] ──> [ Espera de E/S Oculta ] ──> [ Mayor Ocupación de CPU ] ──> [ Aumento de Throughput ]
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 1