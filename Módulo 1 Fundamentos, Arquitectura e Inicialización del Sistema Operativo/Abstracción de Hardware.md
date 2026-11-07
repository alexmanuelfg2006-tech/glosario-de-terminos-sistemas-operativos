>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---

***Abstracción de hardware / Hardware Abstraction

Según **Andrew S. Tanenbaum** y **Herbert Bos** (2015) la abstracción de hardware transforma una arquitectura física compleja, desordenada y repleta de detalles de bajo nivel (como registros de interrupción, temporizadores o controladores de disco) en una abstracción limpia (como un proceso o un flujo de datos).En pocas palabras la abstracción del hardware es el mecanismo que oculta la complejidad del hardware para ofrecer al kernel y a los programas una interfaz simple


![[Pasted image 20261103113309.png]]

```
[ Hardware Físico ] (Silicio, Transistores, Registros Eléctricos)
          │
          ▼
 [ Firmware / BIOS / UEFI ] (Software grabado en ROM/Flash que inicializa el sistema)
          │
          ▼
 [ Capa de Abstracción de Hardware (HAL) ] (Aísla al Kernel de variaciones de la placa base)
          │
          ▼
 [ Drivers / Controladores de Dispositivo ] (Traducen llamadas del SO a comandos del componente)
          │
          ▼
 [ Núcleo del Sistema Operativo (Kernel) ] (Gestiona memoria, procesos y recursos lógicos)
          │
          ▼
 [ APIs del Sistema / Llamadas al Sistema (Syscalls) ] (Interfaz uniforme para programas)
          │
          ▼
 [ Aplicaciones de Usuario ] (Software que opera sin contacto directo con el hardware)
```
### Referencia
Tanenbaum, A. S., y Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson.