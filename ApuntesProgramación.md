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
#Java

> Un solo try puede tener más de un catch, eso es jugoso

Los catch tienen nombres y NetBeans se queja si lo haces mal, así que sin problemas

## Como hacer un multicatch
Como un catch de toda la vida pero agregando | 
#Java
![Logo Java](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRX4mZCEDMSJuTyD3WMEcpRK76qbrYmvBMW4Ml11M1bvg&s=10)
