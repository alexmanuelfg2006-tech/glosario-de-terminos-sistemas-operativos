>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
interrupción por temporizador / timer interrupt

Según Silberschatz et al. (2018), la interrupción por temporizador (_timer interrupt_) es una señal generada periódicamente por un circuito de hardware dedicado para devolver el control del procesador al sistema operativo y evitar que un proceso monopolice indefinidamente la CPU. Sirve para que se ejecuten algunas funciones en tiempos determinados

C

```
#include <stdio.h>
#include <unistd.h>
#include <signal.h>

void manejador_timer(int sig) {
    printf("[Timer Interrupt] Quantum agotado. Cediendo CPU al planificador...\n");
    alarm(1); // Renueva la interrupción del temporizador cada 1 segundo
}

int main() {
    signal(SIGALRM, manejador_timer);
    alarm(1);
    printf("Sistema iniciado con multitiempos. Ejecutando procesos...\n");
    for(int i = 0; i < 3; i++) {
        sleep(2); // Simula carga de trabajo
    }
    return 0;
}
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 1