	#### 3.2 Actividad

| Guía       | Título                                                                                    |
| ---------- | ----------------------------------------------------------------------------------------- |
| **06-168** | **Elementos de un Diagrama de Actividad UML**                                             |
| 06-169     | Ejemplo: Cómo Diseñar un Diagrama de Actividad para un Sistema de Calificaciones en Línea |

----
# 06-168:  Diagramas de Actividad



1. Introducción a los Diagramas de Actividad

2. Elementos Principales

3. Análisis Detallado de Elementos
   
   - Estado Inicial (Punto de Inicio)
   - Estado de Actividad/Acción
   - Flujo de Acción
   - Puntos de Decisión y Ramificación
   - Guardas
   - Estado Final (Punto Final)
   - Carriles (Swim Lanes) (Swim Lanes)

4. Contexto de Aplicación Práctica

5. Consideraciones de Diseño y Mejores Prácticas

---


## ***1.     Introducción a los Diagramas de Actividad***
---
Los Diagramas de Actividad UML son **diagramas comportamentales que ilustran el flujo de actividades dentro de un sistema o proceso**.   

Proporcionan una **representación visual de flujos de trabajo**, procesos de negocio y lógica algorítmica, haciéndolos herramientas esenciales para el análisis y diseño de sistemas.


Los diagramas de actividad son particularmente útiles para:

- Modelar procesos de negocio
- Describir escenarios de casos de uso
- Representar flujos de trabajo algorítmicos
- Documentar comportamiento del sistema a través de diferentes actores

---

## ***2.     Elementos Principales***
---
Los diagramas de actividad consisten en **SIETE** elementos fundamentales que trabajan juntos para representar el flujo de procesos:

1. **Estado Inicial** 
   El punto de inicio de cualquier flujo de actividad

2. **Estado de Actividad/Acción**  
   Acciones/procesos individuales dentro del flujo de trabajo.

3. **Flujo de Acción** 
   Conexiones entre diferentes estados mostrando la dirección del proceso

4. **Puntos de Decisión**
   Puntos de ramificación donde el flujo puede tomar diferentes caminos

5. **Guardas**
   Condiciones que determinan qué camino seguir en los puntos de decisión

6. **Estado Final** 
   El punto de terminación del flujo de actividad

7. **Carriles (Swim Lanes)**
   Límites organizacionales que agrupan actividades por responsabilidad

---


## ***3.     Análisis Detallado de Elementos***
---

### **1.    Estado Inicial (Punto de Inicio)**

El **Estado Inicial** está representado por **un círculo negro grueso relleno y marca el comienzo de cualquier diagrama de actividad**.

Este elemento **indica dónde un usuario o sistema comienza el flujo del proceso**.

![](./06-168_IMG1.png)

#### **Características**

- Cada diagrama de actividad debe tener exactamente un estado inicial
- Representa el disparador o condición de inicio para todo el proceso
- Sin flujos entrantes, solo flujos de acción salientes

#### **Contexto del ejemplo** 

En un sistema de calificaciones, el estado inicial representa cuándo un profesor decide asignar una prueba o quiz.

---

### 2.    **Estado de Actividad/Acción**

**Las Actividades** o **Estados de Acción** son los bloques de construcción principales de los diagramas de actividad, representados por cajas rectangulares (pueden tener bordes redondeados dependiendo de la herramienta UML utilizada).

![](./06-168_IMG2.png)

#### **Características**

- **Cada caja** representa **una sola acción, proceso o estado** dentro del flujo de trabajo
- Las actividades deben ser "atómicas" -> **representando una acción o transformación clara**
- La mayor parte del contenido del diagrama consiste en estos estados de actividad
- Las actividades **representan puntos donde ocurren cambios o alteraciones de datos**

#### **Principios de Diseño**

 Al traversar el diagrama como usuario, cada actividad representa una etapa donde algo significativo sucede a los datos o estado del sistema.

#### **Ejemplos del Sistema de Calificaciones**

- *"Generar conjunto individual de preguntas"*
- *"Confirmar parámetros de preguntas"*
- *"Hacer pregunta al estudiante"*

---

### 3.    **Flujo de Acción**

**Los Flujos de Acción** están **representados por flechas** con puntas de flecha rellenas que conectan diferentes actividades, mostrando la dirección del flujo del proceso.

![](./06-168_IMG3.png)

#### **Características**

- **Indica la secuencia y dirección** de las actividades
- Muestra **cómo los datos o control se mueven de un estado a otro**
- Crea el **camino lógico** a través del proceso
- Esencial para entender las dependencias del proceso

#### **Comprensión Conceptual**

 Los flujos de acción <u>representan el "movimiento"</u> de algo (datos, control o estado del proceso) de una actividad a otra, creando la estructura lógica del flujo de trabajo.

---

### 4.    **Puntos de Decisión y Ramificación**

**Los Puntos de Decisión** están **representados por formas de diamante** ("cuadrado rotado 45 grados") e indican ubicaciones donde **deben tomarse decisiones**, donde **el flujo del proceso debe elegir** entre diferentes caminos basados en condiciones específicas.

![](./06-168_IMG4.png)

#### **Características**

- La forma de diamante representa un **punto de ramificación o nodo de decisión**
- Exactamente **un flujo entrante y múltiples flujos salientes**
- **Cada flujo saliente** representa un **camino posible diferente**
- Las decisiones se basan en condiciones o criterios evaluados en ese punto

#### **Contexto del ejemplo** 

En el sistema de calificaciones, un punto de decisión podría preguntar "¿Era esta la última pregunta?" llevando a diferentes acciones basadas en la respuesta.

---

### 5.    **Guardas**

**Las Guardas** son **condiciones** o **criterios** asociados con flujos de acción **que salen de puntos de decisión**, típicamente representadas como etiquetas de texto como "sí," "no," o expresiones condicionales más complejas.

![](./06-168_IMG5.png)

#### **Características**

- Definen las **condiciones bajo las cuales se toma un camino de flujo particular**
- Pueden ser condiciones booleanas simples o expresiones lógicas complejas
- Esenciales para entender cuándo se ejecutan diferentes caminos
- Críticas para la lógica del proceso y control de flujo

#### **Consideración de Diseño** 

> **Mientras más guardas y ramificaciones en un sistema, mayor la complejidad. **

Múltiples ramificaciones desde un solo punto de decisión pueden indicar necesidad de revisión de diseño, ya que los cambios se vuelven más difíciles de propagar a través del sistema.

---

### 6.    **Estado Final (Punto Final)**

El **Estado Final** representa la **terminación del flujo de actividad**, mostrado como un círculo con un círculo relleno más pequeño adentro (patrón de ojo de buey).

![](./06-168_IMG6.png)

#### **Características**

- Indica la compleción de todo el proceso
- Según la especificación UML, **cada diagrama de actividad debe tener un estado final**
- **Solo flujos entrantes**, sin flujos salientes
- Representa la compleción exitosa del flujo de trabajo

#### **Ejemplo de Contexto** 

En el sistema de calificaciones, el estado final ocurre cuando los resultados se almacenan en la base de datos del sistema.

---

### 0.    **Carriles (Swim Lanes) (Swim Lanes)**

**Los Carriles (Swim Lanes)** son divisiones verticales u horizontales que organizan actividades basadas en responsabilidad, rol o límites organizacionales.

![](./06-168_IMG7.png)

#### **Características**

- Proporcionan estructura organizacional a diagramas complejos
- Delinean claramente responsabilidades entre diferentes actores
- Ayudan a identificar quién realiza qué actividades
- Esenciales para procesos multi-actor

#### **Beneficios**

- **Claridad de Responsabilidad/Actores**: Identificación visual inmediata de quién hace qué
- **Organización del Sistema**: Separación clara de responsabilidades del sistema, usuario y actores externos
- **Comprensión del Proceso**: Comprensión más fácil de interacciones de roles y traspasos

#### **Ejemplo de Estructura del Sistema de Calificaciones:**

- **Carril del Mentor**: Actividades relacionadas con creación de pruebas y revisión de resultados

- **Carril del Sistema**: Procesos automatizados como generación de preguntas y almacenamiento de resultados

- **Carril del Estudiante**: Actividades realizadas por estudiantes durante la evaluación

***


## ***4.     Contexto de Aplicación Práctica***
---
El ejemplo del sistema de calificaciones demuestra cómo estos elementos trabajan juntos en un escenario del mundo real:

1. **Iniciación del Proceso**: El profesor decide crear un quiz (Estado Inicial)
2. **Acciones del Sistema**: Generar preguntas, configurar parámetros (Actividades)
3. **Control de Flujo**: Preguntas presentadas en secuencia (Flujos de Acción)
4. **Lógica de Decisión**: Determinar si quedan más preguntas (Puntos de Decisión con Guardas)
5. **Compleción del Proceso**: Almacenar resultados en base de datos (Estado Final)
6. **Distribución de Responsabilidades**: Separación clara entre acciones de profesor, sistema y estudiante (Carriles (Swim Lanes))

---


## ***5.     Consideraciones de Diseño y Mejores Prácticas***
---
### Gestión de la Complejidad

- **Minimizar Ramificación**: Los puntos de decisión excesivos aumentan la complejidad del sistema
- **Actividades Atómicas**: Cada actividad debe representar una acción clara e indivisible
- **Dirección de Flujo Clara**: Asegurar que los flujos de acción creen caminos lógicos y fáciles de seguir

### Claridad Organizacional

- **Carriles (Swim Lanes) Efectivos**: Usar Carriles (Swim Lanes) para separar claramente responsabilidades
- **Nomenclatura Consistente**: Usar nombres claros y descriptivos para actividades y guardas
- **Agrupación Lógica**: Agrupar actividades relacionadas dentro de carriles apropiados

### Mantenibilidad / Escalabilidad

- **Análisis de Impacto**: Considerar cómo los cambios se propagan a través de múltiples ramificaciones
- **Documentación**: Asegurar que las guardas y condiciones de decisión estén claramente documentadas
- **Validación**: Verificar que todos los caminos lleven a estados finales apropiados

---
