>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Podman / Gestor de Contenedores Rootless

Silberschatz et al. (2018) presentan este motor de gestión de contenedores OCI destacando que no requiere un demonio central en segundo plano ni ejecución obligatoria como superusuario. Al adoptar una arquitectura sin demonio, cada contenedor se ejecuta como un hijo directo del proceso del usuario que lo invoca, mejorando la seguridad. Utiliza los namespaces de usuario de Linux para mapear privilegios de root dentro del contenedor a usuarios sin privilegios en el host. Mantiene total compatibilidad con la sintaxis de comandos de Docker.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Herramienta Podman (CLI de Usuario)         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución directa sin intermediario demonio)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │       Llamadas a Concurrency / Runtime (runc / crun)    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución segura y aislada en modo usuario / Rootless)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Contenedor Activo como Proceso del Sistema       │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
