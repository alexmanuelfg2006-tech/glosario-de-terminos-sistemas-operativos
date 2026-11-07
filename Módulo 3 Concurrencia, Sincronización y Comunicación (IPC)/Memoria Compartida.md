>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Memoria Compartida / Shared Memory
Silberschatz et al. (2018) resaltan que esta técnica IPC representa el canal más veloz al permitir que múltiples procesos compartan el acceso directo al mismo segmento físico de la memoria RAM. Al eliminar la necesidad de copiar datos a través de búferes del kernel, las aplicaciones leen y escriben a la máxima velocidad del bus de memoria. Requiere el uso complementario de mecanismos de sincronización como semáforos o mutexes para evitar condiciones de carrera al modificar la memoria. Se emplea en servidores de bases de datos y procesamiento gráfico.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
