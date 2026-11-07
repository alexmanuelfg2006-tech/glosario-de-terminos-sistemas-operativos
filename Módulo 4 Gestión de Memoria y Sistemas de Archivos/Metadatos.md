>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Metadatos / Atributos Estructurales de Archivo

Tanenbaum y Bos (2015) clasifican esta información descriptiva almacenada sobre un objeto en disco (permisos, propietarios, marcas temporales, tamaño) exceptuando su contenido real. En sistemas de archivos basados en UNIX, estos atributos se consolidan internamente dentro de las estructuras de inodos. Permiten al sistema operativo validar autorizaciones de acceso, gestionar cuotas de disco y mantener el orden del árbol de directorios. La consistencia de los metadatos resulta crítica para evitar la corrupción del volumen de almacenamiento.


```
 ┌─────────────────────────────────────────────────────────┐
 │           Archivo Almacenado en el Sistema              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Información de control y gestión asociada)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                   Bloque de Metadatos                   │
 │  * Propietario y Permisos (UID / GID / RWX)             │
 │  * Tamaños y Tiempos (Timestamps: ctime, mtime, atime)  │
 │  * Punteros físicos a los bloques de datos reales       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Utilizado por el Sistema Operativo para control)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Gestión Segura y Localización de Archivos       │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
