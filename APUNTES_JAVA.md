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