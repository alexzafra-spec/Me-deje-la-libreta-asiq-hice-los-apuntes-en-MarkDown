# Clase 1
## Prevención laboral
### Obligaciones del trabajador
* Usar adecuadametne el material de trabajao
* Usar los epis que te proporciona la empresa
* Tener en cuanta las protecciones electricas a la hora de usar maquinas
* Expandir las normas
* Informar al empresario de posibles medidas de seguridad
### ¿Donde tenemos el problema?

+ ***Pantalla***: Hay que ajustar la luminosiadad el tamaño y los caracteres, la pantalla debería ser inclinable a voluntad para facilitar ni debe tener reflejaos/reberberaciones (rebotes de luz) para que sea corrrecto debe estar 40-70cm de la vista.

> [!WARNING]
**La pantalla** es el *mayor problema* para los que trabajamos en ifnormatica

+ **Teclado**: Debe de mantener una postura comoda para las muñecas y los brazos, debe de estar 10-15cm alejados del borde de la mesa.

+ **Mesa**: Debe ser lo suficientemente grande como para poner todo el amterial ahí sin mucho problema.

+ **La silla** debe de ser estable regulable en altura debe proporcionar libertad de movimientos y proporcionar una postara confortable

+ **Entorno**: Debe de tener una buena temperatura, humedad y debe estar correctamente iluminado.

+ Espalda debe estar recta

+ Si usamos equipos nuevos ex impresiores y/o escanaeres leer el manual y mantenerlo en buen estado, no tocar enchufes con las manos mojadas...

# Clase 2
(pag 34 aprox)
## Las redes
### ¿Que es una red?
Una red es una cosa qe permite que varios ordenadores se puedan comunicar entre si

#### Ventajas
* Comunicación eficiente
* Compartición de archivos
* Flexibilidad y movilidad
* Escalabilidad
* Centralización de datos
* Soporte para nuevas tecnologías.
#### inconvenientes
* Estamos expuestos a ataques ciberneticos
* Costes iniciales altos
* Requiere costes de mantenimiento y gestiones
* Es complejo
* Genera dependencía
### Tipos de redes
Se pueden clasificar de muchas formas

#### Tamaño
**Pan** (Redes blouetooth, nfc...)
**Lan/Wlan** (Estilo sala LAN en videojuegos)
**Man**: Metropolitan Xarxa Area
**One**: Cuando ya te conectas a internet y cubres muchisimas distancías
#### Segun transmisión:
**Punto a punto**: Solo dos ordebadores se unen entre si para comunicarse
**Multipunto**: Un ordenador se comunica con varios ordenadores

Según su función
Entre iguales (P2P)

Cliente Servidor
El de toda la vida, pides datos al servidor como cliente y te los da

Según el medio de comuncación
Sin hilos Wifi, bluetooth...
Cableada
Mixto

Componentes de una red informatica:
+ **Repetidor**: Repite una señal que le envia una amplificada
+ **Hub**: cacharro con muchos agujeros, en cada agujero tienes un equipo conectado. El hub hace de "intermediatio". Pc1 le quiere enviar un mensaje a PC3, Hub lo manda a todos el 2 y el 4 lo rechazan y el 4 se lo queda
+ **Switch**: Es la evolución del Switch, está más optimizado, hace un puente internamente para que la infó solo le llegue a un sitio para llevarlo a los ordenadores concretos, es inteligente.
+ **PA**: El punto de acceso es lo que hace que los dispositivos con tarjeta de wifi se conecten a internet y puedan acceder a la red
+ **Router**: Conecta diferentes redes entre si

> El Hub, Switch y PA se usan para comunicarse dentro de una red

Los routers pueden ser rackeables (se puede poner en un rack) o empresarial
Los routers domesticos son Soho

Una tabla de enlazamiento, es algo que sirve para que cuando llega un paquete al router, este sepa donde enviarlo

Comandos básicos:
ip rout show Linux
netstat -r Windowa

Topologia de red:
La topologia de la red es como están conectados los equipos entre si.

+ Ethernet/en bus: Se usa un cable coaxial, une todos los equipos entre si
+ En anillo/Token Ring: Espera a que le llegue un token, cuando llega a el se lo envia y el token se lo da al pc destino, hay dos cables, si uno se rompe hay otro de seguiridad
+ Topologia estrella: Es un switch donde conectas varios equipos
+ Topologia en arbol: Es le evolución de la de estrella, son diferentes Switchs conectados entre si, es la que más se usa a gran escala
+ En malla: Todos los equipos están conectados con todos los equipos, es caro, resiliente y requiere tarjetas de redes muy potentes, tienden a ser pequeñas pero se usan en estructuras crliticas.
> Un token es una señal electrica que va dando vueltas en el token ring.

Tipo de cableado
Cuando hablamos de medios de comunicación cableado nos referimos de dos:

Coble de par trenzado: El LAN del PC, tiene 8 cables enredados de 2 en 4 pares de 2, es un cable blanco

U/FTP: cable con los 4 cables enrollados
F/FTP: El U/FTP pero con cables puestos
S/FTP: F/FTP + malla
F/UTP: Se agrega aluminio
SF/UTP: agrega otra capa más

Entre mas cosas tengan los cables son más rigidos, uno rigido te permite girarlo menos pero reduce las EMI (interferencias electromagneticas), contaminación electrica que hay en el aire pero que nosotors no la vemos, esto puede causar su destrucción o que no llegue correctamente a su destino.

Se sa el conector RJ-45, el LAN de toda la vida.

En un extremo tiene 8 laminas por de color dorado, se meten por el lado puestom se apretan con la gripadora,

Se pueden poner de dos formas:

T-568 B
T-568 B

> Puedes usar la que quieras pero solo un tipo por red

En función de lo buenos o malos que sean los cables se le ponen categorías.

Que un cable sea más grande que otro varia en el ancho de banda, el ancho de banda es la cantidad que puede pasar por ahí

La Fibra Optica

Se usa un cable con un hilo de pastico especial que tiene diferentes recubrimientos;

Tiene dos estructuras:
Ajustada
Ajustada

Revestimiento
Recubrimeinto Primario
Recubrimiento Secundario (lo q vemos)

Sm (Mono Modo): Lo que circula por el núcleo no es electricidad sinó una luz especial, solo hay un rayito de luz por ahí.
MM (Multi Modo): Permite poner varios rayos de luz que no se mezcalan entre si.

Dispositivos de interconexión:

Rack, el armario dnd metes los Switches, Routers...
Patch panel: Un sitio donde escribes que ordenador va conectado a ese cable
Otros elementos

Adaptador de red: Tarjeta de red; Pueden ser para fibra optica o para cable trenzado
La tarjeta de red puede estar incluida en la placa base o comprar una e insertarla en un puerto PCI
Pueden funcionar en dos modos: Full Dúplex o Half Dúplex

Half: Dúplex: Si hay dos PCs comunicandose solo puede hablar uno
Full Dúplex: Permite que ambos PCs funcionen a la vez

Velocidad Vits/sec!=Bites/sec
Wake On Lan: Permite encender el PC dsd la red

### 1.9 Mapa físico y Lógico de una web local
El mapa físico 
Es el plano de una planta que explica como estan distribuidos los dispositivos entre si. Explica que equipos, nombres y en que partes estan los equipos, cada equio tiene un nombre
Mapa Lógico
Explica como esan connectados los equipos enter si, en cada equipo esta su nombre junto a su dirección IP local

> Mapa fisico te dice donde esta ubicado cada dispositivo y donde esán los cables, mientras que el mapa logíco te deice donde estan conectados y de que forma
