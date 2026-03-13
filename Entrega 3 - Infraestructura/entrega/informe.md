# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

*Taller 3 - Infraestructura*

## 👥 Integrantes del equipo

* Oscar David Vergara — [@Oscarvm117](https://github.com/Oscarvm117)
* Jaime Andrés Olarte — [@JAIMEPCI](https://github.com/JAIMEPCI)
* Juan David Moreno — [@285JuanDM](https://github.com/285JuanDM)

# 🧠 Descripción general del trabajo

El objetivo del taller fue analizar y representar la **infraestructura tecnológica actual (AS-IS)** de una empresa real mediante un **diagrama de arquitectura tecnológica**. Para ello se seleccionó la empresa colombiana **TransCapital S.A.S**, dedicada al transporte privado terrestre de pasajeros.

Se realizó un levantamiento de información sobre los sistemas, herramientas y recursos tecnológicos que utiliza la empresa actualmente. Se identificó que la organización tiene una **baja madurez digital**, ya que sus procesos principales se gestionan mediante archivos de **Microsoft Excel almacenados localmente** y servicios externos básicos.

A partir de este análisis se construyó un **diagrama de infraestructura tecnológica**, que representa los usuarios, dispositivos, red local, aplicaciones utilizadas y servicios externos que intervienen en la operación diaria de la empresa.

# 🔧 Proceso de desarrollo

El proceso inició con la identificación de los **componentes tecnológicos reales** utilizados por la empresa, como computadores de oficina, red local, aplicaciones utilizadas y servicios externos. Se decidió modelar la arquitectura utilizando un enfoque **AS-IS**, con el fin de reflejar fielmente la situación tecnológica actual.

Posteriormente se estructuró el modelo en **capas de arquitectura tecnológica**, incluyendo usuarios, infraestructura local, red, aplicaciones y servicios externos. Esta organización permitió representar de manera clara la relación entre los diferentes elementos del entorno tecnológico.

Finalmente, el diagrama fue refinado agregando conexiones, agrupaciones y anotaciones que explican el flujo de información y los puntos críticos de la infraestructura, como el almacenamiento de datos empresariales en un único computador.

# 🧩 Análisis del modelo propuesto

El modelo entregado se estructura en diferentes capas que representan los principales componentes de la arquitectura tecnológica: usuarios, infraestructura local de oficina, red, aplicaciones y servicios externos. Esta organización permite visualizar cómo interactúan los actores con los recursos tecnológicos de la empresa.

El diagrama refleja las necesidades actuales del cliente al representar los sistemas y herramientas realmente utilizados en la operación diaria. Se incluyen elementos como los computadores de oficina, el uso de archivos Excel para la gestión de información, el correo electrónico y el sistema externo de monitoreo GPS de los vehículos.

Durante el modelado se asumió que la empresa no cuenta con sistemas empresariales centralizados ni infraestructura de servidores dedicada. Asimismo, se consideró que los datos críticos se almacenan localmente en un único equipo, lo que representa un riesgo importante dentro de la arquitectura tecnológica actual.

# 📈 Diagrama final entregado

!["Diagrama de infraestructura de TransCapital S.A.S"](/Entrega%203%20-%20Infraestructura/entrega/TransCapital_Infraestructura.png)


# 📋 Tabla de actores, entidades o componentes

| Nombre del elemento     | Tipo             | Descripción                                                                      | Responsable           |
| ----------------------- | ---------------- | -------------------------------------------------------------------------------- | --------------------- |
| Personal administrativo | Actor            | Empleados encargados de la gestión administrativa y registro de información      | Empresa               |
| Personal operativo      | Actor            | Personal encargado de la coordinación y operación del servicio de transporte     | Empresa               |
| Computadores de oficina | Infraestructura  | Equipos utilizados por el personal para acceder a aplicaciones y datos           | Empresa               |
| Red LAN                 | Infraestructura  | Red local que conecta los equipos dentro de la oficina                           | Empresa               |
| Router / Módem          | Infraestructura  | Dispositivo que conecta la red interna con internet                              | Proveedor de internet |
| Microsoft Excel         | Aplicación       | Herramienta utilizada para registrar viajes, FUEC y datos de conductores         | Empresa               |
| Gmail                   | Aplicación       | Servicio de correo electrónico utilizado para comunicación y envío de documentos | Google                |
| Sistema GPS GreenLink   | Servicio externo | Plataforma utilizada para monitorear la ubicación de los vehículos               | GreenLink             |

# 🔍 Investigación complementaria

### Tema investigado:

Buenas prácticas en diagramas de infraestructura tecnológica y su uso en arquitectura empresarial.

### Resumen

Los diagramas de infraestructura tecnológica son representaciones visuales que permiten describir los componentes físicos y lógicos que soportan los sistemas de información dentro de una organización. Estos diagramas suelen incluir elementos como usuarios, dispositivos, redes, aplicaciones, almacenamiento y servicios externos, mostrando cómo se conectan entre sí.

Actualmente, estos diagramas son ampliamente utilizados en **arquitectura empresarial y arquitectura de sistemas**, ya que facilitan la comprensión del entorno tecnológico y permiten identificar riesgos, dependencias y oportunidades de mejora. Herramientas como diagramas de arquitectura AS-IS y TO-BE ayudan a analizar la situación actual de una organización y planificar su evolución tecnológica.

En el contexto del taller, estas buenas prácticas se aplicaron para estructurar el modelo en capas y representar de manera clara la infraestructura tecnológica actual de TransCapital S.A.S. Esto permitió documentar el estado real de la organización y evidenciar limitaciones como la ausencia de sistemas centralizados y la dependencia de herramientas locales.
