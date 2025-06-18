| Guía       | Título                                                   |
| ---------- | -------------------------------------------------------- |
| 06-161     | Visión General de Diagramas Estructurales en UML        |
| **06-162** | **Visión General de Diagramas de Comportamiento en UML** |

---
# 06-162:  Diagramas de Comportamiento


1. Introducción a los Diagramas de Comportamiento

2. Diagramas de Actividad
   2.1. Propósito y Accesibilidad No Técnica  
   2.2. Elementos Principales  
   2.3. Ejemplo de Servicio de Pedidos de Café  
   2.4. Modelado de Experiencia de Usuario  

3. Diagramas de Casos de Uso
   3.1. Ilustración de Sistema de Autorización  
   3.2. Componentes Principales  
   3.3. Ejemplo de Motor de Marketing  
   3.4. Control de Acceso Basado en Actores  

4. Diagramas de Máquina de Estados
   4.1. Visualización del Ciclo de Vida de Datos  
   4.2. Elementos Esenciales  
   4.3. Ejemplo de Embudo de Leads  
   4.4. Comparación con Diagramas de Actividad  

5. Diagramas de Secuencia
   5.1. Diseño de Sistemas Basado en Mensajes  
   5.2. Elementos Enfocados en Implementación  
   5.3. Ejemplo de Analizador de Teléfonos  
   5.4. Pensamiento de Sistemas Entrada-Salida  

6. Mejores Prácticas y Directrices de Implementación

7. Herramientas y Criterios de Selección de Diagramas

---



## ***1.    Introducción a los Diagramas de Comportamiento***
---
Los diagramas de Comportamiento representan los aspectos dinámicos del modelado UML, ilustrando **cómo los sistemas deben comportarse, actuar e interactuar con componentes internos y actores externos.** 

A diferencia de los diagramas estructurales que muestran qué existe en el sistema, los diagramas de Comportamiento **se enfocan en qué sucede** cuando el sistema se ejecuta, **aportando claridad** acerca del **comportamiento del sistema, interacciones de usuario y las relaciones dinámicas entre componente**s del sistema.

|                                  | Propósito                                     |
| -------------------------------- | --------------------------------------------- |
| **Diagrama de Casos de Uso**     | Actores e interacciones del sistema          |
| **Diagrama de Actividad**        | Flujos de trabajo y procesos de negocio      |
| **Diagrama de Máquina de Estados** | Estados de objetos y transiciones          |
| **Diagrama de Secuencia**        | Interacciones ordenadas en el tiempo         |
| **Diagrama de Comunicación**     | Interacciones de objetos con enlaces         |
| **Diagrama de Temporización**    | Interacciones con restricciones de tiempo    |
| **Diagrama de Visión General de Interacción** | Flujo de control entre interacciones |


Los **CUATRO** diagramas de Comportamiento principales cubiertos son:

- **Diagramas de Actividad**: Modelado de flujos de trabajo y procesos
- **Diagramas de Casos de Uso**: Interacción de usuario y funcionalidad del sistema
- **Diagramas de Máquina de Estados**: Transiciones de estado de objetos y ciclo de vida
- **Diagramas de Secuencia**: Paso de mensajes e interacciones del sistema


---

## ***2.    Diagramas de Actividad***
---
### Propósito y Accesibilidad No Técnica

Los diagramas de actividad son excepcionalmente poderosos para visualizar flujos de trabajo del sistema y procesos de usuario.   

Su mayor fortaleza radica en su **accesibilidad para partes interesadas no técnicas**. 

Stakeholders, usuarios comunes, que pueden no tener conocimientos sobre UML, pueden entender fácilmente los diagramas de actividad, haciéndolos invaluables para la comunicación entre todas las partes.

#### **Beneficios**

- **Mejora de la Comunicación**: Puente entre equipos técnicos y no técnicos
- **Documentación de Procesos**: Visualización clara de flujos de trabajo de negocio
- **Planificación de Sistemas**: Base para construir sistemas desde cero
- **Mapeo de Recorrido del Usuario**: Visualización completa del ciclo de vida del usuario


### Elementos Principales

Los diagramas de actividad comprenden seis componentes esenciales:

1. **Estado Inicial**: Punto de inicio del proceso (círculo negro sólido)
2. **Estado de Actividad/Acción**: Pasos o procesos individuales (rectángulos redondeados)
3. **Flujo de Acción**: Flechas direccionales mostrando el flujo del proceso
4. **Decisiones/Ramificación**: Formas de diamante representando puntos de elección
5. **Guardas**: Condiciones que deben cumplirse para las transiciones
6. **Estado Final**: Punto final del proceso (círculo negro sólido con anillo exterior)

---
### Ejemplo de Servicio de Pedidos de Café

El servicio de pedidos de café demuestra cómo los diagramas de actividad capturan interacciones complejas de usuario:

#### **Flujo del Proceso**

1. Usuario inicia pedido en línea
2. Punto de decisión basado en selección del usuario
3. Múltiples caminos dependiendo de las elecciones:

   - Búsqueda y selección de producto
   - Visualización de producto y detalles
   - Adición al carrito y gestión
   - Checkout y procesamiento de pago

Este único diagrama encapsula toda la experiencia del usuario, proporcionando a los desarrolladores una hoja de ruta clara para la implementación de la aplicación.

### Modelado de Experiencia de Usuario

Los diagramas de actividad sobresalen en el modelado de procesos de alto nivel porque se enfocan en actividades en lugar de detalles técnicos de implementación. Responden preguntas críticas:

- ¿Qué sucede cuando los usuarios buscan productos?
- ¿Cómo navegan los usuarios la selección de productos?
- ¿Qué puntos de decisión existen en el recorrido del usuario?
- ¿Cómo afectan las diferentes elecciones del usuario al flujo de trabajo?

---


## ***3.    Diagramas de Casos de Uso***
---
### Ilustración de Sistema de Autorización

Los diagramas de casos de uso **proporcionan visualmente un alto nivel de la funcionalidad del sistema y derechos de acceso del usuario.**  

Son particularmente valiosos para diseñar sistemas de autorización, mostrando claramente qué diferentes tipos de usuarios pueden acceder y lograr dentro del sistema.

#### **Aplicaciones Principales**

- **Diseño de Autorización**: Definir roles de usuario y permisos
- **Definición de Alcance del Sistema**: Establecer límites para la funcionalidad del sistema
- **Comunicación con Partes Interesadas**: Presentación clara de capacidades del sistema
- **Planificación de Características**: Vista comprehensiva de características del sistema


### Componentes Principales

Los diagramas de casos de uso consisten en **CUATRO** elementos fundamentales:

1. **Casos de Uso**: Funcionalidad del sistema representada como óvalos
2. **Actores**: Usuarios o sistemas externos (figuras de palitos)
3. **Subsistemas**: Funcionalidad agrupada dentro de límites del sistema
4. **Relaciones**: Conexiones mostrando interacciones y dependencias

---
### Ejemplo de Motor de Marketing

El diagrama de casos de uso del motor de marketing ilustra escenarios de actor dual:

#### **Roles de Actores**

- **Especialista en Marketing**: Acceso administrativo y creación de contenido
- **Cliente**: Interacción de usuario final y consumo


#### **Tipos de Relaciones**

- **Asociación**: Conexiones directas actor-a-caso de uso
- **Include**: Dependencias de funcionalidad requerida
- **Extend**: Extensiones de funcionalidad opcional

Diferentes actores acceden a los mismos casos de uso a través de diferentes caminos, demostrando cómo los sistemas de autorización controlan el comportamiento del usuario y los derechos de acceso.


### Control de Acceso Basado en Actores

Los diagramas de casos de uso modelan efectivamente escenarios complejos de autorización:

- **Empleado vs. Admin**: Diferentes niveles de acceso a sistemas de hojas de tiempo
- **Cliente vs. Especialista**: Capacidades variables dentro del mismo sistema
- **Permisos Basados en Roles**: Visualización clara de quién puede hacer qué

---


## ***4.    Diagramas de Máquina de Estados***
---
### Visualización del Ciclo de Vida de Datos

Los diagramas de máquina de estados representan uno de los conceptos fundamentales de las ciencias de la computación, **visualizando cómo los datos y objetos transicionan a través de diferentes estados durante el ciclo de vida del sistema.**  

Se enfocan en las varias etapas de los componentes del sistema y las condiciones que disparan cambios de estado.

#### **Propósito Principal**

- **Modelado de Transición de Estados**: Cómo los objetos cambian con el tiempo
- **Lógica Basada en Condiciones**: Reglas que gobiernan cambios de estado
- **Comportamiento del Sistema**: Aspectos dinámicos de componentes del sistema
- **Gestión del Ciclo de Vida**: Visualización completa del ciclo de vida del objeto


### Elementos Esenciales

Los diagramas de máquina de estados incorporan cinco componentes clave:

1. **Punto de Entrada**: Estado inicial (círculo negro sólido)
2. **Elecciones**: Puntos de decisión determinando transiciones
3. **Restricciones**: Condiciones que gobiernan cambios de estado
4. **Estados**: Condiciones o situaciones estables (rectángulos)
5. **Transiciones**: Movimientos estado-a-estado (flechas)

---
### Ejemplo con el Embudo de Leads

La máquina de estados del embudo de leads demuestra la progresión del cliente:

#### **Progresión de Estados**

- **Visitante**: Estado inicial del usuario
- **Convertido**: Estado post-envío de formulario
- **Lead**: Estado de prospecto calificado
- **Cliente**: Estado de conversión final

Cada transición requiere condiciones específicas, ilustrando cómo las reglas de negocio gobiernan la progresión del cliente a través del embudo de ventas.

---
### Comparación con Diagramas de Actividad

Los diagramas de máquina de estados comparten similitudes con los diagramas de actividad pero se enfocan en aspectos diferentes:

#### **En qué se Enfoca la Máquina de Estados**

- Estados de objetos y transiciones
- Cambios basados en condiciones
- Gestión del ciclo de vida de datos


#### **En qué se Enfoca el Diagrama de Actividades**

- Flujos de trabajo de procesos
- Actividades de usuario
- Acciones secuenciales


>**La elección entre diagramas depende de si estás modelando estados de objetos o flujos de trabajo de procesos.**

---


## ***5.    Diagramas de Secuencia***
---

### Diseño de Sistemas Basado en Mensajes

Los diagramas de secuencia ***representan interacciones sofisticadas del sistema a través del paso de mensajes***.     

Los desarrolladores senior favorecen estos diagramas porque modelan aplicaciones como sistemas de componentes comunicantes, tanto internos como externos.   

Proporcionan detalle a nivel de implementación que se traduce directamente a estructura de código.

#### **Valor Estratégico**

- **Guía de Implementación**: Traducción directa a código
- **Arquitectura del Sistema**: Diseño de sistema basado en mensajes
- **Planificación de Integración**: Comunicación de sistemas externos
- **Ayuda de Depuración**: Entender el flujo de mensajes del sistema



### Elementos Enfocados en Implementación

Los diagramas de secuencia comprenden **CUATRO componentes críticos**:

1. **Roles de Clase/Participantes**: Componentes del sistema involucrados en interacciones
2. **Activación/Ocurrencia de Ejecución**: Períodos de procesamiento activo (rectángulos anchos)
3. **Mensajes** (Y Respuestas): Comunicaciones entre componentes (flechas)
4. **Líneas de Vida**: Líneas verticales representando la existencia del componente a través del tiempo


---
### Ejemplo de Analizador de Teléfonos

El diagrama de secuencia del analizador de teléfonos ilustra interacciones complejas del sistema:

#### **Flujo de Mensajes**

1. **Entrada**: Datos a analizar entran al sistema
2. **Auto-Mensaje**: Motor de análisis procesa internamente ("eliminar todos los símbolos excepto números")
3. **Mensaje Externo**: Solicitud de validación al validador de longitud de dígitos
4. **Mensaje de Respuesta**: Resultado de validación (flecha punteada)
5. **Salida**: Resultado del número de teléfono analizado

Este diagrama proporciona comprensión completa de entrada-salida, mostrando tanto el objetivo como el camino de implementación.

----
### Pensamiento de Sistemas Entrada-Salida

Los diagramas de secuencia promueven pensamiento sistemático sobre:

- **Entradas de Método**: Qué datos entran a cada componente
- **Salidas Esperadas**: Qué resultados produce cada componente
- **Contratos de Mensaje**: Definiciones claras de interfaz
- **Dependencias del Sistema**: Requisitos de interacción de componentes


>**Entender sistemas a través del paso de mensajes crea hojas de ruta claras de implementación y simplifica arquitectura compleja del sistema en patrones de comunicación manejables.**

---


## ***6.    Buenas Prácticas y Directrices de Implementación***
---
### Directrices para Diagramas de Actividad

- Empezar con puntos de entrada del usuario e identificar todos los endpoints posibles
- Usar etiquetas claras y descriptivas para actividades y puntos de decisión
- Mantener diagramas enfocados en procesos únicos o recorridos de usuario
- Incluir todos los puntos de decisión significativos y caminos alternativos
- Validar flujos de trabajo con partes interesadas del negocio

### Recomendaciones para Diagramas de Casos de Uso

- Definir claramente límites del sistema antes de identificar casos de uso
- Enfocarse en objetivos del usuario en lugar de características del sistema
- Usar representaciones consistentes de actores a través de diagramas
- Documentar relaciones entre casos de uso relacionados
- Revisar regularmente derechos de acceso y permisos con partes interesadas

### Buenas Prácticas para Diagramas de Máquina de Estados

- Identificar todos los estados posibles antes de modelar transiciones
- Definir condiciones claras para cada transición de estado
- Incluir estados de error y manejo de excepciones
- Documentar acciones de entrada y salida de estado
- Validar lógica de estado con expertos del dominio

### Directrices para Diagramas de Secuencia

- Enfocarse en intercambios de mensajes significativos, evitar interacciones triviales
- Usar convenciones de nomenclatura consistentes para participantes
- Mostrar tanto flujos de mensajes exitosos como de error
- Incluir mensajes de retorno para interacciones complejas
- Alinear diagramas con arquitectura de implementación real



### Consejos Generales para Diagramas de Comportamiento

- **Selección de Diagramas**: Elegir diagramas basados en necesidades específicas de modelado
- **Alineación de Partes Interesadas**: Hacer coincidir complejidad del diagrama con nivel técnico de la audiencia
- **Refinamiento Iterativo**: Actualizar continuamente diagramas conforme evoluciona la comprensión
- **Trazabilidad de Implementación**: Asegurar que los diagramas puedan guiar el desarrollo real
- **Consistencia Entre Diagramas**: Mantener consistencia a través de diferentes tipos de diagramas

---


## ***7.    Criterios de Selección de Diagramas***
---
### Marco de Selección de Diagramas

Cada diagrama comportamental sirve escenarios específicos:

### **Cuándo Usar Diagramas de Actividad**

- Modelar procesos de negocio
- Comunicar con partes interesadas no técnicas
- Planificar flujos de trabajo de experiencia de usuario
- Documentar procesos del sistema


### **Cuándo Usar Diagramas de Casos de Uso**

- Definir alcance y límites del sistema
- Diseñar sistemas de autorización
- Planificar características del sistema
- Comunicar con analistas de negocio


### **Cuándo Usar Diagramas de Máquina de Estados**

- Modelar ciclos de vida de objetos
- Diseñar comportamiento dependiente de estado
- Planificar lógica basada en condiciones
- Entender transiciones de datos


### **Cuándo Usar Diagramas de Secuencia**

- Diseñar interacciones del sistema
- Planificar integraciones de API
- Entender flujos de mensajes
- Crear planos de implementación

---
