>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Imagen OCI / Especificación de Imagen Abierta

Tanenbaum y Bos (2015) examinan esta especificación estandarizada de empaquetado de archivos y capas para la distribución e instanciación de contenedores de software. Establecido por la Open Container Initiative, empaqueta los binarios, configuraciones y el sistema de archivos raíz en un conjunto de capas comprimidas indexadas por hashes SHA-256. Garantiza que una imagen creada por una herramienta como Docker pueda ejecutarse de forma idéntica en cualquier motor compatible como Podman o Containerd. Su inmutabilidad facilita la integración continua.

```
 ┌─────────────────────────────────────────────────────────┐
 │              Manifiesto y Configuración OCI             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Define el punto de entrada y metadatos)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Capas de Sistema de Archivos (Solo Lectura)     │
 │  * Capa Base (ej. Distribución Linux limpia)            │
 │  * Capa Intermedia (Instalación de dependencias)        │
 │  * Capa Superior (Archivos y binarios de la aplicación) │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
