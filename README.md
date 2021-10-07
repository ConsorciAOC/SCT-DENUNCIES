# SCT-PDA
Documentació d'integració del servei SCT-PDA del Consorci AOC.


![Shape1](RackMultipart20211007-4-lhpxvq_html_5602d5d1052c90d7.gif) ![Shape2](RackMultipart20211007-4-lhpxvq_html_3e4607557e4024fb.gif)

![](RackMultipart20211007-4-lhpxvq_html_9a7a6ca44ec1f4e7.png)

![Shape3](RackMultipart20211007-4-lhpxvq_html_1b8fb08c0870b915.gif)
 ![Shape4](RackMultipart20211007-4-lhpxvq_html_201e7ff272053041.gif)

# **Via**

#

# **Oberta**

#

# **–**

#

# **SCT**

#

# **Denúncies**

# **Documentd&#39;integraciódelservei**

![Shape5](RackMultipart20211007-4-lhpxvq_html_34bb42a41399ce18.gif)
 ![Shape6](RackMultipart20211007-4-lhpxvq_html_88f2446ea12b4e83.gif)

![](RackMultipart20211007-4-lhpxvq_html_9ee666534977765a.png)

Realitzat per: Àrea de Tecnologia - ProjectesVersió: 1.1

Data:17/5/2021

**Control del**** document**

**Informació**** general**

|
**Títol:** |
ViaOberta –SCTDenúncies |
| --- | --- |
|
**Creatper:** |
ÀreadeTecnologia -Projectes |
|
**Arevisarper:** |
ÀreadeTecnologia -SuportTècnic |
|
**Aaprovarper:** |
ÀreadeTecnologia-SuportTècnic |
|
**Llistadedistribució:** |
 |
|
**Nomdeldocument:** |
DI-ViaOberta-SCTDenúncies.doc |

**Històric**** de ****revisions**

|
**Versió** |
**Data** |
**Autor** |
**Comentaris** |
| --- | --- | --- | --- |
|
V1.0 |
23/02/2013 |
CarlosMenaFernandez |
Creaciódeldocument |
| --- | --- | --- | --- |
|
V1.1 |
13/04/2021 |
RogerNoguerai Arnau |
Recuperaciódelserveiirevisiódel |
| --- | --- | --- | --- |
|
 |
 |
 | càlculdeldígitdecontroldel&#39;expedient. |
|
 |
 |
ServeiCatalàdeTrànsit |
Revisió del càlcul de lalínia de |
|
 |
 |
 | cobrament,codidebarresitextdels |
|
 |
 |
 | avisoslegals aincloureenlesbutlletes. |
|
 |
 |
 |
 |
| --- | --- | --- | --- |
|
 |
 |
 |
 |
| --- | --- | --- | --- |
|
 |
 |
 |
 |
| --- | --- | --- | --- |
|
 |
 |
 |
 |
| --- | --- | --- | --- |

**Índex**

1. [Introducció 1](#_bookmark0)
2. [Transmissionsdedades disponibles 1](#_bookmark1)
3. [Missatgeria dels serveis 1](#_bookmark2)
  1. [Enviamentderemesadebutlletes (SCT\_REMESA) 1](#_bookmark3)
    1. [Petició–dades genèriques 1](#_bookmark4)
    2. [Remesa 2](#_bookmark5)
    3. [Resposta específica 11](#_bookmark9)
  2. [Obtencióderangde butlletes (SCT\_BUTLLETES) 15](#_bookmark12)
    1. [Petició–dades específiques 16](#_bookmark13)
    2. [Resposta–dades específiques 16](#_bookmark14)
  3. [Descàrregadelcatàlegde normatives (SCT\_CATALEG) 17](#_bookmark15)
    1. [Petició–dades específiques 17](#_bookmark16)
    2. [Resposta–dades específiques 17](#_bookmark17)

[Annexes 19](#_bookmark18)

[Càlculdeldígitdecontrold&#39;unnúmerod&#39;expedient19](#_bookmark19)

[Líniadecobrament icodidebarresd&#39;unabutlletadesanció20](#_bookmark20)

[Líniadecobrament 20](#_bookmark21)

[Codidebarres 22](#_bookmark22)

[Textdelsavisos legalsaincloureenlesbutlletes 23](#_bookmark23)

1.
# Introducció

Aquestdocumentdetallalamissatgeriaassociadaalserveid&#39;enviamentdedenúnciesalServeiCatalàdeTrànsit(enendavantSCT).

Perapoderrealitzar laintegraciócalconèixerprèviamentlasegüentdocumentació:

- DocumentdeMissatgeriaGenèricade laPCI delConsorciAOC.

1.
# Transmissionsdedadesdisponibles

Lesdadesdisponiblesa travésdel serveisón lesqueespresentenacontinuació:

| **EMISSOR** |
| --- |
| ServeiCatalàdeTrànsit |
| **PRODUCTE** | **MODALITAT** | **DESCRIPCIO** |
| **SCT\_DENUNCIES** | SCT\_REMESA | Enviamentderemesadebutlletes(frontal **asíncron** de laPCI). |
| SCT\_BUTLLETES | Obtencióderangdebutlletes(frontal **síncron** delaPCI). |
| SCT\_CATALEG | Descàrregadel catàleg de normatives (frontal **síncron** de la PCI). |

1.
# Missatgeriadelsserveis

  1.
## Enviamentderemesadebutlletes(SCT\_REMESA)

EnviamentdelesdenúnciesalsistemadelSCTprevialasevaincorporacióal&#39;aplicaciódelProcediment SancionadordelSCT (PSN).

    1.
### Petició–dadesgenèriques

Elfitxercorresponentalaremesas&#39;hadereferenciaralblocdedades//Ficheros/Ficherodelesdadesgenèriques delasol·licitud.

| _Element_ | _Descripció_ |
| --- | --- |
| //Ficheros/Fichero/Contenido | ContingutdelfitxerencasdetransferènciaperMTOM(enlacridacorresponalareferència XOPdelfitxer). |

    1.
### Remesa

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | Perlimitacionsdelsistema delSCTelfitxerderemesa nopotsuperarles50butlletes.
ActualmentelsistemadelSCTúnicamentsuportal&#39;enviamentdedenúnciesdetipusgenèrica.Nohiha previsió acurtterminiperrebredenúnciesdevelocitato d&#39;alcoholèmia.
ElSCTprocessalesremesesdiàriamentales20h.Lesremesesenviadesposteriormentnoesprocessaranfins al diasegüent.
Terminid&#39;enviament:

- Caducitat delesdenúncies:lesdenúnciesnopodenseranteriorsa2mesos.


- El sistema de SCT treballa amb una finestra de processament de 3 dies laborables. Així,una remesa no pot contenir denúncies que puguin caducar abans de 3 dies des del&#39;enviamentdelaremesa.
 |
| --- | --- |

![](RackMultipart20211007-4-lhpxvq_html_65792acda1c64307.png)

| _Element_ | _Descripció_ |
| --- | --- |
| /DADES/CAPCALERA/FITXER\_PDA | Nomdefitxerdelaremesa.Nomenclatura:
BUTCCCCCAAAAMMDDHHMI\_\&lt;num-ordre\&gt;.xml
on:
- BUT:prefix.
- CCCCC:codiINE delmunicipi.
- AAAAMMDD:datad&#39;enviamentdelaremesa.
- HHMI:hora de laremesa.
- \&lt;num-ordre\&gt;: si s&#39;envia més d&#39;unaremesaenundia,éselnúmerod&#39;ordre(encas contrari:1).
- Extensió:.xml
 |
| /DADES/CAPCALERA/NUM\_BUTLLETES | Númerodebutlletesquecontélaremesa(màxim50). |
| /DADES/BUTLLETES | Bloc dedadescorresponentalesbutlletes.
ElSCTestableixunmàximde50butlletesperremesa. |
| /DADES/BUTLLETES/BUTLLETA | Bloc dedadescorresponentaunabutlleta. |

      1.
#### Butlleta

![](RackMultipart20211007-4-lhpxvq_html_15d7bada3f86fb56.png) ![](RackMultipart20211007-4-lhpxvq_html_7351847cce1286c1.png)

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/ACCIO | A:alta/B:anul·lació.Encasd&#39;anul·laciódebutlletacal informar totes les dades de la butlleta, el motiu(MOTIU\_ANULLACIO) i la data d&#39;anul·lació(DATA\_HORA\_ANULLACIO). |
| //BUTLLETA/ID\_BUTLLETA | Identificadordelabutlletaenelsistemaorigenoidentificadordins delaremesa.
DinsdelsistemadelSCTl&#39;identificadordeladenúnciasónelselementsSERVEI\_TERRITi NUM\_EXPEDIENT. |
| //BUTLLETA/SERVEI\_TERRIT | Demarcacióterritorial: 08,17,25,43. |
| //BUTLLETA/NUM\_EXPEDIENT | Númerod&#39;expedient.IdentificadordeladenúnciaenelsistemadelSCT.Ésunnúmerodebutlletadelrangdenúmerosdebutlletaques&#39;halliuratal&#39;Ajuntament.
Permésdetallssobreelmecanismed&#39;obtenciódelrangdebutlletesvegeu l&#39;apartat |
| //BUTLLETA/DIGIT\_CONTROL | Dígit de control de la butlleta. Vegeu l&#39;annex [_Càlcul del_](#_bookmark19)[_dígit __de control__ d&#39;un número__d&#39;expedient_.](#_bookmark19) |
| //BUTLLETA/TIPUS\_DENUNCIA | Tipusdedenúncia:
- G:genèrica.
- A: alcoholèmia (aquest cas requereix informar blocdedades DENUNCIA\_ALCOHOLEMIA).
- V:velocitat(aquestcasrequereixinformarblocdedades DENUNCIA\_VELOCITAT).
 |
| //BUTLLETA/DATA\_DENUNCIA | Datadeladenúncia(formatAAAAMMDD). |
| //BUTLLETA/HORA\_DENUNCIA | Horadeladenúncia(format HHMISS). |
| //BUTLLETA/IDIOMA\_DENUNCIA | C:català/E:castellà |
| //BUTLLETA/NORMA\_DENUNCIA | Normainfringida(delcatàlegdenormatives). |
| //BUTLLETA/ARTICLE\_DENUNCIA | Codidel&#39;articledelainfracció(delcatàlegdenormatives). |
| //BUTLLETA/SUBARTICLE\_DENUNCIA | Codidesubarticlede lainfracció(delcatàlegdenormatives). |
| //BUTLLETA/OPCIO\_DENUNCIA | Númerod&#39;opció(delcatàlegdenormatives). |
| //BUTLLETA/PUNTS | Punts(delcatàlegdenormatives). |
| //BUTLLETA/MESOS\_RETIRADA | Suspensió(delcatàlegdenormatives). |
| //BUTLLETA/NUM\_DENUNCIANT | Númerodel&#39;agentdenunciant. |
| //BUTLLETA/NUM\_NOTIFICADOR | Númerodel&#39;agentnotificador. |

| _Element_ | _Descripció_ |
| --- | --- |
|
 |
 |
| //BUTLLETA/TIPUS\_VIA | Laviaidentificaelllocons&#39;hacoméslainfracció,potserdedos tipus:

- V:Viainterurbana(carretera)
- C:Viaurbana(carrer)
Quanlaviaésinterurbanas&#39;had&#39;indicar:

- Al&#39;elementVIA,elcodide carretera(p.e.C-33).
- Al&#39;elementVIA\_NUMERO,elpuntquilomètricdeladenúncia (format fins a dos dígits decimals iseparadorcoma,p.e.11,20).

Quanlaviaésurbanas&#39;had&#39;indicar:

- Al&#39;elementVIA,elnomdelcarrer.
- Al&#39;elementVIA\_NUMERO,elnúmerodecarrerdeladenúncia(valorsencersensepartdecimal).
 |
| //BUTLLETA/VIA | Viadeladenúncia. |
| //BUTLLETA/VIA\_NUMERO | Númerodelavia. |
| //BUTLLETA/DESCRIPCIO\_POBLACIO | Descripciódelapoblació. |
| //BUTLLETA/DIRECCIO\_DENUNCIA | Sentitdeladenúncia. |
| //BUTLLETA/NUM\_AGENT\_COBRADOR | Númerodel&#39;agentcobrador. |
| //BUTLLETA/IMPORT\_NOMINAL | Importdelaquantia deladenúnciaambdosdecimals.10 primeres posicions és la part sencera (amb zeros al&#39;esquerra)iles duesdarrereslapartdecimal.
Perexemple,100:000000010000. |
| //BUTLLETA/IMPORT\_PAGAT | Import pagatdelabutlleta ambdosdecimals.FormatidènticaIMPORT\_NOMINAL. |
| //BUTLLETA/IMPORT\_DESCOMPTE | Importdeladenúnciaambdescompteambdosdecimals.FormatidènticaIMPORT\_NOMINAL. |
| //BUTLLETA/DATA\_LIMIT\_DESCOMPTE | Datalímitdeldescompte(format AAAAMMDD).20diesdesde la datade la infracciósegonslleiactual. |
| //BUTLLETA/IND\_NOTIFICACIO | Indicadordesignaturadenunciatinotificació:
- X:nonotificada.
- S:notificada.
 |
| //BUTLLETA/M\_NO\_NOTIF | Motiunonotificació(obligatoriquanésunadenúncianonotificada): |

| _Element_ | _Descripció_ |
| --- | --- |
|
 |
- 0001:Conductorabsent
- 0002:Circularensentitcontrari
- 0003:Assistènciaenaccident
- 0004:Serveid&#39;urgència
- 0005:Regulaciódetrànsit
- 0006:Provaesportiva/recreativa
- 0007:Transportespecial
- 0008:Desobediènciaagent
- 0009:Helicòpter
- 0010:Inexistènciallocperaturarinfractor
- 0011:Serveiapeu
- 0012:Formularunaaltradenúncia
- 0013:Perillperalacirculació
- 0014:Responsabilitattitular
- 0015:Completardades
- 0017:Seguretatperalarestad&#39;usuaris
- 0018:Requalificaciódedenuncia
- 0019:Imatgecaptadaautomàticament
- 0020:Atestats
- 0021:Vehiclenologotipat
- 0022:Denúnciavoluntària
- 0023:Mancaresultatanalítica
- 0024:Controlestupefaents/RESIDENT
- 0025:Denúnciaincoadad&#39;ofici
- 0026:Mancaresultatanalítica
 |
| //BUTLLETA/DATA\_HORA\_ANULLACIO | Dataihoradel&#39;anul·lació(formatAAAA-MM-DDHH:MI:SS). Obligatori quan és una denúnciaanul·lada. |
| //BUTLLETA/MOTIU\_ANULLACIO | Motiuanul·lació.Obligatoriquanésunadenúnciaanul·lada:

- 0001:Fetnosancionable
- 0002:Denúnciaduplicada
- 0003:Butlletaanul·ladaperl&#39;agent
- 0004:Butlletadeteriorada
- 0005:Mancadecompetènciapersancionar
- 0006:RetardenlatramesadenúnciaalSCT
- 0007:Error/Mancadadesbàsiquesdenúncia
- 0008:ErroromancadeDNI
- 0009:DenúnciesdeTransports
- 0010:Fotosnovàlides
- 0011:Anul·ladacanviadscripcióterritorial
- 0012:Butlletaanul·ladaperreposiciómodels
- 0013:Butlletaanul·ladaperdocència
- 0014:Butlletaanul·lada apeticióSCT
- 0015:SENSEESPECIFICAR
- 0016:Butlletanoutilitzada
- 0017:Trasllatdel&#39;expedient
- 0018:Prescripciódelainfracció
- 0021:Fetnosancionable
- 0024:Trasllatdel&#39;expedient
- 0025:Prescripciódelainfracció
 |

| _Element_ | _Descripció_ |
| --- | --- |
|
 |
- 0026:Erroromancaenlesdadesbàsiques
- 0027:ErroromancadeDNI
- 0028:Fotosnovàlides
- 0029:Butlletesanul·ladesd&#39;ofici
- 0030:Mancacertificat
- 0031:Mancacompetènciasancionar
- 0032:PDA-CriticaNonotificada
- 0033:Resultatnegatiu
- 0034:Butlletanoutilitzada
- 0035:Baixapererrorenl&#39;aplicacióPDA
 |
| //BUTLLETA/IND\_DGT\_VEHICLE |
- S:dadesdelvehicle obtingudesdeconsulta alabasededades delaDGT
- N:introduïdesmanualment perl&#39;agent
 |
| //BUTLLETA/DESCRIPCIO\_MARCA | Marca. |
| //BUTLLETA/DESCRIPCIO\_MODEL | Model. |
| //BUTLLETA/COLOR\_VEHICLE | Color. |
| //BUTLLETA/TIPUS\_VEHICLE |
- 00:Sensevalor
- 01:Bicicleta
- 02:Ciclomotor
- 03:Motocicleta
- 04:Turisme
- 05:Furgoneta
- 06:Remolc
- 07:Camió
- 08:Autobús
- 09:Altresvehicles
- 10:Temporals
- 11:Turístiques
- 12:Vehicleespecial
- 23:Motocicletaestrangera
- 24:Turismeestranger
- 25:Furgonetaestrangera
- 27:Camióestranger
- 28:Autobúsestranger
- 29:Vehiclegenèric
- 30:Vehicleespecial
 |
| //BUTLLETA/MATRICULA\_DENUNCIA | Númerodelamatrícula. |
| //BUTLLETA/NUMERO\_BASTIDOR | Númerodebastidor. |
| //BUTLLETA/DESCRIPCIO\_PAIS | Descripciódelpaís.ESPANYAen cas d&#39;Espanya.
EncasdedescripcióESPANYAactualmentelSCTnovalidaelformatdelamatrícula pelsvehiclesespanyols però es recomana ajustar-se als formatsproposats en l&#39;apartat [3.1.3.2](#_bookmark11)si en un futur el SCTrealitzalavalidació. |

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/IND\_IMMOBILITZACIO\_VEH | Indicadord&#39;immobilitzaciódelvehicle (S/ N). |
| //BUTLLETA/NUM\_ACTA\_IMMOBILITZACIO | Númerod&#39;actad&#39;immobilització.ObligatorisiIND\_IMMOBILITZACIO\_VEH=S. |
| //BUTLLETA/NOM\_TITULAR | Nomdeltitular. |
| //BUTLLETA/COGNOM1\_TITULAR | Primercognomdeltitular. |
| //BUTLLETA/COGNOM2\_TITULAR | Segoncognomdeltitular. |
| //BUTLLETA/NIF\_TITULAR | Número de document identificador del titular /propietaridelvehicle(NIF,NIE,CIF,passaportoaltresdocuments). |
| //BUTLLETA/ADRECA\_TITULAR | Adreçadeltitular. |
| //BUTLLETA/POBLACIO\_TITULAR | Poblaciódeltitular. |
| //BUTLLETA/PROVINCIA\_TITULAR | Provínciadeltitular. |
| //BUTLLETA/CODI\_POSTAL\_TITULAR | Codipostaldeltitular. |
| //BUTLLETA/FET\_DENUNCIAT | Descripciódel fet denunciat.Textlliure,sibépotportarlainformaciódelcatàlegdenormatives. |
| //BUTLLETA/FET\_DENUNCIAT2 | Descripciódelfetdenunciat.Textlliure addicional. |
| //BUTLLETA/IND\_DGT\_CONDUCTOR |
- S:dadesdelconductorobtingudesdeconsultaalabasededades delaDGT
- N:Introduïdesmanualmentperl&#39;agent
 |
| //BUTLLETA/INDICADOR\_CONDUCTOR |
- I:infractornoconductor
- C:conductor
 |
| //BUTLLETA/TIPUS\_DOCUMENT |
- 01:Personafísica
- 02:Personajurídica
- 03:Estrangerresident
- 04:Estrangernoresident
- 05:Senseidentificar
 |
| //BUTLLETA/NUMERO\_DOCUMENT | Númerodedocument. |
| //BUTLLETA/TIPUS\_PERMIS | Classepermísdeconduir(A,B,etc.). |
| //BUTLLETA/DATA\_EXPEDICIO | Datad&#39;expedició(formatAAAAMMDD). |
| //BUTLLETA/NOM\_CONDUCTOR | Nomdelconductor. |
| //BUTLLETA/COGNOM1\_CONDUCTOR | Primercognomdelconductor. |
| //BUTLLETA/COGNOM2\_CONDUCTOR | Segoncognomdelconductor. |

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/DATA\_NAIXEMENT\_CONDUCTOR | Datadenaixement(formatAAAAMMDD). |
| //BUTLLETA/DESCRIPCIO\_PAIS\_CONDUCTOR | Nacionalitatdelconductor. |
| //BUTLLETA/DOMICILI\_CONDUCTOR | Domicilidelconductor. |
| //BUTLLETA/DESC\_POBLACIO\_CONDUCTOR | Poblaciódeldomicilidelconductor. |
| //BUTLLETA/CODI\_POSTAL\_CONDUCTOR | Codipostaldelconductor. |
| //BUTLLETA/OBSERVACIONS | Observacions. |
| //BUTLLETA/IMATGE | Butlletacodificada enbase 64(màxim400K). |
| //BUTLLETA/TIPUS\_IMATGE | Formatdelabutlleta(jpg/pdf). |
| //BUTLLETA/DENUNCIA\_VELOCITAT | Bloc de dades corresponents a les dades de ladenúnciaencasdeTIPUS\_DENUNCIA=V.Per mésdetallsvegeu l&#39;apartat [3.1.2.2.](#_bookmark6) |
| //BUTLLETA/DENUNCIA\_ALCOHOLEMIA | Bloc de dades corresponents a les dades de ladenúnciaencasdeTIPUS\_DENUNCIA=A.Per mésdetallsvegeu l&#39;apartat [3.1.2.3.](#_bookmark7) |
| //BUTLLETA/TARGETA | Bloc de dades corresponents a les dades depagament.Permésdetallsvegeul&#39;apartat[3.1.2.4.](#_bookmark8) |

      1.
#### Denúnciavelocitat

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | S&#39;haprevistaquestblocdedadespelfuturenviamentdelesdenúnciesdevelocitat.Mentrestant,nos&#39;had&#39;informarelblocdedadesDENUNCIA\_VELOCITAT(nomésessuportaTIPUS\_DENUNCIA=G). |
| --- | --- |

| _Element_ | _Descripció_ |
| --- | --- |
| //DENUNCIA\_VELOCITAT/VELOCITAT\_REGISTRADA | Km/h.
- 3primersdígits:partsencera,zerosal&#39;esquerra
- 3darrersdígits:partdecimal,zerosaladretaPerexemple,142 Km/h: 142000.
 |
| //DENUNCIA\_VELOCITAT/VELOCITAT\_LIMIT | Km/h.4dígitssencers,zerosal&#39;esquerra.Perexemple,120 Km/h: 0120. |
| //DENUNCIA\_VELOCITAT/TIPUS\_LIMITACIO |
- U:Limitacióenviaurbana
- I:Limitacióenviainterurbana
- F:Limitaciófixadapersenyal
 |
| //DENUNCIA\_VELOCITAT/CINEMOMETRE | Cinemòmetre. |

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/CODI\_ANTENA | Antena. |

      1.
#### Denúnciaalcoholèmia

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | S&#39;haprevistaquestblocdedadespelfuturenviamentdelesdenúnciesd&#39;alcoholèmia.Mentrestant,nos&#39;had&#39;informarelblocdedadesDENUNCIA\_ALCOHOLEMIA(nomésessuportaTIPUS\_DENUNCIA=G). |
| --- | --- |

| _Element_ | _Descripció_ |
| --- | --- |
| //DENUNCIA\_ALCOHOLEMIA/TIPUS\_LECTURA |
- A:Aireespirat
- S:Contingut ensang
 |
| //DENUNCIA\_ALCOHOLEMIA/PCT\_1\_LECTURA | Taxaalcoholèmia 1a prova.
- 3primersdígits:partsencera,zerosal&#39;esquerra
- 3darrers dígits:partdecimal,zeros a ladretaPerexemple,0,39: 000390.
 |
| //DENUNCIA\_ALCOHOLEMIA/DATA\_1\_LECTURA | Data1aprova(format AAAAMMDD). |
| //DENUNCIA\_ALCOHOLEMIA/HORA\_1\_LECTURA | Hora1a prova(formatHHMISS). |
| //DENUNCIA\_ALCOHOLEMIA/PCT\_2\_LECTURA | Taxaalcoholèmia 2aprova.Format idènticaPCT\_1\_LECTURA. |
| //DENUNCIA\_ALCOHOLEMIA/DATA\_2\_LECTURA | Data2aprova(format AAAAMMDD). |
| //DENUNCIA\_ALCOHOLEMIA/HORA\_2\_LECTURA | Hora2a prova(formatHHMISS). |
| //DENUNCIA\_ALCOHOLEMIA/MODEL\_ETILOMETRE |
- 01:Dräger Alcotest7110
- 02:Lion1400LS
- 03:Dräger Alcotest7410
- 04:Alcotest7110-E
 |
| //DENUNCIA\_ALCOHOLEMIA/NUMERO\_ETILOMETRE | Númerodesèriedel&#39;etilòmetre. |

      1.
#### Targeta

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | S&#39;haprevistaquestblocdedadesperunpossibleúsfuturdelpagamentambtargeta.Mentrestant,elvalordel&#39;elementIND\_TARGETAseràsempreN. |
| --- | --- |

| _Element_ | _Descripció_ |
| --- | --- |
| //TARGETA/IND\_TARGETA |
- S:pagamentambtargeta
- N:sensetargeta, noimplicaques&#39;hagifet elpagamentenmetàl·lic
 |

| _Element_ | _Descripció_ |
| --- | --- |
| //TARGETA/NUMERO\_TARGETA | 4últims dígitsdelatargeta. |
| //TARGETA/DATA\_CADUCITAT\_TARGETA | Datadecaducitatdelatargeta(format AAAAMMDD). |
| //TARGETA/NUMERO\_TERMINAL | Númerodeterminal. |
| //TARGETA/CODI\_COMERC | Codidecomerç. |
| //TARGETA/NUMERO\_COMANDA | Númerodecomanda. |
| //TARGETA/NUMERO\_AUTORITZACIO | Númerod&#39;autorització. |
| //TARGETA/DATA\_JUSTIFICANT | Datadeljustificant(formatAAAAMMDD). |
| //TARGETA/HORA\_JUSTIFICANT | Horadeljustificant(formatHHMISS). |

    1. **Resposta**** específica**

![](RackMultipart20211007-4-lhpxvq_html_2a0d348306953ebf.jpg)

| _Element_ | _Descripció_ |
| --- | --- |
| /respostaEnviamentRemesa/DADES | Bloc dedadescorresponentaldetalldel&#39;enviamentde laremesa. |
| //DADES/CAPCALERA/FITXER\_PDA | Nomdefitxerdelaremesa.Referènciadelaremesa. |
| //DADES/CAPCALERA/NUM\_BUTLLETES | Númerode butlletesquecontélaremesa. |
| //DADES/CAPCALERA/CODI\_INCIDENCIA | Codidelaincidència. |
| //DADES/CAPCALERA/DESCRIPCIO\_INCIDENCIA | Descripciódelaincidència |
| //DADES/BUTLLETES/BUTLLETA | Blocdedadescorresponentalresultatdeltractamentd&#39;unabutlleta. |
| //DADES/BUTLLETES/BUTLLETA/ID\_BUTLLETA | Identificador delabutlletaenelsistemaorigeno |

| _Element_ | _Descripció_ |
| --- | --- |
|
 | identificadordinsde laremesa. |
| //DADES/BUTLLETES/BUTLLETA/SERVEI\_TERRIT | Serveiterritorial. |
| //DADES/BUTLLETES/BUTLLETA/NUM\_EXPEDIENT | Númerod&#39;expedient. |
| //DADES/BUTLLETES/BUTLLETA/RESULTAT |
- 0:tractamentcorrecte
- 1:contébutlletesamb errorsnocrítics
- 2:contébutlletesamb errorscrítics
Quan s&#39;intenta carregar una butlleta, si no superales validacions del sistema del SCT quedamarcada com a crítica i no es tramita. Per tal detramitar-lacalreenviar-laambl&#39;errorcríticcorregit. |
| //DADES/BUTLLETES/BUTLLETA/DATA\_LIMIT | Per a butlletes crítiques, data màxima per areenviar-laamblesdadescorregides(formatAAAAMMDD). |
| //DADES/BUTLLETES/BUTLLETA/INCIDENCIES | Bloc dedadescorresponentalarelaciód&#39;incidènciesdetectadesenlabutlleta. |
| //INCIDENCIES/INCIDENCIA | Blocdedadescorresponentaunaincidènciadetectada enlabutlleta. |
| //INCIDENCIA/CODI\_INCIDENCIA | Codideincidència.Vegeuapartat[3.1.3.1](#_bookmark10)d&#39;aquestdocument. |
| //INCIDENCIA/DESCRIPCIO\_INCIDENCIA | Descripciód&#39;incidència. |
| //INCIDENCIA/INFORMACIO\_ADDICIONAL | Informacióaddicionaldela incidència. |
| /respostaEnviamentRemesa/resultat/codiResultat |
- 0: enviament de la remesa realitzatcorrectament (detalls de cada butlleta al&#39;elementDADES).
- 0502:errorrealitzantl&#39;enviament.
 |
| /respostaEnviamentRemesa/resultat/descripcio | Descripciódelresultat. |

      1.
#### Codisd&#39;incidència

| _Tipus_ | _Codi_ | _Descripció_ | _Campsvalidats_ | _Validació_ |
| --- | --- | --- | --- | --- |
| _Capçalera_ |
| CRÍTIC | CAP002 | Nombre dedenúncieserroni | NUM\_BUTLLETES | NombredeBUTLLETAdelaremesano coincideix amb elNUM\_BUTLLETES. |
| _Validacionsdeformat_ |
| CRÍTIC | INT001 | Dada numèricaerrònia | IMPORT\_NOMINALIMPORT\_PAGATIMPORT\_DESCOMPTE | Elvalornoes potconvertiranúmero,aplicantelpatrócorresponent. |
| NO | INT002 | Dadanumèrica | VIA\_NUMERO | Elvalornoespotconvertiranúmero, |

| _Tipus_ | _Codi_ | _Descripció_ | _Campsvalidats_ | _Validació_ |
| --- | --- | --- | --- | --- |
| CRÍTICA |
 | errònia |
 | aplicantelpatrócorresponent. |
| CRÍTIC | DAT001 | Dataerrònia | DATA\_DENUNCIA | FormatincorrecteAAAAMMDD. |
| NOCRÍTICA | DAT002 | Dataerrònia | DATA\_LIMIT\_DESCOMPTE | FormatincorrecteAAAAMMDD. |
| CRÍTIC | DAT003 | Dataerrònia | DATA\_HORA\_ANULLACIO | El valor no es pot convertir a una datasegons el format: YYYY-MM-DD-HH:MI:SS&#39;. |
| CRÍTIC | HOR001 | Horaerrònia | HORA\_DENUNCIA | Elvalornoespotconvertiraunahorasegonsel format HHMISS. |
| _Validacionsdecontingut_ |
| CRÍTIC | BUT002 | Butlletaduplicada | SERVEI\_TERRITNUM\_EXPEDIENT | Aquestabutlletajaexisteixalsistema.
Unabutlletanoméséspotenviarunavegada,amb ACCIO:
- A:Alta.
- B:Anul·lació.

Noméss&#39;admetunabutlletarepetidaquan es tracta del reenviament deunabutlletacrítica. |
| CRÍTIC | BUT003 | Butlleta fora derang | SERVEI\_TERRITNUM\_EXPEDIENT | Labutlletanocorresponalrangassignat a la policia localcorresponent. |
| CRÍTIC | BUT004 | Elementobligatori NOinformat | ACCIONORMA\_DENUNCIAARTICLE\_DENUNCIASUBARTICLE\_DENUNCIAOPCIO\_DENUNCIANUM\_DENUNCIANTTIPUS\_VIAVIAVIA\_NUMEROIMPORT\_NOMINALIMPORT\_PAGATIMPORT\_DESCOMPTEDATA\_LIMIT\_DESCOMPTEIND\_NOTIFICACIO |
 |
| CRÍTIC | BUT004 | Elementobligatori NOinformat | INDICADOR\_CONDUCTORTIPUS\_DOCUMENTNUMERO\_DOCUMENTNOM\_CONDUCTORCOGNOM1\_CONDUCTORCODI\_PAIS\_CONDUCTORDOMICILI\_CONDUCTORCODI\_MUNICIPI\_CONDUCTOR | Aquests elements només sónobligatoris per a denúnciesnotificades. |
| CRÍTIC | BUT007 | Codi controlbutlletaerroni | DIGIT\_CONTROL |
 |
| NOCRÍTICA | BUT011 | Camp massallarg |
 | Són camps que en l&#39;entorn PDA sónmésgrans queen entornPSN.
Elementslagrandàriadelsqualsésmésgrana lamissatgeriadela |

| _Tipus_ | _Codi_ | _Descripció_ | _Campsvalidats_ | _Validació_ |
| --- | --- | --- | --- | --- |
|
 |
 |
 |
 | remesaquealssistemesdelSCT. |
| NOCRÍTICA | BUT013 | Manca codipostal | CODI\_POSTAL\_CONDUCTOR | El codi postal del conductor no estàinformat. |
| CRÍTIC | BUT014 | Butlletaarxivada | SERVEI\_TERRITNUM\_EXPEDIENT | S&#39;hatornataenviarunabutlletaqueja s&#39;havia arxivat perquè s&#39;havia rebutcom a CRÍTICA amb errors CRÍTICS is&#39;ha exhaurit el termini per reenviar-la. |
| NOCRÍTICA | BUT015 | Butlletareenviada | SERVEI\_TERRITNUM\_EXPEDIENT | Les butlletes reenviades generaranuna incidència no crítica per forçarque passin pel mòdul de validació dePSN,malgratquenohihagicapaltraincidènciaenla butlleta. |
| CRÍTIC | BUT018 | Butlletapagada nonotificada | IMPORT\_PAGATIND\_NOTIFICACIO | Quanl&#39;elementIND\_NOTIFICACIOsigui &quot;X&quot; (butlleta no notificada),l&#39;import pagat ha de ser 0, si no ésaixíesgenera error. |
| CRÍTIC | NOR001 | Normativainexistent | NORMA\_DENUNCIAARTICLE\_DENUNCIASUBARTICLE\_DENUNCIAOPCIO\_DENUNCIA | No existeix al catàleg de normativalegal. |
| NOCRÍTICA | NOR002 | Normativa NOvigent | NORMA\_DENUNCIAARTICLE\_DENUNCIASUBARTICLE\_DENUNCIAOPCIO\_DENUNCIA | Existeixalcatàlegdenormativalegalperò no és vigent respecte a la datadeladenúncia. |
| NOCRÍTICA | NOR003 | Import de laquantia de ladenúnciaincorrecte | IMPORT\_NOMINAL | Import incorrecte per la normativainfringida. |
| NOCRÍTICA | NOR004 | Nombre depunts adetreureincorrecte | PUNTS | Punts incorrectes per la normativainfringida. |
| CRÍTIC | NOT001 | CampobligatoriNOnotificacióNOinformat | M\_NO\_NOTIF | Quanl&#39;elementIND\_NOTIFICACIOsigui &quot;X&quot; (butlleta no notificada), elmotiuésobligatori. |
| CRÍTIC | ANU001 | Campobligatorianul·lacióNOinformat | DATA\_HORA\_ANULLACIOMOTIU\_ANULLACIO | Ésobligatoriquanl&#39;elementACCIOés &quot;B&quot; (anul·lació). |
| CRÍTIC | MAT001 | Formatmatriculaerrònia | MATRICULA\_DENUNCIA | Actualment no es valida el format dela matrícula pels vehicles espanyols(DESCRIPCIO\_PAIS=ESPANYA)tot i que en un futur el SCT podriavalidar-lo. |

      1.
#### Formatsdematrícula

Formatsde matrícularecomanatspelSCT:

- Turisme/Motocicleta/Camió/Furgoneta/Autobús(onndígits,Llletres,bespais).

![Shape43](RackMultipart20211007-4-lhpxvq_html_72e53ebffdeeaf7.gif)

- Remolc(onndígitsiLlletres):

RnnnnLLL

- VehiclesEspecials(onnnúmeros,Llletres, Efixa,bespais):

EnnnnLLL LLnnnnnE LbnnnnnE LLnnnnnnE LbnnnnnnE

- Turístics(onnnúmeros,Llletres,Tfixa,bespais):

TnnnnLLL nnLLnnnn nnLbnnnn

- Temporals(onnnúmeros,Llletres,T,R,P,S,Vfixes,bespais):

![Shape44](RackMultipart20211007-4-lhpxvq_html_6edaa7c797ff51d3.gif)

- Ciclomotors(onnnúmeros,Llletres,Cfixa):

CnnnnLLL

- AltresVehicles(onnnúmeros,Llletres,CD,OI,CC,TA,H,PMM,PGCfixes,bespais):

| CDnnnn | OInnnn | CCnnnn | TAnnnn | HnnnnLLL | PMMnnnnnn |
| --- | --- | --- | --- | --- | --- |
| PMMnnnnLL | PMMnnnnbL | PGCnnnnnn | PGCnnnnLL | PGCnnnnbL |
 |

  1.
## Obtencióderangdebutlletes(SCT\_BUTLLETES)

LespolicieslocalsnecessitendisposardebutlletesdelSCTperpoderinterposardenúnciescompetència del SCT. Actualment disposen de talonaris de butlletes en paper lliurats per el SCT quetenenpreimprès el númerodebutlleta(expedient).

Per aquelles policies que s&#39;acullin al sistema de denúncies via PDA ofereix aquesta modalitat perobtenirrangs debutlletes.

LesdenúnciescompetènciadelSCThand&#39;estaridentificades per:

- SERVEI\_TERRIT:demarcacióterritorial.

- NUM\_EXPEDIENT:noésunvaloraleatori,ésunnúmerodebutlletadelrangdenúmerosqueeslliuraalapolicial localcorresponent.

Aquesta informació ha de mostrar-se en les butlletes que la policia local notifica als infractors. Tambéenaquelles nonotificades.

    1.
### Petició–dadesespecífiques

![](RackMultipart20211007-4-lhpxvq_html_79f1d74ad1da344a.png)

| _Element_ | _Descripció_ |
| --- | --- |
| /respostaObtencioRangButlletes/NUM\_BUTLLETES\_SOLICITADES | Númerodebutlletessol·licitades(màxim9999). |

    1.
### Resposta –dadesespecífiques

![](RackMultipart20211007-4-lhpxvq_html_c3f1ca5017688e6c.png)

| _Element_ | _Descripció_ |
| --- | --- |
| /respostaObtencioRangButlletes/SORTIDA/RESULTAT |
- 0:s&#39;hanlliuratlesbutlletessol·licitades.
- 1:s&#39;hanlliuratmenysbutlletesdelessol·licitades.
- 2:noesdisposadebutlletes.Encasques&#39;obtinguiaquest errorcontacteuamb el SCT.
 |
| /respostaObtencioRangButlletes/SORTIDA/NUM\_BUTLLETES\_LLIURADES | Númerodebutlleteslliurades. |
| /respostaObtencioRangButlletes/SORTIDA/RANGS/RANG | Bloc dedadescorresponentaunrangde butlletes.Elsistema del SCT pot lliurar el nombre de butlletes enrangsdiscontinus. |
| //RANG/ID\_RANG | Identificadordelrang. |
| //RANG/SERVEI\_TERRIT | Demarcacióterritorial. |
| //RANG/TALONARI\_INICIAL | Valorinicialdelrang.Númerodebutlletainicial. |
| //RANG/TALONARI\_FINAL | Valorfinaldelrang.Númerode butlletafinal. |
| /respostaObtencioRangButlletes/resultat/codiResultat |
- 0:consultarealitzadacorrectament.
- 0502:errorrealitzantlaconsulta.
 |
| /respostaObtencioRangButlletes | Descripciódelresultat. |

| /resultat/descripcio |
 |
| --- | --- |

  1.
## Descàrregadelcatàlegdenormatives(SCT\_CATALEG)

Les policieslocalsnecessitendisposardelcatàlegdenormativesperpoderindicar lanormainfringidaquan interposenunadenúnciacompetènciadelSCT.

Actualmentdisposend&#39;uncatàlegd&#39;infraccionsimprèsenformatdeminillibre,quanrealitzenunadenúnciaescriuenmanualmentalabutlletalesdadesidentificativesdelaopciónormativainfringida.

Peraquellespoliciesques&#39;acullinalsistemadedenúnciesviaPDA,s&#39;ofereixunamodalitatperobtenirelcatàlegdenormatives enformatdigital.

    1.
### Petició–dadesespecífiques

Lamodalitatnorequereixcaptipusdedadesespecífiquesal&#39;horaderealitzarlapetició.

    1.
### Resposta –dadesespecífiques

| _Element_ | _Descripció_ |
| --- | --- |
| /respostaConsultaCatalegNormatives/NORMATIVES/NORMATIVA | Bloc dedadescorresponentalblocdedadesdecadascuna deles normatives. |
| //NORMATIVA/CODI\_NL | Codidenormallegal. |
| //NORMATIVA/ARTICLE | Articleinfringit. |
| //NORMATIVA/SUBARTICLE | Subarticleinfringit. |
| //NORMATIVA/OPCIO | Opció. |
| //NORMATIVA/GRAVETAT |
- G:Greu
- L:Lleu
- M:Moltgreu
- V:62.2LSV
- W:67.4LSV
 |
| //NORMATIVA/DESC\_BREU | Descripcióbreudelconceptedelainfracció. |
| //NORMATIVA/FET\_DENUNCIAT | Conceptedelainfracció(català). |
| //NORMATIVA/HECHO\_DENUNCIADO | Conceptedelainfracció(castellà). |
| //NORMATIVA/FET\_DENUNCIAT\_ARANES | Conceptedelainfracció(aranès). |
| //NORMATIVA/IMPORT\_NOMINAL | Quantia de la multa sense descompte amb dosdecimals.10primeres posicionssónlapartsencera(amb zeros a l&#39;esquerra) i les dues darreres la partdecimal.
Perexemple,100:000000010000. |

| _Element_ | _Descripció_ |
| --- | --- |
|
 |
 |
| //NORMATIVA/PUNTS | Pèrduadepuntsquecomportalainfracció. |
| /respostaConsultaCatalegNormatives/resultat/codiResultat |
- 0:consultarealitzadacorrectament.
- 0502:errorrealitzantlaconsulta.
 |
| /respostaConsultaCatalegNormatives/resultat/descripcio | Descripciódelresultat. |

![](RackMultipart20211007-4-lhpxvq_html_4aa877f961bb22d4.png)

# Annexes

## Càlculdeldígitdecontrold&#39;unnúmerod&#39;expedient

Donatunnúmerod&#39;expedient,eldígitdecontrolcorresponentescalculatalicomesdescriuacontinuació:

1. Obtenirl&#39;emissoraalaquepertanyl&#39;expedient.

| _Serveiterritorial_ | _Emissora_ |
| --- | --- |
| Barcelona (08) | 8500514 |
| Girona(17) |
- Sinúmeroexpediententre1i400008500459
- Sinúmeroexpediententre40001i 1125008500459
- Sinúmeroexpedient\&gt;=1125018500472
 |
| Lleida(25) | 8500484 |
| Tarragona(43) | 8500540 |

1. Sil&#39;emissoraés8500459eldígitdecontrolés9.

1. Altrament,percalculareldígitdecontrols&#39;hadediferenciarsil&#39;expedientésde7o8dígits(número d&#39;expedient\&gt;9999999).

Concatenarelserveiterritorialielnúmerod&#39;expedient

- Expedientde7omenysdígits:formatantambzerosperl&#39;esquerrafinsa7dígits.

- Expedientde8dígits:nocalformatarperl&#39;esquerra.

i a aquest sumar-li el número de l&#39;emissora i invertir el resultat.Perexemple,ambl&#39;expedient08/5168515iemissora8500514:

085168515+8500514=93669029

Invertint-lo:

92096639

1. Multiplicarcadadígitdelresultatobtingutpelvalorqueestrobaenlamateixaposicióenelsegüentarray (constant).

|
2 |
3 |
4 |
5 |
6 |
7 |
8 |
9 |
2 |
3 |
4 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

(9\*2)+(2\*3)+(0\*4)+(9\*5)+(6\*6)+(6\*7)+(3\*8)+(9\*9)=252

1. Dividirelvalorobtingut entre11 iquedar-seambelresidu.

252mod11=10

1. Sielresidu és10,eldígit decontrolserà0.Enqualsevolaltrecasseràelvalorobtingut.

Així,elnúmerod&#39;expedientcomplertserà08/5168515-0.

## Líniadecobramenticodidebarresd&#39;unabutlletadesanció

Acontinuacióesdetallacomgenerarlalíniadecobramenticodidebarresquecalincorporaralesbutlletes.

![Shape45](RackMultipart20211007-4-lhpxvq_html_63e8589e19f67bfc.gif)

### Líniadecobrament

Percomposarlalíniadecobrament:

![](RackMultipart20211007-4-lhpxvq_html_d916cd932b4ffe30.jpg)

- RINF5Emissora:valorfix05850043.

- Sufix(XXX):enfunciódelServeiTerritorial.

| _ServeiTerritorial_ |
| --- |
| _Barcelona(91)_ | _Girona(92)_ | _Lleida(93)_ | _Tarragona(94)_ |
| 608 | 617 | 625 | 643 |

- Referència(SSSSYYYYYYY-CC/SSSYYYYYYYY-CC)constadetresparts:

  - ServeiTerritorial(SSSS, 4posicions i3posicions per expedients de8dígits):
    - Barcelona
      - 0008:perexpedients demenysde8posicions
      - 008:perexpedients de8posicions
    - Girona
      - 0017:perexpedients demenysde8posicions
      - 017:perexpedients de8posicions
    - Lleida
      - 0025:perexpedients de menysde8 posicions
      - 025:perexpedients de8posicions
    - Tarragona
      - 0043:perexpedients demenysde8posicions
      - 043:perexpedients de8posicions

  - Númerod&#39;expedient(YYYYYYYoYYYYYYYY-8posicions)

  - Dígitsdecontrol(CC,2posicions)calculatssegonsl&#39;algoritmeinclòsal&#39;Annex2delQuadern

57&quot;_Cobros por __ventanilla__ y__autoservicio_&quot;.

Depenentdesil&#39;expedientes8omenysposicionselformatdelareferènciaes:

&#39; **00&#39;**** (2****posicions)**+SERVEI\_TERRITORIAL(2posicions)+ **NUM\_EXPEDIENT**** (7****posicions)** + DC(2posicions)

&#39;**0&#39; (1****posició)**+SERVEI\_TERRITORIAL(2 posicions)+**NUM\_EXPEDIENT****(8****posicions)**+

DC(2posicions)

- Datalímit(DDMMAAAA):terminide20diesdes de ladatadeladenúncia.

- Importambdescompte:S.C.

### Codide barres

Pelquefaalacomposició delcodide barresde46 dígitstenim:

- Codiinicialfix(5posicions): 90507.

- Codid&#39;emissorafixpelSCT(8posicions): 05850043.

- Sufix(3posicions)enbasealServeiTerritorial,vegeuapartatanterior.

- ServeiTerritorial(3/4 posicions),vegeuapartatanterior.

- Númerod&#39;expedient(7/8posicions).

- Dígitsdecontrol(2posicions)calculatssegonsl&#39;algoritmeinclòsal&#39;Annex2delQuadern57&quot;_Cobros __por ventanilla__ y__autoservicio_&quot;.

- Identificació(6 posicions):corresponaladatalímit(DDMMAA),vegeuapartatanterior.

- Import(10posicions):les2darreresposicionscorresponenalsdecimals.

- ![Shape46](RackMultipart20211007-4-lhpxvq_html_581d8521ea69d4a2.gif)Dígitfinalfix(1posició):0.

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | A l&#39;Annex 1 del Quadern 38 (_&quot;Códigos de Barras en Documentos Financieros&quot;_) podeuconsultar la informació referent a la representació del codi de barres EAN-128 que inclou elformat icomesgeneraelcaràcterdecontrolques&#39;ha d&#39;incloure. |
| --- | --- |

![Shape47](RackMultipart20211007-4-lhpxvq_html_f556900526b51d9b.gif)

![](RackMultipart20211007-4-lhpxvq_html_92efe5ef7d85f2ca.png)

## Textdelsavisoslegalsaincloureenlesbutlletes

INFORMACIÓIADVERTÈNCIESLEGALS

Sigles de les normes: R, Reglament general de circulació (RD 1428/03); V, Reglament general devehicles (RD 2822/98); G, Reglament general de conductors (RD 818/09); A, Llei sobre responsabilitatcivil i assegurança en la circulació de vehicles de motor (Rdleg. 8/04); TRLSV, text refós de la Lleisobretrànsit,circulaciódevehiclesdemotoriseguretatviària(RDL6/2015);E,Reglamentd&#39;autoescoles(RD1295/03).

NOTIFICACIÓDELADENÚNCIA IINCOACIÓDELPROCEDIMENT

Usnotifiquemaquestadenúnciaiusfemsaberquequedaincoatelcorresponentprocedimentsancionador(article89TRLSV)

PROCEDIMENTABREUJATIPROCEDIMENTORDINARI

Si us voleu acollir a la tramitació pel procediment abreujat, disposeu d&#39;un termini de 20 dies naturalsdes de la notificació per realitzar el pagament de l&#39;import de la sanció, amb un descompte del 50%.Aquest procediment implica: la renúncia a formular al·legacions (es tindran per no presentades), lafinalització del procediment sense dictar resolució expressa, l&#39;esgotament de la via administrativa(nomésespodrà

recórrer davant del Jutjat ) i la fermesa de la sanció des del moment del pagament. Si la sanció ésgreu i no comporta detracció de punts, no s&#39;anotarà com antecedent en el Registre de conductors iinfractors. En cas de no efectuar el pagament amb descompte del 50%, continua la tramitació pelprocediment ordinari, que us permet formular al·legacions i proposar o aportar proves en el termini de20dies naturals des dela

notificació. L&#39;escrit d&#39;al·legacions s&#39;ha d&#39;adreçar al Servei Territorial de Trànsit corresponent i es potpresentar en qualsevol dels registres legalment establerts (\*).Si no formuleu al·legacions ni aboneul&#39;import de la sanció, aquesta denúncia tindrà efecte d&#39;acte resolutori del procediment sancionador.Contra la sanció es podrà interposar recurs de reposició, amb caràcter potestatiu, en el termini d&#39;unmes. La sanció podrà executar-se transcorreguts 30 dies naturals des de la notificació d&#39;aquestadenúncia.

ÒRGANSQUEINTERVENEN ENELPROCEDIMENT

Òrgan instructor: el/la cap del Servei Territorial de Trànsit de Barcelona. Autoritat sancionadora: lapersona titular de la Direcció del Servei Català de Trànsit (article 11.1 de la Llei 14/1997, de 24 dedesembre,decreació del ServeiCatalàdeTrànsit,D.O.G.C.núm.5537,de 31-12-2009)

RESOLUCIÓDEL&#39;EXPEDIENTSANCIONADOR

Elterminimàximperresoldreinotificarlaresoluciódel&#39;expedientsancionadoriniciatmitjançantaquestadenúnciaésd&#39;unanydes de l&#39;inicidelprocediment(article112.3TRLSV)

PÈRDUADEPUNTSEN ELSPERMISOSILLICÈNCIESDECONDUCCIÓ

Els punts indicats a aquesta butlleta es detrauran quan la sanció sigui ferma. Podeu consultar el saldodepunts en [www.dgt.es](http://www.dgt.es/)

NOTIFICACIONSELECTRÒNIQUES

LaTRLSVhaestablertqueapartirdel24-11-2010espuguinefectuarlesnotificacionspermitjanselectrònics.Siusvoleu acollir aaquestapossibilitat,consulteuelweb[http://transit.gencat.cat](http://transit.gencat.cat/)

FORMADEPAGAMENT

Podeuutilitzaruna de lessegüentsmodalitatsperferefectiuelpagament dela multa:

- Pagar-ladirectamentambtargetaal&#39;agentqueushadenunciat.

- Pagar-laambaquestimprès,perl&#39;importifinsladatalímitdepagamentreflectitsalpeudelabutlletadedenúncia,aqualsevoldelesoficines deCaixaBank.

- Pagar-laambtargeta,directamentaqualsevoldelesdependènciesterritorialsdelServeiCatalàdeTrànsit.

- Pagar-laperinternetmitjançantelportal[http://tramits.gencat.cat](http://tramits.gencat.cat/)

(\*) Els subjectes **obligats a relacionar-se electrònicament** amb l&#39;administració (art 14.2 i 14.3 de laLlei 39/2015 i art 3 de l&#39;Ordre PDA/20/2019) han de presentar les al·legacions per internet accedint alweb[http://transit.gencat.cat.](http://transit.gencat.cat/)

PROTECCIÓDEDADES.

Tractament SCT: Expedients sancionadors per infraccions de trànsit. Responsable: la persona titulardelaDirecciódel&#39;SCT(Diputació,355,08009Barcelona).ContacteDelegatdeprotecciódedades:Diputació, 355, 08009 Barcelonao [dpd.interior@gencat.cat](mailto:dpd.interior@gencat.cat)Finalitat: gestionar les dadesrelatives als expedients sancionadors que s´incoïn per infraccions en aquesta matèria. Informacióaddicionalaccediual[webdel&#39;SCT.](http://transit.gencat.cat/ca/el_servei/proteccio_dades/)

TractamentAjuntamentde...............:amblafinalitatdegeneraraquestdocument,lesdadespersonals seran tractades per l&#39;Ajuntament dexxxxxxxxxxxxxxxxxxxxxxPodeu consultar informacióaddicionalsobreaquesttractament i protecció de dades enwww.xxxxxxxxxxxxxxxxxxxx
