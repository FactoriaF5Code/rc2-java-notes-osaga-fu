# APUNTES JAVA

## Cómo funciona

1) El códigoo fuente es compilado en un lenguaje intermedio que no es codigo fuente ni código máquina: __*Bytecode*__

    __Código fuente__ (.java) ==> __COMPILADOR__ ==> __Bytecode__ (.class)

2) A continación la máquina virtual de Java o __*JVM*__ transforma el Bytecode en codigo binario que la máquina puede entender.

    __Bytecode__ (.class) ==> __JVM__ ==> __Código Binario__ (especifico para el SO que se este usando)

## Método Main

Es el punto de entrada a las aplicaciones Java, es decir, nos permite ejecurtar nuestras aplicaciones.

La sintaxis es la siguiente:

```java
public static void main(String[] args) {
    //Aquí nuestro código
}
```
`public` es un modificador que indica que es un método público.

`static` indica que el método pertenece a esta clase, no a sus objetos.

`void` indica que el método no devolverá nada.


## Variables

Java es un lenguaje fuertemente tipado, es decir, debemos especificar a qué tipo de datos pertenece cada variable.

Es un espacio de memoria donde almacenar datos que pueden variar a lo largo de la ejecución de la aplicación.

### Declaración de una variable

Siempre contiene dos partes: el tipo de dato de la variable y el nombre de la variable o identificador.


```java 
String nombre = "Pepito";
```
A partir de la versión 10 se introdujeron también en java las variables dinámicas de manera que no hace falta poner el tipo de dato:

```java
var numero = 10;
```

El nombre de las variables debe escribirse siempre en camelCase.

## Tipos de datos

### 1) Númericos

#### Enteros:

```java
byte entero1 = 1;
short entero2 = 45;
int entero3 = 345;
long entero4 = 123543;
Integer entero5 = 324;
```

#### Decimales:

```java
float decimal1 = 2.5f;
double decimal2 = 10.45d; //la d es opcional
```

### 2) Booleanos

```java
boolean variableBooleana = true;
```

### 3) Texto

```java
char caracter = "a";
String cadenaDeTexto = "Hola a todxs";
```

## Funciones

Es un bloque de código que vamos a poder repetir.  

### Declaración de funciones

```java
tipoDeDatoDevuelve nombreFuncion(tipoDeDatoParametro nombreParametro) {
 //aqui el cuerpo de la funcion
}
```

Cuando nuestra función no devuelve nada debemos poner void en la declaración de la misma:

```java
void showMenu(){
    System.out.println("Este es el menú");
}
```
Cuando nos devuelve algo tenemos que poner el tipo de dato que nos devuelve en la declaración de la función

```java
String getSaludo( String name){
    return "Hello "+ name;
}
```

### Funciones anónimas

Normalmente se le pasan a un método (funciones que pertenecen a una clase y se usan con los objetos de la misma) que en lugar de parámetros recibe una función anónima.

```java
() -> System.out.println("Hola Mundo!");
```  
### Sobrecarga de métodos

Permite duplicar un método o función  siempre y cuando tenga diferente número o tipo de parámetros:

```java
int suma (int numero1, int numero2){
    return numero1 + numero2;
}

int suma( int numero1, int numero2 , int numero3) {
    return numero1 + numero2 + numero3;
}
```
Si el número de parámetros fuese exactamente igual nos daría un error.

## Estructuras de control

### Condicionales

#### IF

```java
int edad = 21;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
}

//otro ejemplo

boolean esMayorDeEdad = edad >= 18;

if (esMayorDeEdad) {
    System.out.println("Eres mayor de edad");
}
```

#### IF ELSE

```java
int edad = 19;

if (edad >= 18){
    System.out.println("Es mayor de edad");
    } else {
    System.out.println("Es menor de edad");
    }
```

#### SWITCH

```java
switch(dia) {
    case "Lunes":
        System.out.println("Animo chavales");
        break;
    case "Martes":
        System.out.println("Dale don dale");
        break;
    case "Miercoles":
        System.out.println("Socorro");
        break;
    default:
        System.out.println("Eso ni es un día ni na!");
        break;
}
```

### Bucles

#### FOR

```java
for (int i = 0; i < 10; i++){
    System.out.println("Hola")
}
//Nos imprimirá Hola 10 veces
```

```java
String[] nombres = { "Pepito", "Menganito", "Fulanito"}

for (int i = 0; i < nombre.length; i++){
    System.out.println(nombres[i]);
}

//Me imprimirá en consola todos los nombres que haya en el Array
```
#### FOR EACH

```java
String[] nombres = { "Pepito", "Menganito", "Fulanito"};

for(String nombre : nombres){
    System.out.println(nombre);
}

//Nos imprime cada uno de los nombres del array
```

```java
int[] numeros = {1, 3, 6}

int suma = 0;

for (int numero : numeros){
    suma += numero;
}
//nos va sumando todos los numeros almacenando el resultado en suma
```

#### WHILE

Es un bucle indeterminado al igual que el do while, no tiene un numero de veces determinado que tiene que durar si no que depende de que se cumpla una condición.

```java
edad = 0;

while ( edad < 18){
    Sytem.out.println("no puedes pasar");
    edad++
}
```
Evalua la condición mientras edad no sea menor que 18 ejecuta el bloque de codigo.  
__CUIDADO__ podemos caer en bucles infinitos si la condición no llega a cumplirse nunca.

Podemos romper un bucle con la palabra `break` o `continue`.  
__BREAK__ rompe el bucle y se detiene en la iteración que lo pongamos   
__CONTINUE__ se salta la iteración donde pongamos el continue