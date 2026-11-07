>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
**Núcleo híbrido / Hybrid kernel

Según Silberschatz et al. (2018), un núcleo híbrido es una arquitectura que combina la estructura modular o orientada a mensajes del micronúcleo con la eficiencia del núcleo monolítico, ejecutando controladores o servicios clave en el espacio del núcleo para optimizar el rendimiento. es una estructura del sistema operativo que combina los micronucleos y los nucleos monoliticos


```
uname -mrs
```

```
 ┌─────────────────────────────────────────────────────────┐
 │               Aplicaciones de Usuario (Ring 3)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas al sistema / API)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Arquitectura del Núcleo Híbrido           │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Núcleo Base / Servicios Críticos (Ring 0)         │  │
 │  │ * Planificador, Memoria Virtual, IPC de alto rend.│  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Subsistemas Modulares / Drivers (Ring 0 o Ring 3) │  │
 │  │ * Subsistema gráfico, drivers no esenciales       │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                     Hardware Físico                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 2
