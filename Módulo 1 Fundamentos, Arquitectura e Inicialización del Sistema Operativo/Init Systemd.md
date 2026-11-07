>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Proceso Init Systemd / Init process Systemd

Según Bovet y Cesati (2005), `init` (y su contraparte moderna `systemd`) es el primer proceso en el espacio de usuario (PID 1) ejecutado por el núcleo tras el arranque del sistema, actuando como el ancestro o padre directo de todos los demás procesos y gestionando los servicios y demonios de fondo. Se ejecuta como proceso inicial para arrancar el sistema operativo
Plaintext

```
 ┌─────────────────────────────────────────────────────────┐
 │               Kernel de Linux (PID 0)                   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Lanza proceso init / systemd - PID 1)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               systemd / Init (PID 1)                    │
 │  * Lee archivos de configuración de unidades (.service) │
 │  * Resuelve dependencias y paraleliza el arranque       │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Activación Concurrente)                ▼ (Gestión de Control)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    Servicios y Daemons       │          │ Grupos de Control (cgroups)  │
 │   (Red, SSH, DBus, etc.)     │          │  y Aislamiento de Procesos   │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Bovet, D. P., & Cesati, M. (2005). _Understanding the Linux Kernel_ (3.ª ed.). O'Reilly Media.Capítulo 3