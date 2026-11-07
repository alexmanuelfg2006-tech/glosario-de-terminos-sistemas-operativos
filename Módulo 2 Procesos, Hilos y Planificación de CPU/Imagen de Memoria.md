>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Imagen de memoria / Memory Image

Según Stallings (2017), la imagen de memoria representa la organización lógica y física del espacio de direcciones de un proceso en la memoria RAM, incluyendo los segmentos de código (texto), datos globales, pila (_stack_) y montón (_heap_). La imagen de memoria es un proceso completo de elementos que almacena y define a un proceso en la memoria
- C
    
    ```
    #include <stdio.h>
    #include <stdlib.h>
    
    int global_iniciada = 42; // Segmento Data
    
    int main() {
        int local = 10;       // Segmento Stack
        int *dinamica = (int *)malloc(sizeof(int)); // Segmento Heap
    
        printf("Dirección del Código (main):   %p\n", (void *)&main);
        printf("Dirección de Global (Data):    %p\n", (void *)&global_iniciada);
        printf("Dirección de Dinámica (Heap):  %p\n", (void *)dinamica);
        printf("Dirección de Local (Stack):    %p\n", (void *)&local);
    
        free(dinamica);
        return 0;
    }
    ```

```
 [ Binario Compilado ] ──> [ Asignación de Segmentos en RAM ] ──> [ Imagen de Memoria (Text, Data, Heap, Stack) ]
```


### Referencia 
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson. Capítulo 3