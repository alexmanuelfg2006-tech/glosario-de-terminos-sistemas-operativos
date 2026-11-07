>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
DAC / Control de Acceso Discrecional

Tanenbaum y Bos (2015) examinan este esquema de seguridad tradicional en entornos POSIX donde los propietarios de los recursos deciden los permisos de acceso para otros usuarios. La autorización se basa en la identidad del propietario y la pertenencia a grupos, clasificando los permisos en lectura, escritura y ejecución. El propietario de un archivo posee la facultad discrecional de modificar sus bits de permiso mediante comandos como chmod. Sin embargo, presenta limitaciones en seguridad avanzada ya que no impide que el software malicioso modifique permisos si tiene privilegios.

```
 ┌─────────────────────────────────────────────────────────┐
 │               Propietario del Objeto (Owner)            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Decide discrecionalmente permisos rwx)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Modelo DAC (Control de Acceso Discrecional)     │
 │  * Asignación basada en la identidad del usuario        │
 │  * Listas de control simples (Propietario, Grupo, Otros) │
 └────────────────────────────┬────────────────────────────┘
                              │ (Validación de acceso)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Acceso Autorizado o Denegado al Archivo         │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
