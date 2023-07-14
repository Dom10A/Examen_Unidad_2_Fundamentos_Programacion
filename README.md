# Examen_Unidad_2_Fundamentos_Programacion
En este repositorio se vera reflejado 10 ejercicios de fundamentos de programación en C++ los mismos que fueron creados por mi persona con fines educativos. 
Programa 1 
CONSTRUCCIÓN DE LA PLANTILLA PARA EL PROGRAMA MENU FUNCIONES CON
SWITCH CASE
Código 
//EJERCICIO 1 DOMINIC_COLLAGUAZO_:)//
//CONSTRUCCIÓN DE LA PLANTILLA PARA EL PROGRAMA MENU FUNCIONES CON//
//SWITCH CASE//
#include <iostream>
#include <cstdlib>

using namespace std;

int main()
{
    int opcion;
    bool repetir = true;
    
    do {
        system("cls");
        
        // Texto del menú que se verá cada vez
        cout << "\n\nMenu de Opciones" << endl;
        cout << "1. Opcion 1" << endl;
        cout << "2. Opcion 2" << endl;
        cout << "3. Opcion 3" << endl;
        cout << "4. Opcion 4" << endl;
        cout << "0. SALIR" << endl;
        
        cout << "\nIngrese una opcion: ";
        cin >> opcion;
        
        switch (opcion) {
            case 1:
                // Lista de instrucciones de la opción 1                
                
                system("pause>nul"); // Pausa
                break;
                
            case 2:
                // Lista de instrucciones de la opción 2                
                
                system("pause>nul"); // Pausa
                break;
                
            case 3:
                // Lista de instrucciones de la opción 3                
                
                system("pause>nul"); // Pausa            
                break;
                
            case 4:
                // Lista de instrucciones de la opción 4                
                
                system("pause>nul"); // Pausa                
                break;
            
            case 0:
            	repetir = false;
            	break;
        }        
    } while (repetir);
	 
    return 0;
}



Programa 2
Hacer un programa que muestre 3 números ordenados desendentemente, utilizar un
procedimiento para cada operación
Código:
//EJERCICIO 2 DOMINIC_COLLAGUAZO_:)//
//Hacer un programa que muestre 3 números ordenados desendentemente, utilizar un//
//procedimiento para cada operación//
#include <iostream>
using namespace std;

// Procedimiento para intercambiar dos números
void intercambiar(int& a, int& b) {
    int temp = a;
    a = b;
    b = temp;
}

// Procedimiento para ordenar tres numeros en orden descendente
void ordenarDescendente(int& num1, int& num2, int& num3) {
    if (num1 < num2)
        intercambiar(num1, num2);
    if (num1 < num3)
        intercambiar(num1, num3);
    if (num2 < num3)
        intercambiar(num2, num3);
}

int main() {
    int num1, num2, num3;

    cout << "Ingrese el primer numero: ";
    cin >> num1;
    cout << "Ingrese el segundo numero: ";
    cin >> num2;
    cout << "Ingrese el tercer numero: ";
    cin >> num3;

    ordenarDescendente(num1, num2, num3);

    cout << "Los numeros en orden descendente son: " << num1 << ", " << num2 << ", " << num3 << endl;

    return 0;
}



Prógrama 3
Hace un programa que muestre 3 números ordenados de ascendentemente,
utilizar un procedimiento para cada operación.
Código 
//Ejecicio 3 _Dominic_Collaguazo_:)//
//Hace un programa que muestre 3 números ordenados de ascendentemente,//
//utilizar un procedimiento para cada operación//
#include <iostream>
#include <iomanip>
using namespace std;
int main(void)
{
    //se declaran tres variables enteras que contendrán los tres números a ordenar                                
    int A, B, C;
    system("cls");
	
    //se introducen los números por teclado
    cout << "\nPrimer numero: ";
    cin >> A;
    cout << "\nSegundo numero: ";
    cin >> B;
    cout << "\nTercer numero: ";
    cin >> C;

    //se realizan las comparaciones para determinar el orden entre ellos                                          
    if(A > B)
       if( B > C)
           cout << C << " " << B << " " << A << endl;
       else if(A > C)
               cout << B << " " << C << " " << A << endl;
            else
               cout << B << " " << A << " " << C << endl;
    else if(B > C)
            if(A > C)
               cout << C << " " << A << " " << B << endl;
            else
               cout << A << " " << C << " " << B << endl;
         else
            cout << A << " " << B << " " << C << endl;
    
    system("pause");
}



Programa 4
Hacer un programa que muestre una tabla de multiplicar hasta el 20 de un número
cualquiera por pantalla, el número se pedirá en el programa principal. Usar procedimiento
Código
//Ejecicio_4_Dominic_Collaguazo_:)//
//Hacer un programa que muestre una tabla de multiplicar hasta el 20 de un número//
//cualquiera por pantalla, el número se pedirá en el programa principal. Usar procedimiento//
#include <iostream>
using namespace std;

void tablaMultiplicar(int num) {
    for (int i = 1; i <= 20; i++) {
        cout << num << " x " << i << " = " << num * i << endl;
    }
}

int main() {
    int num;
    cout << "Ingrese un numero: ";
    cin >> num;
    tablaMultiplicar(num);
    return 0;
}


Programa 5 
Hacer un programa que pida por pantalla una temperatura en grados Celsius,
muestre un menú para convertirlos a Fahrenheit o Kelvin y muestre el equivalente por
pantalla, utilizar funciones
Código 
//Ejercicio_5_Dominic_Collaguazo_:)//
//Hacer un programa que pida por pantalla una temperatura en grados Celsius,//
//muestre un menú para convertirlos a Fahrenheit o Kelvin y muestre el equivalente por//
//pantalla, utilizar funciones//
#include <iostream>
using namespace std;

float celsiusToFahrenheit(float celsius) {
    return (celsius * 9 / 5) + 32;
}

float celsiusToKelvin(float celsius) {
    return celsius + 273.15;
}

int main() {
    float celsius;
    int opcion;

    cout << "Ingrese la temperatura en grados Celsius: ";
    cin >> celsius;

    cout << "Seleccione una opcion:" << endl;
    cout << "1. Convertir a Fahrenheit" << endl;
    cout << "2. Convertir a Kelvin" << endl;
    cin >> opcion;

    switch(opcion) {
        case 1:
            cout << "La temperatura en grados Fahrenheit es: " << celsiusToFahrenheit(celsius) << endl;
            break;
        case 2:
            cout << "La temperatura en grados Kelvin es: " << celsiusToKelvin(celsius) << endl;
            break;
        default:
            cout << "Opción inválida" << endl;
            break;
    }

    return 0;
}


Prógrama 6 
Utilizar la función fopen(), para determinar si existe un archivo de texto (.txt)
o no.
fopen(nombre de archivo , modo);
nombre de archivo = cadena ... contiene el identificar externo del archivo
modo = cadena ... contiene el modo en que va a ser tratado el archivo
Código
//Ejercicio_6_Dominic_Collaguazo_:)//
//Utilizar la función fopen(), para determinar si existe un archivo de texto (.txt)//
//o no.//
//fopen(nombre de archivo , modo);//
//nombre de archivo = cadena ... contiene el identificar externo del archivo//
//modo = cadena ... contiene el modo en que va a ser tratado el archivo//
#include <stdio.h>

int main()
{
    FILE *archivo;
    char nombreArchivo[] = "archivo.txt";

    archivo = fopen(nombreArchivo, "r");

    if (archivo == NULL)
    {
        printf("El archivo no existe.\n");
    }
    else
    {
        printf("El archivo existe.\n");
        fclose(archivo);
    }

    return 0;
}



Prógrama 7
Crear un archivo de texto (.txt), donde guardar los emails de amigos.
fprintf(puntero, informacion);
fwrite(dato a guardar, tamaño, longitud, puntero)
Código 
// Crear un archivo de texto (.txt), donde guardar los emails de amigos.//
//fprintf(puntero, informacion);//
//fwrite(dato a guardar, tamaño, longitud, puntero)//
#include <iostream>
#include <fstream>
using namespace std;

int main() {
  // Crear un archivo de texto
  ofstream archivo("amigos.txt");

  // Escribir en el archivo
  archivo << "amigo1@example.com" << endl;
  archivo << "amigo2@example.com" << endl;
  archivo << "amigo3@example.com" << endl;

  // Cerrar el archivo
  archivo.close();
}


Prógrama 8
Crear un programa en C++, que pueda seguir agregando contactos de email, hacia el
archivo que creamos en el ejercicio 7
Código 
//Ejecicio_4_Dominic_Collaguazo_:)//
//Crear un programa en C++, que pueda seguir agregando contactos de email, hacia el//
//archivo que creamos en el ejercicio 7//
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    string nombre, email;
    ofstream archivo("contactos.txt", ios::app);

    cout << "Ingrese el nombre: ";
    getline(cin, nombre);

    cout << "Ingrese el email: ";
    getline(cin, email);

    archivo << nombre << ", " << email << endl;

    archivo.close();

    return 0;
}

Programa 9 
Hacer una estructura llamada alumno, en la cual se tendrán los siguientes
Campos: Nombre, edad, promedio, pedir datos al usuario para 3 alumnos, comprobar cuál
de los 3 tiene el mejor promedio y posteriormente imprimir los datos del alumno
Código 
//EJERCICIO 2 DOMINIC_COLLAGUAZO_:)//
//Hacer una estructura llamada alumno, en la cual se tendrán los siguientes//
//Campos: Nombre, edad, promedio, pedir datos al usuario para 3 alumnos, comprobar cuál//
//de los 3 tiene el mejor promedio y posteriormente imprimir los datos del alumno//
#include <iostream>
#include <string>

using namespace std;

struct Alumno {
    string nombre;
    int edad;
    float promedio;
};

int main() {
    Alumno alumnos[3];
    float mejor_promedio = 0;
    int mejor_alumno = 0;

    for (int i = 0; i < 3; i++) {
        cout << "Ingrese el nombre del alumno " << i + 1 << ": ";
        getline(cin, alumnos[i].nombre);

        cout << "Ingrese la edad del alumno " << i + 1 << ": ";
        cin >> alumnos[i].edad;

        cout << "Ingrese el promedio del alumno " << i + 1 << ": ";
        cin >> alumnos[i].promedio;

        if (alumnos[i].promedio > mejor_promedio) {
            mejor_promedio = alumnos[i].promedio;
            mejor_alumno = i;
        }

        cin.ignore();
    }

    cout << endl;
    cout << "El alumno con el mejor promedio es: " << endl;
    cout << "Nombre: " << alumnos[mejor_alumno].nombre << endl;
    cout << "Edad: " << alumnos[mejor_alumno].edad << endl;
    cout << "Promedio: " << alumnos[mejor_alumno].promedio << endl;

    return 0;
}


Programa 10 
Pedir al usuario que digite una palabra. luego mostrar la palabra invertida y
comprobar si es capicúa
Código 

//EJERCICIO 2 DOMINIC_COLLAGUAZO_:)//
//Pedir al usuario que digite una palabra. luego mostrar la palabra invertida y//
//comprobar si es capicúa//
#include <iostream>
#include <algorithm>
#include <string>

int main() {
    std::string palabra;
    std::cout << "Introduce una palabra\n";
    std::cin >> palabra;
    std::string invertida(palabra.rbegin(),palabra.rend());
    std::cout << "Palabra invertida: " << invertida << '\n';
}
