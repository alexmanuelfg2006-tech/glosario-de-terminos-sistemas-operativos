>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Hard Link / enlace duro

Tanenbaum y Bos (2015) definen este elemento como un nombre o entrada de directorio adicional que referencia directamente a un número de inodo existente en el mismo volumen de almacenamiento. A diferencia de las copias físicas, no duplica el contenido de los datos en el disco ni consume nuevos bloques de almacenamiento. Todos los enlaces duros asociados a un archivo comparten los mismos permisos, propietarios y marcas temporales dentro de la tabla de inodos. El archivo sólo se elimina físicamente cuando el contador de enlaces duros se reduce a cero.


```
 ┌─────────────────────────────────────────────────────────┐
 │        Directorio 1                 Directorio 2        │
 │     [ Archivo_A ]                  [ Archivo_B ]        │
 └───────────┬────────────────────────────┬────────────────┘
             │ (Ambos apuntan exactamente al mismo)
             ▼                            ▼
 ┌─────────────────────────────────────────────────────────┤
 │                    Inodo Único Compartido               │
 │  * Número de inodo idéntico                             │
 │  * Contador de enlaces (Link Count) incrementado        │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a los mismos bloques en disco)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Bloques de Datos Físicos en el Disco           │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
