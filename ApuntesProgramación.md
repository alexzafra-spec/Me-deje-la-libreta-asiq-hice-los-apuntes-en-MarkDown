# Clase 1
## Tipus d'errors
**Els errors dels programadors**: La has cagado, no sabes programar, eres tontito, dejalo.
**Errors d'usuari**: Tu usuario es tontito... ¿Cómo no?
**Altres**: 
## Como pasar String a números?
Para pasar de Stirng a int se pone
```java
String nombre="4"
int n = Integrer.parseInt(nombre) //Para convertir a int
double a = Double.parsedouble(nombre) //Para convertir a double
```
Esto se hace para interfaces gráficas y lectura de ficheros. Son como castings pero para strings.

¿Como hago eso?
## La exepciones en Java
### ¿Como leer el mensaje de error?

> [IMPORTANT]
> Para las siguientes lineas usaremos este código de referencia
```java
package mientras;

import java.util.Scanner;

public class Mientras {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Introduce un número: ");
        int numero = sc.nextInt();
        System.out.println("Has escrito: " + numero);
    }
}
```
1. La primera línea tiende a ser la causa del error en el 99,99% de los casos, suele decirte **el que** ha fallado y **porque**  ha fallado
En el mensaje de error seria algo tipo
```java
Exception in thread "main" java.util.InputMismatchException
	at java.base/java.util.Scanner.throwFor(Scanner.java:939)
	at java.base/java.util.Scanner.next(Scanner.java:1594)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2258)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2212)
	at mientras.Mientras.main(Mientras.java:10)
C:\Users\a.zafra\Documents\NetBeansProjects\Mientras\nbproject\build-impl.xml:1330: The following error occurred while executing this line:
C:\Users\a.zafra\Documents\NetBeansProjects\Mientras\nbproject\build-impl.xml:936: Java returned: 1
BUILD FAILED (total time: 6 seconds)
```
Aquí vemos mucho texto y lo normal es que intimide pero nos fijamos en la primera lìnea: `Exception in thread "main" java.util.![alt text](image.png) Aqó podemos ver que en la parte **main** ha habido un error en un imput. Sin embargo "at" que esta justo antes de la primera dirección, en el `at mientras.Mientras.main(Mientras.java:10)` lo cual  quiere decir "te peta esto", no te dice la causa, solo el error. 

Pero esto no se queda en algo tan simple xd

HAY MÁS: 
en la parte de: `InputMismatchException` tienes literalmente el error. Lo cual nos es extremadamente útil para más adelante:
Para que esto no pase lo metemos todo en un `try` y agregamos el `catch`

```java
package buclesalexzafra;

import java.util.InputMismatchException;
import java.util.Scanner;

/**
 *
 * @author a.zafra
 */
public class FADCO {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        try {
            int na = 0;
            System.out.println("Introdueix un nombre:");
            na = s.nextInt();
            System.out.println("hola");
            s.close();
        } catch (InputMismatchException ndr5) {
            System.out.println("No pongas letras");
        }
    }

}
```
Aquí se puede ver esto. En otras palabras: Puedes crear un bucle en el que le pides a un usuario que te meta un int y mantenerlo dentro eternamente hasta que le muy motherfuker te ponga le maleito catch.

> Un solo try puede tener más de un catch, eso es jugoso

## Como hacer un multicatch
Como un catch de toda la vida pero agregando | 

#Java

![Logo Java](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRX4mZCEDMSJuTyD3WMEcpRK76qbrYmvBMW4Ml11M1bvg&s=10)
# Clase 2
Si queremos ordenar los Arrys es un rollo sobretodo cuando són grandes. Hay algoritmos que son automaticos que lo hacen, se hacen de forma automatica.

De forna interna compara pares de numeros entre ellos y va empujando a la derecha el numero que ve hasta que está bien. 
![gif de algoritmo de burbuja](https://stackabuse.s3.amazonaws.com/media/bubble-sort-in-java-1.gif)

Aqui hay un ejemplo
```java
// Java program for implementation
// of Bubble Sort

class BubbleSort {  
    void bubbleSort(int arr[])
    {
        int n = arr.length;
      
        for (int i = 0; i < n - 1; i++)
            for (int j = 0; j < n - i - 1; j++)
                if (arr[j] > arr[j + 1]) {
                  
                    // swap temp and arr[i]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
    }

    // Driver method to test above
    public static void main(String args[])
    {
        BubbleSort ob = new BubbleSort();
        int a[] = { 64, 34, 25, 12 };
      
        ob.bubbleSort(a);
      
      	int n = a.length;
      
        for (int i = 0; i < n; ++i)
            System.out.print(a[i] + " ");
        System.out.println();
    }
}

// Output: 12 25 34 64 
```
No hay que poner archivos ni proyectos que se llame arrays//array
Actualmente se pone así
```java
Arrays.sort(notes)
```
Si quieres Strings te los ordena según tablas ascii. Sigue orden alfabetico poniendo arriba las mayúsculas.

El .toCharArry
## Como conseguir las letras de una palabra
```java
String palabra = "Electricidad";
char[] letras = palabra.toCharArray(); // Con esto separamos las letras
 ```

 Con esto puedes ordenar las letras y ver si es un anagrama o no. Osea puedes poner: `Arrays.sort(var)` para que se ordene y luego un bucle que compare uno a uno.
