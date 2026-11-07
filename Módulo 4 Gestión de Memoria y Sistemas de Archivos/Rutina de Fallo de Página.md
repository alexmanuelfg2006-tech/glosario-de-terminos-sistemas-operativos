>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Rutina de Fallo de Página / Page Fault Service Routine

Según Silberschatz et al. (2018), la rutina de servicio de fallo de página es el conjunto de instrucciones del núcleo encargadas de gestionar el almacenamiento secundario, asignar un marco físico en la RAM, cargar la página requerida y actualizar las estructuras de control. Es el procedimiento de software en modo kernel que se ejecuta de manera automática al producirse un fallo de página.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Inicio de Rutina de Fallo de Página         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Verifica validez de la dirección lógica)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │  1. Búsqueda de Marco Libre (o reemplazo por algoritmo) │
 │  2. Lectura de la página desde el Disco / Archivo / Swap│
 │  3. Actualización de la PTE (Asigna marco y Bit = 1)    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Restauración del contexto)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │   Reanudación de la Instrucción Original en el Proceso  │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. (Capítulo 10
