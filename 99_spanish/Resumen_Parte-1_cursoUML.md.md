# Resumen de la primera parte del curso UML


>  ***¿Qué y  Para qué, respecto a UML?***
>  
>  UML es una _**herramienta de comunicación visual**_ que permite a los equipos de desarrollo _**planificar, diseñar y documentar**_ sistemas de software de manera efectiva. 

---

> ***¿Cómo, respecto a UML?***
> 
> Los _**diagramas de tipo ESTRUCTURAL**_, (como los de **Clases/Objetos, Paquetes, Despliegue,**... )  muestran la estructura estática del sistema, mientras que los _**diagramas de tipo COMPORTAMENTAL**_ (como los de **Actividades, Casos de Uso, Secuenciales**,... ) modelan el comportamiento dinámico y los flujos de trabajo.
> 
> En las ***distintas fases de desarrollo*** (`Pre-Desarrollo`, `Desarrollo Activo`, `Post-Desarrillo/Mantenimiento`), usaremos un tipo u otro de diagrama para facilitar el diseño y análisis necesarios de cara a hacer una efectiva implementación

---

>  ***¿Por qué, de UML?***
>  
>  "_**Pensar primero, programar después**_"
>  
>   La inversión en análisis y diseño UML reduce significativamente el tiempo de desarrollo, errores de implementación y facilita la comunicación entre todas las partes involucradas en un proyecto, indistintamente de si poseen conocimientos técnicos (desarrolladores), o no (partes administrativas, inversores, clientes finales).


---

1. **Fundamentos de UML**
    
    1. La Importancia del Análisis y Diseño de Sistemas
    2. Visión General de Sistemas de Software
    3. Qué es UML
    4. Etapas de Desarrollo donde se Utiliza UML

2. **Elementos Comunes de UML**
    
    1. Marcos (Frames)
    2. Clasificadores (Classifiers)
    3. Estereotipos (Stereotypes)
    4. Comentarios y Notas
    5. Dependencias
    6. Características y Propiedades

3. **Tipos de Diagramas UML**
    
    1. Clasificación Principal
    2. Diagramas Estructurales 
    3. Diagramas de Comportamiento 

4. **Diagramas de Clases **
    
    1. Estructura Básica
    2. Asociaciones y Relaciones
    3. Ejemplos Prácticos Detallados

5. **Diagramas de Actividad **
    
    1. Elementos Principales
    2. Aplicación Práctica
    3. Ventajas

6. **Conceptos Generales para implementación
    
    1. Principios Fundamentales
    2. Buenas prácticas

---

## _**1. Fundamentos de UML**_

### **1.1 La Importancia del Análisis y Diseño de Sistemas**

- **Objetivo Principal**: Desarrollar _**mentalidad analítica**_ de resolución de problemas
- **Filosofía**: _**"Piensa Primero, Programa Después"**_
- **Beneficios**:
    - _**Mejor planificación**_ = Implementación más fácil
    - _**Reduce errores**_ y refactorización
    - _**Enfoque sistemático**_ para sistemas complejos

---

### **1.2 Visión General de Sistemas de Software**

- **Sistemas de Alto Nivel**: Aplicaciones con _**interacción directa del usuario**_
- **Sistemas de Bajo Nivel**: Componentes que operan _**"tras el telón"**_
- **Categorías**: _**Web apps, móviles, empresariales, embebidos**_, etc.
- **Enfoque Holístico**: Considerar _**todas las piezas**_ como un sistema completo

---

### **1.3 Qué es UML**

- **Definición**: _**Lenguaje de Modelado Unificado**_ (Unified Modeling Language)
- **Propósito**: Comunicación _**agnóstica del lenguaje**_ entre desarrolladores y stakeholders
- **Beneficios**:
    - _**Abstracción**_ de detalles de implementación
    - _**Comunicación**_ con partes no técnicas
    - _**Herramienta de análisis**_ y planificación

---

### **1.4 Etapas de Desarrollo donde se Utiliza UML**

- **Pre-Desarrollo**: _**Diagramas de Actividad**_ y Despliegue
- **Desarrollo Activo**: _**Diagramas de Clases**_ y Casos de Uso
- **Post-Desarrollo/Mantenimiento**: _**Diagramas de Secuencia**_ y Paquetes

---



## _**2. Elementos Comunes de UML**_
---
### **2.1 Marcos (Frames)**

- **Propósito**: _**Contenedores de encapsulación**_ con límites contextuales
- **Estructura**: Borde rectangular + _**Encabezado**_ (esquina superior izquierda)
- **Formato**: `[TipoDeDiagrama] NombreDiagrama [InfoOpcional]`
- **Abreviaciones**: `uc` (Casos de Uso), `class` (Clases), `act` (Actividad), etc.

---

### **2.2 Clasificadores (Classifiers)**

- **Definición**: _**Mecanismos de identificación**_ para elementos UML
- **Naturaleza**: _**Abstracta**_ - no se implementan directamente
- **Uso**: Nombrar _**clases, actores, casos de uso**_, etc.
- **Aplicación**: _**Universal**_ a través de todos los diagramas UML

---

### **2.3 Estereotipos (Stereotypes)**

- **Sintaxis**: `<<nombre_estereotipo>>`
- **Propósito**: _**Extender vocabulario UML**_ para dominios específicos
- **Ejemplos**: `<<controller>>`, `<<model>>`, `<<view>>` (patrón MVC)
- **Beneficio**: Hacer _**concretos conceptos abstractos**_

---

### **2.4 Comentarios y Notas**

- **Representación**: Rectángulo con _**esquina "doblada"**_
- **Conexión**: _**Líneas punteadas**_ a elementos relacionados
- **Contenido**: _**Texto de forma libre**_, sin restricciones
- **Uso**: Explicar _**reglas de negocio**_, guía de implementación

---

### **2.5 Dependencias**

- **Notación**: Línea discontinua con flecha abierta (`Cliente -----> Proveedor`)
- **Significado**: _**"A depende de B"**_ - cambios en B pueden afectar A
- **Tipos**: _**Uso, abstracción, permiso, realización, sustitución**_
- **Gestión**: _**Minimizar acoplamiento fuerte**_

---

### **2.6 Características y Propiedades**

- **Características**: Qué _**puede hacer**_ (comportamental)
- **Propiedades**: Qué _**tiene**_ (estructural)
- **Visibilidad**: `+` público, `-` privado, `#` protegido, `~` paquete
- **Sintaxis**: `[visibilidad] nombre: tipo [multiplicidad] = valorDefecto`

---



## _**3. Tipos de Diagramas UML**_
---

### **3.1 Clasificación Principal**


#### 🏗️ **Estructurales** (7 tipos): Muestran qué _**existe**_ en el sistema

- _**Clases, Objetos, Componentes**_, _**Paquetes, Despliegue**_, Perfil,  Estructura Compuesta


#### ⚡ **de Comportamiento** (7 tipos): Muestran qué _**sucede**_ en el sistema

- _**Casos de Uso, Actividad**_, _**Secuencia**_, ***Máquina de Estados***, Comunicación, Temporización, Visión General de Interacción

---

### **3.2 Diagramas Estructurales**

- **Diagramas de Clases**: _**Más populares**_, diseño de esquemas de BBDD, relaciones entre objetos
- **Diagramas de Despliegue**: _**Arquitectura física**_, nodos y componentes, integración CI/CD
- **Diagramas de Paquetes**: _**Organización de bibliotecas**_, gestión de ***dependencias***

---

### **3.3 Diagramas de Comportamiento**

- **Diagramas de Actividad**: _**Flujos de trabajo**_, accesibles para no técnicos
- **Diagramas de Casos de Uso**: _**Sistema de autorización**_, roles y permisos
- **Diagramas de Máquina de Estados**: _**Ciclo de vida de datos**_, transiciones
- **Diagramas de Secuencia**: _**Diseño basado en mensajes**_, implementación detallada

---



## _**4. Diagramas de Clases**_
----
### **4.1 Estructura Básica**

#### 📋 **Tres secciones obligatorias:**

1. **Nombre**: Sustantivo en _**PascalCase**_
2. **Atributos**: `[visibilidad] nombre: tipo`
3. **Operaciones**: `[visibilidad] nombreMetodo(): tipoRetorno`

---


### **4.2 Asociaciones y Relaciones**

#### 🔗 **Asociación**

- **Definición**: _**Conexión fundamental**_ entre clases que modela relaciones del mundo real

- **Representación**: _**Línea sólida**_ entre clases

- **Tipos**:
    - **Bidireccional**: Por defecto, _**ambas clases pueden acceder**_ entre sí
    - **Unidireccional**: Solo _**una clase puede acceder**_ a la otra (flecha en un extremo)

- **Propósito**: Define ***cómo las instancias se relacionan y dependen e***ntre sí


---

#### 📊 **Multiplicidad**

- **Definición**:   _**Restricciones numéricas**_ que definen cardinalidad de relaciones
  
- **Notaciones**:
  
    - `1`: _**Exactamente una instancia**_ (obligatorio)
    - `0..1`: _**Cero o una instancia**_ (opcional)
    - `1..*`: _**Una o más instancias**_ (al menos una requerida)
    - `0..*` o `*`: _**Cero o más instancias**_ (completamente opcional)
    - `n..m`: _**Rango específico**_ entre n y m instancias
      

- **Uso**: Se coloca en _**ambos extremos**_ de la línea de asociación

- **Aplicación**: Refleja las _**restricciones reales**_ de un sistema genérico 
  
Por ejemplo, en una tienda on-line, un `Pedido` no podría tener CERO artículos, sino uno como mínimo.

Su multiplicidad podría definirse así: 

`Pedido (1) <--> LineasDePedido (1... *)` )

#### **Patrones de Multiplicidad Comunes**

- **1:1** - _**Persona ↔ Identificación**_
- **1:N** - _**Cliente (1) ↔ Pedido (*)**_
- **N:M** - _**Estudiante (*) ↔ Curso (*)**_


---

#### 🧭 **Navegabilidad**

- **Definición**: Reglas que determinan _**rutas de comunicación**_ entre clases

- **Capacidades**:

     - **Acceso Directo**: Siguiendo _**líneas de asociación inmediatas**_
    - **Acceso Indirecto**: Traversando _**múltiples rutas**_ de asociación

- **Tipos de Navegación**:

    - **Bidireccional**: Acceso posible en _**ambas direcciones**_ (Por defecto)
    - **Unidireccional**: Acceso restringido a _**una dirección específica**_

- **Implementación**: Se traduce directamente en _**referencias de objetos**_ en código

- **Ventaja Visual**: UML permite _**trazar rutas**_ de relación visualmente


---
#### 🎭 **Roles (Contexto Adicional)**

- **Definición**: Nombres que describen el _**papel de cada clase**_ en la asociación

- **Uso**: Clarifica el contexto cuando _**la relación no es obvia**_

- **Ejemplo**: En "Persona - Empresa", los roles podrían ser _**"empleado" y "empleador"**_

---

### **4.3 Ejemplo Sistema por capas MVC, usando Clases

#### 📝 **Ejemplo Topic-Guide-Tag**

![large](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+12.14.41+PM.png)

```
Topic (1) ←─── pertenece a ───→ Guide (1..*)
  │                               │
  └─ Rol: "categoría"             └─ Rol: "contenido"

Guide (*) ←─── etiquetada con ───→ Tag (1..*)
  │                                 │
  └─ Rol: "contenido"               └─ Rol: "palabra clave"
```


#### 🗺️ **Navegabilidad en el Ejemplo**

- **Desde Topic**: Acceso a _**todas las guías**_ → acceso indirecto a etiquetas
- **Desde Guide**: Acceso directo al _**topic padre**_ y a etiquetas asociadas
- **Desde Tag**: Acceso a _**guías**_ → acceso indirecto a topics


---

## _**5. Diagramas de Actividad **_

### **5.1 Elementos Principales (7)**

1. **Estado Inicial**: _**Círculo negro relleno**_ (punto de inicio)

2. **Estado de Actividad/Acción**: _**Rectángulos redondeados**_

3. **Flujo de Acción**: _**Flechas con puntas rellenas**_

4. **Puntos de Decisión**: _**Formas de diamante**_

5. **Guardas**: Condiciones como _**"sí", "no", expresiones**_

6. **Estado Final**: _**Círculo con círculo relleno**_ adentro (ojo de buey)

7. **Carriles (Swim Lanes)**: _**Divisiones por responsabilidad/rol**_

---

### **5.2 Aplicación Práctica**

#### 🎓 **Sistema de Calificación en Línea**: Ejemplo completo

![large](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+10.36.27+AM.png)

- #### **Tres Carriles**:     _**Mentor, Sistema, Estudiante**_


- #### **Flujo de Proceso**
  _**Asignar → Generar → Confirmar → Preguntar/Responder**_ (bucle) → _**Procesar → Aprobar → Almacenar**_


- #### **Punto de Decisión** 
  _**"¿Es la última pregunta?"**_ (Sí/No)

---

### **5.3  Ventajas de Actividades**

- _**Accesibles**_ para cualquiera sin conocimientos técnicos
- _**Modelado**_ de procesos reales de un negocio/proyecto
- _**Documentación**_ de flujos de trabajo
- _**Planificación**_ de experiencia de usuario

---



## _**6. Conceptos Generales para el uso de UML**_
---

### **6.1    Principios Fundamentales**

- #### **Análisis antes que picar código** 
  _**Planificación visual**_ que reduce errores
  
- #### **Comunicación universal** 
  _**UML como lenguaje común**_

- #### **Abstracción apropiada** 
  Enfoque en _**diseño, no en la implementación**_

- #### **Reutilización** 
  _**Patrones y elementos comunes**_ que pueden replicarse según sea necesario

---

### **6.2    Buenas Prácticas**

- ##### _**Nomenclatura consistente**_ y descriptiva

- ##### _**Minimizar complejidad**_ y dependencias

- ##### Usar _**herramientas apropiadas**_ para cada fase

- ##### Mantener _**diagramas actualizados**_ respecto al código

- ##### _**Potenciar la Colaboración**_ entre equipos técnicos y no técnicos

---