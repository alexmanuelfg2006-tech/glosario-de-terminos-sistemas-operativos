>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Cuotas de CPU (cpu.max) / Límite de Ancho de Banda de CPU

Silberschatz et al. (2018) explican este parámetro de configuración en cgroups v2 como el valor que determina el tiempo máximo de procesamiento que un grupo de tareas puede consumir en un ciclo. Se especifica mediante dos valores: el límite de tiempo de ejecución permitido en microsegundos y la duración del periodo de referencia. Si un contenedor agota su cuota asignada antes de finalizar el periodo, el planificador del kernel suspende temporalmente su ejecución hasta el siguiente ciclo. Este control previene que un proceso desbocado monopolice el procesador.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
