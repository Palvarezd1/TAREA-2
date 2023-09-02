# TAREA 2 - TRIANGULOS DE ASTERISCOS
## **Instrucciones**: *Escriba tres algoritmos (C++, Python y Pseudocódigo). Que se le solicite al usuario un número entero positivo e indique qué tipo de triángulo rectángulo quiere visualizar, son cuatro opciones y debe mostrar el triángulo según el número indicado y el elegido. La imagen siguiente hace referencia a las opciones y al número 5. Los tres códigos fuentes deben estar en un solo archivo Markdown y subirlo al repositorio (uno nuevo de preferencia y dejarlo como readme.md), Solo debe indicar la URL del mismo*
---
>## **PSEUDOCODIGO**
###### **CODIGO**:
:computer:
```
Algoritmo Triangulo_Asteriscos
	Definir asteriscos Como Entero
	definir op Como Entero
	Escribir "Ingrese el numero de asteriscos que desee que tenga el triangulo"
	Leer asteriscos
	
	Escribir "¿Cual de las 4 formas de los Tringulos desea ver?"
	
	Escribir "1-"
	Escribir " *"
	Escribir " **"
	Escribir " ***"
	Escribir " ****"
	Escribir " *****"
	
	Escribir "2-"
	Escribir "   *****"
	Escribir "    ****"
	Escribir "     ***"
	Escribir "      **"
	Escribir "       *"
	
	Escribir "3-"
	Escribir " *****"
	Escribir " ****"
	Escribir " ***"
	Escribir " **"
	Escribir " *"
	
	Escribir "4-"
	Escribir "     *"
	Escribir "    **"
	Escribir "   ***"
	Escribir "  ****"
	Escribir " *****"
	
	leer op 
	
	Segun op Hacer
		1:
			Para i<-1 Hasta asteriscos Con Paso 1 Hacer
				Para j<-1 Hasta i Con Paso 1 Hacer
					Escribir  "*", " "  Sin Saltar
				Fin Para
				Escribir " " 
			Fin Para
		2:
			Para i<- asteriscos Hasta 1 Con Paso -1 Hacer
				Para j<-0 Hasta (asteriscos-i-1) Con Paso 1 Hacer
					Escribir  " " Sin Saltar
				Fin Para
				Para j<-1 Hasta i Con Paso 1 Hacer
					Escribir "*" Sin Saltar
				Fin Para
				Escribir " " 
			Fin Para
		3:
			Para i<-0 Hasta asteriscos-1 Con Paso 1 Hacer
				Para j<-0 Hasta asteriscos-(i+1) Con Paso 1 Hacer
					Escribir "*"," " Sin Saltar
				Fin Para
				Escribir " "
			Fin Para
		4: 
			Para i<-0 Hasta asteriscos Con Paso 1 Hacer
				Para j<-0 Hasta (asteriscos-i-1) Con Paso 1 Hacer
					Escribir  " " Sin Saltar
				Fin Para
				Para j<-1 Hasta i Con Paso 1 Hacer
					Escribir "*" Sin Saltar
				Fin Para
				Escribir " " 
			Fin Para
	Fin Segun
FinAlgoritmo
```
---
___
> ## **C++**
###### **CODIGO**: 
:computer:
```c++
#include<iostream>
using namespace std;

int main() {
	int asteriscos, j ,i, op;
	cout << "Ingrese el numero de asteriscos que desee que tenga el triangulo" << endl;
	cin >> asteriscos;
	cout << "¿Cual de las 4 formas de los Tringulos desea ver?" << endl;
	cout << "1-" << endl;
	cout << " *" << endl;
	cout << " **" << endl;
	cout << " ***" << endl;
	cout << " ****" << endl;
	cout << " *****" << endl;
	cout << "2-" << endl;
	cout << "   *****" << endl;
	cout << "    ****" << endl;
	cout << "     ***" << endl;
	cout << "      **" << endl;
	cout << "       *" << endl;
	cout << "3-" << endl;
	cout << " *****" << endl;
	cout << " ****" << endl;
	cout << " ***" << endl;
	cout << " **" << endl;
	cout << " *" << endl;
	cout << "4-" << endl;
	cout << "     *" << endl;
	cout << "    **" << endl;
	cout << "   ***" << endl;
	cout << "  ****" << endl;
	cout << " *****" << endl;
	cin >> op;
	switch (op) {
	case 1:
		for (i=1;i<=asteriscos;i++) {
			for (j=1;j<=i;j++) {
				cout << "*" << " ";
			}
			cout << " " << endl;
		}
		break;
	case 2:
		for (i=asteriscos;i>=1;i--) {
			for (j=0;j<=(asteriscos-i-1);j++) {
				cout << " ";
			}
			for (j=1;j<=i;j++) {
				cout << "*";
			}
			cout << " " << endl;
		}
		break;
	case 3:
		for (i=0;i<=asteriscos-1;i++) {
			for (j=0;j<=asteriscos-(i+1);j++) {
				cout << "*" << " ";
			}
			cout << " " << endl;
		}
		break;
	case 4:
		for (i=0;i<=asteriscos;i++) {
			for (j=0;j<=(asteriscos-i-1);j++) {
				cout << " ";
			}
			for (j=1;j<=i;j++) {
				cout << "*";
			}
			cout << " " << endl;
		}
		break;
	}
	return 0;
}
```
---
___
> ## **PYTHON** 
###### **CODIGO**: 
:computer:
```python
num = int(input("Ingrese el numero de asteriscos que desee que tenga el triangulo: "))
print("¿Cual de las 4 formas de los triangulos desea ver?")
print("1-")
print("*")
print("**")
print("***")
print("****")

print("2-")
print("****")
print(" ***")
print("  **")
print("   *")

print("3-")
print("****")
print("***")
print("**")
print("*")

print("4-")
print("   *")
print("  **")
print(" ***")
print("****")

eleccion = int (input())

if eleccion == 1:
    for i in range (1,num+1):
        print('*' * i)

if eleccion == 2:
     for i in range (num+1):
        saltos = i
        print(' '*saltos+'*'*(num-i))

if eleccion == 3:
    for i in range (num,0,-1):
        print('*' * i)

if eleccion == 4:
    for i in range (num+1):
        saltos = num - i
        print(' '*saltos+'*'*i)
```