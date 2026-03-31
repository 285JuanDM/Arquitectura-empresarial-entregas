# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

*Taller 5 - Normativa*

## 👥 Integrantes del equipo

* Oscar David Vergara — [@Oscarvm117](https://github.com/Oscarvm117)
* Jaime Andrés Olarte — [@JAIMEPCI](https://github.com/JAIMEPCI)
* Juan David Moreno — [@285JuanDM](https://github.com/285JuanDM)

# 🧠 Descripción general del trabajo

El objetivo del taller fue evaluar el cumplimiento de aspectos legales, normativos y de seguridad de la información en un sistema, utilizando listas de control basadas en marcos como **ISO/IEC 27001** y la **Ley 1581 de 2012 (Habeas Data)** en Colombia.

Para el desarrollo, se aplicó un checklist de cumplimiento al sistema del cliente real **TransCapital S.A.S**, específicamente al proceso de **generación de FUEC**, el cual involucra el manejo de datos personales de conductores y clientes.

Se analizaron aspectos clave como consentimiento, control de acceso, seguridad de la información, retención de datos y trazabilidad. A partir de este análisis, se identificaron brechas de cumplimiento normativo y se formularon recomendaciones orientadas a mejorar la protección de los datos y reducir riesgos legales.

# 🔧 Proceso de desarrollo

El proceso inició con la comprensión del sistema actual de TransCapital S.A.S, el cual se basa en el uso de archivos Excel y procedimientos manuales para la generación de FUEC. Se identificaron los tipos de datos manejados, destacando la presencia de información personal y potencialmente sensible.

Posteriormente, se tomó como referencia una plantilla de checklist de cumplimiento normativo, evaluando cada criterio frente al estado actual del sistema. Para cada punto se determinó el nivel de cumplimiento (cumple, parcial o no cumple), acompañado de su respectiva justificación.

Finalmente, se consolidaron los hallazgos en una tabla estructurada, permitiendo identificar de manera clara las principales debilidades del sistema y proponiendo acciones correctivas alineadas con buenas prácticas y normativas vigentes.

# 🧩 Análisis del modelo propuesto

El modelo se basa en un checklist de cumplimiento que evalúa diferentes dimensiones de la gestión de datos personales y seguridad de la información. Esta estructura permite contrastar los requisitos normativos con la realidad operativa del sistema.

El análisis evidenció que TransCapital S.A.S presenta múltiples incumplimientos, principalmente debido a la ausencia de controles formales, políticas de privacidad y mecanismos de seguridad. Problemas como la falta de consentimiento del usuario, inexistencia de control de accesos y ausencia de trazabilidad representan riesgos críticos.

Se asumió que la organización no cuenta con un sistema de gestión de seguridad de la información implementado ni con lineamientos formales de protección de datos. Bajo este contexto, se identificó un alto riesgo de incumplimiento legal y exposición de información sensible.

# 📈 Tabla final entregada

<img width="1678" height="320" alt="image" src="https://github.com/user-attachments/assets/314dca4d-6b8d-4e92-8c04-5adebb653ddf" />

# 📋 Tabla de actores, entidades o componentes

| Nombre del elemento             | Tipo            | Descripción                                  | Responsable |
| ------------------------------- | --------------- | -------------------------------------------- | ----------- |
| Personal administrativo         | Actor           | Encargado de gestionar y generar los FUEC    | Empresa     |
| Archivo Excel                   | Componente      | Contiene datos personales y operativos       | Empresa     |
| Computador principal            | Infraestructura | Equipo donde se procesa la información       | Empresa     |
| Plantilla FUEC                  | Componente      | Herramienta para generar documentos          | Empresa     |
| Documentos físicos              | Componente      | FUEC impresos utilizados en operación        | Empresa     |
| Datos de clientes y conductores | Datos           | Información personal utilizada en el proceso | Empresa     |

# 🔍 Investigación complementaria

### Tema investigado:

Cumplimiento normativo en protección de datos personales y seguridad de la información.

### Resumen:

La **Ley 1581 de 2012** establece el régimen general de protección de datos personales en Colombia, definiendo principios como legalidad, finalidad, libertad, veracidad, transparencia y seguridad. Esta normativa exige que las organizaciones obtengan el consentimiento del titular y garanticen la protección de su información [1].

Por otro lado, la norma **ISO/IEC 27001** proporciona un marco para implementar un Sistema de Gestión de Seguridad de la Información (SGSI), basado en la identificación y tratamiento de riesgos. Incluye controles relacionados con gestión de accesos, criptografía, seguridad física y auditoría [2].

En el contexto del taller, la ausencia de controles técnicos y administrativos en TransCapital S.A.S evidencia un bajo nivel de madurez en seguridad de la información. Esto implica riesgos tanto operativos como legales, especialmente en relación con el manejo inadecuado de datos personales.

*Este documento hace parte de la entrega del taller 5 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana.*
