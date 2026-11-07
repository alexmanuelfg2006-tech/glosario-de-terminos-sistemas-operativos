>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Registro de estado / Flags Register

Según Stallings (2017), el registro de estado o de _flags_ es un conjunto de bits individuales en el hardware de la CPU que indican el resultado de operaciones de la unidad aritmético-lógica (como desbordamiento o signo negativo) y el estado operativo general de las interrupciones. Es un registro en la Cpu donde se guardan resultados binarios despues de una operacion

C

```
#include <stdio.h>

int main() {
    int a = 5;
    int b = 5;
    if (a == b) { // Esta operación modifica el Zero Flag (ZF = 1) en el procesador
        printf("Los números son iguales (Zero Flag activado).\n");
    }
    return 0;
}
```

### Referencia
tallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson. Capítulo 1