```mermaid
flowchart TD
    A[Inicio: Cliente envía la orden de compra] --> B[Llega la orden de compra vía página web]
    B --> C[Administración descarga la orden de compra]
    C --> D[Chequeo superficial de la orden]
    D --> E{La orden tiene errores?}
    E -- Sí --> F[Comunicación con el cliente]
    F --> G[Corrección del error en el pedido]
    G --> D
    E -- No --> H[Traslado de la nota de ventas hacia expedición]
    H --> I[Preparación del pedido]
    I --> J[Chequeo minucioso del pedido]
    J --> K{Hay errores en la preparación del pedido?}
    K -- Sí --> L[Corrección de errores en expedición]
    L --> J
    K -- No --> M[Regresa la nota de ventas para facturar]
    M --> N[Facturación]
    N --> O[Coordinación de la logística del pedido con el transportista]
    O --> P[Carga del pedido y control con la factura]
    P --> Q[Entrega del pedido al transportista y al cliente]
    Q --> R[Fin del proceso]

