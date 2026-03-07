# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

Taller 1 - Modelado de Procesos de Negocio con BPMN

## 👥 Integrantes del equipo

* Sofia Vargas Garzon
* Juan David Moreno Suarez
* Jaime Andres Olarte
* Oscar Vergara

## 🧠 Descripción general del trabajo

Este taller tuvo como objetivo modelar el proceso de generación del Formato Único de Extracto del Contrato (FUEC) de la empresa TRANS CAPITAL S.A.S utilizando la notación BPMN. El FUEC es un documento obligatorio que certifica la legalidad de los servicios de transporte prestados, incluyendo información del conductor, vehículo y servicio. El modelado permitió representar gráficamente el flujo actual del proceso, facilitando su comprensión, análisis e identificación de oportunidades de mejora.

## 🔧 Proceso de desarrollo

El desarrollo inició con el análisis del proceso real de generación del FUEC, identificando las actividades involucradas desde la solicitud del documento hasta su envío al conductor. Se determinó que el proceso es manual y depende completamente del personal administrativo.

Posteriormente, se identificaron los elementos BPMN necesarios, como el evento de inicio, las actividades, el punto de decisión relacionado con la verificación de la información y el evento de fin. Se utilizó draw.io como herramienta para construir el diagrama, organizando el flujo de manera secuencial y clara. Durante el modelado, se realizaron ajustes para asegurar que el diagrama representara correctamente el proceso real.

## 🧩 Análisis del modelo propuesto

El modelo se estructura de forma secuencial, iniciando con la necesidad de generar el FUEC, seguido por el diligenciamiento de la información en Excel, la verificación de los datos, la impresión del documento, su digitalización y su envío final.

El modelo representa adecuadamente las necesidades de la empresa, ya que refleja el flujo real utilizado para generar el documento, así como el rol principal del personal administrativo en todas las actividades.

Se asumió que la verificación de la información es un punto crítico del proceso, ya que los errores en la digitación pueden afectar la validez del documento. También se consideró que el proceso es completamente manual y no cuenta con automatización.

## 📈 Diagrama final entregado

![Modelo BPMN Generación FUEC](modelo-final.png)

## 📋 Tabla de actores, entidades o componentes

| Nombre del elemento     | Tipo        | Descripción                                                     | Responsable             |
| ----------------------- | ----------- | --------------------------------------------------------------- | ----------------------- |
| Personal administrativo | Actor       | Encargado de diligenciar, verificar, generar y enviar el FUEC   | TRANS CAPITAL S.A.S     |
| FUEC                    | Documento   | Documento que certifica la legalidad del servicio de transporte | TRANS CAPITAL S.A.S     |
| Plantilla Excel         | Herramienta | Archivo utilizado para registrar la información del FUEC        | Personal administrativo |

## 🔍 Investigación complementaria

### Tema investigado:

Buenas prácticas en el modelado de procesos utilizando BPMN.

#### Buenas Prácticas BPMN y Aplicación en la Industria

Para el modelado efectivo de modelos de negocio implementado BPMN se requiere el seguimiento de principios fundamentales que garantizan la claridad y comprensión del diagrama. Para esto primeramente se tiene que usar Momenclatura, la cual constituye un elemento crítico, donde cada actividad debe nombrarse utilizando la estructura verbo-sustantivo, como "Registrar Paciente" o "Validar Documentos”, este uso de nomenclaturas permite que cualquier lector identifique inmediatamente la acción y el objeto sobre el cual se ejecuta, evitando ambigüedades que puedan generar interpretaciones erróneas del proceso. Dentro de la estructura del proceso debe seguirse principios de diseño que faciliten su comprensión visual. Freund y Rücker establecen la regla que sugiere mantener entre 5 y 9 elementos por linea  para preservar la legibilidad del modelo.Cuando se sobrecarga un diagrama este pierde su comprensión y dificulta su análisis. Asimismo, cada proceso principal debe contar con un único evento de inicio y un único evento de fin claramente identificables, permitiendo trazar el flujo completo desde su activación hasta su conclusión. El flujo debe diseñarse de izquierda a derecha y de arriba hacia abajo, siguiendo los patrones naturales de lectura occidental, lo que facilita la navegación intuitiva a través del proceso.

El uso correcto de los elementos BPMN representa otro pilar fundamental de las buenas prácticas. Las compuertas deben hacerse explícitos mediante el uso de rombos de decisión, evitando la práctica incorrecta de generar múltiples flujos directamente desde una tarea. Esta claridad permite identificar con precisión los puntos de decisión y las condiciones que gobiernan cada rama del proceso. Es esencial comprender la diferencia conceptual entre eventos y tareas: los eventos representan algo que sucede, mientras que las tareas representan algo que se hace activamente.

#### Ejemplos de Aplicación en la Industria

En el sector de tecnología y software, IBM implementó BPMN para optimizar sus procesos de desarrollo y entrega de software siguiendo metodologías DevOps, logrando reducir el tiempo de despliegue. Su modelo incluyó lanes para Development, Testing, Operations y Security, integrando procesos de integración continua y entrega continua (CI/CD). Adicionalmente, utilizaron internamente  BPMN para modelar sus procesos de clientes en servicios SaaS, incorporando subprocesos para configuración técnica, capacitación de usuarios y migración de datos. Este enfoque les permitió estandarizar la experiencia de implementación y reducir el tiempo promedio de activación de nuevos clientes.

#### Validación de modelos BPMN
 
La validación de un modelo BPMN debe evaluarse en múltiples dimensiones para garantizar su calidad y utilidad. Desde el punto de vista sintáctico, cada gateway debe mantener un balance entre sus entradas y salidas, asegurando que todos los flujos que se dividen eventualmente conduzcan a eventos de fin válidos. La semántica del modelo requiere que no existan elementos cuyo significado sea ambiguo o complejo, cada actividad, evento o gateway debe tener un propósito claramente definido que pueda explicarse con claridad.

## 📚 Referencias

* [1] Object Management Group. *Business Process Model and Notation (BPMN) Version 2.0*. [https://www.omg.org/spec/BPMN/](https://www.omg.org/spec/BPMN/)
* [2] Camunda. *BPMN Reference Guide*. [https://camunda.com/bpmn/reference/](https://camunda.com/bpmn/reference/)