>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Segmento de Texto / Text Segment

Según Silberschatz et al. (2018), el segmento de texto es la región de la memoria virtual de un proceso que almacena el código máquina ejecutable, configurada generalmente como de solo lectura para evitar modificaciones accidentales y permitir su compartición entre múltiples instancias. es un segmento en la memoria de un programa donde estan las instrucciones paso a paso para su ejecucion.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Archivo Binario Compilado en Disco          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Carga inicial del cargador del sistema)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Segmento de Texto en Memoria Virtual (Text)     │
 │    * Contiene el código de máquina (instrucciones CPU)  │
 │    * Permisos de memoria configurados como: R-X         │
 │    * Compartible entre múltiples instancias del proceso │
 └────────────────────────────┬────────────────────────────┘
                              │ (Lectura secuencial por el Contador de Programa - PC)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Unidad de Procesamiento (Ejecución ALU)        │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3
