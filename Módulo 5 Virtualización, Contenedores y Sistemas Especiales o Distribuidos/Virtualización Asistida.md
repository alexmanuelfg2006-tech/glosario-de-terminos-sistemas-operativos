>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Virtualización Asistida / Virtualización Acelerada por Hardware

Silberschatz et al. (2018) destacan cómo este enfoque aprovecha las instrucciones físicas del procesador (Intel VT-x / AMD-V) para ejecutar tareas de virtualización con mínima penalización. El procesador asume de forma nativa la ejecución de instrucciones de modo privilegiado del sistema invitado sin requerir emulación pesada por software. Permite que el hipervisor transfiera el control de la CPU directamente a la máquina virtual reduciendo significativamente los retardos de interrupción. Eleva el rendimiento a niveles de hardware real.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Hipervisor Tipo 1 o Tipo 2                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Instrucciones con soporte de hardware)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Extensiones de CPU (Intel VT-x / AMD-V)         │
 │  * Nuevos modos de operación: Root y Non-Root           │
 │  * Interceptación automática de instrucciones privilegiadas│
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución directa en el procesador físico)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Hardware Físico del Procesador              │
 └─────────────────────────────────────────────────────────┘
```



---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
