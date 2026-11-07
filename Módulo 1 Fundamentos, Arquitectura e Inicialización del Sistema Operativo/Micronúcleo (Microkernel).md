>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Micronúcleo / Microkernel

Según Tanenbaum y Bos (2015), un micronúcleo es una arquitectura que busca la tolerancia a fallos reduciendo el código en modo kernel al mínimo imprescindible (mecanismos de IPC, memoria básica y manejo de interrupciones), trasladando los servicios y controladores al modo usuario. Es un tipo de núcleo que tiene las funciones básicas del sistema operativo


```
 ┌─────────────────────────────────────────────────────────┐
 │               Aplicaciones de Usuario (Ring 3)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Paso de Mensajes IPC)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Servidores del Sistema en Espacio de Usuario (Ring 3)│
 │    [Servidor de Archivos]   [Drivers]   [Red / Subsistemas]│
 └────────────────────────────┬────────────────────────────┘
                              │ (Comunicación IPC mediante kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Micronúcleo Mínimo (Ring 0 exclusivo)          │
 │         (Solo IPC, hilos básicos y gestión de memoria)  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                     Hardware Físico                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 1