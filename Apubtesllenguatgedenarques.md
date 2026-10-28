# RA4
## Mecanismes de validació de documents
### Tipus Simples
Tienes documentos: el XML y el XSD. El **XSD** es lo que se encarga de que tu XML se vea como tu quieres.

> **XSD**: XML Schema Verification

Define que la información sea como a ti te interesa que quieras. Para que esto funcione, necesitamos *decirle a cada XML cual es el XSD que le valida*

Esto se hace así:
```XML
<nodeArrell xmkls:"http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation="esquema.xsd">
    <node>info</node>
</nodeArrell>
```
Tanto en la práctica como en el examen la profesora nos dara el XML.

Todas las lineas empiezan así: ``

Llamamos a los nodos "Element". Es algo como 
```XSD
<xs:element name="nomDelElement" type="xs:integer"/> <!-- Enteros -->
<xs:element name="nomDelElement" type="xs:decimal"/> <!--Reales -->
<xs:element name="nomDelElement" type="xs:boolean"/> <!--Decimales -->
<xs:element name="nomDelElement" type="xs:string"/> <!--String -->
<xs:element name="nomDelElement" type="xs:date"/> <!-- Dates AAAA-MM-DD -->
<xs:element name="nomDelElement" type="xs:time"/> <!-- Hora en format format HH:MM:SS--> 
<xs:element name="any" type="xs:gYear"/> <!-- Any-->
<xs:element name="nomDelElement" type="xs:string" default="red"/> <!-- Que si l'usuari no ha introduit cap color que el predeterminat sigui el vermell -->
<xs:element name="color" type="xs:string" fixed="red"/> <!-- Seria l'equivalent a una constatn en Java, fixa el color a vermell sense posibilitat de cambiar-ho -->
```
### Tipus complexes
Ejemplo para pillarlo ez:
```XSD
<xs:schema xmlns:xs"http://www.w3.org/2001/XMLSchema"> <!-- Linea predeternibada del principio, no pones el nombre del XML que cuelga del XSD. Eso se pone en el XML, no es necesario rallarse por eso -->
    <xs:element name="dispositius"> <!-- Abrimos un nodo -->
        <xs:complexType> <!-- Lo declaras como un XML complejo -->
            <xs:sequence> <!-- Per poder fer sequencies -->
                <xs: element name="nom" type="xs.string">
                <xs: element name="bateria" type="xs.integer">
            </xs:sequence>
        </xs:complezType>
    </xs:element>
</xs:schema>
```XSD
Ahora imaginate un ti

<xs:ekenebt name="person">
        <person>
            <employee>
        </person>
            <client>
        </person>
```
El maxOccurs="x" y minOccurs="x" sirven para marcar un máximo y un mínimo de veces que puade aparecer un nodo, se usa mucho para campos opcionales. No es necesario poner ambos, con solo ubo ya vale.

> Cuando pones ***minOccurs="0"*** quiere decir que hasta con eso vacío ira bien, osea que ni siquiera es obligatorio ponerlo.
> Para poder poner una cantidad de nodos hay que poner ***maxOccurs="unbounded"

Para poner un compledjo dentro de otro complejo hay que poner:
```XSD
<xs:schema xmlns:xs"http://www.w3.org/2001/XMLSchema"> <!-- Linea predeternibada del principio, no pones el nombre del XML que cuelga del XSD. Eso se pone en el XML, no es necesario rallarse por eso -->
    <xs:element name="dispositius">
        <xs:complexType>
            <xs:sequence> <!-- Per poder fer una sequencia encara que no és el cas -->
                <xs: element name="sensor" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs: element name="nom" type="xs.string">
                          <xs: element name="bateria" type="xs.integer">
                        </xs:sequence>
                    </xs:complexType>
                </xs:element name="sensor">
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>
```
> [!IMPORTANT]
> En el examen nos daran un código XML para que hagamos su XSD. Este tendrá limitaciones, restricciones, etc. Tendrás que hacer el examen en papel


> [!TIP]
> 1. Líneas, escribir a lapíz lineas
> 2. EscribiR a lapíz los nodos abiertos y cerrados
> 3. Dejar la estructura de tabulación, es más útil de lo que parece
> 4. Por favor si alguien se sabe más trucos que me lo diga por favor

Hay que repetir la estructura.
### Ejemplo

Para este código XML;
```XML
<registros  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xsi:noNamespaceSchemaLocation="act2.xsd"> <!-- Recuerda que está línea es para vÍncular un XML a un XSD -->
    
    <usuario>
        <id>101</id>
        <nombre>Eva</nombre>
        <segundoNombre>María</segundoNombre>
        <apellido>Molina</apellido>
        <correo>eva@ejemplo.com</correo>
    </usuario>
    <usuario>
        <id>102</id>
        <nombre>Ana</nombre>
        <apellido>Márquez</apellido>
        <correo>ana@ejemplo.com</correo>
    </usuario>
</registros>
```
Su XSD es;
```XSD
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="registros">
    <xs:complexType>
      <xs:sequence>
         <xs:element name="usuario" maxOccurs="unbounded">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="id" type="xs:integer"/>
                  <xs:element name="nombre" type="xs:string"/>
                  <xs:element name="segundoNombre" type="xs:string" minOccurs="0"/>
                  <xs:element name="apellido" type="xs:string"/>
                  <xs:element name="correo" type="xs:string"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
      </xs:sequence>
    </xs:complexType>
 </xs:element>
</xs:schema> 
```
