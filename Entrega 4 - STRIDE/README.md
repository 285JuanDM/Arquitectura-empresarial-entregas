# Arq-Emp-Taller-4

**Taller 4 – Evaluación de Seguridad con STRIDE**

# 👥 Integrantes del Grupo

* Oscar Vergara
* Jaime Andres Olarte
* Juan David Moreno Suarez

# 📖 Descripción del Proyecto

Este repositorio contiene el desarrollo del taller de **evaluación de seguridad utilizando el modelo STRIDE** en el curso de Arquitectura Empresarial.

El objetivo principal fue analizar los riesgos de seguridad en sistemas tecnológicos mediante la identificación de amenazas como suplantación, manipulación de datos, divulgación de información, denegación de servicio y elevación de privilegios.

El trabajo se dividió en dos casos principales:

* **Caso base – EdukIT:** se realizó un análisis de seguridad sobre una plataforma de educación virtual, evaluando riesgos en procesos como acceso a cursos, manejo de datos personales y control de roles.
* **Caso real – TransCapital S.A.S:** se aplicó el modelo STRIDE al proceso de **generación de FUEC**, identificando vulnerabilidades relacionadas con el uso de archivos Excel, falta de control de acceso, ausencia de trazabilidad y dependencia de infraestructura local.

Para el desarrollo del análisis se utilizó **Excel** para la construcción de tablas STRIDE y **Markdown** para la documentación de resultados, permitiendo estructurar de manera clara las amenazas, impactos y estrategias de mitigación.

# 🎯 Objetivo

Aplicar el modelo **STRIDE** para identificar y analizar amenazas de seguridad en sistemas tecnológicos, evaluando su impacto y proponiendo estrategias de mitigación.

A través del análisis se buscó identificar:

* Vulnerabilidades en procesos críticos del sistema
* Riesgos asociados a la confidencialidad, integridad y disponibilidad de la información
* Posibles escenarios de ataque
* Nivel de riesgo de cada amenaza
* Controles de seguridad y oportunidades de mejora

Este enfoque permite anticipar problemas de seguridad y diseñar soluciones que fortalezcan la protección de la información y la continuidad operativa.

# ↗️ Análisis de Seguridad STRIDE

## Caso Base – 🎓 EdukIT (Plataforma de Educación Virtual)

El análisis STRIDE aplicado a **EdukIT** permitió evaluar los riesgos asociados al acceso de estudiantes a cursos, la gestión de contenidos por parte de docentes y el manejo de datos personales y pagos.

Se identificaron amenazas como accesos no autorizados, manipulación de contenido académico, exposición de información sensible y posibles interrupciones del servicio. Estas vulnerabilidades evidencian la importancia de implementar controles de autenticación, autorización y monitoreo dentro del sistema.

El modelo permite comprender cómo los diferentes roles (estudiante, docente y administrador) interactúan con la plataforma y qué riesgos se presentan en cada punto del flujo de información.

> 📊 Ver tabla STRIDE en:
> `clase/tabla-stride-clase.xlsx`

## Caso Real – 🚌 TransCapital S.A.S

El análisis STRIDE de **TransCapital S.A.S** se enfocó en el proceso de **generación de FUEC**, el cual actualmente se realiza mediante archivos Excel y procesos manuales.

El modelo evidenció múltiples riesgos críticos, como la posibilidad de manipulación de datos, falta de trazabilidad, exposición de información sensible y dependencia de un único equipo para la operación. Estos problemas afectan directamente la seguridad y continuidad del negocio.

El análisis permitió proponer mejoras como la implementación de controles de acceso, auditoría de acciones, respaldo de información y migración hacia sistemas más robustos y centralizados.

> 📊 Ver tabla STRIDE en:
> `entrega/tabla-stride-cliente.xlsx`

# 📁 Estructura del Repositorio

```id="v2m2m8"
taller-05-seguridad-stride/
│
├── README.md
│
├── clase/
│   ├── notas.md
│   └── tabla-stride-clase.xlsx
│
├── entrega/
│   ├── informe.md
│   ├── referencias.md
│   └── tabla-stride-cliente.xlsx
```

# 🔎 Tecnologías y Herramientas Utilizadas

Durante el desarrollo del taller se utilizaron las siguientes herramientas:

* **Microsoft Excel** para la construcción de tablas STRIDE
* **Markdown** para la documentación técnica
* **GitHub** para el control de versiones y gestión del repositorio

Estas herramientas permitieron estructurar el análisis de seguridad de forma clara, facilitando la identificación de riesgos y la propuesta de soluciones.

# ✅ Licencia

Este proyecto fue desarrollado como parte del curso **Arquitectura Empresarial (AREM)** de la **Universidad de La Sabana**.
Uso académico bajo licencia MIT.
