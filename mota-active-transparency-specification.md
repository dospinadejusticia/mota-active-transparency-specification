# MOTA - Especificación de transparencia activa para entidades gubernamentales 0.5.1
Borrador de editores 07 de julio de 2020

Esta versión:
- https://github.com/Dejusticia/mota-active-transparency-specification/

Latest published version:
- https://github.com/Dejusticia/mota-active-transparency-specification/

Latest editor's draft:
- https://github.com/Dejusticia/mota-active-transparency-specification/

Editores:

- Celso Bessa (Dejusticia)
- Maria Paula Ángel Arango (Dejusticia)
- Daniel Ospina Celis (Dejusticia)
- Juan Carlos Upegui (Dejusticia)

## Abstract

Este documento especifica los criterios de evaluación de obligaciones y de buenas prácticas para la publicación y divulgación de la información pública en Internet por parte de entidades gubernamentales en Colombia (obligaciones de transparencia activa según la Ley 1712 de 2014).

Su principal y primer objetivo es servir de foro para reunir a las partes interesadas en la transparencia activa en Colombia, al habilitar un proceso público, participativo y recurrente de estandarización de las obligaciones y de las buenas prácticas sobre publicación y divulgación de información pública en Internet. Esto con el propósito de que la transparencia activa desplegada por las entidades gubernamentales en Colombia sea lo más completa y eficiente posible.

Por estas razones, aunque esta especificación es originalmente un proyecto creado por el Centro de Estudios de Derecho, Sociedad y Justicia - Dejusticia, la intención es que las organizaciones públicas y privadas, académicos y ciudadanos en general se apropien y participen en su desarrollo.

Esta especificación es, por lo tanto, también un llamado a la construcción colectiva de la política y la práctica y evaluación de la transparencia activa gubernamental en Colombia.

Cabe destacar que en Colombia ya existen varios instrumentos e iniciativas de transparencia y datos abiertos muy buenas. La iniciativa MOTA no reemplaza estas iniciativas, busca sumarse a ellas y complementarlas. Además, busca ser un punto de encuentro para el debate y la actualización de la forma de caracterizar las obligaciones de transparencia activa y sobre todo de medir su concreción. Esto, ante el hecho innegable de que la tecnología y la sociedad están en constante transformación.

El segundo objetivo es ofrecer una visión general de los objetivos y de la filosofía de la iniciativa MOTA--Monitoreo de Obligaciones de Transparencia Activa--.  La iniciativa MOTA busca incentivar el cumplimiento de las obligaciones de transparencia activa de las entidades gubernamentales, con la esperanza de que esto redunde en una mejor rendición de cuentas de las entidades gubernamentales, y sirva como una herramienta más en la lucha contra corrupción.  Esto, a través de incentivar ejercicios de transparencia activa de la información en formatos abiertos, estandarizados y fácilmente legibles por máquinas en los sitios web de los sujetos obligados (información mínima obligatoria de los arts. 9, 10 y 11 de la Ley 1712 de 2014).

El tercero objetivo es reunir y explicar de forma aterrizada y práctica, en un solo documento, las obligaciones legales, estándares, metodologíaas y buenas prácticas en materia de transparencia activa de las entidades gubernamentales, que suelen estar dispersas en diversas fuentes.

Al mismo tiempo, busca permitir que los desarrolladores web de las entidades públicas puedan encontrar facilmente la información, estándares y referencias necesarias para la ejecución del noble trabajo de informar a la ciudadanía.

Es de destacar que esta especificación es utilizada por otros componentes de la iniciativa, como el robot evaluador de sitios gubernamentales, que a su vez alimenta una base de datos con los resultados de evaluación, la webapp de evaluación de sitios web gubernamentales y una biblioteca de insumos (ejemplos de códigos, patrones de diseño, modelos de textos, etc).

También resaltamos el carácter interdisciplinar de la especificación, en tanto la misma comprende aproximaciones desde las ciencias del derecho, de la ingeniería, del diseño y de la información, entre otros.

Esta especificación ha sido construida sobre otras especificaciones, patrones, leyes y otros conjuntos de buenas prácticas incluso, resolución [HTML5](https://w3c.github.io/html/), [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), [wai-aria-1.2](https://w3c.github.io/aria/), [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/), [schema.org](https://schema.org), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD).


Entendida como un continuo trabajo en progreso está sujeta a cambios, mejoras, adiciones y extensiones.  Aunque los principios y criterios primarios están bien definidos, los criterios secundarios, los casos especiales y las implementaciones específicas todavía tal vez no están adecuadamente escritos o deban ser definidos en otros documentos.

Palabras clave: Transparencia activa, rendición de cuentas

## Estado y tipología del documento

Este documento sigue la metodología [Versionado Semántico (SEMVER)](https://semver.org/lang/es/) para control de versión. También utiliza los valores de la variable [specStatus](https://github.com/w3c/respec/wiki/specStatus) de la herramienta [ReSpec de W3C](https://github.com/w3c/respec/) de W3C para determinar el tipo/estado de la especificación.

En la fecha de publicación se encontrará en la versión 0.4.0 y estado Borrador de Editores (ED - Editor's Draft).

Aunque esta especificación fue inspirada por el trabajo de grupos como W3C, la iniciativa MOTA y sus organizadores no son ni están afiliados a estas organizaciones.

## Tabla de contenido

- [MOTA - Especificación de transparencia activa para entidades gubernamentales 0.5.1](#mota---especificación-de-transparencia-activa-para-entidades-gubernamentales-051)
  - [Abstract](#abstract)
  - [Estado y tipología del documento](#estado-y-tipología-del-documento)
  - [Tabla de contenido](#tabla-de-contenido)
  - [1. Introducción](#1-introducción)
    - [1.1 Transparencia, Rendición de Cuentas y lucha contra la corrupción](#11-transparencia-rendición-de-cuentas-y-lucha-contra-la-corrupción)
    - [1.2 Público objetivo](#12-público-objetivo)
    - [1.3 Filosofía y Presupuestos](#13-filosofía-y-presupuestos)
    - [1.4 Interdisciplinaridad](#14-interdisciplinaridad)
    - [1.5 Regulación](#15-regulación)
    - [1.6 Documentos de Apoyo](#16-documentos-de-apoyo)
    - [1.7 Colaboración](#17-colaboración)
  - [2. Uso de la especificación](#2-uso-de-la-especificación)
  - [3. Conformidad y Categorias de Éxito](#3-conformidad-y-categorias-de-éxito)
    - [3.1 Conformidad](#31-conformidad)
    - [3.2. OBLIGACIÓN y RECOMENDACIÓN](#32-obligación-y-recomendación)
    - [3.4 - Escala de Puntos: diretrices de disponibilidad de información](#34---escala-de-puntos-diretrices-de-disponibilidad-de-información)
      - [Nivel A: Información disponible en archivo](#nivel-a-información-disponible-en-archivo)
      - [Nivel AA: Información disponible para personas disponibles en la misma página](#nivel-aa-información-disponible-para-personas-disponibles-en-la-misma-página)
      - [Nível AAA: Información disponible como meta-datos estructurados legible por máquina](#nível-aaa-información-disponible-como-meta-datos-estructurados-legible-por-máquina)
        - [Observaciones sobre Criterios de Éxito](#observaciones-sobre-criterios-de-éxito)
    - [3.1 Herramientas para examen de conformidad](#31-herramientas-para-examen-de-conformidad)
      - [WCAG2.1 y Acessibilidad](#wcag21-y-acessibilidad)
  - [4. Términos importantes (vocabulario)](#4-términos-importantes-vocabulario)
  - [5. Categoría - Disponibilidad de Acceso](#5-categoría---disponibilidad-de-acceso)
    - [5.1 Existencia de sitio web](#51-existencia-de-sitio-web)
      - [5.1.1 Criterio de Éxito - Nivel AAA](#511-criterio-de-éxito---nivel-aaa)
    - [5.2 Gratuidad](#52-gratuidad)
      - [5.2.1. Criterio de Éxito - Nivel AA](#521-criterio-de-éxito---nivel-aa)
      - [5.2.2. Criterio de Éxito - Nivel AAA](#522-criterio-de-éxito---nivel-aaa)
    - [5.3. - Universalidad: Acceso directo](#53---universalidad-acceso-directo)
      - [5.3.1. Criterio de Éxito - Nivel A](#531-criterio-de-éxito---nivel-a)
      - [5.3.2. Criterio de Éxito - Nivel AA](#532-criterio-de-éxito---nivel-aa)
      - [5.3.3. Criterio de Éxito - Nivel AAA](#533-criterio-de-éxito---nivel-aaa)
    - [5.4 - Universalidad: Patrones de accesibilidad y web standards](#54---universalidad-patrones-de-accesibilidad-y-web-standards)
      - [5.4.1. Criterio de Éxito - Nivel A](#541-criterio-de-éxito---nivel-a)
      - [5.4.2. Criterio de Éxito - Nivel AA](#542-criterio-de-éxito---nivel-aa)
      - [5.4.3. Criterio de Éxito - Nivel AAA](#543-criterio-de-éxito---nivel-aaa)
    - [5.5 - Universalidad: Rendimiento](#55---universalidad-rendimiento)
      - [5.5.1. Criterio de Éxito - Nivel A](#551-criterio-de-éxito---nivel-a)
        - [WebPagetest](#webpagetest)
        - [Pagespeed Insights](#pagespeed-insights)
      - [5.5.2. Criterio de Éxito - Nivel AA](#552-criterio-de-éxito---nivel-aa)
        - [WebPagetest](#webpagetest-1)
        - [Pagespeed Insights](#pagespeed-insights-1)
      - [5.5.3. Criterio de Éxito - Nivel AAA](#553-criterio-de-éxito---nivel-aaa)
        - [WebPagetest](#webpagetest-2)
        - [Pagespeed Insights](#pagespeed-insights-2)
    - [5.6 - Seguridad: Conexión encriptada](#56---seguridad-conexión-encriptada)
      - [5.6.1. Criterio de Éxito - Nivel A](#561-criterio-de-éxito---nivel-a)
      - [5.6.2. Criterio de Éxito - Nivel AA](#562-criterio-de-éxito---nivel-aa)
      - [5.6.3. Criterio de Éxito - Nivel AAA](#563-criterio-de-éxito---nivel-aaa)
    - [5.7 - Dados Abiertos: Acceso vía API REST](#57---dados-abiertos-acceso-vía-api-rest)
      - [5.7.1. Criterio de Éxito - Nivel AA](#571-criterio-de-éxito---nivel-aa)
      - [5.7.2. Criterio de Éxito - Nivel AA](#572-criterio-de-éxito---nivel-aa)
      - [5.7.3. Criterio de Éxito - Nivel AAA](#573-criterio-de-éxito---nivel-aaa)
  - [6. Información Mínima Obligatoria sobre la Estructura](#6-información-mínima-obligatoria-sobre-la-estructura)
    - [6.1. Estructura orgánica / Organigrama](#61-estructura-orgánica--organigrama)
      - [6.1.1. Criterio de Éxito - Nivel A (datos)](#611-criterio-de-éxito---nivel-a-datos)
      - [6.1.2. Criterio de Éxito - Nivel AA](#612-criterio-de-éxito---nivel-aa)
      - [6.1.3. Criterio de Éxito - Nivel AAA](#613-criterio-de-éxito---nivel-aaa)
    - [6.2. Funciones y deberes](#62-funciones-y-deberes)
      - [6.2.1. Criterio de Éxito - Nivel A](#621-criterio-de-éxito---nivel-a)
      - [6.2.2. Criterio de Éxito - Nivel AA](#622-criterio-de-éxito---nivel-aa)
      - [6.2.3. Criterio de Éxito - Nivel AAA](#623-criterio-de-éxito---nivel-aaa)
    - [6.3. Ubicación de sus sedes y áreas, divisiones o departamentos / Localización física, sucursales o regionales](#63-ubicación-de-sus-sedes-y-áreas-divisiones-o-departamentos--localización-física-sucursales-o-regionales)
      - [6.3.1. Criterio de Éxito - Nivel A](#631-criterio-de-éxito---nivel-a)
      - [6.3.2. Criterio de Éxito - Nivel AA](#632-criterio-de-éxito---nivel-aa)
      - [6.3.3. Criterio de Éxito - Nivel AAA](#633-criterio-de-éxito---nivel-aaa)
    - [6.4. Divisiones o departamentos](#64-divisiones-o-departamentos)
      - [6.4.1. Criterio de Éxito - Nivel A](#641-criterio-de-éxito---nivel-a)
      - [6.4.2. Criterio de Éxito - Nivel AA](#642-criterio-de-éxito---nivel-aa)
      - [6.4.3. Criterio de Éxito - Nivel AAA](#643-criterio-de-éxito---nivel-aaa)
    - [6.5. Horario de atención al público](#65-horario-de-atención-al-público)
      - [6.5.1. Criterio de Éxito - Nivel A](#651-criterio-de-éxito---nivel-a)
      - [6.5.2. Criterio de Éxito - Nivel AA](#652-criterio-de-éxito---nivel-aa)
      - [6.5.3. Criterio de Éxito - Nivel AAA](#653-criterio-de-éxito---nivel-aaa)
    - [6.6. Presupuesto general](#66-presupuesto-general)
      - [6.6.1. Criterio de Éxito - Nivel A](#661-criterio-de-éxito---nivel-a)
      - [6.6.2. Criterio de Éxito - Nivel AA](#662-criterio-de-éxito---nivel-aa)
      - [6.6.3. Criterio de Éxito - Nivel AAA](#663-criterio-de-éxito---nivel-aaa)
    - [6.7. Ejecución histórica anual](#67-ejecución-histórica-anual)
      - [6.7.1. Criterio de Éxito - Nivel A](#671-criterio-de-éxito---nivel-a)
      - [6.7.2. Criterio de Éxito - Nivel AA](#672-criterio-de-éxito---nivel-aa)
      - [6.7.3. Criterio de Éxito - Nivel AAA](#673-criterio-de-éxito---nivel-aaa)
    - [6.8. Planes de gasto público por año fiscal](#68-planes-de-gasto-público-por-año-fiscal)
      - [6.8.1. Criterio de Éxito - Nivel A](#681-criterio-de-éxito---nivel-a)
      - [6.8.2. Criterio de Éxito - Nivel AA](#682-criterio-de-éxito---nivel-aa)
      - [6.8.3. Criterio de Éxito - Nivel AAA](#683-criterio-de-éxito---nivel-aaa)
    - [6.9. Directorio de servidores públicos, empleados (i.e. funcionários)](#69-directorio-de-servidores-públicos-empleados-ie-funcionários)
      - [6.9.1. Criterio de Éxito - Nivel A](#691-criterio-de-éxito---nivel-a)
      - [6.9.2. Criterio de Éxito - Nivel AA](#692-criterio-de-éxito---nivel-aa)
      - [6.9.3. Criterio de Éxito - Nivel AAA](#693-criterio-de-éxito---nivel-aaa)
    - [6.10. Directorio de servidores públicos contratistas](#610-directorio-de-servidores-públicos-contratistas)
      - [6.10.1. Criterio de Éxito - Nivel A](#6101-criterio-de-éxito---nivel-a)
      - [6.10.2. Criterio de Éxito - Nivel AA](#6102-criterio-de-éxito---nivel-aa)
      - [6.10.3. Criterio de Éxito - Nivel AAA](#6103-criterio-de-éxito---nivel-aaa)
    - [6.11. Escalas salariales](#611-escalas-salariales)
      - [6.11.1. Criterio de Éxito - Nivel A](#6111-criterio-de-éxito---nivel-a)
      - [6.11.2. Criterio de Éxito - Nivel AA](#6112-criterio-de-éxito---nivel-aa)
      - [6.11.3. Criterio de Éxito - Nivel AAA](#6113-criterio-de-éxito---nivel-aaa)
    - [6.12. Sanciones aplicadas a servidores públicos](#612-sanciones-aplicadas-a-servidores-públicos)
      - [6.12.1. Criterio de Éxito - Nivel A](#6121-criterio-de-éxito---nivel-a)
      - [6.12.2. Criterio de Éxito - Nivel AA](#6122-criterio-de-éxito---nivel-aa)
      - [6.12.3. Criterio de Éxito - Nivel AAA](#6123-criterio-de-éxito---nivel-aaa)
    - [6.13. Información de contratos](#613-información-de-contratos)
      - [6.13.1. Criterio de Éxito - Nivel A](#6131-criterio-de-éxito---nivel-a)
      - [6.13.2. Criterio de Éxito - Nivel AA](#6132-criterio-de-éxito---nivel-aa)
      - [6.13.3. Criterio de Éxito - Nivel AAA](#6133-criterio-de-éxito---nivel-aaa)
    - [6.14. Normas generales](#614-normas-generales)
      - [6.14.1. Criterio de Éxito - Nivel A](#6141-criterio-de-éxito---nivel-a)
      - [6.14.2. Criterio de Éxito - Nivel AA](#6142-criterio-de-éxito---nivel-aa)
      - [6.14.3. Criterio de Éxito - Nivel AAA](#6143-criterio-de-éxito---nivel-aaa)
    - [6.15. Normas Reglamentarias](#615-normas-reglamentarias)
      - [6.15.1. Criterio de Éxito - Nivel A](#6151-criterio-de-éxito---nivel-a)
      - [6.15.2. Criterio de Éxito - Nivel AA](#6152-criterio-de-éxito---nivel-aa)
      - [6.15.3. Criterio de Éxito - Nivel AAA](#6153-criterio-de-éxito---nivel-aaa)
    - [6.16.](#616)
      - [6.16.1. Criterio de Éxito - Nivel A](#6161-criterio-de-éxito---nivel-a)
      - [6.16.2. Criterio de Éxito - Nivel AA](#6162-criterio-de-éxito---nivel-aa)
      - [6.16.3. Criterio de Éxito - Nivel AAA](#6163-criterio-de-éxito---nivel-aaa)
    - [6.17. Metas y objetivos](#617-metas-y-objetivos)
      - [6.17.1. Criterio de Éxito - Nivel A](#6171-criterio-de-éxito---nivel-a)
      - [6.17.2. Criterio de Éxito - Nivel AA](#6172-criterio-de-éxito---nivel-aa)
      - [6.17.3. Criterio de Éxito - Nivel AAA](#6173-criterio-de-éxito---nivel-aaa)
    - [6.18. Indicadores de gestión y/o desempeño](#618-indicadores-de-gestión-yo-desempeño)
      - [6.18.1. Criterio de Éxito - Nivel A](#6181-criterio-de-éxito---nivel-a)
      - [6.18.2. Criterio de Éxito - Nivel AA](#6182-criterio-de-éxito---nivel-aa)
      - [6.18.3. Criterio de Éxito - Nivel AAA](#6183-criterio-de-éxito---nivel-aaa)
    - [6.19. Plan anticorrupción y de atención al ciudadano](#619-plan-anticorrupción-y-de-atención-al-ciudadano)
      - [6.19.1. Criterio de Éxito - Nivel A](#6191-criterio-de-éxito---nivel-a)
      - [6.19.2. Criterio de Éxito - Nivel AA](#6192-criterio-de-éxito---nivel-aa)
      - [6.19.3. Criterio de Éxito - Nivel AAA](#6193-criterio-de-éxito---nivel-aaa)
    - [6.20. Plan anual de compras y adquisiciones](#620-plan-anual-de-compras-y-adquisiciones)
      - [6.20.1. Criterio de Éxito - Nivel A](#6201-criterio-de-éxito---nivel-a)
      - [6.20.2. Criterio de Éxito - Nivel AA](#6202-criterio-de-éxito---nivel-aa)
      - [6.20.3. Criterio de Éxito - Nivel AAA](#6203-criterio-de-éxito---nivel-aaa)
  - [7. Información Mínima Obligatoria respecto a Servicios, Procedimientos y Funcionamiento](#7-información-mínima-obligatoria-respecto-a-servicios-procedimientos-y-funcionamiento)
    - [7.1. Servicios](#71-servicios)
      - [7.1.1. Criterio de Éxito - Nivel A](#711-criterio-de-éxito---nivel-a)
      - [7.1.2. Criterio de Éxito - Nivel AA](#712-criterio-de-éxito---nivel-aa)
      - [7.1.3. Criterio de Éxito - Nivel AAA](#713-criterio-de-éxito---nivel-aaa)
    - [7.2. Trámites](#72-trámites)
      - [7.2.1. Criterio de Éxito - Nivel A](#721-criterio-de-éxito---nivel-a)
      - [7.2.2. Criterio de Éxito - Nivel AA](#722-criterio-de-éxito---nivel-aa)
      - [7.2.3. Criterio de Éxito - Nivel AAA](#723-criterio-de-éxito---nivel-aaa)
    - [7.3. Procedimientos de toma de decisiones](#73-procedimientos-de-toma-de-decisiones)
      - [7.3.1. Criterio de Éxito - Nivel A](#731-criterio-de-éxito---nivel-a)
      - [7.3.2. Criterio de Éxito - Nivel AA](#732-criterio-de-éxito---nivel-aa)
      - [7.3.3. Criterio de Éxito - Nivel AAA](#733-criterio-de-éxito---nivel-aaa)
    - [7.4. Decisiones](#74-decisiones)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-éxito---nivel-a)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-éxito---nivel-aa)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-éxito---nivel-aaa)
    - [7.5. Políticas](#75-políticas)
      - [7.5.1. Criterio de Éxito - Nivel A](#751-criterio-de-éxito---nivel-a)
      - [7.5.2. Criterio de Éxito - Nivel AA](#752-criterio-de-éxito---nivel-aa)
      - [7.5.3. Criterio de Éxito - Nivel AAA](#753-criterio-de-éxito---nivel-aaa)
    - [7.6. Mecanismos de participación ciudadana](#76-mecanismos-de-participación-ciudadana)
      - [7.6.1. Criterio de Éxito - Nivel A](#761-criterio-de-éxito---nivel-a)
      - [7.6.2. Criterio de Éxito - Nivel AA](#762-criterio-de-éxito---nivel-aa)
      - [7.6.3. Criterio de Éxito - Nivel AAA](#763-criterio-de-éxito---nivel-aaa)
    - [7.7. Informe de participación ciudadana](#77-informe-de-participación-ciudadana)
      - [7.7.1. Criterio de Éxito - Nivel A](#771-criterio-de-éxito---nivel-a)
      - [7.7.2. Criterio de Éxito - Nivel AA](#772-criterio-de-éxito---nivel-aa)
      - [7.7.3. Criterio de Éxito - Nivel AAA](#773-criterio-de-éxito---nivel-aaa)
    - [7.8. Mecanismos de participación ciudadana en formulación de políticas](#78-mecanismos-de-participación-ciudadana-en-formulación-de-políticas)
      - [7.8.1. Criterio de Éxito - Nivel A](#781-criterio-de-éxito---nivel-a)
      - [7.8.2. Criterio de Éxito - Nivel AA](#782-criterio-de-éxito---nivel-aa)
      - [7.8.3. Criterio de Éxito - Nivel AAA](#783-criterio-de-éxito---nivel-aaa)
    - [7.9. Informes de gestión, evaluación y auditoría](#79-informes-de-gestión-evaluación-y-auditoría)
      - [7.9.1 Informes de gestión](#791-informes-de-gestión)
        - [7.9.1.1 Criterio de Éxito - Nivel A](#7911-criterio-de-éxito---nivel-a)
        - [7.9.1.2 Criterio de Éxito - Nivel AA](#7912-criterio-de-éxito---nivel-aa)
        - [7.9.1.3 Criterio de Éxito - Nivel AAA](#7913-criterio-de-éxito---nivel-aaa)
      - [7.9.2 Informe de rendición de la cuenta fiscal](#792-informe-de-rendición-de-la-cuenta-fiscal)
        - [7.9.2.1 Criterio de Éxito - Nivel A](#7921-criterio-de-éxito---nivel-a)
        - [7.9.2.2 Criterio de Éxito - Nivel AA](#7922-criterio-de-éxito---nivel-aa)
        - [7.9.2.3 Criterio de Éxito - Nivel AAA](#7923-criterio-de-éxito---nivel-aaa)
      - [7.9.3 Informe de rendición de cuentas a los ciudadanos](#793-informe-de-rendición-de-cuentas-a-los-ciudadanos)
        - [7.9.3.1 Criterio de Éxito - Nivel A](#7931-criterio-de-éxito---nivel-a)
        - [7.9.3.2 Criterio de Éxito - Nivel AA](#7932-criterio-de-éxito---nivel-aa)
        - [7.9.3.3 Criterio de Éxito - Nivel AAA](#7933-criterio-de-éxito---nivel-aaa)
      - [7.9.4 Informes de Auditoría](#794-informes-de-auditoría)
        - [7.9.4.1 Criterio de Éxito - Nivel A](#7941-criterio-de-éxito---nivel-a)
        - [7.9.4.2 Criterio de Éxito - Nivel AA](#7942-criterio-de-éxito---nivel-aa)
        - [7.9.4.3 Criterio de Éxito - Nivel AAA](#7943-criterio-de-éxito---nivel-aaa)
    - [7.10. Mecanismos internos de supervisión](#710-mecanismos-internos-de-supervisión)
      - [7.10.1. Criterio de Éxito - Nivel A](#7101-criterio-de-éxito---nivel-a)
      - [7.10.2. Criterio de Éxito - Nivel AA](#7102-criterio-de-éxito---nivel-aa)
      - [7.10.3. Criterio de Éxito - Nivel AAA](#7103-criterio-de-éxito---nivel-aaa)
    - [7.11. Mecanismos externos de supervisión](#711-mecanismos-externos-de-supervisión)
      - [7.11.1. Criterio de Éxito - Nivel A](#7111-criterio-de-éxito---nivel-a)
      - [7.11.2. Criterio de Éxito - Nivel AA](#7112-criterio-de-éxito---nivel-aa)
      - [7.11.3. Criterio de Éxito - Nivel AAA](#7113-criterio-de-éxito---nivel-aaa)
    - [7.12. Correo electrónico para notificaciones judiciales](#712-correo-electrónico-para-notificaciones-judiciales)
      - [7.12.2. Criterio de Éxito - Nivel A](#7122-criterio-de-éxito---nivel-a)
      - [7.12.2. Criterio de Éxito - Nivel AA](#7122-criterio-de-éxito---nivel-aa)
      - [7.12.3. Criterio de Éxito - Nivel AAA](#7123-criterio-de-éxito---nivel-aaa)
    - [7.13. Procedimientos y lineamientos de contratación](#713-procedimientos-y-lineamientos-de-contratación)
      - [7.13.1. Criterio de Éxito - Nivel A](#7131-criterio-de-éxito---nivel-a)
      - [7.13.2. Criterio de Éxito - Nivel AA](#7132-criterio-de-éxito---nivel-aa)
      - [7.13.3. Criterio de Éxito - Nivel AAA](#7133-criterio-de-éxito---nivel-aaa)
    - [7.14. Políticas en materia de adquisiciones y compras](#714-políticas-en-materia-de-adquisiciones-y-compras)
      - [7.14.1. Criterio de Éxito - Nivel A](#7141-criterio-de-éxito---nivel-a)
      - [7.14.2. Criterio de Éxito - Nivel AA](#7142-criterio-de-éxito---nivel-aa)
      - [7.14.3. Criterio de Éxito - Nivel AAA](#7143-criterio-de-éxito---nivel-aaa)
  - [8. Instrumentos De Gestión De la Información Pública](#8-instrumentos-de-gestión-de-la-información-pública)
    - [8.1. Esquemas de publicación de información](#81-esquemas-de-publicación-de-información)
      - [8.1.1. Criterio de Éxito - Nivel A](#811-criterio-de-éxito---nivel-a)
      - [8.1.2. Criterio de Éxito - Nivel AA](#812-criterio-de-éxito---nivel-aa)
      - [8.1.3. Criterio de Éxito - Nivel AAA](#813-criterio-de-éxito---nivel-aaa)
    - [8.2. Programa de gestión documental](#82-programa-de-gestión-documental)
      - [8.2.1. Criterio de Éxito - Nivel A](#821-criterio-de-éxito---nivel-a)
      - [8.2.2. Criterio de Éxito - Nivel AA](#822-criterio-de-éxito---nivel-aa)
      - [8.2.3. Criterio de Éxito - Nivel AAA](#823-criterio-de-éxito---nivel-aaa)
    - [8.3. Tablas de retención documental](#83-tablas-de-retención-documental)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-éxito---nivel-a)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-éxito---nivel-aa)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-éxito---nivel-aaa)
    - [8.4. Respuestas a solicitudes de información recibidas](#84-respuestas-a-solicitudes-de-información-recibidas)
      - [8.4.1. Criterio de Éxito - Nivel A](#841-criterio-de-éxito---nivel-a)
      - [8.4.2. Criterio de Éxito - Nivel AA](#842-criterio-de-éxito---nivel-aa)
      - [8.4.3. Criterio de Éxito - Nivel AAA](#843-criterio-de-éxito---nivel-aaa)

## 1. Introducción

Esta sección no es normativa.

Esta especificación tiene el propósito de generar una herramienta (que sea a la vez un foro público) sobre la forma de categorizar y de evaluar la transparencia activa de las entidades gubernamentales en Colombia.

Su objetivo general se enmarca en apuntalar el rol de la sociedad civil en el control y seguimiento de la política pública en materia de transparencia del Estado colombiano, a partir de la expedición de la Ley 1712 de 2014.

Alineada con la filosofía de esta ley, esta especificación busca servir de insumo para fomentar la transparencia activa, la rendición de cuentas de los sujetos obligados y aportar a la ingente tarea de la lucha contra la corrupción.

Su público objetivo es doble, por un lado, la ciudadanía (activistas, académicos, ingenieros) interesada en los temas de transparencia estatatal; y por otra parte, las entidades gubernamentales, entendidas como "sujetos obligados", y como las primeras llamadas a satisfacer las demandas de transparencia activa, por tanto, entendidas como sujetos de monitoreo y evaluación por parte de la herramienta.

Esta especificación está pensada para generar un lugar de debate y de mejora sobre la adecuación de las prácticas de transparencia activa, a partir del uso de las páginas web de las entidades gubernamentales, la adecuación de las mismas, su funcionalidad y su constante mejora, a partir de la identificación de las obligaciones generales de transparencia, pero también de la inclusión de recomendaciones o de mejores prácticas en la materia.

### 1.1 Transparencia, Rendición de Cuentas y lucha contra la corrupción

Esta especificación se alimenta de los principios de la Ley 1712 de 2014 en materia de transparencia y acceso a la información pública. Toma nota de las demandas de distintos actores, tanto nacionales, como internacionales, del público especializado y de la ciudadanía en general sobre la importancia de optimizar los recursos y la funcion de las entidades gubernamentales.  Ya desde los foros que afinan las mejores prácticas de la gobernanza del sector público, como desde aquellos que claman por políticas eficaces de lucha contra la corrupción. Esta especificación intenta ser un modesto aporte en estas materias.

Esta especificación tiene como propósito concretar las demandas sobre transparencia activa mediante la definición de ciertas categorías y de ciertos criterios que puedan ser empleados para la medición del cumplimiento de las obligaciones de transparencia activa por parte de las entidades estatales en el entorno digital a través de las páginas web o los sitios web oficiales de dichas entidades en la Internet.

Esta especificación presupone que, entre más transparencia de la actividad estatal, que se pueda concretar y medir, seria y periodicamente, mejor será la rendición de cuentas de los servidores públicos.  Y si esto es así, mejores serán las prácticas en el uso del poder y en la asignación de los recursos públicos, mejores las posibilidades de control por parte de las agencias especializadas, de la prensa y de la ciudadanía. Y por tanto, mejores serán las condiciones para luchar contra el complejo fenómeno de la corrupción.


### 1.2 Público objetivo

El público objetivo de esta especificación es todo aquel interesado en la categorización y la medición de las obligaciones de transparencia activa de las entidades gubernamentales.
Por un lado tenemos a la ciudadanía interesada: académicos, investigadores, periodistas, activistas, miembros de la sociedad civil.  En especial, aquellos que cuenten con algún nivel de conocimiento sobre los pormenores técnicos, científicos, jurídicos y políticos de las herramientas para categorizar y evaluar las obligaciones de transparencia activa de las entidades gubernamentales.
Por el otro, tenemos a las entidades gubernamentales, en cabeza de sus órganos directivos, funcionarios  y contratistas especializados en las áreas de transparencia y diseño de las páginas web de las entidades gubernamentales.

### 1.3 Filosofía y Presupuestos

La filosofía de esta especificación es la del trabajo colaborativo.  Está orientada por la idea de habilitar un foro público de discusión en materia de categorización de las obligaciones de transparencia activa en Colombia, y en materia de evaluación del desempeño de las entidades gubernamentales.

Esta especificación está concebida como un permanente trabajo en progreso. En donde distintos actores son bienvenidos para sugerir mejoras, cambios, adiciones, revisiones sobre la mejor funcionalidad, pertinencia y adecuación de la misma.  No es ni pretende ser un trabajo acabado sobre la forma de categorizar y evaluar las obligaciones de transparencia activa de las entidades gubernamentales en Colombia.

Esta especificación parte de los siguientes presupuestos:

i) que la sociedad civil ha de tomar parte en los procesos que la afectan, y en especial, debe tomar parte en la agenda de transparentar el Estado y de llamarlo a rendir cuentas

ii) que las discusiones de la sociedad civil sobre transparencia activa han de tener lugar en público (transparencia acerca de transparencia) y aprovechar todas las ventajas que los desarrollos tecnológicos permiten.

iii) que es necesario que las parte interesadas -- la sociedad civil (i.e. ciudadanía, investigadores, académicos) y las entidades gubernamentales-- tengan una base común, sobre el vocabulario técnico, las categorías de análisis y los criterios de evaluación, que permita evaluar los desempeños y ajustar las expectativas en materia de transparencia activa.

iv) que en la medida en que se estandaricen y se concerten mecanismos de evaluación de desempeño de las políticas de transparencia activa, será más fácil medir los resultados, identificar los avances o los retrocesos, y llamar a cuentas a los responsables dentro de las entidades gubernamentales

### 1.4 Interdisciplinaridad

Conforme con su filosofía, esta especificación ha sido construida a partir de la concurrencia de distintos saberes, desde la ciencias de la información, pasando por la ciencia de la administración pública y la disciplina jurídica, hasta las propias de la programación, la ingeniería de sistemas y el diseño.

Esta especificación está abierta a la participación y a la colaboración de distintos actores (desde diversas disciplinas) que compartan la filosofía y finalidad de la especificación.

### 1.5 Regulación

La identificación de las categorías y de los criterios de investigación de esta regulación se basan principalmente en los mandatos de la Ley 1712 de 2014, *"Por medio de la cual se crea la Ley de Transparencia y del Derecho de Acceso a la Información Pública Nacional y se dictan otras disposiciones."* Tal y como fue interpretada por la Corte Constitucional en la Sentencias C-274 de 2013, MP María Victoria Calle.

En los contenidos del Decreto 103 de 2015, *"Por el cual se reglamenta parcialmente la Ley 1712 de 2014 y se dictan otras disposiciones"*, que a su vez fue incorporado al Decreto 1078 de 2015, *"Por medio del cual se expide el Decreto Reglamentario Único del Sector Presidencia de la República"*. En especial, en sus artículo Artículos 1.1.1.1 a 3.1.2.

En los contenidos de la Resolución 3564 de 2015 2015 *"Por la cual se reglamentan aspectos relacionados con la Ley de Transparencia y Acceso a la Información Pública"*.

Asimismo, incluye obligaciones específicas que han sido incluidas o precisadas en distintas fuentes normativas, como la Ley 1474 DE 2011 *"Por la cual se dictan normas orientadas a fortalecer los mecanismos de prevención, investigación y sanción de actos de corrupción y la efectividad del control de la gestión pública"* y el Decreto Nacional 1510 de 2013 *"Por el cual se reglamenta el sistema de compras y contratación pública"*, entre otras.

### 1.6 Documentos de Apoyo

### 1.7 Colaboración

La mejor manera de colaborar esto es creando un mensagje en la sessión "issues" en el [repositorio oficial en Github](https://github.com/Dejusticia/mota-active-transparency-specification/). Así, facilita su contribución y ayuda a todos los usuarios. Si tiene experiencia contribuyendo a proyectos de código abierto, puede bifurcar el repositorio oficial, editar los archivos en la rama develop y luego enviar un "pull request".

Una otra forma es enviar un mensaje al correo mota (arroba) dejusticia punto org. Pero en razón del volumen de mensajes, no podemos garantizar respuestas rápidas. Por esto, recomendamos enviar mensaje en el repositorio, asi garantiza que su mensaje sea leído por todos los miembros del equipo de desarrollo del proyecto y otros usuarios que podrán responder más rápidamente y colaborativamente.

Por favor, sea claro, conciso y civilizado. Preferimos [español](CONTRIBUYENDO.md), pero también puede usar [inglés](CONTRIBUTING.md) y [portugués](CONTRIBUINDO.md).

Más información puede encontrarse en el documento [CONTRIBUYENDO.md](CONTRIBUYENDO.md).

## 2. Uso de la especificación

Esta sección no es normativa.

## 3. Conformidad y Categorias de Éxito

Además de las secciones marcadas como "no normativas", todos los diagramas, ejemplos y notas en esta especificación son no normativos (excepto cuando marcados en contrario). El resto de esta especificación es normativo.

Las palabras clave ("DEBE"), ("NO DEBE"), ("REQUERIDO"), ("DEBERÍA"), ("NO DEBERÍA"), ("DEBERÁ"), ("NO DEBERÁ"), ("RECOMENDADO"), ("PUEDE") y ("OPCIONAL") en este documento serán interpretadas tal como se describe en [RFC2119](https://tools.ietf.org/html/rfc2119). Sin embargo, por razones de legibilidad, estas palabras no aparecen en mayúsculas en esta especificación.

### 3.1 Conformidad

Para que un sitio web esté en conformidad con esta especificación, debe cumplir con todos y cada uno de los critérios de evaluación en cada uno de los criterios en al menos el nivel A. La categoria de conformidad (A, AA o AAA) es determinada de acuerdo con los grados obtenidos en la evaluación. Es decir, un sitio web obtiene Conformidad A si ha obtenido el grado A en todos los criterios de evaluación. Del mismo modo, cumple con AA solo si obtiene la calificación AA en todos los criterios, etc.

Para que un sitio web esté en conformidad con esta especificación, debe cumplir con todos y cada uno de los critérios de evaluación en cada uno de los criterios en al menos el nivel A y obtener no menos de 50 puntos en la escala de conformidad general, cuyos valores varían entre 0 y 100:

- 90-100 (Conformidad)
- 50-89 (Conformidad parcial)
- 20-49 (Insuficiente)
- 1-19 (Deficiente)
- 0 (No conformidad)

Un sitio web que no cumple con al menos 1 de los critérios de evaluación, se considera en no conformidad.

### 3.2. OBLIGACIÓN y RECOMENDACIÓN

Clasificamos cada criterio como OBLIGACIÓN o RECOMENDACIÓN. El primero significa que el criterio de evaluación es obligatorio y DEBE ser implementado, pues es REQUERIDO de acuerdo con el marco legal colombiano. Mientras que el segundo significa que el criterio es OPCIONAL, y el sujeto obligado DEBERÍA implementarlo para que: i) el acceso y la comprensión de la información sean efectivos; y/o ii) se mejore la experiencia del usuario, especialmente aquellos en condiciones donde el acceso a la información es más difícil debido a discapacidades físicas, cognitivas, neuronales o condiciones técnicas y económicas tales como acceso restringido a conexiones de datos, o baja velocidad de conexiones, o dispositivos con capacidades de procesamiento más bajas.

### 3.3. - Nivel de Éxito en Critérios de Evaluación

**Nivel A:** el sitio web satisface lo especificado para nivel A en cada criterio de evaluación adelante. Si el criterio de evaluación no especifica una puntuación diferente, el cumplimiento del criterio en nivel A equivale a **50 puntos**.

Este es el nivel mínimo aceptable dentro del contexto de las entidades públicas colombianas a partir de julio de 2019.

**Nivel AA:** el sitio web satisface lo especificado para nivel AA y A en cada criterio de evaluación adelante. Si el criterio de evaluación no especifica una puntuación diferente, el cumplimiento del criterio en nivel AA equivale a **80 puntos**, no cumulativos con los puntos del nivel A.

Este es el nivel deseado de forma inmediata o a corto plazo, considerando el contexto de las entidades públicas colombianas en julio de 2019.

**Nivel AAA:** el sitio web satisface *lo especificado para nivel AAA y también DEBE satisfacer lo especificado en nivel AA y A* en cada criterio de evaluación adelante. Si el criterio de evaluación no especifica una puntuación diferente, el cumplimiento del criterio en nivel A equivale a **100 puntos**, no cumulativos con los puntos del nivel A.

Este es el nivel ideal, el objetivo a medio y largo plazo a partir de agosto de 2019.

**Incumplimiento:** Si el sitio no cumple con el mínimo determinado en el nivel A del criterio de evaluación, recibe un puntaje cero y se considera que está en incumplimiento con el criterio.

### 3.4 - Escala de Puntos: diretrices de disponibilidad de información

Las directrices relacionadas con la disponibilidad de información adoptan una escala de puntos más detallada que aquella basada en la disponibilidad o no de la informacion.

Como regla general, mide el cumplimiento de las mejores prácticas delineadas por Open Knowledge Foundation en El manual de Open Data [(Open Data Handbook)](http://opendatahandbook.org/guide/es/) y las recomendaciones de W3C en [publicación de datos de gobierno abierto](https://www.w3.org/TR/gov-data/).

La escala de puntos varía de 0 a 100, y se correlaciona con el marco [5 estrellas para Datos Abiertos](https://5stardata.info/es/), con las siguientes reglas base de puntuación.

#### Nivel A: Información disponible en archivo

La información está disponible en archivo, de acuerdo a una de las opciones a seguir:

   - en formato propietario (docx, xlsx, pdf): 20 puntos
   - en formato abierto y libre, pero no legible/acesible por máquina (e.g. texto o tabla digitalizado): 35 puntos
   - en formato abierto y libre, con datos estructurados (e.g. en caso de tablas) y legible/acesible por máquina: 50 puntos

Los puntos no son acumulativos.

> *Observación**: aproximadamente igual a los grados 2 o 3 estrellas en el marco [5 estrellas para Datos Abiertos](https://5stardata.info/es/).

**Importante:** si los datos están solamente en otros sitios (e.g. SECOP, Datos Abiertos, etc.), la puntuación es reducida a la mitad.


#### Nivel AA: Información disponible para personas disponibles en la misma página

La información está disponibles en el sitio web, de acuerdo a una de las opciones a seguir:

   - en formato HTML en la misma página: 15 puntos
   - en HTML5 estructurado, semántico y en la misma página: 30 puntos
     - ejemplo: tabla para datos estructurados; H2, h3, etc para subtítulos

Los puntos se pueden acumular con los puntos del nivel A.

#### Nível AAA: Información disponible como meta-datos estructurados legible por máquina

Además de conformidad con el nivel AA, la información está disponible como meta-datos estructurados legible por máquina.

   - datos estructurados (schema.org, json, meta-datos, etc) en la misma página: 20 puntos

Los puntos se pueden acumular con los puntos del nivel AA.

Para directrices no relacionadas con la disponibilidad de informacción, como por ejemplo, el desempeño de la página y la facilidad para acceder a la información, además de cambiar los pesos de los criterios (abajo) debemos cambiar la puntuación según sea necesario, solo SI es necesario.

> **Observación**: aproximadamente igual a grado 4 estrellas en el marco [4 estrellas para Datos Abiertos](https://5stardata.info/es/).

##### Observaciones sobre Criterios de Éxito

Nota 1: A pesar de que la conformidad sólo puede lograrse en los niveles indicados, se anima a los autores a notificar en sus declaraciones cualquier progreso que se realice para satisfacer los criterios de éxito de todo nivel más allá del nivel de conformidad alcanzado.

Nota 2: No se recomienda como política general exigir el nivel de conformidad AAA para sitios enteros porque es posible que haya casos de sitios que no puedan satisfacer todos los criterios de éxito de nivel AAA.

### 3.1 Herramientas para examen de conformidad

#### WCAG2.1 y Acessibilidad

- Functional Accessibility Evaluator: https://fae.disability.illinois.edu
- Taw Web accessibility test: [https://www.tawdis.net/index](https://www.tawdis.net/index)

## 4. Términos importantes (vocabulario)

## 5. Categoría - Disponibilidad de acceso

Esta categoría reúne los criterios de evaluación sobre la disponibilidad de acceso al sitio web del sujeto obligado. Incluye obligaciones y recomendaciones básicas como la existencia de un sitio web, acceso gratuito, uso de contraseñas para acceder y el seguimiento de buenas prácticas de accesibilidad que permiten el acceso a personas con discapacidades físicas, cognitivas o que tienen conexiones o dispositivos de baja capacidad.

### 5.1 Existencia de sitio web
<span class="criteria-type">Tipo: OBLIGACIÓN. - Artículo 7 de la Ley 1712 de 2014</span>

> **Resumen:** La entidad deberá mantener un sitio web que deberá estar disponible para acesso via una URL oficial por personas y sistemas automáticos (e.g. robots). Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

La entidad deberá mantener un sitio web que deberá estar disponible para acesso via una URL oficial por personas y sistemas automáticos (e.g. robots).

Este criterio de evaluación tiene solo un nivel de exito (AAA).

#### 5.1.1 Criterio de Éxito - Nivel AAA

El sitio retorna páginas con códigos HTTP 200 o 314 en su URI oficial, cuando es accedido por cualquier usuario.

Nota: se aceptan redireccionamientos con códigos HTTP 301 y 302, siempre que i) no exceda de 2 redireccionamientos y ii) conduzca a páginas que retornen los códigos HTTP 200 y 314.

### 5.2 Gratuidad
Tipo: OBLIGACIÓN.

> **Resumen:** El sítio debe tener acceso gratuito a los servicios informáticos que presta la entidad excepto para los casos previstos en la ley o en los reglamentos.

El sitio web debe tener acceso gratuito a los servicios informáticos que presta la entidad excepto para casos previstos en ley o en los reglamentos.

Este critério de evaluación tiene solo dos niveles de exito (AA y AAA).

#### 5.2.1. Criterio de Éxito - Nivel AA

Algunos servicios solo son accesibles por contraseña u otro identificador obtenidos a partir de botones y/o otros métodos de pago detectados en el sitio.

#### 5.2.2. Criterio de Éxito - Nivel AAA

Todos los servicios son accesibles sin contrapartida financiera, botones u otros métodos de pago.

### 5.3. - Universalidad: Acceso directo
Tipo: RECOMENDACIÓN

> **Resumen:** Los servicios informáticos que presta la entidad en su sitio web deben ser abiertos a todo el público que desee acceder a ellos y no deben estar restringidos a ciertos usuarios previo registro y recepción de una clave de acceso, exceto para casos previstos en ley y en reglamentos.

Los servicios informáticos que presta la entidad en su sitio web deben ser abiertos a todo el público que desee acceder a ellos y no deben estar restringidos a ciertos usuarios previo registro y recepción de una clave de acceso, exceto para casos previstos en ley y en reglamentos.

#### 5.3.1. Criterio de Éxito - Nivel A

Registro y clave de acceso son necesarios para acceder a una parte del sitio sin una justificación adecuada (e.g. privacidad de datos personales o seguridad).

#### 5.3.2. Criterio de Éxito - Nivel AA

Registro y clave de acceso son necesarios para acceder a una parte del sitio con una justificación adecuada (e.g. privacidad de datos personales o seguridad).

#### 5.3.3. Criterio de Éxito - Nivel AAA

Todos los servicios son accesibles sin registro previo ni clave de acceso.

### 5.4 - Universalidad: Patrones de accesibilidad y web standards
Tipo: RECOMENDACIÓN

> **Resumen:** Para garantizar el acceso a la mayor cantidad posible de ciudadanos, independientemente de sus circunstancias físicas, cognitivas, sociales o económicas, los sitios web deben desarrollarse siguiendo los estándares web y las mejores prácticas de accesibilidad. Los sitios deben permitir acesso de tecnologias asistivas como lectores de tela, asistentes por voz, etc., así como desde dispositivos de baja capacidad y conexión de baja velocidad.

Los sitios deben permitir acceso igualitario por:

   1) Tecnologías de asistencia como lectores de pantalla, asistentes de voz, etc;
   2) Acceso sin uso de javascript o plugins de terceros;
   3) Acceso por dispositivos variados como computadores, teléfonos inteligentes, asistentes de voz (e.g. Amazon Alexa), SmartTVs y otros dispositivos;
   4) Acceso  con distintos tipos de conexiones (banda ancha,5G, 4G y 3G de bajo rendimiento), para lo cual deben seguir principios y directrices de accesibilidad conforme a los definidos por la [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/), recomendación WCAG2.1 y WAI-ARIA de W3C y siguiendo las mejores prácticas determinadas en The Web Standards projects para markup sin considerar metadatos o atributos semánticos (e.g. elementos HTML semánticos, sin considerar schema.org o RDF markup).

La evaluación se realizó sobre la página de inicio (ubicación oficial) y otras 20 páginas: 10 de primer nivel, 5 páginas de segundo nivel y 5 de tercer nivel, determinadas según posición en el menú principal y/o directorios en la dirección URL después del nombre de dominio.

#### 5.4.1. Criterio de Éxito - Nivel A

El sitio web es válido en el [https://validator.w3.org/unicorn/](https://validator.w3.org/unicorn/) con no más que 50 errores, siguiendo la especificación [HTML5](https://w3c.github.io/html/). **Temporalmente**, la recomendación [XHTML 1.1](https://www.w3.org/TR/xhtml11/) también es aceptada por MOTA.

###### Sobre la aceptación de XHTML

**Temporalmente, debido a la necessidad de compatibilidad con versiones anteriores de sistemas de gerenciamento de contenido**, la recomendación [XHTML 1.1](https://www.w3.org/TR/xhtml11/) también es aceptada por MOTA.

Sin embargo, observamos que XHTML no es la recomendación más reciente y más efectiva para los sitios web para público general. Además, el estándar HTML5 proporciona medios para crear documentos que son válidos como HTML5 y XML. De hecho, XHTML5 es un documento HTML5 enviado con la MIME Type `application/xhtml+xml` y, preferiblemente, siguiendo el concepto de marcado de texto políglota. Por lo que este solo se aceptará en la versión 1.0 de la especificación MOTA o a partir julio de 2020.

 Más información acerca XML+HTML5 se puede encontrar en inglés en [WHATWG](https://html.spec.whatwg.org/multipage/introduction.html#html-vs-xhtml), [W3C](https://dev.w3.org/html5/html-polyglot/) y [Wikipedia](https://en.wikipedia.org/wiki/Polyglot_markup#Polyglot_HTML_requirements)

#### 5.4.2. Criterio de Éxito - Nivel AA

El sitio web es válido en el [https://validator.w3.org/unicorn/](https://validator.w3.org/unicorn/) con no más que 50 errores, siguiendo la especificación [HTML5](https://w3c.github.io/html/) y utilizando los elementos de la especificación de forma semántica. Es decir, utilizando correctamente los elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, nav para elemento de navegación etc.).

El sitio cumple con los criterios A de la [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/) o su equivalente [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/) (en inglés).

#### 5.4.3. Criterio de Éxito - Nivel AAA

El sitio web es válido en el [https://validator.w3.org/unicorn/](https://validator.w3.org/unicorn/)  sin errores y con no más que 50 advertencias, siguiendo la especificación [HTML5](https://w3c.github.io/html/) y utilizando los elementos de la especificación de forma semántica. Es decir, utilización correctamente los elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, nav para elemento de navegación etc.).

El sitio cumple con los criterios A y AA de la [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/) o su equivalente [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/) (en inglés).

El sitio utiliza de forma adequada las prácticas [wai-aria-1.2](https://w3c.github.io/aria/) (en inglés);

### 5.5 - Universalidad: Rendimiento
Tipo: RECOMENDACIÓN

> **Resumen:** Los sitios deben permitir acceso con velocidad razonable y estable incluso en malas condiciones de acceso, como conexión por dispositivos móviles en redes de bajo rendimiento.

Los sitios deben permitir acceso con velocidad razonable y estable incluso en malas condiciones de acceso, como conexión por dispositivos móviles en redes de bajo rendimiento. Los sitios deben obtener grados mínimos en la herramientas [Webpagetest](http://webpagetest.org/result/190506_KG_29de3021baf30242013b8f58843cd7df/) y [Pagespeed Insights](https://developers.google.com/speed/pagespeed/insights/), de acuerdo con lo descrito a continuación.

En Webpagetest, los test son efectuados con la siguiente configuración:
    - Test Location: Android Devices - Dulles, VA, Moto G (gen 4);
    - Browser: Moto G4 - Chrome;
    - Connection: 3G (1.6 Mbps/768 Kbps RTT)
    - Number of Tests to Run: 9;
    - Repeat View: First View and Repeat View;
    - Capture Video: marcado
    - Ignore SSL Certificate Errors: marcado

#### 5.5.1. Criterio de Éxito - Nivel A

Los sitios deben obtener los siguientes grados máximos:

##### WebPagetest
    - Time to First Byte: 3.500s
    - First Interactive (beta): 30.000s
    - Speed Index: 21.000s
    - Bytes in: 4.096kb

##### Pagespeed Insights
    - Ordenador: 60
    - Móvil: 30

#### 5.5.2. Criterio de Éxito - Nivel AA

Los sitios deben obtener los siguientes grados máximos:

##### WebPagetest
    - Time to First Byte: 2.500s
    - First Interactive (beta): 25.000s
    - Speed Index: 14.000s
    - Bytes in: 2.048kb

##### Pagespeed Insights
    - Ordenador: 75
    - Móvil: 50

#### 5.5.3. Criterio de Éxito - Nivel AAA

Los sitios deben obtener los siguientes grados máximos:

##### WebPagetest
    - Time to First Byte: 1.500s
    - First Interactive (beta): 15.000s
    - Speed Index: 7.000s
    - Bytes in: 1.536kb

##### Pagespeed Insights
    - Ordenador: 90
    - Móvil: 75

### 5.6 - Seguridad: Conexión encriptada
Tipo: RECOMENDACIÓN

> **Resumen:** Para garantizar una mayor privacidad y seguridad de la información de los ciudadanos, los sitios web deben ofrecer acceso encriptado, utilizando certificados de seguridad y versiones modernas del protocolo TLS.

Para garantizar una mayor privacidad y seguridad de la información de los ciudadanos, los sitios web deben ofrecer acceso encriptado, utilizando certificados de seguridad válidos generados por autoridades de certificación internacionalmente reconocidas y versiones modernas del protocolo TLS (1.3, preferencialmente).

#### 5.6.1. Criterio de Éxito - Nivel A

El sitio es accesible en conexión encriptada opcional, utilizando protocolos 1.2 o 1.3.

#### 5.6.2. Criterio de Éxito - Nivel AA

El sitio es accesible solo en conexión encriptada, utilizando protocolos 1.2.

#### 5.6.3. Criterio de Éxito - Nivel AAA

El sitio es accesible solo en conexión encriptada, utilizando protocolos 1.3.

### 5.7 - Dados Abiertos: Acceso vía API REST
Tipo: RECOMENDACIÓN

> **Resumen:** Los contenidos del sitio son acesibles por una API REST con datos estructurados, incluso meta-dados. Esta recomendación busca facilitar el acesso a la información por robots y sistemas automatizados, aumentando las capacidades de veeduría ciudadana.

Para facilitar acesso a información por robots y sistemas automatizados, aumentando las capacidades de veeduría ciudadana, los contenidos del sitio como páginas, noticias o secciones son accesibles por máquinas utilizando [API](https://es.wikipedia.org/wiki/Interfaz_de_programaci%C3%B3n_de_aplicaciones) [REST](https://es.wikipedia.org/wiki/Transferencia_de_Estado_Representacional) [web](https://es.wikipedia.org/wiki/Web_API) con [datos estructurados](https://es.wikipedia.org/wiki/Modelo_de_datos), incluso [meta-dados](https://es.wikipedia.org/wiki/Metadatos), seguindo las mejores prácticas de datos abiertos como delineados por Open Knowledge Foundation en El manual de Open Data [(Open Data Handbook)](http://opendatahandbook.org/guide/es/) y las recomendaciones de W3C en [publicación de datos de gobierno abierto](https://www.w3.org/TR/gov-data/) para que cumplan com los requisitos del grado 4 estrellas del marco [5 estrellas para Datos Abiertos](https://5stardata.info/es/).

#### 5.7.1. Criterio de Éxito - Nivel AA

API REST disponible, con datos estructurados, en formato XML o JSON, pero sin meta-datos

#### 5.7.2. Criterio de Éxito - Nivel AA

API REST disponible, con datos estructurados y meta-datos, en formato XML o JSON.

#### 5.7.3. Criterio de Éxito - Nivel AAA

API REST disponible, con datos estructurados y meta-datos y en formato JSON.

## 6. Información Mínima Obligatoria sobre la Estructura

Información sobre la estructura del sujeto obligado, de acuerdo con el artículo 9 de la Ley 1712 de 2014.

### 6.1. Estructura orgánica / Organigrama
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 201 5, anexo 1, punto 3.4.

> **Resumen:** Para que la ciudadanía conozca la jerarquía de empleados y departamentos disponibles en la entidad, esta publica su estructura orgánica de manera gráfica (ejemplo: organigrama), y tambíen publica una descripción de la estructura orgánica, donde se ofrezca información general de cada división o dependencia.  Preferiblemente en dos formatos: descripción textual en la página e imagem o archivos en formato estructurado y abierto.

El sujeto obligado publica su estructura orgánica de manera gráfica y legible (ejemplo: organigrama), en un formato accesible y usable. Asimismo, publica una descripción de la estructura orgánica, donde se ofrezca información general de cada división o dependencia. Para que la ciudadanía conozca la jerarquía de empleados y departamentos disponibles en la entidad, y pueda llevar a cabo procedimientos de manera asertiva, el sitio web del sujeito obligado debe contener descripción de la forma en que se compone y se organiza la entidade y no tan sólo la cabeza o principal órgano que se trate.

#### 6.1.1. Criterio de Éxito - Nivel A (datos)

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx), pdf no-accesible, o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.1.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

Cumplimiento alternativos:

Además del criterio de éxito

#### 6.1.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (e.g. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

Referencias:

  - https://schema.org/Organization
  - https://schema.org/GovernmentOrganization
  - https://schema.org/GovernmentOffice
  - [(https://schema.org/department)]
  - https://schema.org/employee
  - Considerar creación de esquemas de identificadores como NIT, CC, CE, etc. e.g. https://schema.org/naics
  - Considerar vocabulario específico como https://schema.org/duns ou http://www.heppnetz.de/projects/goodrelations/
  - https://schema.org/contactPoint
  - https://schema.org/OrganizationRole

### 6.2. Funciones y deberes
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 3.2.

> **Resumen:** Para que la población tenga claridad sobre el papel y qué esperar de la entidad, el sujeto obligado publica una descripción de funciones y deberes de la entidad en general y no tan sólo la cabeza o principal órgano que lo compone. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

Para que la población tenga claridad sobre el papel y qué esperar de la entidad, el sujeto obligado publica una descripción de funciones y deberes de la entidad en general y no tan sólo la cabeza o principal órgano que lo compone. El sujeto obligado publica sus funciones y deberes de acuerdo con su norma de creación o reestructuración. Si alguna norma le asigna funciones adicionales, éstas también están incluidas.

#### 6.2.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerrpo de la capa de sesión.

#### 6.2.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página en HTML. (e.g. tablas o listas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.2.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (e.g. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.3. Ubicación de sus sedes y áreas, divisiones o departamentos / Localización física, sucursales o regionales
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 1.2.

> **Resumen:** Ubicación física del sujeto obligado, de sus sedes, áreas, divisiones, departamentos y/o regionales, según corresponda, incluyendo ciudad y departamento de ubicación. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

Ubicación física del sujeto obligado, de sus sedes, áreas, divisiones, departamentos y/o regionales, según corresponda, incluyendo ciudad y departamento de ubicación.

#### 6.3.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) o disponibles en una página en formato de imagen. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.3.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en un página en HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Al menos una ubicación disponible en pie de página.

#### 6.3.3. Criterio de Éxito - Nivel AAA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página en HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Al menos una ubicación disponible en pie de página. La información también está  disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org  [GovernmentOffice](https://schema.org/GovernmentOffice), [GovernmentBuilding](https://schema.org/GovernmentBuilding), [Organization](https://schema.org/Organization), [PostalAddress](https://schema.org/PostalAddress).

### 6.4. Divisiones o departamentos
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 1.2.

> **Resumen:** Información general sobre las divisiones territoriales del sujeto obligado: indicación cáales son las divisiones, direcciones, etc. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

Información sobre la totalidad de divisiones territoriales. Para considerar como positiva esta pauta, basta con que la información sea general (indicación de cuales son, direcciones, etc.) y no es necesario que todo el contenido del sitio sea el mismo para todas las divisiones territoriales.

#### 6.4.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.4.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en un página, en HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.4.3. Criterio de Éxito - Nivel AAA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página, en HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Al menos una ubicación disponible en pie de página. La información también está  disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org  [GovernmentOffice](https://schema.org/GovernmentOffice), [GovernmentBuilding](https://schema.org/GovernmentBuilding), [Organization](https://schema.org/Organization) con propriedad [department](https://schema.org/department), [PostalAddress](https://schema.org/PostalAddress).

### 6.5. Horario de Atención al Público
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 1.2.

> **Resumen:**: La entidad debe publicar información sobre horarios y días de atención al público de la entidad y de sus divisiones o sucursales en diferentes medios: en la sede, teléfono, correo electrónico, etc.

La entidade debe publica información sobre horarios y días de atención al público de la entidad y sus divisiones en diferentes medios: en la sede, teléfono, correo electrónico, etc. Enlace a los datos de contacto de las sucursales que tenga el sujeto obligado.

#### 6.5.1. Criterio de Éxito - Nivel A

Texto disponible en página específica, accesible por elemento de navegación principal o en el cuerpo de la capa de sesión, incluye horarios de atención de diferentes departamentos o sedes.

#### 6.5.2. Criterio de Éxito - Nivel AA

Texto disponible en página específica, accesible por elemento de navegación principal o en el cuerpo de la capa de sesión, incluye horarios de atención de diferentes departamentos o sedes. Horarios más importante de la sede o servicio principal también disponible en pié de página de todas las páginas.

#### 6.5.3. Criterio de Éxito - Nivel AAA

Texto disponible en página específica, incluye horarios de atención de diferentes departamentos o sedes. Horarios más importante de la sede o servicio principal también disponible en pie de página de todas las páginas. En los dos casos, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org.

### 6.6. Presupuesto general
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal b).
Resolución 3564 de 2015, anexo 1, punto 5.1.

> **Resumen:** El presupuesto de la entidad para la respectiva vigencia debe estar disponible para verificación del público. Puede ser el presupuesto inicial o final. Eo presupuesto debe ofrecer datos (valores, ingresos, gastos) de forma clara, organizada y desagregada. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica su presupuesto general para cada año fiscal. Puede ser el presupuesto inicial o final. El presupuesto debe ofrecer datos (valores, ingresos, gastos) de forma clara, organizada y debe estar desagregado conforme se describe a continuación, con encabezados o títulos en paréntesis:

- Ingresos presupuestarios (Ingresos);
- Gastos de personal (Gastos);
- Bienes y servicios de consumo;
- Adquisición de activos no financieros;
- Edificios, mobiliarios y otros;
- Equipos informáticos;
- Programas informáticos;
- Actualizado hasta el último trimestre concluido;

Para las entidades u organismos de la Rama Judicial, el requisito tambíen se entenderá cumplido si los requisitos descritos anteriormente están disponibles, a través de un enlace directo, en el sitio web del Consejo Superior de la Judicatura.

#### 6.6.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.6.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos del tipo hoja de cálculo, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. El archivo sigue el patrón del modelo de archivo Datos Presupuestales disponible en la base de patrones MOTA.

#### 6.6.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.7. Ejecución histórica anual
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal b).
Resolución 3564 de 2015, anexo 1, punto 5.2.

> **Resumen:** El sujeto obligado publica la información histórica detallada de la ejecución presupuestal aprobada y ejecutada de ingresos y gastos anuales, idealmente con porcentajes de ejecución. Debe ofrecer datos (gastos, valores, ingresos) de forma clara y organizada. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica la información histórica detallada de la ejecución presupuestal aprobada y ejecutada de ingresos y gastos anuales. La información que reposa debe ser al menos de los últimos dos (2) años anteriores al año en ejercicio, con corte a diciembre del período respectivo y debe ser acorde con el reporte enviado al Sistema Integrado de Información Financiera (SIIF), para lo sujetos que aplique.  Los datos pueden ser agregados mensualmente o trimestralmente, idealmente con porcentajes de ejecución, y deben ofrecer datos (gastos, valores, ingresos) de forma clara, organizada y encontrarse desagregados conforme se describe a continuación, con encabezados o títulos en paréntesis:

- Ingresos presupuestarios (Ingresos);
- Gastos de personal (Gastos);
- Bienes y servicios de consumo;
- Adquisición de activos no financieros;
- Edificios, mobiliarios y otros;
- Equipos informáticos;
- Programas informáticos;
- Actualizado hasta el último trimestre concluido;

En la base de patrones MOTA, presentamos modelos de archivo "Ejecución Presupuestal Mensual" y "Ejecución Presupuestal Trimestral", que cumplen con los requisitos y buenas prácticas aquí mencionadas.

Para las entidades u organismos de la Rama Judicial, el requisito tambíen se entenderá cumplido si los requisitos descritos anteriormente están disponibles, a través de un enlace directo, en el sitio web del Consejo Superior de la Judicatura.

#### 6.7.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.7.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.7.3. Criterio de Éxito - Nivel AAA

Información disponibles en la página, estructurada semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.8. Planes de gasto público por año fiscal
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal b).
Resolución 3564 de 2015, anexo 1, punto 6.2.
Ley 1474 de 2011, artículo 74.

> **Resumem:** El sujeto obligado publica su plan de gasto público para cada año fiscal, en el cual se especifican los objetivos, las estrategias, los proyectos, las metas, los responsables, los planes generales de compras y la distribución presupuestal de sus proyectos de inversión junto a los indicadores de gestión. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica su plan de gasto público para cada año fiscal, en el cual se especifican los objetivos, las estrategias, los proyectos, las metas, los responsables, los planes generales de compras y la distribución presupuestal de sus proyectos de inversión junto a los indicadores de gestión. Asimismo, el plan deberá estar acompañado del informe de gestión del año inmediatamente anterior.

Para las entidades u organismos de la Rama Judicial, el requisito tambíen se entenderá cumplido si los requisitos descritos anteriormente están disponibles, a través de un enlace directo, en el sitio web del Consejo Superior de la Judicatura.

#### 6.8.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.8.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.8.3. Criterio de Éxito - Nivel AAA

Información disponibles en la página, estructurada semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.9. Directorio de servidores públicos, empleados (i.e. funcionários)
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal c) y parágrafo 2.
Decreto 103 de 2015, artículo 5.
Resolución 3564 de 2015, anexo 1, punto 3.5.

> **Resumen:** El sujeto obligado publica en formato accesible y reutilizable el directorio de información de los servidores públicos empleados, incluyendo aquellos que laboran en las sedes, áreas, divisiones, departamentos y/o regionales.

El sujeto obligado publica en formato accesible y reutilizable el directorio de información de los servidores públicos empleados, incluyendo aquellos que laboran en las sedes, áreas, divisiones, departamentos y/o regionales, según corresponda, con la siguiente información:

- Nombres y apellidos completos
- País, Departamento y Ciudad de nacimiento
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades)
- Experiencia laboral y profesional
  - Nombres específicos de empleadores previos
  - Cargos anteriores
  - Fecha de inicio y fin en cada cargo
- Empleo, cargo o actividad que desempeña
- Dependencia en la que presta sus servicios en la entidad o institución
- Dirección de correo electrónico institucional
- Teléfono institucional y extensión
- Escala salarial según las categorías para servidores públicos

#### 6.9.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) . Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

Alternativamente el requisito se entenderá cumplido a través de un enlace a la página de la información que contiene el directorio en el Sistema de Información de Empleo Público (SIGEP).

#### 6.9.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

En caso de que el directorio no contenga alguna de las informaciones requeridas (e.g. no hay correo electrónico), el grado de calificación será disminuido al grado anterior. Es decir, el puntaje obtenido será A y no AA.

#### 6.9.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

En caso de que el directorio no contenga alguna de las informaciones requeridas (e.g. no hay correo electrónico), el grado de calificación será disminuido al grado anterior. Es decir, el puntaje obtenido será AA y no AAA.


### 6.10. Directorio de servidores públicos contratistas
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal c) y parágrafo 2.
Decreto 103 de 2015, artículo 5.
Resolución 3564 de 2015, anexo 1, punto 3.5.

> **Resumen:** El sujeto obligado publica en formato accesible y reutilizable el directorio de información de los servidores públicos contratistas (incluyendo el objeto del contrato), incluyendo aquellos que laboran en las sedes, áreas, divisiones, departamentos y/o regionales.

El sujeto obligado publica en formato accesible y reutilizable el directorio de información de los servidores públicos contratistas, incluyendo aquellos que laboran en las sedes, áreas, divisiones, departamentos y/o regionales, según corresponda, con la siguiente información:

- Nombres y apellidos completos
- País, Departamento y Ciudad de nacimiento
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades)
- Experiencia laboral y profesional
  - Nombres específicos de empleadores previos
  - Cargos anteriores
  - Fecha de inicio y fin en cada cargo
- Cargo y el rol que desempeña con base en el objeto contractual
- Dependencia en la que presta sus servicios en la entidad o institución
- Dirección de correo electrónico institucional
- Teléfono institucional y extensión
- Escala salarial según las categorías para empleados del sector privado
- Objeto, valor total de los honorarios, fecha de inicio y de terminación de contratos de prestación de servicios

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 6.10.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Alternativamente, un enlace al SIGEP es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

#### 6.10.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

En caso de que el directorio no contenga alguna de las informaciones requeridas (e.g. no hay correo electrónico), el grado de calificación será disminuido al grado anterior. Es decir, el puntaje obtenido será A y no AA.

#### 6.10.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

En caso de que el directorio no contenga alguna de las informaciones requeridas (e.g. no hay correo electrónico), el grado de calificación será disminuido al grado anterior. Es decir, el puntaje obtenido será AA y no AAA.

### 6.11. Escalas salariales
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal c).
Resolución 3564 de 2015, anexo 1, punto 3.5.

> **Resumen:** Es posible encontrar una tabla con los rangos de salarios de la entidad, identificado por el título "Rangos de salario por nivel", y el decreto de asignaciones salariales de la entidad en un lugar visible. Preferiblemente en dos formatos: página web y archivos en formato estructurado y abierto.

Es posible encontrar una tabla con los rangos de salarios de la entidad, identificado por el título "Rangos de salario por nivel", y el decreto de asignaciones salariales de la entidad en un lugar visible.

La tabla debe estar actualizada al menos al último año concluido y contener información sobre el salario base por jerarquía y/o categoría ocupacional, de acuerdo con la categoría, tipo y otras especificidades de la entidad. Ejemplo, en el sitio web de la Fiscalía General de la Nación se espera encontrar datos separados por jerarquía y/o categoría de fiscales y también por jerarquía y/o categoría ocupacional de otros funcionarios no fiscales.

**Importante:** si los datos están solamente en otros sitios (e.g. SECOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 6.11.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 6.11.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.11.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.12. Sanciones aplicadas a servidores públicos
Tipo: OBLIGACIÓN

> **Resumen:** Es posible encontrar información sobre sanciones disciplinarias o de otro tipo que hayan sido impuestas a funcionarios de la entidad, así como estadísticas sobre las sanciones impuestas. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

Es posible encontrar información sobre sanciones disciplinarias o de otro tipo que hayan sido impuestas a funcionarios de la entidad. Hay estadísticas sobre las sanciones impuestas, actualizadas hasta el último año concluido y se encuentran desagregadas según el tipo de funcionario (e.g. en el sitio web de la Fiscalía General de la Nación la información debe estar desagregadas entre fiscales y otros cargos).

#### 6.12.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.12.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.12.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquemas [Report](https://schema.org/Report), [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.13. Información de contratos
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal c).
Resolución 3564 de 2015, anexo 1, punto 3.5.

> **Resumen:** Es posible encontrar información sobre los contratos realizados por la entidad, disponible en formatos abiertos. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

Es posible encontrar información sobre los contratos realizados por la entidad, disponible en formatos abiertos. Alternativamente, un enlace al SIGEP es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 6.13.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

#### 6.13.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 6.13.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

### 6.14. Normas generales
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 4.

> **Resumen:** El sujeto obligado publica la normatividad de orden constitucional o legal que lo rige, que determina su competencia y le es aplicable a su actividad, en una sección con normas y reglamentos pertinentes para la entidad: decretos, circulares, leyes, etc.

El sujeto obligado publica la normatividad de orden constitucional o legal que lo rige, que determina su competencia y le es aplicable a su actividad, en una sección con normas y reglamentos pertinentes para la entidad: decretos, circulares, leyes, etc., relativas a creacción de reglamentos de la entidad. Idealmente, dos versiones están disponibles:

- Listado de normas de orden constitucional o legal que indique nombre, fecha de expedición y una descripción corta de la misma, organizadas de la más reciente a la más antigua.
- Un enlace que redirija al usuario a un archivo o recurso con el documento integral.

#### 6.14.1. Criterio de Éxito - Nivel A

Resumen disponible en la página en HTML. Con normas disponibles para bajar en formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.14.2. Criterio de Éxito - Nivel AA

Resumen disponible en la página en HTML, en lenguaje sencillo, con normas completas disponibles también en HTML en la misma página o en otra página en el mismo sitio. Para las normas completas, archivos en formatos abiertos (e.g. odf) accesibles en el mismo sitio y dominio es válido. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.14.3. Criterio de Éxito - Nivel AAA

Resumen disponible en la página, en HTML, en lenguaje sencillo, con normas completas disponibles también en HTML en la misma página o en otra página en el mismo sitio. En los dos casos, el contenido es estructurado semánticamente (i.e. elementos HTML5 apropiados) y sus meta-datos disponibles en sintaxis LD+JSON y vocabulario schema.org segundo esquema [legislation](https://schema.org/Legislation) y [LegislationObject](https://schema.org/LegislationObject). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.15. Normas Reglamentarias
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 4.

> **Resumen:** La entidad publica el decreto único reglamentario sectorial, que compila todas las normas reglamentarias vigentes del sector administrativo del que hace parte. Por medio de este decreto se debe generar el acceso a las normas compiladas a través de hipervínculos. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica el decreto único reglamentario sectorial, que compila todas las normas reglamentarias vigentes del sector administrativo del que hace parte. Por medio de este decreto se debe generar el acceso a las normas compiladas a través de hipervínculos. Esta información debe ser descargable y en un formato que facilite la búsqueda del texto dentro del documento, así como su continua actualización. Asimismo, el sujeto obligado agrega a través de hipervínculos la referencia a todos los actos que adicionen, modifiquen o deroguen cualquiera de las disposiciones del decreto único reglamentario sectorial, así como a las decisiones judiciales que declaren la nulidad de apartes del decreto.

Además, se publican los decretos no compilados, como los de estructura, salarios, decretos que desarrollan leyes marco, entre otros. Esta información debe ser descargable.

Asimismo, si existen resoluciones, circulares u otro tipo de actos administrativos de terceros o que produce el mismo sujeto obligado para el desarrollo de sus funciones, se publica en dos versiones:
- un listado que indique el tipo de acto (resolución, circular, ordenanza, acuerdo, etc.), la fecha de expedición y una descripción corta del mismo (verbatim), organizados del más reciente al más antiguo.
- un enlace que redirija al usuario a un archivo o recurso con el documento integral.

 Existencia de información sobre normas reglamentarias pertinentes a la entidad: resoluciones y directivas.Dos están disponibles:

- Resumen en lenguaje sencillo, destacando secciones de reglamentos pertinentes;
- Copias literales de las normas.
  - En casos de documentos largos y cuyo alcance exceda el tema de Normas generales, está permitido copias verbatim de apenas las seccionespertinentes, pero es necesario un enlace que redirija al usuario a un archivo o recurso con el documento integral.

#### 6.15.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.15.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.15.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.16.
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.1.
Ley 1474 de 2011, artículo 73.

> **Resumen:** El sujeto obligado publica sus lineamientos, manuales y toda política que haya adoptado y afecte al público, junto con sus fundamentos y toda interpretación autorizada de ellas. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica sus lineamientos, manuales y toda política que haya adoptado y afecte al público, junto con sus fundamentos y toda interpretación autorizada de ellas. Entre las políticas, lineamientos y manuales pueden estar (lista ilustrativa, no taxativa):

- Políticas y lineamientos sectoriales e institucionales.
- Manuales.
- Planes estratégicos, sectoriales e institucionales.
- Plan de rendición de cuentas.
- Plan de servicio al ciudadano.
- Plan anticorrupción.

Si el sujeto obligado realiza un plan de acción unificado, es válido.


#### 6.16.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.16.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.16.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org según esquema. [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.17. Metas y Objetivos
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.4.

> **Resumen:** La entidad y sus unidades administrativas publican la información relacionada con sus metas y objetivos, de conformidad con sus programas operativos y los demás planes exigidos. También publica su estado de avance, mínimo cada tres (3) meses. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado y sus unidades administrativas publican la información relacionada con sus metas y objetivos, de conformidad con sus programas operativos y los demás planes exigidos por la normatividad.

Se debe publicar su estado de avance, mínimo cada tres (3) meses.

#### 6.17.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.17.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.17.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.18. Indicadores de gestión y/o desempeño
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.4.

> **Resumen:** La entidad publica información sobre los indicadores de gestión o desempeño que utiliza, así como reportes con estadísticas y análisis del desempeño en relación con sus programas operativos y los demás planes. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

Las entidades deben proveer información sobre los indicadores de gestión y/o desempeño que utilizan, deben publicar también reportes con estadísticas y análisis del desempeño de la entidad en relación con sus programas operativos y los demás planes exigidos por la normatividad.

#### 6.18.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.18.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.18.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.19. Plan anticorrupción y de atención al ciudadano
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal g).
Ley 1474 de 2011, artículo 73.

> **Resumen:** El sujeto obligado publica anualmente una estrategia de lucha contra la corrupción y de atención al ciudadano. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica anualmente una estrategia de lucha contra la corrupción y de atención al ciudadano. Dicha estrategia contempla, entre otras cosas:
- el mapa de riesgos de corrupción en la respectiva entidad;
- las medidas concretas para mitigar esos riesgos;
- las estrategias anticorrupción;
- los mecanismos para mejorar la atención al ciudadano.


#### 6.19.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.19.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.19.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.20. Plan anual de compras y adquisiciones
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 9, literal e).
Decreto 103 de 2015, artículo 10.
Resolución 3564 de 2015, anexo 1, punto 8.4.
Ley 1474 de 2011, artículo 74.
Decreto 1510 de 2013, artículos 3, 4, 5, 6 y 7.

> **Resumen:** La entidad publica en su sitio web y en el sistema SECOP su plan general de compras, entendido como un instrumento de planeación contractual que las entidades estatales deben diligenciar, publicar y actualizar por lo menos una vez durante su vigencia y hacer ajustes según lo establecido en la ley y otras normativas. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado que contrata con cargo a recursos públicos publica en su sitio web y en el Sistema Electrónico de Contratación Pública (SECOP) su plan general de compras, entendido como un instrumento de planeación contractual que las entidades estatales deben diligenciar, publicar y actualizar por lo menos una vez durante su vigencia y: (i) cuando haya ajustes en los cronogramas de adquisición, valores, modalidad de selección, origen de los recursos; (ii) para incluir nuevas obras, bienes y/o servicios; (iii) excluir obras, bienes y/o servicios; o (iv) modificar el presupuesto anual de adquisiciones. El plan debe compreender:

- La lista de bienes, obras y servicios que se pretenden adquirir durante el año.
- La necesidad ( y cuando conoce el bien, obra o servicio que satisface esa necesidad debe identificarlo utilizando el clasificador de bienes y servicios)
- El valor estimado del contrato
- El tipo de recursos con cargo a los cuales la entidad estatal pagará el bien, obra o servicio
- La modalidad de selección del contratista
- La fecha aproximada en la cual la entidad estatal iniciará el proceso de contratación. - Proceso de gestión contractual / Procedimiento plan anual de adquisiciones


#### 6.20.1. Criterio de Éxito - Nivel A

Información disponible en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf), con links al SECOP. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.20.2. Criterio de Éxito - Nivel AA

Contenido del Plan disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 6.20.3. Criterio de Éxito - Nivel AAA
Proceso de Gestión Contractual y lista de documentos disponibles en la página, estructurados semánticamente (i.e. elementos HTML5 apropiados), información de contratos disponible en archivos, en formatos abiertos (e.g. .odf), incluyendo links para el SECOP. Meta-dados de la colección de documentos contienen nombre del documento, autor, data de actualización, URI y enlace para el SECOP) en sintaxis LD+JSON y vocabulario schema.org según esquema [Collection](https://schema.org/Collection), [DigitalDocument](https://schema.org/DigitalDocument) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

## 7. Información mínima obligatoria respecto a servicios, procedimientos y funcionamiento

Información mínima obligatoria respecto a servicios, procedimientos y funcionamiento, de acuerdo con el artículo 11 de la Ley 1712 de 2014.

### 7.1. Servicios
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal a).
Decreto 103 de 2015, artículo 6.
Resolución 3564 de 2015, anexo 1, punto 9.

> **Resumen:** El sitio web de la entidad  contiene una o más páginas con información de los servicios que brinda directamente al público, incluyendo i) normas ii) formularios y formatos y iii) protocolos de atención a diferentes públicos. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sitio web del sujeto obligado contiene una o más páginas con información de los servicios que brinda directamente al público, incluyendo:
- La norma que los sustenta
- Proceso a seguir
- Costos asociados
- Formularios y formatos requeridos
- Protocolos de atención a los siguientes públicos: 1) Ciudadanos en general; 2) Prensa; 3) grupos de interés, según la entidad.
- Indicación de aquellos que se encuentren disponibles en línea.


#### 7.1.1. Criterio de Éxito - Nivel A

Información disponibles en una o más páginas interligadas, en HTML, con modelos de formularios y formatos disponibles en archivos (e.g. .pdf, .xlsx, o .docx). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.1.2. Criterio de Éxito - Nivel AA

Información disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.1.3. Criterio de Éxito - Nivel AAA

Información disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Información también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.2. Trámites
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal b).
Decreto 103 de 2015, artículo 6.
Resolución 3564 de 2015, anexo 1, punto 9.

> **Resumen:** El sitio web contiene información de los trámites que se pueden agotar en la entidad, incluyendo i) normativa(s) relacionada(s); ii) proceso a seguir, incluso formularios y formatos; iii) costos asociados; y iv) aquellos que se encuentren disponibles en línea. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica toda la información correspondiente a los trámites que se pueden agotar en la entidad, incluyendo:
- La norma que los sustenta
- Proceso a seguir
- Costos asociados
- Formularios y formatos requeridos
- Indicación de aquellos que se encuentren disponibles en línea.

Además de la información de cada trámite, se recomienda una tabla resumen en la que se enlisten costos, normatividad aplicable y links que detallen cada trámite.

Este requisito se entenderá cumplido con la inscripción de los trámites en el Sistema Único de Información de Trámites y Procedimientos Administrativos (SUIT) y la relación de los nombres de los mismos en el respectivo sitio web oficial del sujeto obligado con un enlace al portal del Estado Colombiano o el que haga sus veces.

#### 7.2.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, en HTML, con modelos de formularios y formatos disponibles en archivos (e.g. .pdf, xlsx, o .docx). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.


#### 7.2.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), incluso una tabla resumen en la que se enlisten costos, normatividad aplicable y links que detallen cada trámite. Incluye modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.2.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), incluso una tabla resumen en la que se enlisten costos, normatividad aplicable y links que detallen cada trámite, y modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Información también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.3. Procedimientos de toma de decisiones
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal c).
Resolución 3564 de 2015, anexo 1, punto 3.3.

> **Resumen:** El sitio web de la entidad contiene la descripción de los procesos y procedimientos que se siguen para tomar decisiones en las diferentes áreas. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica en su sitio la descripción de los procesos y procedimientos que se siguen para tomar decisiones en las diferentes áreas.

Ejemplo: Procedimientos mínimos Fiscalía General de la Nación:

1. Investigación de conductas punibles
2. Acusación de presuntos infractores de la ley ante juzgados y tribunales competentes
3. Coordinación de las funciones de policía judicial
4. Creación o supresión de direcciones de la Fiscalía
5. Decisiones sobre protección a víctimas
6. Decisiones sobre política criminal

#### 7.3.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necesario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.3.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.3.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Información también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.4. Decisiones
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal d).

> **Resumen:** En el sitio web de la entidad se encuentra publicado los contenidos de las decisiones adoptadas que afecten al público, junto con sus fundamentos e interpretaciones. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica en su sitio web los contenidos de las decisiones adoptadas que afecten al público, junto con sus fundamentos e interpretaciones.

Ejemplo: listado de decisiones mínimas que debe contener el sitio web de la Corte Constitucional:

1. Sentencias de tutela
2. Sentencias de constitucionalidad
3. Autos
4. Acuerdos de Sala Plena
5. Respuesta a peticiones de ciudadanos con identidad de objeto

Además de la publicación de información acerca cada decisión, se recomienda una tabla o listado de decisiones organizadas de forma cronológica de la más reciente a la más antigua (i.e. las decisiones más recientes al principio de la lista).

#### 7.4.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.4.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Información también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.5. Políticas
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.1.

> **Resumen:** La entidad publica en su sitio web las políticas adoptadas que afecten al público, junto con sus fundamentos e interpretaciones. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica en su sitio web los contenidos de las decisiones adoptadas que afecten al público, junto con sus fundamentos e interpretaciones.

Ejemplo: listado de políticas mínimas que debe contener el sitio web de la Fiscalía General de la Nación:

1. Política pública de priorización.
   1. Incluso criterios de priorización.
2. Políticas en materia de internacionalización para afrontar transnacionalidad de delitos.
3. Políticas de adopción y aplicación de enfoques diferenciales.
4. Políticas sobre investigación de crimen organizado.
5. Resultados de las políticas adoptadas.
   1.  Incluso resultados y casos emblemáticos.

Además de la información acerca cada política, se recomienda una tabla o listado de políticas organizadas de forma cronológica de la más reciente a la más antigua (i.e. las decisiones más recientes al principio de la lista).

#### 7.5.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillp. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.5.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.5.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Información también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.6. Mecanismos de participación ciudadana
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal h).
Resolución 3564 de 2015, anexo 1, puntos 1.1, 2.4 y 10.9, y anexo 2.

> **Resumen:** El sitio de la entidad debe ofrecer mecanismos de presentación directa de solicitudes, quejas, denuncias y reclamos a disposición del público: teléfonos fijos y móviles, con líneas gratuitas y fax, correo electrónico institucional, correo físico o postal, formulario electrónico de solicitudes, peticiones, quejas, reclamos.

El sujeto obligado dispone de canales para la atención al ciudadano y para recibir peticiones, quejas, reclamos, denuncias y solicitudes de información pública, tales como:
Teléfonos fijos y móviles, con líneas gratuitas y fax, incluyendo el indicativo nacional e internacional en el formato (+57 número del área respectiva).
Correo electrónico institucional para la recepción de solicitudes de información.
Correo físico o postal para la recepción de solicitudes de información.
Link al formulario electrónico de solicitudes, peticiones, quejas, reclamos.

Además, el sujeto obligado ofrece una lista de preguntas frecuentes con las respectivas respuestas, relacionadas con su gestión y los servicios y trámites que presta en páginas web.


#### 7.6.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.6.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

En caso de un gran número de preguntas frequentes, un formulario de búsqueda debe estar presente.

#### 7.6.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf).

En caso de un gran número de preguntas frecuentes, un formulario de búsqueda debe estar presente.

Información disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.7. Informe de participación ciudadana
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal h).
Decreto 103 de 2015, artículo 52.
Resolución 3564 de 2015, anexo 1, punto 10.10.

> **Resumen:** El sitio de la entidad debe contener un informe de todas las peticiones, quejas, reclamos, denuncias y solicitudes de acceso a información pública recibidas, los tiempos de respuesta del sujeto obligado y un análisis resumido de este tema. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica un informe de todas las peticiones, quejas, reclamos, denuncias y solicitudes de acceso a información pública recibidas, los tiempos de respuesta del sujeto obligado y un análisis resumido de este tema. Respecto de las solicitudes de acceso a información pública, el informe debe discriminar la siguiente información mínima agregada:

- El número de solicitudes recibidas.
- El número de solicitudes que fueron trasladadas a otra institución.
- El tiempo de respuesta a cada solicitud.
- El número de solicitudes en las que se negó el acceso a la información.


#### 7.7.1. Criterio de Éxito - Nivel A

Estadísticas agregadas y análisis disponibles en una o más páginas estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en un archivo .xls o .xlsx.

#### 7.7.2. Criterio de Éxito - Nivel AA

Estadísticas agregadas y análisis disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en archivos con formatos abiertos (.csv o .odf).

#### 7.7.3. Criterio de Éxito - Nivel AAA

Estadísticas agregadas y análisis disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con descripciónes textuales en lenguaje sencillo. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en archivos con formatos abiertos (.csv o .odf) y también como meta-datos en sintaxis LD+JSON y vocabulario schema.org.

### 7.8. Mecanismos de participación ciudadana en formulación de políticas
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal i).
Decreto 103 de 2015, artículo 15.
Resolución 3564 de 2015, anexo 1, punto 6.5.

> **Resumen:** El sitio de la entidad debe contener información sobre todo mecanismo o procedimiento al que deben sujetarse los ciudadanos, usuarios o interesados en participar en la formulación de la política, en el ejercicio de las facultades de ese sujeto obligado, o en el control o evaluación de la gestión institucional. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica información sobre todo mecanismo o procedimiento al que deben sujetarse los ciudadanos, usuarios o interesados en participar en la formulación de la política, en el ejercicio de las facultades de ese sujeto obligado, o en el control o evaluación de la gestión institucional, indicando:
- Los sujetos que pueden participar
- Los medios presenciales y electrónicos
- Las áreas responsables de la orientación y vigilancia para su cumplimiento.
Este ítem incluye la publicidad de invitaciones públicas, convocatorias o procesos de participación pública.

#### 7.8.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.8.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

#### 7.8.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos formatos abiertos (e.g. .odf). Información también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.9. Informes de gestión, evaluación y auditoría
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal e).
Resolución 3564 de 2015, anexo 1, punto 7.1.

> **Resumen:** La entidad publica todos los informes de gestión, evaluación y auditoría: Informe enviado al Congreso / Asamblea / Consejo; Informe de rendición de la cuenta fiscal; Informe de rendición de cuentas a los ciudadanos; Informes a organismos de inspección, vigilancia y control; Informe de la auditoría al ejercicio presupuestal. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica todos los informes de gestión, evaluación y auditoría. Para los sujetos obligados que aplique. Como mínimo, deben publicar -dentro del mes en el que se envió o realizó el evento, según corresponda- los siguientes informes:

- Informe enviado al Congreso / Asamblea / Consejo.
- Informe de rendición de la cuenta fiscal a la Contraloría General de la República o a las Contralorías Territoriales, según corresponda.
- Informe de rendición de cuentas a los ciudadanos, incluyendo la respuesta a las solicitudes de los ciudadanos antes y durante el ejercicio de rendición.
- Informes a organismos de inspección, vigilancia y control. Informe de la auditoría al ejercicio presupuestal.

**Nota:** Idealmente, los informes deben ser presentados en dos formatos: página web y archivos en formato estructurado y abierto. Cada uno de los informes mencionados se evalúa por separado, como se describe a continuación.

#### 7.9.1 Informes de gestión
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal e).
Resolución 3564 de 2015, anexo 1, punto 7.1.

> **Resumen:** La entidad publica todos los informes de gestión enviado al Congreso / Asamblea / Consejo. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica todos los informes de gestión enviado al Congreso / Asamblea / Consejo, dentro del mes en el que se envió o realizó el evento. Idealmente, los informes deben ser presentados en dos formatos: página web y archivos en formato estructurado y abierto.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

##### 7.9.1.1 Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Alternativamente, un enlace a sitios externos (e.g. SIGEP, SECOP, es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente una página la información disponible o el archivo.

##### 7.9.1.2 Criterio de Éxito - Nivel AA
Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

##### 7.9.1.3 Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

#### 7.9.2 Informe de rendición de la cuenta fiscal
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal e).
Resolución 3564 de 2015, anexo 1, punto 7.1.

> **Resumen:** La entidad publica todos los informes de rendición de la cuenta fiscal a la Contraloría General de la República o a las Contralorías Territoriales, según corresponda. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica todos los informes de rendición de la cuenta fiscal a la Contraloría General de la República o a las Contralorías Territoriales, según corresponda, dentro del mes en el que se envió o realizó el evento. Idealmente, los informes deben ser presentados en dos formatos: página web y archivos en formato estructurado y abierto.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

##### 7.9.2.1 Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Alternativamente, un enlace a sitios externos (e.g. SIGEP, SECOP, es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente una página la información disponible o el archivo.

##### 7.9.2.2 Criterio de Éxito - Nivel AA
Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

##### 7.9.2.3 Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

#### 7.9.3 Informe de rendición de cuentas a los ciudadanos
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal e).
Resolución 3564 de 2015, anexo 1, punto 7.1.

> **Resumen:** La entidad publica todos los informes de rendición de cuentas a los ciudadanos, incluyendo la respuesta a las solicitudes de los ciudadanos antes y durante el ejercicio de rendición. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica todos los informes de rendición de la cuenta fiscal a la Contraloría General de la República o a las Contralorías Territoriales, según corresponda, dentro del mes en el que se envió o realizó el evento. Idealmente, los informes deben ser presentados en dos formatos: página web y archivos en formato estructurado y abierto.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

##### 7.9.3.1 Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Alternativamente, un enlace a sitios externos (e.g. SIGEP, SECOP, es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente una página la información disponible o el archivo.

##### 7.9.3.2 Criterio de Éxito - Nivel AA
Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

##### 7.9.3.3 Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

#### 7.9.4 Informes de auditoría
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal e).
Resolución 3564 de 2015, anexo 1, punto 7.1.

> **Resumen:** La entidad publica todos los informes de la auditoría al ejercicio presupuestal enviados a organismos de inspección, vigilancia y control. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica todos los informes a organismos de inspección, vigilancia y control -Informe de la auditoría al ejercicio presupuestal-, dentro del mes en el que se envió o realizó el evento. Idealmente, los informes deben ser presentados en dos formatos: página web y archivos en formato estructurado y abierto.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

##### 7.9.4.1 Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión. Alternativamente, un enlace a sitios externos (e.g. SIGEP, SECOP, es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente una página la información disponible o el archivo.

##### 7.9.4.2 Criterio de Éxito - Nivel AA
Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión.

##### 7.9.4.3 Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.10. Mecanismos internos de supervisión
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 10, literal d) y artículo 11, literal f).
Resolución 3564 de 2015, anexo 1, puntos 7.2, 7.3, y 7.4.

> **Resumen:** La entidad publica información relacionada con los informes, planes de mejoramiento, entes y mecanismos de supervisión y control que existen al interior del sujeto obligado, incluyendo como mínimo: ente de control interno que vigila al sujeto obligado y reportes de control interno. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica información relacionada con los informes, planes de mejoramiento, entes y mecanismos de supervisión y control que existen al interior del sujeto obligado, incluyendo como mínimo:

Ente de control interno que vigila al sujeto obligado: El sitio web de la entidad contiene una o más páginas con información acerca de la Oficina de Control Interno, de manera que los funcionarios o la ciudadanía tengan claro que hay una dependencia a la que se puede acudir para presentar denuncias u observaciones acerca del funcionamiento interno de la entidad. En este sentido, se puede encontrar información sobre las funciones (la misión o los objetivos), los procesos ( cómo se hace efectiva una sanción, entre otros.) o mecanismos (que instrumentos de denuncia tienen) de la Oficina. También es útil información que explique la diferencia entre el control interno disciplinario y el control interno de gestión.

Reportes de control interno: el sujeto obligado publica como mínimo el informe pormenorizado del estado del control interno. Dicho informe se debe publicar cada cuatro (4) meses. Planes de mejoramiento: el sujeto obligado publica los planes de mejoramiento vigentes exigidos por el ente de control interno.

#### 7.10.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.10.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.10.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.11. Mecanismos externos de supervisión
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 10, literal d) y artículo 11, literal f).
Resolución 3564 de 2015, anexo 1, puntos 7.3 y 7.4.

> **Resumen:** La entidad publica información relacionada con los informes, planes de mejoramiento, entes y mecanismos de supervisión y control externo, incluyendo como mínimo: Entes de control externo que vigilan al sujeto obligado,  mecanismos de supervisión y la manera como un particular puede comunicar una irregularidad ante los entes que ejercen supervisión y control. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sujeto obligado publica información relacionada con los informes, planes de mejoramiento, entes y mecanismos de supervisión y control externo, incluyendo como mínimo:

Entes de control externo que vigilan al sujeto obligado y mecanismos de supervisión: el sujeto obligado publica la relación de todas las entidades que lo vigilan y de los mecanismos externos de supervisión, notificación y vigilancia pertinente que existen frente al sujeto obligado. Para ello se debe indicar como mínimo:

- Tipo de control que se ejecuta (e.g. fiscal, disciplinario, político, social, etc.)
- Planes de mejoramiento: el sujeto obligado publica los planes de mejoramiento vigentes exigidos por entes de control externo. Asimismo, cuenta con un enlace al sitio web del organismo de control en donde se encuentren los informes que éste ha elaborado sobre el respectivo sujeto obligado.

El sujeto obligado informa sobre la manera como un particular puede comunicar una irregularidad ante los entes que ejercen supervisión y control sobre el sujeto obligado.

#### 7.11.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.11.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.11.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.12. Correo electrónico para notificaciones judiciales
Tipo: OBLIGACIÓN.
Resolución 3564 de 2015, anexo 1, punto 1.3.

> **Resumen:** La entidad publica la dirección de correo electrónico para notificaciones judiciales. Idealmente en el pie de página de todas las páginas del sitio web, y al menos en la página principal del sitio web del sujeto obligado así como en la sección de atención al ciudadano.

El sujeto obligado publica la dirección de correo electrónico para notificaciones judiciales, la cual debe estar disponible en el pie de página de la página principal del sitio web del sujeto obligado, así como en la sección de atención al ciudadano. El correo para notificaciones judiciales debe estar configurado de forma tal que envíe acuse de recibo al remitente de forma automática.

#### 7.12.2. Criterio de Éxito - Nivel A
Información disponibleen el pie de página de la página principal del sitio web (i.e. home) del sujeto obligado, así como en la sección de atención al ciudadano, en formato HTML.

#### 7.12.2. Criterio de Éxito - Nivel AA
Información disponibleen el pie de página  del sujeto obligado, así como en la sección de atención al ciudadano, en formato HTML.

#### 7.12.3. Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org of types [GovernmentOrganization](https://schema.org/GovernmentOrganization) y [ContactPoint](https://schema.org/ContactPoint).

### 7.13. Procedimientos y lineamientos de contratación
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal g).
Resolución 3564 de 2015, anexo 1, punto 8.3.

> **Resumen**: El sitio web de la entidad debe contener información de procedimientos y lineamientos de contratación. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sitio web del sujeto obligado debe contener información de procedimientos y lineamientos de contratación. Documentos ex-ante (de planeación o tipo manual) que den guía sobre cómo se va a proceder para hacer algo), formulado por la entidad. Puede que el que esté disponible haya sido formulado en una vigencia diferente a la actual. Publicación de documentos que den guía sobre cómo se maneja la contratación en la entidad según cada modalidad. En la mayoría de casos, estos lineamientos se consolidan en un documento llamado "Manual de Contratación".

#### 7.13.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.13.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.13.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.14. Políticas en materia de adquisiciones y compras
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 11, literal g).
Resolución 3564 de 2015, anexo 1, punto 8.4.

> **Resumen**: El sitio web de la entidad debe contener información de su plan de adquisiciones: proceso de gestión contractual, plan anual de adquisiciones; datos y processos y ejecución de los contratos. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sitio web del sujeto obligado debe ofrecer información de su plan de adquisiciones. El plan debe compreender:

- Proceso de Gestión Contractual / Procedimiento Plan Anual de Adquisiciones
- Datos/procesos de adjudicación de los contratos
- Datos/procesos de ejecución de los contratos

#### 7.14.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf no-accesible.Información disponible en archivos, formatos propietarios (e.g. .docx, xlsx), pdf no-accesible, con links para SECOP. Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión;

#### 7.14.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.14.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

## 8. Instrumentos de gestión de la información pública

Información respecto a instrumentos de gestión de la información pública requeridos por la Ley 1712 de 2014.

### 8.1. Esquemas de publicación de información
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 12.

> **Resumen:** El sitio de la entidad debe contener una o más páginas con información del Esquemas de Publicación de información, publicada en una página denominada \"Acceso a información pública\". Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sitio web de la entidad debe contener una o más páginas con información de Esquemas de Publicación de información, publicadas en una página denominada "Acceso a información pública"  que incluya: i) qué tipo de información está publicada en el sitio web ii) qué información se publicará de manera proactiva iii) formatos de publicación iv) idioma v) responsable de la producción de información vi) la periodicidad en la divulgación, entre otros.

Un ejemplo de esquema de publicación, en archivo xls, se encuentra en el enlace: https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2

#### 8.1.1. Criterio de Éxito - Nivel A

El sitio ofrece una página e con el título "acceso a información pública", Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf no-accesible. Este archivo contiene una tabla describiendo esquema de publicación de información similar all ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

    Alternativamente, para la tabla un enlace al SIGEP es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 8.1.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados), con el título "acceso a información pública", Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

    Alternativamente, para la tabla un enlace al SIGEP es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

**Importante:** si los datos están solamente en otros sitios (e.g. SICOP, Datos Abiertos, etc), la puntuación es reducida a la mitad.

#### 8.1.3. Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org, según esquema [ItemList](https://schema.org/ItemList)y [DigitalDocument](https://schema.org/DigitalDocument) y relacionados.

### 8.2. Programa de gestión documental
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 15.
Resolución 3564 de 2015, anexo 1, punto 10.5.

> **Resumen:** El sitio de la entidad debe contener una o más páginas con información del Programa de Gestión Documental, publicada en una página denominada \"Gestión Documental\" e informar procedimientos y lineamientos necesarios para la producción, distribución, organización, consulta y conservación de los documentos públicos.

El sitio web de la entidad debe contener una o más páginas con información acerca del Programa de Gestión Documental, publicadas en una página denominada "Gestión Documental" e informar "procedimientos y lineamientos necesarios para la producción, distribución, organización, consulta y conservación de los documentos públicos". Comprende la vida del documento desde su creación hasta su disposición final.

Un ejemplo de Programa de Gestión Documental se encuentra en el enlace: http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

#### 8.2.1. Criterio de Éxito - Nivel A

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados) con el título "Gestión Documental", Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf no-accesible, similar al ejemplo disponible en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

    Alternativamente, para la tabla un enlace a sitios externos (e.g. SIGEP, SECOP, Datos Abiertos) es válido, pero i) sólo si se especifica que ahí se puede entrar y encontrar esta información ii) y cuando se abre el enlace, se abre directamente la tabla con la información disponible.

**Importante:** si los datos están solamente en otros sitios, la puntuación es reducida a la mitad.


#### 8.2.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados), con el título "Programa de Gestión Documental", accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf


#### 8.2.3. Criterio de Éxito - Nivel AAA

Además de conformidad con el nivel AA, la misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org, según esquema [ItemList](https://schema.org/ItemList)y [DigitalDocument](https://schema.org/DigitalDocument) y relacionados.

### 8.3. Tablas de retención documental
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 13.
Resolución 3564 de 2015, anexo 1, punto 10.6.

> **Resumen:** El sitio de la entidad debe contener una o más páginas con información acerca de las Tablas de Retención Documental, en una sección identificada con el nombre \"Transparencia y acceso a información pública\". Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sitio web del sujeto obligado debe contener una o más páginas con información acerca de las Tablas de Retención Documental, en una sección identificada con el nombre "Transparencia y acceso a información pública".

#### 8.3.1. Criterio de Éxito - Nivel A
El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados) con el título "Gestión Documental", Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt, o .pdf escaneado).

#### 8.3.2. Criterio de Éxito - Nivel AA

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "Tabla de retención documental", Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**.

#### 8.3.3. Criterio de Éxito - Nivel AAA

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y en conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "Tabla de retención documental", Accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**.

### 8.4. Respuestas a solicitudes de información recibidas
Tipo: OBLIGACIÓN.
Ley 1712 de 2014, artículo 14

> **Resumen:** El sitio de la entidad debe contener una o más páginas con las respuestas a solicitudes de acceso a información pública anterior a la entrada en vigencia de la Ley 1712 de 2014. Preferencialmente en dos formatos: página web y archivos en formato estructurado y abierto.

El sitio del sujeto obligado debe contener una o más páginas con Respuestas a solicitudes de información recibidas. Cuando se dé respuesta a una de las solicitudes de acceso a información pública anterior a la entrada en vigencia de la Ley 1712 de 2014, esta deberá hacerse pública de manera proactiva en el sitio web del sujeto obligado.

#### 8.4.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) ,accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf non-accesible.


#### 8.4.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia.

También es aceptable archivo de formato abierto (.odf) o **.pdf accesible**.


#### 8.4.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/) accesible por elemento de navegación secundario (i.e. submenu) o en el cuerpo de la capa de sesión transparencia.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**.

Los mismos datos son encontrado como datos estructurados en sintaxis LD+JSON y vocabulario schema.org.
