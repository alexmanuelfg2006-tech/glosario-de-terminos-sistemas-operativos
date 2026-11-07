>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Valgrind / Herramienta de Análisis Dinámico

Silberschatz et al. (2018) presentan esta suite de herramientas para depuración y perfilado dinámico de programas que permite detectar fugas de memoria y accesos inválidos en C/C++. Su módulo principal, Memcheck, ejecuta el código fuente sobre una CPU sintética emulada para inspeccionar cada asignación y liberación en el heap. Identifica el uso de variables no inicializadas, lecturas fuera de los límites de arreglos y punteros colgados con precisión milimétrica. Resulta indispensable para garantizar código robusto.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
