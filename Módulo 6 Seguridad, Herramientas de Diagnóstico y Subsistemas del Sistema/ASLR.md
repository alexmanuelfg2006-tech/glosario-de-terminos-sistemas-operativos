>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
ASLR / Aleatorización del Espacio de Direcciones

Silberschatz et al. (2018) analizan esta técnica como un mecanismo de seguridad crítico del sistema operativo que posiciona de forma aleatoria las zonas clave de memoria durante el arranque de un proceso. Al cambiar constantemente la ubicación del stack, el heap y las bibliotecas dinámicas compartidas en la RAM, dificulta la ejecución exitosa de exploits. Los atacantes no pueden predecir las direcciones físicas necesarias para inyectar código malicioso o realizar ataques de desbordamiento de búfer. Esta protección requiere soporte conjunto entre el compilador y la unidad de gestión de memoria (MMU).


```
 ┌─────────────────────────────────────────────────────────┐
 │          Carga y Lanzamiento de un Proceso              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Aplicación de semilla aleatoria del Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Distribución Aleatoria del Espacio Virtual      │
 │  * Posición de la Pila (Stack) desplazada               │
 │  * Posición del Montón (Heap) desplazada                │
 │  * Posición de Librerías (.so / DLL) aleatorizada       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Prevención de ataques orientados a direcciones fijas)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Entorno Protegido contra Explotación            │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
