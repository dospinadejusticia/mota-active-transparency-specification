# MOTA - Especificación de Transparencia Activa para Entidades Gubernamentales 0.1
Borrador de editores 29 Abril 2019

Esta versión:
    https://github.com/Dejusticia/mota-active-transparency-specification/
Latest published version:
    https://github.com/Dejusticia/mota-active-transparency-specification/
Latest editor's draft:
    https://github.com/Dejusticia/mota-active-transparency-specification/
Editors:
    Celso Bessa (Dejusticia)
    Maria Paula Ángel (Dejusticia)


## Abstract

Una especificación de los obligaciones y buenas prácticas para publicación e compartimento de información de transparencia gubernamental en Colombia.

Esta documento especifica los criterios, obligaciones legales, estándares y buenas prácticas para publicación e compartimento de información de transparencia en la web de forma más fácil y útil por parte de entidades gubernamentales en Colombia. También prové una visión general de los objectivos y filosofia de la iniciativa MOTA-Monitoreo de Obligaciones de Transparencia Activa-- que busca incentivar el cumplimiento de la rendición de cuentas en la lucha contra corrupción en Colombia, a saber: la transparencia de información en formatos abiertos, padronizados y fácilmente legibles por máquinas en los sitios web de sujetos obligados (información mínima obligatoria de los arts. 9, 10 y 11 de la Ley 1712 de 2014) y la claridad de los procesos de toma de decisiones que allí se exponen.

De hecho, esta especificación és utilizada por otros componentes de la inciativa, como el robot evaluador de sitios gubernamentales, que por su vez alimenta un banco de dados com los resultados de evalución y también el la webapp de evaluación de sitios web gubernamentales y también una biblioteca de insumos (ejemplos de códigos, patrones de diseño, modelos de textos, etc). Interdisciplinar -- abrangendo legislación, tecnologia, diseño, redacción, ciencia de información, entre otros --  esta especificación és construyda  sobre otras especifaciones, patrones, leys y otros conjuntos de buenas prácticas incluso, [HTML5](https://w3c.github.io/html/), [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/) [wai-aria-1.2](https://w3c.github.io/aria/), [schema.org](https://schema.org), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) y, como un contínuo trabajo en progreso, esta sujeta a cambios, aperfeiçoamentos y extensión. Aun que los principios y criterios principales estón bien definidos, critérios secundários, casos especiales y implementaciones especificas todavia non estón adecuadamente escritos o deben ser definidos en otros documentos.

NOTA: Este documento contiene un número grande de informaciónes introdutorias y contextuales. Tal vez quiera es posible que desee seguir directamente los criterios y ejemplos. Si desea contribuir, vea la sección Cómo Contribuir.

Palabras clave: Rendición de cuentas, Transparencia

## Estado y Tipologia del documento

Este documento segue la metodologia [Versionado Semántico (SEMVER)](https://semver.org/lang/es/) par controlo de versión. También utiliza los valores de la variable [specStatus](https://github.com/w3c/respec/wiki/specStatus) del la herramienta [ReSpec de W3C](https://github.com/w3c/respec/) para determinar el tipo/estado de la especificación.

En la fecha de publicación se encontra en la versión 0.1.0 y estado Borrador de Editores (ED - Editor's Draft).

Aún que esta especificación sea inspirada por lo trabajo de grupos como W3C, la iniciativa MOTA y sus organizadores non són afiliados a estas organizaciones.

- [MOTA - Especificación de Transparencia Activa para Entidades Gubernamentales 0.1](#mota---especificaci%C3%B3n-de-transparencia-activa-para-entidades-gubernamentales-01)
  - [Abstract](#abstract)
  - [Estado y Tipologia del documento](#estado-y-tipologia-del-documento)
  - [1. Introduccíon](#1-introducc%C3%ADon)
    - [1.4 Interdisciplinaridade](#14-interdisciplinaridade)
  - [2. Uso de la especificación](#2-uso-de-la-especificaci%C3%B3n)
  - [3. Conformidad](#3-conformidad)
  - [4. Termínos importantes (vocabulario)](#4-term%C3%ADnos-importantes-vocabulario)
  - [5. Categoria - Disponibilidad de Aceso](#5-categoria---disponibilidad-de-aceso)
    - [5.1 Existencia de Sítio Web](#51-existencia-de-s%C3%ADtio-web)
    - [5.2 Regimen de Aceso](#52-regimen-de-aceso)
        - [5.2.1.1. Critério de Suceso - Level AA](#5211-crit%C3%A9rio-de-suceso---level-aa)
        - [5.2.1.2. Critério de Suceso - Level AAA](#5212-crit%C3%A9rio-de-suceso---level-aaa)
      - [5.2.2 - Universalidad: Acesso Directo](#522---universalidad-acesso-directo)
        - [5.2.2.1. Critério de Suceso - Level A](#5221-crit%C3%A9rio-de-suceso---level-a)
        - [5.2.2.2. Critério de Suceso - Level AA](#5222-crit%C3%A9rio-de-suceso---level-aa)
        - [5.2.2.3. Critério de Suceso - Level AAA](#5223-crit%C3%A9rio-de-suceso---level-aaa)
      - [5.2.3 - Universalidad: Patrones de Acessibilidade y Web Standards](#523---universalidad-patrones-de-acessibilidade-y-web-standards)
        - [5.2.3.1. Critério de Suceso - Level A](#5231-crit%C3%A9rio-de-suceso---level-a)
        - [5.2.3.2. Critério de Suceso - Level AA](#5232-crit%C3%A9rio-de-suceso---level-aa)
        - [5.2.3.3. Critério de Suceso - Level AAA](#5233-crit%C3%A9rio-de-suceso---level-aaa)
      - [5.2.4 - Universalidad: Performance](#524---universalidad-performance)
        - [5.2.4.1. Critério de Suceso - Level A](#5241-crit%C3%A9rio-de-suceso---level-a)
          - [WebPagetest](#webpagetest)
          - [Pagespeed Insights](#pagespeed-insights)
        - [5.2.4.2. Critério de Suceso - Level AA](#5242-crit%C3%A9rio-de-suceso---level-aa)
          - [WebPagetest](#webpagetest-1)
          - [Pagespeed Insights](#pagespeed-insights-1)
        - [5.2.4.3. Critério de Suceso - Level AAA](#5243-crit%C3%A9rio-de-suceso---level-aaa)
          - [WebPagetest](#webpagetest-2)
          - [Pagespeed Insights](#pagespeed-insights-2)
      - [5.2.5 - Seguridad: Conexión Encriptada](#525---seguridad-conexi%C3%B3n-encriptada)
        - [5.2.5.1. Critério de Suceso - Level AA](#5251-crit%C3%A9rio-de-suceso---level-aa)
        - [5.2.5.2. Critério de Suceso - Level AAA](#5252-crit%C3%A9rio-de-suceso---level-aaa)
      - [5.2.6 - Dados Abiertos: Aceso via API REST](#526---dados-abiertos-aceso-via-api-rest)
        - [5.2.6.1. Critério de Suceso - Level AA](#5261-crit%C3%A9rio-de-suceso---level-aa)
        - [5.2.6.2. Critério de Suceso - Level AA](#5262-crit%C3%A9rio-de-suceso---level-aa)
        - [5.2.6.3. Critério de Suceso - Level AAA](#5263-crit%C3%A9rio-de-suceso---level-aaa)
  - [6. Información Mínima Obligatoria de Estructura](#6-informaci%C3%B3n-m%C3%ADnima-obligatoria-de-estructura)
    - [6.1. Estructura orgánica](#61-estructura-org%C3%A1nica)
    - [6.2. Funciones y deberes](#62-funciones-y-deberes)
    - [6.3. Ubicación de sus sedes y áreas](#63-ubicaci%C3%B3n-de-sus-sedes-y-%C3%A1reas)
    - [6.4. Divisiones o departamentos](#64-divisiones-o-departamentos)
    - [6.5. Horário de Atención al Público](#65-hor%C3%A1rio-de-atenci%C3%B3n-al-p%C3%BAblico)
    - [6.6. Presupuesto](#66-presupuesto)
    - [6.6. Ejecución Histórica Anual](#66-ejecuci%C3%B3n-hist%C3%B3rica-anual)
    - [6.7. Planes de gasto público por año fiscal](#67-planes-de-gasto-p%C3%BAblico-por-a%C3%B1o-fiscal)
    - [6.8. Directorio de funcionarios - Básico](#68-directorio-de-funcionarios---b%C3%A1sico)
    - [6.9. Directorio de funcionarios - Completo](#69-directorio-de-funcionarios---completo)
    - [6.10. Escalas salariales](#610-escalas-salariales)
    - [6.11. Sanciones aplicadas a servidores públicos](#611-sanciones-aplicadas-a-servidores-p%C3%BAblicos)
    - [6.12. Directório con Informaciones de Contratos com Contratistas - Básico](#612-direct%C3%B3rio-con-informaciones-de-contratos-com-contratistas---b%C3%A1sico)
    - [6.13. Directório con Informaciones de Contratos com Contratistas - Completo](#613-direct%C3%B3rio-con-informaciones-de-contratos-com-contratistas---completo)
    - [6.14. Normas generales](#614-normas-generales)
    - [6.14. Normas Reglamentárias](#614-normas-reglament%C3%A1rias)
    - [6.15. Manuales](#615-manuales)
    - [6.16. Metas y Objectivos](#616-metas-y-objectivos)
    - [6.17. Resultado de Auditorias](#617-resultado-de-auditorias)
    - [6.18. Indicadores de Desempeño](#618-indicadores-de-desempe%C3%B1o)
    - [6.19. Plan Anticorrupción y de Atención al Ciudadano](#619-plan-anticorrupci%C3%B3n-y-de-atenci%C3%B3n-al-ciudadano)
    - [6.20. Plan de Compras y Adquisición](#620-plan-de-compras-y-adquisici%C3%B3n)


## 1. Introduccíon

Esta sección no és normativa

Los objectivos de esta especificación incluen:
(a fazer)


### 1.1 Transparencia, Rendición de Cuentas y combate a corrupción
(a fazer)

### 1.2 Target Audience


(a fazer)

### 1.3 Filosofia y Presupuestos

### 1.4 Interdisciplinaridade

### 1.5 Regulamentación
(a fazer) lista de regulamentación (leys, reglamentos, etc), talvez con una breve análisis de la doutrina legal y/o algunos pontos importantes (e.g. jurisprudencia ambígua, etc)

### 1.6 Documentos de Apoyo

### 1.7 Collaboración

## 2. Uso de la especificación

This section is non-normative.

## 3. Conformidad

Además secciones marcadas cmo non-normativas, todos los diagramas, ejemplos y notas en esta especificación son non-normativas (exceto cuando marcadas en contrário). Todo el resto en esta especificación és normativo.

The key words MAY, MUST, MUST NOT, OPTIONAL, RECOMMENDED, REQUIRED, SHALL, SHALL NOT, SHOULD, and SHOULD NOT are to be interpreted as described in [RFC2119]. Además, clasificamos cada critérios como OBLIGACIÓN o RECOMENDACIÒN.

Para que una página web sea conforme con esta especificación, debe satisfacer todos y cada uno de los siguientes requisitos de conformidad:

1. Nivel de conformidad: Uno de los siguientes niveles de conformidad se satisface por completo.

    Nivel A: Para el nivel A de conformidad (el mínimo nivel de conformidad), el sítio web satisface todos los criterios de éxito de nivel A, o se proporciona una versión alternativa conforme.

    Nivel AA: Para el nivel AA de conformidad, el sítio web satisface todos los criterios de éxito de nivel A y AA, o se proporciona una versión alternativa conforme al nivel AA.

    Nivel AAA: Para el nivel AAA de conformidad, el sítio web satisface todos los criterios de éxito de nivel A, AA y AAA, o se proporciona una versión alternativa conforme al nivel AAA.

Nota 1: A pesar de que la conformidad sólo puede lograrse en los niveles indicados, se anima a los autores a notificar en sus declaraciones cualquier progreso que se realice para satisfacer los criterios de éxito de todo nivel más allá del nivel de conformidad alcanzado.

Nota 2: No se recomienda como política general exigir el nivel de conformidad AAA para sitios enteros porque no es posible que algunos contenidos puedan satisfacer todos los criterios de éxito de nivel AAA.

### 3.1 Conformidad de Dependencias

(a fazer) como se define conformidad de otras especificaciones, técnicas, etc?

### 3.4 Conformance Checkers
(a fazer)

## 4. Termínos importantes (vocabulario)

(a fazer)


## 5. Categoria - Disponibilidad de Aceso

(afazer: intro corta)

### 5.1 Existencia de Sítio Web
Tipo: OBLIGACIÓN

La entidade deberá mantener um sítio web, que deberá estar disponible para acesso via una URI oficial por cualquier user-agent.

#### 5.1.1. Disponibilidad

El sitio está disponible para acesso via una URI oficial por cualquier user-agent.

#### 5.1.1.1 Critério de Suceso - Level AAA

El sítio retorna páginas com códigos HTTP 200 o 314 en su URI oficial, cuando acesado por cualquier user-agent.

### 5.2 Regimen de Aceso
Tipo: MEZCLADO

(afazer: intro)

#### 5.2.1. Gratuidad
Tipo: OBLIGACIÓN

El sítio debe tener aceso gratuidad a los servicios judiciales informáticos que presta la Corte, exceto para casos previstos en ley e reglamentos.

##### 5.2.1.1. Critério de Suceso - Level AA

Algunos servicios solo son acesibles por contraseña o otro identificador obtidos a partir de botones y/o otros métodos de pago detectados en el sitio.

##### 5.2.1.2. Critério de Suceso - Level AAA

Todos los servicios son acesibles sin contrapartida financeira y botones o otros metodos de pagos no son detectados en el sítio.

#### 5.2.2 - Universalidad: Acesso Directo
Tipo: RECOMENDACIÓN

Los servicios informáticos que presta la Corte deben ser abiertos a todo el público que desee acceder a ellos y no deben estar restringidos a ciertos usuarios previo registro y recepción de una clave de acceso.

##### 5.2.2.1. Critério de Suceso - Level A

Registro y clave de acesso son necesários para aceder parte del sitio SIN una buena justificativa (e.g. privacidad de datos personaldes o seguridad)

##### 5.2.2.2. Critério de Suceso - Level AA

Registro y clave de acesso son necesários para aceder parte del sitio CON una buena justificativa (e.g. privacidad de datos personaldes o seguridad)

##### 5.2.2.3. Critério de Suceso - Level AAA

Todos los servicios son acesibles sin registro prévio y clave de aceso.

#### 5.2.3 - Universalidad: Patrones de Acessibilidade y Web Standards
Tipo: RECOMENDACIÓN

Los sitios deben permitir acesso igualitário por:

   1) tecnologias asistivas como lectores de tela, asistentes por voz, etc;
   2) aceso sin uso de javascript or plugins de terceros;
   3) aceso por dispositivos variados como computadores, teléfonos smartphones, asistentes por voz (e.g. Amazon Alexa), SmartTVs y otros dispositivos;
   4) aceso en condiciones variadas de conexiones (broadband y 2G/3G de baja performance), para isto deben seguir principios y diretrizes de acesibilidade conforme definidos pela recomendación WCAG2.1 y WAI-ARIA de W3C para y seguindo las mejores prácticas determinadas en The Web Standards projects para markup sin considerar metadatos o attributos semanticos (i.e. elementos HTML semanticos, sin considerar schema.org o RDF markup);

##### 5.2.3.1. Critério de Suceso - Level A

El sítio web és valido sin errores en el  https://validator.w3.org seguindo la specificación HTML5 y utilizando los elementos de la specificación de forma semántica. És decir, utilización correcta de elementos HTML de acuerda a su función (e.g. H1 para cabecera más importante o título, UL para lista de elementos, etc)

[HTML5](https://w3c.github.io/html/), [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/) [wai-aria-1.2](https://w3c.github.io/aria/), [schema.org](https://schema.org), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD)****

##### 5.2.3.2. Critério de Suceso - Level AA

El sítio web és valido sin errores en https://validator.w3.org seguindo la specificación HTML5 y utilizando los elementos de la specificación de forma semántica. És decir, utilización correcta de elementos HTML de acuerda a su función (e.g. H1 para cabecera más importante o título, UL para lista de elementos, etc);

El sítio cumple com los criterios A y AA de WCAG 2.1 (e.g. https://fae.disability.illinois.edu );

##### 5.2.3.3. Critério de Suceso - Level AAA

El sítio web és valido sin errores en https://validator.w3.org seguindo la specificación HTML5 y utilizando los elementos de la specificación de forma semántica. És decir, utilización correcta de elementos HTML de acuerda a su función (e.g. H1 para cabecera más importante o título, UL para lista de elementos, etc);

El sítio cumple com los criterios A y AA de WCAG 2.1 (e.g. https://fae.disability.illinois.edu );

El sítio utiliza de forma adequada las prácticas WAI-ARIA;

#### 5.2.4 - Universalidad: Performance
Tipo: RECOMENDACIÓN

Los sitios deben permitir acesso con velocidade rasonable y estable mismo em malas condiciones de aceso, como conexión por dispositivos móbiles en reds de baja performance. Los sitios deben obtener grados máximos, de acuerdo con los criterios bajo, en dos herramientas de evaluación de performance reconecidas por su qualidade: [Webpagetest](http://webpagetest.org/result/190506_KG_29de3021baf30242013b8f58843cd7df/) y Pagespeed Insights.

En Webpagetest, los test son efectuados con la seguinte configuración:
    - Test Location: Android Devices - Dulles, VA, Moto G (gen 4);
    - Browser: Moto G4 - Chrome;
    - Connection: 3G (1.6 Mbps/768 Kbps RTT)
    - Number of Tests to Run: 9;
    - Repeat View: First View and Repeat View;
    - Capture Video: marcado
    - Ignore SSL Certificate Errors: marcado

##### 5.2.4.1. Critério de Suceso - Level A

Los sitios deben obtener los seguintes grados máximos:

###### WebPagetest
    - Time to First Byte: 3.500s
    - First Interactive (beta): 10.000s
    - Speed Index: 11.000s
    - Bytes in: 2.048kb
    - Cost: $$$

###### Pagespeed Insights
    - Ordenador: 70
    - Móvil: 50

##### 5.2.4.2. Critério de Suceso - Level AA

Los sitios deben obtener los seguintes grados máximos:

###### WebPagetest
    - Time to First Byte: 3.000s
    - First Interactive (beta): 8.000s
    - Speed Index: 7.000s
    - Bytes in: 1.536kb
    - Cost: $$$

###### Pagespeed Insights
    - Ordenador: 85
    - Móvil: 60

##### 5.2.4.3. Critério de Suceso - Level AAA

Los sitios deben obtener los seguintes grados máximos:

###### WebPagetest
    - Time to First Byte: 2.500s
    - First Interactive (beta): 6.000s
    - Speed Index: 5.000s
    - Bytes in: 1.024kb
    - Cost: $$

###### Pagespeed Insights
    - Ordenador: 95
    - Móvil: 75

#### 5.2.5 - Seguridad: Conexión Encriptada
Tipo: RECOMENDACIÓN

El sítio és acessible en conexión encriptada (SSL/TLS).

##### 5.2.5.1. Critério de Suceso - Level AA

El sítio és acessible en conexión encriptada (SSL/TLS) opcional.

##### 5.2.5.2. Critério de Suceso - Level AAA

El sítio és acessible en conexión encriptada (SSL/TLS) y solamente por conexión criptograda.

#### 5.2.6 - Dados Abiertos: Aceso via API REST
Tipo: RECOMENDACIÓN

Los contenidos del sitio son acesibles por una API REST con datos estructurados, incluso meta-dados.

##### 5.2.6.1. Critério de Suceso - Level AA

API REST disponible, pero sin meta-datos.

##### 5.2.6.2. Critério de Suceso - Level AA

API REST disponible, CON meta-datos.

##### 5.2.6.3. Critério de Suceso - Level AAA

API REST disponible, CON meta-datos e en formato JSON.

## 6. Información Mínima Obligatoria de Estructura
(afazer: intro)

Informaciónes sobre la estructura, acuerdo artículo 9 de la ley _______ de _____.

### 6.1. Estructura orgánica
Tipo: OBLIGACIÓN

Descripción de la forma en que se compone y se organiza la entidade y no tan sólo la cabeza o principal órgano que se trate.

#### 6.1.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) o disponibles en lá página en formato de imagen. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.1.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.1.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org o motaSchema. Acesible por elemento de navegación principal o en el corpo de la capa de seción.

Referencias:

  - https://schema.org/Organization
  - https://schema.org/GovernmentOrganization
  - https://schema.org/GovernmentOffice
  - [(https://schema.org/department)]
  - https://schema.org/employee
  - Considerar criação de schemas de identificadores como NIT, CC, CE, etc. e.g. https://schema.org/naics
  - Considerar vocabulário específicos como https://schema.org/duns ou http://www.heppnetz.de/projects/goodrelations/
  - https://schema.org/contactPoint
  - https://schema.org/OrganizationRole

### 6.2. Funciones y deberes
Tipo: OBLIGACIÓN

Descripción de funciones y deberes entidade en general y no tan sólo la cabeza o principal órgano que se trate.

#### 6.2.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) o disponibles en lá página en formato de imagen. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.2.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.2.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org o motaSchema. Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.3. Ubicación de sus sedes y áreas
Tipo: OBLIGACIÓN

Descripción de ubicación de sedes y áreas de la entidade en general y no tan sólo la cabeza o principal órgano que se trate.

#### 6.3.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) o disponibles en lá página en formato de imagen. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.3.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML5. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.3.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org o motaSchema. Acesible por elemento de navegación principal o en el corpo de la capa de seción.

Referencias:

  - https://schema.org/GovernmentOffice
  - https://schema.org/GovernmentBuilding

### 6.4. Divisiones o departamentos
Tipo: OBLIGACIÓN

Informaciones sobre la totalidad de divisiones territoriales. Para considerar como positiva esta pauta, basta que la información sea general (indicación de cuales son, direcciones, etc.) y no es necesario que todo el contenido del sitio sea el mismo para todas las divisiones territoriales.

#### 6.4.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) o disponibles en lá página en formato de imagen. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.4.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.4.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org o motaSchema. Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.5. Horário de Atención al Público
Tipo: OBLIGACIÓN

Informaciones sobre horários de atencíon al público de la entidade y sus divisiones en diferentes médios: en la sede, teléfono, correo eletronico, etc

#### 6.5.1. Critério de Suceso - Level A

Texto disponible en página específica, acesible por elemento de navegación principal o en el corpo de la capa de seción, inclue horarios de atención de diferenes departamentos o sedes.

#### 6.5.2. Critério de Suceso - Level AA

Texto disponible en página específica, acesible por elemento de navegación principal o en el corpo de la capa de seción, inclue horarios de atención de diferenes departamentos o sedes. Horários más importante de la sede o servicio principal también disponible en pié de página de todas las páginas.

#### 6.5.3. Critério de Suceso - Level AAA

Texto disponible en página específica, inclue horarios de atención de diferenes departamentos o sedes. Horários más importante de la sede o servicio principal también disponible en pié de página de todas las páginas. En los dos casos, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org o motaSchema.

### 6.6. Presupuesto
Tipo: OBLIGACIÓN

El presupuesto en ejercicio de la entidad para la respectiva vigencia debe estar disponible para verificación del público. Puede ser el presupuesto inicial o final. Lo presupuesto debe ofrecer datos (gastos, valores, ingresos, gastos) de forma clara, organizada y se encuentrar desagregado conforme descrito a seguir, con cabeceras ou títulos seguindos nomes patrones en paréntesis:

- ingresos presupuestarios (Ingresos);
- gastos de personal (Gastos con);
- bienes y servicios de consumo;
- adquisición de activos no financieros;
- edificios, mobiliarios y otros;
- equipos informáticos;
- programas informáticos;
- actualizado hasta el último trimestre concluido;

En lo banco de patrones MOTA, presentamos un modelo de archivo Dados Presupuestais, que cumpre con los requisitos e buenas prácticas mencionadas.

#### 6.6.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) o disponibles en lá página en formato de imagen. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.6.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción. Lo archivo sigue el patrón del modelo de archivo Dados Presupuestais en lo banco de patrones MOTA.

#### 6.6.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.6. Ejecución Histórica Anual
Tipo: OBLIGACIÓN

El sitio web contiene contiene información relativa al presupuesto ejecutado en el año en curso, que muestren cómo se está llevando a cabo la ejecución del presupuesto en la respectiva vigencia. Los datos pueden ser agregados mensualmente o trimestralmente, idealmente con porcentajes de ejecución, y deben ofrecer datos (gastos, valores, ingresos, gastos) de forma clara, organizada y se encuentrar desagregado conforme descrito a seguir, con cabeceras ou títulos seguindos nomes patrones en paréntesis:

- ingresos presupuestarios (Ingresos);
- gastos de personal (Gastos con);
- bienes y servicios de consumo;
- adquisición de activos no financieros;
- edificios, mobiliarios y otros;
- equipos informáticos;
- programas informáticos;
- actualizado hasta el último trimestre concluido;

En lo banco de patrones MOTA, presentamos modelos de archivo Ejecución Presupuestal Mensual y Ejecución Presupuestal Trimestral, que cumpren con los requisitos e buenas prácticas mencionadas.

#### 6.6.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) o disponibles en lá página en formato de imagen. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.6.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción. Lo archivo sigue el patrón de los modelos de archivo Ejecución Presupuestal Mensual y Ejecución Presupuestal Trimestral en lo banco de patrones MOTA.

#### 6.6.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org o motaSchema. Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.7. Planes de gasto público por año fiscal
Tipo: OBLIGACIÓN

AFAZER

En lo banco de patrones MOTA, presentamos modelos de archivo ____________________, que cumpren con los requisitos e buenas prácticas mencionadas.

#### 6.7.1. Critério de Suceso - Level A

AFAZER

#### 6.7.2. Critério de Suceso - Level AA

AFAZER

#### 6.7.3. Critério de Suceso - Level AAA

AFAZER


### 6.8. Directorio de funcionarios - Básico
Tipo: OBLIGACIÓN

El sitio web contiene contiene un directório de funcionarios com sus informaciones basicas:

- nombres y apellidos;
- direcciones de correo;
- teléfono del despacho y dependencia.

#### 6.8.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf) . Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.8.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.8.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.9. Directorio de funcionarios - Completo
Tipo: OBLIGACIÓN

El sitio web contiene contiene un directório de funcionarios com sus informaciones completas.

- nombres y apellidos;
- direcciones de correo;
- teléfono del despacho y dependencia.
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades)
- Experiencia laboral y profesional
  - Nombres específicos de empleadores previos
  - Cargos anteriores
  - Fecha inicio y fecha fin en cada cargo
- Sanciones aplicadas a servidores públicos

 Alternativamente, enlace al SIGEP és válido, pero solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones.

#### 6.9.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción; alternativamente, enlace al SIGEP és válido solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones.

#### 6.9.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.9.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.10. Escalas salariales
Tipo: OBLIGACIÓN

Es posible encontrar tabla com rangos de salarios de la entidade, identificado por el título "Rangos de salario por nivel", y el decreto de asignaciones salariales de la entidad en un lugar visible. Un enlace al SIGEP és válido, pero solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones.

La tabla debe ser actualizada con al menos al último año concluido y contiene información sobre el salario base por jerarquía y/o categoría ocupacional, en acuerdo com la categoria, tipo y otras especificidades de la entidade. Ejemplo, en el sitio de la Fiscal General de La Nácion Contiene, se espera encontrar datos separados por jerarquía y/o categoría de fiscales y también por jerarquía y/o categoría ocupacional de otros funcionarios no fiscales.

#### 6.10.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción; alternativamente, un enlace al SIGEP és válido, pero solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las

#### 6.10.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.10.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.11. Sanciones aplicadas a servidores públicos
Tipo: OBLIGACIÓN

Es posible encontrar informaciones sobre sanciones disciplinarias o de otro tipo que hayan sido impuestas  a funcionários de la entidade. Hay estadísticas sobre las sanciones impuestas, actualizadas hasta el último año concludio y se encuentran desagregadas según el tipo de funcionarios. e.g. en el sitio de la Fiscal General de La Nácion Contiene, las informaciones deben esta desagregadas entre fiscales y no-fiscales.

#### 6.11.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.11.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.11.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquemas [Report](https://schema.org/Report), [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.12. Directório con Informaciones de Contratos com Contratistas - Básico
Tipo: OBLIGACIÓN

Es posible encontrar informaciones sobre los contratos con contratistas en formatos abertos. Alternativamente, un enlace al SIGEP és válido, pero solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones.

- nombres y apellidos;
- direcciones de correo;
- teléfono del despacho y dependencia;
- objeto del contrato.

#### 6.12.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción; alternativamente, un enlace al SIGEP és válido, pero solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones

#### 6.12.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.12.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.13. Directório con Informaciones de Contratos com Contratistas - Completo
Tipo: OBLIGACIÓN

El sitio web contiene contiene un directório de funcionarios com sus informaciones completas.

- nombres y apellidos;
- direcciones de correo;
- teléfono del despacho y dependencia.
- objeto del contrato
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades).
  - Por formación académica se entiende, al menos, el grado académico que ostenta, la profesión que tiene y la institución académica por la que fue otorgada.
- Experiencia laboral y profesional. Por experiencia laboral, se entiende, al menos, aquella vinculada a la profesión que tiene, o el evento de que no aparezca su profesión, las actividades laborales relacionadas con el cargo, área o institución en la que se desempeña.
  - Nombres específicos de empleadores previos
  - Cargos anteriores
  - Fecha inicio y fecha fin en cada cargo
- Sanciones aplicadas a servidores públicos

 Alternativamente, enlace al SIGEP és válido, pero solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones

#### 6.13.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción; alternativamente, enlace al SIGEP és válido solo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlance, se abre directamente la tabla com las informaciones.

#### 6.13.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.13.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.

### 6.14. Normas generales
Tipo: OBLIGACIÓN

Existencia de una sección con normas y reglamentos pertinentes para la entidad: decretos, circulares, leyes, etc relativas a creacción e reglamentos de la entidad. El documento MOTA - Reglas Contextuales especifica normas necesárias por entidades, o classes de entidades. Dos versiones deberán estar disponibles:

- resumen en lenguage sencilla, destacando trechos de reglamentos pertinentes;
- copias verbatim de las normas.
  - en casos de documentos largos y cuyo escopo exceda el tema de Normas generales, és permitido copias verbatim de apenas los trechos pertinentes, pero és necessário un enlace para um archivo o recurso com el documento integral.

#### 6.14.1. Critério de Suceso - Level A

Resumen disponible en la página, em HTML. Con normas disponibles para bajar en formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.14.2. Critério de Suceso - Level AA

Resumen disponible en la página, em HTML, en lenguage sencilla, con normas completas disponibles también en HTML en la mesma página o en otra página en el mesmo sítio. Para las normas completas, archivos em formatos abertos (e.g. odf) acessibles en el mesmo sitio y dominio és válido. Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.14.3. Critério de Suceso - Level AAA

Resumen disponible en la página, em HTML, en lenguage sencilla, con normas completas disponibles también en HTML en la mesma página o otra página en el mesmo sítio. En los dos casos, el contenido és estruturado semanticamente (i.e. elementos HTML5 apropriados) y sus meta-datos disponibles en formato LD+JSON y vocabulario schema.org segundo esquema [legislation](https://schema.org/Legislation) y [LegislationObject](https://schema.org/LegislationObject) y . Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.14. Normas Reglamentárias
Tipo: OBLIGACIÓN

Existencia de informaciones de normas reglamentárias pertinentes a la entidad: resoluciones y directivas. El documento MOTA - Reglas Contextuales especifica normas necesárias por entidades, o classes de entidades. Dos versiones deberán estar disponibles:

- resumen en lenguage sencilla, destacando trechos de reglamentos pertinentes;
- copias verbatim de las normas.
  - en casos de documentos largos y cuyo escopo exceda el tema de Normas generales, és permitido copias verbatim de apenas los trechos pertinentes, pero és necessário un enlace para um archivo o recurso com el documento integral.

#### 6.14.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.14.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.14.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.15. Manuales
Tipo: OBLIGACIÓN

(afazer)

#### 6.15.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.15.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.15.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.16. Metas y Objectivos
Tipo: OBLIGACIÓN

(afazer) (video plan de acion de fiscalia)

#### 6.16.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.16.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.16.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.17. Resultado de Auditorias
Tipo: OBLIGACIÓN

(afazer)
#### 6.17.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.17.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.17.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.18. Indicadores de Desempeño
Tipo: OBLIGACIÓN

Las entidades deben proveer informacions sobre los indicadores de desempeño que utilizam y reportes com estadísticas y análisis del desempeño de la entidade (em relación a _________) y de sus funcionarios. Para entidades nacionales, deben contener informacion a nivel nacional y territorial. El documento MOTA - Reglas Contextuales especifica normas necesárias por entidades, o classes de entidades.

#### 6.18.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.18.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.18.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.19. Plan Anticorrupción y de Atención al Ciudadano
Tipo: OBLIGACIÓN

(afazer)

#### 6.19.1. Critério de Suceso - Level A

Datos disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf). Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.19.2. Critério de Suceso - Level AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.19.3. Critério de Suceso - Level AAA

Texto disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados) y disponible como meta-datos en formato LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.


### 6.20. Plan de Compras y Adquisición
Tipo: OBLIGACIÓN

La entidad debe ofrecer informaciones de su Plan de Compras Anual. El documento MOTA - Reglas Contextuales especifica normas necesárias por entidades, o classes de entidades. El plan debe compreender:

- Processo de Gestíon Contractual / Procedimento Plan Anual de Adquisiciones
- Contrataciones adjudicadas para la correspondiente vigencia, incluso funcionamiento e inversión, obras públicas, bienes adquiridos y arrendados, estudios o investigaciones.
- Plazos de cumplimiento de los contratos
- Contrataciones en curso

NOTA: Todos los contratos e ítens debem contener enlace a SECOP

En caso de entidades con multiplas divisiones (e.g. secciones territoriales), debe-se utilizar de un archivo o una página web para cada división

#### 6.20.1. Critério de Suceso - Level A

Informaciones disponibles en archivos, formatos proprietários (e.g. .docx, xlsx, pdf), con links para SECOP. Acesible por elemento de navegación secundário o en el corpo de la capa de seción;

#### 6.20.2. Critério de Suceso - Level AA

Processo de Gestíon Contractual disponible en lá página, estruturado semanticamente (i.e. elementos HTML5 apropriados), informaciones de contratos disponibles en archivos, formatos abiertos (e.g. .odf), con links para SECOP. Acesible por elemento de navegación secundário o en el corpo de la capa de seción.

#### 6.20.3. Critério de Suceso - Level AAA
Processo de Gestíon Contractual y lista de documentos disponibles en lá página, estruturados semanticamentes (i.e. elementos HTML5 apropriados), informaciones de contratos disponibles en archivos, en formatos abiertos (e.g. .odf), contendo links para SECOP. Meta-dados de la collecion de  documentos contenend nombre del docmento, author, data de actualizacion, URI e enlance para SECOP) en formato LD+JSON y vocabulario schema.org segundo esquema [Collection](https://schema.org/Collection), [DigitalDocument](https://schema.org/DigitalDocument) y relacionados. Acesible por elemento de navegación principal o en el corpo de la capa de seción.
