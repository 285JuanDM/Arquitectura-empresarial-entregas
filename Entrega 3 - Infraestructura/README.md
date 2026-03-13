# Arq-Emp-Taller-3

**Taller 3 – Modelado de Infraestructura Tecnológica**

# 👥 Integrantes del Grupo

* Oscar Vergara
* Jaime Andres Olarte
* Juan David Moreno Suarez

# 📖 Descripción del Proyecto

Este repositorio contiene el desarrollo de los talleres de **modelado de infraestructura tecnológica** del curso de Arquitectura Empresarial.

El objetivo principal fue analizar y representar la **infraestructura tecnológica de diferentes sistemas**, identificando componentes clave como usuarios, redes, aplicaciones, servicios externos y almacenamiento de datos.

El trabajo se dividió en dos casos principales:

* **Caso real – TransCapital S.A.S:** se modeló la infraestructura tecnológica actual (AS-IS) de una empresa de transporte terrestre que utiliza herramientas básicas como archivos Excel locales, correo electrónico y servicios externos de rastreo GPS.
* **Caso base – RedExpress:** se desarrolló un mapa de infraestructura híbrida para una plataforma logística digital que incluye servicios en la nube, balanceadores de carga, microservicios, bases de datos distribuidas y servidores regionales.

Para el desarrollo de los diagramas se utilizaron herramientas de modelado visual como **draw.io**, junto con documentación en **Markdown** para describir el proceso de análisis, diagnóstico técnico y resultados obtenidos.

# 🎯 Objetivo

Aplicar conceptos de **arquitectura tecnológica e infraestructura empresarial** para representar visualmente la estructura de un sistema tecnológico.

A través de los diagramas de infraestructura se buscó identificar:

* Componentes principales de la arquitectura tecnológica
* Relaciones entre aplicaciones, usuarios y servicios
* Dependencias entre sistemas internos y externos
* Posibles **puntos únicos de falla (SPOF)** dentro del sistema
* Cuellos de botella potenciales en procesamiento o almacenamiento
* Oportunidades de mejora en disponibilidad y escalabilidad

Este análisis permite comprender mejor el funcionamiento de una infraestructura tecnológica y facilita la toma de decisiones para mejorar su rendimiento, seguridad y resiliencia.

# ↗️ Diagramas de Infraestructura

## Caso Real – 🚌 TransCapital S.A.S

El diagrama de infraestructura de **TransCapital S.A.S** representa la arquitectura tecnológica actual de la empresa. La organización cuenta con una infraestructura sencilla basada principalmente en **computadores de oficina conectados a una red local**, donde se gestionan los procesos administrativos mediante archivos de **Microsoft Excel almacenados localmente**.

El sistema incluye diferentes actores como personal administrativo, personal operativo y conductores. La empresa utiliza servicios externos como el correo electrónico y una plataforma de rastreo GPS para monitorear la ubicación de los vehículos.

El modelo permite identificar algunos riesgos tecnológicos importantes, como la dependencia de un solo computador para almacenar datos críticos de la empresa y la ausencia de sistemas centralizados o mecanismos de respaldo automatizado.

!["Diagrama de infraestructura de TransCapital S.A.S"](/Entrega%203%20-%20Infraestructura/entrega/TransCapital_Infraestructura.png)

## Caso Base – 🚚 RedExpress (Plataforma Logística)

El modelo de infraestructura de **RedExpress** representa una arquitectura tecnológica híbrida diseñada para soportar una plataforma digital de logística y rastreo de paquetes.

La arquitectura incluye diferentes capas como zona cliente, seguridad perimetral, balanceadores de carga, API Gateway, microservicios en la nube, servidores regionales y una zona de almacenamiento de datos. Además, se incorporan herramientas de monitoreo y observabilidad para supervisar el comportamiento del sistema.

Dentro del modelo se identificaron componentes críticos como el sistema de rastreo en tiempo real, la base de datos principal y los servidores regionales encargados de procesar rutas de entrega. El diagrama también permite visualizar posibles riesgos como puntos únicos de falla y limitaciones en la escalabilidad de algunos servicios.

!["Diagrama de Infraestructura caso ficticio"](/Entrega%203%20-%20Infraestructura//clase/RedExpress_Infraestructura.png)

# 📁 Estructura del Repositorio

```
taller-infraestructura/
│
├── README.md
│
├── clase/
│   ├── notas.md
│   ├── RedExpress_Infraestructura.png
│   └── RedExpress_Infraestructura_Final.png
│
├── entrega/
│   ├── informe.md
│   ├── referencias.md
│   ├── TransCapital_Infraestructura.drawio
│   └── TransCapital_Infraestructura.png
|
```

# 🔎 Tecnologías y Herramientas Utilizadas

Durante el desarrollo del taller se utilizaron las siguientes herramientas:

* **draw.io** para la creación de diagramas de infraestructura
* **Markdown** para la documentación del proyecto
* **GitHub** para el control de versiones y almacenamiento del repositorio

Estas herramientas permitieron documentar de forma clara la arquitectura tecnológica de los casos analizados y facilitar la presentación del trabajo realizado.

# ✅ Licencia

Este proyecto fue desarrollado como parte del curso **Arquitectura Empresarial (AREM)** de la **Universidad de La Sabana**.
Uso académico bajo licencia MIT.