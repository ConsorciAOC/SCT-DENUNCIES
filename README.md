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
2. [Transmissions de dades disponibles 1](#_bookmark1)
3. [Missatgeria dels serveis 1](#_bookmark2)
  1. [Enviament de remesa de butlletes (SCT\_REMESA) 1](#_bookmark3)
    1. [Petició–dades genèriques 1](#_bookmark4)
    2. [Remesa 2](#_bookmark5)
    3. [Resposta específica 11](#_bookmark9)
  2. [Obtenció de rang de butlletes (SCT\_BUTLLETES) 15](#_bookmark12)
    1. [Petició–dades específiques 16](#_bookmark13)
    2. [Resposta–dades específiques 16](#_bookmark14)
  3. [Descàrrega del catàleg de normatives (SCT\_CATALEG) 17](#_bookmark15)
    1. [Petició–dades específiques 17](#_bookmark16)
    2. [Resposta–dades específiques 17](#_bookmark17)

[Annexes 19](#_bookmark18)

[Càlcul del dígit de control d'un número d'expedient 19](#_bookmark19)

[Líniadecobrament icodidebarresd&#39;unabutlletadesanció20](#_bookmark20)

[Líniadecobrament 20](#_bookmark21)

[Codidebarres 22](#_bookmark22)

[Text dels avisos legals a incloure en les butlletes 23](#_bookmark23)

1.
# Introducció

Aquest document detallala missatgeria associada al servei d&#39;enviament de denúncies al Servei Català de Trànsit(enendavantSCT).

Per a poder realitzar la integració cal conèixer prèviament la següent documentació:

- Document de Missatgeria Genèrica de la PCI del Consorci AOC.

1.
# Transmissions de dades disponibles

Les dades disponibles a través del servei són les que es presenten a continuació:

| **EMISSOR** |
| --- |
| ServeiCatalàdeTrànsit |
| **PRODUCTE** | **MODALITAT** | **DESCRIPCIO** |
| **SCT\_DENUNCIES** | SCT\_REMESA | Enviamentderemesadebutlletes(frontal **asíncron** de laPCI). |
| SCT\_BUTLLETES | Obtencióderangdebutlletes(frontal **síncron** delaPCI). |
| SCT\_CATALEG | Descàrregadel catàleg de normatives (frontal **síncron** de la PCI). |

1.
# Missatgeria del sserveis

  1.
## Enviament de remesade butlletes(SCT\_REMESA)

Enviament de les denúncies al sistema del SCT previa la seva incorporació al&#39;aplicació del Procediment Sancionador del SCT (PSN).

    1.
### Petició–dadesgenèriques

El fitxer corresponent a la remesas&#39;hadereferenciaralblocdedades//Ficheros/Fichero de les dades genèriques de la sol·licitud.

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

- V:Via interurbana(carretera)
- C:Via urbana(carrer)
Quan la via és interurbana s'ha d'indicar:

- A l'element VIA,elcodide carretera(p.e.C-33).
- A l'element VIA\_NUMERO,el punt quilomètric de la denúncia (format fins a dos dígits decimals iseparadorcoma,p.e.11,20).

Quan la via és urbana s'ha d'indicar:

- A l'element VIA,el nom del carrer.
- A l'element VIA\_NUMERO,el número de carrer de la denúncia(valor sencer sense part decimal).
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
- 0008:Desobediència agent
- 0009:Helicòpter
- 0010:Inexistèncialloperaturarinfractor
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

## Línia de cobrament i codi de barres d&#39;una butlleta de sanció

A continuació es detalla com generar la línia de cobrament i codi de barres que cal incorporar a les
butlletes.

![image](https://user-images.githubusercontent.com/32306731/137284289-9ea74e0c-27bb-445b-8600-7d695a6b3939.png)

### Línia de cobrament

Per composar la línia de cobrament:

![image](https://user-images.githubusercontent.com/32306731/137283999-406e86ce-78f5-4bc3-a06e-01e0011231ec.png)

- RIN F5 Emissora: valor fix 05850043.

- Sufix (XXX): en funció del Servei Territorial.

![image](https://user-images.githubusercontent.com/32306731/137283786-f7248b53-a16d-4a76-9494-3847164f2a98.png)

| _ServeiTerritorial_ |
| --- |
| _Barcelona(91)_ | _Girona(92)_ | _Lleida(93)_ | _Tarragona(94)_ |
| 608 | 617 | 625 | 643 |

- Referència (SSSSYYYYYYY-CC / SSSYYYYYYYY-CC) consta de tres parts:

  - Servei Territorial (SSSS, 4 posicions i 3 posicions per expedients de 8 dígits):
    - Barcelona
      - 0008: per expedients de menys de 8 posicions
      - 008: per expedients de 8 posicions
    - Girona
      - 0017: per expedients de menys de 8posicions
      - 017: per expedients de 8 posicions
    - Lleida
      - 0025: per expedients de menys de 8 posicions
      - 025: per expedients de 8 posicions
    - Tarragona
      - 0043: per expedients de menys de 8 posicions
      - 043: per expedients de 8 posicions

  - Número d’expedient (YYYYYYY o YYYYYYYY- 8 posicions)

  - Dígits de control (CC, 2 posicions) calculats segons l’algoritme inclòs a l’Annex 2 del Quadern 57 &quot;_Cobros por __ventanilla__ y__autoservicio_&quot;.

Depenent de si l’expedient es 8 o menys posicions el format de la referència es:

**‘00’ (2 posicions)** + SERVEI_TERRITORIAL (2 posicions) + **NUM_EXPEDIENT (7 posicions)** + DC (2 posicions)

**‘0’ (1 posició)** + SERVEI_TERRITORIAL (2 posicions) + **NUM_EXPEDIENT (8 posicions)** + DC (2 posicions)

- Data límit (DDMMAAAA): termini de 20 dies des de la data de la denúncia.

- Import amb descompte: S.C.

### Codi de barres

Pel que fa a la composició del codi de barres de 46 dígits tenim:

- Codi inicial fix (5 posicions): 90507.

- Codi d’emissora fix pel SCT (8 posicions): 05850043.

- Sufix (3 posicions) en base al Servei Territorial, vegeu apartat anterior.

- Servei Territorial (3/4 posicions), vegeu apartat anterior.

- Número d’expedient (7/8 posicions).

- Dígits de control (2 posicions) calculats segons l’algoritme inclòs a l’Annex 2 del Quadern 57 &quot;_Cobros __por ventanilla__ y__autoservicio_&quot;.

- Identificació (6 posicions): correspon a la data límit (DDMMAA), vegeu apartat anterior.

- Import (10 posicions): les 2 darreres posicions corresponen als decimals.

- Dígit final fix (1 posició): 0.

![image](https://user-images.githubusercontent.com/32306731/137281698-9dfc2044-94f7-487f-a7d6-9a4e0707feb3.png) A l’Annex 1 del Quadern 38 (“Códigos de Barras en Documentos Financieros”) podeu consultar la informació referent a la representació del codi de barres EAN-128 que inclou el
format i com es genera el caràcter de control que s’ha d’incloure.

![image](https://user-images.githubusercontent.com/32306731/137281455-fb7a0d64-621e-4337-a136-46323d877708.png)

![image](https://user-images.githubusercontent.com/32306731/137281095-b86e4677-b97f-465f-8eec-cb3bb8f26b4d.png)


## Text dels avisos legals a incloure en les butlletes

INFORMACIÓ I ADVERTÈNCIES LEGALS

Sigles  de  les  normes:  R,  Reglament  general  de  circulació  (RD  1428/03);  V,  Reglament  general  de vehicles (RD 2822/98); G, Reglament general de conductors (RD 818/09); A, Llei sobre responsabilitat civil  i  assegurança  en  la  circulació  de  vehicles  de  motor  (Rdleg.  8/04);  TRLSV,  text  refós  de  la  Llei sobre  trànsit,  circulació  de  vehicles  de  motor  i  seguretat  viària  (RDL  6/2015);  E,  Reglament d'autoescoles (RD 1295/03).

NOTIFICACIÓ DE LA DENÚNCIA I INCOACIÓ DEL PROCEDIMENT

Us  notifiquem  aquesta  denúncia  i  us  fem  saber  que  queda  incoat  el  corresponent  procediment sancionador (article89 TRLSV)

PROCEDIMENT ABREUJAT I PROCEDIMENT ORDINARI

Si us voleu acollir a la tramitació pel procediment abreujat, disposeu d'un termini de 20 dies naturals des  de  la  notificació  per  realitzar  el  pagament  de  l'import  de  la  sanció,  amb  un  descompte  del  50%. Aquest  procediment  implica:  la  renúncia  a  formular  al·legacions  (es  tindran  per  no  presentades),  la finalització  del  procediment  sense  dictar  resolució  expressa,  l'esgotament  de  la  via  administrativa (només es podràrecórrer  davant  del  Jutjat  )  i  la  fermesa  de  la  sanció  des  del  moment  del  pagament.  Si  la  sanció  és greu  i  no  comporta  detracció  de  punts,  no  s'anotarà  com  antecedent  en  el  Registre  de  conductors  i infractors.  En  cas  de  no  efectuar  el  pagament  amb  descompte  del  50%,  continua  la  tramitació  pelprocediment ordinari, que us permet formular al·legacions i proposar o aportar proves en el termini de 20 dies naturals des de lanotificació.  L'escrit  d'al·legacions  s'ha  d'adreçar  al  Servei  Territorial  de  Trànsit  corresponent  i  es  pot presentar en qualsevol dels registres legalment establerts (*).  Si no formuleu al·legacions ni aboneu l'import  de  la  sanció,  aquesta  denúncia  tindrà  efecte  d'acte  resolutori  del  procediment  sancionador. Contra  la  sanció  es  podrà  interposar  recurs  de  reposició,  amb  caràcterpotestatiu,  en  el  termini  d'un mes.  La  sanciópodrà  executar-se  transcorreguts  30  dies  naturals  des  de  la  notificació  d'aquesta denúncia.

ÒRGANS QUE INTERVENEN EN EL PROCEDIMENT

Òrgan  instructor:  el/la  cap  del  Servei  Territorial  de  Trànsit  de  Barcelona.  Autoritat  sancionadora:  la persona  titular  de  la  Direcció  del  Servei  Català  de  Trànsit  (article  11.1  de  la  Llei  14/1997,  de  24  de desembre, de creació del Servei Català de Trànsit, D.O.G.C. núm. 5537, de 31-12-2009)

RESOLUCIÓ DE L'EXPEDIENT SANCIONADOR

El  termini  màxim  per  resoldre  i  notificar  la  resolució  de  l'expedient  sancionador  iniciat  mitjançant aquesta denúncia és d'un any des de l'inici del procediment (article 112.3 TRLSV)

PÈRDUA DE PUNTS EN ELS PERMISOS I LLICÈNCIES DE CONDUCCIÓ

Els punts indicats a aquesta butlleta es detrauran quan la sanció sigui ferma. Podeu consultar el saldodepunts en [www.dgt.es](http://www.dgt.es/)

NOTIFICACIONS ELECTRÒNIQUES

La  TRLSV  ha  establert  que  a  partir  del  24-11-2010  es  puguin  efectuar  les  notificacionsper  mitjans electrònics. Si us voleu acollir a aquesta possibilitat, consulteu el web[http://transit.gencat.cat](http://transit.gencat.cat/)

FORMA DE PAGAMENT

Podeu utilitzar una de les següents modalitats per fer efectiu el pagament de la multa:

- Pagar-la directament amb targeta a l’agent que us ha denunciat.

- Pagar-la amb aquest imprès, per l’import i fins la data límit de pagament reflectits al peu de la butlleta de denúncia, a qualsevol de les oficines de CaixaBank.

- Pagar-la  amb targeta, directament a qualsevol de  les dependències territorials del  Servei Català de Trànsit.

- Pagar-la per internet mitjançant el portal[http://tramits.gencat.cat](http://tramits.gencat.cat/)

(*) Els subjectes **obligats a relacionar-se electrònicament** amb l’administració (art 14.2i 14.3de la Llei 39/2015 i art 3 de l’Ordre PDA/20/2019) han de presentar les al·legacions per internet accedint al web[http://transit.gencat.cat.](http://transit.gencat.cat/)

PROTECCIÓ DE DADES.

Tractament SCT: Expedients sancionadors per infraccions de trànsit. Responsable: la persona titular de  la  Direcció  de  l’SCT  (Diputació,  355,  08009  Barcelona).  Contacte  Delegat  de  protecció  de dades:Diputació,  355,  08009  Barcelonao dpd.interior@gencat.catFinalitat:  gestionar  les  dades relatives  als  expedients  sancionadors  que  s ́incoïn  per  infraccions  en  aquesta  matèria.  Informació addicional accediu al web de l'SCT.Tractament  Ajuntament  de  ...............:  amb  la  finalitat  de  generar  aquest  document,  les  dades personals seran tractades per l’Ajuntament de  xxxxxxxxxxxxxxxxxxxxxx   Podeu consultar informació addicional sobre aquest tractament i protecció de dades en www.xxxxxxxxxxxxxxxxxxxx
