# SCT-PDA
Documentació d'integració del servei SCT-PDA del Consorci AOC.

![](RackMultipart20211007-4-lhpxvq_html_9a7a6ca44ec1f4e7.png)

![image](https://user-images.githubusercontent.com/32306731/137329381-80aa8572-dce6-47b7-b687-c6df75a5ff37.png)


# **Via Oberta - SCT Denúncies**

# **Document d&#39;integració del servei**

![image](https://user-images.githubusercontent.com/32306731/137329514-3b8da43c-0abd-44ed-9bf3-6e2e885d9f9f.png)


![](RackMultipart20211007-4-lhpxvq_html_9ee666534977765a.png)

Realitzat per: Àrea de Tecnologia - Projectes
Versió: 1.1
Data: 17/5/2021

**Control del document**

**Informació general**

|
**Títol:** |
ViaOberta –SCT Denúncies |
| --- | --- |
|
**Creat per:** |
ÀreadeTecnologia -Projectes |
|
**A revisar per:** |
Àrea de Tecnologia -Suport Tècnic |
|
**Aaprovarper:** |
Àrea de Tecnologia-Suport Tècnic |
|
**Llistadedistribució:** |
 |
|
**Nomdeldocument:** |
DI-ViaOberta-SCTDenúncies.doc |

**Històric de revisions**

| Versió | Data | Autor | ComentarisTest |
| --- | --- | --- | --- |

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


# 1 Introducció

Aquest document detallala missatgeria associada al servei d&#39;enviament de denúncies al Servei Català de Trànsit(enendavantSCT).

Per a poder realitzar la integració cal conèixer prèviament la següent documentació:

- Document de Missatgeria Genèrica de la PCI del Consorci AOC.


# 2 Transmissions de dades disponibles

Les dades disponibles a través del servei són les que es presenten a continuació:

| **EMISSOR** |
| --- |
| ServeiCatalàdeTrànsit |
| **PRODUCTE** | **MODALITAT** | **DESCRIPCIO** |
| **SCT\_DENUNCIES** | SCT\_REMESA | Enviament de remesa de butlletes(frontal **asíncron** de la PCI). |
| SCT\_BUTLLETES | Obtenció de rang de butlletes(frontal **síncron** de la PCI). |
| SCT\_CATALEG | Descàrregadel catàleg de normatives (frontal **síncron** de la PCI). |


# 3 Missatgeria del sserveis

  
## 3.1 Enviament de remesade butlletes(SCT\_REMESA)

Enviament de les denúncies al sistema del SCT previa la seva incorporació al&#39;aplicació del Procediment Sancionador del SCT (PSN).

    
### 3.1.1 Petició–dades genèriques

El fitxer corresponent a la remesas&#39;hadereferenciaralblocdedades//Ficheros/Fichero de les dades genèriques de la sol·licitud.

| _Element_ | _Descripció_ |
| --- | --- |
| //Ficheros/Fichero/Contenido | ContingutdelfitxerencasdetransferènciaperMTOM(enlacridacorresponalareferència XOPdelfitxer). |

    
### 3.2.1 Remesa

| ![image](https://user-images.githubusercontent.com/32306731/137331712-bc31edd6-6b5b-4372-977b-6230938c4af6.png) | Per limitacions del sistema del SCT el fitxer de remesa no pot superar les 50 butlletes.
Actualment el sistema del SCT únicament suporta l&#39;enviament de denúncies de tipus genèrica. No hi ha previsió a curt termini per rebre denúncies de velocitat o d&#39;alcoholèmia.
ElSCT processa les remeses diàriament a les20h.Les remeses enviades posteriorment no es processaran fins al dia següent.
Terminid&#39;enviament:

- Caducitat de les denúncies:les denúncies no poden ser anteriors a 2mesos.


- El sistema de SCT treballa amb una finestra de processament de 3 dies laborables. Així,una remesa no pot contenir denúncies que puguin caducar abans de 3 dies des del&#39;enviament de la remesa.
 |
| --- | --- |

![image](https://user-images.githubusercontent.com/32306731/137331907-08511998-e779-482b-89d0-2cba19c4e1ed.png)

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
| //BUTLLETA/ACCIO | A:alta/B:anul·lació.Encas d&#39;anul·lació de butlletac al informar totes les dades de la butlleta, el motiu(MOTIU\_ANULLACIO) i la data d&#39;anul·lació(DATA\_HORA\_ANULLACIO). |
| //BUTLLETA/ID\_BUTLLETA | Identificador de la butlleta en el sistema origen o identificador dins de la remesa.
Dins del sistema del SCTl&#39;identificador de la denúncia són elselements SERVEI\_TERRITi NUM\_EXPEDIENT. |
| //BUTLLETA/SERVEI\_TERRIT | Demarcació territorial: 08,17,25,43. |
| //BUTLLETA/NUM\_EXPEDIENT | Número d&#39;expedient.Identificador de la denúncia en el sistemade lSCT.És un número de butlleta del rang de números de butlleta que s&#39;ha lliurat a l&#39;Ajuntament.
Permés detalls sobre el mecanisme d&#39; obtenció del rang de butlletes vegeu l&#39;apartat |
| //BUTLLETA/DIGIT\_CONTROL | Dígit de control de la butlleta. Vegeu l&#39;annex [_Càlcul del_](#_bookmark19)[_dígit __de control__ d&#39;un número__d&#39;expedient_.](#_bookmark19) |
| //BUTLLETA/TIPUS\_DENUNCIA | Tipusdedenúncia:
- G:genèrica.
- A: alcoholèmia (aquest cas requereix informar blocdedades DENUNCIA\_ALCOHOLEMIA).
- V:velocitat(aquestcasrequereixinformarblocdedades DENUNCIA\_VELOCITAT).
 |
| //BUTLLETA/DATA\_DENUNCIA | Data de la denúncia(formatAAAAMMDD). |
| //BUTLLETA/HORA\_DENUNCIA | Hora de lad enúncia(format HHMISS). |
| //BUTLLETA/IDIOMA\_DENUNCIA | C:català/E:castellà |
| //BUTLLETA/NORMA\_DENUNCIA | Norma infringida(del catàleg de normatives). |
| //BUTLLETA/ARTICLE\_DENUNCIA | Codi de l&#39;article de la infracció(del catàleg de normatives). |
| //BUTLLETA/SUBARTICLE\_DENUNCIA | Codidesubarticlede la infracció(del catàleg de normatives). |
| //BUTLLETA/OPCIO\_DENUNCIA | Número d&#39;opció(del catàleg de normatives). |
| //BUTLLETA/PUNTS | Punts(del catàleg de normatives). |
| //BUTLLETA/MESOS\_RETIRADA | Suspensió(del catàleg de normatives). |
| //BUTLLETA/NUM\_DENUNCIANT | Número de l&#39;agent denunciant. |
| //BUTLLETA/NUM\_NOTIFICADOR | Número de l&#39;agent denunciant. |

| _Element_ | _Descripció_ |
| --- | --- |
|
 |
 |
| //BUTLLETA/TIPUS\_VIA | Laviaidentificaelllocons&#39;hacoméslainfracció,potserdedos tipus:

- V:Via inter urbana(carretera)
- C:Via urbana(carrer)
Quan la via és interurbana s'ha d'indicar:

- A l'element VIA, el codi de carretera(p.e.C-33).
- A l'element VIA\_NUMERO,el punt quilomètric de la denúncia (format fins a dos dígits decimals iseparadorcoma,p.e.11,20).

Quan la via és urbana s'ha d'indicar:

- A l'element VIA,el nom del carrer.
- A l'element VIA\_NUMERO,el número de carrer de la denúncia(valor sencer sense part decimal).
 |
| //BUTLLETA/VIA | Via de la denúncia. |
| //BUTLLETA/VIA\_NUMERO | Número de la via. |
| //BUTLLETA/DESCRIPCIO\_POBLACIO | Descripció de la població. |
| //BUTLLETA/DIRECCIO\_DENUNCIA | Sentit de la denúncia. |
| //BUTLLETA/NUM\_AGENT\_COBRADOR | Número de l&#39;agent cobrador. |
| //BUTLLETA/IMPORT\_NOMINAL | Import de la quantia de la denúncia amb dos decimals.10 primeres posicions és la part sencera (amb zeros al&#39;esquerra) i les dues darreres la part decimal.
Per exemple,100:000000010000. |
| //BUTLLETA/IMPORT\_PAGAT | Import pagat de la butlleta amb dos decimals.Format idèntica IMPORT\_NOMINAL. |
| //BUTLLETA/IMPORT\_DESCOMPTE | Import de la denúncia amb descompte amb dos decimals. Format idèntica IMPORT\_NOMINAL. |
| //BUTLLETA/DATA\_LIMIT\_DESCOMPTE | Data límit del descompte(format AAAAMMDD).20 dies des de la data de la infracció segons llei actual. |
| //BUTLLETA/IND\_NOTIFICACIO | Indicador de signatura denunciat i notificació:
- X:no notificada.
- S:notificada.
 |
| //BUTLLETA/M\_NO\_NOTIF | Motiu no notificació(obligatori quan és una denúncia no notificada): |

| _Element_ | _Descripció_ |
| --- | --- |
|
 |
- 0001:Conductor absent
- 0002:Circular en sentit contrari
- 0003:Assistència en accident
- 0004:Servei d&#39;urgència
- 0005:Regulació de trànsit
- 0006:Prova esportiva/recreativa
- 0007:Transport especial
- 0008:Desobediència agent
- 0009:Helicòpter
- 0010:Inexistèncialloperaturar infractor
- 0011:Servei a peu
- 0012:Formular una altra denúncia
- 0013:Perill per a la circulació
- 0014:Responsabilitat titular
- 0015:Completar dades
- 0017:Seguretat per a la resta d&#39;usuaris
- 0018:Requalificació de denuncia
- 0019:Imatge captada automàticament
- 0020:Atestats
- 0021:Vehicle no logotipat
- 0022:Denúncia voluntària
- 0023:Manca resultat analítica
- 0024:Control estupefaents/RESIDENT
- 0025:Denúncia incoada d&#39;ofici
- 0026:Manca resultat analítica
 |
| //BUTLLETA/DATA\_HORA\_ANULLACIO | Data i hora de l&#39;anul·lació(formatAAAA-MM-DDHH:MI:SS). Obligatori quan és una denúncia anul·lada. |
| //BUTLLETA/MOTIU\_ANULLACIO | Motiu anul·lació.Obligatori quan és una denúncia anul·lada:

- 0001:Fet no sancionable
- 0002:Denúncia duplicada
- 0003:Butlleta anul·lada per l&#39;agent
- 0004:Butlleta deteriorada
- 0005:Manca de competència per sancionar
- 0006:Retard en la tramesa denúncia al SCT
- 0007:Error/Manca dades bàsiques denúncia
- 0008:Error o manca de DNI
- 0009:Denúncies de Transports
- 0010:Fotos no vàlides
- 0011:Anul·lada canvi adscripció territorial
- 0012:Butlleta anul·lada per reposició models
- 0013:Butlleta anul·lada per docència
- 0014:Butlleta anul·lada a petició SCT
- 0015:SENSE ESPECIFICAR
- 0016:Butlleta no utilitzada
- 0017:Trasllat de l&#39;expedient
- 0018:Prescripció de la infracció
- 0021:Fet no sancionable
- 0024:Trasllat de l&#39;expedient
- 0025:Prescripció de la infracció
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
- S:dades del vehicle obtingudes de consulta a la base de dades de la DGT
- N:introduïdesmanualment perl&#39;agent
 |
| //BUTLLETA/DESCRIPCIO\_MARCA | Marca. |
| //BUTLLETA/DESCRIPCIO\_MODEL | Model. |
| //BUTLLETA/COLOR\_VEHICLE | Color. |
| //BUTLLETA/TIPUS\_VEHICLE |
- 00:Sense valor
- 01:Bicicleta
- 02:Ciclomotor
- 03:Motocicleta
- 04:Turisme
- 05:Furgoneta
- 06:Remolc
- 07:Camió
- 08:Autobús
- 09:Altres vehicles
- 10:Temporals
- 11:Turístiques
- 12:Vehicle especial
- 23:Motocicleta estrangera
- 24:Turisme estranger
- 25:Furgoneta estrangera
- 27:Camió estranger
- 28:Autobús estranger
- 29:Vehicle genèric
- 30:Vehicle especial
 |
| //BUTLLETA/MATRICULA\_DENUNCIA | Número de la matrícula. |
| //BUTLLETA/NUMERO\_BASTIDOR | Número de bastidor. |
| //BUTLLETA/DESCRIPCIO\_PAIS | Descripció del país.ESPANYAen cas d&#39;Espanya.
Encas de descripció ESPANYA actualmente lSCT no valida el format de la matrícula pels vehicles espanyols però es recomana ajustar-se als formats proposats en l&#39;apartat [3.1.3.2](#_bookmark11) si en un futur el SCT realitza la validació. |

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/IND\_IMMOBILITZACIO\_VEH | Indicador d&#39;immobilització del vehicle (S/ N). |
| //BUTLLETA/NUM\_ACTA\_IMMOBILITZACIO | Número d&#39;acta d&#39;immobilització. Obligatori si IND\_IMMOBILITZACIO\_VEH=S. |
| //BUTLLETA/NOM\_TITULAR | Nom del titular. |
| //BUTLLETA/COGNOM1\_TITULAR | Primer cognom del titular. |
| //BUTLLETA/COGNOM2\_TITULAR | Segon cognom del titular. |
| //BUTLLETA/NIF\_TITULAR | Número de document identificador del titular /propietaridelvehicle(NIF,NIE,CIF,passaportoaltresdocuments). |
| //BUTLLETA/ADRECA\_TITULAR | Adreçadeltitular. |
| //BUTLLETA/POBLACIO\_TITULAR | Població del titular. |
| //BUTLLETA/PROVINCIA\_TITULAR | Província del titular. |
| //BUTLLETA/CODI\_POSTAL\_TITULAR | Codi postal del titular. |
| //BUTLLETA/FET\_DENUNCIAT | Descripció del fet denunciat.Text lliure,si bé pot  portar la informació del catàleg de normatives. |
| //BUTLLETA/FET\_DENUNCIAT2 | Descripció del fet denunciat.Text lliure addicional. |
| //BUTLLETA/IND\_DGT\_CONDUCTOR |
- S:dades del conductor obtingudes de consulta a la base de dades de la DGT
- N:Introduïdes manualment per l&#39;agent
 |
| //BUTLLETA/INDICADOR\_CONDUCTOR |
- I:infractornoconductor
- C:conductor
 |
| //BUTLLETA/TIPUS\_DOCUMENT |
- 01:Persona física
- 02:Persona jurídica
- 03:Estranger resident
- 04:Estranger no resident
- 05:Sense identificar
 |
| //BUTLLETA/NUMERO\_DOCUMENT | Número de document. |
| //BUTLLETA/TIPUS\_PERMIS | Classe permís de conduir(A,B,etc.). |
| //BUTLLETA/DATA\_EXPEDICIO | Data d&#39;expedició(formatAAAAMMDD). |
| //BUTLLETA/NOM\_CONDUCTOR | Nomd el conductor. |
| //BUTLLETA/COGNOM1\_CONDUCTOR | Primer cognom del conductor. |
| //BUTLLETA/COGNOM2\_CONDUCTOR | Segon cognom del conductor. |

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/DATA\_NAIXEMENT\_CONDUCTOR | Data de naixement(formatAAAAMMDD). |
| //BUTLLETA/DESCRIPCIO\_PAIS\_CONDUCTOR | Nacionalitat del conductor. |
| //BUTLLETA/DOMICILI\_CONDUCTOR | Domicili del conductor. |
| //BUTLLETA/DESC\_POBLACIO\_CONDUCTOR | Població del domicili del conductor. |
| //BUTLLETA/CODI\_POSTAL\_CONDUCTOR | Codi postal del conductor. |
| //BUTLLETA/OBSERVACIONS | Observacions. |
| //BUTLLETA/IMATGE | Butlleta codificada en base 64(màxim400K). |
| //BUTLLETA/TIPUS\_IMATGE | Format de la butlleta(jpg/pdf). |
| //BUTLLETA/DENUNCIA\_VELOCITAT | Bloc de dades corresponents a les dades de la denúncia en cas de TIPUS\_DENUNCIA=V.Per més detalls vegeu l&#39;apartat [3.1.2.2.](#_bookmark6) |
| //BUTLLETA/DENUNCIA\_ALCOHOLEMIA | Bloc de dades corresponents a les dades de la denúncia en cas de TIPUS\_DENUNCIA=A.Per més detalls vegeu l&#39;apartat [3.1.2.3.](#_bookmark7) |
| //BUTLLETA/TARGETA | Bloc de dades corresponents a les dades depagament.Permésdetallsvegeul&#39;apartat[3.1.2.4.](#_bookmark8) |

      1.
#### Denúnciavelocitat

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | S&#39;ha previst aquest bloc de dades pel futur enviament de les denúncies de velocitat. Mentrestant,no s&#39;ha d&#39;informar el bloc de dadesDENUNCIA\_VELOCITAT(només es suporta TIPUS\_DENUNCIA=G). |
| --- | --- |

| _Element_ | _Descripció_ |
| --- | --- |
| //DENUNCIA\_VELOCITAT/VELOCITAT\_REGISTRADA | Km/h.
- 3 primers dígits:part sencera,zeros a l&#39;esquerra
- 3 darrers dígits:part decimal,zeros a la dreta Per exemple,142 Km/h: 142000.
 |
| //DENUNCIA\_VELOCITAT/VELOCITAT\_LIMIT | Km/h.4dígitssencers,zerosal&#39;esquerra.Perexemple,120 Km/h: 0120. |
| //DENUNCIA\_VELOCITAT/TIPUS\_LIMITACIO |
- U:Limitació envia urbana
- I:Limitació envia interurbana
- F:Limitació fixada per senyal
 |
| //DENUNCIA\_VELOCITAT/CINEMOMETRE | Cinemòmetre. |

| _Element_ | _Descripció_ |
| --- | --- |
| //BUTLLETA/CODI\_ANTENA | Antena. |

      1.
#### Denúnciaalcoholèmia

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | S&#39;ha previst aquest bloc de dades pel futur enviament de les denúncies d&#39;alcoholèmia. Mentrestant,no s&#39;ha d&#39;informar el bloc de dades DENUNCIA\_ALCOHOLEMIA(només es suporta TIPUS\_DENUNCIA=G). |
| --- | --- |

| _Element_ | _Descripció_ |
| --- | --- |
| //DENUNCIA\_ALCOHOLEMIA/TIPUS\_LECTURA |
- A:Aire espirat
- S:Contingut en sang
 |
| //DENUNCIA\_ALCOHOLEMIA/PCT\_1\_LECTURA | Taxa alcoholèmia 1a prova.
- 3 primers dígits: part sencera, zeros a l&#39;esquerra
- 3 darrers dígits: part decimal, zeros a la dreta Perexemple,0,39: 000390.
 |
| //DENUNCIA\_ALCOHOLEMIA/DATA\_1\_LECTURA | Data 1a prova(format AAAAMMDD). |
| //DENUNCIA\_ALCOHOLEMIA/HORA\_1\_LECTURA | Hora 1a prova(formatHHMISS). |
| //DENUNCIA\_ALCOHOLEMIA/PCT\_2\_LECTURA | Taxa alcoholèmia 2a prova. Format idèntic a PCT\_1\_LECTURA. |
| //DENUNCIA\_ALCOHOLEMIA/DATA\_2\_LECTURA | Data 2a prova(format AAAAMMDD). |
| //DENUNCIA\_ALCOHOLEMIA/HORA\_2\_LECTURA | Hora 2a prova(formatHHMISS). |
| //DENUNCIA\_ALCOHOLEMIA/MODEL\_ETILOMETRE |
- 01:Dräger Alcotest 7110
- 02:Lion 1400LS
- 03:Dräger Alcotest 7410
- 04:Alcotest7110-E
 |
| //DENUNCIA\_ALCOHOLEMIA/NUMERO\_ETILOMETRE | Número de sèrie de l&#39;etilòmetre. |

      1.
#### Targeta

| ![](RackMultipart20211007-4-lhpxvq_html_2510d52f0494e7cf.png) | S&#39;ha previs taquest bloc de dades per un possible ús futur del pagament amb targeta. Mentrestant, el valor de l&#39;element IND\_TARGETA serà sempre N. |
| --- | --- |

| _Element_ | _Descripció_ |
| --- | --- |
| //TARGETA/IND\_TARGETA |
- S:pagament amb targeta
- N:sensetargeta, no implica que s&#39;hagi fet el pagament en metàl·lic
 |

| _Element_ | _Descripció_ |
| --- | --- |
| //TARGETA/NUMERO\_TARGETA | 4últims dígits de la targeta. |
| //TARGETA/DATA\_CADUCITAT\_TARGETA | Data de caducitat de la targeta(format AAAAMMDD). |
| //TARGETA/NUMERO\_TERMINAL | Número de terminal. |
| //TARGETA/CODI\_COMERC | Codi de comerç. |
| //TARGETA/NUMERO\_COMANDA | Número de comanda. |
| //TARGETA/NUMERO\_AUTORITZACIO | Número d&#39;autorització. |
| //TARGETA/DATA\_JUSTIFICANT | Data del justificant(formatAAAAMMDD). |
| //TARGETA/HORA\_JUSTIFICANT | Hora del justificant(formatHHMISS). |

    1. **Resposta**** específica**

![](RackMultipart20211007-4-lhpxvq_html_2a0d348306953ebf.jpg)

| _Element_ | _Descripció_ |
| --- | --- |
| /respostaEnviamentRemesa/DADES | Bloc dedadescorresponentaldetalldel&#39;enviament de la remesa. |
| //DADES/CAPCALERA/FITXER\_PDA | Nom de fitxer de la remesa.Referència de la remesa. |
| //DADES/CAPCALERA/NUM\_BUTLLETES | Númerode butlletesquecontélaremesa. |
| //DADES/CAPCALERA/CODI\_INCIDENCIA | Codidelaincidència. |
| //DADES/CAPCALERA/DESCRIPCIO\_INCIDENCIA | Descripciódelaincidència |
| //DADES/BUTLLETES/BUTLLETA | Bloc de dades corresponent al resultat del tractament d&#39;una butlleta. |
| //DADES/BUTLLETES/BUTLLETA/ID\_BUTLLETA | Identificador de la butlleta en el sistema origeno |

| _Element_ | _Descripció_ |
| --- | --- |
|
 | identificadordinsde laremesa. |
| //DADES/BUTLLETES/BUTLLETA/SERVEI\_TERRIT | Servei territorial. |
| //DADES/BUTLLETES/BUTLLETA/NUM\_EXPEDIENT | Número d&#39;expedient. |
| //DADES/BUTLLETES/BUTLLETA/RESULTAT |
- 0:tractamentcorrecte
- 1:contébutlletesamb errors no crítics
- 2:contébutlletesamb errors crítics
Quan s&#39;intenta carregar una butlleta, si no supera les validacions del sistema del SCT queda marcada com a crítica i no es tramita. Per tal de tramitar-la cal reenviar-la amb l&#39;error crític corregit. |
| //DADES/BUTLLETES/BUTLLETA/DATA\_LIMIT | Per a butlletes crítiques, data màxima per a reenviar-la amb les dades corregides(formatAAAAMMDD). |
| //DADES/BUTLLETES/BUTLLETA/INCIDENCIES | Bloc de dades corresponent a la relació d&#39;incidències detectades en la butlleta. |
| //INCIDENCIES/INCIDENCIA | Bloc de dades corresponent a una incidència detectada en la butlleta. |
| //INCIDENCIA/CODI\_INCIDENCIA | Codi de incidència.Vegeu apartat[3.1.3.1](#_bookmark10) d&#39;aquest document. |
| //INCIDENCIA/DESCRIPCIO\_INCIDENCIA | Descripció d&#39;incidència. |
| //INCIDENCIA/INFORMACIO\_ADDICIONAL | Informació addicional de la incidència. |
| /respostaEnviamentRemesa/resultat/codiResultat |
- 0: enviament de la remesa realitzat correctament (detalls de cada butlleta a l&#39;element DADES).
- 0502:error realitzant l&#39;enviament.
 |
| /respostaEnviamentRemesa/resultat/descripcio | Descripció del resultat. |

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
| CRÍTIC | DAT001 | Data errònia | DATA\_DENUNCIA | FormatincorrecteAAAAMMDD. |
| NO CRÍTICA | DAT002 | Data errònia | DATA\_LIMIT\_DESCOMPTE | FormatincorrecteAAAAMMDD. |
| CRÍTIC | DAT003 | Data errònia | DATA\_HORA\_ANULLACIO | El valor no es pot convertir a una data segons el format: YYYY-MM-DD-HH:MI:SS&#39;. |
| CRÍTIC | HOR001 | Hora errònia | HORA\_DENUNCIA | El valor no es pot convertir a una hora segons el format HHMISS. |
| _Validacionsdecontingut_ |
| CRÍTIC | BUT002 | Butlleta duplicada | SERVEI\_TERRITNUM\_EXPEDIENT | Aquesta butlleta ja existeix al sistema.
Una butlleta només és pot enviar una vegada, amb ACCIO:
- A:Alta.
- B:Anul·lació.

Només s&#39;admet una butlleta repetida quan es tracta del reenviament de una butlleta crítica. |
| CRÍTIC | BUT003 | Butlleta fora derang | SERVEI\_TERRITNUM\_EXPEDIENT | La butlleta no correspon al rang assignat a la policia local corresponent. |
| CRÍTIC | BUT004 | Element obligatori NO informat | ACCIONORMA\_DENUNCIAARTICLE\_DENUNCIASUBARTICLE\_DENUNCIAOPCIO\_DENUNCIANUM\_DENUNCIANTTIPUS\_VIAVIAVIA\_NUMEROIMPORT\_NOMINALIMPORT\_PAGATIMPORT\_DESCOMPTEDATA\_LIMIT\_DESCOMPTEIND\_NOTIFICACIO |
 |
| CRÍTIC | BUT004 | Element obligatori NO informat | INDICADOR\_CONDUCTORTIPUS\_DOCUMENTNUMERO\_DOCUMENTNOM\_CONDUCTORCOGNOM1\_CONDUCTORCODI\_PAIS\_CONDUCTORDOMICILI\_CONDUCTORCODI\_MUNICIPI\_CONDUCTOR | Aquests elements només són obligatoris per a denúncies notificades. |
| CRÍTIC | BUT007 | Codi control butlleta erroni | DIGIT\_CONTROL |
 |
| NO CRÍTICA | BUT011 | Camp massa llarg |
 | Són camps que en l&#39;entorn PDA sónmésgrans queen entornPSN.
Elements la grandària dels quals és més grana la missatgeria de la |

| _Tipus_ | _Codi_ | _Descripció_ | _Campsvalidats_ | _Validació_ |
| --- | --- | --- | --- | --- |
|
 |
 |
 |
 | remesa que als sistemes del SCT. |
| NO CRÍTICA | BUT013 | Manca codipostal | CODI\_POSTAL\_CONDUCTOR | El codi postal del conductor no estàinformat. |
| CRÍTIC | BUT014 | Butlleta arxivada | SERVEI\_TERRITNUM\_EXPEDIENT | S&#39;ha tornat a enviar una butlleta que ja s&#39;havia arxivat perquè s&#39;havia rebutcom a CRÍTICA amb errors CRÍTICS i s&#39;ha exhaurit el termini per reenviar-la. |
| NO CRÍTICA | BUT015 | Butlleta reenviada | SERVEI\_TERRITNUM\_EXPEDIENT | Les butlletes reenviades generaran una incidència no crítica per forçar que passin pel mòdul de validació de PSN, malgrat que no hi hagi cap altra incidència en la butlleta. |
| CRÍTIC | BUT018 | Butlleta pagada no notificada | IMPORT\_PAGATIND\_NOTIFICACIO | Quanl&#39;elementIND\_NOTIFICACIOsigui &quot;X&quot; (butlleta no notificada),l&#39;import pagat ha de ser 0, si no és així es genera error. |
| CRÍTIC | NOR001 | Normativainexistent | NORMA\_DENUNCIAARTICLE\_DENUNCIASUBARTICLE\_DENUNCIAOPCIO\_DENUNCIA | No existeix al catàleg de normativa legal. |
| NOCRÍTICA | NOR002 | Normativa NOvigent | NORMA\_DENUNCIAARTICLE\_DENUNCIASUBARTICLE\_DENUNCIAOPCIO\_DENUNCIA | Existeix al catàleg de normativa legal però no és vigent respecte a la data de la denúncia. |
| NO CRÍTICA | NOR003 | Import de la quantia de la denúncia incorrecte | IMPORT\_NOMINAL | Import incorrecte per la normativa infringida. |
| NO CRÍTICA | NOR004 | Nombre de punts adetreure incorrecte | PUNTS | Punts incorrectes per la normativa infringida. |
| CRÍTIC | NOT001 | Camp obligatori NO notificació NO informat | M\_NO\_NOTIF | Quanl&#39;elementIND\_NOTIFICACIOsigui &quot;X&quot; (butlleta no notificada), el motiu és obligatori. |
| CRÍTIC | ANU001 | Camp obligatori anul·lació NO informat | DATA\_HORA\_ANULLACIOMOTIU\_ANULLACIO | És obligatori quan l&#39;element ACCIO és &quot;B&quot; (anul·lació). |
| CRÍTIC | MAT001 | Format matricula errònia | MATRICULA\_DENUNCIA | Actualment no es valida el format de la matrícula pels vehicles espanyols(DESCRIPCIO\_PAIS=ESPANYA)tot i que en un futur el SCT podria validar-lo. |

      1.
#### Formats de matrícula

Formats de matrícula recomanats pel SCT:

- Turisme/Motocicleta/Camió/Furgoneta/Autobús(on n dígits, L lletres, b espais).

nnnnLLL LLnnnnLL LLnnnnbL LLnnnnnn LbnnnnLL LbnnnnbL Lbnnnnnn

- Remolc(on n dígits i L lletres):

RnnnnLLL

- VehiclesEspecials(onnnúmeros,Llletres, Efixa,bespais):

EnnnnLLL LLnnnnnE LbnnnnnE LLnnnnnnE LbnnnnnnE

- Turístics(onnnúmeros,Llletres,Tfixa,bespais):

TnnnnLLL nnLLnnnn nnLbnnnn

- Temporals(on n números, L lletres, T, R, P, S, V fixes, b espais):

LLnnnnTnn LbnnnnTnn LLnnnnRnn LbnnnnRnn PnnnnLLL SnnnnLLL nnnnLLL

- Ciclomotors(onnnúmeros,Llletres,Cfixa):

CnnnnLLL

- Altres Vehicles(o n nnúmeros,L lletres, CD, OI, CC, TA, H, PMM,PGC fixes,b espais):

| CDnnnn | OInnnn | CCnnnn | TAnnnn | HnnnnLLL | PMMnnnnnn |
| --- | --- | --- | --- | --- | --- |
| PMMnnnnLL | PMMnnnnbL | PGCnnnnnn | PGCnnnnLL | PGCnnnnbL |
 |

  1.
## Obtenció de rang de butlletes(SCT\_BUTLLETES)

Les policies locals necessiten disposar de butlletes del SCT per poder interposar denúncies competència del SCT. Actualment disposen de talonaris de butlletes en paper lliurats per el SCT que tenen preimprès el número de butlleta(expedient).

Per aquelles policies que s&#39;acullin al sistema de denúncies via PDA ofereix aquesta modalitat per obtenir rangs de butlletes.

LesdenúnciescompetènciadelSCThand&#39;estaridentificades per:

- SERVEI\_TERRIT:demarcacióterritorial.

- NUM\_EXPEDIENT:no és un valor aleatori,és un número de butlleta del rang de números que es lliura a la policial local corresponent.

Aquesta informació ha de mostrar-se en les butlletes que la policia local notifica als infractors. També en aquelles no notificades.

    
### 3.2.1 Petició–dades específiques

![image](https://user-images.githubusercontent.com/32306731/137328706-df5c9ce6-fa3b-4350-9042-07e343fca52c.png)

| _Element_ | _Descripció_ |
| --- | --- |
| /resposta Obtencio Rang Butlletes/NUM\_BUTLLETES\_SOLICITADES | Número de butlletes sol·licitades(màxim9999). |

    
### 3.2.2 Resposta –dades específiques

![image](https://user-images.githubusercontent.com/32306731/137328536-ce4cb9ec-160f-475e-a6a7-a4d8cbf4384d.png)


| _Element_ | _Descripció_ |
| --- | --- |
| /respostaObtencioRangButlletes/SORTIDA/RESULTAT |
- 0: s&#39;han lliurat les butlletes sol·licitades.
- 1: s&#39;han lliurat menys butlletes de les sol·licitades.
- 2: no es disposa de butlletes.En cas que s&#39;obtingui aquest error contacteu amb el SCT.
 |
| /respostaObtencioRangButlletes/SORTIDA/NUM\_BUTLLETES\_LLIURADES | Número de butlletes lliurades. |
| /respostaObtencioRangButlletes/SORTIDA/RANGS/RANG | Bloc de dades corresponent a un rang de butlletes.El sistema del SCT pot lliurar el nombre de butlletes en rangs discontinus. |
| //RANG/ID\_RANG | Identificador del rang. |
| //RANG/SERVEI\_TERRIT | Demarcació territorial. |
| //RANG/TALONARI\_INICIAL | Valor inicial del rang.Número de butlleta inicial. |
| //RANG/TALONARI\_FINAL | Valor final del rang.Número de butlleta final. |
| /respostaObtencioRangButlletes/resultat/codiResultat |
- 0: consulta realitzada correctament.
- 0502: error realitzant la consulta.
 |
| /respostaObtencioRangButlletes | Descripció del resultat. |

| /resultat/descripcio |
 |
| --- | --- |

  
## 3.3 Descàrrega del catàleg de normatives(SCT\_CATALEG)

Les policies locals necessiten disposar del catàleg de normatives per poder indicar la norma infringida quan interposenuna denúncia competència del SCT.

Actualmentdisposend&#39;uncatàlegd&#39;infraccionsimprèsenformatdeminillibre,quanrealitzenunadenúnciaescriuenmanualmentalabutlletalesdadesidentificativesdelaopciónormativainfringida.

Per aquelles policies que s&#39;acullin al sistema de denúncies via PDA, s&#39;ofereix una modalitat per obtenir el catàleg de normatives en format digital.

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
| //NORMATIVA/IMPORT\_NOMINAL | Quantia de la multa sense descompte amb dos decimals. 10 primeres posicions són la part sencera(amb zeros a l&#39;esquerra) i les dues darreres la part decimal.
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

![image](https://user-images.githubusercontent.com/32306731/137328964-69421ef9-e63d-46a0-9f7c-9c24723aac9e.png)

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

4. Multiplicar cada dígit del resultat obtingut pel valor que es troba en la mateixa posició en el següent array (constant).

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

![image](https://user-images.githubusercontent.com/32306731/137285335-e6b319e8-d76d-4632-915e-92553adda3aa.png)


5. Dividir el valor obtingut entre 11 i quedar-se amb el residu.

![image](https://user-images.githubusercontent.com/32306731/137285147-baec349f-44c0-48b0-9e52-0fe1a68f62ac.png)

6. Si el residu és 10, el dígit de control serà 0. En qualsevol altre cas serà el valor obtingut.

Així,el número d&#39;expedient complert serà 08/5168515-0.

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
