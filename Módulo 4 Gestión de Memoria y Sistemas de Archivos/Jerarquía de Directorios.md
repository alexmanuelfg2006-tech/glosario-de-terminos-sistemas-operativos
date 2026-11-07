>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Jerarquía de Directorios / Estructura Jerárquica UNIX

Silberschatz et al. (2018) analizan cómo esta organización lógica de archivos y carpetas se dispone en forma de árbol cuya raíz absoluta está delimitada por la barra diagonal /. Define convenciones estandarizadas (FHS) donde /bin contiene binarios esenciales, /etc alberga archivos de configuración y /var gestiona datos variables. Esta abstracción permite unificar diferentes dispositivos de almacenamiento en un único árbol lógico mediante puntos de montaje. Facilita la administración de permisos de acceso de manera recursiva e intuitiva.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Directorio Raíz del Sistema ( / )           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asocia nombres a inodos de carpetas)
                              ▼
         ┌────────────────────┴────────────────────┐
         ▼                                         ▼
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │       Directorio /home       │          │       Directorio /etc        │
 └───────┬──────────────────────┘          └──────────────────────────────┘
         │ (Subdirectorios y archivos)
         ▼
 ┌──────────────────────────────┐
 │     Archivo de Usuario       │
 └──────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
