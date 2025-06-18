#### 3.4 Despliegue

| Guía   | Título                                                                          |
| ------ | ------------------------------------------------------------------------------- |
| 07-175 | Diagramas de Despliegue                                                         |
| **07-176** | **Ejemplo: Construir un Diagrama de Motor de Despliegue de Solicitud de Canciones** |

---
# 07-176: Diagramas de Despliegue - Ejemplo


1. Caso de Uso Real: Servicio de Solicitud de Música   

	* Visión General de la Arquitectura del Sistema
	* Análisis del Nodo Frontend
	* Nodo del Sistema de Autenticación
	* Nodo de la API Backend
	* Análisis de Dependencias

2. Entendiendo las Dependencias en Sistemas de Software

	* Dependencias Unidireccionales vs Bidireccionales
	* Principios de Independencia del Sistema
	* Patrones Comunes en Aplicaciones Modernas

3. Mejores Prácticas - Consejos

4. Aplicaciones Prácticas

---



## ***1.    Caso Real:    Servicio de Solicitud de Canciones***
---

![large](./07-176_IMG1.png)

Analicemos un servicio práctico de solicitud de música que permite a los usuarios iniciar sesión y crear listas de reproducción.  

Este sistema demuestra la arquitectura típica de aplicaciones web modernas.

---
### Visión General de la Arquitectura del Sistema

El sistema consta de tres nodos principales:

1. **Nodo de Servicio Web** (Frontend)
2. **Nodo del Sistema de Autenticación**
3. **Nodo de la API Rails** (Backend)

![large](07-176_IMG02.png)

Cada nodo se ejecuta en sistemas operativos Linux y sirve propósitos específicos en la arquitectura general de la aplicación.

---
### Análisis del Nodo Frontend

#### **Configuración del Nodo**

- **Artefacto**: Dispositivo de Servicio Web
- **Sistema Operativo**: Linux
- **Componente**: Aplicación Angular

![large](./07-176_IMG03.png)

#### **Dependencias**

- API Rails (para gestión de datos y lógica de negocio)
- Sistema de Autenticación (para inicio de sesión de usuario y gestión de sesiones)

El frontend Angular no puede funcionar sin estas dependencias porque:

- Sin la API, no tendría datos que mostrar
- Sin autenticación, los usuarios no podrían acceder a características protegidas

----
### Nodo del Sistema de Autenticación

#### **Configuración del Nodo**

- **Artefacto**: Servicio de Autenticación
- **Sistema Operativo**: Linux
- **Protocolo**: JWT (JSON Web Tokens)

![large](./07-176_IMG04.png)
#### **Dependencias**: Ninguna

Este sistema es intencionalmente independiente porque:

- Solo recibe solicitudes y proporciona respuestas
- La tecnología frontend puede cambiarse (Angular a React) sin afectar la autenticación
- Su único propósito es validar credenciales y gestionar sesiones

---
### Nodo de la API Backend

#### **Configuración del Nodo**

- **Artefacto**: Servicio de la API Rails
- **Sistema Operativo**: Linux
- **Protocolos**: JSON, API RESTful

![large](./07-176_IMG05.png)
#### **Dependencias**

- Sistema de Autenticación (para validación de solicitudes)

La API depende de la autenticación porque debe verificar que las solicitudes entrantes provengan de usuarios autenticados antes de procesarlas.

---



## ***2.     Entendiendo las Dependencias en Sistemas de Software***
---

![medium](./07-176_IMG06.png)
### Dependencias Unidireccionales vs Bidireccionales

La mayoría de sistemas bien diseñados tienen **dependencias unidireccionales** que fluyen en una dirección:

- Frontend depende del Backend
- Backend depende de la Autenticación
- Autenticación no depende de nada (en este ejemplo)

Esto crea una **jerarquía clara** y **previene dependencias circulares** que pueden complicar el mantenimiento y las actualizaciones del sistema.

---
### Principios de Independencia del Sistema

#### **Independencia del Sistema de Autenticación**

El sistema de autenticación demuestra independencia perfecta:

- No le importa la tecnología frontend empleada
- No necesita conocer sobre la lógica de negocio
- Sirve un propósito único y bien definido


#### **Independencia Parcial del Sistema API**

La API Rails es independiente del frontend pero depende de la autenticación:

- La tecnología frontend puede cambiar sin modificaciones en la API
- La dependencia de autenticación es necesaria para la validación de seguridad

---

### Patrones Comunes en Aplicaciones Modernas

El ejemplo demuestra una típica **arquitectura de tres capas**:

1. **Capa de Presentación**: Frontend Angular
2. **Capa de Lógica de Negocio**: API Rails
3. **Capa de Seguridad**: Sistema de autenticación


Este patrón es prevalente porque:

- Separa las responsabilidades efectivamente
- Permite escalamiento independiente de componentes
- Habilita flexibilidad en la pila tecnológica
- Simplifica el mantenimiento y las actualizaciones

---


## ***3.    Buenas Prácticas 
---

### Principios de Diseño

- **Minimizar Dependencias**: Cada sistema debe depender del menor número posible de otros
- **Separación Clara**: Cada nodo debe tener una responsabilidad única y bien definida
- **Documentación de Protocolos**: Siempre especificar protocolos de comunicación entre nodos
- **Detalles del Entorno**: Incluir información del SO y tiempo de ejecución para claridad del despliegue

### Estándares para Documentación

- Usar notación consistente para componentes similares
- Incluir especificaciones de protocolo (JWT, REST, JSON)
- Agregar notas para patrones de comunicación complejos
- Especificar requisitos de despliegue para cada nodo


### Gestión de Dependencias

- **Evitar dependencias circulares** a toda costa
- Diseñar **sistemas** para que sean **lo más independientes posible**
- **Documentar por qué existe cada dependencia**
- Considerar **mecanismos de respaldo** para dependencias críticas

---


## ***4.     Aplicaciones Prácticas***
---

### Comunicación del Equipo de Desarrollo

Los diagramas de despliegue **sirven como planos para equipos de desarrollo**:

- Los desarrolladores backend entienden los límites del sistema
- Los desarrolladores frontend conocen los endpoints de la API y requisitos de autenticación
- Los equipos DevOps entienden las necesidades de despliegue e infraestructura


### Planificación del Sistema y Arquitectura

Antes de la implementación, los diagramas de despliegue ayudan a:

- Identificar posibles cuellos de botella
- Planificar requisitos de escalabilidad
- Entender límites de seguridad
- Estimar costos de infraestructura


### Toma de Decisiones Tecnológicas

La representación visual ayuda a evaluar:

- Compatibilidad entre las tecnologías implementadas
- Eficiencia del protocolo de comunicación
- Posibilidades y Requisitos para escalabilidad
- Complejidad del posible mantenimiento
