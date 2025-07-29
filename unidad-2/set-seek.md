# Unidad 2

## 🔎 Fase: Set + Seek

###Actividad 1

**Dibujando un punto en la pantalla**

Vamos a resolver juntos este problema:

La pantalla del computador Hack se controla a través de un mapa de memoria que comienza en la dirección 16384 (SCREEN). Cada bit en este mapa de memoria representa un pixel en la pantalla (1 = negro, 0 = blanco). Escribe un programa que dibuje un punto negro en la esquina superior izquierda de la pantalla. (Recuerda que la esquina superior izquierda corresponde al primer bit del primer word en la dirección SCREEN).

Traduce este programa a lenguaje C++ para que relaciones cómo los conceptos de alto nivel se traducen a bajo nivel.

``` cpp
screen= 1; // suponiendo que sscreen representa la posicion 16384

```

### Actividad 02


Dibujando una línea horizontal
Vamos a resolver juntos este problema:

Modifica el programa anterior para que dibuje una línea horizontal negra de 16 pixeles de largo en la esquina superior izquierda de la pantalla. (Recuerda que cada word en la memoria representa 16 pixeles).

``` asm
screen= -1; // forzar al compilador para que asigne la variables screen a  la direccion  1684

```

Traduce este programa a lenguaje C++ para que relaciones cómo los conceptos de alto nivel se traducen a bajo nivel.

``` cpp
screen= -1; // forzar al compilador para que asigne la variables screen a  la direccion  1684

```
Otra forma de hacerlo.
``` cpp
screen= 0xFFFF; // forzar al compilador para que asigne la variables screen a  la direccion  1684

```
