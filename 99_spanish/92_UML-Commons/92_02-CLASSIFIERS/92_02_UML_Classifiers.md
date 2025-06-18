| Guía       | Título                                                       |
| ---------- | ------------------------------------------------------------ |
| 06-152     | Introducción a los Componentes UML y Elementos Comunes       |
| 06-153     | Componentes Comunes de UML: Marcos (Frames)                  |
| **06-154** | **Componentes Comunes de UML: Clasificadores (Classifiers)** |
| 06-155     | Componentes Comunes de UML: Estereotipos (Stereotypes)       |
| 06-156     | Componentes Comunes de UML: Comentarios y Notas              |
| 06-157     | Componentes Comunes de UML: Dependencias                     |
| 06-158     | Componentes Comunes de UML: Características y Propiedades    |
| 06-159     | Cuestionario: Introducción a UML                             |

---

# 06-154: CLASIFICADORES

1. Qué son los Clasificadores
2. Naturaleza Abstracta de los Clasificadores
3. Aplicación Universal a Través de Diagramas
4. Características y Funciones Clave
5. Ejemplos de Uso Común
6. Clasificadores vs Clases - Distinción Clave
7. Pautas de Implementación

---

## _**1. Qué son los Clasificadores**_
---
Los clasificadores son componentes fundamentales de UML que sirven como **mecanismos de identificación para varios elementos dentro de los diagramas UML**.

> Nos referimos a una clase, un objeto, un componente, o un nodo de despliegue como clasificadores en UML ya que definen un conjunto común de propiedades.
> 
> Somos capaces de diseñar diagramas de objetos instanciando clasificadores.

Proporcionan **una convención de nomenclatura estandarizada** que **permite comunicación clara** entre diseñadores, desarrolladores y stakeholders a lo largo del ciclo de vida del desarrollo de software.

El propósito principal de los clasificadores es exactamente lo que su nombre implica - **clasifican elementos**.

Este **sistema de categorización de alto nivel**:

- #### **Asegura consistencia y claridad** a través de toda la documentación UML
    
- #### **Sirve** como base **para entender la estructura y relaciones dentro de un sistema**.
    

---


## 2. Naturaleza Abstracta de los Clasificadores
---
Uno de los conceptos más importantes de entender sobre los clasificadores es su **naturaleza abstracta**.

Esto significa:

- **No implementarás un clasificador directamente** en código
- Los clasificadores son más bien una **categoría o plantilla** para componentes
- Sirven como un **marco conceptual** en lugar de implementaciones concretas
- Esta característica abstracta a menudo confunde a los nuevos en UML

---


## 3. Aplicación Universal a Través de Diagramas
---
Los clasificadores se utilizan en virtualmente todo tipo de diagrama UML, haciéndolos uno de los elementos más omnipresentes en el modelado UML.

Aparecen en:

- **Diagramas de Clases** - Nombrando clases y sus relaciones
- **Diagramas de Casos de Uso** - Identificando actores y casos de uso
- **Diagramas de Secuencia** - Etiquetando objetos y líneas de vida
- **Diagramas de Actividad** - Nombrando actividades y puntos de decisión
- **Diagramas de Componentes** - Identificando componentes del sistema
- **Diagramas de Despliegue** - Nombrando nodos de hardware y software
- **Diagramas de Máquina de Estados** - Etiquetando estados y transiciones
- **Diagramas de Comunicación** - Identificando objetos participantes

---

## 4. Características y Funciones Clave
---

### _**Estandarización**_

Los clasificadores proporcionan un **enfoque de nomenclatura unificado** a través de todos los elementos UML, asegurando una  documentación y comunicación consistentes.

### _Identificación_

Sirven como **identificadores únicos** para diferentes componentes, haciendo más fácil referenciar y discutir elementos específicos durante el desarrollo.

### _Comunicación_

Los clasificadores actúan como un **lenguaje común** entre miembros del equipo, facilitando mejor entendimiento y colaboración.

### _Documentación_

Proporcionan **etiquetado claro** que hace los diagramas UML autodocumentados y más fáciles de mantener con el tiempo.

---

## 5. Ejemplos de Uso Común
---

### _Diagramas de Clases_

En un diagrama de clases, el clasificador aparece como el **nombre de la clase** en la parte superior de cada caja de clase.

![large](./06-154_IMG3.png)

Por ejemplo, si tienes una clase representando un sistema de blog, "Topic" sería el clasificador para esa clase particular.

---

### _Diagramas de Casos de Uso_

Al crear diagramas de casos de uso, los clasificadores identifican:

- **Nombres de actores** (ej., "Usuario", "Administrador")
- **Nombres de casos de uso** (ej., "Iniciar Sesión", "Crear Publicación", "Gestionar Contenido")

---

### _Diagramas de Objetos_

Los clasificadores en diagramas de objetos representan el **tipo o clase** al cual pertenece cada instancia de objeto.

---


## 6. Clasificadores vs Clases
---
Una fuente común de confusión es la relación entre **clasificadores** y **clases**:

### Clasificador

- Un **mecanismo de nomenclatura** usado a través de todos los diagramas UML
- Un **concepto abstracto** para identificación
- **No específico** solo a diagramas de clases
- Usado para **propósitos de categorización**

### Clase

- Un **elemento específico** en diagramas de clases
- Representa un **blueprint concreto** para objetos
- Contiene **atributos y métodos**
- **Enfocado en implementación**

> **Nota Importante**: Una clase en un diagrama de clases **tiene** un clasificador (su nombre), pero el clasificador en si mismo no es lo mismo que la clase.   
> 
> El clasificador es simplemente la etiqueta de identificación.

---

## 7. Pautas de Implementación
---

### _Convenciones de Nomenclatura_

- Usa **nombres claros y descriptivos** que reflejen el propósito del elemento
- Sigue **patrones de nomenclatura consistentes** a través de tu proyecto
- Evita **abreviaciones** a menos que sean ampliamente entendidas
- Usa **terminología significativa** relevante al dominio del problema


### _Consistencia_

- Mantén **estilos de nomenclatura uniformes** a través de todos los diagramas
- Asegura **alineación** entre diferentes tipos de diagrama
- Usa el **mismo clasificador** para el mismo concepto a través de diferentes vistas


### _Documentación_

- **Documenta significados de clasificadores** cuando puedan ser ambiguos
- Proporciona **contexto** para terminología específica del dominio
- Mantén un **glosario** de clasificadores usados en proyectos complejos

---


## Buenas Prácticas - Consejos
---

### 🎨 Fase de Diseño

- **Planifica tu estrategia de nomenclatura de clasificadores** temprano en el proyecto
- **Involucra a stakeholders** en definir nombres significativos
- **Considera mantenimiento futuro** al elegir nombres

### </> Implementación

- **Revisa consistencia de clasificadores** regularmente a través de diagramas
- **Refactoriza nombres** cuando cambien los requerimientos
- **Valida entendimiento** con miembros del equipo

### 📝 Documentación

- **Mantén una lista maestra** de todos los clasificadores usados
- **Actualiza documentación** cuando cambien los clasificadores
- **Proporciona contexto** para términos técnicos o específicos del dominio

### ❌ Errores Comunes

- No confundas clasificadores con los elementos de implementación reales
- Evita usar el mismo nombre para conceptos diferentes
- No cambies nombres de clasificadores sin actualizar todos los diagramas relacionados
- Resiste la tentación de usar jerga excesivamente técnica

---