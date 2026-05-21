# 📄 Resumen Ejecutivo del Proyecto Arquitectónico

## 🏢 Nombre del Cliente

TransCapital S.A.S — Empresa de transporte privado especial
(empresarial, escolar y particular). Bogotá, Colombia.

## 🎯 Objetivo General del Proyecto

TransCapital S.A.S opera en un sector altamente regulado: el transporte
especial en Colombia exige que cada servicio esté respaldado por un FUEC
(Formato Único de Extracto del Contrato), documento legal obligatorio
ante el Ministerio de Transporte. Al inicio del proyecto, este proceso
crítico dependía enteramente de archivos Excel locales, envíos por
WhatsApp y conocimiento no documentado del personal administrativo —
una arquitectura que exponía al negocio a riesgos operacionales,
legales y de continuidad de alto impacto.

El objetivo del proyecto fue analizar la arquitectura actual (AS-IS),
identificar los riesgos estructurales en todos los dominios de la
organización y proponer una arquitectura futura (TO-BE) que garantice
la continuidad operativa, la trazabilidad legal de los documentos y la
seguridad de la información, manteniendo la menor fricción posible para
el equipo administrativo durante la transición.

El valor aportado es concreto: TransCapital puede ahora operar desde
cualquier lugar, con historial auditable de cada FUEC emitido, sin
depender de un único equipo físico ni de personas específicas, y
cumpliendo los requisitos de la Resolución 3068 de 2014 del Ministerio
de Transporte.

## 🧱 Vistas Arquitectónicas Cubiertas

| Vista                   | Alcance de la solución                                                                                                                                                                                                                                   |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Procesos de negocio     | Modelado BPMN del flujo completo de emisión del FUEC: solicitud → registro de contrato → generación automática → emisión digital con historial                                                                                                           |
| Información / Datos     | Modelo Entidad-Relación con cinco entidades centrales: Conductores, Buses, Contratos, FUEC y Contrato_Buses (tabla intermedia N:M)                                                                                                                       |
| Aplicaciones / Sistemas | REST API (Node.js/Python) como capa de lógica de negocio; Google Workspace (Sheets + Drive) como interfaz de usuario y respaldo; Apps Script como conector entre Sheets y la API                                                                         |
| Infraestructura         | VPS económico con PostgreSQL accesible únicamente vía Tailscale VPN; router Mikrotik con firewall perimetral; PCs con cifrado de disco completo; backups diarios pg_dump → Google Drive                                                                  |
| Seguridad               | Análisis STRIDE completo; controles por capa: MFA (Google Identity), cifrado en tránsito (HTTPS/WireGuard), cifrado en reposo (BitLocker/FileVault), Zero Trust networking (Tailscale), logs de auditoría y Cloudflare como protección perimetral futura |
| Cumplimiento normativo  | Checklist de cumplimiento frente a la Resolución 3068 de 2014 del Ministerio de Transporte, verificando requisitos de contenido, trazabilidad y archivo del FUEC                                                                                         |
| Integración de vistas   | Marco de integración de las seis vistas en una narrativa arquitectónica coherente, validando que cada capa soporta a las demás y que las decisiones técnicas responden a los objetivos del negocio                                                       |

## 🧩 Hallazgos Clave

- ❗ El proceso de generación del FUEC dependía de un único archivo Excel
  local sin respaldo, sin control de acceso y sin historial auditable,
  constituyendo un punto único de falla (SPOF) que podía paralizar
  completamente la operación legal de la empresa.

- 🔄 La arquitectura AS-IS presentaba silos de información críticos:
  datos de conductores, vehículos y contratos vivían en hojas
  desconectadas entre sí, generando riesgo de duplicidad e
  inconsistencia en documentos con valor legal.

- 🔒 No existía ningún control de acceso, autenticación ni cifrado sobre
  la información sensible de la empresa: cédulas, contratos y datos de
  conductores estaban en texto plano accesibles para cualquier persona
  con acceso físico al equipo.

- 📌 La dependencia de WhatsApp como canal de distribución del FUEC
  impedía cualquier tipo de trazabilidad o auditoría del ciclo de vida
  del documento, exponiendo a la empresa ante posibles controles del
  Ministerio de Transporte.

- 🌐 La limitación geográfica del sistema (solo operable desde la
  oficina) era incompatible con el crecimiento del negocio y con
  cualquier escenario de trabajo remoto o contingencia.

## 🚀 Recomendaciones Principales

- **Migrar la persistencia de datos** desde archivos Excel locales hacia
  PostgreSQL centralizado en VPS, usando el modelo ER desarrollado como
  esquema base, con restricciones de unicidad para eliminar duplicidades
  y backups automáticos diarios hacia Google Drive.

- **Implementar la REST API** como única puerta de entrada a los datos,
  con autenticación por roles y validaciones automáticas (vigencia de
  licencia del conductor, integridad del contrato) antes de permitir
  la generación de cualquier FUEC.

- **Conectar Google Sheets a la API mediante Apps Script**, manteniendo
  la interfaz familiar para el equipo administrativo pero reemplazando
  la lógica de fórmulas Excel por llamadas a la API. Esto minimiza la
  resistencia al cambio y permite una transición gradual.

- **Desplegar Tailscale en todos los dispositivos** del personal
  administrativo y en el VPS, eliminando la exposición pública de
  cualquier servicio y garantizando que el acceso remoto sea tan seguro
  como el acceso local.

- **Activar MFA en Google Workspace** para todos los usuarios,
  vinculándolo con Tailscale como segundo factor de autenticación de
  red, cerrando la principal vulnerabilidad de acceso identificada en
  el análisis STRIDE.

## 💡 Reflexión Final

Este proyecto demostró que los retos de arquitectura empresarial de
TransCapital no eran únicamente tecnológicos. La dependencia de un
archivo Excel para un proceso con consecuencias legales directas
reflejaba una brecha estructural entre la operación del negocio y su
soporte tecnológico — una brecha que ninguna herramienta aislada podía
cerrar sin una visión arquitectónica integrada.

El mayor aprendizaje del equipo fue entender que una arquitectura
bien diseñada no necesita ser costosa ni compleja para ser efectiva.
La solución TO-BE de TransCapital logra nivel de seguridad y
disponibilidad enterprise con un VPS de menos de 20 dólares mensuales,
herramientas open source y Google Workspace que la empresa ya paga.
La arquitectura no agrega complejidad — la elimina, reemplazando siete
puntos de falla distribuidos en archivos Excel por un sistema cohesivo
donde cada componente tiene un rol claro y cada riesgo identificado
tiene su mitigación correspondiente.

_Este resumen ejecutivo forma parte de la entrega final del curso AREM -
Arquitectura Empresarial - Universidad de La Sabana._
