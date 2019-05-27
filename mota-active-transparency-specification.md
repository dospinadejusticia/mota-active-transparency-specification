# MOTA - Especificación de Transparencia Activa para entidades Gubernamentales 0.2
Borrador de editores 22 Mayo 2019

Esta versión:
    https://github.com/Dejusticia/mota-active-transparency-specification/
Latest published version:
    https://github.com/Dejusticia/mota-active-transparency-specification/
Latest editor's draft:
    https://github.com/Dejusticia/mota-active-transparency-specification/
Editores:
    Celso Bessa (Dejusticia)
    Maria Paula Ángel (Dejusticia)

## Notes

Este documento está escrito utilizando la sintaxis Markdown:

https://www.markdownguide.org/getting-started
https://www.markdownguide.org/basic-syntax

Este documento tiene control de versión inspirado en el sistema de versión semántico de software:
https://semver.org/lang/es/
https://www.celsobessa.com.br/2016/01/05/organizando-os-arquivos/

## AFAZERES en destaque

- especificar LD+JSON em arquivo externo via link element com rel="alternate" e type="application/json" mime-type
- especificar o que é um PDF acessível e melhore práticas para gerá-los. Definir se há diferença entre acessível e machine readable
  - https://helpx.adobe.com/acrobat/using/create-verify-pdf-accessibility.html
  - https://webaim.org/techniques/acrobat/
  - https://webaim.org/techniques/acrobat/converting

## Abstract

Una especificación de los obligaciones y buenas prácticas para publicación y divulgación de información de transparencia activa en Colombia.

Esta documento especifica los criterios, obligaciones legales, estándares y buenas prácticas para publicación y divulgación de información de transparencia en la web de forma más fácil y útil por parte de las entidades gubernamentales en Colombia. También provee una visión general de los objetivos y filosofía de la iniciativa MOTA--Monitoreo de Obligaciones de Transparencia Activa-- que busca incentivar el cumplimiento de la rendición de cuentas en la lucha contra corrupción en Colombia, a saber: la transparencia de la información en formatos abiertos, patronizados y fácilmente legibles por máquinas en los sitios web de los sujetos obligados (información mínima obligatoria de los arts. 9, 10 y 11 de la Ley 1712 de 2014) y la claridad de los procesos de toma de decisiones que allí se exponen.

De hecho, esta especificación es utilizada por otros componentes de la iniciativa, como el robot evaluador de sitios gubernamentales, que por su vez alimenta una base de datos con los resultados de evaluación,  la webapp de evaluación de sitios web gubernamentales y una biblioteca de insumos (ejemplos de códigos, patrones de diseño, modelos de textos, etc). Interdisciplinar -- cubriendo legislación, tecnología, diseño, redacción, ciencia de la información, entre otros --  esta especificación es construida  sobre otras especificaciones, patrones, leyes y otros conjuntos de buenas prácticas incluso, [HTML5](https://w3c.github.io/html/), [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/) [wai-aria-1.2](https://w3c.github.io/aria/), [schema.org](https://schema.org), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) y, como un continuo trabajo en progreso, está sujeta a cambios, perfeccionamientos y extensión. Aunque los principios y criterios principales están bien definidos, criterios secundarios, casos especiales e implementaciones específicas todavía no están adecuadamente escritos o deben ser definidos en otros documentos.

NOTA: Este documento contiene un número grande de informaciones introductorias y contextuales. Tal vez es posible que desee seguir directamente los criterios y ejemplos. Si desea contribuir, vea la sección Cómo Contribuir.

Palabras clave: Rendición de cuentas, Transparencia

## Estado y Tipología del documento

Este documento sigue la metodología [Versionado Semántico (SEMVER)](https://semver.org/lang/es/) para control de versión. También utiliza los valores de la variable [specStatus](https://github.com/w3c/respec/wiki/specStatus) de la herramienta [ReSpec de W3C](https://github.com/w3c/respec/) para determinar el tipo/estado de la especificación.

En la fecha de publicación se encontrará en la versión 0.1.0 y estado Borrador de Editores (ED - Editor's Draft).

Aunque esta especificación fue inspirada por el trabajo de grupos como W3C, la iniciativa MOTA y sus organizadores no  afiliados a estas organizaciones.

- [MOTA - Especificación de Transparencia Activa para entidades Gubernamentales 0.2](#mota---especificaci%C3%B3n-de-transparencia-activa-para-entidades-gubernamentales-02)
  - [Notes](#notes)
  - [AFAZERES en destaque](#afazeres-en-destaque)
  - [Abstract](#abstract)
  - [Estado y Tipología del documento](#estado-y-tipolog%C3%ADa-del-documento)
  - [1. Introducción](#1-introducci%C3%B3n)
    - [1.1 Transparencia, Rendición de Cuentas y lucha contra la corrupción](#11-transparencia-rendici%C3%B3n-de-cuentas-y-lucha-contra-la-corrupci%C3%B3n)
    - [1.2 Público objetivo](#12-p%C3%BAblico-objetivo)
    - [1.3 Filosofía y Presupuestos](#13-filosof%C3%ADa-y-presupuestos)
    - [1.4 Interdisciplinaridad](#14-interdisciplinaridad)
    - [1.5 Regulación](#15-regulaci%C3%B3n)
    - [1.6 Documentos de Apoyo](#16-documentos-de-apoyo)
    - [1.7 Colaboración](#17-colaboraci%C3%B3n)
  - [2. Uso de la especificación](#2-uso-de-la-especificaci%C3%B3n)
  - [3. Conformidad](#3-conformidad)
    - [Herramientas para examen de conformidad](#herramientas-para-examen-de-conformidad)
      - [WCAG2.1](#wcag21)
    - [3.1 Conformidad de Dependencias](#31-conformidad-de-dependencias)
    - [3.4 Conformance Checkers](#34-conformance-checkers)
  - [4. Términos importantes (vocabulario)](#4-t%C3%A9rminos-importantes-vocabulario)
  - [5. Categoría - Disponibilidad de Acceso](#5-categor%C3%ADa---disponibilidad-de-acceso)
    - [5.1 Existencia de sitio Web](#51-existencia-de-sitio-web)
      - [5.1.1. Disponibilidad](#511-disponibilidad)
      - [5.1.1.1 Criterio de Éxito - Nivel AAA](#5111-criterio-de-%C3%A9xito---nivel-aaa)
    - [5.2 Régimen de Acceso](#52-r%C3%A9gimen-de-acceso)
      - [5.2.1. Gratuidad](#521-gratuidad)
        - [5.2.1.1. Criterio de Éxito - Nivel AA](#5211-criterio-de-%C3%A9xito---nivel-aa)
        - [5.2.1.2. Criterio de Éxito - Nivel AAA](#5212-criterio-de-%C3%A9xito---nivel-aaa)
      - [5.2.2 - Universalidad: Acceso Directo](#522---universalidad-acceso-directo)
        - [5.2.2.1. Criterio de Éxito - Nivel A](#5221-criterio-de-%C3%A9xito---nivel-a)
        - [5.2.2.2. Criterio de Éxito - Nivel AA](#5222-criterio-de-%C3%A9xito---nivel-aa)
        - [5.2.2.3. Criterio de Éxito - Nivel AAA](#5223-criterio-de-%C3%A9xito---nivel-aaa)
      - [5.2.3 - Universalidad: Patrones de Acesibilidad y Web Standards](#523---universalidad-patrones-de-acesibilidad-y-web-standards)
        - [5.2.3.1. Criterio de Éxito - Nivel A](#5231-criterio-de-%C3%A9xito---nivel-a)
        - [5.2.3.2. Criterio de Éxito - Nivel AA](#5232-criterio-de-%C3%A9xito---nivel-aa)
        - [5.2.3.3. Criterio de Éxito - Nivel AAA](#5233-criterio-de-%C3%A9xito---nivel-aaa)
      - [5.2.4 - Universalidad: Performance](#524---universalidad-performance)
        - [5.2.4.1. Criterio de Éxito - Nivel A](#5241-criterio-de-%C3%A9xito---nivel-a)
          - [WebPagetest](#webpagetest)
          - [Pagespeed Insights](#pagespeed-insights)
        - [5.2.4.2. Criterio de Éxito - Nivel AA](#5242-criterio-de-%C3%A9xito---nivel-aa)
          - [WebPagetest](#webpagetest-1)
          - [Pagespeed Insights](#pagespeed-insights-1)
        - [5.2.4.3. Criterio de Éxito - Nivel AAA](#5243-criterio-de-%C3%A9xito---nivel-aaa)
          - [WebPagetest](#webpagetest-2)
          - [Pagespeed Insights](#pagespeed-insights-2)
      - [5.2.5 - Seguridad: Conexión Encriptada](#525---seguridad-conexi%C3%B3n-encriptada)
        - [5.2.5.1. Criterio de Éxito - Nivel AA](#5251-criterio-de-%C3%A9xito---nivel-aa)
        - [5.2.5.2. Criterio de Éxito - Nivel AAA](#5252-criterio-de-%C3%A9xito---nivel-aaa)
      - [5.2.6 - Dados Abiertos: Acceso vía API REST](#526---dados-abiertos-acceso-v%C3%ADa-api-rest)
        - [5.2.6.1. Criterio de Éxito - Nivel AA](#5261-criterio-de-%C3%A9xito---nivel-aa)
        - [5.2.6.2. Criterio de Éxito - Nivel AA](#5262-criterio-de-%C3%A9xito---nivel-aa)
        - [5.2.6.3. Criterio de Éxito - Nivel AAA](#5263-criterio-de-%C3%A9xito---nivel-aaa)
  - [6. Información Mínima Obligatoria de Estructura](#6-informaci%C3%B3n-m%C3%ADnima-obligatoria-de-estructura)
    - [6.1. Estructura orgánica](#61-estructura-org%C3%A1nica)
      - [6.1.1. Criterio de Éxito - Nivel A](#611-criterio-de-%C3%A9xito---nivel-a)
      - [6.1.2. Criterio de Éxito - Nivel AA](#612-criterio-de-%C3%A9xito---nivel-aa)
      - [6.1.3. Criterio de Éxito - Nivel AAA](#613-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.2. Funciones y deberes](#62-funciones-y-deberes)
      - [6.2.1. Criterio de Éxito - Nivel A](#621-criterio-de-%C3%A9xito---nivel-a)
      - [6.2.2. Criterio de Éxito - Nivel AA](#622-criterio-de-%C3%A9xito---nivel-aa)
      - [6.2.3. Criterio de Éxito - Nivel AAA](#623-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.3. Ubicación de sus sedes y áreas](#63-ubicaci%C3%B3n-de-sus-sedes-y-%C3%A1reas)
      - [6.3.1. Criterio de Éxito - Nivel A](#631-criterio-de-%C3%A9xito---nivel-a)
      - [6.3.2. Criterio de Éxito - Nivel AA](#632-criterio-de-%C3%A9xito---nivel-aa)
      - [6.3.3. Criterio de Éxito - Nivel AAA](#633-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.4. Divisiones o departamentos](#64-divisiones-o-departamentos)
      - [6.4.1. Criterio de Éxito - Nivel A](#641-criterio-de-%C3%A9xito---nivel-a)
      - [6.4.2. Criterio de Éxito - Nivel AA](#642-criterio-de-%C3%A9xito---nivel-aa)
      - [6.4.3. Criterio de Éxito - Nivel AAA](#643-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.5. Horario de Atención al Público](#65-horario-de-atenci%C3%B3n-al-p%C3%BAblico)
      - [6.5.1. Criterio de Éxito - Nivel A](#651-criterio-de-%C3%A9xito---nivel-a)
      - [6.5.2. Criterio de Éxito - Nivel AA](#652-criterio-de-%C3%A9xito---nivel-aa)
      - [6.5.3. Criterio de Éxito - Nivel AAA](#653-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.6. Presupuesto](#66-presupuesto)
      - [6.6.1. Criterio de Éxito - Nivel A](#661-criterio-de-%C3%A9xito---nivel-a)
      - [6.6.2. Criterio de Éxito - Nivel AA](#662-criterio-de-%C3%A9xito---nivel-aa)
      - [6.6.3. Criterio de Éxito - Nivel AAA](#663-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.6. Ejecución Histórica Anual](#66-ejecuci%C3%B3n-hist%C3%B3rica-anual)
      - [6.6.1. Criterio de Éxito - Nivel A](#661-criterio-de-%C3%A9xito---nivel-a-1)
      - [6.6.2. Criterio de Éxito - Nivel AA](#662-criterio-de-%C3%A9xito---nivel-aa-1)
      - [6.6.3. Criterio de Éxito - Nivel AAA](#663-criterio-de-%C3%A9xito---nivel-aaa-1)
    - [6.7. Planes de gasto público por año fiscal](#67-planes-de-gasto-p%C3%BAblico-por-a%C3%B1o-fiscal)
      - [6.7.1. Criterio de Éxito - Nivel A](#671-criterio-de-%C3%A9xito---nivel-a)
      - [6.7.2. Criterio de Éxito - Nivel AA](#672-criterio-de-%C3%A9xito---nivel-aa)
      - [6.7.3. Criterio de Éxito - Nivel AAA](#673-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.8. Directorio de funcionarios - Básico](#68-directorio-de-funcionarios---b%C3%A1sico)
      - [6.8.1. Criterio de Éxito - Nivel A](#681-criterio-de-%C3%A9xito---nivel-a)
      - [6.8.2. Criterio de Éxito - Nivel AA](#682-criterio-de-%C3%A9xito---nivel-aa)
      - [6.8.3. Criterio de Éxito - Nivel AAA](#683-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.9. Directorio de funcionarios - Completo](#69-directorio-de-funcionarios---completo)
      - [6.9.1. Criterio de Éxito - Nivel A](#691-criterio-de-%C3%A9xito---nivel-a)
      - [6.9.2. Criterio de Éxito - Nivel AA](#692-criterio-de-%C3%A9xito---nivel-aa)
      - [6.9.3. Criterio de Éxito - Nivel AAA](#693-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.10. Escalas salariales](#610-escalas-salariales)
      - [6.10.1. Criterio de Éxito - Nivel A](#6101-criterio-de-%C3%A9xito---nivel-a)
      - [6.10.2. Criterio de Éxito - Nivel AA](#6102-criterio-de-%C3%A9xito---nivel-aa)
      - [6.10.3. Criterio de Éxito - Nivel AAA](#6103-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.11. Sanciones aplicadas a servidores públicos](#611-sanciones-aplicadas-a-servidores-p%C3%BAblicos)
      - [6.11.1. Criterio de Éxito - Nivel A](#6111-criterio-de-%C3%A9xito---nivel-a)
      - [6.11.2. Criterio de Éxito - Nivel AA](#6112-criterio-de-%C3%A9xito---nivel-aa)
      - [6.11.3. Criterio de Éxito - Nivel AAA](#6113-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.12. Directorio con Informaciones de Contratos de Contratistas - Básico](#612-directorio-con-informaciones-de-contratos-de-contratistas---b%C3%A1sico)
      - [6.12.1. Criterio de Éxito - Nivel A](#6121-criterio-de-%C3%A9xito---nivel-a)
      - [6.12.2. Criterio de Éxito - Nivel AA](#6122-criterio-de-%C3%A9xito---nivel-aa)
      - [6.12.3. Criterio de Éxito - Nivel AAA](#6123-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.13. Directorio con Informaciones de Contratos de Contratistas - Completo](#613-directorio-con-informaciones-de-contratos-de-contratistas---completo)
      - [6.13.1. Criterio de Éxito - Nivel A](#6131-criterio-de-%C3%A9xito---nivel-a)
      - [6.13.2. Criterio de Éxito - Nivel AA](#6132-criterio-de-%C3%A9xito---nivel-aa)
      - [6.13.3. Criterio de Éxito - Nivel AAA](#6133-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.14. Normas generales](#614-normas-generales)
      - [6.14.1. Criterio de Éxito - Nivel A](#6141-criterio-de-%C3%A9xito---nivel-a)
      - [6.14.2. Criterio de Éxito - Nivel AA](#6142-criterio-de-%C3%A9xito---nivel-aa)
      - [6.14.3. Criterio de Éxito - Nivel AAA](#6143-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.14. Normas Reglamentarias](#614-normas-reglamentarias)
      - [6.14.1. Criterio de Éxito - Nivel A](#6141-criterio-de-%C3%A9xito---nivel-a-1)
      - [6.14.2. Criterio de Éxito - Nivel AA](#6142-criterio-de-%C3%A9xito---nivel-aa-1)
      - [6.14.3. Criterio de Éxito - Nivel AAA](#6143-criterio-de-%C3%A9xito---nivel-aaa-1)
    - [6.15. Manuales](#615-manuales)
      - [6.15.1. Criterio de Éxito - Nivel A](#6151-criterio-de-%C3%A9xito---nivel-a)
      - [6.15.2. Criterio de Éxito - Nivel AA](#6152-criterio-de-%C3%A9xito---nivel-aa)
      - [6.15.3. Criterio de Éxito - Nivel AAA](#6153-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.16. Metas y Objetivos](#616-metas-y-objetivos)
      - [6.16.1. Criterio de Éxito - Nivel A](#6161-criterio-de-%C3%A9xito---nivel-a)
      - [6.16.2. Criterio de Éxito - Nivel AA](#6162-criterio-de-%C3%A9xito---nivel-aa)
      - [6.16.3. Criterio de Éxito - Nivel AAA](#6163-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.17. Resultado de Auditorías](#617-resultado-de-auditor%C3%ADas)
      - [6.17.1. Criterio de Éxito - Nivel A](#6171-criterio-de-%C3%A9xito---nivel-a)
      - [6.17.2. Criterio de Éxito - Nivel AA](#6172-criterio-de-%C3%A9xito---nivel-aa)
      - [6.17.3. Criterio de Éxito - Nivel AAA](#6173-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.18. Indicadores de Desempeño](#618-indicadores-de-desempe%C3%B1o)
      - [6.18.1. Criterio de Éxito - Nivel A](#6181-criterio-de-%C3%A9xito---nivel-a)
      - [6.18.2. Criterio de Éxito - Nivel AA](#6182-criterio-de-%C3%A9xito---nivel-aa)
      - [6.18.3. Criterio de Éxito - Nivel AAA](#6183-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.19. Plan Anticorrupción y de Atención al Ciudadano](#619-plan-anticorrupci%C3%B3n-y-de-atenci%C3%B3n-al-ciudadano)
      - [6.19.1. Criterio de Éxito - Nivel A](#6191-criterio-de-%C3%A9xito---nivel-a)
      - [6.19.2. Criterio de Éxito - Nivel AA](#6192-criterio-de-%C3%A9xito---nivel-aa)
      - [6.19.3. Criterio de Éxito - Nivel AAA](#6193-criterio-de-%C3%A9xito---nivel-aaa)
    - [6.20. Plan de Compras y Adquisición](#620-plan-de-compras-y-adquisici%C3%B3n)
      - [6.20.1. Criterio de Éxito - Nivel A](#6201-criterio-de-%C3%A9xito---nivel-a)
      - [6.20.2. Criterio de Éxito - Nivel AA](#6202-criterio-de-%C3%A9xito---nivel-aa)
      - [6.20.3. Criterio de Éxito - Nivel AAA](#6203-criterio-de-%C3%A9xito---nivel-aaa)
  - [7. Información Mínima Obligatoria respecto a Servicios, Procedimientos y Funcionamiento](#7-informaci%C3%B3n-m%C3%ADnima-obligatoria-respecto-a-servicios-procedimientos-y-funcionamiento)
    - [7.1. Atención al ciudadano](#71-atenci%C3%B3n-al-ciudadano)
      - [7.1.1. Criterio de Éxito - Nivel A](#711-criterio-de-%C3%A9xito---nivel-a)
      - [7.1.2. Criterio de Éxito - Nivel AA](#712-criterio-de-%C3%A9xito---nivel-aa)
      - [7.1.3. Criterio de Éxito - Nivel AAA](#713-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.2. Trámites](#72-tr%C3%A1mites)
      - [7.2.1. Criterio de Éxito - Nivel A](#721-criterio-de-%C3%A9xito---nivel-a)
      - [7.2.2. Criterio de Éxito - Nivel AA](#722-criterio-de-%C3%A9xito---nivel-aa)
      - [7.2.3. Criterio de Éxito - Nivel AAA](#723-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.3. Procedimientos](#73-procedimientos)
      - [7.3.1. Criterio de Éxito - Nivel A](#731-criterio-de-%C3%A9xito---nivel-a)
      - [7.3.2. Criterio de Éxito - Nivel AA](#732-criterio-de-%C3%A9xito---nivel-aa)
      - [7.3.3. Criterio de Éxito - Nivel AAA](#733-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.4. Decisiones](#74-decisiones)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-%C3%A9xito---nivel-a)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-%C3%A9xito---nivel-aa)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.5. Políticas](#75-pol%C3%ADticas)
      - [7.5.1. Criterio de Éxito - Nivel A](#751-criterio-de-%C3%A9xito---nivel-a)
      - [7.5.2. Criterio de Éxito - Nivel AA](#752-criterio-de-%C3%A9xito---nivel-aa)
      - [7.5.3. Criterio de Éxito - Nivel AAA](#753-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.4. Participación Ciudadana - Mecanismos de Presentación Directa](#74-participaci%C3%B3n-ciudadana---mecanismos-de-presentaci%C3%B3n-directa)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-%C3%A9xito---nivel-a-1)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-%C3%A9xito---nivel-aa-1)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-%C3%A9xito---nivel-aaa-1)
    - [7.5. Reporte de Participación Ciudadana](#75-reporte-de-participaci%C3%B3n-ciudadana)
      - [7.5.1. Criterio de Éxito - Nivel A](#751-criterio-de-%C3%A9xito---nivel-a-1)
      - [7.5.2. Criterio de Éxito - Nivel AA](#752-criterio-de-%C3%A9xito---nivel-aa-1)
      - [7.5.3. Criterio de Éxito - Nivel AAA](#753-criterio-de-%C3%A9xito---nivel-aaa-1)
    - [7.6. Mecanismos de Participación Ciudadana en Formulación de Políticas](#76-mecanismos-de-participaci%C3%B3n-ciudadana-en-formulaci%C3%B3n-de-pol%C3%ADticas)
      - [7.6.1. Criterio de Éxito - Nivel A](#761-criterio-de-%C3%A9xito---nivel-a)
      - [7.6.2. Criterio de Éxito - Nivel AA](#762-criterio-de-%C3%A9xito---nivel-aa)
      - [7.6.3. Criterio de Éxito - Nivel AAA](#763-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.7. Informes de Gestión](#77-informes-de-gesti%C3%B3n)
      - [7.7.1. Criterio de Éxito - Nivel A](#771-criterio-de-%C3%A9xito---nivel-a)
      - [7.7.2. Criterio de Éxito - Nivel AA](#772-criterio-de-%C3%A9xito---nivel-aa)
      - [7.7.3. Criterio de Éxito - Nivel AAA](#773-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.8. Informes de Evaluación](#78-informes-de-evaluaci%C3%B3n)
      - [7.8.1. Criterio de Éxito - Nivel A](#781-criterio-de-%C3%A9xito---nivel-a)
      - [7.8.2. Criterio de Éxito - Nivel AA](#782-criterio-de-%C3%A9xito---nivel-aa)
      - [7.8.3. Criterio de Éxito - Nivel AAA](#783-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.9. Informes de Auditoría](#79-informes-de-auditor%C3%ADa)
      - [7.9.1. Criterio de Éxito - Nivel A](#791-criterio-de-%C3%A9xito---nivel-a)
      - [7.9.2. Criterio de Éxito - Nivel AA](#792-criterio-de-%C3%A9xito---nivel-aa)
      - [7.9.3. Criterio de Éxito - Nivel AAA](#793-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.10. Mecanismos Internos de Supervisión - Oficina de Control Interno](#710-mecanismos-internos-de-supervisi%C3%B3n---oficina-de-control-interno)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-%C3%A9xito---nivel-a-2)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-%C3%A9xito---nivel-aa-2)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-%C3%A9xito---nivel-aaa-2)
    - [7.11. Mecanismos Externos de Supervisión](#711-mecanismos-externos-de-supervisi%C3%B3n)
      - [7.11.1. Criterio de Éxito - Nivel A](#7111-criterio-de-%C3%A9xito---nivel-a)
      - [7.11.2. Criterio de Éxito - Nivel AA](#7112-criterio-de-%C3%A9xito---nivel-aa)
      - [7.11.3. Criterio de Éxito - Nivel AAA](#7113-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.12. Mecanismos Notificación](#712-mecanismos-notificaci%C3%B3n)
      - [7.12.1. Criterio de Éxito - Nivel A](#7121-criterio-de-%C3%A9xito---nivel-a)
      - [7.12.2. Criterio de Éxito - Nivel AA](#7122-criterio-de-%C3%A9xito---nivel-aa)
      - [7.12.3. Criterio de Éxito - Nivel AAA](#7123-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.13. Mecanismos de Vigilancia](#713-mecanismos-de-vigilancia)
      - [7.13.1. Criterio de Éxito - Nivel A](#7131-criterio-de-%C3%A9xito---nivel-a)
      - [7.13.2. Criterio de Éxito - Nivel AA](#7132-criterio-de-%C3%A9xito---nivel-aa)
      - [7.13.3. Criterio de Éxito - Nivel AAA](#7133-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.14. Procedimientos y Lineamientos de Contratación](#714-procedimientos-y-lineamientos-de-contrataci%C3%B3n)
      - [7.14.1. Criterio de Éxito - Nivel A](#7141-criterio-de-%C3%A9xito---nivel-a)
      - [7.14.2. Criterio de Éxito - Nivel AA](#7142-criterio-de-%C3%A9xito---nivel-aa)
      - [7.14.3. Criterio de Éxito - Nivel AAA](#7143-criterio-de-%C3%A9xito---nivel-aaa)
    - [7.15. Políticas en materia de adquisiciones y compras](#715-pol%C3%ADticas-en-materia-de-adquisiciones-y-compras)
      - [7.15.1. Criterio de Éxito - Nivel A](#7151-criterio-de-%C3%A9xito---nivel-a)
      - [7.15.2. Criterio de Éxito - Nivel AA](#7152-criterio-de-%C3%A9xito---nivel-aa)
      - [7.15.3. Criterio de Éxito - Nivel AAA](#7153-criterio-de-%C3%A9xito---nivel-aaa)
  - [8. Instrumentos De Gestión De la Información Pública](#8-instrumentos-de-gesti%C3%B3n-de-la-informaci%C3%B3n-p%C3%BAblica)
    - [8.1. Esquemas de Publicación de información](#81-esquemas-de-publicaci%C3%B3n-de-informaci%C3%B3n)
      - [8.1.1. Criterio de Éxito - Nivel A](#811-criterio-de-%C3%A9xito---nivel-a)
      - [8.1.2. Criterio de Éxito - Nivel AA](#812-criterio-de-%C3%A9xito---nivel-aa)
      - [8.1.3. Criterio de Éxito - Nivel AAA](#813-criterio-de-%C3%A9xito---nivel-aaa)
    - [8.2. Programa de Gestión Documental](#82-programa-de-gesti%C3%B3n-documental)
      - [8.2.1. Criterio de Éxito - Nivel A](#821-criterio-de-%C3%A9xito---nivel-a)
      - [8.2.2. Criterio de Éxito - Nivel AA](#822-criterio-de-%C3%A9xito---nivel-aa)
      - [8.2.3. Criterio de Éxito - Nivel AAA](#823-criterio-de-%C3%A9xito---nivel-aaa)
    - [8.3. Tablas De Retención Documental](#83-tablas-de-retenci%C3%B3n-documental)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-%C3%A9xito---nivel-a)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-%C3%A9xito---nivel-aa)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-%C3%A9xito---nivel-aaa)
    - [8.4. Información Publicada Antes De La Ley 1712 De 2014](#84-informaci%C3%B3n-publicada-antes-de-la-ley-1712-de-2014)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-%C3%A9xito---nivel-a-1)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-%C3%A9xito---nivel-aa-1)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-%C3%A9xito---nivel-aaa-1)
    - [8.5. Respuestas A Solicitudes De Información Recibidas](#85-respuestas-a-solicitudes-de-informaci%C3%B3n-recibidas)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-%C3%A9xito---nivel-a-2)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-%C3%A9xito---nivel-aa-2)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-%C3%A9xito---nivel-aaa-2)


## 1. Introducción

Esta sección no es normativa

Los objetivos de esta especificación incluyen:
(a fazer)


### 1.1 Transparencia, Rendición de Cuentas y lucha contra la corrupción
(a fazer)

### 1.2 Público objetivo


(a fazer)

### 1.3 Filosofía y Presupuestos

### 1.4 Interdisciplinaridad

### 1.5 Regulación
(a fazer) lista de regulación (leyes, reglamentos, etc), tal vez con una breve análisis de la doctrina legal y/o algunos puntos importantes (e.g. jurisprudencia ambigua, etc)

### 1.6 Documentos de Apoyo

### 1.7 Colaboración

## 2. Uso de la especificación

This section is non-normative.

## 3. Conformidad

Además de las secciones marcadas como no normativas, todos los diagramas, ejemplos y notas en esta especificación son no normativos (excepto cuando marcados en contrario). Todo el resto en esta especificación es normativo.

The key words MAY, MUST, MUST NOT, OPTIONAL, RECOMMENDED, REQUIRED, SHALL, SHALL NOT, SHOULD, and SHOULD NOT are to be interpreted as described in [RFC2119]. Además, clasificamos cada criterio como OBLIGACIÓN o RECOMENDACIÒN.

Para que una página web esté conforme con esta especificación, debe satisfacer todos y cada uno de los siguientes requisitos de conformidad:

1. Nivel de conformidad: Uno de los siguientes niveles de conformidad se satisface por completo.

    Nivel A: Para el nivel A de conformidad (el mínimo nivel de conformidad), el sitio web satisface todos los criterios de éxito de nivel A, o se proporciona una versión alternativa conforme.

    Nivel AA: Para el nivel AA de conformidad, el sitio web satisface todos los criterios de éxito de nivel A y AA, o se proporciona una versión alternativa conforme al nivel AA.

    Nivel AAA: Para el nivel AAA de conformidad, el sitio web satisface todos los criterios de éxito de nivel A, AA y AAA, o se proporciona una versión alternativa conforme al nivel AAA.

Nota 1: A pesar de que la conformidad sólo puede lograrse en los niveles indicados, se anima a los autores a notificar en sus declaraciones cualquier progreso que se realice para satisfacer los criterios de éxito de todo nivel más allá del nivel de conformidad alcanzado.

Nota 2: No se recomienda como política general exigir el nivel de conformidad AAA para sitios enteros porque no es posible que algunos contenidos puedan satisfacer todos los criterios de éxito de nivel AAA.

### Herramientas para examen de conformidad

#### WCAG2.1

- Functional Accessibility Evaluator: https://fae.disability.illinois.edu

### 3.1 Conformidad de Dependencias

(a fazer) como se define conformidad de otras especificaciones, técnicas, etc?

### 3.4 Conformance Checkers
(a fazer)

## 4. Términos importantes (vocabulario)

(a fazer)


## 5. Categoría - Disponibilidad de Acceso

(afazer: intro corta)

### 5.1 Existencia de sitio Web
Tipo: OBLIGACIÓN

La entidad deberá mantener un sitio web, que deberá estar disponible para acesso via una URI oficial por cualquier user-agent.

#### 5.1.1. Disponibilidad

El sitio está disponible para acceso vía una URI oficial por cualquier user-agent.

#### 5.1.1.1 Criterio de Éxito - Nivel AAA

El sitio retorna páginas con códigos HTTP 200 o 314 en su URI oficial, cuando es accedido por cualquier user-agent.

### 5.2 Régimen de Acceso
Tipo: MEZCLADO

(afazer: intro)

#### 5.2.1. Gratuidad
Tipo: OBLIGACIÓN

El sitio debe tener acceso gratuito a los servicios informáticos que presta la entidad excepto para casos previstos en ley o en los reglamentos.

##### 5.2.1.1. Criterio de Éxito - Nivel AA

Algunos servicios solo son accesibles por contraseña u otro identificador obtenidos a partir de botones y/o otros métodos de pago detectados en el sitio.

##### 5.2.1.2. Criterio de Éxito - Nivel AAA

Todos los servicios son accesibles sin contrapartida financiera y botones u otros métodos de pagos no son detectados en el sitio.

#### 5.2.2 - Universalidad: Acceso Directo
Tipo: RECOMENDACIÓN

Los servicios informáticos que presta la entidad deben ser abiertos a todo el público que desee acceder a ellos y no deben estar restringidos a ciertos usuarios previo registro y recepción de una clave de acceso.

##### 5.2.2.1. Criterio de Éxito - Nivel A

Registro y clave de acceso son necesarios para acceder a parte del sitio SIN una buena justificación (e.g. privacidad de datos personales o seguridad)

##### 5.2.2.2. Criterio de Éxito - Nivel AA

Registro y clave de acceso son necesarios para acceder a parte del sitio CON una buena justificación (e.g. privacidad de datos personales o seguridad)

##### 5.2.2.3. Criterio de Éxito - Nivel AAA

Todos los servicios son accesibles sin registro previo ni  clave de acceso.

#### 5.2.3 - Universalidad: Patrones de Acesibilidad y Web Standards
Tipo: RECOMENDACIÓN

Los sitios deben permitir acceso igualitario por:

   1) Tecnologías de asistencia como lectores de pantalla, asistentes de voz, etc;
   2) Acceso sin uso de javascript o plugins de terceros;
   3) Acceso por dispositivos variados como computadores, teléfonos inteligentes, asistentes de voz (e.g. Amazon Alexa), SmartTVs y otros dispositivos;
   4) Acceso en condiciones variadas de conexiones (broadband y 2G/3G de baja performance), para lo cual deben seguir principios y directrices de accesibilidad conforme definidos por la recomendación WCAG2.1 y WAI-ARIA de W3C y siguiendo las mejores prácticas determinadas en The Web Standards projects para markup sin considerar metadatos o atributos semánticos (e.g. elementos HTML semánticos, sin considerar schema.org o RDF markup);

##### 5.2.3.1. Criterio de Éxito - Nivel A

El sitio web es válido sin errores en el https://validator.w3.org siguiendo la especificación HTML5 y utilizando los elementos de la especificación de forma semántica. Es decir, utilización correctamente los e elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, etc.)

[HTML5](https://w3c.github.io/html/), [schema.org](https://schema.org), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD)

##### 5.2.3.2. Criterio de Éxito - Nivel AA

El sitio web es válido sin errores en https://validator.w3.org siguiendo la especificación HTML5 y utilizando los elementos de la especificación de forma semántica. Es decir, utilización correcta de elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, etc.);

El sitio cumple con los criterios A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/)

##### 5.2.3.3. Criterio de Éxito - Nivel AAA

El sitio web es válido sin errores en https://validator.w3.org siguiendo la especificación HTML5 y utilizando los elementos de la especificación de forma semántica. Es decir, utilización correcta de elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, etc.);

El sitio cumple con los criterios A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/)

El sitio utiliza de forma adequada las prácticas [wai-aria-1.2](https://w3c.github.io/aria/);

#### 5.2.4 - Universalidad: Performance
Tipo: RECOMENDACIÓN

Los sitios deben permitir acceso con velocidad razonable y estable incluso en malas condiciones de acceso, como conexión por dispositivos móviles en redes de baja performance. Los sitios deben obtener grados mínimos en la herramientas [Webpagetest](http://webpagetest.org/result/190506_KG_29de3021baf30242013b8f58843cd7df/) y Pagespeed Insights, de acuerdo con lo descrito a continuación.

En Webpagetest, los test son efectuados con la siguiente configuración:
    - Test Location: Android Devices - Dulles, VA, Moto G (gen 4);
    - Browser: Moto G4 - Chrome;
    - Connection: 3G (1.6 Mbps/768 Kbps RTT)
    - Number of Tests to Run: 9;
    - Repeat View: First View and Repeat View;
    - Capture Video: marcado
    - Ignore SSL Certificate Errors: marcado

##### 5.2.4.1. Criterio de Éxito - Nivel A

Los sitios deben obtener los siguientes grados máximos:

###### WebPagetest
    - Time to First Byte: 3.500s
    - First Interactive (beta): 10.000s
    - Speed Index: 11.000s
    - Bytes in: 2.048kb
    - Cost: $$$

###### Pagespeed Insights
    - Ordenador: 70
    - Móvil: 50

##### 5.2.4.2. Criterio de Éxito - Nivel AA

Los sitios deben obtener los siguientes grados máximos:

###### WebPagetest
    - Time to First Byte: 3.000s
    - First Interactive (beta): 8.000s
    - Speed Index: 7.000s
    - Bytes in: 1.536kb
    - Cost: $$$

###### Pagespeed Insights
    - Ordenador: 85
    - Móvil: 60

##### 5.2.4.3. Criterio de Éxito - Nivel AAA

Los sitios deben obtener los siguientes grados máximos:

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

El sitio es accesible en conexión encriptada (SSL/TLS).

##### 5.2.5.1. Criterio de Éxito - Nivel AA

El sitio es accesible en conexión encriptada (SSL/TLS) opcional.

##### 5.2.5.2. Criterio de Éxito - Nivel AAA

El sitio es accesible en conexión encriptada (SSL/TLS) y solamente por conexión criptograda.

#### 5.2.6 - Dados Abiertos: Acceso vía API REST
Tipo: RECOMENDACIÓN

Los contenidos del sitio son accesibles por una API REST con datos estructurados, incluso meta-dados.

##### 5.2.6.1. Criterio de Éxito - Nivel AA

API REST disponible, pero sin meta-datos.

##### 5.2.6.2. Criterio de Éxito - Nivel AA

API REST disponible, CON meta-datos.

##### 5.2.6.3. Criterio de Éxito - Nivel AAA

API REST disponible, CON meta-datos y en formato JSON.

## 6. Información Mínima Obligatoria de Estructura
(afazer: intro)

Informaciones sobre la estructura, de acuerdo con el artículo 9 de la ley 1712 de 2014.

### 6.1. Estructura orgánica
Tipo: OBLIGACIÓN

Descripción de la forma en que se compone y se organiza la entidad y no tan sólo la cabeza o principal órgano que lo compone.

#### 6.1.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx), pdf no-accesible, o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.1.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.1.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (e.g. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org o motaSchema. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

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
Tipo: OBLIGACIÓN

Descripción de funciones y deberes de la entidad en general y no tan sólo la cabeza o principal órgano que lo compone.

#### 6.2.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerrpo de la capa de sesión.

#### 6.2.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.2.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (e.g. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org o motaSchema. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.3. Ubicación de sus sedes y áreas
Tipo: OBLIGACIÓN

Descripción de ubicación de sedes y áreas de la entidad en general y no tan sólo la cabeza o principal órgano que lo compone.

#### 6.3.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.3.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML5. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.3.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org o motaSchema. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

Referencias:

  - https://schema.org/GovernmentOffice
  - https://schema.org/GovernmentBuilding

### 6.4. Divisiones o departamentos
Tipo: OBLIGACIÓN

Informaciones sobre la totalidad de divisiones territoriales. Para considerar como positiva esta pauta, basta con que la información sea general (indicación de cuales son, direcciones, etc.) y no es necesario que todo el contenido del sitio sea el mismo para todas las divisiones territoriales.

#### 6.4.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.4.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en lá página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.4.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org o motaSchema. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.5. Horario de Atención al Público
Tipo: OBLIGACIÓN

Informaciones sobre horarios de atención al público de la entidad y sus divisiones en diferentes medios: en la sede, teléfono, correo electrónico, etc

#### 6.5.1. Criterio de Éxito - Nivel A

Texto disponible en página específica, accesible por elemento de navegación principal o en el cuerpo de la capa de sesión, incluye horarios de atención de diferentes departamentos o sedes.

#### 6.5.2. Criterio de Éxito - Nivel AA

Texto disponible en página específica, accesible por elemento de navegación principal o en el cuerpo de la capa de sesión, incluye horarios de atención de diferentes departamentos o sedes. Horarios más importante de la sede o servicio principal también disponible en pié de página de todas las páginas.

#### 6.5.3. Criterio de Éxito - Nivel AAA

Texto disponible en página específica, incluye horarios de atención de diferentes departamentos o sedes. Horarios más importante de la sede o servicio principal también disponible en pié de página de todas las páginas. En los dos casos, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org o motaSchema.

### 6.6. Presupuesto
Tipo: OBLIGACIÓN

El presupuesto de la entidad para la respectiva vigencia debe estar disponible para verificación del público. Puede ser el presupuesto inicial o final. Eo presupuesto debe ofrecer datos (valores, ingresos, gastos) de forma clara, organizada y debe estar desagregado conforme se describe a continuación, con encabezados o títulos acuerdo los títulos en paréntesis:

- Ingresos presupuestarios (Ingresos);
- gastos de personal (Gastos);
- Bienes y servicios de consumo;
- Adquisición de activos no financieros;
- Edificios, mobiliarios y otros;
- Equipos informáticos;
- Programas informáticos;
- Actualizado hasta el último trimestre concluido;

En la base de patrones MOTA, presentamos un modelo de archivo Datos Presupuestales, que cumple con los requisitos y buenas prácticas aquí mencionadas.

#### 6.6.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.6.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. El archivo sigue el patrón del modelo de archivo Datos Presupuestales en la base de patrones MOTA.

#### 6.6.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.6. Ejecución Histórica Anual
Tipo: OBLIGACIÓN

El sitio web contiene información relativa al presupuesto ejecutado en el año en curso, que muestre cómo se está llevando a cabo la ejecución del presupuesto en la respectiva vigencia. Los datos pueden ser agregados mensualmente o trimestralmente, idealmente con porcentajes de ejecución, y deben ofrecer datos (gastos, valores, ingresos, gastos) de forma clara, organizada y encontrarse desagregados conforme se describe a continuación, con encabezados o títulos en paréntesis:

- Ingresos presupuestarios (Ingresos);
- Gastos de personal (Gastos);
- Bienes y servicios de consumo;
- Adquisición de activos no financieros;
- Edificios, mobiliarios y otros;
- Equipos informáticos;
- Programas informáticos;
- Actualizado hasta el último trimestre concluido;

En la base de patrones MOTA, presentamos modelos de archivo “Ejecución Presupuestal Mensual” y “Ejecución Presupuestal Trimestral”, que cumplen con los requisitos y buenas prácticas aquí mencionadas.

#### 6.6.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.6.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. El archivo sigue el patrón de los modelos de archivo “Ejecución Presupuestal Mensual” y “Ejecución Presupuestal Trimestral” en la base de patrones MOTA.

#### 6.6.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org o motaSchema. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.7. Planes de gasto público por año fiscal
Tipo: OBLIGACIÓN

AFAZER

En la base de patrones MOTA, presentamos modelos de archivo ____________________, que cumplen con los requisitos y  buenas prácticas aquí mencionadas.

#### 6.7.1. Criterio de Éxito - Nivel A

AFAZER

#### 6.7.2. Criterio de Éxito - Nivel AA

AFAZER

#### 6.7.3. Criterio de Éxito - Nivel AAA

AFAZER


### 6.8. Directorio de funcionarios - Básico
Tipo: OBLIGACIÓN

El sitio web contiene un directorio de funcionarios con sus informaciones básicas:

- Nombres y apellidos;
- Direcciones de correo electrónico;
- Teléfono del despacho y dependencia.

#### 6.8.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) . Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.8.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.8.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.9. Directorio de funcionarios - Completo
Tipo: OBLIGACIÓN

El sitio web contiene un directorio de funcionarios con sus informaciones completas.

- Nombres y apellidos;
- Direcciones de correo electrónico;
- Teléfono del despacho y dependencia.
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades)
- Experiencia laboral y profesional
  - Nombres específicos de empleadores previos
  - Cargos anteriores
  - Fecha de inicio y fin en cada cargo
- Sanciones aplicadas a servidores públicos

 Alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla con las informaciones.

#### 6.9.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla con las informaciones.

#### 6.9.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.9.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.10. Escalas salariales
Tipo: OBLIGACIÓN

Es posible encontrar una tabla con los rangos de salarios de la entidad, identificado por el título "Rangos de salario por nivel", y el decreto de asignaciones salariales de la entidad en un lugar visible. Un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones.

La tabla debe ser actualizada al menos al último año concluido y contiene información sobre el salario base por jerarquía y/o categoría ocupacional, de acuerdo con la categoría, tipo y otras especificidades de la entidad. Ejemplo, en el sitio de la Fiscal General de la Nación se espera encontrar datos separados por jerarquía y/o categoría de fiscales y también por jerarquía y/o categoría ocupacional de otros funcionarios no fiscales.

#### 6.10.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las

#### 6.10.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.10.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.11. Sanciones aplicadas a servidores públicos
Tipo: OBLIGACIÓN

Es posible encontrar informaciones sobre sanciones disciplinarias o de otro tipo que hayan sido impuestas  a funcionarios de la entidad. Hay estadísticas sobre las sanciones impuestas, actualizadas hasta el último año concluído y se encuentran desagregadas según el tipo de funcionario. e.g. en el sitio de la Fiscal General de la Nación las informaciones deben esta desagregadas entre fiscales y no fiscales.

#### 6.11.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.11.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.11.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquemas [Report](https://schema.org/Report), [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.12. Directorio con Informaciones de Contratos de Contratistas - Básico
Tipo: OBLIGACIÓN

Es posible encontrar informaciones sobre los contratos de contratistas en formatos abiertos. Alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones.

- Nombres y apellidos;
- Direcciones de correo;
- Teléfono del despacho y dependencia;
- Objeto del contrato.

#### 6.12.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones

#### 6.12.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.12.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.13. Directorio con Informaciones de Contratos de Contratistas - Completo
Tipo: OBLIGACIÓN

El sitio web contiene contiene un directorio de funcionarios de sus informaciones completas.

- Nombres y apellidos;
- Direcciones de correo;
- Teléfono del despacho y dependencia.
- Objeto del contrato
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades).
  - Por formación académica se entiende, al menos, el grado académico que ostenta, la profesión que tiene y la institución académica por la que fue otorgada.
- Experiencia laboral y profesional. Por experiencia laboral, se entiende, al menos, aquella vinculada a la profesión que tiene, o en el evento de que no aparezca su profesión, las actividades laborales relacionadas con el cargo, área o institución en la que se desempeña.
  - Nombres específicos de empleadores previos.
  - Cargos anteriores.
  - Fecha de inicio y fin en cada cargo.
- Sanciones aplicadas a servidores públicos.

 Alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones

#### 6.13.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones.

#### 6.13.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.13.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.14. Normas generales
Tipo: OBLIGACIÓN

Existencia de una sección con normas y reglamentos pertinentes para la entidad: decretos, circulares, leyes, etc. relativas a creacción e reglamentos de la entidad. El documento MOTA - “Reglas Contextuales” especifica normas necesarias por entidad, o clases de entidad. Dos versiones deberán estar disponibles:

- Resumen en lenguaje sencillo, destacando secciones pertinentes de reglamentos;
- Copias verbatim de las normas.
  - En casos de documentos largos y cuyo alcance exceda el tema de Normas generales, está permitido copias verbatim de apenas las secciones pertinentes, pero es necesario un enlace que redirija al usuario a un archivo o recurso con el documento integral.

#### 6.14.1. Criterio de Éxito - Nivel A

Resumen disponible en la página, en HTML. Con normas disponibles para bajar en formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.14.2. Criterio de Éxito - Nivel AA

Resumen disponible en la página, em HTML, en lenguaje sencillo, con normas completas disponibles también en HTML en la misma página o en otra página en el mismo sitio. Para las normas completas, archivos en formatos abiertos (e.g. odf) accesibles en el mismo sitio y dominio es válido. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.14.3. Criterio de Éxito - Nivel AAA

Resumen disponible en la página, en HTML, en lenguaje sencillo, con normas completas disponibles también en HTML en la misma página o otra página en el mismo sitio. En los dos casos, el contenido es estructurado semánticamente (i.e. elementos HTML5 apropiados) y sus meta-datos disponibles en sintaxis LD+JSON y vocabulario schema.org segundo esquema [legislation](https://schema.org/Legislation) y [LegislationObject](https://schema.org/LegislationObject). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.14. Normas Reglamentarias
Tipo: OBLIGACIÓN

Existencia de información sobrenormas reglamentarias pertinentes a la entidad: resoluciones y directivas. El documento MOTA - “Reglas Contextuales” especifica normas necesarias por entidad, o clases de entidad. Dos versiones deberán estar disponibles:

- Resumen en lenguaje sencillo, destacando secciones de reglamentos pertinentes;
- Copias verbatim de las normas.
  - En casos de documentos largos y cuyo alcance exceda el tema de Normas generales, está permitido copias verbatim de apenas las seccionespertinentes, pero es necesario un enlace que redirija al usuario a un archivo o recurso con el documento integral.

#### 6.14.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.14.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.14.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.15. Manuales
Tipo: OBLIGACIÓN

(afazer)

#### 6.15.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.15.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, em HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.15.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org según esquema. [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.16. Metas y Objetivos
Tipo: OBLIGACIÓN

(afazer) (video plan de acción de Fiscalía)

#### 6.16.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.16.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.16.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.17. Resultado de Auditorías
Tipo: OBLIGACIÓN

(afazer)
#### 6.17.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.17.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.17.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.18. Indicadores de Desempeño
Tipo: OBLIGACIÓN

Las entidades deben proveer información sobre los indicadores de desempeño que utilizan y reportes con estadísticas y análisis del desempeño de la entidad (en relación a _________) y de sus funcionarios. Para entidades nacionales, deben contener información a nivel nacional y territorial. El documento MOTA - “Reglas Contextuales” especifica normas necesarias por entidad, o clases de entidad.

#### 6.18.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.18.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.18.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.19. Plan Anticorrupción y de Atención al Ciudadano
Tipo: OBLIGACIÓN

(afazer)

#### 6.19.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.19.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página, en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.19.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.20. Plan de Compras y Adquisición
Tipo: OBLIGACIÓN

La entidad debe ofrecer informaciones de su Plan de Compras Anual. El documento MOTA - Reglas Contextuales especifica normas necesarias por entidad, o clases de entidad. El plan debe compreender:

- Proceso de Gestión Contractual / Procedimiento Plan Anual de Adquisiciones
- Contrataciones adjudicadas para la correspondiente vigencia, incluso funcionamiento e inversión, obras públicas, bienes adquiridos y arrendados, estudios o investigaciones.
- Plazos de cumplimiento de los contratos.
- Contrataciones en curso.

NOTA: Todos los contratos e ítems deben contener enlace al SECOP.

En caso de entidades con múltiples divisiones (e.g. secciones territoriales), se debe utilizar un archivo o una página web para cada división.

#### 6.20.1. Criterio de Éxito - Nivel A

Informaciones disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf), con links para el SECOP. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.20.2. Criterio de Éxito - Nivel AA

Proceso de Gestión Contractual disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados), informaciones de contratos disponibles en archivos, formatos abiertos (e.g. .odf), con links para el SECOP. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.20.3. Criterio de Éxito - Nivel AAA
Proceso de Gestión Contractual y lista de documentos disponibles en la página, estructurados semánticamente (i.e. elementos HTML5 apropiados), informaciones de contratos disponibles en archivos, en formatos abiertos (e.g. .odf), contendo links para el SECOP. Meta-dados de la colección de documentos contienen nombre del documento, autor, data de actualización, URI y enlace para el SECOP) en sintaxis LD+JSON y vocabulario schema.org según esquema [Collection](https://schema.org/Collection), [DigitalDocument](https://schema.org/DigitalDocument) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

## 7. Información Mínima Obligatoria respecto a Servicios, Procedimientos y Funcionamiento
(afazer: intro)

Información Mínima Obligatoria respecto a Servicios, Procedimientos y Funcionamiento, acuerdo artículo 11 de la ley 1712 de 2014.

### 7.1. Atención al ciudadano
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con información de los servicios que brinda directamente al público, incluyendo i) normas ii) formularios y formatos y, iii) protocolos de atención a los siguientes públicos:

1 - Ciudadanos en general;
2 - Prensa;
3 - Públicos específicos (e.g. litigantes en Corte Constitucional, Corte Suprema de Justicia, Consejo de Estado, etc.)

El documento MOTA - “Reglas Contextuales” especifica normas necesarias por entidad, o clases de entidad.

#### 7.1.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, en HTML, con modelos de formularios y formatos disponibles en archivos (e.g. .pdf, xlsx, o PDF). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.1.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.1.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.2. Trámites
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con informaciones de los trámites que se pueden agotar en la entidad, incluyendo i) normativa(s) relacionada(s) ii) proceso a seguir, incluso formularios y formatos y, iii) costos asociados.

Además de informaciones acerca cada trámite, se recomienda una tabla resumen listando costos, normativas y link para informaciones en detalles de cada trámite.

Los trámites mínimos requeridos para cada entidad o clases de entidades son especificados en el documento MOTA - “Reglas Contextuales”.

#### 7.2.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, en HTML, con modelos de formularios y formatos disponibles en archivos (e.g. .pdf, xlsx, o PDF). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.


#### 7.2.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), incluso una tabla listando costos, normativas y link para informaciones en detalles de cada trámite, y modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.2.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), incluso una tabla listando costos, normativas y link para informaciones en detalles de cada trámite, y modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.3. Procedimientos
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con informaciones sobre los procedimientos que se siguen para tomar decisiones en diferentes áreas y procesos. Los procedimientos mínimos requeridos para cada entidad o clases de entidad son especificados en el documento MOTA - “Reglas Contextuales”.

Ejemplo: Procedimientos mínimos Fiscalía General de la Nación:

1. Investigación de conductas punibles
2. Acusación de presuntos infractores de la ley ante juzgados y tribunales competentes
3. Coordinación de las funciones de policía judicial
4. Creación o supresión de direcciones de la Fiscalía
5. Decisiones sobre protección a víctimas
6. Decisiones sobre política criminal

#### 7.3.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.3.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.3.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.4. Decisiones
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con los contenidos de las decisiones adoptadas que afecten al público, junto con sus fundamentos e interpretaciones. Los procedimientos mínimos requeridos para cada entidad o clases de entidad son especificados en el documento MOTA - “Reglas Contextuales”.

Ejemplo: listado de decisiones mínimas que debe contener el sitio de la Fiscalía General de la Nación:

1. Decisiones sobre adopción de políticas internas de investigación
2. afazer
3. afazer
4. afazer
5. afazer

Además de informaciones acerca cada decisión, se recomenda una tabla o listado de decisiones organizadas de forma cronológica en reversa (i.e. las decisiones más recientes al inicio de la lista).

#### 7.4.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.4.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.5. Políticas
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con los contenidos de las políticas adoptadas que afecten al público, junto con sus fundamentos e interpretaciones. Los procedimientos mínimos requeridos para cada entidad o clases de entidad son especificados en el documento MOTA - “Reglas Contextuales”.

Ejemplo: listado de políticas mínimas que debe contener el sitio de la Fiscalía General de la Nación:

1. Política pública de priorización.
   1. Incluso criterios de priorización.
2. Políticas en materia de internacionalización para afrontar transnacionalidad de delitos.
3. Políticas de adopción y aplicación de enfoques diferenciales.
4. Políticas sobre investigación de crimen organizado.
5. Resultados de las políticas adoptadas.
   1.  Incluso resultados y casos emblemáticos.

Además de informaciones acerca cada política, se recomenda una tabla o listado de políticas organizadas de forma cronológica en reversa (i.e. las decisiones más recientes en al principio de la lista).

#### 7.5.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillp. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.5.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.5.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.4. Participación Ciudadana - Mecanismos de Presentación Directa

Tipo: OBLIGACIÓN

El sitio de la entidad debe ofrecer mecanismos de presentación directa de solicitudes, quejas y reclamos a disposición del público. Los mecanismos mínimos son:

1. Correo para información
2. Buzón de PQRs en forma de formulário sencillo, sin obligaciones de identificación o registro.
3. Preguntas frecuentes

El buzón de PQRs y el correo para información deben ser considerados mecanismos válidos para presentación de derechos de petición y solicitudes de acceso a información pública (Transparencia Pasiva), y para hacerle seguimiento al Derecho de petición a través da generación de radicado o que escriban durante el proceso donde va la PQR. En caso de que el buzón de PQRs sea utilizado para derechos de petición, es válido solicitar un correo electrónico para respuesta y seguimiento.

#### 7.4.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necesario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.4.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

En caso de un gran número de preguntas frequentes, un formulario de búsqueda debe estar presente.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf).

En caso de un gran número de preguntas frequentes, un formulario de búsquedadebe estar presente.

Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.5. Reporte de Participación Ciudadana
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con reportes generales y agregados de datos de quejas y reclamos de la entidad, correspondientes a la respectiva vigencia y a años anteriores.

El reporte general debe contener:

- Estadísticas agregadas de solicitudes, denuncias y los tiempos de respuesta del sujeto obligado.
- Análisis de las estadísticas, lecciones aprendidas y desafíos para el próximo año.

El conjunto de datos, en formato tabla u hoja de cálculos, debe contener informaciones de todas las solicitudes recibidas, con identificador de la queja, denuncias y tiempos de respuestas del sujeto obligado, pero sin informaciones que identifiquen directamente a ciudadanos.

#### 7.5.1. Criterio de Éxito - Nivel A

Estadísticas agregadas y análisis disponibles en una o más páginas estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en un archivo xls o xlsx.

#### 7.5.2. Criterio de Éxito - Nivel AA

Estadísticas agregadas y análisis disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en archivos con formatos abiertos (.csv o .odf).

#### 7.5.3. Criterio de Éxito - Nivel AAA

Estadísticas agregadas y análisis disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con descripciónes textuales en lenguaje sencilla. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en archivos con formatos abiertos (.csv o .odf) y tambiéncomo meta-datos en sintaxis LD+JSON y vocabulario schema.org.

### 7.6. Mecanismos de Participación Ciudadana en Formulación de Políticas
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas describiendo los mecanismos de participación ciudadana que ofrece para la formulación de políticas o ejercicios de facultades del sujeto obligado, incluyendo publicidad de invitaciones públicas, convocatorias o procesos de participación pública.

#### 7.6.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.6.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.6.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.7. Informes de Gestión
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener Informes de Gestión del periodo vigente y de períodos anteriores. Los informes resumen los resultados de la entidad por un período determinado, así como la administración hecha a sus recursos, contratación, entre otros.

AFAZER: aclarar "Documentos ex - post: vienen después de la gestión realizada en la respectiva vigencia

Idealmente, los informes deben ser presentarnos en páginas HTML, pero archivos también son válidos.


#### 7.7.1. Criterio de Éxito - Nivel A

El sitio contiene una página Informes de Gestión con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia.

#### 7.7.2. Criterio de Éxito - Nivel AA

El sitio contiene una página Informes de Gestión con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.7.3. Criterio de Éxito - Nivel AAA

El sitio contiene una página Informes de Gestión con listado o tabla de links para reportes en archivos PDF, PPT o DOC del  período vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencilla y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

Las mismas informaciones en el listado están disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.8. Informes de Evaluación
Tipo: OBLIGACIÓN


AFAZER: aclarar o que és estes ítem.

El sitio de la entidad debe contener Informes de Evaluación del periodo vigente y de los períodos anteriores. contratación, entre otros.

Idealmente, los informes deben ser presentarnos en páginas HTML, pero archivos también son válidos.

#### 7.8.1. Criterio de Éxito - Nivel A

El sitio contiene una página Informes de Evaluación con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia.

#### 7.8.2. Criterio de Éxito - Nivel AA

El sitio contiene una página Informes de Evaluación con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.8.3. Criterio de Éxito - Nivel AAA

El sitio contiene una página Informes de Evaluación con listado o tabla de links para reportes en archivos PDF, PPT o DOC del período vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

Las mismas informaciones en el listado están disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.9. Informes de Auditoría
Tipo: OBLIGACIÓN


AFAZER: aclarar o que és estes ítem.

El sitio de la entidad debe contener Informes de Auditoría del período vigente y de los anteriores. contratación, entre otros.

Idealmente, los informes deben ser presentados en páginas HTML, pero archivos también son válidos.

#### 7.9.1. Criterio de Éxito - Nivel A

El sitio contiene una página Informes de Auditoría con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia.

#### 7.9.2. Criterio de Éxito - Nivel AA

El sitio contiene una página Informes de Auditoría con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.9.3. Criterio de Éxito - Nivel AAA

El sitio contiene una página Informes de Auditoría con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencilla y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

Las mismas informaciones en el listado están disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.10. Mecanismos Internos de Supervisión - Oficina de Control Interno
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con información acerca de la Oficina de Control Interno, de manera que los funcionarios o la ciudadanía tengan claro que hay una dependencia a la que se puede acudir para presentar denuncias u observaciones acerca del funcionamiento interno de la entidad. En este sentido, se puede encontrar información sobre las funciones (la misión o los objetivos), los procesos (en qué consisten los planes de mejoramiento, cómo se hace efectiva una sanción, entre otros.) o mecanismos (qué instrumentos de denuncia tienen) de la Oficina. También se vale información que explique la diferencia entre el control interno disciplinario y el control interno de gestión.

#### 7.4.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.4.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.11. Mecanismos Externos de Supervisión
Tipo: OBLIGACIÓN

AFAZER: aclarear o que debemos encontrar

El sitio de la entidad debe contener una o más páginas con informaciones acerca de Mecanismos Externos de Supervisión, de manera que funcionarios o ciudadanía tengan claro a qué entidad se puede acudir para presentar denuncias u observaciones acerca del funcionamiento interno de la entidad.

#### 7.11.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.11.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.11.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.12. Mecanismos Notificación
Tipo: OBLIGACIÓN

AFAZER: aclarear o que debemos encontrar

#### 7.12.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.12.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.12.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.13. Mecanismos de Vigilancia
Tipo: OBLIGACIÓN

AFAZER: aclarear o que debemos encontrar

#### 7.13.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.13.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.13.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.14. Procedimientos y Lineamientos de Contratación
Tipo: OBLIGACIÓN

AFAZER: aclarear o que són documento ex-ante, por ejemplo

El sitio de la entidad debe contener una o más páginas con los procedimientos y lineamientos de contratación.

Documentos ex - ante (de planeación o tipo manual) que den guía sobre cómo se va a proceder para hacer algo). Formulado por la entidad. Pudo ser formulado en una vigencia diferente a la actual. Publicación de documentos que den guía sobre cómo se maneja la contratación en la entidad según cada modalidad. En la mayoría de casos, estos lineamientos se consolidan en un documento llamado "Manual de Contratación".

#### 7.14.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.14.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.14.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.15. Políticas en materia de adquisiciones y compras
Tipo: OBLIGACIÓN

AFAZER: aclarear este íten. Ejemplo, esto no el mismo que Plan de Compras (ítem 6.20)?

La entidad debe ofrecer informaciones de su Plan de adquisiciones. El documento MOTA - Reglas Contextuales especifica normas necesarias por entidad, o clases de entidad. El plan debe compreender:

- Proceso de Gestin Contractual / Procedimiento Plan Anual de Adquisiciones
- Datos/procesos de adjudicación de los contratos
- Datos/procesos de ejecución de los contratos

#### 7.15.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.Informaciones disponibles en archivos, formatos propietarios (e.g. .docx, xlsx), pdf non-accesible, con links para SECOP. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión;

#### 7.15.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.15.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y en conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

## 8. Instrumentos De Gestión De la Información Pública
(afazer: intro)

Información respecto a instrumentos de gestión de la información pública requeridos por la Ley 1712 de 2014

### 8.1. Esquemas de Publicación de información
Tipo: OBLIGACIÓN

AFAZER: aclarear este ítem. Que ejemplos de información teríamos aqui?

El sitio de la entidad debe contener una o más páginas con informaciones de Esquemas de Publicación de información, publicadas en una página denominada "Acceso a información pública" y estable i) qué tipo de información está publicada en el sitio web ii) qué información se publicará de manera proactiva iii) formatos de publicación iv) idioma v) responsable de la producción de información vi) la periodicidad en la divulgación, entre otros.

Un ejemplo de esquema de publicación, en archivo xls, se encuentra en el enlace: https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2

#### 8.1.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) com el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf non-accesible. Este archivo contiene una tabla describiendo esquema de publicación de información similar all ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.


#### 8.1.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad com directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

También es aceptable, para la tabla, un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene una tabla describiendo esquema de publicación de información similar al ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.


#### 8.1.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla em HTML5 describiendo esquema de publicación de información similar all ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

También es aceptable, para tabla, un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene una tabla describiendo esquema de publicación de información similar al ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

Los mismos datos de la tabla son encontrado como datos estructurados en sintaxis LD+JSON y vocabulario schema.org [ItemList](https://schema.org/ItemList), [ListItem](https://schema.org/ListItem),[DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 8.2. Programa de Gestión Documental
Tipo: OBLIGACIÓN

AFAZER: aclarear este ítem. Que ejemplos de información teríamos aqui?

El sitio de la entidad debe contener una o más páginas con informaciones de Programa de Gestión Documental, publicadas en una página denominada "Gestión Documental" e informar "procedimientos y lineamientos necesarios para la producción, distribución, organización, consulta y conservación de los documentos públicos". Comprende la vida del documento desde su creación hasta su disposición final.

Un ejemplo de Programa de Gestión Documental se encuentra en el enlace: http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

#### 8.2.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) con el título "Gestión Documental", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf non-accesible. Este archivo procedimientos y lineamientos necesarios para la producción, distribución, organización, consulta y conservación de los documentos públicos similar al ejemplo en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf


#### 8.2.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y deconformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla em HTML5 describiendo esquema de publicación de información similar al ejemplo en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

También es aceptable para los procedimientos y lineamientos, un archivo de formato abierto (.odf) o **.pdf accesible**.


#### 8.2.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

También es aceptable para los procedimiento y lineamientos, un archivo de formato abierto (.odf) o **.pdf accesible**.

Los meta-datos de la página y cualquier documento o archivo accesorio son encontrados como datos estructurados en sintaxis LD+JSON y vocabulario schema.org [ItemList](https://schema.org/ItemList), [ListItem](https://schema.org/ListItem),[DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 8.3. Tablas De Retención Documental
Tipo: OBLIGACIÓN

AFAZER: aclarear este ítem. Que queremos aqui? que ejemplos de información teríamos aqui?

#### 8.3.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) com el título "AFAZER", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf non-accesible. Este archivo contiene una tabla describiendo esquema de publicación de información similar al ejemplo en AFAZER.


#### 8.3.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), com el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.


#### 8.3.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y en conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable  un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.

Los mismos datos son encontrado como datos estructurados en sintaxis LD+JSON y vocabulario schema.org AFAZER: definir schemas requeridos.

### 8.4. Información Publicada Antes De La Ley 1712 De 2014
Tipo: OBLIGACIÓN

AFAZER: aclarear este ítem. Que ejemplos de información teríamos aqui?

AFAZER: aclarear este ítem. Que queremos aqui? que ejemplos de información teríamos aqui?

#### 8.3.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) com el título "AFAZER", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf non-accesible. Este archivo contiene una tabla describiendo esquema de publicación de información similar a el ejemplo en AFAZER.


#### 8.3.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), com el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.


#### 8.3.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.

Los mismos datos son encontrados como datos estructurados en sintaxis LD+JSON y vocabulario schema.org AFAZER: definir schemas requeridos.

### 8.5. Respuestas A Solicitudes De Información Recibidas
Tipo: OBLIGACIÓN

AFAZER: aclarear este ítem. Que ejemplos de información teríamos aqui?

AFAZER: aclarear este ítem. Que queremos aqui? que ejemplos de información teríamos aqui?

#### 8.3.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) com el título "AFAZER", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf non-accesible. Este archivo contiene una tabla describiendo esquema de publicación de información similar all ejemplo en AFAZER.


#### 8.3.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.


#### 8.3.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.

Los mismos datos son encontrado como datos estructurados en sintaxis LD+JSON y vocabulario schema.org AFAZER: definir schemas requeridos.
