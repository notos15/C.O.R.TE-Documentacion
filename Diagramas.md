# Catálogo de Diagramas de Arquitectura y Diseño - Proyecto C.O.R.T.E.

En este documento se presentan los diagramas de modelado del sistema para el proyecto **C.O.R.T.E. (Control Operativo y Registro Total de Espacios)** de Cervecería Cuello Negro.

Cada sección contiene la visualización del diagrama, una breve descripción técnica de su propósito y el enlace correspondiente para su consulta o edición externa.

---

### 1. Diagrama de Componentes
![Diagrama de Componentes](diagramas/Componentes.png)

* **Comparativa y Propósito:** Ilustra la arquitectura modular del sistema, la interacción entre el cliente (interfaz del Gemelo Digital en tablets/móviles), el API Backend de lógica de negocios, el motor de recomendación espacial (FEFO/FIFO) y la integración con el ERP existente.
* **Cambios realizados:** Se estructuraron las interfaces de comunicación REST/Webhooks y los límites de componentes.
* **Link de visualización/edición:** [Ver en herramienta de diseño (Lucidchart / Figma)](https://tu-link-aqui.com)

---

### 2. Diagrama de Base de Datos
![Diagrama de Base de Datos](diagramas/Base_de_datos.png)

* **Comparativa y Propósito:** Especifica la implementación física relacional (tablas, tipos de datos, llaves primarias, llaves foráneas e índices) para la persistencia del inventario, gestión de lotes y control de ubicaciones dentro de la bodega de frío.
* **Cambios realizados:** Normalización de tablas para garantizar la integridad referencial de los estados de apilamiento y caducidad.
* **Link de visualización/edición:** [Ver en herramienta de diseño (DBDiagram / Draw.io)](https://tu-link-aqui.com)

---

### 3. Diagrama Entidad-Relación (E/R)
![Diagrama Entidad Relacion](diagramas/Entidad-Relacion.png)

* **Comparativa y Propósito:** Define las entidades del dominio de negocio (Pallet, Lote, Ubicación, Registro de Movimiento, Usuario, Orden) y sus cardinalidades conceptuales dentro del proceso logístico.
* **Cambios realizados:** Se incorporó la regla de negocio para el control de capacidad y límite de apilado (máximo 4 pallets por columna).
* **Link de visualización/edición:** [Ver en herramienta de diseño](https://tu-link-aqui.com)

---

### 4. Diagrama de Actividad
![Diagrama de Actividad](diagramas/Actividad.jpng)

* **Comparativa y Propósito:** Modela el flujo operativo paso a paso que realiza un operario de planta desde la recepción e ingreso de producto hasta la asignación de ubicación guiada por el algoritmo y el posterior despacho de lotes.
* **Cambios realizados:** Inclusión de bifurcaciones condicionales para manejo de excepciones de conectividad u offline en la bodega de frío.
* **Link de visualización/edición:** [Ver en herramienta de diseño (Miro / Figma)](https://tu-link-aqui.com)