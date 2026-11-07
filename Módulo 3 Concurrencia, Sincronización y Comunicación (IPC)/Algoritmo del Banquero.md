>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Algoritmo del Banquero / Banker's Algorithm

Según Silberschatz et al. (2018), el algoritmo del banquero es un método diseñado para comprobar si existe una secuencia segura de asignación de recursos antes de otorgar una petición en firme. Es el algoritmo clásico de evitación de interbloqueos que simula la concesión de recursos y evalúa si el sistema permanece en un estado seguro antes de aprobar solicitudes.


```
 ┌─────────────────────────────────────────────────────────┐
 │         Solicitud de Recursos por un Proceso            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Simulación previa en el Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Algoritmo del Banquero (Evasión)             │
 │  * ¿Solicitud <= Necesidad máxima declarada?            │
 │  * ¿Solicitud <= Recursos Disponibles actuales?         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Evaluación de secuencia segura)
                              ▼
         ┌────────────────────┴────────────────────┐
         ▼ (Estado Seguro / Existe Secuencia)      ▼ (Estado Inseguro / Riesgo)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │   Se conceden los recursos   │          │  Se deniega o suspende la    │
 │       al proceso             │          │    solicitud temporalmente   │
 └──────────────────────────────┘          └──────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 8