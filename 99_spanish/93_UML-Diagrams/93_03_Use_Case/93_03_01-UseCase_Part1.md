#### 3.3  Casos de Uso

| Guía       | Título                                                                   |
| ---------- | ------------------------------------------------------------------------ |
| **07-172** | **Visión General de Elementos del Diagrama de Casos de Uso UML**        |
| 07-173     | Inmersión Profunda: Construir un Diagrama de Casos de Uso de Sistema de Automatización de Marketing |

---
# 07-172:    Diagramas de Casos de Uso (1)


1. Qué son los Diagramas de Casos de Uso UML
2. Visión General de Elementos Principales
3. Casos de Uso
4. Actores
5. Subsistemas (Límites del Sistema)
6. Relaciones
7. Principios Clave de Diseño

---

## ***1.      Qué son los Diagramas de Casos de Uso UML***

Los Diagramas de Casos de Uso son **diagramas UML comportamentales diseñados para modelar la funcionalidad del sistema desde la perspectiva del usuario (actores)**. 

Su propósito principal es establecer **reglas de autorización** e **ilustrar qué características pueden acceder diferentes tipos de usuarios o clientes dentro de un sistema**.

#### **Objetivos Principales**

- Definir **permisos de acceso y límites de autorización**
- Visualizar funcionalidad del sistema disponible para diferentes tipos de usuarios
- Proporcionar a los desarrolladores requisitos claros para construir motores de autorización
- Documentar accesibilidad de características a través de diferentes roles de usuario

---


## ***2.      Elementos Principales***
---
Los Diagramas de Casos de Uso consisten en **CUATRO elementos fundamentales** que trabajan juntos para representar acceso y funcionalidad del sistema:

1.  **Casos de Uso**: Acciones específicas o funcionalidades disponibles en el sistema

2. **Actores**: Usuarios, sistemas o clientes que interactúan con el sistema

3. **Subsistemas**: Límites organizacionales que agrupan casos de uso relacionados

4. **Relaciones**: Conexiones entre actores y casos de uso


---


## 3. Casos de Uso
---
#### **Representación Visual**

![medium](./07-171_IMG1.png)
Óvalos o formas elípticas conteniendo descripciones de acciones

#### **Características**

- Representan acciones específicas o funcionalidades dentro del sistema
- Deben estar **orientados a acciones** usando formato verbo-sustantivo
- Se enfocan en qué pueden hacer los usuarios, no en cómo el sistema lo implementa
- Abstraen detalles de implementación y atributos de datos

#### **Ejemplos de Casos de Uso**

>- "Obtener Reportes"
>- "Obtener Mensajes"
>- "Gestionar Contactos"
>- "Visitar Recursos"


#### **Principio de Diseño**

Los casos de uso deben comunicar claramente las características disponibles a los desarrolladores, permitiéndoles entender los requisitos de autorización sin atascarse en detalles técnicos de implementación.


#### 🙅 **Lo que los Casos de Uso NO Incluyen**

- Atributos de datos o detalles de esquema de base de datos
- Métodos específicos o implementaciones de funciones
- Especificaciones técnicas de implementación
- Procesos internos del sistema invisibles para los usuarios

---


## ***4.     Actores***
---
#### **Representación Visual** 
Figuras de palitos o símbolos de actores posicionados fuera del límite del sistema

![medium](./07-171_IMG2.png)

#### **Definición** 

Cualquier entidad que interactúa con el sistema desde afuera, incluyendo tanto usuarios humanos como sistemas no humanos.
##### Actores Humanos

- **Admin**: Administradores del sistema con privilegios elevados
- **Cliente**: Usuarios finales o clientes usando el sistema
- **Gerente**: Usuarios con permisos específicos basados en roles
##### Actores No Humanos

- **Clientes API**: Aplicaciones externas que consumen APIs del sistema
- **Aplicaciones Móviles**: Apps iOS/Android accediendo servicios backend
- **Sistemas de Terceros**: Sitios web externos o servicios que se integran con el sistema
- **Servicios Automatizados**: Procesos programados o sistemas de monitoreo


#### **Consideración Importante** 

En arquitecturas impulsadas por API, puede que nunca tengas usuarios humanos directos. En su lugar, varios clientes de software (apps móviles, aplicaciones web, otras APIs) actúan como los actores principales accediendo funcionalidad del sistema.


#### **Ejemplo de Escenario** 

> Una API que proporciona posts de blog o datos de usuario a aplicaciones móviles, donde la app móvil misma es el actor, no los usuarios individuales de esa app móvil.

---


## ***5.      Subsistemas (Límites del Sistema)***
---
#### **Representación Visual** 
Cajas rectangulares grandes que contienen casos de uso relacionados y otros elementos
![medium](./07-171_IMG3.png)

#### **Propósito**
Organizar y agrupar funcionalidad relacionada dentro de límites lógicos del sistema


#### **Características**

- Ayudan a organizar sistemas complejos en secciones manejables
- Delinean claramente qué funcionalidad pertenece a qué parte del sistema
- Proporcionan separación visual entre diferentes componentes o módulos del sistema


#### **Ejemplo de Estructura**

```
Panel Web (Subsistema)
|
├── Obtener Reportes
├── Obtener Mensajes  
├── Gestionar Contactos
├── Visitar Recursos
└── Formularios

Externo al Panel Web:
|
├── Gestionar Recorridos y Formas
├── Disparar Eventos de Recorrido
└── Obtener Notificaciones Acerca de Recorridos
```


#### 🗿 **Beneficios Organizacionales**

- **Definición Clara de Alcance**: Muestra exactamente qué características pertenecen a cada componente del sistema
- **Planificación de Desarrollo**: Ayuda a los equipos a entender qué características implementar en qué módulos
- **Visualización de Arquitectura del Sistema**: Proporciona vista de alto nivel de la organización del sistema

---


## ***6.     Relaciones***
---
#### **Representación Visual**

Líneas conectando actores a casos de uso, típicamente con flechas indicando dirección de interacción

![medium](./07-171_IMG4.png)

## **Tipos de Líneas de Relación:

- ##### **Líneas Sólidas**: 
  Asociaciones directas entre actores y casos de uso

- ##### **Líneas Punteadas con Flechas Abiertas** 
  Muestran relaciones y conexiones entre diferentes casos de uso


#### **Propósito**

##### Establecer conexiones claras entre quién puede acceder qué funcionalidad en el sistema



#### **Funciones de Relaciones**

- Conectar actores directamente a los casos de uso que pueden acceder
- Mostrar con qué elementos del sistema puede interactuar cada tipo de actor
- Visualizar patrones de permisos y acceso
- Documentar reglas de autorización en formato visual


#### **Mapeo de Autorización**

Las relaciones sirven como la representación visual de una matriz de autorización, mostrando a los desarrolladores exactamente qué actores deben tener acceso a qué características del sistema.

---


## ***7.      Principios de Diseño***
---
### Enfoque Orientado a Acciones

Los casos de uso deben enfatizar **qué** pueden hacer los usuarios en lugar de **cómo** el sistema logra esas tareas. Esto mantiene los diagramas enfocados en funcionalidad en lugar de implementación.

### Diseño Centrado en Autorización

El objetivo principal es crear un marco de autorización claro que los desarrolladores puedan usar para implementar controles de acceso apropiados y sistemas de permisos.

### Nivel de Abstracción

Los diagramas de casos de uso operan a un alto nivel de abstracción, enfocándose en funcionalidad visible al usuario mientras ocultan la complejidad interna del sistema.

### Reconocimiento de Diversidad de Actores

Los sistemas modernos a menudo tienen tipos diversos de actores, incluyendo sistemas automatizados, APIs y varias aplicaciones cliente, no solo usuarios humanos.

### Claridad Organizacional

Los subsistemas ayudan a gestionar complejidad en sistemas grandes proporcionando agrupaciones lógicas de funcionalidad relacionada, haciendo el sistema general más fácil de entender e implementar.
