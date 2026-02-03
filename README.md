# Taller Analisis de Complejidad #
mirando a fondo ela archivo de complijidad cuenta con 12 archivos; de los cuales esta:
---
```bash
Comandos.txt (instrucciones a compilación y para ejecturar)
factorial_functions.cxx
factorial_functions.h
my_test_factorial
my_test_sort_random
sort_functions.cxx
sort_functions.h
sort_functions.hxx
test_factorial.cxx
test_sort_inverse.cxx
test_sort:random.cxx
test_sort_sorted.cxx
```
---
# Archivos header (*.h / *.hxx) #
-
  factorial_functions.h — declara:
  unsigned long factorial_recursive(unsigned long n);
  unsigned long factorial_iterative(unsigned long n);
  sort_functions.h — declara:
  void bubblesort(long* a, long n);
  void quicksort(long* a, long n);
  void heapsort(long* a, long n);
  template<bool> is_sorted(I first, I last) (incluye sort_functions.hxx).
  sort_functions.hxx — implementa la plantilla is_sorted (comprobador de orden).
---
# Archivos fuente (*.cxx) #

  factorial_functions.cxx — implementa las dos versiones del factorial (recursiva e iterativa).
  sort_functions.cxx — implementa bubblesort, quicksort (con partición) y heapsort (std::make_heap +   std::sort_heap).
  test_factorial.cxx — ejecutable de prueba: calcula factorial recursivo e iterativo y mide tiempos.
  test_sort_random.cxx — ejecutable de prueba: genera array aleatorio, aplica 3 sorts, verifica        is_sorted y mide tiempos.
  test_sort_sorted.cxx — igual que anterior pero con arrays ya ordenados.
  test_sort_inverse.cxx — igual pero con arrays en orden inverso.

# Ejecutables generados (por comandos.txt) #
  my_test_factorial
    my_test_sort_random
    my_test_sort_inverse
    my_test_sort_sorted

Argumentos por línea de comandos

    my_test_factorial: recibe 1 arg posicional — n (entero).
    my_test_sort_*: reciben 1 arg posicional — count (número de elementos).

Formato de salida (qué imprime y significado de columnas)

    my_test_factorial (5 columnas, separadas por espacios):
        n
        resultado_recursivo (unsigned long)
        resultado_iterativo (unsigned long)
        tiempo_recursivo (ns)
        tiempo_iterativo (ns)

    my_test_sort_* (7 columnas, separadas por espacios):
        count
        is_sorted_bubble (1/0)
        is_sorted_quick (1/0)
        is_sorted_heap (1/0)
        time_bubble (ns)
        time_quick (ns)
        time_heap (ns)

Puntos importantes / recomendaciones breves

    Overflow: factorial usa unsigned long → overflow a partir de 21! en 64-bit. Los valores >20 no son factoriales correctos.
    Medición: solo una medición por ejecución; para datos fiables hacer repeticiones y estadísticas (media/mediana).
    Seguridad: se usa delete en vez de delete[] para arreglos → comportamiento indefinido; recomiendo usar delete[] o std::vector.
    Uso: comandos.txt incluye ejemplos para generar tablas con bucles (redirigir a .txt).
