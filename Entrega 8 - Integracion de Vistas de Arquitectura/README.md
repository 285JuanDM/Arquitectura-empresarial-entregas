# Arq-Emp-Entrega-8
Entrega 8 – Integración de Vistas de Arquitectura

## 👥 Integrantes del Grupo
- Oscar Vergara
- Jaime Andres Olarte
- Juan David Moreno Suarez

## 📖 Descripción del Proyecto

Este repositorio contiene el desarrollo de la Entrega 8 del curso de Arquitectura Empresarial, correspondiente a la **integración de todas las vistas arquitectónicas** trabajadas a lo largo del semestre en una narrativa visual coherente.

El objetivo principal fue unificar las vistas de negocio, información, aplicaciones, infraestructura y seguridad para mostrar cómo se relacionan y se alinean para soportar los objetivos estratégicos del cliente.

El trabajo se dividió en dos partes principales:

- **Caso base – FarmApp**: se construyó un tablero visual que integra las cinco capas arquitectónicas de una cadena de farmacias con e-commerce, mostrando cómo se conectan los procesos de compra, las entidades de información, los sistemas aplicativos, la infraestructura en nube híbrida y los controles de seguridad.

- **Caso real – TransCapital S.A.S**: se aplicó la misma integración al proceso real de generación de FUEC, articulando las vistas desarrolladas en entregas anteriores en un único marco arquitectónico TO-BE que refleja las decisiones clave de diseño adoptadas para el cliente.

Para el desarrollo se utilizaron **draw.io / Mermaid** para los tableros visuales y **Markdown** para la documentación narrativa.

## 🎯 Objetivo

Integrar todas las vistas arquitectónicas desarrolladas a lo largo del curso en una narrativa visual coherente, identificando cómo se relacionan y soportan los objetivos del cliente.

A través del análisis se buscó:

- Conectar las capas arquitectónicas (negocio → aplicaciones → infraestructura) de forma trazable
- Documentar las decisiones arquitectónicas clave que articulan cada vista
- Realizar una reflexión crítica sobre la coherencia interna de la arquitectura
- Contrastar con ejemplos reales de documentación de vistas en empresas similares

Este enfoque permite visualizar la arquitectura como un sistema integrado, garantizando coherencia entre los niveles estratégico, lógico y físico.

## ↗️ Integración de Vistas de Arquitectura

### Caso Base – 💊 FarmApp (Cadena de Farmacias con E-Commerce)

El tablero integrado de FarmApp organiza las cinco capas arquitectónicas mostrando cómo los procesos de negocio (compra, prescripción, despacho) son soportados por aplicaciones como la app móvil, el CRM y el sistema POS, los cuales se despliegan sobre una infraestructura de nube híbrida con base de datos replicada.

La capa de seguridad actúa de forma transversal: el control de accesos por rol protege el acceso a las prescripciones médicas, el cifrado resguarda los datos personales de clientes, y el monitoreo de fraude evalúa las transacciones en la pasarela de pagos.

Esta integración permitió identificar las dependencias clave entre capas y sirvió como modelo estructural para el análisis del cliente real.

### Caso Real – 🚌 TransCapital S.A.S

La integración arquitectónica TO-BE de TransCapital S.A.S articula las cinco vistas en torno al proceso central de generación de FUEC:

- **Vista de negocio**: flujo de solicitud → registro → generación de FUEC → emisión y envío de PDF
- **Vista de aplicaciones**: WhatsApp (comunicación), Google Workspace (historial de FUEC), PostgreSQL (base de datos), GreenLink (GPS de buses)
- **Vista de información**: entidades Conductores, Vehículos, Contratos y FUEC persistidas en PostgreSQL como fuente única de verdad
- **Vista de infraestructura**: VPS en nube con backups diarios a Drive, red Zero Trust mediante Tailscale/WireGuard y equipos locales cifrados con router Mikrotik
- **Vista de seguridad**: identidad con Google MFA y roles en API, cifrado HTTPS en tránsito y en reposo (disco + BD), red perimetral con Cloudflare (futuro)

El tablero integrado evidencia cómo cada decisión técnica (adoptar Tailscale, centralizar en PostgreSQL, eliminar Excel) responde directamente a los procesos de negocio y a los requisitos de seguridad identificados en entregas anteriores.

## 📁 Estructura del Repositorio

```
entrega-08-integracion-vistas/
│
├── README.md
│
├── clase/
│   ├── tablero-farmapp.drawio
│   └── notas.md
│
├── entrega/
│   ├── tablero-integrado-cliente.png
│   ├── informe.md
│   └── referencias.md
```

---

## 🔎 Tecnologías y Herramientas Utilizadas

Durante el desarrollo de la entrega se utilizaron las siguientes herramientas:

- **draw.io / Mermaid** para la construcción de los tableros de integración visual
- **Markdown** para la documentación narrativa e informe técnico
- **GitHub** para el control de versiones y gestión del repositorio

Estas herramientas permitieron construir una representación coherente de la arquitectura, facilitando la trazabilidad entre capas y la comunicación de decisiones de diseño.

## ✅ Licencia

Este proyecto fue desarrollado como parte del curso Arquitectura Empresarial (AREM) de la Universidad de La Sabana. Uso académico bajo licencia MIT.
