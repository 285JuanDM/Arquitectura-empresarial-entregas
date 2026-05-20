# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

_Taller 7 - Integración de Vistas de Arquitectura_

## 👥 Integrantes del equipo

- Oscar David Vergara
- Jaime Andrés Olarte
- Juan David Moreno

## 🧠 Descripción general del trabajo

El objetivo de este taller fue integrar las cinco vistas arquitectónicas
desarrolladas a lo largo del curso (negocio, información, aplicaciones,
infraestructura y seguridad) en una narrativa visual y narrativa coherente
para el cliente real TransCapital S.A.S, empresa colombiana de transporte
privado especial.

La actividad consistió en tomar todos los entregables previos — el proceso
BPMN del FUEC, el modelo entidad-relación, el diagrama de infraestructura
TO-BE, el análisis STRIDE y el checklist de cumplimiento normativo — y
demostrar cómo cada vista se articula con las demás para conformar una
arquitectura unificada. El resultado es un marco de integración que muestra
cómo las decisiones en cada capa (desde el proceso de negocio hasta los
controles de seguridad) se soportan mutuamente y responden a los objetivos
estratégicos del cliente.

## 🔧 Proceso de desarrollo

El trabajo se desarrolló en tres fases:

**Fase 1 — Inventario de entregables previos.** Revisamos los cinco
entregables del curso para identificar qué vista representaba cada uno y
qué artefactos (diagramas, modelos, análisis) teníamos disponibles. Este
paso fue clave para detectar que la vista de aplicaciones estaba implícita
en el diagrama TO-BE de infraestructura pero no había sido documentada
explícitamente como vista independiente.

**Fase 2 — Identificación de relaciones entre vistas.** Mapeamos cómo
cada vista depende de las demás. El hallazgo central fue que el proceso
crítico de negocio (generación del FUEC) es el hilo conductor que atraviesa
todas las capas: define las entidades de datos necesarias, determina las
funciones de la API, condiciona los requisitos de disponibilidad de la
infraestructura y establece los controles de seguridad requeridos por la
normativa colombiana.

**Fase 3 — Construcción del diagrama integrado y redacción del informe.**
Construimos el tablero de vistas integradas siguiendo la estructura del
Gartner Hybrid Integration Platform Framework como referencia visual, con
capas horizontales para cada vista y etiquetas de gobierno y operaciones
en los márgenes. Se decidió incluir seis capas (usuarios, negocio,
aplicaciones, información, infraestructura y seguridad) en lugar de las
cinco genéricas del caso base, ya que la vista de usuarios era necesaria
para mostrar cómo los actores se relacionan con el sistema.

La herramienta principal fue draw.io para el tablero visual y el diagrama
TO-BE de infraestructura sirvió como ancla para las decisiones
arquitectónicas de las demás vistas.

## 🧩 Análisis del modelo propuesto

**Estructura del modelo:**
El marco de integración está organizado en seis capas horizontales
apiladas de arriba hacia abajo, siguiendo la dirección natural de
dependencia: los usuarios demandan el negocio, el negocio define las
aplicaciones, las aplicaciones operan sobre los datos, los datos residen
en la infraestructura y la seguridad atraviesa todas las capas de forma
transversal. Esta estructura hace visible de un vistazo cómo una decisión
en una capa impacta a las demás.

**Cómo representa las necesidades del cliente:**
TransCapital tiene una necesidad central: garantizar la emisión legal del
FUEC de forma continua, trazable y sin depender de un único equipo físico
o persona. El modelo refleja esto poniendo la generación del FUEC como el
proceso dominante de la vista de negocio, y mostrando cómo cada capa
inferior lo soporta: PostgreSQL guarda el historial, la API lo genera
automáticamente, Tailscale garantiza acceso remoto seguro y el MFA
controla quién puede emitirlo. La decisión de mantener Google Sheets como
interfaz principal (en lugar de un formulario web) también está reflejada
en la vista de aplicaciones, donde Apps Script aparece como el conector
entre la herramienta familiar del equipo administrativo y la nueva
infraestructura centralizada.

**Supuestos tomados:**

- Se asume que el personal administrativo continuará usando Google Sheets
  como interfaz de entrada de datos, conectada a la API mediante Apps
  Script, para minimizar el cambio operativo.
- Se asume que el VPS económico (Hetzner o DigitalOcean, ~$15/mes) tiene
  capacidad suficiente para el volumen actual de operaciones de
  TransCapital.
- Cloudflare se incluyó como componente de seguridad perimetral pero
  marcado como implementación futura, dado que actualmente el VPS no
  expone servicios web públicos.
- Se asume que todos los dispositivos del personal administrativo tienen
  Tailscale instalado y configurado como condición previa para acceder
  al sistema.

## 📈 Diagrama final entregado

> 📎 Ver archivo: [`tablero-integrado-cliente.png`](https://github.com/285JuanDM/Arquitectura-empresarial-entregas/blob/master/Entrega%208%20-%20Integracion%20de%20Vistas%20de%20Arquitectura/Entrega/tablero-integrado-cliente.png)
>
> El diagrama muestra el marco de integración de las seis vistas
> arquitectónicas de TransCapital S.A.S en formato de capas horizontales,
> con relaciones de dependencia entre capas y componentes clickeables
> que permiten navegar al detalle de cada elemento.

## 📋 Tabla de actores, entidades o componentes

| Nombre del elemento          | Tipo               | Descripción                                                           | Vista           |
| ---------------------------- | ------------------ | --------------------------------------------------------------------- | --------------- |
| Personal administrativo      | Actor              | Genera y valida FUECs desde Google Sheets                             | Usuarios        |
| Conductores                  | Actor              | Reciben el FUEC digital para portar durante el servicio               | Usuarios        |
| Clientes (empresas/colegios) | Actor              | Contratan el servicio y son parte del contrato                        | Usuarios        |
| Administrador TI             | Actor              | Gestiona el VPS, Tailscale y los accesos                              | Usuarios        |
| Generación del FUEC          | Proceso            | Proceso crítico del negocio — sin él la operación se detiene          | Negocio         |
| REST API (Node.js/Python)    | Componente         | Lógica de negocio, validaciones y generación del PDF del FUEC         | Aplicaciones    |
| Google Workspace             | Componente         | Colaboración, Gmail, Drive para backups y Google Sheets como interfaz | Aplicaciones    |
| Apps Script                  | Componente         | Conector entre Google Sheets y la REST API                            | Aplicaciones    |
| WhatsApp Business            | Componente         | Canal de notificación a conductores y clientes                        | Aplicaciones    |
| Greenlink GPS                | Componente externo | Rastreo de vehículos — servicio externo sin modificaciones            | Aplicaciones    |
| Conductores (entidad)        | Entidad de datos   | cédula, nombre, fecha_vigencia_licencia                               | Información     |
| Vehículos / Buses            | Entidad de datos   | placa, tipo, SOAT, tarjeta de operación                               | Información     |
| Contratos                    | Entidad de datos   | identificación contratante, representante, dirección                  | Información     |
| FUEC                         | Entidad de datos   | Documento legal generado por contrato — entidad central del negocio   | Información     |
| Contrato_Buses               | Entidad de datos   | Tabla intermedia que relaciona contratos con vehículos (N:M)          | Información     |
| VPS económico                | Infraestructura    | Servidor cloud con PostgreSQL + API, accesible solo vía Tailscale     | Infraestructura |
| Tailscale VPN Mesh           | Infraestructura    | Red Zero Trust WireGuard — elimina exposición pública del VPS         | Infraestructura |
| Router Mikrotik              | Infraestructura    | Reemplaza router Claro, con firewall y bloqueo de puertos             | Infraestructura |
| PCs de oficina               | Infraestructura    | Equipos con BitLocker/FileVault — cifrado de disco completo           | Infraestructura |
| Google Identity (MFA)        | Seguridad          | Autenticación multifactor para acceso a Workspace y Tailscale         | Seguridad       |
| Cifrado en tránsito          | Seguridad          | HTTPS + WireGuard — todo el tráfico viaja cifrado                     | Seguridad       |
| Cifrado en reposo            | Seguridad          | BitLocker (Windows), FileVault (macOS), cifrado en PostgreSQL         | Seguridad       |
| Logs de auditoría            | Seguridad          | Registro de quién generó cada FUEC, cuándo y desde dónde              | Seguridad       |
| Cloudflare Free              | Seguridad          | Protección DDoS básica para servicios web expuestos (futuro)          | Seguridad       |

## 🔍 Investigación complementaria

### Tema investigado:

Integración de vistas arquitectónicas: marcos de referencia y buenas
prácticas de documentación (TOGAF, C4 Model, Gartner HIP Framework)

### Resumen:

TOGAF (The Open Group Architecture Framework) propone organizar la
arquitectura empresarial en cuatro dominios: negocio, datos, aplicaciones
y tecnología. Este taller siguió esa estructura base pero la adaptó
agregando una vista de usuarios y una de seguridad transversal, dado que
el contexto regulatorio colombiano (Resolución 3068/2014 del Ministerio de
Transporte) impone requisitos específicos de trazabilidad y control de
acceso que no quedan completamente cubiertos por los cuatro dominios
estándar de TOGAF.

El C4 Model de Simon Brown complementa a TOGAF ofreciendo una forma
práctica de documentar la vista de aplicaciones en cuatro niveles de
zoom: contexto, contenedores, componentes y código. Para TransCapital
aplicamos el nivel de contenedores, que es donde reside la distinción
clave entre la API (lógica) y PostgreSQL (persistencia), y el nivel de
componentes para mostrar cómo Apps Script conecta Google Sheets con la
API sin necesidad de desarrollar un formulario web independiente. Esta
decisión reduce el costo y la curva de adopción para el equipo
administrativo.

El Gartner Hybrid Integration Platform Capability Framework fue usado
como referencia visual para el tablero integrado: su estructura de capas
horizontales con gobernanza a la izquierda y operaciones a la derecha
resulta especialmente adecuada para TransCapital porque hace explícito
que la seguridad y el cumplimiento normativo no son una capa más sino
un eje transversal que atraviesa todas las demás. Esto refuerza el
argumento arquitectónico central del proyecto: que la propuesta TO-BE
no es solo una mejora técnica sino una respuesta directa a los
requisitos legales del negocio de transporte especial en Colombia.

_Este documento hace parte de la entrega del Taller 7 del curso de
Arquitectura Empresarial — Universidad de La Sabana._
