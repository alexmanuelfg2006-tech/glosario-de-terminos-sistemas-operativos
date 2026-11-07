>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
vector de interrupciones / Interrupt Descriptor Table

Según Silberschatz et al. (2018), el vector de interrupciones (o _Interrupt Descriptor Table_) es una tabla en memoria administrada por el procesador que asocia los números de interrupción con las direcciones de las rutinas de servicio (_Interrupt Service Routines_) que manejan cada evento. Es una estructura de datos que asocia cada vector de interrupción con su respectiva Rutina de Servicio de Interrupción

- Bash
    
    ```
    cat /proc/interrupts
    ```
    


```
 [ Evento / Hardware / Trap ] ──> [ CPU Consulta IDT ] ──> [ Puntero de ISR ] ──> [ Ejecución en Ring 0 ]
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 1