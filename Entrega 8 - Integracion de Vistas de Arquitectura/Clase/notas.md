# Taller 7: Integración de Vistas de Arquitectura - FarmApp 💊🚗
> **Curso:** Arquitectura Empresarial | **Institución:** Universidad de La Sabana 


---

## 👥 Integrantes del Equipo
* Oscar David Vergara Moreno 
* Jaime Andrés Olarte 
* Juan David Moreno

---

## 🗺️ 1. Entregable A: Tablero de Vistas Integradas (Caso Base)
*Este tablero visual representa la interconexión completa de las 5 capas arquitectónicas solicitadas, garantizando que ningún componente quede aislado.*
```mermaid
flowchart TD
    %% Estilos de Capas
    classDef negocio fill:#f9f,stroke:#333,stroke-width:2px;
    classDef info fill:#bbf,stroke:#333,stroke-width:2px;
    classDef app fill:#fbf,stroke:#333,stroke-width:2px;
    classDef infra fill:#fdb,stroke:#333,stroke-width:2px;
    classDef seg fill:#f66,stroke:#fff,stroke-width:2px,stroke-dasharray: 5 5;

    %% CAPA DE NEGOCIO
    subgraph Capa_Negocio [1. VISTA DE NEGOCIO]
        N1[Proceso de Compra Web/App] --> N2[Validación de Prescripción Médica]
        N2 --> N3[Gestión de Despacho y Logística]
    end
    class N1,N2,N3 negocio;

    %% CAPA DE INFORMACIÓN
    subgraph Capa_Informacion [2. VISTA DE INFORMACIÓN]
        I1[(Entidad: Cliente / CRM)] --- I2[(Entidad: Pedido)]
        I2 --- I3[(Entidad: Producto / Stock)]
        I1 --- I4[(Entidad: Descuentos / Promociones)]
    end
    class I1,I2,I3,I4 info;

    %% CAPA DE APLICACIONES
    subgraph Capa_Aplicaciones [3. VISTA DE APLICACIONES]
        A1[App Móvil / Frontend Web] --> A2[Plataforma E-Commerce Core]
        A2 --> A3[Sistema CRM]
        A2 --> A4[Sistema POS Tiendas Físicas]
    end
    class A1,A2,A3,A4 app;

    %% CAPA DE INFRAESTRUCTURA
    subgraph Capa_Infraestructura [4. VISTA DE INFRAESTRUCTURA]
        IN1[Cloud: AWS EC2 / Azure VMs] --- IN2[(Base de Datos Replicada en la Nube)]
        IN4[On-Premise: Servidores Regionales / Locales POS] --- IN2
    end
    class IN1,IN2,IN4 infra;

    %% CAPA DE SEGURIDAD (Transversal)
    subgraph Capa_Seguridad [5. VISTA DE SEGURIDAD]
        S1[Control de Accesos por Rol - RBAC]
        S2[Cifrado de Datos Personales - TLS/AES]
        S3[Monitoreo Activo de Fraude]
    end
    class S1,S2,S3 seg;

    %% RELACIONES ENTRE CAPAS (Trazabilidad Corregida)
    N1 -->|Soportado por| A1
    I2 -->|Procesado en| A2
    I1 -->|Almacenado en| A3
    A2 -->|Desplegado en| IN1
    A4 -->|Ejecutado en| IN4
    S1 -.->|Protege acceso a fórmulas| N2
    S2 -.->|Resguarda datos PII| I1
    S3 -.->|Evalúa pasarela de pagos| A2
```

## 🔍 3. Resumen de las Vistas Arquitectónicas

Para entender cómo funciona **FarmApp**, podemos dividir el sistema en 5 capas que trabajan en equipo. Ninguna funciona sola; cada una apoya a la siguiente:

### 1. Vista de Negocio (¿Qué hace la empresa?)
Es la capa que ve el cliente y la operación del negocio. Aquí se definen los pasos que se siguen en la vida real: desde que una persona entra a la aplicación a buscar un medicamento, pasando por la revisión obligatoria de su receta médica, hasta que el repartidor lleva el producto a su casa.

### 2. Vista de Información (¿Qué datos manejamos?)
Es el cerebro de los datos. Aquí organizamos la información clave que el negocio necesita recordar y procesar. Incluye las fichas de los **Clientes** (sus datos y alergias), el inventario de **Productos** (qué medicamentos hay y cuáles están agotados), los detalles de cada **Pedido** y los **Descuentos** que se le pueden aplicar a un usuario fiel.

### 3. Vista de Aplicaciones (¿Qué software usamos?)
Son los programas y plataformas que hacen posible el trabajo. En esta capa se encuentran la **App móvil** y la **Página Web** que usa el cliente, el **Sistema POS** (la pantalla que usan los cajeros en las tiendas físicas para cobrar) y el **CRM** (el sistema que administra las promociones y los datos de los clientes).

### 4. Vista de Infraestructura (¿Dónde corre todo?)
Es la maquinaria tecnológica física y virtual que sostiene los programas. FarmApp utiliza un modelo híbrido:
*   **La Nube:** Donde se guarda la página web, la app y la base de datos principal para que nunca se caigan y soporten miles de clientes a la vez.
*   **Servidores Locales:** Computadores físicos dentro de cada farmacia para que, si el internet se llega a ir, los cajeros puedan seguir vendiendo sin problemas.

### 5. Vista de Seguridad (¿Cómo nos protegemos?)
Es la capa que cuida todo el ecosistema de punta a punta. Se encarga de tres cosas críticas: que solo los empleados autorizados (como los farmacéuticos) puedan ver recetas médicas, que los datos personales y de tarjetas de los clientes viajen encriptados (secretos), y que haya un sistema vigilando en tiempo real para evitar fraudes con los pagos.
