>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
SELinux / Security-Enhanced Linux

Tanenbaum y Bos (2015) revisan esta arquitectura de seguridad para el kernel Linux desarrollada originalmente por la NSA que aplica políticas de Control de Acceso Obligatorio (MAC). Asigna etiquetas de seguridad contextuales a todos los archivos, procesos, puertos y conectores de red del sistema. Cada interacción entre un proceso y un objeto es evaluada frente a una base de reglas cargada en el núcleo, bloqueando accesos no explícitamente autorizados. Evita que un atacante escale privilegios incluso obteniendo permisos de root.

```
 ┌─────────────────────────────────────────────────────────┐
 │        Proceso Solicitante (Con Contexto SELinux)       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Intenta acceder a recurso con etiqueta específica)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │       Subsistema SELinux en el Kernel (Vector MAC)      │
 │  * Consulta la base de datos de políticas de seguridad  │
 │  * Compara Contexto del Proceso vs Contexto del Objeto  │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si la política lo permite)             ▼ (Si la política lo prohíbe)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │       Acceso Concedido       │          │   Acceso Denegado (Log en    │
 │                              │          │        /var/log/audit)       │
 └──────────────────────────────┘          └──────────────────────────────┘
```


---
**Referencia:
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.