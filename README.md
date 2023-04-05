# estructura-de-datos-c

#include <iostream>
#include "triangulo.h"
using namespace std;
int main()
{
    triangulo triangulo1;
    float x, y;
    cout << "ingrese los datos de base :";
    cin >> x;
    cout << "ingrese los datos de la altura:";
    cin >> y;
    triangulo triangulo2(7, 10);
    cout << "el area del triangulo es :" << triangulo1.calculararea(x, y);
    cout << "el area es :" << triangulo2.calculararea(x, y);
    cout << "la base es en el triangulo 1 : " << triangulo1.getbase() << endl;
    cout << "la base en el triangulo dos es : " << triangulo2.getbase()<< endl;
    triangulo1.setbase(x);

}


triangulo .h 
//Declaracion de la clase
class triangulo
{
	// Atributos - Variables
private:
	float base;
	float altura;
	float area;
	//Metodos - Funciones
public:
	triangulo(float a, float b);
	triangulo(void); //Constructor - asigna memoria 
	~triangulo(void); //Deestructor - libera memoria
	//Prototipos
	float calculararea(float b, float h);
	float getbase();
	void setbase(float b);
};

triangulo cpp 
#include "triangulo.h"
//Implementacion de los metodos de la clase
//Declaracion del constructor
triangulo::triangulo(void)
{
	base = 4;
	altura = 3;
}
triangulo :: triangulo (float b, float h )
{
	base = b;
	altura = h;
}
//Declaracion del destructor
triangulo::~triangulo(void)
{
}
//Declaración del metodo - funcion
float triangulo::calculararea(float b, float h)
{
	area = (b * h) / 2;
	return area;
}

float triangulo:: getbase ()
{
	return base;

}
void  triangulo::setbase(float b)
{
	base = b;
}
