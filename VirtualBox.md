Virtualització. Configuració de màquines virtuals.

1. Què és un Sistema de Virtualització?
   En informàtica un sistema de virtualització es refereix a la creació a través de Programari d'un recurs tecnològic, aquest pot ser un ordinador físic complet, o altres recursos de maquinari.

Ens ofereix una abstracció dels recursos maquinari d'un ordinador a través del que anomenarem Hypervisor. Els sistemes virtualitzats han estat un gran avanç en les tecnologies de la informació, els avantatges d'aquests sistemes pel que fa a aprofitament de recursos han fet que siguin una opció cada vegada més usada en els sistemes d'informació inclosos els servidors.

Ara és possible fer pràctiques que abans eren inviables de dur a terme en una classe ordinària per la insuficiència de recursos maquinari, o pels problemes derivats de realitzar-les.

Per posar algun exemple, quan s'estudia la interconnexió d'ordinadors en xarxa, abans era necessària la coordinació d'un mínim de dos ordinadors amb els seus respectius alumnes per fer les proves, mentre que ara es poden fer usant una sola màquina amfitriona i una altra virtualitzada. Un altre clar exemple, és la instal·lació de diversos sistemes operatius en la mateixa màquina sense perill que un mal pas modifiqui l'arrencada, o alteri accidentalment particions d'algun dels sistemes que es pretenia fer "conviure" en el mateix sistema.

En el model de màquines virtuals es crea un sistema client / servidor on cada client actuarà com un sistema virtual d'el maquinari sobre el qual està implementat. Els avantatges d'aquest sistema enfront d'altres per a realitzar les proves aquest model no modifica en cap moment el sistema sobre el qual s'instal·la. En aquest model hi ha un administrador dels recursos maquinari anomenat Hypervisor, o monitor de màquina virtual que serà l'encarregat de fer les peticions a la CPU i administrar els privilegis en aquestes peticions. En el nostre cas VirtualBox serà aquest Hypervisor

Una màquina virtual és un contenidor de programari perfectament aïllat que pot executar els seus propis sistemes operatius i aplicacions com si fos un ordinador físic. La màquina virtual es comporta exactament igual que un ordinador físic i conté la seva pròpia CPU virtual, memòria, disc dur, targeta d'interfície de xarxa ...

A tots els efectes una màquina virtual es considera com una màquina amb el seu sistema operatiu propi fins i tot els altres ordinadors de la xarxa així ho veuran. Tot i que no hem d'oblidar que en realitat tot està basat en programari. Això ens reporta una sèrie d'avantatges i algun inconvenient.

1.1.Guest i Host:
A mesura que anem llegint documentació veurem moltes maneres de referir-se a les màquines virtualitzades i als hypervisores. Una de les nomenclatures que més pot aparèixer són les paraules Guest i Host: Guest (convidat) és la màquina virtualitzada, la que viu "dins" de la màquina real. Host (amfitrió) és la màquina real, la qual disposa de maquinari real i virtualitza les altres.

1.2.Avantatges de la Virtualització
El principal avantatge de la virtualització és poder tenir diversos sistemes dins d'un sol maquinari físic com si de diverses màquines amb els seus respectius components maquinari es tractés, sent independents els uns dels altres.

Altres de les avantatges són:

    • Els usuaris veuran els recursos que fan servir com si fossin dedicats.
    • Una administració centralitzada.
    • Facilita fer recursos més homogenis arribant a estandarditzar-.
    • Suporta traslladar sistemes i configuracions d'un sistema a un altre, fins i tot en "calent".
    • Augmenta la flexibilitat i aprofitament de recursos i consum elèctric.
    • Millora la tolerància a fallades, si cau un sistema els altres segueixen inalterats.
    • Facilita les còpies de seguretat.

1.3.Desavantatges de la Virtualització
El principal desavantatge de la virtualització, és que lògicament el sistema principal que suportés les màquines virtuals, ha de disposar d'una major quantitat i potència de recursos a major nombre de sistemes vulguem tenir virtualitzats en ell. Els components principals que determinaran el nombre de màquines virtuals que es podran suportar sobre un maquinari i el rendiment de cadascuna d'elles són: la quantitat i velocitat de memòria RAM, la potència de l'processador i la velocitat de lectura, accés i transferència de el disc dur, encara que hi ha més factors que determinaran el rendiment final de el sistema.

Una altra de les desavantatges és que en ocasions apareixen problemes en la compatibilitat amb el maquinari virtualitzat, encara que en les últimesnversions dels programes de virtualització aquests problemes no es presenten gairebé mai. També podríem comptar com a desavantatge que encara ens és difícil de configurar determinats recursos en màquines virtualitzades, en ocasions per enteniment i altres per limitacions de l'propi programari de virtualització.

2.Tipus de virtualització
Hi ha dos grans grups de Virtualizadores, o Hypervisores:

2.1.ParaVirtualització:
També denominat nadiu o barem metall (sobre el metall nu), és programari que s'executa directament sobre el maquinari, per oferir la funcionalitat descrita. En aquest cas el maquinari aquesta compartit entre les maquines virtuals i el Sistema Operatiu que allotja a l'Hypervisor, d'aquesta manera els recursos poden ser utilitzats de manera més adequada. Ja que cada un dels sistemes instal·lats gestiona els recursos físics, permet un millor aprofitament dels mateixos.

Exemples d’aquesta tecnologia:
• VMwware ESXi Free (gratis)
• VMware ESX (de pago)
• Docker
• Microsoft Hyper-V Server (gratis)
• Proxmox (gratis/de pago)

2.2.Virtualització completa:
També anomenat completa, ja que la virtualització virtualitza tot el maquinari. Requereix de més recursos per a realitzar la virtualització, ja que el sistema operatiu de la màquina amfitriona ha de gestionar tots els recursos, tant els discos durs, la memòria RAM, el microprocessador, etc.
Exemples :
• VirtualBox (gratis)
• VirtualBox OSE (libre)
• VMware Workstation (de pago)
• QEMU (libre)
