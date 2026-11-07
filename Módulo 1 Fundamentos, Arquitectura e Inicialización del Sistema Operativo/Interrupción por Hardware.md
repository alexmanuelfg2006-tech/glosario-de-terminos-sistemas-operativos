>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Interrupcion por hardware / hardware interrupt

Según Stallings (2017), una interrupción por hardware es una señal eléctrica asíncrona enviada por un dispositivo de entrada/salida al procesador para notificarle un evento que requiere atención inmediata, provocando la suspensión temporal del hilo de ejecución actual. es cuando algún componente del hardware falla y manda una señal al procesador 



```
 [ Dispositivo Físico / Periférico ]
                 │
                 ▼ (Pulso eléctrico asíncrono)
 [ Controlador de Interrupciones (APIC / PIC) ]
                 │
                 ▼ (Vector de Interrupción - IRQ)
      [ Tabla IDT en Memoria ]
                 │
                 ▼ (Puntero a función)
      [ ISR (Interrupt Service Routine) ]
                 │
        ┌────────┴────────────────────────┐
        ▼                                 ▼
 [ Cambio de Contexto ]          [ Limpieza del Buffer de Hardware ]
        │                                 │
        └────────────────┬────────────────┘
                         ▼
        [ Retorno al Hilo de Usuario (IRET) ]
```

C

```
#include <stdio.h>
#include <unistd.h>
#include <signal.h>

// Manejador simulado para la interrupción de hardware (ej. señal de alarma o hardware externo)
void manejador_irq_hardware(int signum) {
    write(STDOUT_FILENO, "[Hardware IRQ] Dispositivo externo atendido por la ISR.\n", 53);
}

int main() {
    // Asociamos una señal del sistema operativo que simula una notificación de hardware
    signal(SIGALRM, manejador_irq_hardware);

    printf("Simulando espera de eventos de hardware...\n");
    
    // Configuramos una alarma que actúa como evento periódico de hardware (ej. Timer del sistema)
    alarm(2); 

    while(1) {
        pause(); // El CPU espera de forma eficiente hasta que ocurra la interrupción asíncrona
    }

    return 0;
}
```
### Referencia
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson. Capítulo 1