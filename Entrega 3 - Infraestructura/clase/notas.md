# 🗒️ Registro de Trabajo en Clase - Taller 3

## 📆 Fecha de la sesión

07/03/2026

## 👥 Integrantes presentes

* Oscar David Vergara
* Jaime Andrés Olarte
* Juan David Moreno

# 🧠 Actividades realizadas en clase

Durante la sesión se analizó el caso de estudio **RedExpress**, una plataforma logística que gestiona envíos y rastreo de paquetes mediante una aplicación móvil y una plataforma web. El equipo discutió cómo estructurar un **mapa de infraestructura tecnológica** que representara las diferentes capas del sistema, incluyendo clientes, seguridad perimetral, entrada a la plataforma, microservicios, servidores regionales y almacenamiento de datos.

Se decidió modelar la arquitectura separando el sistema en **zonas funcionales** para facilitar la comprensión del flujo de información y la identificación de riesgos. Entre estas zonas se incluyeron la zona cliente, zona de seguridad (CDN y WAF), zona de entrada con balanceadores y API Gateway, microservicios en la nube, servidores regionales para procesamiento local y una zona de datos centralizada.

Para el modelado se utilizó **draw.io** como herramienta principal de diagramación. Durante la clase se logró construir una versión preliminar del mapa de infraestructura, identificando componentes clave como balanceadores de carga, servicios de autenticación, módulos de rastreo y almacenamiento de datos. También se comenzaron a marcar posibles **puntos únicos de falla y cuellos de botella** dentro del sistema.

# 🧩 Boceto inicial del modelo

![Diagrama de Infraestructura caso ficticio](/Entrega%203%20-%20Infraestructura//clase/RedExpress_Infraestructura.png)

El modelo preliminar representa la arquitectura lógica de la plataforma RedExpress, incluyendo los flujos principales entre los usuarios, los servicios en la nube y los servidores regionales. El diagrama permite visualizar cómo las solicitudes de los clientes pasan por capas de seguridad, balanceadores de carga y microservicios antes de interactuar con los sistemas de almacenamiento y monitoreo.

# 🔁 Tareas definidas para complementar el taller

Durante la sesión se definieron algunas tareas para completar el modelo final y el análisis técnico del sistema.

| Tarea asignada                                                            | Responsable         | Fecha estimada |
| ------------------------------------------------------------------------- | ------------------- | -------------- |
| Refinar el diagrama final de infraestructura en draw.io                   | Oscar David Vergara | 10/03          |
| Identificar cuellos de botella                                            | Jaime Andrés Olarte | 11/03          |
| Investigación de buenas prácticas en diagramas de infraestructura         | Juan David Moreno   | 11/03          |

*Este documento resume el trabajo colaborativo realizado durante la sesión del taller 3 en el curso AREM - Universidad de La Sabana.*
