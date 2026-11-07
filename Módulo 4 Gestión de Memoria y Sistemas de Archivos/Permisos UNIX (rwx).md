>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Permisos UNIX (rwx) / Esquema de Permisos POSIX

Silberschatz et al. (2018) definen este modelo básico de seguridad de archivos especificando facultades de lectura (r), escritura (w) y ejecución (x) según Propietario, Grupo y Otros. En archivos de texto, la lectura permite abrir el contenido, la escritura modificarlo y la ejecución procesar el binario. En directorios, la ejecución otorga el permiso de acceder a su interior y listar inodos. Este esquema simple pero potente forma la primera línea de defensa en sistemas operativos de la familia POSIX frente a accesos no autorizados.


```
 ┌─────────────────────────────────────────────────────────┐
 │           Estructura de Permisos del Inodo              │
 ├──────────────┬──────────────┬──────────────┬────────────┤
 │ TipoArchivo  │ Propietario  │ Grupo        │ Otros      │
 │ (ej. - / d)  │ (rwx)        │ (rwx)        │ (rwx)      │
 └──────────────┴──────┬───────┴──────┬───────┴─────┬──────┘
                       │              │             │
                       ▼              ▼             ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Evaluación del Kernel en Solicitudes de Acceso    │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
