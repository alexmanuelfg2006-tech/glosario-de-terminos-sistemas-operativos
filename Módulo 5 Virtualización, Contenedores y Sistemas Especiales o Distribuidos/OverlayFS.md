>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
OverlayFS / Sistema de Archivos Superpuesto

Tanenbaum y Bos (2015) describen este mecanismo de unión de archivos en Linux que combina capas de directorios distintas (lectura/escritura) presentando una vista unificada al usuario. Superpone una capa superior modificable (UpperDir) sobre una o más capas inferiores de solo lectura (LowerDir). Si un proceso intenta alterar un archivo de la capa base, OverlayFS realiza una copia automática del archivo a la capa superior mediante Copy-on-Write. Es la tecnología predilecta para estructurar las capas inmutables de imágenes de Docker.

```
┌─────────────────────────────────────────────────────────┐
 │         Capa Superior de Escritura (UpperDir / CoW)     │
 ├─────────────────────────────────────────────────────────┤
 │         Capas Base de Solo Lectura (LowerDirs / OCI)    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Unificados y presentados como un único directorio)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Punto de Montaje Unificado                │
 │  * Vista combinada para las aplicaciones del contenedor │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
