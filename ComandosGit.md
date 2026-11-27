# Clase 1

Abans de tocar comandaments (que desafortunadament tocarem) paralarem de GIT d'una forma diferent. No ho hem de veure com un enemic (encarà que ho sembla i es comporta com a tal) però ho fatrem de bona fe. No hem de pensar en una cosa pesada o una cosa a la qual enfrentar-nos, sinó més bé com una eina amb molt potencial que hem de saber aprofitar.
## Introducció
### Queè és GIT?
Quan fas una cosa i li fas molt canvis i arriba un moment en el qual ja no saps què és què. GIT és la resposta. Et permet gestionar les versions i restaurar versions diferents. Quan treballes en grup aixpo és pitjor encarà, per això GIT és una bona solució.
### Què és GIT?
> GIT és **la solució** a aquests problemes
En concret permet:
+ **Recordar** cada versió del teu projecte
+ **Viatjar en el temps** Restaurar versions anteriors a l'instant
+ **Treballar en paralel i gestió de conflictes** Aquesta és una part maca d'ell. Pots resoldre conflictes i que diferents persones treballin en coses diferents o fins i tot en la mateixa cosa amb més faciltat
### La filosofia de GIT
Per entendré millor hem d'entendre bé el que cerquen:

1. Eliminar la por a equivocar-se
2. Tothom té tota l'historia, potser una cosa d'una versió anterior què una persona no va poder desenvolupar bé en l'actualitat una altre li fa tres retocs i li sembla un diamant en brut.
3. No et deixa modificar les versions pasades: Per guardar els cambis que facis has de fer un altre commit per tant si per cojons has de tornar enrrera i no pots tens una alternativa disponible.
4. Ràpid i local
5. Branquificar és nromal i no experimental
### Les branques
#### Què són?
Les branques són línees de treball independients entre ells. Ho pensarem com a conducció

Main: L'autopista, la carretera principal

La resta: Sortides, hi han sortides d'autopistes a carreteres de poble les quals també poden tenir sortides als pobles.
#### Per a que serveixen?
El pròposit principal de les branques és aillar el treball. *si, ara som antisocials*, pots ser antosicial sense entendre això però no pots entendre això sense ser antisocial.


Permet fer moltes coses a la vegada i que la branca principal sempre funcioni. Una cosa deixa de funcionar? Pots restaurar versions anteriors.


Això també és molt bo perque pots fer tants experiments com poguis sense por a equivocar-te i en aquestes situacions és quan et pots donar més soltura a tu mateix sense por de carregar-te gens important


A més fer revisions i un seguiment del progres mai habia estat tant fàcil, no?
#### Què fas quan treballes amb les branques
+ Pots crear noves "linees del temps"
+ Moure't entre les diferents línees del temps
+ Mirar els cambis
+ Unir versions
+ Fer revisions
+ Descartar contingut
+ Compartir el contingut amb la resta del teu equip
### Com funciona GIT?  
Git està pensat per fer un control de versions i treballar a l'hora en diferents dispositius.

És com una màquina del temps que permet fer diferents viatges en el temps, crear linees del temps, fusionar-les... Cada branca és una linea del temps i cada comit és una instant d'aquella branca.
### Quan surt a comptes fer servir GIT?
Abans de tocar temes de funcionament hem de saber quan renta i quan no renta fer servir GIT. Renta quan:

Programes, practicament en tots els casos.
Treballes amb equip en un tema sensible
En qualsevol tema sensible en realitat
En projectes a molt llarg termini i temes o vols trobar una cosa que va fallar
Probar idees arriscades
### Quan no surt a comptes fer servir GIT?
Ja que hem explicat quan renta és hora d'explicar quan no és una bona idea

En arxius exageradament pessats
Documetns d'edició en temps real com google docs
Quan fas coses de fer servir i llençar
Ammb dades sensibles
### Aventatges de GIT
1. Tens tota la informació
2. Pots crear moltes rames sense problema
3. És molt escalable
4. És ràpid i no depends d'un extern
5. Facilita la integritat
6. Codi obert
7. És l'estàndar actual a l'industria
8. Compatibilitat multidispositiu
### Inconvenients de GIT
1. Curva d'apenentratge plena de fricció
2. Els conflictes dels mergem s'han de resoldre a mà (no és díficil, ja parlarem d'això en un futur)
3. Pot convertir-se en un repositori molt pessat si arrastra totes les versions anteriors
4. Requireix disciplina
5. És assumir un risc amb les dades sensibles
### Els comits
#### Que és un commit?
En aquesta part ja sabem què un commit és un punt de guardat del projecte, és la unitat bàsica de git.

**Inclou**
+ L'instant en si
+ Autor i data
+ Missatge de guardat - És obligatori (crec)
+ Referencia del commit anterior
+ *Hash*: un identificador únic per a aquest commit 
#### 3 zones
Els commits estàn diviidits internament en tres zones:

1. **Zona de treball**: El que edites lliurament
2. **Staging**: Les parts en las que ja has treballat i estàn esperant per fer cambis
3. **Historial**
### Local vs remot

`git status` -> Et mostra que ha cambiat
`git commit -m "gergarsrnrñr"` -> Fa un commit i et deixa personalitzar el missastge
`git ad .` -> Prepara tots els arxius