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

@MATRIZ


;auntomatizamos la matriz mara que llegue hasta 10
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
@10
A=D
@i
A=M
D=D-A
;
@1
D=A
@i
M=D
@MATRIZ
D;JEQ


; creamos el ciclo for: en el ciclo se debe intanciar
@j
M=0
@FOR
; ahora j debe coger el dato de la posicion indicada La matriz i
@j
D=M
@i
D=D+A
@R13    ; Vamos a usar R13 como temporal
M=D     ; Guardamos D en R13
@10     ; que el puntero de j se reste con 10
D=A
@R13
A=M    ; estamos en la posicion M(j) + i para coger el dato que existe en la posicion actual
A=M
D=D-A  ; que el puntero de j se reste con 10

;comparamos si D = 0, si no que vuelva a @FOR
@FIN
D;JEQ
@j
M=M+1
@FOR
D;JMP



@FIN
```



