# Testing con Junit

Este es un ejemplo sencillo de pruebas unitarias usando Junit 5

Observa que este proyecto no tiene ninguna clase con el método `main`, no nos hace fatal. Además, tampoco tiene ningún `scanner` ni ningún `print`.

Haz un fork de este proyecto en tu repositorio de Github y contesta a las siguientes preguntas:

1. ¿Qué sentido puede tener este proyecto y para que lo podrías usar?

-Sirve para realizar pruebas asegurandose que la calculadora funciona correctamente hacia las operaciones como debe.

2. Revisa las pruebas de la suma y comenta lo que te parezca de interés

-Que hay 3 tests distintos una suma normal, una suma mal hecha aproposito y un test multiple donde se suma normal 2 veces con distintos numeros se suma con cero y se suman un negativo y un positivo. Me parece curioso que se repita el test de sumar normal 3 veces, en el primer test y luego dos veces más en el test multiple también que no se prube a sumar 2 negativos. 

3. Realiza un estudio de caja negra de la división e implementa las pruebas en junit: Se realizará en markdown.

-Tendremos que comprobar los siguientes casos:
 división de 2 numeros positivos; entrada 8/2, salida esparada 4
 división de un 1 positivo y un negativo; 8/-2, salida esperada -4
 divsion de 2 numeros negativos; -10/-2, salida esperada 5
 division de un numero entre 0; 4/0, salida esperada excepción OperacionNoValidaException

 -Implementacion en junit;

@Test
    void dividirPositivos() {

        int valor1 = 8;
        int valor2 = 2;
        int esperado = 4;

        assertEquals(esperado, Calculadora.dividir(valor1, valor2));
    }

    @Test
    void dividirPositivoyNegativo() {

        int valor1 = 8;
        int valor2 = -2;
        int esperado = 4;

        assertEquals(esperado, Calculadora.dividir(valor1, valor2));
    }

    @Test
    void dividirNegativos() {

        int valor1 = -10;
        int valor2 = -2;
        int esperado = 5;

        assertEquals(esperado, Calculadora.dividir(valor1, valor2));
    }

 La prueba de división por cero ya está implementada correctamente en el proyecto:

## Instrucciones

El alumno deberá hacer un fork de este proyecto e implementar la solución solicitada (preguntas y código).

>Se deberá utilizar este fichero, y los artefactos de código del proyecto, para resolver el ejercicio.


**Si no se puede acceder al repositorio la evaluación del ejercicio será de 0. No se evaluarán entregas modificadas/entregadas fuera del plazo establecido en la tarea**