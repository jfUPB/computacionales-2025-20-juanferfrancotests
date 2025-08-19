# Unidad 3

## 🔎 Fase: Set + Seek

## Actividad 01


* ¿Para qué sirven los breakpoints?

Sirven para correr los el progrma o el codigo en un punto en especifico y poder hacer un rastreo paso a paso para saber como se esta ejecutando el codigo

* ¿Para qué se usa la ventana de depuración Autos?

  La ventana de depuracion sirve para que el programa corra correctamnte, es una ventana en donde el programa escanea la receta de lo que se va a realizar.

## Actividad 02



```cpp

#include <iostream>
#include <cstdlib>

using namespace std;

// Variables globales
int global_inicializada = 42;
int global_no_inicializada;

// Constante global
const char* const mensaje_ro = "Hola, memoria de solo lectura";

// Función de ejemplo que muestra la dirección de su variable local estática
void funcionConStatic() { // Segmento de código (instrucciones, funciones)
    static int var_estatica = 100;  // Variables globales y estáticas
    cout << "Dirección de var_estatica (static): " << &var_estatica << endl;
} 

// Función que asigna memoria dinámica (heap)
int* crearArrayHeap(int tam) {
    int* arr = new int[tam];
    for (int i = 0; i < tam; i++) {
        arr[i] = i;
    }
    return arr;
}

// Una función simple para representar el código (se encontrará en la región de código)
int suma(int a, int b) {
    int c = a + b; // "c" es una variable local (stack)
    return c;
}

int main() {
    // Variable local (stack)
    int a = 10;  // Variable local (stack)
    int b = 20;  // Variable local (stack)
    int c = suma(a, b);  // Variable local (stack)

    cout << "Resultado de suma(a, b): " << c << endl;
    cout << "Dirección de variable local 'a': " << &a << endl;
    cout << "Dirección de variable local 'b': " << &b << endl;
    cout << "Dirección de la variable local 'c' (resultado): " << &c << endl;

    // Variables globales
    cout << "Dirección de 'global_inicializada': " << &global_inicializada << endl;
    cout << "Dirección de 'global_no_inicializada': " << &global_no_inicializada << endl;

    // Constante global (solo lectura)
    cout << "Dirección de 'mensaje_ro' (zona de solo lectura): " << static_cast<const void*>(mensaje_ro) << endl;

    // Llamada a función que tiene variable estática
    funcionConStatic();

    // Uso del Heap: asignación dinámica
    int tamArray = 10;
    int* arrayHeap = crearArrayHeap(tamArray);
    cout << "Dirección del primer elemento del array asignado en Heap: " << arrayHeap << endl;
    for (int i = 0; i < tamArray; i++) {
        cout << "arrayHeap[" << i << "] = " << arrayHeap[i]
            << " en " << (arrayHeap + i) << endl;
    }
    delete[] arrayHeap; // Liberamos la memoria dinámica

    return 0;
}

```

## Actividad 04

### Experimento 1: modificar el segmento de texto:

<img width="778" height="313" alt="image" src="https://github.com/user-attachments/assets/00147607-d7f3-4f04-85bd-62a15a0a36f4" />

- ¿Qué ocurre?

se bloquea el programa
  
- ¿Por qué?

porque se intenta modificar la funcion main, lo cual el sistema operativo lo detecta y lo bloquea

### Experimento 2: modificar el segmento de datos (constante global):


