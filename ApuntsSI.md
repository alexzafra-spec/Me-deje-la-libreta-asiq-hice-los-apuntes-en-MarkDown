Wide Area Network
> estos comandos sirven para: 
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