# 🙋‍♂️ Reflexión Individual — Arquitectura Empresarial

## 👤 Nombre del Estudiante
*Jaime Andrés Olarte*

## 💼 Rol en el equipo
- **Arquitecto de infraestructura** – Diseño de la arquitectura AS-IS y TO-BE, incluyendo la propuesta de VPS con PostgreSQL, red privada Tailscale y configuración de acceso remoto seguro.
- **Responsable de seguridad técnica** – Definición de controles por capa: cifrado en tránsito (WireGuard), cifrado en reposo (BitLocker), autenticación MFA con Google Identity y logs de auditoría.
- **Analista de riesgos** – Identificación y priorización de los quince riesgos distribuidos en siete dominios, con énfasis en los tres riesgos críticos de impacto operativo directo.

## 🎓 Aprendizajes Clave

- 📌 Aprendí que la infraestructura no es solo tecnología — es la materialización de decisiones de negocio. Cada componente que propuse (el VPS, Tailscale, los backups nocturnos) responde directamente a un riesgo identificado o a un principio de gobernanza definido en equipo. Diseñar así me hizo entender que una buena arquitectura de infraestructura siempre tiene una justificación de negocio detrás, no solo una justificación técnica.

- 💡 Comprendí el valor real del modelo Zero Trust en un contexto empresarial pequeño. Antes asociaba ese concepto con grandes corporaciones con equipos de seguridad dedicados. TransCapital demostró que con Tailscale y MFA se puede implementar una postura Zero Trust funcional con menos de veinte dólares mensuales y sin personal técnico especializado.

- ⚙️ Afiancé mi capacidad para analizar riesgos de forma estructurada por dominios — negocio, procesos, datos, infraestructura, seguridad, personas y normativa. Pasar de identificar un riesgo a proponer una mitigación concreta, medible y operacionalmente viable para una empresa como TransCapital fue uno de los ejercicios más exigentes y más útiles del curso.

- 🗺️ Entendí que los trade-offs son parte inherente de cualquier decisión arquitectónica. En la presentación final expuse abiertamente las limitaciones de cada decisión que tomamos — la dependencia de Tailscale, el riesgo de vendor lock-in con Google Workspace — y eso, lejos de debilitar la propuesta, demostró criterio y madurez arquitectónica.

## 🔄 Retos Superados

- Mi mayor dificultad fue conectar la dimensión legal y normativa con las decisiones de infraestructura. Al principio veía la Resolución 3068 y la Ley 1581 como requisitos externos que había que "cumplir" de forma separada a lo técnico. El reto fue entender que cada control de infraestructura que proponía — los logs de auditoría, el cifrado de datos, los backups estructurados — era también una respuesta directa a esos requisitos normativos. Lograr esa conexión fue lo que le dio coherencia real a la arquitectura TO-BE.

- También fue difícil dimensionar la solución correctamente para el contexto de TransCapital. Mi instinto inicial fue proponer una arquitectura más robusta y compleja, pero rápidamente entendí que una solución que el cliente no puede operar por sí mismo no es una solución — es un problema nuevo. Aprender a diseñar con restricción operativa como criterio de diseño, no como limitación, fue un cambio de perspectiva significativo.

## 🌱 Áreas por Mejorar

- Quiero profundizar en marcos de modelado arquitectónico como C4, Archimate y TOGAF. Durante el proyecto trabajé principalmente con diagramas de infraestructura y riesgos, pero reconozco que me faltan herramientas para representar arquitecturas de forma más estandarizada y comunicable entre diferentes audiencias técnicas y no técnicas.

- Me gustaría también fortalecer mi capacidad para documentar decisiones arquitectónicas de forma más formal — por ejemplo, mediante Architecture Decision Records (ADRs) — de modo que las justificaciones de cada elección queden registradas y sean auditables en el tiempo, no solo implícitas en los diagramas.

## 🧠 Contribución Personal

Siento que mi mayor aporte al equipo fue traducir los riesgos en arquitectura concreta. Identificar que el SPOF del Excel era crítico es un diagnóstico; proponer que PostgreSQL en VPS con backups automáticos y acceso exclusivo por Tailscale elimina ese riesgo específico es arquitectura. Esa diferencia — entre nombrar un problema y diseñar su solución con componentes reales, costos reales y decisiones justificadas — es lo que más me esforcé en aportar durante el proyecto, y creo que se refleja en la coherencia entre la vista de infraestructura TO-BE, el análisis de riesgos y los trade-offs que presentamos.

*Esta reflexión individual hace parte de la entrega final del curso AREM - Arquitectura Empresarial - Universidad de La Sabana.*
*Mi nombre es Jaime Andrés Olarte y fui arquitecto de infraestructura y responsable de seguridad técnica del equipo.*
