>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Enlace Simbólico / Symlink 

Silberschatz et al. (2018) explican que este archivo especial guarda una cadena de texto representando la dirección de ruta relativa o absoluta hacia otro archivo o directorio. Funciona de manera similar a los accesos directos en sistemas Windows, ya que posee su propio número de inodo y permisos independientes del objeto apuntado. Si el archivo original se elimina o cambia de ubicación, el enlace simbólico permanece en el sistema pero queda roto o inoperativo. A diferencia de los enlaces duros, pueden cruzar diferentes sistemas de archivos.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Enlace Simbólico (Symlink)                │
 │  * Posee su propio Inodo independiente                  │
 │  * Sus datos almacenan una cadena de texto con la ruta  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Resuelve y redirige la ruta de texto)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Archivo o Directorio de Destino Real            │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
