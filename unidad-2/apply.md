# Unidad 2


## 🛠 Fase: Apply

Implementa el programa anterior en lenguaje ensamblador aplicando el concepto de punteros.

```cpp

int arr[] = {1,2,3,4,5,6,7,8,9,10};
int sum = 0;

for (int j = 0; j < 10; j++) {
    sum = sum + arr[j];
}

```

```asm

;Creamos un Array
;contador de los saltos de las celdas
@16
D=A
@i  
M=D

@j
M=1

;auntomatizamos la matriz mara que llegue hasta 10
@MATRIZ
@j
D=A
@1
D=D+A

;Hacemos la matriz Coloque en la Ram el numero que corresponde
@i
A=M
D=A
D=D+1
@i
A=M
M=D     ; colocamos el valor de D en el posicion que tenga pordentro de la ram (i) 
@i      ; hcaemos que i aumente 10 veces
M=M+1


```
