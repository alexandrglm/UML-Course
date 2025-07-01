| Guía   | Título                                           |
| ------ | ------------------------------------------------ |
| 07-187 | La Importancia del Análisis y Diseño de Sistemas |
| 07-188 | Visión General de los Sistemas de Software       |

| Guía       | Título                                    |
| ---------- | ----------------------------------------- |
| **06-150** | **Visión General de UML**                 |
| 06-151     | Etapas de Desarrollo donde se Utiliza UML |

---

## 06-150: Visión General de UML

1. Qué es UML

2. Contexto Histórico y Creación

3. Beneficios para Desarrolladores
   
   1. Comunicación Agnóstica del Lenguaje
   2. Comunicación con Stakeholders No Técnicos
   3. Logro de Nivel de Abstracción

4. Propuesta de Valor Fundamental

---

## 1. Qué es UML

---

![UML LOGO](./01_03_IMG1.png)

**UML** significa **Lenguaje de Modelado Unificado** (Unified Modeling Language).

El término "Unificado" es crucial para entender el propósito y origen de UML, ya que **representa la estandarización de multitud de enfoques de modelado visual previamente fragmentados en el desarrollo de software**.

UML es un lenguaje visual estandarizado para modelar sistemas de software, proporcionando **una notación común que desarrolladores, arquitectos y stakeholders pueden usar para comunicar diseño y comportamiento del sistema** independientemente de su trasfondo técnico o lenguaje de programación preferido.

> Proporciona una forma común para todas las partes involucradas en el desarrollo de software, aquellas conscientes de aspectos técnicos del desarrollo (desarrolladores, diseñadores, ...) y aquellas sin conocimiento técnico/capacidades, como stakeholders, cliente final, etc.

---

## 2. Contexto Histórico y Creación

---

### El Problema Antes de UML

Antes de la creación de UML, el modelado de software se caracterizaba por:

- **Enfoques Fragmentados**: Múltiples métodos de modelado visual incompatibles

- **Barreras de Comunicación**: Los desarrolladores usaban estilos de diagramas personales que otros no podían entender

- **Dificultades de Conversión a Código**: Los modelos visuales no podían convertirse fácilmente en código accionable

- **Ineficiencia de la Industria**: Falta de métodos estandarizados de comunicación visual

### Cronología de Creación de UML

- **1994**: Tres ingenieros de software*, que venían de diferentes sectores industriales/empresas y se habían afincado en **RationalSoftware Corp.**, comenzaron a desarrollar un enfoque unificado para el modelado de sistemas.

- **1996**: El Lenguaje de Modelado Unificado fue oficialmente lanzado como una especificación propietaria.

- **1997**: El O.M.G. (Object Management Group) tomó el liderazgo de UML adoptándolo y estableciéndolo como un estándar accesible para cualquiera.

### Los Tres Fundadores*

- **Grady Booch**
- **Ivar Jacobson**    
- **James Rumbaugh**

### Evolución y Estabilidad

UML ha experimentado actualizaciones continuas desde 1996 (se encuentra en la versión 2.5 actualmente), similar a los lenguajes de programación, mientras mantiene su base conceptual central.

Los principios fundamentales establecidos en 1996 siguen siendo relevantes y ampliamente utilizados hoy en día.

---

## 3. Beneficios de UML

---

### 1. UML como Herramienta de Análisis/Resolución de Problemas

UML no sirve sólo como una herramienta de documentación—**además, es un poderoso instrumento de análisis y resolución de problemas** que transforma cómo abordamos el desarrollo de software.

Muchos desarrolladores se sienten intimidados cuando enfrentan la construcción de nuevas aplicaciones o agregar características complejas a sistemas existentes.

> **A través del uso de UML, se proporciona un enfoque estructurado para descomponer estos desafíos en componentes más pequeños, manejables y visuales.**

---

### 1.2. Beneficios del Modelado de Sistemas / Beneficios de UML

### **Planificación Visual**

- Modelar sistemas antes de comenzar a escribir código.

### **Reducción de Riesgos**

- Identificar problemas potenciales en etapas iniciales.
- Minimizar errores de arquitectura.

### **Comunicación**

- Conectar a todas las partes involucradas, partes técnicas y no técnicas.
- Mejorar la comunicación.

### **Organización**

- Estructurar sistemas complejos lógicamente.
- Mantener calidad del código a través de organización visual.

### **Eficiencia**

- Reducir tiempo de desarrollo a través de mejor planificación.

---

### A) Comunicación Agnóstica del Lenguaje

#### **Escenario Típico**

Un desarrollador de Ruby necesita explicar arquitectura del sistema a desarrolladores de Java o JavaScript que no entienden la sintaxis de Ruby.


#### **Solución con UML**

Los modelos visuales trascienden las barreras de lenguajes de programación enfocándose en:

- Patrones de interacción del sistema
- Estructuras de organización de datos
- Diseño de base de datos
- Mensajería entre clases y comportamiento
- Arquitectura general del sistema


> **Los desarrolladores pueden comunicar conceptos complejos del sistema sin estar restringidos por sintaxis específicas del lenguaje o detalles de implementación.**

---

### B) Comunicación con Stakeholders No Técnicos

#### **Desafío**

Los no desarrolladores no pueden entender código pero necesitan verificar que el comportamiento del sistema coincida con requerimientos y expectativas del proyecto.

#### **Aplicación UML**

- ##### **Modelado de Comportamiento del Usuario**
	  Representación visual de cómo los usuarios interactúan con el sistema.

- ##### **Visualización de Procesos del Sistema**
	   Diagramas claros mostrando qué hace el sistema.

- ##### **Validación de Requerimientos**
	   Los stakeholders pueden verificar que el comportamiento modelado se alinee con sus expectativas.

- ##### **Comunicación entre todos los componentes del Proyecto**
	   Conecta la brecha entre implementación técnica y requerimientos de proyecto del cliente.

> **UML aporta Valor al Proyecto, ya que permite colaboración efectiva entre equipos técnicos y no técnicos, reduciendo malentendidos y asegurando alineación perfecta entre los requisitos del proyecto y las acciones de todas las partes involucradas.**

---

### C) Logro de Nivel de Abstracción

#### **Concepto de Abstracción**

UML proporciona un nivel de abstracción que aminora detalles muy concretos y específicos de implementación, enfocándose más en comportamientos y estructura del sistema, en un vistazo de alto nivel.

#### 🙅 **Lo que UML trata de impedir**

- ❌ Sintaxis de código específica e implementación
- ❌ Detalles específicos del lenguaje
- ❌ Complejidades técnicas de bajo nivel
- ❌ Consideraciones específicas de plataforma

#### 🤙 **Lo que UML Enfatiza**

- 🗿 Patrones de comportamiento del sistema
- 🗿 Relaciones estructurales
- 🗿 Flujo y organización de datos
- 🗿 Interacción y Relaciones entre componentes
- 🗿 Flujos de trabajo de procesos

> **Beneficio para Todos** 
> 
> UML permite un **enfoque en diseño de sistema y arquitectura sin dejar de lado del todo cuestiones de implementación**, **facilitando mejores decisiones de planificación y diseño**.

---

## 4. Propuesta de Valor Fundamental

---

UML sirve como un **lenguaje visual universal** para desarrollo de software que:

- #### **Estandariza  la Comunicación**
	   Proporciona una notación consistente entendida por toda la industria.

- #### **Conecta Vacíos Técnicos**
	   Permite comunicación entre desarrolladores usando diferentes lenguajes de programación.

- #### **Facilita la Colaboración de Inversores** 
	  Permite que miembros del equipo técnicos y no técnicos participen en discusiones de diseño del sistema

- #### **Mejora el Proceso de Diseño** 
	  Permite un  pensamiento de sistema de alto nivel antes de sumergirse en detalles de implementación

- #### **Mejora el proceso de Documentación** 
	  Crea documentación visual que permanece relevante independientemente de cambios en el código

- #### **Herramienta de Análisis/Planificación**
	   Sirve como un mecanismo de planificación efectivo para arquitectura y diseño de sistemas

> El valor principal de UML radica en su **capacidad de abstraer la complejidad de implementación mientras preserva información esencial de diseño del sistema**, haciéndolo una herramienta de alto nivel tanto para desarrolladores individuales como para equipos colaborativos que trabajan en el diseño, desarrollo y análisis de sistemas de software complejos.

---