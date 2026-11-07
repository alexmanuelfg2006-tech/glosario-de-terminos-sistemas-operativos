>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Espacio de Direcciones Compartido / Shared Address Space

Según Tanenbaum y Bos (2015), el espacio de direcciones compartido es la característica que permite a múltiples hilos de un mismo proceso acceder a las mismas variables globales, segmentos de datos y montón, facilitando una comunicación interprocesos de alto rendimiento. es un espacio de memoria virtual que permite que dos o mas procesos o hilos de ejecucion  puedan acceder a ella
- Bash
    
    ```
    ipcs -m
    ```
    
    _Salida de ejemplo:_
    
    ```
    ------ Shared Memory Segments --------
    key        shmid      owner      perms      bytes      nattch     status      
    0x00000000 32768      alex       666        4096       2          
    ```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 2