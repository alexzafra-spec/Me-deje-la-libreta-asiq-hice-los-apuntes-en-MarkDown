# Clase 1
## Prevención laboral
### Obligaciones del trabajador
* Usar adecuadamente el material de trabajo
* Usar los EPIs que te proporciona la empresa
* Tener en cuenta las protecciones eléctricas a la hora de usar máquinas
* Explicar y promover las normas
* Informar al empresario de posibles medidas de seguridad
### ¿Dónde tenemos el problema?
 
+ ***Pantalla***: Hay que ajustar la luminosidad, el tamaño y los caracteres. La pantalla debería ser inclinable a voluntad para facilitar el uso y no debe tener reflejos/reverberaciones (rebotes de luz). Para que sea correcto, debe estar a 40-70 cm de la vista.
> [!WARNING]
**La pantalla** es el *mayor problema* para los que trabajamos en informática
 
+ **Teclado**: Debe mantener una postura cómoda para las muñecas y los brazos, y debe estar a 10-15 cm del borde de la mesa.
+ **Mesa**: Debe ser lo suficientemente grande como para poner todo el material ahí sin mucho problema.
+ **La silla** debe ser estable, regulable en altura, y debe proporcionar libertad de movimientos y una postura confortable.
+ **Entorno**: Debe tener una buena temperatura y humedad, y estar correctamente iluminado.
+ **Espalda**: Debe estar recta.
+ Si usamos equipos nuevos (por ejemplo impresoras y/o escáneres), leer el manual y mantenerlos en buen estado. No tocar enchufes con las manos mojadas...
# Clase 2
(pág. 34 aprox.)
## Las redes
### ¿Qué es una red?
Una red es un sistema que permite que varios ordenadores se puedan comunicar entre sí.
 
#### Ventajas
* Comunicación eficiente
* Compartición de archivos
* Flexibilidad y movilidad
* Escalabilidad
* Centralización de datos
* Soporte para nuevas tecnologías
#### Inconvenientes
* Estamos expuestos a ataques cibernéticos
* Costes iniciales altos
* Requiere costes de mantenimiento y gestión
* Es complejo
* Genera dependencia
### Tipos de redes
Se pueden clasificar de muchas formas.
 
#### Tamaño
+ **PAN** (redes Bluetooth, NFC...)
+ **LAN/WLAN** (estilo sala LAN en videojuegos)
+ **MAN**: Metropolitan Area Network
+ **WAN**: Cuando ya te conectas a internet y cubres muchísimas distancias
#### Según transmisión
+ **Punto a punto**: Solo dos ordenadores se unen entre sí para comunicarse
+ **Multipunto**: Un ordenador se comunica con varios ordenadores
#### Según su funcionamiento
+ Entre iguales (P2P)
+ Cliente-servidor → El de toda la vida: pides datos al servidor como cliente y te los da
#### Según el medio de comunicación
+ Sin hilos: Wifi, Bluetooth...
+ Cableada
+ Mixto
### Componentes de una red informática
+ **Repetidor**: Repite una señal que le llega, enviándola amplificada.

![Imagen de un repetidor](https://www.powerplanetonline.com/cdnassets/xiaomi_wifi_extender_n300_blanco_01_l_sf.webp?w=256&q=75&format=webp)
 
![Símbolo de un repetidor](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTE0SNc2KBurW3qaU4fLjkgDb-ScS61CIYHwfvyQVp0zA&s=10)
 
+ **Hub**: Cacharro con muchos agujeros; en cada agujero tienes un equipo conectado. El hub hace de "intermediario". Si el PC1 le quiere enviar un mensaje al PC3, el hub lo manda a todos: el 2 y el 4 lo rechazan y el 3 se lo queda.
![Imagen de un hub](https://www.fibermall.com/blog/wp-content/uploads/2025/03/b-20.png)
 
![Símbolo de un hub](https://png.pngtree.com/png-vector/20220724/ourmid/pngtree-hub-vector-png-image_6046057.png)
 
+ **Switch**: Es la evolución del hub, está más optimizado. Hace un puente internamente para que la información solo le llegue a un sitio, es decir, la lleva a los ordenadores concretos. Es inteligente.

![Imagen de un switch](https://www.simpleinformatica.es/wp-content/uploads/2017/05/switch-8-bocas-e1495722515186.png)

![Símbolo de un switch](https://img.pikbest.com/png-images/20251118/network-switch-with-six-ports-modern-tech-infrastructure-symbol_12264801.jpg)
 
+ **PA**: El punto de acceso es lo que hace que los dispositivos con tarjeta de wifi se conecten a internet y puedan acceder a la red.
![Imagen de un punto de acceso](https://www.fibermall.com/blog/wp-content/uploads/2024/10/5-1.png)
 
![Símbolo de un punto de acceso](https://thumb.wikimedia.org/wikipedia/commons/thumb/5/5c/Router.svg/330px-Router.svg.png)
 
+ **Router**: Conecta diferentes redes entre sí.
![Imagen de un router](https://keenetic.com/storage/uploads/c4d6040a-39f3-4f8f-99da-3a2ece5ad12b.png)
 
![Símbolo de un router](https://thumb.wikimedia.org/wikipedia/commons/thumb/5/55/Router_symbol-Blue.svg/1280px-Router_symbol-Blue.svg.png)
 
> El hub, el switch y el PA se usan para comunicarse dentro de una red.
 
Los routers pueden ser rackeables (se pueden poner en un rack) o empresariales.
Los routers domésticos son SOHO.
 
Una *tabla de enrutamiento* es algo que sirve para que, cuando llega un paquete al router, este sepa dónde enviarlo.
 
### Comando básico
Este muestra dónde se envían los paquetes según su destino.
`ip route show` → Linux
 
![Imagen de Tux, el pingüino de Linux](https://thumb.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/1280px-Tux.svg.png)
 
`netstat -r` → Windows
 
![Imagen del logo de Windows](https://thumb.wikimedia.org/wikipedia/commons/thumb/4/48/Windows_logo_-_2012_%28dark_blue%29.svg/3840px-Windows_logo_-_2012_%28dark_blue%29.svg.png)
 
### La topología de red
La topología de la red es *cómo los equipos están conectados entre sí*.
 
+ **Ethernet/en bus**: Se usa un cable coaxial que une todos los equipos entre sí.
+ **En anillo/Token Ring**: Se espera a que llegue un token; cuando llega, el equipo envía su mensaje y el token se lo da al PC destino. Hay dos cables: si uno se rompe, hay otro de seguridad.
+ **Topología en estrella**: Es un switch donde conectas varios equipos.
+ **Topología en árbol**: Es la evolución de la estrella: son diferentes switches conectados entre sí. Es la que más se usa a gran escala.
+ **En malla**: Todos los equipos están conectados con todos los equipos. Es cara, resiliente y requiere tarjetas de red muy potentes. Tienden a ser pequeñas, pero se usan en estructuras críticas.
> Un token es una señal eléctrica que va dando vueltas en el Token Ring.
 
## Tipos de cableado
Cuando hablamos de medios de comunicación cableados, nos referimos a dos:
1. De cobre trenzado
2. Fibra óptica
### El cable de cobre trenzado
Cable de par trenzado: el LAN del PC. Tiene 8 cables enredados en 4 pares de 2. Es un cable blanco.
 
#### Tipos de trenzado
***T-568 A***:
1. Blanco/verde
2. Verde
3. Blanco/naranja
4. Azul
5. Blanco/azul
6. Naranja
7. Blanco/marrón
8. Marrón
***T-568 B***:
1. Blanco/naranja
2. Naranja
3. Blanco/verde
4. Azul
5. Blanco/azul
6. Verde
7. Blanco/marrón
8. Marrón
> Puedes usar la que quieras, pero solo un tipo por red. Literalmente no hay diferencia, así que coge la más barata, la que tengan en más unidades o la que te pongan.
 
![Comparativa visual de ambos cables](https://www.profesionalreview.com/wp-content/uploads/2020/08/Cable-par-trenzado-crizado-2.png)
 
#### Tipos de cables de cobre trenzado
**U/FTP**: Es el más básico de todos: 4 pares trenzados, cada uno con un hilo de aluminio individual llamado *foil*, y una cubierta exterior de plástico.
 
![Ejemplo visual de U/FTP](https://dintek.com.tw/images/2025/07/14/u_ftp-image-for-article-photoroom.png)
 
**F/FTP**: Coge como base el U/FTP pero agrega un *foil exterior*, una lámina de aluminio que engloba todos los cables.
 
![Ejemplo de F/FTP](https://dintek.com.tw/images/2025/07/14/futp-image-for-article-photoroom.png)
 
**S/FTP**: Como esto es acumulativo, este cable es el F/FTP pero con una malla general metálica.
 
![Ejemplo de S/FTP](https://www.televes.com/media/catalog/product/cache/8b5c4868bcf0d2edd78a91ade7eeafb3/i/p/ipr04190003_1_135775.png)
 
**F/UTP**: Es el opuesto al U/FTP: hay una lámina de aluminio global que envuelve a los cables, pero los pares individuales de hilos no tienen protección.
 
![Ejemplo de F/UTP](https://telecom.samm.com/categora-6a-f-utp-23awg-500mhz-lszh-data-cable-dca-copper-network-cables-samm-teknoloji-16295-14-B.webp)
 
**SF/UTP**: Parte del F/UTP pero agregando un foil con una *shield* (capa de aluminio trenzada).
 
![Ejemplo de SF/UTP](https://cdn-reichelt.de/bilder/web/xxl_ws/E910%2FCAT5PATD.png?type=ProductXxl)
 
Cuantas más capas tienen los cables, más rígidos son: uno rígido te permite doblarlo menos, pero reduce las EMI (interferencias electromagnéticas), que son contaminación eléctrica que hay en el aire pero que nosotros no vemos. Esto puede causar la destrucción de la señal o que no llegue correctamente a su destino.
 
Se usa el conector RJ-45, el LAN de toda la vida.
 
El RJ-45 tiene 8 láminas de color dorado en un extremo. Se meten por el lado opuesto los cables y se compactan con una crimpadora.
 
En función de lo buenos o malos que sean los cables, se les ponen categorías.
 
### La fibra óptica
Se usa un cable con un hilo de plástico especial que tiene diferentes recubrimientos.
 
Tiene dos estructuras:
1. **Ajustada**: Solo pasa un cable dentro.
2. **Holgada**: Tiene varios cables juntos.
Están recubiertos de la siguiente forma:
+ **Núcleo**: El trocito de plástico que envía la información. Hay uno por cada cable.
+ **Revestimiento**: Protección más cercana al núcleo. Hay una por cada cable.
+ **Recubrimiento primario**: Protección general, capa 1.
+ **Recubrimiento secundario**: Lo que vemos.
#### Tipos de cable de fibra óptica
**SM (monomodo)**: Lo que circula por el núcleo no es electricidad sino una luz especial. Solo hay un rayito de luz por ahí. Se usa para distancias largas.
 
**MM (multimodo)**: Permite poner varios rayos de luz que no se mezclan entre sí.
 
### Funcionamiento de los cables de fibra óptica
Pueden funcionar en dos modos: full dúplex o half dúplex.
 
+ **Half dúplex**: Si hay dos PCs comunicándose, solo puede hablar uno.
+ **Full dúplex**: Permite que ambos PCs funcionen a la vez.
## Dispositivos de interconexión de red
+ **Rack**: El armario donde metes los switches, routers...
+ **Patch panel**: Un sitio del rack donde escribes qué ordenador va conectado a ese cable.
+ **Otros elementos**
### Otros elementos
**Adaptador de red**: Tarjeta de red. Pueden ser para fibra óptica o para cable trenzado.
La *tarjeta de red* puede estar incluida en la placa base, o puedes comprar una e insertarla en un puerto PCI.
 
**Velocidad**: Bits/s ≠ Bytes/s
 
**Wake on LAN**: Permite encender el PC desde la red.
 
### Mapa físico y lógico de una red local
#### Mapa físico
Es el plano de una planta que explica cómo están distribuidos los dispositivos entre sí. Explica qué equipos hay, sus nombres y en qué partes están ubicados; cada equipo tiene un nombre.
 
#### Mapa lógico
Explica cómo están conectados los equipos entre sí. En cada equipo aparece su nombre junto a su dirección IP local.
 
> El mapa físico te dice dónde está ubicado cada dispositivo y dónde están los cables, mientras que el mapa lógico te dice dónde están conectados y de qué forma.
