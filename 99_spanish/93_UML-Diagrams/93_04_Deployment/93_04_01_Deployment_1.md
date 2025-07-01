#### 3.4 Despliegue

| Guía       | Título                                                                          |
| ---------- | ------------------------------------------------------------------------------- |
| **07-175** | **Diagramas de Despliegue**                                                     |
| 07-176     | Ejemplo: Construir un Diagrama de Motor de Despliegue de Solicitud de Canciones |

---
# 07-175:  Elementos del Diagrama de Despliegue 

1. Introducción a los Diagramas de Despliegue

2. Visión General de Elementos Principales

	1. Nodos
	2. Componentes
	3. Artefactos
	4. Enlaces
	5. Dependencias
	6. Asociaciones

3. Principios de Diseño y Mejores Prácticas

---


## ***1. Introducción a los Diagramas de Despliegue***
---
Los diagramas de despliegue son **diagramas UML estructurales que modelan la arquitectura física de un sistema.** 

Se usan principalmente para **decisiones de arquitectura del sistema** y muestran cómo los componentes de software se distribuyen a través de la infraestructura de hardware.

#### **Propósito Principal**

- **Visualizar arquitectura del sistema y requisitos de infraestructura**
- **Definir estrategias de despliegue y necesidades de configuración**
- Mostrar relaciones entre componentes de hardware y **software**
- **Guiar configuración de infraestructura y procesos de despliegue**


#### **Cuándo Usar**

- Planificación de la arquitectura del sistema al inicio del proyecto
- Documentar infraestructura del sistema existente
- Comunicar requisitos de despliegue a equipos de operaciones
- Diseñar sistemas escalables y distribuidos

---

## ***2. Visión General de Elementos Principales***
---
Los diagramas de despliegue consisten en **SEIS** elementos fundamentales que trabajan juntos para representar la arquitectura del sistema:

![large](./07-175_IMG0.png)

- **Nodos**: Unidades físicas o lógicas de hardware/software
- **Componentes**: Aplicaciones de software o servicios ejecutándose en nodos
- **Artefactos**: Elementos de software desplegables con configuraciones específicas
- **Enlaces**: Conexiones básicas entre nodos
- **Dependencias**: Relaciones direccionales mostrando dependencias
- **Asociaciones**: Relaciones complejas en sistemas distribuidos

---


## ***1.      Nodos***
---

### **Definición** 

>  Los nodos representan **los bloques de construcción fundamentales** de los diagramas de despliegue - son **los componentes reales del mundo real donde se ejecuta el software**.


### **Representación Visual**

![large](./07-175_IMG1.png)

Cajas o cubos tridimensionales representando objetivos de despliegue físicos o lógicos


### **Tipos de Nodos**

- **Servidores Físicos**: Servidores web, servidores de base de datos, servidores de aplicación
- **Máquinas Virtuales**: Instancias de nube, contenedores
- **Bases de Datos**: Sistemas de gestión de base de datos
- **APIs**: Endpoints de servicio
- **Dispositivos de Red**: Balanceadores de carga, routers, firewalls


### **Principio Fundamental** 

> **Todo en un diagrama de despliegue es esencialmente un nodo**. 
> 
> El resto elementos, bien se añaden en detalles a los nodos o bien se muestran las relaciones entre ellos.


#### **Ejemplos**

- Servidor Web alojando un frontend React/Angular
- Servidor de Base de Datos ejecutando MongoDB, PostgreSQL
- Gateway API gestionando solicitudes de servicio
- Balanceador de Carga distribuyendo tráfico

---


## ***2.      Componentes***
---

### **Definición**

> **Aplicaciones de software, servicios o unidades lógicas que se ejecutan dentro de nodos** y manejan lógica de negocio y comunicación.



![large](07-175_IMG3.png)



### **Representación Visual**
![large](./07-175_IMG2.png)

Rectángulos redondeados contenidos dentro de nodos, a menudo con estereotipos de componentes


### **Tipos de Componentes**

- **Aplicaciones Web**: Aplicaciones front-end (Angular, React, Vue)
- **Servicios Web**: Servicios back-end y APIs
- **Sistemas de Base de Datos**: Software de gestión de base de datos
- **Middleware**: Colas de mensajes, sistemas de caché
- **Servicios de Lógica de Negocio**: Aplicaciones específicas del dominio


### **Sintaxis Alternativa**

Diferentes herramientas UML pueden representar componentes con estilos visuales variados:

- **Estilo Estándar**: Rectángulos redondeados con etiquetas de componentes
- **Estilo Enterprise Architect**: Cajas rectangulares con estereotipos de componentes
- **Estilo Simplificado**: Etiquetas de texto dentro de nodos



### **Filosofía de Diseño**

> **La representación visual específica es menos importante que comunicar claramente los componentes de software** y su organización. 

##### Elige el estilo que mejor sirva a tus partes interesadas y necesidades de documentación.

---


## ***3.      Artefactos***
---

### **Definición**

**Elementos de software específicos "desplegables"** que proporcionan información detallada de configuración y despliegue.


#### **Representación Visual**

Similar a estereotipos, son texto rodeado por corchetes angulares tipo guillemets (ej., `<<device>>`, `<<angular web service>>`)

![large](./07-175_IMG4.png)



### **Propósito**

Los artefactos indican a los arquitectos y equipos de desarrollo exactamente **qué necesita ser instalado, configurado y desplegado** en cada nodo.



### **Tipos de Información de Artefactos**

- **Requisitos del Stack de Software**: Especificaciones de framework y runtime
- **Detalles del Sistema Operativo**: Requisitos de tipo y versión del SO
- **Parámetros de Configuración**: Configuraciones específicas del entorno
- **Especificaciones de Interfaz**: Protocolos de comunicación y puertos


#### **Ejemplos**

- `<<device:webServer Interface {OS=Linux}>>`
- `<<angular web service>>`
- `<<Rails API {version=7.0, database=PostgreSQL}>>`



### **Ejemplo de Valor Práctico**

#### 1. Cuando un artefacto especifica "angular web service" ....
#### 2. .... los equipos de operaciones comprenden que deben instalar Node.js, NPM y dependencias de Angular. 

#### 1. Si especifica "Rails web service,".... 
#### 2. .... saben que deben preparar Ruby, Rails y las dependencias asociadas.



### **Convención de Nomenclatura Formal**

El formato estándar UML incluye **tipo de dispositivo, especificación de interfaz y parámetros de configuración en un formato estructurado** para instrucciones precisas de despliegue.

---


## ***4.      Enlaces***
---

### **Definición**

Conexiones básicas entre nodos mostrando que ocurre comunicación entre componentes del sistema.

### **Representación Visual**

Líneas simples conectando nodos sin información direccional

![large](07-175_IMG5.png)

### **Propósito**

- **Mostrar qué nodos pueden comunicarse entre sí**
- Indicar requisitos de conectividad de red
- Visualizar topología básica del sistema


### **Ejemplos de Conexiones**

- Front-end Angular enlazado al sistema de Autentificación
- Front-end enlazado a API Rails
- API enlazada al sistema de Autentificación


### **Caso de Uso**

> **Los enlaces proporcionan una vista de alto nivel de conectividad del sistema sin especificar la naturaleza o dirección de dependencias.**

---


## ***5.      Dependencias***
---

### **Definición**

Relaciones direccionales que especifican qué nodos dependen de otros para funcionalidad.


### **Representación Visual**

Líneas punteadas con flechas apuntando hacia los nodos de los cuales se depende

![large](07-175_IMG6.png)


### **Propósito**

- **Mostrar relaciones de dependencia explícitas**
- Indicar requisitos de **orden de despliegue**
- **Aclarar** dependencias de servicio para resolución de problemas
- **Guiar secuencias de inicio y apagado del sistema**


### **Beneficios del Análisis de Dependencias**

- **Evaluación Rápida**: De un vistazo, entender qué componentes dependen de otros
- **Planificación de Despliegue**: Las dependencias indican qué servicios deben iniciarse primero
- **Análisis de Impacto**: Entender qué componentes se ven afectados si falla una dependencia


### **Ejemplo de Patrón**

- Front-end Angular depende del sistema de Autentificación (flecha apunta a Auth)
- Front-end Angular depende de API Rails (flecha apunta a API)
- API Rails depende del sistema de Autentificación (flecha apunta a Auth)

---


## ***6.      Asociaciones***
---

### **Definición**

Relaciones complejas en sistemas distribuidos que muestran cómo múltiples nodos trabajan juntos en arquitecturas sofisticadas.


### **Representación Visual**

Líneas conectando múltiples nodos, a menudo en patrones hub-and-spoke o de red

![large](07-175_IMG7.png)


### **Casos de Uso**

- **Arquitecturas de Balanceador de Carga**: Mostrar cómo los balanceadores de carga distribuyen solicitudes a múltiples servidores de aplicación
- **Comunicación de Microservicios**: Modelar patrones complejos de comunicación servicio-a-servicio
- **Clustering de Base de Datos**: Representar relaciones de replicación y clustering de base de datos
- **Redes CDN**: Mostrar distribución de contenido y relaciones de caché


###  **Ejemplo de Arquitectura**  

Un balanceador de carga recibiendo solicitudes de Internet y mapeándolas a varios servidores de aplicación, que luego se comunican con clusters de base de datos.


### **Perspectivas de Estrategia de Despliegue**

Los patrones de asociación proporcionan una "receta" para configuración de infraestructura, mostrando:

- Número de servidores de aplicación necesarios
- Requisitos de clustering de base de datos
- Necesidades de configuración del balanceador de carga
- Requisitos de topología de red

---


## ***3.      Principios de Diseño y Mejores Prácticas***
---

### Claridad Sobre Perfección

- Enfocarse en comunicación clara en lugar de notación UML perfecta
- Elegir estilos visuales que tengan sentido para tus partes interesadas
- Priorizar comprensión sobre adherencia estricta a símbolos


### Enfoque "Arquitectura-Primero"

- Usar diagramas de despliegue temprano en la planificación del proyecto
- Dejar que los requisitos de infraestructura impulsen las elecciones tecnológicas
- Considerar escalabilidad y mantenimiento desde el inicio

### Comunicación entre todas las partes involucradas

- Asegurar que los diagramas sirvan tanto a audiencias técnicas como de negocio
- Incluir suficientes detalles para  la implementación, pero sin abrumar
- Usar notación consistente a través de la documentación del proyecto

### Mentalidad de "Receta de Despliegue"

- Diseñar diagramas que sirvan como guías de despliegue
- Incluir detalles de configuración en artefactos
- Mostrar dependencias claramente para secuenciación apropiada de despliegue

### Flexibilidad de Herramientas

- Aceptar que diferentes herramientas UML pueden tener representaciones visuales variadas
- Enfocarse en precisión de contenido en lugar de consistencia visual entre herramientas
- Documentar cualquier elección de notación específica de herramienta para claridad del equipo
