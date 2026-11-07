>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Bit NX / Bit de No Ejecución

Silberschatz et al. (2018) tratan esta bandera de seguridad a nivel de hardware en la CPU como un control que marca zonas específicas de memoria virtual como no ejecutables. La Unidad de Gestión de Memoria (MMU) rechaza automáticamente cualquier intento del procesador de interpretar instrucciones ubicadas en segmentos marcados con el bit NX. Esta propiedad impide que código malicioso inyectado en búferes de datos de la pila (stack) o del heap logre tomar el control del flujo del programa. Es conocida como XD en arquitecturas Intel y EVP en procesadores AMD.

Plaintext

```
 ┌─────────────────────────────────────────────────────────┤
 │         Entrada de Tabla de Páginas (PTE)               │
 │  * Contiene el Bit NX / XD (No-Execute / Execute-Disable│
 └────────────────────────────┬────────────────────────────┘
                              │ (Evaluación del hardware de la CPU al intentar saltar)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Validación de Permisos de Ejecución             │
 ├────────────────────────────┬────────────────────────────┤
 │ Si Bit NX == 1 (Bloqueado) │ Si Bit NX == 0 (Permitido) │
 │ ▼                          │ ▼                          │
 │ Excepción de Violación de  │ Ejecución normal de código │
 │ Memoria (Protección activa)│ autorizado en memoria      │
 └────────────────────────────┴────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.