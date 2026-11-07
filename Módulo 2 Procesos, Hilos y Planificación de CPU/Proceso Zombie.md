>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Proceso Zombie /  Zombie Process

Según Tanenbaum y Bos (2015), un proceso zombie es aquel que ha completado su ejecución pero cuya entrada permanece en la tabla de procesos del núcleo debido a que su proceso padre aún no ha leído su código de salida mediante la llamada al sistema `wait()`. Es el proceso que fue completado pero el proceso padre que lo creo no lee el fin de su ejecucion 


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso Hijo (Ejecución Concluida)        │
 └────────────────────────────┬────────────────────────────┘
                              │ (Termina y libera memoria, pero retiene PCB)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Estado Zombie (Defunciones)               │
 │    * Entrada en la tabla de procesos del Kernel         │
 │    * Código de salida (Exit Status) almacenado          │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si el Proceso Padre ejecuta wait())    ▼ (Si el Padre muere antes)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │   El Kernel libera el PCB    │          │  El proceso es adoptado por  │
 │     definitivamente          │          │      init / systemd (PID 1)  │
 └──────────────────────────────┘          └──────────────────────────────┘
```
### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson. Capítulo 2