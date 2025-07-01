|Guía|Título|
|---|---|
|07-187|La Importancia del Análisis y Diseño de Sistemas|
|07-188|Visión General de Sistemas de Software|

|Guía|Título|
|---|---|
|06-150|Visión General de UML|
|06-151|Etapas de Desarrollo donde se Utiliza UML|

|Guía|Título|
|---|---|
|**06-160**|**Introducción a Diagramas y Categorías**|

---

# 06-150: Diagramas UML - Visión general de categorías


# _**1. Tipos  de Diagramas UML**_
---

Los diagramas UML (Unified Modeling Language) se dividen en **dos categorías principales**:

- #### 1. Estructurales
    
- #### 2. De Comportamiento.
    

Esta distinción clara ayuda a los desarrolladores a identificar rápidamente qué tipo de diagrama usar basándose en lo que están modelando.

---

## Diagramas Estructurales

|                                      | Propósito                                          |
| ------------------------------------ | -------------------------------------------------- |
| **Diagrama de Clases**               | Clases, atributos, métodos, relaciones             |
| **Diagrama de Objetos**              | Instancias específicas en tiempo de ejecución      |
| **Diagrama de Componentes**          | Componentes de software y dependencias             |
| **Diagrama de Estructura Compuesta** | Estructura interna de clases/componentes           |
| **Diagrama de Paquetes**             | Paquetes y sus dependencias                        |
| **Diagrama de Despliegue**           | Despliegue de hardware/software                    |
| **Diagrama de Perfil**               | Estereotipos y extensiones específicos del dominio |

## Diagramas Comportamentales 

|                                               | Propósito                                 |
| --------------------------------------------- | ----------------------------------------- |
| **Diagrama de Casos de Uso**                  | Actores e interacciones del sistema       |
| **Diagrama de Actividad**                     | Flujos de trabajo y procesos de negocio   |
| **Diagrama de Máquina de Estados**            | Estados de objetos y transiciones         |
| **Diagrama de Secuencia**                     | Interacciones ordenadas en el tiempo      |
| **Diagrama de Comunicación**                  | Interacciones de objetos con enlaces      |
| **Diagrama de Temporización**                 | Interacciones con restricciones de tiempo |
| **Diagrama de Visión General de Interacción** | Flujo de control entre interacciones      |

---

```mermaid
graph TD
    UML[Diagramas UML] --> ST[Estructurales<br/>(7 tipos)]
    UML --> BH[Comportamentales<br/>(7 tipos)]
    
    ST --> CL[Clases]
    ST --> OB[Objetos]
    ST --> CO[Componentes]
    ST --> CS[Estructura Compuesta]
    ST --> PK[Paquetes]
    ST --> DP[Despliegue]
    ST --> PR[Perfil]
    
    BH --> UC[Casos de Uso]
    BH --> AC[Actividad]
    BH --> SM[Máquina de Estados]
    BH --> SQ[Secuencia]
    BH --> CM[Comunicación]
    BH --> TM[Temporización]
    BH --> IO[Visión General de Interacción]
```

---


## _**2. Marco de Decisión**_
---
Al elegir un tipo de diagrama UML, pregúntate:

- **¿Estoy modelando la arquitectura del sistema?** → Usa Diagramas Estructurales
    
- **¿Estoy modelando el comportamiento del sistema?** → Usa Diagramas Comportamentales
    

---

## _**Diagramas Estructurales**_

### Definición

Los diagramas estructurales modelan **cómo está arquitecturado un sistema** - se enfocan en los aspectos estáticos del sistema.

### Características

- Muestran la **estructura** y **organización** de los componentes del sistema
- Definen relaciones entre diferentes partes
- Se enfocan en **qué existe** en el sistema

### Ejemplo Principal: Diagrama de Clases

- Diagrama estructural más popular
- Define:
    - Nombres de clases
    - Atributos (propiedades/campos)
    - Nombres de métodos
    - Relaciones entre clases

### Casos de Uso

- Planificación de arquitectura del sistema
- Visualización de estructura de código
- Relaciones entre componentes
- Modelado de esquemas de base de datos

---

## _**Diagramas Comportamentales**_

### Definición

Los diagramas comportamentales modelan **cómo se comporta un sistema** - se enfocan en los aspectos dinámicos e interacciones.

### Características

- Muestran **interacciones** y **procesos**
- Modelan **comunicación** entre componentes
- Se enfocan en **qué sucede** en el sistema

### Preguntas Clave que Responden

- _**¿Qué mensajes envía un sistema a otro?**_
- _**¿Qué permisos tiene el Usuario A vs el Usuario B?**_
- _**¿Cómo interactúan las diferentes partes del sistema?**_
- _**¿Cuál es el flujo de operaciones?**_

### Casos de Uso

- Modelado de flujos de proceso
- Escenarios de interacción del usuario
- Patrones de comunicación del sistema
- Modelado de permisos y control de acceso

---

## _**3. Aplicación Práctica**_

### Para Programación Orientada a Objetos

- **Estructurales**: Modela tus clases, jerarquías de herencia, relaciones de composición
- **Comportamentales**: Modela llamadas a métodos, interacciones de objetos, cambios de estado

### Flujo de Trabajo de Desarrollo

1. **Fase de Planificación**: Usa diagramas estructurales para diseñar la arquitectura del sistema
2. **Fase de Implementación**: Usa diagramas comportamentales para modelar interacciones y flujos de trabajo
3. **Fase de Documentación**: Combina ambos tipos para documentación comprehensiva del sistema

---

### Y, ¿Esto era todo?

##### No (xD) 

Más adelante, en 03_Diagramas, se amplía en detalle cada diagraam,  tipos, clasificaciones, etc.

Por ahora, después de una breve visión general de los tipos de diagramas existentes y su clasificación, procederemos a definir primero todos los elementos comunes entre cada tipo de diagrama en la sección 02- Commons.