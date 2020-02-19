# MOTA - Especificación de Transparencia Activa para entidades Gubernamentales 0.3.2
Borrador de editores 19 de febrero de 2020

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



## Tabla de contenido

- [MOTA - Especificación de Transparencia Activa para entidades Gubernamentales 0.3.2](#mota---especificaci%c3%b3n-de-transparencia-activa-para-entidades-gubernamentales-032)
  - [Tabla de contenido](#tabla-de-contenido)
  - [1. Introducción](#1-introducci%c3%b3n)
    - [1.1 Transparencia, Rendición de Cuentas y lucha contra la corrupción](#11-transparencia-rendici%c3%b3n-de-cuentas-y-lucha-contra-la-corrupci%c3%b3n)
    - [1.2 Público objetivo](#12-p%c3%bablico-objetivo)
    - [1.3 Filosofía y Presupuestos](#13-filosof%c3%ada-y-presupuestos)
    - [1.4 Interdisciplinaridad](#14-interdisciplinaridad)
    - [1.5 Regulación](#15-regulaci%c3%b3n)
    - [1.6 Documentos de Apoyo](#16-documentos-de-apoyo)
    - [1.7 Colaboración](#17-colaboraci%c3%b3n)
  - [2. Uso de la especificación](#2-uso-de-la-especificaci%c3%b3n)
  - [3. Conformidad](#3-conformidad)
      - [Información disponible en archivo](#informaci%c3%b3n-disponible-en-archivo)
      - [Información disponible para personas disponibles en la misma página](#informaci%c3%b3n-disponible-para-personas-disponibles-en-la-misma-p%c3%a1gina)
      - [Información disponible como meta-datos estructurados legible por máquina](#informaci%c3%b3n-disponible-como-meta-datos-estructurados-legible-por-m%c3%a1quina)
    - [Observaciones sobre Criterios de Éxito](#observaciones-sobre-criterios-de-%c3%89xito)
    - [Herramientas para examen de conformidad](#herramientas-para-examen-de-conformidad)
      - [WCAG2.1](#wcag21)
    - [3.1 Conformidad de Dependencias](#31-conformidad-de-dependencias)
    - [3.4 Conformance Checkers](#34-conformance-checkers)
  - [4. Términos importantes (vocabulario)](#4-t%c3%a9rminos-importantes-vocabulario)
  - [5. Categoría - Disponibilidad de Acceso](#5-categor%c3%ada---disponibilidad-de-acceso)
    - [5.1 Existencia de sitio Web](#51-existencia-de-sitio-web)
      - [5.1.1. Disponibilidad](#511-disponibilidad)
      - [5.1.1.1 Criterio de Éxito - Nivel AAA](#5111-criterio-de-%c3%89xito---nivel-aaa)
    - [5.2 Régimen de Acceso](#52-r%c3%a9gimen-de-acceso)
      - [5.2.1. Gratuidad](#521-gratuidad)
        - [5.2.1.1. Criterio de Éxito - Nivel AA](#5211-criterio-de-%c3%89xito---nivel-aa)
        - [5.2.1.2. Criterio de Éxito - Nivel AAA](#5212-criterio-de-%c3%89xito---nivel-aaa)
      - [5.2.2 - Universalidad: Acceso directo](#522---universalidad-acceso-directo)
        - [5.2.2.1. Criterio de Éxito - Nivel A](#5221-criterio-de-%c3%89xito---nivel-a)
        - [5.2.2.2. Criterio de Éxito - Nivel AA](#5222-criterio-de-%c3%89xito---nivel-aa)
        - [5.2.2.3. Criterio de Éxito - Nivel AAA](#5223-criterio-de-%c3%89xito---nivel-aaa)
      - [5.2.3 - Universalidad: Patrones de accesibilidad y web standards](#523---universalidad-patrones-de-accesibilidad-y-web-standards)
        - [5.2.3.1. Criterio de Éxito - Nivel A](#5231-criterio-de-%c3%89xito---nivel-a)
        - [5.2.3.2. Criterio de Éxito - Nivel AA](#5232-criterio-de-%c3%89xito---nivel-aa)
        - [5.2.3.3. Criterio de Éxito - Nivel AAA](#5233-criterio-de-%c3%89xito---nivel-aaa)
      - [5.2.4 - Universalidad: Rendimiento](#524---universalidad-rendimiento)
        - [5.2.4.1. Criterio de Éxito - Nivel A](#5241-criterio-de-%c3%89xito---nivel-a)
          - [WebPagetest](#webpagetest)
          - [Pagespeed Insights](#pagespeed-insights)
        - [5.2.4.2. Criterio de Éxito - Nivel AA](#5242-criterio-de-%c3%89xito---nivel-aa)
          - [WebPagetest](#webpagetest-1)
          - [Pagespeed Insights](#pagespeed-insights-1)
        - [5.2.4.3. Criterio de Éxito - Nivel AAA](#5243-criterio-de-%c3%89xito---nivel-aaa)
          - [WebPagetest](#webpagetest-2)
          - [Pagespeed Insights](#pagespeed-insights-2)
      - [5.2.5 - Seguridad: Conexión encriptada](#525---seguridad-conexi%c3%b3n-encriptada)
        - [5.2.5.1. Criterio de Éxito - Nivel AA](#5251-criterio-de-%c3%89xito---nivel-aa)
        - [5.2.5.2. Criterio de Éxito - Nivel AAA](#5252-criterio-de-%c3%89xito---nivel-aaa)
      - [5.2.6 - Dados Abiertos: Acceso vía API REST](#526---dados-abiertos-acceso-v%c3%ada-api-rest)
        - [5.2.6.1. Criterio de Éxito - Nivel AA](#5261-criterio-de-%c3%89xito---nivel-aa)
        - [5.2.6.2. Criterio de Éxito - Nivel AA](#5262-criterio-de-%c3%89xito---nivel-aa)
        - [5.2.6.3. Criterio de Éxito - Nivel AAA](#5263-criterio-de-%c3%89xito---nivel-aaa)
  - [6. Información Mínima Obligatoria sobre la Estructura](#6-informaci%c3%b3n-m%c3%adnima-obligatoria-sobre-la-estructura)
    - [6.1. Estructura orgánica / Organigrama](#61-estructura-org%c3%a1nica--organigrama)
      - [6.1.1. Criterio de Éxito - Nivel A (datos)](#611-criterio-de-%c3%89xito---nivel-a-datos)
      - [6.1.2. Criterio de Éxito - Nivel AA](#612-criterio-de-%c3%89xito---nivel-aa)
      - [6.1.3. Criterio de Éxito - Nivel AAA](#613-criterio-de-%c3%89xito---nivel-aaa)
    - [6.2. Funciones y deberes](#62-funciones-y-deberes)
      - [6.2.1. Criterio de Éxito - Nivel A](#621-criterio-de-%c3%89xito---nivel-a)
      - [6.2.2. Criterio de Éxito - Nivel AA](#622-criterio-de-%c3%89xito---nivel-aa)
      - [6.2.3. Criterio de Éxito - Nivel AAA](#623-criterio-de-%c3%89xito---nivel-aaa)
    - [6.3. Ubicación de sus sedes y áreas, divisiones o departamentos / Localización física, sucursales o regionales](#63-ubicaci%c3%b3n-de-sus-sedes-y-%c3%a1reas-divisiones-o-departamentos--localizaci%c3%b3n-f%c3%adsica-sucursales-o-regionales)
      - [6.3.1. Criterio de Éxito - Nivel A](#631-criterio-de-%c3%89xito---nivel-a)
      - [6.3.2. Criterio de Éxito - Nivel AA](#632-criterio-de-%c3%89xito---nivel-aa)
      - [6.3.3. Criterio de Éxito - Nivel AAA](#633-criterio-de-%c3%89xito---nivel-aaa)
    - [6.4. Divisiones o departamentos](#64-divisiones-o-departamentos)
      - [6.4.1. Criterio de Éxito - Nivel A](#641-criterio-de-%c3%89xito---nivel-a)
      - [6.4.2. Criterio de Éxito - Nivel AA](#642-criterio-de-%c3%89xito---nivel-aa)
      - [6.4.3. Criterio de Éxito - Nivel AAA](#643-criterio-de-%c3%89xito---nivel-aaa)
    - [6.5. Horario de Atención al Público](#65-horario-de-atenci%c3%b3n-al-p%c3%bablico)
      - [6.5.1. Criterio de Éxito - Nivel A](#651-criterio-de-%c3%89xito---nivel-a)
      - [6.5.2. Criterio de Éxito - Nivel AA](#652-criterio-de-%c3%89xito---nivel-aa)
      - [6.5.3. Criterio de Éxito - Nivel AAA](#653-criterio-de-%c3%89xito---nivel-aaa)
    - [6.6. Presupuesto general](#66-presupuesto-general)
      - [6.6.1. Criterio de Éxito - Nivel A](#661-criterio-de-%c3%89xito---nivel-a)
      - [6.6.2. Criterio de Éxito - Nivel AA](#662-criterio-de-%c3%89xito---nivel-aa)
      - [6.6.3. Criterio de Éxito - Nivel AAA](#663-criterio-de-%c3%89xito---nivel-aaa)
    - [6.6. Ejecución histórica anual](#66-ejecuci%c3%b3n-hist%c3%b3rica-anual)
      - [6.6.1. Criterio de Éxito - Nivel A](#661-criterio-de-%c3%89xito---nivel-a-1)
      - [6.6.2. Criterio de Éxito - Nivel AA](#662-criterio-de-%c3%89xito---nivel-aa-1)
      - [6.6.3. Criterio de Éxito - Nivel AAA](#663-criterio-de-%c3%89xito---nivel-aaa-1)
    - [6.7. Planes de gasto público por año fiscal](#67-planes-de-gasto-p%c3%bablico-por-a%c3%b1o-fiscal)
      - [6.7.1. Criterio de Éxito - Nivel A](#671-criterio-de-%c3%89xito---nivel-a)
      - [6.7.2. Criterio de Éxito - Nivel AA](#672-criterio-de-%c3%89xito---nivel-aa)
      - [6.7.3. Criterio de Éxito - Nivel AAA](#673-criterio-de-%c3%89xito---nivel-aaa)
    - [6.8. Directorio de servidores públicos, empleados y contratistas](#68-directorio-de-servidores-p%c3%bablicos-empleados-y-contratistas)
      - [6.8.1. Criterio de Éxito - Nivel A](#681-criterio-de-%c3%89xito---nivel-a)
      - [6.8.2. Criterio de Éxito - Nivel AA](#682-criterio-de-%c3%89xito---nivel-aa)
      - [6.8.3. Criterio de Éxito - Nivel AAA](#683-criterio-de-%c3%89xito---nivel-aaa)
    - [6.9. Directorio de funcionarios - Completo](#69-directorio-de-funcionarios---completo)
      - [6.9.1. Criterio de Éxito - Nivel A](#691-criterio-de-%c3%89xito---nivel-a)
      - [6.9.2. Criterio de Éxito - Nivel AA](#692-criterio-de-%c3%89xito---nivel-aa)
      - [6.9.3. Criterio de Éxito - Nivel AAA](#693-criterio-de-%c3%89xito---nivel-aaa)
    - [6.10. Escalas salariales](#610-escalas-salariales)
      - [6.10.1. Criterio de Éxito - Nivel A](#6101-criterio-de-%c3%89xito---nivel-a)
      - [6.10.2. Criterio de Éxito - Nivel AA](#6102-criterio-de-%c3%89xito---nivel-aa)
      - [6.10.3. Criterio de Éxito - Nivel AAA](#6103-criterio-de-%c3%89xito---nivel-aaa)
    - [6.11. Sanciones aplicadas a servidores públicos](#611-sanciones-aplicadas-a-servidores-p%c3%bablicos)
      - [6.11.1. Criterio de Éxito - Nivel A](#6111-criterio-de-%c3%89xito---nivel-a)
      - [6.11.2. Criterio de Éxito - Nivel AA](#6112-criterio-de-%c3%89xito---nivel-aa)
      - [6.11.3. Criterio de Éxito - Nivel AAA](#6113-criterio-de-%c3%89xito---nivel-aaa)
    - [6.12. Directorio con información de contratos de contratistas - Básico](#612-directorio-con-informaci%c3%b3n-de-contratos-de-contratistas---b%c3%a1sico)
      - [6.12.1. Criterio de Éxito - Nivel A](#6121-criterio-de-%c3%89xito---nivel-a)
      - [6.12.2. Criterio de Éxito - Nivel AA](#6122-criterio-de-%c3%89xito---nivel-aa)
      - [6.12.3. Criterio de Éxito - Nivel AAA](#6123-criterio-de-%c3%89xito---nivel-aaa)
    - [6.13. Directorio con Informaciones de Contratos de Contratistas - Completo](#613-directorio-con-informaciones-de-contratos-de-contratistas---completo)
      - [6.13.1. Criterio de Éxito - Nivel A](#6131-criterio-de-%c3%89xito---nivel-a)
      - [6.13.2. Criterio de Éxito - Nivel AA](#6132-criterio-de-%c3%89xito---nivel-aa)
      - [6.13.3. Criterio de Éxito - Nivel AAA](#6133-criterio-de-%c3%89xito---nivel-aaa)
    - [6.14. Normas generales](#614-normas-generales)
      - [6.14.1. Criterio de Éxito - Nivel A](#6141-criterio-de-%c3%89xito---nivel-a)
      - [6.14.2. Criterio de Éxito - Nivel AA](#6142-criterio-de-%c3%89xito---nivel-aa)
      - [6.14.3. Criterio de Éxito - Nivel AAA](#6143-criterio-de-%c3%89xito---nivel-aaa)
    - [6.15. Normas Reglamentarias](#615-normas-reglamentarias)
      - [6.15.1. Criterio de Éxito - Nivel A](#6151-criterio-de-%c3%89xito---nivel-a)
      - [6.15.2. Criterio de Éxito - Nivel AA](#6152-criterio-de-%c3%89xito---nivel-aa)
      - [6.15.3. Criterio de Éxito - Nivel AAA](#6153-criterio-de-%c3%89xito---nivel-aaa)
    - [6.16. Políticas, lineamientos o manuales](#616-pol%c3%adticas-lineamientos-o-manuales)
      - [6.16.1. Criterio de Éxito - Nivel A](#6161-criterio-de-%c3%89xito---nivel-a)
      - [6.15.2. Criterio de Éxito - Nivel AA](#6152-criterio-de-%c3%89xito---nivel-aa-1)
      - [6.15.3. Criterio de Éxito - Nivel AAA](#6153-criterio-de-%c3%89xito---nivel-aaa-1)
    - [6.17. Metas y Objetivos](#617-metas-y-objetivos)
      - [6.17.1. Criterio de Éxito - Nivel A](#6171-criterio-de-%c3%89xito---nivel-a)
      - [6.17.2. Criterio de Éxito - Nivel AA](#6172-criterio-de-%c3%89xito---nivel-aa)
      - [6.17.3. Criterio de Éxito - Nivel AAA](#6173-criterio-de-%c3%89xito---nivel-aaa)
    - [6.18. Indicadores de gestión y/o desempeño](#618-indicadores-de-gesti%c3%b3n-yo-desempe%c3%b1o)
      - [6.18.1. Criterio de Éxito - Nivel A](#6181-criterio-de-%c3%89xito---nivel-a)
      - [6.18.2. Criterio de Éxito - Nivel AA](#6182-criterio-de-%c3%89xito---nivel-aa)
      - [6.18.3. Criterio de Éxito - Nivel AAA](#6183-criterio-de-%c3%89xito---nivel-aaa)
    - [6.19. Plan anticorrupción y de atención al ciudadano](#619-plan-anticorrupci%c3%b3n-y-de-atenci%c3%b3n-al-ciudadano)
      - [6.19.1. Criterio de Éxito - Nivel A](#6191-criterio-de-%c3%89xito---nivel-a)
      - [6.19.2. Criterio de Éxito - Nivel AA](#6192-criterio-de-%c3%89xito---nivel-aa)
      - [6.19.3. Criterio de Éxito - Nivel AAA](#6193-criterio-de-%c3%89xito---nivel-aaa)
    - [6.20. Plan anual de compras y adquisiciones](#620-plan-anual-de-compras-y-adquisiciones)
      - [6.20.1. Criterio de Éxito - Nivel A](#6201-criterio-de-%c3%89xito---nivel-a)
      - [6.20.2. Criterio de Éxito - Nivel AA](#6202-criterio-de-%c3%89xito---nivel-aa)
      - [6.20.3. Criterio de Éxito - Nivel AAA](#6203-criterio-de-%c3%89xito---nivel-aaa)
  - [7. Información Mínima Obligatoria respecto a Servicios, Procedimientos y Funcionamiento](#7-informaci%c3%b3n-m%c3%adnima-obligatoria-respecto-a-servicios-procedimientos-y-funcionamiento)
    - [7.1. Servicios](#71-servicios)
      - [7.1.1. Criterio de Éxito - Nivel A](#711-criterio-de-%c3%89xito---nivel-a)
      - [7.1.2. Criterio de Éxito - Nivel AA](#712-criterio-de-%c3%89xito---nivel-aa)
      - [7.1.3. Criterio de Éxito - Nivel AAA](#713-criterio-de-%c3%89xito---nivel-aaa)
    - [7.2. Trámites](#72-tr%c3%a1mites)
      - [7.2.1. Criterio de Éxito - Nivel A](#721-criterio-de-%c3%89xito---nivel-a)
      - [7.2.2. Criterio de Éxito - Nivel AA](#722-criterio-de-%c3%89xito---nivel-aa)
      - [7.2.3. Criterio de Éxito - Nivel AAA](#723-criterio-de-%c3%89xito---nivel-aaa)
    - [7.3. Procedimientos de toma de decisiones](#73-procedimientos-de-toma-de-decisiones)
      - [7.3.1. Criterio de Éxito - Nivel A](#731-criterio-de-%c3%89xito---nivel-a)
      - [7.3.2. Criterio de Éxito - Nivel AA](#732-criterio-de-%c3%89xito---nivel-aa)
      - [7.3.3. Criterio de Éxito - Nivel AAA](#733-criterio-de-%c3%89xito---nivel-aaa)
    - [7.4. Decisiones](#74-decisiones)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-%c3%89xito---nivel-a)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-%c3%89xito---nivel-aa)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-%c3%89xito---nivel-aaa)
    - [7.5. Políticas](#75-pol%c3%adticas)
      - [7.5.1. Criterio de Éxito - Nivel A](#751-criterio-de-%c3%89xito---nivel-a)
      - [7.5.2. Criterio de Éxito - Nivel AA](#752-criterio-de-%c3%89xito---nivel-aa)
      - [7.5.3. Criterio de Éxito - Nivel AAA](#753-criterio-de-%c3%89xito---nivel-aaa)
    - [7.4. Mecanismos de participación ciudadana](#74-mecanismos-de-participaci%c3%b3n-ciudadana)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-%c3%89xito---nivel-a-1)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-%c3%89xito---nivel-aa-1)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-%c3%89xito---nivel-aaa-1)
    - [7.5. Informe de participación ciudadana](#75-informe-de-participaci%c3%b3n-ciudadana)
      - [7.5.1. Criterio de Éxito - Nivel A](#751-criterio-de-%c3%89xito---nivel-a-1)
      - [7.5.2. Criterio de Éxito - Nivel AA](#752-criterio-de-%c3%89xito---nivel-aa-1)
      - [7.5.3. Criterio de Éxito - Nivel AAA](#753-criterio-de-%c3%89xito---nivel-aaa-1)
    - [7.6. Mecanismos de participación ciudadana en formulación de políticas](#76-mecanismos-de-participaci%c3%b3n-ciudadana-en-formulaci%c3%b3n-de-pol%c3%adticas)
      - [7.6.1. Criterio de Éxito - Nivel A](#761-criterio-de-%c3%89xito---nivel-a)
      - [7.6.2. Criterio de Éxito - Nivel AA](#762-criterio-de-%c3%89xito---nivel-aa)
      - [7.6.3. Criterio de Éxito - Nivel AAA](#763-criterio-de-%c3%89xito---nivel-aaa)
    - [7.7. Informes de gestión, evaluación y auditoría](#77-informes-de-gesti%c3%b3n-evaluaci%c3%b3n-y-auditor%c3%ada)
      - [7.7.1. Criterio de Éxito - Nivel A](#771-criterio-de-%c3%89xito---nivel-a)
      - [7.7.2. Criterio de Éxito - Nivel AA](#772-criterio-de-%c3%89xito---nivel-aa)
      - [7.7.3. Criterio de Éxito - Nivel AAA](#773-criterio-de-%c3%89xito---nivel-aaa)
    - [7.8. Informes de evaluación](#78-informes-de-evaluaci%c3%b3n)
      - [7.8.1. Criterio de Éxito - Nivel A](#781-criterio-de-%c3%89xito---nivel-a)
      - [7.8.2. Criterio de Éxito - Nivel AA](#782-criterio-de-%c3%89xito---nivel-aa)
      - [7.8.3. Criterio de Éxito - Nivel AAA](#783-criterio-de-%c3%89xito---nivel-aaa)
    - [7.9. Informes de Auditoría](#79-informes-de-auditor%c3%ada)
      - [7.9.1. Criterio de Éxito - Nivel A](#791-criterio-de-%c3%89xito---nivel-a)
      - [7.9.2. Criterio de Éxito - Nivel AA](#792-criterio-de-%c3%89xito---nivel-aa)
      - [7.9.3. Criterio de Éxito - Nivel AAA](#793-criterio-de-%c3%89xito---nivel-aaa)
    - [7.10. Mecanismos internos de supervisión](#710-mecanismos-internos-de-supervisi%c3%b3n)
      - [7.4.1. Criterio de Éxito - Nivel A](#741-criterio-de-%c3%89xito---nivel-a-2)
      - [7.4.2. Criterio de Éxito - Nivel AA](#742-criterio-de-%c3%89xito---nivel-aa-2)
      - [7.4.3. Criterio de Éxito - Nivel AAA](#743-criterio-de-%c3%89xito---nivel-aaa-2)
    - [7.11. Mecanismos externos de supervisión](#711-mecanismos-externos-de-supervisi%c3%b3n)
      - [7.11.1. Criterio de Éxito - Nivel A](#7111-criterio-de-%c3%89xito---nivel-a)
      - [7.11.2. Criterio de Éxito - Nivel AA](#7112-criterio-de-%c3%89xito---nivel-aa)
      - [7.11.3. Criterio de Éxito - Nivel AAA](#7113-criterio-de-%c3%89xito---nivel-aaa)
    - [7.12. Correo electrónico para notificaciones judiciales](#712-correo-electr%c3%b3nico-para-notificaciones-judiciales)
      - [7.12.1. Criterio de Éxito - Nivel A](#7121-criterio-de-%c3%89xito---nivel-a)
      - [7.12.2. Criterio de Éxito - Nivel AA](#7122-criterio-de-%c3%89xito---nivel-aa)
      - [7.12.3. Criterio de Éxito - Nivel AAA](#7123-criterio-de-%c3%89xito---nivel-aaa)
    - [7.13. Mecanismos de Vigilancia](#713-mecanismos-de-vigilancia)
      - [7.13.1. Criterio de Éxito - Nivel A](#7131-criterio-de-%c3%89xito---nivel-a)
      - [7.13.2. Criterio de Éxito - Nivel AA](#7132-criterio-de-%c3%89xito---nivel-aa)
      - [7.13.3. Criterio de Éxito - Nivel AAA](#7133-criterio-de-%c3%89xito---nivel-aaa)
    - [7.14. Procedimientos y Lineamientos de Contratación](#714-procedimientos-y-lineamientos-de-contrataci%c3%b3n)
      - [7.14.1. Criterio de Éxito - Nivel A](#7141-criterio-de-%c3%89xito---nivel-a)
      - [7.14.2. Criterio de Éxito - Nivel AA](#7142-criterio-de-%c3%89xito---nivel-aa)
      - [7.14.3. Criterio de Éxito - Nivel AAA](#7143-criterio-de-%c3%89xito---nivel-aaa)
    - [7.15. Políticas en materia de adquisiciones y compras](#715-pol%c3%adticas-en-materia-de-adquisiciones-y-compras)
      - [7.15.1. Criterio de Éxito - Nivel A](#7151-criterio-de-%c3%89xito---nivel-a)
      - [7.15.2. Criterio de Éxito - Nivel AA](#7152-criterio-de-%c3%89xito---nivel-aa)
      - [7.15.3. Criterio de Éxito - Nivel AAA](#7153-criterio-de-%c3%89xito---nivel-aaa)
  - [8. Instrumentos De Gestión De la Información Pública](#8-instrumentos-de-gesti%c3%b3n-de-la-informaci%c3%b3n-p%c3%bablica)
    - [8.1. Esquemas de publicación de información](#81-esquemas-de-publicaci%c3%b3n-de-informaci%c3%b3n)
      - [8.1.1. Criterio de Éxito - Nivel A](#811-criterio-de-%c3%89xito---nivel-a)
      - [8.1.2. Criterio de Éxito - Nivel AA](#812-criterio-de-%c3%89xito---nivel-aa)
      - [8.1.3. Criterio de Éxito - Nivel AAA](#813-criterio-de-%c3%89xito---nivel-aaa)
    - [8.2. Programa de Gestión Documental](#82-programa-de-gesti%c3%b3n-documental)
      - [8.2.1. Criterio de Éxito - Nivel A](#821-criterio-de-%c3%89xito---nivel-a)
      - [8.2.2. Criterio de Éxito - Nivel AA](#822-criterio-de-%c3%89xito---nivel-aa)
      - [8.2.3. Criterio de Éxito - Nivel AAA](#823-criterio-de-%c3%89xito---nivel-aaa)
    - [8.3. Tablas de retención documental](#83-tablas-de-retenci%c3%b3n-documental)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-%c3%89xito---nivel-a)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-%c3%89xito---nivel-aa)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-%c3%89xito---nivel-aaa)
    - [8.4. Información Publicada Antes De La Ley 1712 De 2014](#84-informaci%c3%b3n-publicada-antes-de-la-ley-1712-de-2014)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-%c3%89xito---nivel-a-1)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-%c3%89xito---nivel-aa-1)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-%c3%89xito---nivel-aaa-1)
    - [8.5. Respuestas a solicitudes de información recibidas](#85-respuestas-a-solicitudes-de-informaci%c3%b3n-recibidas)
      - [8.3.1. Criterio de Éxito - Nivel A](#831-criterio-de-%c3%89xito---nivel-a-2)
      - [8.3.2. Criterio de Éxito - Nivel AA](#832-criterio-de-%c3%89xito---nivel-aa-2)
      - [8.3.3. Criterio de Éxito - Nivel AAA](#833-criterio-de-%c3%89xito---nivel-aaa-2)

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

### 3.1 - Nivel de Éxito - Categorias

Para que una página web esté conforme con esta especificación, debe satisfacer todos y cada uno de los siguientes requisitos de conformidad:

**1. Nivel de conformidad:** Uno de los siguientes niveles de conformidad se satisface por completo.

    **Nivel A:** Para el nivel A de conformidad (el mínimo nivel de conformidad), el sitio web satisface todos los criterios de éxito de nivel A o se proporciona una versión alternativa conforme al nivel A. Si la guía no especifica una puntuación diferente, el cumplimiento del criterio A equivale a **30 puntos**.

    Este es el nivel mínimo aceptable dentro en el contexto de las entidades públicas colombianas a partir de julio de 2019.

    **Nivel AA:** Para el nivel AA de conformidad, el sitio web satisface todos los criterios de éxito de nivel A y AA o se proporciona una versión alternativa conforme al nivel AA. Si la guía no especifica una puntuación diferente, el cumplimiento del criterio A equivale a **50 puntos**.

    Este es el nivel deseado de forma inmediata o a corto plazo, considerando el contexto de las entidades públicas colombianas en julio de 2019.

    **Nivel AAA:** Para el nivel AAA de conformidad, el sitio web satisface todos los criterios de éxito de nivel A, AA y AAA o se proporciona una versión alternativa conforme al nivel AAA. Si la guía no especifica una puntuación diferente, el cumplimiento del criterio AAA equivale a **20 puntos**.

    Este es el nivel ideal, el objectivo a medio y largo plazo a partir de agosto de 2019.

### 3.2 - Escala de puntos: diretrices de disponibilidad de informacción

Las directrices relacionadas a la disponibilidad de informacción adoptan una escala de puntos más completa y no se limita a valorar la disponibilidad o no de la informacion, sino que también incluye la forma y/o ubicación en la que la información está disponible, la adopción de las mejores prácticas de datos abiertos, etc.

La escala de puntos varía de 0 a 100, con las siguientes reglas de puntuación base:

#### Información disponible en archivo
   - en formato propietario (docx, xlsx, pdf): 10 puntos
   - en formato abierto, pero no legible/acesible por máquina (e.g. texto o tabla digitalizado): 20 puntos
   - en formato abierto y datos estructurados (e.g. en caso de tablas) legible/acesible por máquina: 30 puntos

**Importante: si los datos están únicamente en otros sítios (e.g. SECOP, datos.gov.co), la pontuación se reduce a la mitad**

#### Información disponible para personas disponibles en la misma página

   - en formato HTML en la misma página: 30 puntos
   - en HTML5 estructurado, semántico y en la misma página: 50 puntos

#### Información disponible como meta-datos estructurados legible por máquina

   - datos estructurados (schema.org, json, meta-datos, etc) en la misma página: 20 puntos

Los puntajes **pueden ser ligeramente modificadas según el contexto**. Si la información está disponible para el usuario en una página sin descargar archivos, **debe agregarse la puntuación del criterio eliminado (archivo abierto).**

Para directrices no relacionadas a la disponibilidad de informacción, además de cambiar los pesos de critérios (ver abajo), cambiamos la puntuación según fuera necesario. Lo anterior, únicamente si es necesario.

### Observaciones sobre Criterios de Éxito

Nota 1: A pesar de que la conformidad sólo puede lograrse en los niveles indicados, se invita a las entidades públicas a notificar en sus declaraciones cualquier progreso que se realice para satisfacer los criterios de éxito de todo nivel más allá del nivel de conformidad alcanzado.

Nota 2: No se recomienda como política general exigir el nivel de conformidad AAA para sitios enteros porque no es posible que algunos contenidos puedan satisfacer todos los criterios de éxito de nivel AAA.

### Herramientas para examen de conformidad

#### WCAG2.1

- Functional Accessibility Evaluator: https://fae.disability.illinois.edu

### 3.1 Conformidad de Dependencias

(a fazer) como se define conformidad de otras especificaciones, técnicas, etc.

### 3.4 Conformance Checkers
(a fazer)

## 4. Términos importantes (vocabulario)
(a fazer)


## 5. Categoría - Disponibilidad de Acceso

(afazer: intro corta)

### 5.1 Existencia de sitio Web
Tipo: OBLIGACIÓN - Artículo 7 de la Ley 1712 de 2014

La entidad deberá mantener un sitio web, que deberá estar disponible para acesso via una URI oficial por cualquier usuario.

#### 5.1.1. Disponibilidad

El sitio está disponible para acceso vía una URI oficial por cualquier usuario.

#### 5.1.1.1 Criterio de Éxito - Nivel AAA

El sitio retorna páginas con códigos HTTP 200 o 314 en su URI oficial, cuando es accedido por cualquier usuario.

### 5.2 Régimen de Acceso
Tipo: MIXTO

(afazer: intro)

#### 5.2.1. Gratuidad
Tipo: OBLIGACIÓN

El sitio debe tener acceso gratuito a los servicios informáticos que presta la entidad excepto para casos previstos en ley o en los reglamentos.

##### 5.2.1.1. Criterio de Éxito - Nivel AA

Algunos servicios solo son accesibles por contraseña u otro identificador obtenidos a partir de botones y/o otros métodos de pago detectados en el sitio.

##### 5.2.1.2. Criterio de Éxito - Nivel AAA

Todos los servicios son accesibles sin contrapartida financiera, botones u otros métodos de pago.

#### 5.2.2 - Universalidad: Acceso directo
Tipo: RECOMENDACIÓN

Los servicios informáticos que presta la entidad deben ser abiertos a todo el público que desee acceder a ellos y no deben estar restringidos a ciertos usuarios previo registro y recepción de una clave de acceso.

##### 5.2.2.1. Criterio de Éxito - Nivel A

Registro y clave de acceso son necesarios para acceder a una parte del sitio sin una justificación adecuada (e.g. privacidad de datos personales o seguridad).

##### 5.2.2.2. Criterio de Éxito - Nivel AA

Registro y clave de acceso son necesarios para acceder a una parte del sitio con una justificación adecuada (e.g. privacidad de datos personales o seguridad).

##### 5.2.2.3. Criterio de Éxito - Nivel AAA

Todos los servicios son accesibles sin registro previo ni clave de acceso.

#### 5.2.3 - Universalidad: Patrones de accesibilidad y web standards
Tipo: RECOMENDACIÓN

Los sitios deben permitir acceso igualitario por:

   1) Tecnologías de asistencia como lectores de pantalla, asistentes de voz, etc;
   2) Acceso sin uso de javascript o plugins de terceros;
   3) Acceso por dispositivos variados como computadores, teléfonos inteligentes, asistentes de voz (e.g. Amazon Alexa), SmartTVs y otros dispositivos;
   4) Acceso  con distintos tipos de conexiones (banda ancha y 2G/3G de bajo rendimiento), para lo cual deben seguir principios y directrices de accesibilidad conforme a los definidos por la [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/), recomendación WCAG2.1 y WAI-ARIA de W3C y siguiendo las mejores prácticas determinadas en The Web Standards projects para markup sin considerar metadatos o atributos semánticos (e.g. elementos HTML semánticos, sin considerar schema.org o RDF markup).

La evaluación se realizó sobre la página de inicio (ubicación oficial) y otras 20 páginas: 10 de primer nivel, 5 páginas de segundo nivel y 5 de tercer nivel, determinadas según posición en el menú principal y/o directorios en la dirección URL después del nombre de dominio.

##### 5.2.3.1. Criterio de Éxito - Nivel A

El sitio web es válido en el [https://validator.w3.org/unicorn/](https://validator.w3.org/unicorn/) con no más que 50 errores, siguiendo la especificación [HTML5](https://w3c.github.io/html/). **Temporalmente**, la recomendación [XHTML 1.1](https://www.w3.org/TR/xhtml11/) también es aceptada por MOTA.

###### Sobre la aceptación de XHTML

**Temporalmente, debido a la necessidad de compatibilidad con versiones anteriores de sistemas de gerenciamento de contenido**, la recomendación [XHTML 1.1](https://www.w3.org/TR/xhtml11/) también es aceptada por MOTA.

Sin embargo, observamos que XHTML no es la recomendación más reciente y más efectiva para los sitios web para público general. Además, el estándar HTML5 proporciona medios para crear documentos que son válidos como HTML5 y XML. De hecho, XHTML5 és un documento HTML5 enviado con lo MIME Type `application/xhtml+xml` y, preferiblemente, siguiendo el concepto de marcado de texto políglota. Por lo que este solo se aceptará en la versión 1.0 de la especificación MOTA o a partir julio de 2020.

 Más información acerca XML+HTML5 se puede encontrar en inglés en [WHATWG](https://html.spec.whatwg.org/multipage/introduction.html#html-vs-xhtml), [W3C](https://dev.w3.org/html5/html-polyglot/) y [Wikipedia](https://en.wikipedia.org/wiki/Polyglot_markup#Polyglot_HTML_requirements)

##### 5.2.3.2. Criterio de Éxito - Nivel AA

El sitio web es válido en el [https://validator.w3.org/unicorn/](https://validator.w3.org/unicorn/) con no más que 50 errores, siguiendo la especificación [HTML5](https://w3c.github.io/html/) y utilizando los elementos de la especificación de forma semántica. Es decir, utilización correctamente los elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, nav para elemento de navegación etc.).

El sitio cumple con los criterios A de la [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/).

##### 5.2.3.3. Criterio de Éxito - Nivel AAA

El sitio web es válido en el [https://validator.w3.org/unicorn/](https://validator.w3.org/unicorn/)  sin errores y con no más que 50 advertencias, siguiendo la especificación [HTML5](https://w3c.github.io/html/) y utilizando los elementos de la especificación de forma semántica. Es decir, utilización correctamente los elementos HTML de acuerdo a su función (e.g. H1 para encabezado más importante o título, UL para lista de elementos, nav para elemento de navegación etc.).

El sitio cumple con los criterios A y AA de la [Norma Técnica Colombiana (NTC) 5854](https://ntc5854.accesibilidadweb.co/).

El sitio utiliza de forma adequada las prácticas [wai-aria-1.2](https://w3c.github.io/aria/);

#### 5.2.4 - Universalidad: Rendimiento
Tipo: RECOMENDACIÓN

Los sitios deben permitir acceso con velocidad razonable y estable incluso en malas condiciones de acceso, como conexión por dispositivos móviles en redes de bajo rendimiento. Los sitios deben obtener grados mínimos en la herramientas [Webpagetest](http://webpagetest.org/result/190506_KG_29de3021baf30242013b8f58843cd7df/) y Pagespeed Insights, de acuerdo con lo descrito a continuación.

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
    - First Interactive (beta): 30.000s
    - Speed Index: 21.000s
    - Bytes in: 4.096kb

###### Pagespeed Insights
    - Ordenador: 70
    - Móvil: 50

##### 5.2.4.2. Criterio de Éxito - Nivel AA

Los sitios deben obtener los siguientes grados máximos:

###### WebPagetest
    - Time to First Byte: 2.500s
    - First Interactive (beta): 25.000s
    - Speed Index: 14.000s
    - Bytes in: 2.048kb

###### Pagespeed Insights
    - Ordenador: 85
    - Móvil: 60

##### 5.2.4.3. Criterio de Éxito - Nivel AAA

Los sitios deben obtener los siguientes grados máximos:

###### WebPagetest
    - Time to First Byte: 1.500s
    - First Interactive (beta): 15.000s
    - Speed Index: 7.000s
    - Bytes in: 1.536kb

###### Pagespeed Insights
    - Ordenador: 95
    - Móvil: 75

#### 5.2.5 - Seguridad: Conexión encriptada
Tipo: RECOMENDACIÓN

El sitio es accesible en conexión encriptada (SSL/TLS).

##### 5.2.5.1. Criterio de Éxito - Nivel AA

El sitio es accesible en conexión encriptada (SSL/TLS) opcional.

##### 5.2.5.2. Criterio de Éxito - Nivel AAA

El sitio es accesible en conexión encriptada (SSL/TLS) y solamente por conexión criptograda.

#### 5.2.6 - Dados Abiertos: Acceso vía API REST
Tipo: RECOMENDACIÓN

Los contenidos del sitio como páginas, noticias o secciones son accesibles por una API REST con datos estructurados, incluso meta-dados.

##### 5.2.6.1. Criterio de Éxito - Nivel AA

API REST disponible, pero sin meta-datos.

##### 5.2.6.2. Criterio de Éxito - Nivel AA

API REST disponible, con meta-datos.

##### 5.2.6.3. Criterio de Éxito - Nivel AAA

API REST disponible, con meta-datos y en formato JSON.

## 6. Información Mínima Obligatoria sobre la Estructura

Información sobre la estructura del sujeto obligado, de acuerdo con el artículo 9 de la Ley 1712 de 2014.

### 6.1. Estructura orgánica / Organigrama
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 3.4.

El sujeto obligado publica su estructura orgánica de manera gráfica y legible, en un formato accesible y usable. Asismismo, publica una descripción de la estructura orgánica, donde se dé información general de cada división o dependencia.

#### 6.1.1. Criterio de Éxito - Nivel A (datos)

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx), pdf no-accesible, o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.1.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

Cumplimiento alternativos:

Además de lo critério de Éxito

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
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 3.2.

El sujeto obligado publica sus funciones y deberes de acuerdo con su norma de creación o reestructuración. Si alguna norma le asigna funciones adicionales, éstas también están allí incluidas.

#### 6.2.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerrpo de la capa de sesión.

#### 6.2.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página en HTML. (e.g. tablas o listas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.2.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (e.g. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.3. Ubicación de sus sedes y áreas, divisiones o departamentos / Localización física, sucursales o regionales
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 1.2.

Ubicación física del sujeto obligado, de sus sedes, áreas, divisiones, departamentos y/o regionales, según corresponda, incluyendo ciudad y departamento de ubicación.

#### 6.3.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) o disponibles en una página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.3.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en un página en HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. Al menos una ubicación disponible en pie de página.

#### 6.3.3. Criterio de Éxito - Nivel AAA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página en HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. Al menos una ubicación disponible en pie de página. Las informaciones también están  disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org  [GovernmentOffice](https://schema.org/GovernmentOffice), [GovernmentBuilding](https://schema.org/GovernmentBuilding), [Organization](https://schema.org/Organization), [PostalAddress](https://schema.org/PostalAddress).

### 6.4. Divisiones o departamentos
Tipo: OBLIGACIÓN

Informaciones sobre la totalidad de divisiones territoriales. Para considerar como positiva esta pauta, basta con que la información sea general (indicación de cuales son, direcciones, etc.) y no es necesario que todo el contenido del sitio sea el mismo para todas las divisiones territoriales.

#### 6.4.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.4.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en un página, em HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.4.3. Criterio de Éxito - Nivel AAA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página, em HTML5. (e.g. lista , elemento address, etc). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. Al menos una ubicación disponible en pie de página. Las informaciones también estón  disponibles como meta-datos en sintaxis LD+JSON y vocabulario schema.org  [GovernmentOffice](https://schema.org/GovernmentOffice), [GovernmentBuilding](https://schema.org/GovernmentBuilding), [Organization](https://schema.org/Organization) con propriedade [department](https://schema.org/department), [PostalAddress](https://schema.org/PostalAddress).

### 6.5. Horario de Atención al Público
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal a).
Resolución 3564 de 2015, anexo 1, punto 1.2.

Información sobre horarios y días de atención al público de la entidad y sus divisiones en diferentes medios: en la sede, teléfono, correo electrónico, etc. Enlace a los datos de contacto de las sucursales que tenga el sujeto obligado.

#### 6.5.1. Criterio de Éxito - Nivel A

Texto disponible en página específica, accesible por elemento de navegación principal o en el cuerpo de la capa de sesión, incluye horarios de atención de diferentes departamentos o sedes.

#### 6.5.2. Criterio de Éxito - Nivel AA

Texto disponible en página específica, accesible por elemento de navegación principal o en el cuerpo de la capa de sesión, incluye horarios de atención de diferentes departamentos o sedes. Horarios más importante de la sede o servicio principal también disponible en pié de página de todas las páginas.

#### 6.5.3. Criterio de Éxito - Nivel AAA

Texto disponible en página específica, incluye horarios de atención de diferentes departamentos o sedes. Horarios más importante de la sede o servicio principal también disponible en pié de página de todas las páginas. En los dos casos, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org.

### 6.6. Presupuesto general
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal b).
Resolución 3564 de 2015, anexo 1, punto 5.1.

El sujeto obligado publica su presupuesto general para cada año fiscal. Puede ser el presupuesto inicial o final. El presupuesto debe ofrecer datos (valores, ingresos, gastos) de forma clara, organizada y debe estar desagregado conforme se describe a continuación, con encabezados o títulos en paréntesis:

- Ingresos presupuestarios (Ingresos);
- Gastos de personal (Gastos);
- Bienes y servicios de consumo;
- Adquisición de activos no financieros;
- Edificios, mobiliarios y otros;
- Equipos informáticos;
- Programas informáticos;
- Actualizado hasta el último trimestre concluido;

En la base de patrones MOTA, presentamos un modelo de archivo de Datos Presupuestales que cumple con los requisitos y buenas prácticas aquí mencionadas.

Para las entidades u organismos de la Rama Judicial, el requisito se entenderá cumplido a través de un enlace a la publicación del presupuesto general en la página web del Consejo Superior de la Judicatura.

#### 6.6.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.6.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos del tipo hoja de cálculo, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. El archivo sigue el patrón del modelo de archivo Datos Presupuestales disponible en la base de patrones MOTA.

#### 6.6.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.6. Ejecución histórica anual
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal b).
Resolución 3564 de 2015, anexo 1, punto 5.2.

El sujeto obligado publica la información histórica detallada de la ejecución presupuestal aprobada y ejecutada de ingresos y gastos anuales. La información que reposa debe ser al menos de los últimos dos (2) años anteriores al año en ejercicio, con corte a diciembre del período respectivo y debe ser acorde con el reporte enviado al Sistema Integrado de Información Financiera (SIIF), para lo sujetos que aplique.  Los datos pueden ser agregados mensualmente o trimestralmente, idealmente con porcentajes de ejecución, y deben ofrecer datos (gastos, valores, ingresos, gastos) de forma clara, organizada y encontrarse desagregados conforme se describe a continuación, con encabezados o títulos en paréntesis:

- Ingresos presupuestarios (Ingresos);
- Gastos de personal (Gastos);
- Bienes y servicios de consumo;
- Adquisición de activos no financieros;
- Edificios, mobiliarios y otros;
- Equipos informáticos;
- Programas informáticos;
- Actualizado hasta el último trimestre concluido;

En la base de patrones MOTA, presentamos modelos de archivo “Ejecución Presupuestal Mensual” y “Ejecución Presupuestal Trimestral”, que cumplen con los requisitos y buenas prácticas aquí mencionadas.

Para las entidades u organismos de la Rama Judicial, el requisito se entenderá cumplido a través de un enlace a la publicación de la ejecución histórica anual en la página web del Consejo Superior de la Judicatura.

#### 6.6.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf) o disponibles en la página en formato de imagen. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.6.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión. El archivo sigue el patrón de los modelos de archivo “Ejecución Presupuestal Mensual” y “Ejecución Presupuestal Trimestral” en la base de patrones MOTA.

#### 6.6.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.7. Planes de gasto público por año fiscal
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal b).
Resolución 3564 de 2015, anexo 1, punto 6.2.
Ley 1474 de 2011, artículo 74.

El sujeto obligado publica su plan de gasto público para cada año fiscal, en el cual se especifican los objetivos, las estrategias, los proyectos, las metas, los responsables, los planes generales de compras y la distribución presupuestal de sus proyectos de inversión junto a los indicadores de gestión. Así mismo, el plan deberá estar acompañado del informe de gestión del año inmediatamente anterior.

En la base de patrones MOTA, presentamos modelos de archivo ____________________, que cumplen con los requisitos y  buenas prácticas aquí mencionadas.

Para las entidades u organismos de la Rama Judicial, el requisito se entenderá cumplido a través de un enlace a la publicación de los planes de gasto público por año fiscal en la página web del Consejo Superior de la Judicatura.

#### 6.7.1. Criterio de Éxito - Nivel A

AFAZER

#### 6.7.2. Criterio de Éxito - Nivel AA

AFAZER

#### 6.7.3. Criterio de Éxito - Nivel AAA

AFAZER


### 6.8. Directorio de servidores públicos, empleados y contratistas
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal c) y parágrafo 2.
Decreto 103 de 2015, artículo 5.
Resolución 3564 de 2015, anexo 1, punto 3.5.

El sujeto obligado publica en formato accesible y reutilizable el directorio de información de los servidores públicos, empleados y contratistas, incluyendo aquellos que laboran en las sedes, áreas, divisiones, departamentos y/o regionales, según corresponda, con la siguiente información:

- Nombres y apellidos completos
- País, Departamento y Ciudad de nacimiento
- Formación académica
  - Títulos de pregrado y posgrado
  - Instituciones educativas en donde obtuvo los títulos (incluye especificación de seccionales-ciudades)
- Experiencia laboral y profesional
  - Nombres específicos de empleadores previos
  - Cargos anteriores
  - Fecha de inicio y fin en cada cargo
- Empleo, cargo o actividad que desempeña (en caso de contratista, el rol que desempeña con base en el objeto contractual)
- Dependencia en la que presta sus servicios en la entidad o institución
- Dirección de correo electrónico institucional
- Teléfono Institucional y extensión
- Escala salarial según las categorías para servidores públicos y/o empleados del sector privado
- Objeto, valor total de los honorarios, fecha de inicio y de terminación, cuando se trate contratos de prestación de servicios

Para las entidades u organismos públicos, el requisito se entenderá cumplido a través de un enlace a la publicación de la información que contiene el directorio en el Sistema de Información de Empleo Público (SIGEP).
- Nombres y apellidos;
- Direcciones de correo electrónico;
- Teléfono del despacho y dependencia.

#### 6.8.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf) . Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.8.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y/o disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

En caso de que el directorio no contenga alguna de las informaciones requeridas (e.g. no hay correo electrónico), el grado de calificación será disminuido al grado anterior. Es decir, el puntaje obtenido será A y no AA.

#### 6.8.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

En caso de que el directorio no contenga alguna de las informaciones requeridas (e.g. no hay correo electrónico), el grado de calificación será disminuido al grado anterior. Es decir, el puntaje obtenido será A y no AA.


### 6.9. Directorio de funcionarios - Completo
Tipo: OBLIGACIÓN

El sitio web contiene un directorio de funcionarios con sus informaciones completas.

- Nombres y apellidos;
- Direcciones de correo electrónico;
- Teléfono del despacho y dependencia.
- Formación académica
  - Experiencia laboral y profesional
  - Sanciones aplicadas a servidores públicos

 Alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla con las informaciones.

#### 6.9.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla con las informaciones.

#### 6.9.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.9.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.10. Escalas salariales
Tipo: OBLIGACIÓN

Es posible encontrar una tabla con los rangos de salarios de la entidad, identificado por el título "Rangos de salario por nivel", y el decreto de asignaciones salariales de la entidad en un lugar visible. Un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones.

La tabla debe ser actualizada al menos al último año concluido y contiene información sobre el salario base por jerarquía y/o categoría ocupacional, de acuerdo con la categoría, tipo y otras especificidades de la entidad. Ejemplo, en el sitio de la Fiscal General de la Nación se espera encontrar datos separados por jerarquía y/o categoría de fiscales y también por jerarquía y/o categoría ocupacional de otros funcionarios no fiscales.

#### 6.10.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las

#### 6.10.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.10.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.11. Sanciones aplicadas a servidores públicos
Tipo: RECOMENDACIÓN

Es posible encontrar informaciones sobre sanciones disciplinarias o de otro tipo que hayan sido impuestas a funcionarios de la entidad. Hay estadísticas sobre las sanciones impuestas, actualizadas hasta el último año concluIdo y se encuentran desagregadas según el tipo de funcionario (e.g. en el sitio de la Fiscalía General de la Nación las informaciones deben esta desagregadas entre fiscales y otros cargos).

#### 6.11.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.11.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.11.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquemas [Report](https://schema.org/Report), [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.12. Directorio con información de contratos de contratistas - Básico
Tipo: OBLIGACIÓN

Es posible encontrar informaciones sobre los contratos de contratistas en formatos abiertos. Alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones.

- Nombres y apellidos;
- Direcciones de correo;
- Teléfono del despacho y dependencia;
- Objeto del contrato.

#### 6.12.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, xlsx, pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión; alternativamente, un enlace al SIGEP es válido, pero sólo si se especifica que ahí se puede entrar y encontrar esta información y cuando se abre el enlace, se abre directamente la tabla com las informaciones

#### 6.12.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.12.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.13. Directorio con Informaciones de Contratos de Contratistas - Completo
Tipo: OBLIGACIÓN

El sitio web contiene un directorio de funcionarios de sus informaciones completas.

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

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.13.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [employees](https://schema.org/employees) y [GovernmentOrganization](https://schema.org/GovernmentOrganization). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.14. Normas generales
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 4.

El sujeto obligado publica la normatividad de orden constitucional o legal que lo rige, que determina su competencia y le es aplicable a su actividad. Existencia de una sección con normas y reglamentos pertinentes para la entidad: decretos, circulares, leyes, etc., relativas a creacción de reglamentos de la entidad. El documento MOTA “Reglas Contextuales” especifica cuáles son las normas necesarias por entidad o clases de entidad. Dos versiones están disponibles:

- Listado de normas de orden constitucional o legal que indique nombre, fecha de expedición y una descripción corta de la misma, organizadas de la más reciente a la más antigua.
- Un enlace que redirija al usuario a un archivo o recurso con el documento integral.

#### 6.14.1. Criterio de Éxito - Nivel A

Resumen disponible en la página en HTML. Con normas disponibles para bajar en formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.14.2. Criterio de Éxito - Nivel AA

Resumen disponible en la página en HTML, en lenguaje sencillo, con normas completas disponibles también en HTML en la misma página o en otra página en el mismo sitio. Para las normas completas, archivos en formatos abiertos (e.g. odf) accesibles en el mismo sitio y dominio es válido. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.14.3. Criterio de Éxito - Nivel AAA

Resumen disponible en la página, en HTML, en lenguaje sencillo, con normas completas disponibles también en HTML en la misma página o en otra página en el mismo sitio. En los dos casos, el contenido es estructurado semánticamente (i.e. elementos HTML5 apropiados) y sus meta-datos disponibles en sintaxis LD+JSON y vocabulario schema.org segundo esquema [legislation](https://schema.org/Legislation) y [LegislationObject](https://schema.org/LegislationObject). Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.15. Normas Reglamentarias
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 4.

El sujeto obligado publica el decreto único reglamentario sectorial, que compila todas las normas reglamentarias vigentes del sector administrativo del que hace parte. Por medio de este decreto se debe generar el acceso a las normas compiladas a través de hipervínculos. Esta información debe ser descargable y en un formato que facilite la búsqueda del texto dentro del documento, así como su continua actualización. Asimismo, el sujeto obligado agrega a través de hipervínculos la referencia a todos los actos que adicionen, modifiquen o deroguen cualquiera de las disposiciones del decreto único reglamentario sectorial, así como a las decisiones judiciales que declaren la nulidad de apartes del decreto.

Además, se publican los decretos no compilados, como los de estructura, salarios, decretos que desarrollan leyes marco, entre otros. Esta información debe ser descargable.

Así mismo, si existen resoluciones, circulares u otro tipo de actos administrativos de terceros o que produce el mismo sujeto obligado para el desarrollo de sus funciones, se publica en dos versiones:
- un listado que indique el tipo de acto (resolución, circular, ordenanza, acuerdo, etc.), la fecha de expedición y una descripción corta del mismo (verbatim), organizados del más reciente al más antiguo.
- un enlace que redirija al usuario a un archivo o recurso con el documento integral.

 Existencia de información sobre normas reglamentarias pertinentes a la entidad: resoluciones y directivas. El documento MOTA “Reglas Contextuales” especifica cuáles son las normas necesarias por entidad o clases de entidad. Dos están disponibles:

- Resumen en lenguaje sencillo, destacando secciones de reglamentos pertinentes;
- Copias literales de las normas.
  - En casos de documentos largos y cuyo alcance exceda el tema de Normas generales, está permitido copias verbatim de apenas las seccionespertinentes, pero es necesario un enlace que redirija al usuario a un archivo o recurso con el documento integral.

#### 6.15.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.15.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.15.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.16. Políticas, lineamientos o manuales
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.1.
Ley 1474 de 2011, artículo 73.


El sujeto obligado publica sus lineamientos, manuales y toda política que haya adoptado y afecte al público, junto con sus fundamentos y toda interpretación autorizada de ellas. Entre las políticas, lineamientos y manuales pueden estar (lista ilustrativa, no taxativa):

- Políticas y lineamientos sectoriales e institucionales.
- Manuales.
- Planes estratégicos, sectoriales e institucionales.
- Plan de rendición de cuentas.
- Plan de servicio al ciudadano.
- Plan anticorrupción.

Si el sujeto obligado realiza un plan de acción unificado, es válido.


#### 6.16.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.15.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.15.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org según esquema. [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.17. Metas y Objetivos
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.4.


El sujeto obligado y sus unidades administrativas publican la información relacionada con sus metas y objetivos, de conformidad con sus programas operativos y los demás planes exigidos por la normatividad.

Se debe publicar su estado de avance, mínimo cada tres (3) meses.

#### 6.17.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.17.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.17.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.


### 6.18. Indicadores de gestión y/o desempeño
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal d).
Resolución 3564 de 2015, anexo 1, punto 6.4.

Las entidades deben proveer información sobre los indicadores de gestión y/o desempeño que utilizan y reportes con estadísticas y análisis del desempeño de la entidad en relación a sus programas operativos y los demás planes exigidos por la normatividad.

#### 6.18.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.18.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.18.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.19. Plan anticorrupción y de atención al ciudadano
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal g).
Ley 1474 de 2011, artículo 73.

El sujeto obligado publica anualmente una estrategia de lucha contra la corrupción y de atención al ciudadano. Dicha estrategia contempla, entre otras cosas:
- el mapa de riesgos de corrupción en la respectiva entidad;
- las medidas concretas para mitigar esos riesgos;
- las estrategias anticorrupción;
- los mecanismos para mejorar la atención al ciudadano.


#### 6.19.1. Criterio de Éxito - Nivel A

Datos disponibles en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.19.2. Criterio de Éxito - Nivel AA

Datos disponibles en archivos, formatos abiertos (e.g. .odf) y disponibles en la página en HTML. (e.g. tablas). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.19.3. Criterio de Éxito - Nivel AAA

Texto disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados) y disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org segundo esquema [ServiceChannel](https://schema.org/ServiceChannel), y [ContactPoint](https://schema.org/ContactPointOption), [DayOfWeek](https://schema.org/DayOfWeek) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 6.20. Plan anual de compras y adquisiciones
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 9, literal e).
Decreto 103 de 2015, artículo 10.
Resolución 3564 de 2015, anexo 1, punto 8.4.
Ley 1474 de 2011, artículo 74.
Decreto 1510 de 2013, artículos 3, 4, 5, 6 y 7.

El sujeto obligado que contrata con cargo a recursos públicos publica en su página web y en el Sistema Electrónico de Contratación Pública (SECOP) su plan general de compras, entendido como un instrumento de planeación contractual que las Entidades Estatales deben diligenciar, publicar y actualizar por lo menos una vez durante su vigencia y: (i) cuando haya ajustes en los cronogramas de adquisición, valores, modalidad de selección, origen de los recursos; (ii) para incluir nuevas obras, bienes y/o servicios; (iii) excluir obras, bienes y/o servicios; o (iv) modificar el presupuesto anual de adquisiciones. El plan debe compreender:

- La lista de bienes, obras y servicios que se pretenden adquirir durante el año.
- La necesidad ( y cuando conoce el bien, obra o servicio que satisface esa nece­sidad debe identificarlo utilizando el Clasificador de Bienes y Servicios)
- El valor estimado del contrato
- El tipo de recursos con cargo a los cuales la Entidad Estatal pagará el bien, obra o servicio
- La modalidad de selección del contratista
- La fecha aproximada en la cual la Entidad Estatal iniciará el Proceso de Contratación. - Proceso de Gestión Contractual / Procedimiento Plan Anual de Adquisiciones

El documento MOTA "Reglas Contextuales" especifica cuáles son las normas necesarias por entidad o clases de entidad.

#### 6.20.1. Criterio de Éxito - Nivel A

Información disponible en archivos, formatos propietarios (e.g. .docx, .xlsx, .pdf), con links al SECOP. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.20.2. Criterio de Éxito - Nivel AA

Contenido del Plan disponible en la página, estructurado semánticamente (i.e. elementos HTML5 apropiados). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 6.20.3. Criterio de Éxito - Nivel AAA
Proceso de Gestión Contractual y lista de documentos disponibles en la página, estructurados semánticamente (i.e. elementos HTML5 apropiados), información de contratos disponible en archivos, en formatos abiertos (e.g. .odf), incluyendo links para el SECOP. Meta-dados de la colección de documentos contienen nombre del documento, autor, data de actualización, URI y enlace para el SECOP) en sintaxis LD+JSON y vocabulario schema.org según esquema [Collection](https://schema.org/Collection), [DigitalDocument](https://schema.org/DigitalDocument) y relacionados. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

## 7. Información Mínima Obligatoria respecto a Servicios, Procedimientos y Funcionamiento

Información Mínima Obligatoria respecto a servicios, procedimientos y funcionamiento, de acuerdo con el artículo 11 de la Ley 1712 de 2014.

### 7.1. Servicios
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal a).
Decreto 103 de 2015, artículo 6.
Resolución 3564 de 2015, anexo 1, punto 9.

El sitio del sujeto obligado contiene una o más páginas con información de los servicios que brinda directamente al público, incluyendo:
- La norma que los sustenta
- Proceso a seguir
- Costos asociados
- Formularios y formatos requeridos
- Protocolos de atención a los siguientes públicos: 1) Ciudadanos en general; 2) Prensa; 3) grupos de interés, según la entidad.
- Indicación de aquellos que se encuentren disponibles en línea.

El documento MOTA “Reglas Contextuales” especifica cuáles son las normas necesarias por entidad o clases de entidad.

#### 7.1.1. Criterio de Éxito - Nivel A

Informaciones disponibles en una o más páginas interligadas, en HTML, con modelos de formularios y formatos disponibles en archivos (e.g. .pdf, .xlsx, o .docx). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.1.2. Criterio de Éxito - Nivel AA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.1.3. Criterio de Éxito - Nivel AAA

Informaciones disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.2. Trámites
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal b).
Decreto 103 de 2015, artículo 6.
Resolución 3564 de 2015, anexo 1, punto 9.

El sujeto obligado publica toda la información correspondiente a los trámites que se pueden agotar en la entidad, incluyendo:
- La norma que los sustenta
- Proceso a seguir
- Costos asociados
- Formularios y formatos requeridos
- Indicación de aquellos que se encuentren disponibles en línea.

Además de informaciones acerca cada trámite, se recomienda una tabla resumen listando costos, normativa y link para informaciones en detalles de cada trámite.

Los trámites mínimos requeridos para cada entidad o clases de entidades se encuentran en el documento MOTA “Reglas Contextuales”.

Este requisito se entenderá cumplido con la inscripción de los trámites en el Sistema Único de Información de Trámites y Procedimientos Administrativos (SUIT) y la relación de los nombres de los mismos en el respectivo sitio web oficial del sujeto obligado con un enlace al portal del Estado Colombiano o el que haga sus veces.

#### 7.2.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, en HTML, con modelos de formularios y formatos disponibles en archivos (e.g. .pdf, xlsx, o .docx). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.


#### 7.2.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), incluso una tabla listando costos, normativas y links para información en detalle de cada trámite. Incluye modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.2.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), incluso una tabla listando costos, normativas y link para informaciones en detalles de cada trámite, y modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.3. Procedimientos de toma de decisiones
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal c).
Resolución 3564 de 2015, anexo 1, punto 3.3.

El sujeto obligado publica la descripción de los procesos y procedimientos que se siguen para tomar decisiones en las diferentes áreas. Los procedimientos mínimos requeridos para cada entidad o clases de entidad se encuentran en el documento MOTA “Reglas Contextuales”.

Ejemplo: Procedimientos mínimos Fiscalía General de la Nación:

1. Investigación de conductas punibles
2. Acusación de presuntos infractores de la ley ante juzgados y tribunales competentes
3. Coordinación de las funciones de policía judicial
4. Creación o supresión de direcciones de la Fiscalía
5. Decisiones sobre protección a víctimas
6. Decisiones sobre política criminal

#### 7.3.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si apoyos visuales son necessario, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.3.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.3.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.4. Decisiones
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal d).

El sujeto obligado publica los contenidos de las decisiones adoptadas que afecten al público, junto con sus fundamentos e interpretaciones. Los tipos de decisiones mínimos requeridos para cada entidad o clases de entidad se encuentran en el documento MOTA “Reglas Contextuales”.

Ejemplo: listado de decisiones mínimas que debe contener el sitio de la Corte Constitucional:

1. Sentencias de tutela
2. Sentencias de constitucionalidad
3. Autos
4. Acuerdo de Sala Plena

Además de la publicación de información acerca cada decisión, se recomienda una tabla o listado de decisiones organizadas de forma cronológica en reversa (i.e. las decisiones más recientes al inicio de la lista).

#### 7.4.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.4.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.5. Políticas
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con los contenidos de las políticas adoptadas que afecten al público, junto con sus fundamentos e interpretaciones. Los procedimientos mínimos requeridos para cada entidad o clases de entidad se encuentran en el documento MOTA “Reglas Contextuales”.

Ejemplo: listado de políticas mínimas que debe contener el sitio de la Fiscalía General de la Nación:

1. Política pública de priorización.
   1. Incluso criterios de priorización.
2. Políticas en materia de internacionalización para afrontar transnacionalidad de delitos.
3. Políticas de adopción y aplicación de enfoques diferenciales.
4. Políticas sobre investigación de crimen organizado.
5. Resultados de las políticas adoptadas.
   1.  Incluso resultados y casos emblemáticos.

Además de la información acerca cada política, se recomienda una tabla o listado de políticas organizadas de forma cronológica en reversa (i.e. las decisiones más recientes en al principio de la lista).

#### 7.5.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillp. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.5.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.5.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.4. Mecanismos de participación ciudadana
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal h).
Resolución 3564 de 2015, anexo 1, puntos 1.1, 2.4 y 10.9.
Resolución 3564 de 2015, anexo 2.

El sujeto obligado dispone de canales para la atención al ciudadano y para recibir peticiones, quejas, reclamos, denuncias y solicitudes de información pública, tales como:
Teléfonos fijos y móviles, con líneas gratuitas y fax, incluyendo el indicativo nacional e internacional en el formato (+57 número del área respectiva).
Correo electrónico institucional para la recepción de solicitudes de información.
Correo físico o postal para la recepción de solicitudes de información.
Link al formulario electrónico de solicitudes, peticiones, quejas, reclamos.

Además, el sujeto obligado ofrece una lista de preguntas frecuentes con las respectivas respuestas, relacionadas con su gestión y los servicios y trámites que presta.


#### 7.4.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necesarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.4.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

En caso de un gran número de preguntas frequentes, un formulario de búsqueda debe estar presente.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf).

En caso de un gran número de preguntas frequentes, un formulario de búsqueda debe estar presente.

Información disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.5. Informe de participación ciudadana
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal h).
Decreto 103 de 2015, artículo 52.
Resolución 3564 de 2015, anexo 1, punto 10.10.

El sujeto obligado publica un informe de todas las peticiones, quejas, reclamos, denuncias y solicitudes de acceso a información pública recibidas, los tiempos de respuesta del sujeto obligado y un análisis resumido de este tema. Respecto de las solicitudes de acceso a información pública, el informe debe discriminar la siguiente información mínima agregada:

- El número de solicitudes recibidas.
- El número de solicitudes que fueron trasladadas a otra institución.
- El tiempo de respuesta a cada solicitud.
- El número de solicitudes en las que se negó el acceso a la información.


#### 7.5.1. Criterio de Éxito - Nivel A

Estadísticas agregadas y análisis disponibles en una o más páginas estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en un archivo .xls o .xlsx.

#### 7.5.2. Criterio de Éxito - Nivel AA

Estadísticas agregadas y análisis disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en archivos con formatos abiertos (.csv o .odf).

#### 7.5.3. Criterio de Éxito - Nivel AAA

Estadísticas agregadas y análisis disponibles en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con descripciónes textuales en lenguaje sencilla. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

El conjunto de datos con todas las solicitudes, denuncias y tiempos de respuesta está disponible en archivos con formatos abiertos (.csv o .odf) y también como meta-datos en sintaxis LD+JSON y vocabulario schema.org.

### 7.6. Mecanismos de participación ciudadana en formulación de políticas
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 11, literal i).
Decreto 103 de 2015, artículo 15.
Resolución 3564 de 2015, anexo 1, punto 6.5.

El sujeto obligado publica información sobre todo mecanismo o procedimiento al que deben sujetarse los ciudadanos, usuarios o interesados en participar en la formulación de la política, en el ejercicio de las facultades de ese sujeto obligado, o en el control o evaluación de la gestión institucional, indicando:
- Los sujetos que pueden participar
- Los medios presenciales y electrónicos
- Las áreas responsables de la orientación y vigilancia para su cumplimiento.
Este ítem incluye la publicidad de invitaciones públicas, convocatorias o procesos de participación pública.

#### 7.6.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), con descripciones textuales en lenguaje sencillo. Si los apoyos visuales son necessarios, estos deben estar en formato de imagen (.jpg o .png). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.6.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.6.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A, AA y AAA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos formatos abiertos (e.g. .odf). Informaciones también disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org. Accesible por elemento de navegación principal o en el cuerpo de la capa de sesión.

### 7.7. Informes de gestión, evaluación y auditoría
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 10, literal d) y artículo 11, literal e).
Resolución 3564 de 2015, anexo 1, punto 7.1.

El sujeto obligado publica todos los informes de gestión, evaluación y auditoría. Para los sujetos obligados que aplique, como mínimo, deben publicar -dentro del mes en el que se envió o realizó el evento, según corresponda- los siguientes informes:

Informe enviado al Congreso / Asamblea / Consejo.
Informe de rendición de la cuenta fiscal a la Contraloría General de la República o a las Contralorías Territoriales, según corresponda.
Informe de rendición de cuentas a los ciudadanos, incluyendo la respuesta a las solicitudes de los ciudadanos antes y durante el ejercicio de rendición.
Informes a organismos de inspección, vigilancia y control.
Informe de la auditoría al ejercicio presupuestal.

Idealmente, los informes deben ser presentarnos en páginas HTML, pero archivos también son válidos.


#### 7.7.1. Criterio de Éxito - Nivel A

El sitio contiene una página de informes de gestión, evaluación y auditoría con listado o tabla de links para descargar los reportes en archivos PDF, PPT o DOC del periodo vigente y de anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia.

#### 7.7.2. Criterio de Éxito - Nivel AA

El sitio contiene una página Informes de gestión, evaluación y auditoría con listado o tabla de links para descargar los reportes en archivos PDF, PPT o DOC del periodo vigente y de anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.7.3. Criterio de Éxito - Nivel AAA

El sitio contiene una página Informes de gestión, evaluación y auditoría con listado o tabla de links para descargar los reportes en archivos PDF, PPT o DOC del  período vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencilla y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formulários y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

La misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.8. Informes de evaluación
Tipo: OBLIGACIÓN

AFAZER: aclarar

El sitio de la entidad debe contener Informes de Evaluación del periodo vigente y de los períodos anteriores, sobre contratación, entre otros.

Idealmente, los informes deben ser presentarnos en páginas HTML, pero archivos también son válidos.

#### 7.8.1. Criterio de Éxito - Nivel A

El sitio contiene una página de Informes de Evaluación con listado o tabla de links para descargar los reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia.

#### 7.8.2. Criterio de Éxito - Nivel AA

El sitio contiene una página Informes de Evaluación con listado o tabla de links para descargar los reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.8.3. Criterio de Éxito - Nivel AAA

El sitio contiene una página Informes de Evaluación con listado o tabla de links para descargar los reportes en archivos PDF, PPT o DOC del período vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

La misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.9. Informes de Auditoría
Tipo: OBLIGACIÓN


AFAZER: aclarar

El sitio de la entidad debe contener Informes de Auditoría del período vigente y de los anteriores, sobre contratación, entre otros.

Idealmente, los informes deben ser presentados en páginas HTML, pero archivos también son válidos.

#### 7.9.1. Criterio de Éxito - Nivel A

El sitio contiene una página de Informes de Auditoría con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia.

#### 7.9.2. Criterio de Éxito - Nivel AA

El sitio contiene una página de Informes de Auditoría con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencillo y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

#### 7.9.3. Criterio de Éxito - Nivel AAA

El sitio contiene una página de Informes de Auditoría con listado o tabla de links para reportes en archivos PDF, PPT o DOC del periodo vigente y de los anteriores.

Esta página está estructurada semánticamente (i.e. elementos HTML5 apropiados), con descripción textual en lenguaje sencilla y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con modelos de formularios y formatos disponibles en archivos, formatos abiertos (e.g. .odf). Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión.

La misma información disponible en el listado está disponible como meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.10. Mecanismos internos de supervisión
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 10, literal d) y artículo 11, literal f).
Resolución 3564 de 2015, anexo 1, puntos 7.2, 7.3, y 7.4.

El sujeto obligado publica información relacionada con los informes, planes de mejoramiento, entes y mecanismos de supervisión y control que existen al interior del sujeto obligado, incluyendo como mínimo:

Ente de control interno que vigila al sujeto obligado:  El sitio de la entidad contiene una o más páginas con información acerca de la Oficina de Control Interno, de manera que los funcionarios o la ciudadanía tengan claro que hay una dependencia a la que se puede acudir para presentar denuncias u observaciones acerca del funcionamiento interno de la entidad. En este sentido, se puede encontrar información sobre las funciones (la misión o los objetivos), los procesos ( cómo se hace efectiva una sanción, entre otros.) o mecanismos (que instrumentos de denuncia tienen) de la Oficina. También se vale información que explique la diferencia entre el control interno disciplinario y el control interno de gestión.
Reportes de control interno: El sujeto obligado publica como mínimo el informe pormenorizado del estado del control interno. Dicho informe se debe publicar cada cuatro (4) meses.
Planes de mejoramiento: El sujeto obligado publica los Planes de Mejoramiento vigentes exigidos por el ente de control interno.

#### 7.4.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.4.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.4.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.11. Mecanismos externos de supervisión
Tipo: OBLIGACIÓN
Ley 1712 de 2014, artículo 10, literal d) y artículo 11, literal f).
Resolución 3564 de 2015, anexo 1, puntos 7.3 y 7.4.

El sujeto obligado publica información relacionada con los informes, planes de mejoramiento, entes y mecanismos de supervisión y control externo, incluyendo como mínimo:

Entes de control externo que vigilan al sujeto obligado y mecanismos de supervisión:  El sujeto obligado publica la relación de todas las entidades que lo vigilan y de los mecanismos externos de supervisión, notificación y vigilancia pertinente que existen frente al sujeto obligado. Para ello se debe indicar como mínimo:
Tipo de control que se ejecuta (e.g. fiscal, disciplinario, político, social, etc.)
Planes de mejoramiento: El sujeto obligado publica los Planes de Mejoramiento vigentes exigidos por entes de control externo. Así mismo, cuenta con un enlace al sitio web del organismo de control en donde se encuentren los informes que éste ha elaborado sobre el respectivo sujeto obligado.

Asimismo, el sujeto obligado informa sobre la manera como un particular puede comunicar una irregularidad ante los entes que ejercen supervisión y control sobre el sujeto obligado.


#### 7.11.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.11.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.11.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.12. Correo electrónico para notificaciones judiciales
Tipo: OBLIGACIÓN
Resolución 3564 de 2015, anexo 1, punto 1.3.

El sujeto obligado publica la dirección de correo electrónico para notificaciones judiciales, la cual debe estar disponible en el pie de página de la página principal del sitio del sujeto obligado, así como en la sección de Atención al Ciudadano. El correo para notificaciones judiciales debe estar configurado de forma tal que envíe acuse de recibo al remitente de forma automática.


#### 7.12.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.12.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.12.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.13. Mecanismos de Vigilancia
Tipo: OBLIGACIÓN

AFAZER

#### 7.13.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.13.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.13.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.14. Procedimientos y Lineamientos de Contratación
Tipo: OBLIGACIÓN

El sitio de la entidad debe contener una o más páginas con los procedimientos y lineamientos de contratación.

Documentos ex-ante (de planeación o tipo manual) que den guía sobre cómo se va a proceder para hacer algo), formulado por la entidad. Pudo ser formulado en una vigencia diferente a la actual. Publicación de documentos que den guía sobre cómo se maneja la contratación en la entidad según cada modalidad. En la mayoría de casos, estos lineamientos se consolidan en un documento llamado "Manual de Contratación".

#### 7.14.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf non-accesible.

#### 7.14.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.14.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [Report](https://schema.org/Report), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 7.15. Políticas en materia de adquisiciones y compras
Tipo: OBLIGACIÓN

AFAZER: aclarar

La entidad debe ofrecer información de su plan de adquisiciones. El documento MOTA "Reglas Contextuales" especifica cuáles son las normas necesarias por entidad o clases de entidad. El plan debe compreender:

- Proceso de Gestión Contractual / Procedimiento Plan Anual de Adquisiciones
- Datos/procesos de adjudicación de los contratos
- Datos/procesos de ejecución de los contratos

#### 7.15.1. Criterio de Éxito - Nivel A

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .doc, .ppt o .pdf no-accesible.Información disponible en archivos, formatos propietarios (e.g. .docx, xlsx), pdf no-accesible, con links para SECOP. Accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión;

#### 7.15.2. Criterio de Éxito - Nivel AA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

#### 7.15.3. Criterio de Éxito - Nivel AAA

Información disponible en una o más páginas interligadas, estructuradas semánticamente (i.e. elementos HTML5 apropiados) y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión, y modelos de formatos disponibles en archivos .odf o **.pdf accesible**.

Los meta-datos en sintaxis LD+JSON y vocabulario schema.org [DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

## 8. Instrumentos De Gestión De la Información Pública
(afazer: intro)

Información respecto a instrumentos de gestión de la información pública requeridos por la Ley 1712 de 2014.

### 8.1. Esquemas de publicación de información
Tipo: OBLIGACIÓN

AFAZER: aclarear este ítem. Que ejemplos de información teríamos aqui?

El sitio de la entidad debe contener una o más páginas con informaciones de Esquemas de Publicación de información, publicadas en una página denominada "Acceso a información pública" y estable i) qué tipo de información está publicada en el sitio web ii) qué información se publicará de manera proactiva iii) formatos de publicación iv) idioma v) responsable de la producción de información vi) la periodicidad en la divulgación, entre otros.

Un ejemplo de esquema de publicación, en archivo xls, se encuentra en el enlace: https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2

#### 8.1.1. Criterio de Éxito - Nivel A

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados) com el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf no-accesible. Este archivo contiene una tabla describiendo esquema de publicación de información similar all ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.


#### 8.1.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad com directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

También es aceptable, para la tabla, un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene una tabla describiendo esquema de publicación de información similar al ejemplo en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.


#### 8.1.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo disponible en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

También es aceptable, para publicar la tabla, un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene una tabla describiendo el esquema de publicación de información similar al ejemplo disponible en https://www.funcionpublica.gov.co/documents/418537/506991/Esquema+Publicaci%C3%B3n+2014.pdf/c64f12c8-dda2-451b-82d5-b58cba9b14f2.

Los mismos datos de la tabla son encontrado como datos estructurados en sintaxis LD+JSON y vocabulario schema.org [ItemList](https://schema.org/ItemList), [ListItem](https://schema.org/ListItem),[DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 8.2. Programa de Gestión Documental
Tipo: OBLIGACIÓN

AFAZER: aclarar

El sitio de la entidad debe contener una o más páginas con informaciones de Programa de Gestión Documental, publicadas en una página denominada "Gestión Documental" e informar "procedimientos y lineamientos necesarios para la producción, distribución, organización, consulta y conservación de los documentos públicos". Comprende la vida del documento desde su creación hasta su disposición final.

Un ejemplo de Programa de Gestión Documental se encuentra en el enlace: http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

#### 8.2.1. Criterio de Éxito - Nivel A

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados) con el título "Gestión Documental", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y link para un archivo de formato propietario (.doc, .ppt) o .pdf no-accesible. Este archivo de procedimientos y lineamientos necesarios para la producción, distribución, organización, consulta y conservación de los documentos públicos es similar al ejemplo disponible en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf


#### 8.2.2. Criterio de Éxito - Nivel AA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y deconformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo esquema de publicación de información similar al ejemplo en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

También es aceptable para los procedimientos y lineamientos un archivo de formato abierto (.odf) o **.pdf accesible**.


#### 8.2.3. Criterio de Éxito - Nivel AAA

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título "acceso a información pública", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y una tabla en HTML5 describiendo el esquema de publicación de información similar al ejemplo disponible en http://www.mintic.gov.co/portal/604/articles-7077_Programa_Gestion_Documental.pdf

También es aceptable para los procedimiento y lineamientos un archivo de formato abierto (.odf) o **.pdf accesible**.

Los meta-datos de la página y cualquier documento o archivo accesorio son encontrados como datos estructurados en sintaxis LD+JSON y vocabulario schema.org [ItemList](https://schema.org/ItemList), [ListItem](https://schema.org/ListItem),[DigitalDocument](https://schema.org/DigitalDocument), [GovernmentOrganization](https://schema.org/GovernmentOrganization) y relacionados.

### 8.3. Tablas de retención documental
Tipo: OBLIGACIÓN

AFAZER: aclarar

#### 8.3.1. Criterio de Éxito - Nivel A

El sitio ofrece página estructurada semánticamente (i.e. elementos HTML5 apropiados) com el título "AFAZER", accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y un link para un archivo de formato propietario (.doc, .ppt) o .pdf no-accesible. Este archivo contiene una tabla describiendo el esquema de publicación de información similar al ejemplo en AFAZER.


#### 8.3.2. Criterio de Éxito - Nivel AA

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y de conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), com el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.


#### 8.3.3. Criterio de Éxito - Nivel AAA

El sitio ofrece una página estructurada semánticamente (i.e. elementos HTML5 apropiados)  y en conformidad con directrices Nivel A y AA de [WCAG 2.1](https://w3c.github.io/wcag/21/guidelines/), con el título AFAZER, accesible por elemento de navegación secundario o en el cuerpo de la capa de sesión transparencia, que contiene una introducción y AFAZER HTML5 describiendo AFAZER.

También es aceptable un archivo de formato abierto (.odf) o **.pdf accesible**, que contiene AFAZER similar a el ejemplo en AFAZER.

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

### 8.5. Respuestas a solicitudes de información recibidas
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

Atajos:

- [a criterios](#5-Categor%C3%ADa---Disponibilidad-de-Acceso)
- [Tabla de contenido](#Tabla-de-contenido)


Este documento está escrito utilizando la sintaxis Markdown:

https://www.markdownguide.org/getting-started
https://www.markdownguide.org/basic-syntax

Este documento tiene control de versión inspirado en el sistema de versión semántico de software:
https://semver.org/lang/es/
https://www.celsobessa.com.br/2016/01/05/organizando-os-arquivos/
