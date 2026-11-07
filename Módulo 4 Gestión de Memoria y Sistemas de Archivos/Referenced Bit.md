>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Bit de referencia / Referenced Bit

Según Silberschatz et al. (2018), el bit de referencia es un indicador actualizado por el hardware de la CPU cada vez que se referencia la página correspondiente, proporcionando información esencial a los algoritmos de reemplazo para estimar la frecuencia de uso reciente. Es una bandera de control que la MMU marca en 1 cada vez que la página asociada es accedida por la CPU, ya sea para una operación de lectura o de escritura.


```
 ┌─────────────────────────────────────────────────────────┐
 │          Acceso de Lectura o Escritura a Página         │
 └────────────────────────────┬────────────────────────────┘
                              │ (El hardware registra el uso)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Referenced Bit (Indicador de Actividad)         │
 │  * Bit = 1: Página accedida recientemente               │
 │  * Bit = 0: Página inactiva (Candidata para reemplazo)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Revisado periódicamente por el Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │       Optimización de Reemplazo de Páginas              │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10