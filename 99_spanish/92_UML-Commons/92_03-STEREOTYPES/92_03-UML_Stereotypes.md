|Guía|Título|
|---|---|
|06-152|Introducción a los Componentes UML y Elementos Comunes|
|06-153|Componentes Comunes de UML: Marcos (Frames)|
|06-154|Componentes Comunes de UML: Clasificadores (Classifiers)|
|**06-155**|**Componentes Comunes de UML: Estereotipos (Stereotypes)**|
|06-156|Componentes Comunes de UML: Comentarios y Notas|
|06-157|Componentes Comunes de UML: Dependencias|
|06-158|Componentes Comunes de UML: Características y Propiedades|
|06-159|Cuestionario: Introducción a UML|

---

# 06-155: ESTEREOTIPOS UML

### 1. Qué son los ESTEREOTIPOS

- **1.1** Definición y Propósito
- **1.2** Por Qué los Estereotipos Parecen Extraños
- **1.3** Cuándo y Dónde Usarlos

### 2. Sintaxis y Notación de Estereotipos

- **2.1** Reglas de Sintaxis Básicas
- **2.2** Representación Visual

### 3. Entendiendo la Extensión de Metaclases

- **3.1** Qué Significa "Extiende una Metaclase"
- **3.2** Traducción de Abstracto a Práctico
- **3.3** Beneficios de Nomenclatura Estandarizada

### 4. Aplicaciones Comunes de Estereotipos

- **4.1** Patrones Modelo-Vista-Controlador (MVC)
- **4.2** Representación de Patrones Arquitectónicos
- **4.3** Estereotipos Específicos de Framework
- **4.4** Modelado Específico de Dominio

### 5. Ejemplos Prácticos

- **5.1** Estereotipos de Arquitectura MVC
- **5.2** Patrones de Aplicaciones Empresariales
- **5.3** Estereotipos de Desarrollo Web
- **5.4** Estereotipos de Modelado de Base de Datos

### 6. Mejores Prácticas - Consejos

- **6.1** Cuándo Usar Estereotipos
- **6.2** Claridad vs Complejidad
- **6.3** Comunicación en Equipo
- **6.4** Consideraciones de Herramientas

---


## ***1. Qué son los ESTEREOTIPOS***
---

### 1.1 Definición y Propósito

Los **Estereotipos** son un mecanismo de extensión UML que permite:

- #### **Crear nuevos tipos de elementos de modelado ...
    
- #### ... extendiendo metaclases UML existentes.
    

Proporcionan una forma de dar nombres más **prácticos y significativos** a componentes de sistema abstractos o complejos.

#### Propósito

- **Clarificar conceptos abstractos** usando terminología familiar
- **Extender vocabulario UML** para dominios o frameworks específicos
- **Mejorar comunicación** entre miembros del equipo
- **Estandarizar convenciones de nomenclatura** a través de proyectos

---

### 1.2 Por Qué los Estereotipos Parecen Extraños

Los estereotipos pueden parecer confusos por varias razones:

- **No se usan en cada diagrama** - La aplicación selectiva los hace menos familiares

- **Naturaleza abstracta** - Representan extensiones conceptuales en lugar de elementos concretos

- **Sintaxis desconocida** - Los corchetes angulares dobles `<<estereotipo>>` son únicos de UML

- **Implementación incorrecta** - Muchas personas los usan mal, añadiendo confusión

Entender su propósito ayuda a desmitificar su apariencia y uso.

---

### 1.3 Cuándo y Dónde Usarlos

#### **Escenarios apropiados**

- **Documentación de patrones de  arquitectura** - Modelos **MVC, MVP, MVVM**

- **Modelado específico de framework** - Componentes React, Spring, Angular, .NET

- **Aplicaciones específicas de dominio** - Modelado de procesos de negocio, sistemas embebidos

- **Mejora de comunicación en equipo** - Hacer concretos conceptos abstractos

#### **Tipos de diagrama donde se usan comúnmente**

- Diagramas de Clases (más común)
- Diagramas de Componentes
- Diagramas de Paquetes
- Diagramas de Casos de uso (ocasionalmente)

---


## ***2. Sintaxis y Notación de Estereotipos***
---

### 2.1 Reglas de Sintaxis Básicas

#### **Notación estándar y posicionamiento**

```
<<nombre_estereotipo>>
NombreElemento
```

#### **Elementos clave**

- ##### **Corchetes angulares dobles** - `<<` y `>>` (_guillemets_)
    
- ##### **Nombre del estereotipo** - Identificador descriptivo
    
- ##### **Posicionamiento** - Arriba o antes del nombre del elemento
    
- ##### **Sensibilidad de mayúsculas** - Usualmente minúsculas o camelCase
    

---

### 2.2 Representación Visual

#### **Ejemplos de notación apropiada**

![IMG](./06-155_IMG2.png)

---


## 3. Entendiendo la Extensión de Metaclases
---

### 3.1 Qué Significa "Extiende una Metaclase"

#### **Metaclase**

> **METACLASE** = La "clase de una clase" - lo que define qué tipos de elementos pueden existir en UML

#### **Proceso de extensión**

- Tomar un tipo de elemento UML existente (como Clase o Componente)
    
- Agregar significado específico a través de un estereotipo
    
- Crear un nuevo tipo de elemento "virtual" con semántica mejorada
    

##### **Ejemplo**

- **Metaclase base:** Clase
- **Estereotipo:** `<<controller>>`
- **Resultado:** Una clase que específicamente representa un controlador en arquitectura MVC

---

### 3.2 Traducción de Abstracto a Práctico

##### **Escenario problemático**

```
Términos UML Abstractos   → Lo que Ven los Desarrolladores
─────────────────────────  ──────────────────────────────

        Boundary                  "¿Qué es esto?"
        Control                     "No entiendo"
        Entity                 "¿Cómo implemento esto?"
```

##### **Solución con estereotipos**

```
Términos Abstractos + Estereotipos  → Comprensión Clara
───────────────────────────────────  ──────────────────

          Boundary → <<view>>        "Componente de interfaz de usuario"
          Control → <<controller>>   "Manejador de lógica de negocio"
          Entity → <<model>>         "Representación de datos"
```

---

### 3.3 Beneficios de Nomenclatura Estandarizada

##### 😩 **Antes de los estereotipos**

- Desarrolladores confundidos por terminología UML abstracta
- Interpretación inconsistente de elementos de diagrama
- Dificultad conectando UML con implementación de código actual
- Problemas de comunicación en equipo

#### 🗿 **Después de los estereotipos**

- **Vocabulario común** - Todos entienden `<<controller>>`
- **Guía de implementación** - Mapeo claro a patrones de código
- **Alineación de framework** - Coincide con patrones arquitectónicos populares
- **Incorporación más rápida** - Nuevos desarrolladores reconocen términos familiares

---


## ***4. Aplicaciones Comunes de Estereotipos***
---

### _**4.1 Patrones Modelo-Vista-Controlador (MVC)**_

#### **Estereotipos MVC estándar**

|Estereotipo|Propósito|Responsabilidades Típicas|
|---|---|---|
|`<<model>>`|Representación de datos|Lógica de negocio, validación de datos, persistencia|
|`<<view>>`|Interfaz de usuario|Mostrar datos, capturar entrada del usuario, presentación|
|`<<controller>>`|Control de flujo|Manejar requests, coordinar modelo/vista, enrutamiento|

##### **Ejemplo de implementación**

```
 <<model>>      <<controller>>      <<view>>
Usuario        ControladorUsuario  PaginaPerfilUsuario
├─ nombre      ├─ crearUsuario()   ├─ mostrarPerfil()
├─ email       ├─ actualizarUsuario() ├─ editarPerfil()
└─ validar()   └─ eliminarUsuario() └─ mostrarErrores()
```

---

### _**4.2 Representación de Patrones Arquitectónicos**_

#### **Estereotipos de aplicaciones empresariales**

- `<<service>>` - Capa de servicio de negocio
- `<<repository>>` - Capa de acceso a datos
- `<<factory>>` - Patrones de creación de objetos
- `<<facade>>` - Interfaz simplificada a subsistemas complejos
- `<<adapter>>` - Adaptación de interfaz entre componentes incompatibles

---

### _**4.3 Estereotipos Específicos de Framework**_

#### **Ejemplos de Spring Framework**

- `<<component>>` - Componente gestionado por Spring
- `<<restController>>` - Manejador de endpoint de API REST
- `<<service>>` - Bean de servicio de negocio
- `<<repository>>` - Repositorio de acceso a datos

##### **Ejemplos de Framework Angular**

- `<<component>>` - Componente Angular
- `<<service>>` - Servicio inyectable
- `<<directive>>` - Directiva personalizada
- `<<pipe>>` - Pipe de transformación de datos

---

### _**4.4 Modelado Específico de Dominio**_

#### **Estereotipos de desarrollo web**

- `<<api>>` - Interfaz de Web API
- `<<middleware>>` - Middleware de procesamiento de requests
- `<<validator>>` - Componente de validación de entrada
- `<<authenticator>>` - Manejador de autenticación

#### **Estereotipos de modelado de base de datos**

- `<<entity>>` - Entidad/tabla de base de datos
- `<<valueObject>>` - Representación de valor inmutable
- `<<aggregate>>` - Raíz de agregado de dominio
- `<<specification>>` - Especificación de regla de negocio

---


## ***5. Ejemplos Prácticos***
---

### _**5.1 Estereotipos de Arquitectura MVC**_

#### 😩 **UML tradicional (confuso)**

```
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ Boundary    │ │ Control     │ │ Entity      │
│ FormUsuario │ │ ManejadorUs │ │ DatosUsuario│
└─────────────┘ └─────────────┘ └─────────────┘
```

### 🗿 **Con estereotipos (claro)**

```
┌──────────────┐ ┌────────────────┐ ┌────────────────┐
│ <<view>>     │ │<<controller>>  │ │ <<model>>      │
│ FormUsuario  │ │ ManejadorUs    │ │ DatosUsuario   │
├──────────────┤ ├────────────────┤ ├────────────────┤
│ +renderizar()│ │ +procesar()    │ │ +guardar()     │
│ +validar()   │ │ +enrutar()     │ │ +validar()     │
└──────────────┘ └────────────────┘ └────────────────┘
```

---

### _**5.2 Patrones de Aplicaciones Empresariales**_

#### **Arquitectura por capas con estereotipos**

```
┌─────────────────────────────────────┐
│ <<controller>>                      │
│ ControladorOrden                    │
├─────────────────────────────────────┤
│ + crearOrden()                      │
│ + actualizarOrden()                 │
└─────────────────────────────────────┘
│
▼

┌─────────────────────────────────────┐
│ <<service>>                         │
│ ServicioOrden                       │
├─────────────────────────────────────┤
│ + procesarOrden()                   │
│ + calcularTotal()                   │
└─────────────────────────────────────┘
│
▼

┌─────────────────────────────────────┐
│ <<repository>>                      │
│ RepositorioOrden                    │
├─────────────────────────────────────┤
│ + guardar()                         │
│ + buscarPorId()                     │
└─────────────────────────────────────┘
```

---

### _**5.3 Estereotipos de Desarrollo Web**_

#### **Modelado de API REST**

```
┌────────────────────┐
│ <<restController>> │
│ APIUsuario         │
├────────────────────┤
│ + GET /usuarios    │
│ + POST /usuarios   │
│ + PUT /usuarios/:id│
│ + DELETE /usuarios │
└────────────────────┘
│
▼
┌──────────────────────┐
│ <<service>>          │
│ ServicioUsuario      │
├──────────────────────┤
│ + crearUsuario()     │
│ + buscarUsuario()    │
│ + actualizarUsuario()│
│ + eliminarUsuario()  │
└──────────────────────┘
```

---

### _**5.4 Estereotipos de Modelado de Base de Datos**_

#### **Ejemplo de diseño dirigido por dominio**

```
┌─────────────────┐
│ <<aggregate>>   │
│ Orden           │
├─────────────────┤
│ - id:IdOrden    │
│ - total: Dinero │
│ + agregarItem() │
│ + calcular()    │
└─────────────────┘
│
▼
┌─────────────────┐
│ <<entity>>      │
│ ItemOrden       │
├─────────────────┤
│ - id: IdItem    │
│ - cantidad: int │
│ - precio: Dinero│
└─────────────────┘
```

---


## ***6. Mejores Prácticas / Consejos***
---

### 6.1 Cuándo Usar Estereotipos


### 👌 **Usa estereotipos cuando**

- **Elementos UML abstractos necesiten clarificación** para el equipo
    
- **Patrones arquitectónicos** necesiten documentación explícita
    
- **Componentes específicos de framework** requieran identificación
    
- **Terminología de dominio** difiere del vocabulario UML estándar
    
- **Herramientas de generación de código** necesiten información semántica adicional
    

### ❌ **EVITA estereotipos cuando**

- La notación UML estándar ya es clara
    
- Agrega complejidad innecesaria a diagramas simples
    
- Los miembros del equipo no están familiarizados con los significados del estereotipo
    
- Los diagramas se saturan con demasiados estereotipos
    

---

### 6.2 Claridad vs Complejidad

#### 🗿 **Buena práctica - Claro y útil**

```
<<controller>>
ControladorUsuario

+ manejarLogin()
+ manejarRegistro()
```

#### 😩 **Mala práctica - Excesivamente detallado**

```
<<springMvcRestControllerWithJsonResponseHandling>>
ControladorUsuario
```

### **Pautas**

- **Mantén nombres de estereotipos cortos** y significativos
- **Usa convenciones establecidas** cuando sea posible
- **Prioriza claridad** sobre precisión técnica
- **Míralo desde la parte del receptor** - ¿qué entenderán?

---

### 6.3 Comunicación en Equipo

### **Estableciendo estándares de estereotipos**

- **Crea un glosario de equipo** de estereotipos aprobados
- **Documenta significados de estereotipos** y pautas de uso
- **Usa nomenclatura consistente** a través de todos los diagramas del proyecto
- **Entrena a miembros del equipo** en semántica de estereotipos
- **Revisa y valida** el uso de estereotipos en sesiones de diseño

---

### 6.4 Consideraciones de Herramientas

### **Soporte de herramientas UML**

- **Verifica capacidades de herramientas** - no todas las herramientas soportan estereotipos personalizados
- **Usa perfiles estándar** cuando estén disponibles (perfiles UML para dominios específicos)
- **Considera generación de código** - algunas herramientas generan código basado en estereotipos
- **Compatibilidad de exportación** - asegura que los estereotipos sobrevivan las exportaciones de diagramas

### **Beneficios de generación de código**

- Los estereotipos pueden guiar generación de código automática (y manual)
- Se pueden aplicar plantillas específicas de framework
- Los patrones arquitectónicos se pueden estructurar automáticamente
- Mejora la consistencia entre modelo e implementación

---