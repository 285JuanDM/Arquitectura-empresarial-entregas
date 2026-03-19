# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

*Taller 4 - STRIDE*

## 👥 Integrantes del equipo

* Oscar David Vergara — [@Oscarvm117](https://github.com/Oscarvm117)
* Jaime Andrés Olarte — [@JAIMEPCI](https://github.com/JAIMEPCI)
* Juan David Moreno — [@285JuanDM](https://github.com/285JuanDM)

# 🧠 Descripción general del trabajo

El objetivo del taller fue identificar y analizar riesgos de seguridad en un sistema mediante el uso del modelo **STRIDE**, aplicándolo a un proceso crítico del cliente real **TransCapital S.A.S**. En este caso, se seleccionó el proceso de **generación de FUEC**, debido a su importancia operativa y manejo de información sensible.

Se realizó un análisis estructurado de amenazas considerando los seis tipos definidos por STRIDE: suplantación, manipulación, repudio, divulgación de información, denegación de servicio y elevación de privilegios. Este análisis permitió identificar vulnerabilidades existentes en el sistema actual basado en archivos Excel y procesos manuales.

Como resultado, se construyó una tabla de amenazas que incluye escenarios de ataque, impacto, probabilidad, nivel de riesgo y posibles estrategias de mitigación, permitiendo tener una visión clara del estado de seguridad del proceso analizado.

# 🔧 Proceso de desarrollo

El proceso inició con la identificación del flujo crítico de negocio, en este caso la generación de FUEC, analizando cómo se gestiona actualmente mediante archivos Excel y procesos manuales. Se identificaron los componentes involucrados, como el acceso al archivo, almacenamiento de datos, generación de documentos y uso de equipos físicos.

Posteriormente, se aplicó el modelo STRIDE sobre cada componente del proceso, evaluando posibles amenazas y escenarios de ataque. Se definieron criterios de impacto y probabilidad para determinar el nivel de riesgo, lo que permitió priorizar las vulnerabilidades más críticas del sistema.

Para el desarrollo del análisis se utilizó **Excel** como herramienta principal para estructurar la tabla STRIDE. El modelo fue ajustado iterativamente, refinando las amenazas identificadas y proponiendo controles de mitigación alineados con buenas prácticas de seguridad.

# 🧩 Análisis del modelo propuesto

El modelo se estructura como una tabla STRIDE que analiza cada componente del proceso de generación de FUEC, identificando amenazas específicas y evaluando su impacto en la operación del negocio. Esta estructura permite relacionar directamente los riesgos con los elementos reales del sistema.

El análisis refleja adecuadamente las necesidades del cliente, evidenciando problemas críticos como la falta de control de acceso, ausencia de trazabilidad, dependencia de un único equipo y exposición de información sensible. Estos hallazgos están directamente relacionados con la forma en que actualmente se gestiona el proceso mediante Excel.

Se asumió que la empresa no cuenta con controles formales de seguridad, sistemas centralizados ni mecanismos automatizados de respaldo o auditoría. Bajo estos supuestos, se identificaron múltiples riesgos críticos que afectan la confidencialidad, integridad y disponibilidad de la información.

# 📈 Tabla final entregado

> (Insertar aquí la tabla STRIDE del proceso de generación de FUEC o un enlace al archivo Excel)

# 📋 Tabla de actores, entidades o componentes

| Nombre del elemento             | Tipo            | Descripción                                               | Responsable |
| ------------------------------- | --------------- | --------------------------------------------------------- | ----------- |
| Personal administrativo         | Actor           | Encargado de generar los FUEC y gestionar la información  | Empresa     |
| Archivo Excel                   | Componente      | Contiene los datos de contratos, conductores y plantillas | Empresa     |
| Computador principal            | Infraestructura | Equipo donde se almacena y procesa la información         | Empresa     |
| Plantilla FUEC                  | Componente      | Archivo Excel con fórmulas para generar el documento      | Empresa     |
| Documentos físicos              | Componente      | FUEC impresos utilizados en operación                     | Empresa     |
| Datos de clientes y conductores | Datos           | Información sensible utilizada en la generación de FUEC   | Empresa     |

# 🔍 Investigación complementaria

### Tema investigado:

Principios de seguridad informática y modelo STRIDE aplicado a sistemas empresariales.

### Resumen:

El modelo STRIDE es un marco de análisis de amenazas utilizado en seguridad informática para identificar vulnerabilidades en sistemas, clasificándolas en seis categorías: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service y Elevation of Privilege. Este enfoque permite analizar de forma estructurada los riesgos asociados a un sistema y proponer controles adecuados.

En entornos empresariales, la aplicación de STRIDE es fundamental para proteger la información y garantizar la continuidad del negocio. Buenas prácticas como la autenticación de usuarios, control de accesos, cifrado de datos, auditoría de acciones y mecanismos de respaldo son esenciales para mitigar riesgos identificados mediante este modelo.

En el contexto del taller, el uso de STRIDE permitió evidenciar que el sistema actual de TransCapital S.A.S presenta debilidades importantes en seguridad, especialmente en el manejo de datos y control de acceso. Esto resalta la necesidad de migrar hacia soluciones más robustas y seguras que reduzcan los riesgos operativos.

*Este documento hace parte de la entrega del taller 4 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana.*