>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Límites de RAM (memory.max) / Tope Máximo de Memoria cgroups

Silberschatz et al. (2018) analizan este parámetro de configuración dentro de cgroups v2 indicando que determina la cantidad máxima de memoria física que un grupo de control de procesos puede consumir. Cuando las aplicaciones dentro del grupo superan este umbral rígido configurado, el kernel intenta en primera instancia liberar páginas de caché de disco. Si la presión de memoria persiste sin poder reducirse, el kernel finaliza automáticamente la tarea de mayor consumo dentro del cgroup. Garantiza que un contenedor no agote la memoria del host.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
