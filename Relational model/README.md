

<img src="https://ciudadesabiertas.es/assets/img/cabiertas/logo.svg" alt="LogoCiudadesAbiertas" width="200"/> 

# DESARROLLO API REST DE DATOS REUTILIZABLE. MODELO DE TABLAS: CENSO DE LOCALES

&nbsp;

## **ÍNDICE**   
1. [AUTORES](#id1)
2. [LINKS](#id2)
3. [DIAGRAMA CONCEPTUAL](#id3)
4. [TABLAS](#id4)  
    - [LOCAL_COMERCIAL](#id5)  
    - [LOCAL_COMERCIAL_AGRUPACION](#id6)  
    - [LOCAL_COMERCIAL_LICENCIA](#id7)  
    - [LOCAL_COMERCIAL_TERRAZA](#id8) 
5. [TAXONOMÍAS SKOS](#id9)
    - [PERIODO-FUNCIONAMIENTO](#id10)
    - [TIPO-SITUACION](#id11)
    - [TIPO-ESTADO-TRAMITE-LICENCIA](#id12)
    - [TIPO-AGRUPACION](#id13)
    - [CNAE](#id14)



&nbsp;

## AUTORES <a name="id1"></a>
- Juan Carlos Ballesteros
- Leticia Rubalcaba
- Oscar Corcho
- Paola Espinoza Arias

&nbsp;

## LINKS <a name="id2"></a>


Este documento contiene la información detallada del modelo de datos asociado al vocabulario de los convenios. A continuación, se detallan los enlaces de interés asociados a este vocabulario:

- *[Documentación](http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial/index-es.html)*
- *[Repositorio](https://github.com/CiudadesAbiertas/vocab-comercio-censo-locales)*
- *[Webinar](https://youtu.be/LCgEPuI8KD8)*
- *[Requisitos](https://github.com/CiudadesAbiertas/vocab-comercio-censo-locales/blob/master/requirements/Requisitos-Censo%20de%20locales%2C%20terrazas%2C%20licencias%20de%20actividades%20.xlsx)*
- *[Issues](https://github.com/CiudadesAbiertas/vocab-comercio-censo-locales/issues)*

&nbsp;

## DIAGRAMA CONCEPTUAL <a name="id3"></a>

El diagrama muestra las clases y propiedades del vocabulario que representa los convenios adoptados por los ayuntamientos con otras entidades:  
&nbsp;
![Diagrama conceptual](http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial/resources/images/CensoLocalesLicenciasActividad.png)
&nbsp;



## TABLAS <a name="id4"></a>
En principio se considera esta estructura de datos bastante estable y no se estima que sufrirá cambios. Pero puesto que la actuación D2, que es donde se enmarca la definición de estas tablas, aún está en desarrollo, no se puede asegurar al 100% que será la definitiva.     


[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### LOCAL_COMERCIAL <a name="id5"></a>
&nbsp;

|     Campo                       |     Tipo             |     Ejemplo                                         |     Descripción                                                                                                                                                                                                                                                                                                                                                                                                                     |     URL                                                                                      |
|---------------------------------|----------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
|     ikey                        |     varchar(50)      |     1                                               |     Identificador de la Tabla (PK).                                                                                                                                                                                                                                                                                                                                                                                                 |                                                                                              |
|     id                          |     varchar(50)      |     285033785                                       |     Identificador de un local   comercial.                                                                                                                                                                                                                                                                                                                                                                                          |     http://purl.org/dc/terms/identifier                                                      |
|     title                       |     varchar(400)     |     SIN ACTIVIDAD                                   |     Un nombre del local comercial.                                                                                                                                                                                                                                                                                                                                                                                                  |     http://purl.org/dc/terms/title                                                           |
|     description                 |     varchar(400)     |     Descripcion   SIN ACTIVIDAD :                   |     Una   descripción del local comercial.                                                                                                                                                                                                                                                                                                                                                                                          |     http://purl.org/dc/terms/description                                                     |
|     municipio_id                |     varchar(10)      |     28079                                           |     El   identificador de un Municipio es el ente local definido en el artículo 140 de   la Constitución española y la entidad básica de la organización territorial   del Estado según el artículo 1 de la Ley 7/1985, de 2 de abril, Reguladora de   las Bases del Régimen Local.                                                                                                                                                 |                                                                                              |
|     municipio_title             |     varchar(200)     |     Madrid                                          |     Nombre de un   municipio, se especifica con la propiedad dct:title, geonames:name, y   rdf:label es el proporcionado por el Registro de Entidades Locales del   Ministerio de Política Territorial, en http://www.ine.es/nomen2/index.do                                                                                                                                                                                        |                                                                                              |
|     street_address              |     varchar(200)     |     Calle Geranios Num 16 B                         |     La dirección de la calle.                                                                                                                                                                                                                                                                                                                                                                                                       |     http://schema.org/streetAddress                                                          |
|     postal_code                 |     varchar(10)      |     28039                                           |     El código postal.                                                                                                                                                                                                                                                                                                                                                                                                               |     http://schema.org/postalCode                                                             |
|     distrito_id                 |     varchar(50)      |     28079606                                        |     Es el identificador de un   distrito. Un distrito es cada una de las demarcaciones en que se subdivide un   territorio o una población para distribuir y ordenar el ejercicio de los   derechos civiles y políticos, o de las funciones públicas, o de los servicios   administrativos [fuente: Diccionario de la Real Academia (DRAE) 2011].                                                                                   |                                                                                              |
|     barrio_id                   |     varchar(50)      |     280796062                                       |     Es el identificador de un   barrio. Un barrio es cada una de las partes en que se dividen los pueblos   grandes o sus distritos [fuente: Diccionario de la Real Academia (DRAE) 2011].                                                                                                                                                                                                                                          |                                                                                              |
|     x_etrs89                    |     decimal(13,5)    |     441176.61000                                    |     Coordenada X en metros (ETRS89).                                                                                                                                                                                                                                                                                                                                                                                                |     https://datos.ign.es/def/geo_core#xETRS89                                                |
|     y_etrs89                    |     decimal(13,5)    |     4480303.53999                                   |     Coordenada Y en metros (ETRS89).                                                                                                                                                                                                                                                                                                                                                                                                |     https://datos.ign.es/def/geo_core#yETRS89                                                |
|     telephone                   |     varchar(200)     |     9199999916                                      |     Número de teléfono.                                                                                                                                                                                                                                                                                                                                                                                                             |     https://schema.org/telephone                                                             |
|     url                         |     varchar(400)     |     http://api.ciudadesabiertas.org/id=285033785    |     .URL pública donde obtener información de la entidad.                                                                                                                                                                                                                                                                                                                                                                           |     http://schema.org/url                                                                    |
|     tipo_actividad_economica    |     varchar(10)      |     66                                              |     Tipo de actividad económica que   se realiza en un local comercial, de acuerdo con alguna clasificación SKOS.     http://vocab.linkeddata.es/datosabiertos/kos/comercio/cnae     http://vocab.linkeddata.es/datosabiertos/kos/comercio/iae                                                                                                                                                                                      |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#tipoActividadEconomica    |
|     nombre_comercial            |     varchar(200)     |     Nombre Comercial SIN ACTIVIDAD                  |     El nombre comercial es todo   aquel signo que puede ser representado gráficamente y, que identifica a una   empresa en el tráfico mercantil distinguiéndola de las demás empresas que van   a desarrollar actividades idénticas o similares.                                                                                                                                                                                    |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#nombreComercial           |
|     rotulo                      |     varchar(200)     |     Rotulo SIN ACTIVIDAD                            |     Signo o denominación que sirve   para dar a conocer al público un establecimiento comercial y para   distinguirlo de otros destinados a actividades idénticas o similares.                                                                                                                                                                                                                                                      |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#rotulo                    |
|     aforo                       |     int(11)          |     5                                               |     Capacidad del local, expresada   como el número de personas que caben en él.                                                                                                                                                                                                                                                                                                                                                    |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#aforo                     |
|     tipo_situacion              |     varchar(200)     |     clausurado                                      |     Un local comercial puede estar   en una de las siguientes situaciones: activo, cerrado, clausurado, o en   obras. Estos tipos de situaciones se representan mediante una lista de   conceptos de URI http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-situacion.                                                                                                                                                      |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#tipoSituacion             |
|     tipo_acceso                 |     varchar(200)     |     puerta de calle                                 |     Es de tipo SKOS http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-acceso                                                                                                                                                                                                                                                                                                                                               |                                                                                              |
|     referencia_catastral        |     varchar(100)     |     9872023 VH5797S 0001 WX                         |     La referencia catastral es el   identificador oficial y obligatorio de los bienes inmuebles. Consiste en un   código alfanumérico que es asignado por el Catastro de manera que todo   inmueble debe tener una única referencia catastral que permita situarlo   inequívocamente en la cartografía catastral.                                                                                                                   |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#referenciaCatastral       |
|     tiene_licencia_apertura     |     varchar(50)      |     270104879-106-2005-00105                        |     El local comercial puede tener   una o varias licencias de funcionamiento a lo largo de su historia.                                                                                                                                                                                                                                                                                                                            |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#tieneLicenciaApertura     |
|     tiene_terraza               |     varchar(50)      |     4972                                            |     Un local comercial puede tener   una terraza asociada.                                                                                                                                                                                                                                                                                                                                                                          |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#tieneTerraza              |
|     agrupacion_comercial        |     varchar(50)      |     99000218                                        |     Conjunto de locales situados en   uno o en diversos edificios de un mismo espacio comercial, en el cual se   pueden llevar a cabo diferentes actividades económicas. Este concepto incluye   centros comerciales, mercados, estaciones de tren y metro, etc. Es más   genérico que el concepto schema:ShoppingCenter, puesto que puede abordar   otros tipos de agrupaciones comerciales (por ejemplo, una calle comercial).    |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#AgrupacionComercial       |
|     portal_id                   |     varchar(50)      |     PORTAL000098                                    |     El   identificador de un portal.                                                                                                                                                                                                                                                                                                                                                                                                |                                                                                              |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### LOCAL_COMERCIAL_AGRUPACION <a name="id6"></a>
&nbsp;

|     Campo                        |     Tipo            |     Ejemplo                                |     Descripción                                                                                                                                    |     URL                                                                                       |
|----------------------------------|---------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
|     Ikey (PK)                    |     varchar(50)     |     1                                      |     Identificador de la   Tabla (PK).                                                                                                              |                                                                                               |
|     id                           |     varchar(50)     |     99000218                               |     Es el identificador del local comercial con agrupación.                                                                                        |     http://purl.org/dc/terms/identifier                                                       |
|     title                        |     varchar(400)    |     GALERIA DE ALIMENTACION VIÑA VIRGEN    |     El nombre o título de la agrupación de un local comercial.                                                                                     |     http://purl.org/dc/terms/title                                                            |
|     tipo_agrupacion_comercial    |     varchar(400)    |     galeria de alimentacion                |     Tipo de agrupación comercial, de   acuerdo con la lista de conceptos http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-agrupacion.    |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#tipoAgrupacionComercial    |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### LOCAL_COMERCIAL_LICENCIA <a name="id7"></a>
&nbsp;

|     Campo                           |     Tipo            |     Ejemplo                    |     Descripción                                                                                                                                                                                                                                                                                                                                                     |     URL                                                                                          |
|-------------------------------------|---------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
|     ikey                            |     varchar(50)     |     1                          |     Identificador de la   Tabla (PK).                                                                                                                                                                                                                                                                                                                               |                                                                                                  |
|     id                              |     varchar(50)     |     60000068/106-1993-02762    |     Es el identificador del local comercial con licencia.                                                                                                                                                                                                                                                                                                           |     http://purl.org/dc/terms/identifier                                                          |
|     referencia                      |     varchar(20)     |     60000068                   |                                                                                                                                                                                                                                                                                                                                                                     |                                                                                                  |
|     asociada_a                      |     varchar(200)    |     47                         |     Una licencia de apertura está asociada a un local comercial o a   una terraza.                                                                                                                                                                                                                                                                                  |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#asociadaA                     |
|     autoriza_actividad_economica    |     varchar(400)    |     106-1993-02762             |     Una licencia autoriza la realización de una o varias actividades   económicas. El tipo de actividad económica que se autoriza se representa de   acuerdo con alguna clasificación SKOS, preferentemente alguna de las   siguientes: http://vocab.linkeddata.es/datosabiertos/kos/comercio/cnae     http://vocab.linkeddata.es/datosabiertos/kos/comercio/iae    |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#autorizaActividadEconomica    |
|     estado_tramitacion              |     varchar(200)    |     60000068                   |     Estado de tramitación de la licencia, se representa con la lista   de conceptos SKOS http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-estado-tramite-licencia.                                                                                                                                                                                        |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#estadoTramitacion             |
|     fecha_alta                      |     datetime(6)     |     2009-03-10 00:00:00        |     Fecha en la que se ha resuelto la solicitud de la licencia.                                                                                                                                                                                                                                                                                                     |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#fechaAlta                     |
|     fecha_cese                      |     datetime(6)     |     2040-02-16 00:00:00        |     Fecha en la que se ha notificado el cese de la actividad   económica.                                                                                                                                                                                                                                                                                           |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#fechaCese                     |
|     fecha_solicitud                 |     datetime(6)     |     2010-02-16 00:00:00        |     Fecha en la que se ha solicitado la licencia.                                                                                                                                                                                                                                                                                                                   |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#fechaSolicitud                |
|     se_otorga_a                     |     varchar(200)    |     Mario Gomez Gomez          |     Una licencia se otorga a un titular.                                                                                                                                                                                                                                                                                                                            |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#seOtorgaA                     |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### LOCAL_COMERCIAL_TERRAZA <a name="id8"></a>
&nbsp;

|     Campo                        |     Tipo             |     Ejemplo                                        |     Descripción                                                                                                                                                                                                              |     URL                                                                                       |
|----------------------------------|----------------------|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
|     ikey                         |     varchar(50)      |     1                                              |     Identificador de la   Tabla (PK).                                                                                                                                                                                        |                                                                                               |
|     id                           |     varchar(50)      |     1693                                           |     Identificador de un local comercial con terraza.                                                                                                                                                                         |     http://purl.org/dc/terms/identifier                                                       |
|     numero_mesas_autorizadas     |     Int(11)          |     8                                              |     Número de mesas autorizadas para la terraza.                                                                                                                                                                             |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#numeroMesasAutorizadas     |
|     numero_sillas_autorizadas    |     Int(11)          |     32                                             |     Número de sillas autorizadas para la terraza.                                                                                                                                                                            |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#numeroSillasAutorizadas    |
|     periodo_funcionamiento       |     varchar(400)     |     Estacional                                     |     Periodo de funcionamiento de la terraza, que puede ser anual o   estacional. Los periodos se representan mediante la lista de conceptos http://vocab.linkeddata.es/datosabiertos/kos/comercio/periodo-funcionamiento.    |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#periodoFuncionamiento      |
|     superficie                   |     decimal(12,2)    |     6.14                                           |     Superficie en metros cuadrados ocupada por la terraza.                                                                                                                                                                   |     http://vocab.ciudadesabiertas.es/def/comercio/tejido-comercial#superficie                 |
|     opening_hours                |     varchar(400)     |     Lunes a jueves: de 10:00:00 hasta 01:00:00…    |     El horario general de apertura de una empresa.                                                                                                                                                                           |     https://schema.org/openingHours                                                           |
|     description                  |     varchar(400)     |     Acera                                          |     Una descripción del local comercial con   terraza.                                                                                                                                                                       |     http://purl.org/dc/terms/description                                                      |


&nbsp;

## TAXONOMÍAS SKOS <a name="id9"></a>
&nbsp;

### PERIODO-FUNCIONAMIENTO <a name="id10"></a>
http://vocab.linkeddata.es/datosabiertos/kos/comercio/periodo-funcionamiento
&nbsp;
Tesauro que recoge los tipos de periodos de funcionamiento de las terrazas.
|     Término       |     Label         |
|-------------------|-------------------|
|     anual         |     anual         |
|     estacional    |     estacional    |




&nbsp;
### TIPO-SITUACION <a name="id11"></a>
http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-situacion
&nbsp;
Tesauro que recoge los tipos de situación en los que se puede encontrar un local comercial.
|     Término       |     Label         |
|-------------------|-------------------|
|     activo        |     activo        |
|     cerrado       |     cerrado       |
|     clausurado    |     clausurado    |
|     en-obras      |     en obras      |



&nbsp;
### TIPO-ESTADO-TRAMITE-LICENCIA <a name="id12"></a>
http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-estado-tramite-licencia
&nbsp;
Tesauro que recoge los tipos de estado de tramitación de las licencias de apertura.
|     Término       |     Label         |
|-------------------|-------------------|
|     concedida     |     concedida     |
|     denegada      |     denegada      |
|     en-tramite    |     en trámite    |




&nbsp;
### TIPO-AGRUPACION <a name="id13"></a>
http://vocab.linkeddata.es/datosabiertos/kos/comercio/tipo-agrupacion
&nbsp;
Tesauro que recoge los tipos de agrupaciones comerciales.
|     Término                       |     Label                             |
|-----------------------------------|---------------------------------------|
|     aeropuerto                    |     Aeropuerto.                       |
|     centro-comercial              |     Centro comercial.                 |
|     estacion-metro                |     Estación de   metro.              |
|     estacion-tren                 |     Estación de tren.                 |
|     galeria-alimentacion          |     Galería de alimentación.          |
|     intercambiador-transportes    |     Intercambiador de transportes.    |
|     mercado-municipal             |     Mercado municipal.                |
|     no-comercial                  |     No comercial.                     |
|     pasaje-comercial              |     Pasaje comercial.                 |
|     recinto-ferial                |     Recinto ferial.                   |





&nbsp;
### CNAE <a name="id14"></a>
http://vocab.linkeddata.es/datosabiertos/kos/comercio/cnae
&nbsp;
Lista de códigos CNAE 2009.
|     Término    |     Label                                                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     A          |     Agricultura, ganadería, silvicultura y pesca.                                                                                                                |
|     B          |     Industrias extractivas.                                                                                                                                      |
|     C          |     Industria   manufacturera.                                                                                                                                   |
|     D          |     Suministro   de energía eléctrica, gas, vapor y aire acondicionado.                                                                                          |
|     E          |     Suministro de agua, actividades de saneamiento, gestión de   residuos y descontaminación.                                                                    |
|     F          |     Construcción.                                                                                                                                                |
|     G          |     Comercio al por mayor y al por menor; reparación de vehículos   de motor y motocicletas.                                                                     |
|     H          |     Transporte y almacenamiento.                                                                                                                                 |
|     I          |     Hostelería                                                                                                                                                   |
|     J          |     Información y comunicaciones.                                                                                                                                |
|     K          |     Actividades financieras y de seguros.                                                                                                                        |
|     L          |     Actividades inmobiliarias.                                                                                                                                   |
|     M          |     Actividades profesionales, científicas y técnicas.                                                                                                           |
|     N          |     Actividades administrativas y servicios auxiliares.                                                                                                          |
|     O          |     Administración Pública y defensa; Seguiridad Social   obligatoria.                                                                                           |
|     P          |     Educación.                                                                                                                                                   |
|     Q          |     Actividades sanitarias y de servicios sociales.                                                                                                              |
|     R          |     Actividades artísticas, recreativas y de entretenimiento.                                                                                                    |
|     S          |     Otros servicios.                                                                                                                                             |
|     T          |     Actividades de los hogares como empleadores de personal   doméstico; actividades de los hogares como productores de bienes y servicios   para uso propio.    |
|     U          |     Actividades de organizaciones y organismos extraterritoriales.                                                                                               |






&nbsp;

<p float="right" align="center">
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/gobEspana-logo.svg" alt="Logo Gobierno España" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/red-logo.svg" alt="Logo red.es" width="150"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ciudadesInteligentes-logo.svg" alt="Logo CiudadesInteligentes" width="150"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/unionEuropea-logo.svg" alt="Logo UnionEuropea" width="200"/>
</p>


<p float="right" align="center">
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntAcoruna-logo.svg" alt="Logo AyuntACoruña" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntMadrid-logo.svg" alt="Logo Madrid" width="100"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntSantiagoCompostela-logo.svg" alt="Logo Concello Santiago" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntZaragoza-logo.svg" alt="Logo Ayun.Zaragoza" width="200"/>
</p>



