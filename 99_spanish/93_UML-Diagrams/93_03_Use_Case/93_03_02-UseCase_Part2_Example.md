#### 3.3  Casos de Uso

| Guía       | Título                                                                                        |
| ---------- | --------------------------------------------------------------------------------------------- |
| 07-172     | Visión General de los Elementos del Diagrama de Casos de Uso UML                              |
| **07-173** | **Ejemplo: Construir un Diagrama de Casos de Uso del Sistema de Automatización de Marketing** |

---
# 07-173:  Diagrama de Casos de Uso con un ejemplo



1. Visión General del Sistema

2. Análisis de Actores

    - Especialista en Marketing
    - Potencial Cliente / Cliente (Lead)

3. Desglose de Casos de Uso
    - Funciones del Sistema Externo
    - Subsistema del Panel Web (Web Dashboard)

4. Patrones de Relaciones

5. Perspectivas de Implementación de Desarrollo

6. Implicaciones de la Arquitectura del Sistema

7. Demostración del Valor de UML

---

## ***1.      Visión General del Sistema***
---
El diagrama de casos de uso del Sistema de Automatización de Marketing demuestra una implementación completa de todos los elementos del diagrama de casos de uso trabajando juntos para modelar la aplicación de este ejemplo.

Está basado/derivado de lo que revisamos en la sección de Diagrama de Actividades, al menos en la parte de actores. ![small](./07-173_IMG2.png)

Este sistema gestiona todo el recorrido del cliente desde la generación de temas comerciales de interés, hasta la conversión de potencial cliente a cliente, proporcionando diferentes niveles de acceso para especialistas en marketing y clientes.

#### **Propósito Principal del Sistema**

- Rastrear recorridos de clientes desde generación de temas comerciales de interés  hasta la venta
- Automatizar procesos de marketing y notificaciones
- Proporcionar capacidades de reportes y gestión de contactos
- Habilitar creación dinámica de formularios e interacción con clientes

![large](07-173_IMG1.png)

---


## ***2.      Análisis de Actores***
---
## A)   Especialista en Marketing

#### **Definición del Rol**
Usuario administrativo con acceso integral al sistema, funcionando como el operador principal del sistema.

#### **Casos de Uso Disponibles**

- **Gestionar Recorridos y Formas**: Crear y modificar flujos de trabajo de recorridos de clientes

- **Obtener Notificaciones Sobre Recorridos**: Recibir alertas sobre eventos de recorridos de clientes

- **Obtener Reportes**: Acceder a analíticas y datos de rendimiento

- **Gestionar Contactos**: Manejar información de clientes y prospectos

- **Generar Formularios**: Crear formularios dinámicos para interacción con clientes

- **Obtener Mensajes**: Acceder a registros de comunicación y mensajes de clientes

- **Visitar Recursos**: Ver recursos del sistema y documentación

### **Patrón de Acceso** 

El especialista en marketing tiene el acceso más amplio al sistema, incluyendo tanto funciones externas como capacidades completas del panel web.

---

## B)   Potencial Cliente / Cliente

####  **Definición del Rol**

Usuarios externos que interactúan con el sistema de marketing, representando clientes potenciales o existentes.

#### **Casos de Uso Disponibles**

- **Disparar Eventos de Recorrido**: Iniciar flujos de trabajo de marketing (ej. registrarse a través de formularios del sitio web)

- **Obtener Mensajes**: Recibir comunicaciones del sistema de marketing

- **Visitar Recursos**: Acceder a materiales y contenido proporcionado

- **Llenar Formularios**: Completar formularios dinámicos creados por especialistas en marketing

#### **Patrón de Acceso**

Los clientes tienen acceso limitado, enfocado en la interacción, diseñado para capturar compromiso y moverlos a través de embudos de marketing.

---


## ***3.      Desglose de Casos de Uso***
---

### a)     Funciones del Sistema Externo

Funciones que operan fuera del subsistema del panel web:

##### **1)     Gestionar Recorridos y Formas**

- **Propósito**: Configurar flujos de trabajo de recorridos de clientes y árboles de decisión
- **Implicación de Implementación**: Requiere motor de flujo de trabajo y constructor visual de recorridos
- **¿Quién puede acceder?**: Solo Especialista en Marketing

##### **2)     Obtener Notificaciones Sobre Recorridos**

- **Propósito**: Alertar a especialistas en marketing sobre eventos de recorridos de clientes
- **Implicación de Implementación**: Sistema de notificaciones por correo electrónico requerido
- **¿Quién puede acceder?**: Solo Especialista en Marketing
- **Relación Especial**: Conectado a "Disparar Eventos de Recorrido" mediante relación "notificar"

##### **3)      Disparar Eventos de Recorrido**

- **Propósito**: Acciones de clientes que inician o avanzan flujos de trabajo de marketing
- **Implicación de Implementación**: Sistema de seguimiento de eventos y disparador de flujo de trabajo
- **¿Quién puede acceder?**: Solo Potencial Cliente / Cliente
- **Conexión**: Se vincula al sistema de notificaciones para especialistas en marketing

---

### b)     Subsistema del Panel Web

El panel web contiene cinco casos de uso integrados que representan la interfaz administrativa principal:

##### **4)     Obtener Reportes**

- **Propósito**: Analíticas y monitoreo de rendimiento
- **Requisito de Implementación**: Interfaz de reportes con visualización de datos

##### **5)     Gestionar Contactos**

- **Propósito**: Gestión de información de clientes y prospectos
- **Requisito de Implementación**: Base de datos de contactos e interfaz de gestión

##### **6)      Generar Formularios**

- **Propósito**: Creación dinámica de formularios para compromiso de clientes
- **Requisito de Implementación**: Componentes de constructor de formularios y sistema de renderizado

##### **7)       Obtener Mensajes**

- **Propósito**: Acceso y gestión de registros de comunicación
- **Requisito de Implementación**: Sistema de almacenamiento y recuperación de mensajes

##### **8)      Visitar Recursos**

- **Propósito**: Acceso a documentación del sistema y materiales
- **Requisito de Implementación**: Biblioteca de recursos y control de acceso

---


## ***4.      Patrones de Relaciones***
---
### **Relaciones Directas Actor-Caso de Uso**


#### - **Conexiones del Especialista en Marketing**
![small](./07-173_IMG04.png)
- Acceso directo a todas las funciones externas
- Acceso completo al subsistema del panel web
- Privilegios integrales del sistema


#### **- Conexiones del Potencial Cliente/Cliente Converso
![small](./07-173_IMG05.png)
- Limitado a interacciones orientadas al cliente
- Sin acceso administrativo
- Enfocado en compromiso y recolección de datos

---

### **Relaciones Inter-Casos de Uso**

#### **- Relación "Notificar"**
![small](./07-173_IMG06.png)
- **Origen**: Disparar Eventos de Recorrido
- **Destino**: Obtener Notificaciones Sobre Recorridos
- **Propósito**: Flujo de notificación automática cuando los clientes toman acciones
- **Implementación**: Sistema de notificaciones dirigido por eventos

---


## ***5.      Perspectivas de Implementación de Desarrollo***
---
### **Requisitos de Arquitectura del Sistema**
---
##### **Sistema de Notificaciones por Correo Electrónico** 

La ubicación de "Obtener Notificaciones Sobre Recorridos" fuera del panel web indica un servicio de notificaciones por correo electrónico separado que alerta a los especialistas en marketing sobre acciones de clientes.

---
##### **Componentes del Sistema de Formularios** 

El caso de uso "Generar Formularios" implica un sistema de doble componente:

- **Componente Administrativo**: Interfaz de constructor de formularios para especialistas en marketing
- **Componente de Cliente**: Sistema de renderizado y envío de formularios para clientes
- **Flujo de Datos**: Los envíos de formularios alimentan el sistema de reportes

---
##### **Estructura del Panel Web** 

Cinco áreas funcionales distintas que requieren:

- Interfaz de reportes con analíticas
- Sistema de gestión de contactos
- Capacidades de manejo de mensajes
- Biblioteca de recursos
- Herramientas de generación de formularios

---
### **Requisitos del Motor de Autorización**

##### **Control de Acceso Basado en Roles**

- **Especialista en Marketing**: Acceso completo al sistema incluyendo funciones administrativas
- **Potencial Cliente / Cliente**: Limitado a funciones de interacción y compromiso
- **Límites Claros**: El panel web requiere autenticación y verificación de roles

---


## ***6.      Implicaciones de la Arquitectura del Sistema***
---

### Distribución de Componentes

#### **Servicios Externos**

- Motor de gestión de recorridos
- Servicio de notificaciones
- Sistema de seguimiento de eventos

#### **Módulo del Panel Web**

- Interfaz administrativa integrada
- Subsistema de reportes
- Gestión de contactos
- Constructor de formularios
- Gestión de recursos

---
### Patrones de Flujo de Datos

#### **Flujo de Recorrido del Cliente**

1. Cliente dispara evento de recorrido (registro, envío de formulario)
2. Sistema procesa evento y actualiza estado del recorrido
3. Especialista en marketing recibe notificación
4. Reportes actualizados con nuevos datos de compromiso

#### **Flujo de Interacción de Formularios**

1. Especialista en marketing genera formulario en panel web
2. Cliente accede y llena formulario
3. Datos del formulario alimentan sistemas de gestión de contactos y reportes

---


## 7.      Valor de UML
---
## 1. Eficiencia del Modelado Visual

### **Densidad de Información**

Este diagrama compacto transmite información de arquitectura del sistema que requeriría documentación escrita extensa para comunicarse efectivamente.


### **Marco de Autorización Claro**

**La representación visual muestra inmediatamente:**

- **Quién puede acceder a qué funcionalidad**
- **Qué componentes pertenecen a qué módulos del sistema**
- **Cómo diferentes tipos de usuarios interactúan con el sistema**

---
## 2. Beneficios de Planificación de Desarrollo

### **Identificación de Componentes**

Los desarrolladores pueden identificar inmediatamente los componentes del sistema requeridos:

- Interfaz del panel web
- Servicio de notificaciones por correo electrónico
- Sistemas de generación y renderizado de formularios
- Motor de gestión de recorridos
- Infraestructura de reportes

### **Comprensión del Alcance de Características**

Ocho casos de uso revelan requisitos de funcionalidad significativos incluyendo:

- Creación dinámica de formularios
- Seguimiento de recorridos de clientes
- Notificaciones automatizadas
- Reportes integrales
- Gestión de contactos

---
## 3. Demostración del Poder de UML

#### **Herramientas Simples, Sistemas Complejos**

Usando solo cuatro elementos UML (actores, casos de uso, subsistemas, relaciones), el diagrama modela una plataforma completa de automatización de marketing.

#### **Longevidad y Efectividad** 

La relevancia duradera de UML se demuestra por cómo estas herramientas visuales simples pueden capturar requisitos de sistemas complejos de manera clara y eficiente.

#### **Puente de Comunicación** 

El diagrama sirve a múltiples audiencias:

- **Desarrolladores**: Requisitos de implementación claros
- **Partes Interesadas del Negocio**: Comprensión de capacidades del sistema
- **Arquitectos de Sistema**: Organización de alto nivel del sistema
