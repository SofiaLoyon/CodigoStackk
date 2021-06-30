# CodigoStackk

# CodigoStack


@ Examen Unica Oportunidad - Unidad 4- Lenguajes de Interfaz
@ Nombre del Programador: Velazquez Loyon Edna Sofia
@ Objetivo: Comentar el código y subirlo al repositorio de Git a través de comandos


@ Define el comienzo del código

.section __TEXT, __text
.global _main
.align 2

push {r7, lr}   @ Empuja el registro 7 en el registro de enlace
mov   r1, 0xB   @ Cambia el direccionamiento del registro
pop  {r7, pc}   @ Carga el registro 7 en el contador del programa


//Random.cpp

@ Utiliza la libreria iostream y aparta el espacio de memoria
#include <iostream>
using namespace std;


class Randomiser {              @ Crea una clase para generar numeros aleatorios
public: long a; int n;          @ Declara las variables

@ Crea una función para generar una cantidad definida por el usuario  de números aleatorios

        void calc() {
        cout<<"How many random numbers do you want? ";
        cin>>n;
        for (int i = 0; i < n; i++) {
            a = random();
            cout<<a<<"\n";
        }
    }
};

@ Manda a llamar a la función
int main() {
    Randomiser r;
    r.calc();
    return 0;
}
