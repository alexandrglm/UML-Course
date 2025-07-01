|Guía|Título|
|---|---|
|06-152|Introducción a los Componentes UML y Elementos Comunes|
|06-153|Componentes UML Comunes: Marcos (Frames)|
|06-154|Componentes UML Comunes: Clasificadores (Classifiers)|
|06-155|Componentes UML Comunes: Estereotipos (Stereotypes)|
|06-156|Componentes UML Comunes: Comentarios y Notas|
|06-157|Componentes UML Comunes: Dependencias (Dependencies)|
|**06-158**|**Componentes UML Comunes: Características y Propiedades**|
|06-159|Cuestionario: Introducción a UML|

---

# 06-158: UML    CARACTERÍSTICAS-PROPIEDADES

### 1. Qué son las Características y Propiedades

- **1.1** Definición y Conceptos Fundamentales
- **1.2** Aplicación Universal Across Diagramas
- **1.3** Papel en la Especificación de Elementos

### 2. Entendiendo las Características en UML

- **2.1** Fundamentos de Características
- **2.2** Tipos de Características
- **2.3** Características de las Características
- **2.4** Visibilidad y Acceso de Características

### 3. Entendiendo las Propiedades en UML

- **3.1** Definiciones de Propiedades
- **3.2** Tipos y Categorías de Propiedades
- **3.3** Restricciones y Especificaciones de Propiedades
- **3.4** Relaciones de Propiedades

### 4. Convenciones de Nomenclatura Estandarizadas

- **4.1** Importancia de la Consistencia
- **4.2** Beneficios de las Convenciones de Nomenclatura
- **4.3** Mejora de la Comunicación del Equipo
- **4.4** Calidad del Código y Mantenibilidad

### 5. Características y Propiedades en Diferentes Tipos de Diagramas

- **5.1** Diagramas de Clases
- **5.2** Diagramas de Objetos
- **5.3** Diagramas de Componentes
- **5.4** Diagramas de Paquetes
- **5.5** Otras Aplicaciones de Diagramas

### 6. Especificación y Documentación de Atributos

- **6.1** Estándares de Nomenclatura de Atributos
- **6.2** Especificaciones de Tipos de Datos
- **6.3** Multiplicidad y Restricciones
- **6.4** Valores por Defecto e Inicialización

### 7. Visibilidad y Control de Acceso

- **7.1** Modificadores de Visibilidad
- **7.2** Acceso Público, Privado y Protegido
- **7.3** Visibilidad de Paquete e Implementación
- **7.4** Principios de Encapsulación

### 8. Operaciones y Características Comportamentales

- **8.1** Definiciones de Métodos
- **8.2** Firmas de Operaciones
- **8.3** Especificaciones de Parámetros
- **8.4** Tipos de Retorno y Excepciones

### 9. Conceptos Avanzados de Características

- **9.1** Características Estáticas vs de Instancia
- **9.2** Características Abstractas y Virtuales
- **9.3** Propiedades Derivadas
- **9.4** Redefinición de Características y Herencia

### 10. Mejores Prácticas y Directrices

- **10.1** Estándares de Convenciones de Nomenclatura
- **10.2** Estrategias de Documentación
- **10.3** Directrices de Colaboración en Equipo
- **10.4** Prácticas de Aseguramiento de Calidad

### 11. Errores Comunes y Anti-Patrones

- **11.1** Problemas de Nomenclatura Inconsistente
- **11.2** Problemas de Sobre-Especificación
- **11.3** Mal Uso de Visibilidad
- **11.4** Descuido de Documentación

### 12. Herramientas y Soporte de Implementación

- **12.1** Herramientas de Modelado UML
- **12.2** Características de Generación de Código
- **12.3** Capacidades de Ingeniería Inversa
- **12.4** Generación de Documentación

---

## _**1. Qué son las Características y Propiedades**_
---

### 1.1 Definición y Conceptos Fundamentales

**Las Características** (también denominadas **Propiedades**) en UML representan los **bloques fundamentales de construcción que definen las características y capacidades de los elementos del modelo**.

Describen... :  

- #### lo que un elemento _**tiene**_ (propiedades)
    
- #### lo que **puede hacer** (características comportamentales).
    


#### **Definiciones**

##### **Característica (Feature)**

> Una característica distintiva de un elemento del modelo que puede ser estructural o comportamental


##### **Propiedad (Property)**

> Una característica estructural que representa un atributo o extremo de asociación de un clasificador


##### **Elemento (Element)**

> Cualquier parte constituyente de un modelo UML que puede tener características y propiedades

Estos conceptos forman la base para crear modelos UML consistentes, comprensibles y mantenibles a través de diferentes tipos de diagramas y equipos de desarrollo.

---

### 1.2 Aplicación Universal a Través de Diagramas

Su naturaleza universal significa que entender estos conceptos proporciona una base que se aplica a:

- **Diagramas estructurales** - Diagramas de clases, objetos, componentes, paquetes y despliegue
- **Diagramas comportamentales** - Diagramas de casos de uso, actividad, secuencia y máquinas de estado
- **Diagramas de interacción** - Diagramas de comunicación y temporización

Esta universalidad permite prácticas consistentes de comunicación y documentación a través de todos los aspectos del modelado de sistemas.

---

### 1.3 Papel en la Especificación de Elementos

Las características y propiedades cumplen papeles críticos en la especificación de elementos:

- **Identificación** - Identificar y diferenciar elementos de manera única
- **Especificación** - Definir las características detalladas de los elementos
- **Comunicación** - Proporcionar un vocabulario común para discusiones del equipo
- **Documentación** - Crear modelos auto-documentados que expliquen el comportamiento del sistema
- **Guía de implementación** - Dirigir actividades de generación de código y desarrollo

---


## ***2. Entendiendo las Características en UML***
---

### 2.1 Fundamentos de Características

Una **característica** es una característica distintiva de un elemento del modelo.
Las características pueden ser:

- **Características estructurales** - Definen lo que un elemento contiene o de lo que está compuesto
- **Características comportamentales** - Definen lo que un elemento puede hacer o cómo se comporta

#### **Categorías de características**

```
Características

├── Características Estructurales
|       |
│       ├── Propiedades (Atributos)
│       ├── Extremos de Asociación
│       └── Puertos
|
└── Características Comportamentales
|
├── Operaciones (Métodos)
|
├── Recepciones
|
└── Puntos de Extensión
```

---

### 2.2 Tipos de Características

#### **Características Estructurales**

1. **Atributos** - Propiedades simples con valores   
   Ejemplo: `nombre: String`, `edad: Integer`
    
2. **Extremos de Asociación** - Conexiones a otros elementos   
   Ejemplo: Cliente tiene Pedidos (relación de multiplicidad)
    
3. **Puertos** - Puntos de interacción para componentes   
   Ejemplo: Interfaces de servicio, endpoints de comunicación
    

#### **Características  De Comportamiento**

1. **Operaciones** - Métodos que pueden ser invocados   
   Ejemplo: `calcularTotal(): Money`, `validar(): Boolean`
    
2. **Recepciones** - Capacidades de manejo de señales  
   Ejemplo: Manejadores de eventos, procesadores de mensajes
    
3. **Puntos de Extensión** - Puntos de variación en casos de uso   
   Ejemplo: Pasos opcionales en flujos de casos de uso
    

---

### 2.3 Elementos Comunes de las Características

Todas las características tienen características comunes que definen su comportamiento:

#### **Propiedades de identidad**

- **Nombre** - Identificador único dentro del elemento contenedor
- **Tipo** - Tipo de datos o clasificador que define la característica
- **Multiplicidad** - Número de valores que la característica puede contener
- **Visibilidad** - Nivel de acceso para la característica

#### **Propiedades comportamentales**

- **Ámbito** - Nivel de instancia o nivel de clasificador (estático)
- **Capacidad de cambio** - Si los valores pueden modificarse después de la inicialización
- **Ordenamiento** - Si múltiples valores tienen un orden específico
- **Unicidad** - Si se permiten valores duplicados

---

### 2.4 Visibilidad y Acceso de Características

La visibilidad de características controla el acceso a las características desde fuera del elemento contenedor:

|Visibilidad|Símbolo|Nivel de Acceso|Descripción|
|---|---|---|---|
|**Público**|`+`|Sin restricción|Accesible desde cualquier lugar|
|**Privado**|`-`|Solo elemento|Accesible solo dentro del elemento|
|**Protegido**|`#`|Herencia|Accesible al elemento y sus descendientes|
|**Paquete**|`~`|Ámbito paquete|Accesible dentro del mismo paquete|

---


## _**3. Entendiendo las Propiedades en UML**_
---

### 3.1 Definiciones de Propiedades

**Las propiedades** son características estructurales que representan elementos tipados dentro de un clasificador. Son el tipo más común de característica y aparecen como atributos en diagramas de clases.

#### **Sintaxis de propiedades**

```
[visibilidad] nombre [multiplicidad] : tipo [= defecto] [modificadores-propiedad]
```

#### **Ejemplo**

- `+ titulo: String` - Propiedad string pública
- `- id: Integer [1] = 0` - Entero privado con valor por defecto
- `# elementos: Producto [0..*] {ordered}` - Colección protegida con restricciones

---

### 3.2 Tipos y Categorías de Propiedades

#### **Propiedades Simples**

- **Tipos primitivos** - String, Integer, Boolean, Real
- **Tipos de enumeración** - Conjuntos predefinidos de valores
- **Tipos de datos personalizados** - Tipos de valores definidos por el usuario

#### **Propiedades Complejas**

- **Referencias de clase** - Propiedades que referencian otras clases
- **Propiedades de colección** - Arrays, listas, conjuntos de otros elementos
- **Propiedades compuestas** - Propiedades que contienen otros datos estructurados


#### **Categorías Especiales de Propiedades**

##### 1. **Propiedades derivadas** - Valores calculados desde otras propiedades

- Notación: `/nombrePropiedad`
- Ejemplo: `/nombreCompleto` derivado de primerNombre y apellido

##### 2. **Propiedades estáticas** - Compartidas entre todas las instancias

- Notación: Nombre de propiedad subrayado
- Ejemplo: `contador: Integer` (subrayado)

---

### 3.3 Restricciones y Especificaciones de Propiedades

#### **Restricciones de multiplicidad**

- `[1]` - Exactamente uno (por defecto para propiedades de valor único)
- `[0..1]` - Cero o uno (propiedad opcional)
- `[0..*]` - Cero o más (colección ilimitada)
- `[1..*]` - Uno o más (colección requerida)
- `[n..m]` - Entre n y m valores

#### **Modificadores de propiedades**

- `{ordered}` - La colección mantiene orden de inserción
- `{unique}` - No se permiten valores duplicados
- `{readOnly}` - El valor no puede cambiarse después de la inicialización
- `{union}` - La propiedad representa unión de otras propiedades
- `{subsets nombrePropiedad}` - La propiedad es subconjunto de otra propiedad

---

### 3.4 Relaciones de Propiedades

Las propiedades pueden participar en varias relaciones:

#### **Relaciones de subconjunto**

```
Persona
---
+ contactos: Contacto [*]
+ amigos: Persona [*] {subsets contactos}
+ colegas: Persona [*] {subsets contactos}

```

#### **Relaciones de unión**

```
Vehiculo
---
+ /ocupantes: Persona [*] {union}
+ conductor: Persona [1] {subsets ocupantes}
+ pasajeros: Persona [*] {subsets ocupantes}
```

---


## *4. Convenciones de Nomenclatura Estandarizadas*
---

### 4.1 Importancia de la Consistencia

Las convenciones de nomenclatura estandarizadas son cruciales por varias razones:

#### **Beneficios en la Comunicación**

- **Comprensión universal** - Todos los miembros del equipo usan la misma terminología
- **Ambigüedad reducida** - Significado claro elimina confusión
- **Incorporación más rápida** - Los nuevos miembros del equipo aprenden patrones rápidamente
- **Colaboración entre equipos** - Prácticas consistentes a través de proyectos


#### **Beneficios en etapas de post-desarrollo / Mantenimiento

- **Legibilidad del código** - Código auto-documentado a través de nombres claros
- **Seguridad en refactorización** - Patrones consistentes hacen los cambios más seguros
- **Reducción de errores** - Nomenclatura clara reduce malentendidos
- **Transferencia de conocimiento** - Más fácil traspasar proyectos entre desarrolladores

---

### 4.2 Beneficios de las Convenciones de Nomenclatura

#### **Escenario del equipo de desarrollo** 

Sin convenciones de nomenclatura, cinco desarrolladores trabajando independientemente podrían crear:

- Desarrollador A: `usr_nm`, `usrEmail`, `user_created`
- Desarrollador B: `userName`, `emailAddress`, `dateCreated`
- Desarrollador C: `name`, `email`, `timestamp`
- Desarrollador D: `user_name`, `user_email`, `created_at`
- Desarrollador E: `Name`, `Email`, `CreatedDate`

#### **Resultado** 

Base de código inconsistente y confusa que es difícil de mantener.



#### 🗿 **Con estandarización de características y propiedades UML**

- Todos los desarrolladores usan: `name: String`, `email: String`, `createdAt: DateTime`
- **Patrones consistentes** a través de toda la aplicación
- **Estructura predecible** para nuevos desarrolladores
- **Base de código mantenible** con intención clara

---

### 4.3 Mejora de la Comunicación del Equipo

Las características y propiedades estandarizadas crean un **vocabulario común** para la comunicación del equipo:

- **En documentación:** "La clase Usuario tiene una propiedad `name` que almacena el nombre completo del usuario"
    
- **En revisiones de código:** "Actualiza la propiedad `updatedAt` cuando el registro cambie"
    
- **En reuniones:** "Necesitamos añadir una característica `status` para rastrear el estado del pedido"
    

Este lenguaje compartido elimina confusión y acelera las discusiones de desarrollo.

---

### 4.4 Calidad del Código y Mantenibilidad

#### **Mejoras de calidad**

- **Patrones predecibles** - Los desarrolladores saben qué esperar
- **Carga cognitiva reducida** - Menos esfuerzo mental para entender el código
- **Depuración más rápida** - Nomenclatura consistente ayuda en la identificación de problemas
- **Pruebas mejoradas** - Nombres claros de propiedades mejoran legibilidad de pruebas

#### **Beneficios de mantenibilidad**

- **Refactorización más fácil** - Patrones consistentes simplifican cambios a gran escala
- **Preservación de conocimiento** - Las convenciones de nomenclatura codifican conocimiento del equipo
- **Eficiencia de incorporación** - Nuevos desarrolladores aprenden más rápido con patrones consistentes
- **Consistencia entre proyectos** - Los patrones se transfieren entre proyectos

---


## ***5. Características y Propiedades en Diferentes Tipos de Diagramas***
---

### 5.1 Diagramas de Clases

Los diagramas de clases son la ubicación primaria para especificación detallada de características y propiedades:

```
┌─────────────────────────────────┐
│               Tema              │
├─────────────────────────────────┤
│ + titulo: String                │
│ + slug: String                  │
│ + fechaCreacion: DateTime       │
│ + fechaActualizacion: DateTime  │
│ + /topDiez: Query {readOnly}    │
├─────────────────────────────────┤
│ + guardar(): Boolean            │
│ + validar(): Boolean            │
│ + generarSlug(): String         │
└─────────────────────────────────┘
```

![large](06-158_IMG03.png)

#### **Representación de características**

- **Sección de atributos** - Muestra propiedades estructurales
- **Sección de operaciones** - Muestra características comportamentales
- **Indicadores de visibilidad** - Muestran niveles de acceso
- **Especificaciones de tipo** - Definen tipos de datos y restricciones

---

### 5.2 Diagramas de Objetos

Los diagramas de objetos muestran instancias específicas con valores de propiedad reales:

```
┌─────────────────────────────────┐
│       miTema: Tema              │
├─────────────────────────────────┤
│ titulo = "Características UML"  │
│ slug = "caracteristicas-uml"    │
│ fechaCreacion = 2024-01-15      │
│ fechaActualizacion = 2024-01-20 │
└─────────────────────────────────┘
```

#### **Valores de propiedades**

- **Valores concretos** en lugar de tipos
- **Datos específicos de instancia**
- **Representación de estado en tiempo de ejecución**


---

### 5.3 Diagramas de Componentes

Los componentes exponen características a través de interfaces:

```
┌─────────────────────────────┐
│      ServicioUsuario        │
├─────────────────────────────┤
│ ○ IRepositorioUsuario       │
│ ○ IServicioEmail            │
├─────────────────────────────┤
│ + crearUsuario()            │
│ + validarEmail()            │
│ + enviarBienvenida()        │
└─────────────────────────────┘
```

#### **Características de componentes**

- **Interfaces requeridas** - Dependencias en características externas
- **Interfaces proporcionadas** - Características ofrecidas a otros componentes
- **Propiedades internas** - Configuración y estado del componente

---
### 5.4 Diagramas de Paquetes

Los paquetes organizan características en grupos lógicos:

```
┌─────────────────────────────┐
│        Dominio              │
├─────────────────────────────┤
│ + Usuario                   │
│ + Pedido                    │
│ + Producto                  │
├─────────────────────────────┤
│ + RepositorioUsuario        │
│ + ServicioPedido            │
│ + CatalogoProducto          │
└─────────────────────────────┘
```

#### **Características de paquetes**

- **Elementos contenidos** - Clases, interfaces, otros paquetes
- **Reglas de visibilidad** - Qué características son accesibles fuera del paquete
- **Gestión de espacio de nombres** - Alcance y organización de nombres de características


---


### 5.5 Otras Aplicaciones de Diagramas

#### **Diagramas de actividad**

- **Propiedades de actividad** - Duración, recursos, restricciones
- **Características de nodos de objeto** - Especificaciones de estado, transformaciones


#### **Diagramas de casos de uso**

- **Propiedades de actores** - Roles, responsabilidades, capacidades
- **Características de casos de uso** - Precondiciones, postcondiciones, escenarios


#### **Diagramas de secuencia**

- **Propiedades de línea de vida** - Estados de objeto, creación/destrucción
- **Características de mensajes** - Parámetros, valores de retorno, restricciones de temporización

---


## ***6. Especificación y Documentación de Atributos***
---
### 6.1 Estándares de Nomenclatura de Atributos

#### **Directrices de nomenclatura**

- **Usar nombres descriptivos** - `nombreCliente` no `nc`
- **Seguir convenciones de mayúsculas** - `camelCase` para la mayoría de lenguajes
- **Evitar abreviaciones** - `direccion` no `dir`
- **Usar frases nominales** - `fechaPedido` no `fechaDelPedido`
- **Ser consistente** - Los mismos conceptos usan los mismos nombres

#### **Patrones comunes de nomenclatura**

| Patrón                     | Ejemplo                                         | Uso                     |
| -------------------------- | ----------------------------------------------- | ----------------------- |
| **Sustantivos simples**    | `nombre`, `precio`, `cantidad`                  | Propiedades básicas     |
| **Sustantivos compuestos** | `primerNombre`, `precioUnitario`, `fechaPedido` | Propiedades específicas |
| **Banderas booleanas**     | `estaActivo`, `tieneHijos`, `puedeEditar`       | Propiedades de estado   |
| **Colecciones**            | `elementos`, `pedidos`, `hijos`                 | Propiedades multi-valor |

---
### 6.2 Especificaciones de Tipos de Datos

#### **Tipos primitivos**

- `String` - Datos de texto
- `Integer` - Números enteros
- `Real` - Números decimales
- `Boolean` - Valores verdadero/falso
- `Date` - Fechas de calendario
- `DateTime` - Fecha con hora
- `Time` - Hora sin fecha

#### **Tipos personalizados**

- `Money` - Cantidades de moneda con precisión
- `EmailAddress` - Strings de email validados
- `PhoneNumber` - Números de teléfono formateados
- `URL` - Direcciones web
- `UUID` - Identificadores únicos

#### **Tipos de colección**

- `Array[Tipo]` - Colección ordenada de tamaño fijo
- `List[Tipo]` - Colección ordenada de tamaño variable
- `Set[Tipo]` - Colección de valores únicos
- `Map[TipoLlave, TipoValor]` - Pares llave-valor

---

### 6.3 Multiplicidad y Restricciones

#### **Especificación de multiplicidad**

```
Cliente
+ nombre: String [1]           // Valor único requerido
+ apodo: String [0..1]         // Valor único opcional
+ numerosTelefono: String [1..*] // Al menos uno requerido
+ etiquetas: String [*]        // Cero o más permitidos
+ preferencias: String [3..5]   // Entre 3 y 5 valores
```

#### **Ejemplos de restricciones**

```
Producto
+ precio: Money [1] {precio > 0}
+ categorias: Categoria [1..*] {ordered}
+ reseñas: Reseña [*] {readOnly}
+ /calificacionPromedio: Real {derived}
```


---
### 6.4 Valores por Defecto e Inicialización

#### **Sintaxis de valores por defecto**

```
Usuario
+ estado: String = "activo"
+ conteoLogin: Integer = 0
+ fechaRegistro: Date = hoy()
+ preferencias: Map = vacio()
```

#### **Estrategias de inicialización**

- **Valores literales** - Asignación directa de valores
- **Inicialización de constructor** - Valores establecidos durante creación de objeto
- **Métodos factory** - Inicialización a través de métodos especializados
- **Inyección de dependencias** - Valores proporcionados por sistemas externos

---


## ***7. Visibilidad y Control de Acceso***
---

### 7.1   Modificadores de Visibilidad

UML define **CUATRO** niveles estándar de visibilidad que controlan el acceso a las características:

| Modificador | Símbolo     | Nombre    | Nivel de Acceso                         |
| ----------- | ----------- | --------- | --------------------------------------- |
| `+`         | Más         | Público   | Accesible desde cualquier lugar         |
| `-`         | Menos       | Privado   | Solo dentro del elemento propietario    |
| `#`         | Almohadilla | Protegido | Dentro del elemento y sus descendientes |
| `~`         | Virgulilla  | Paquete   | Dentro del mismo paquete                |

---
### 7.2 Acceso Público, Privado y Protegido

#### **Características públicas (`+`):**

```
Cliente
+ nombre: String              // Cualquiera puede acceder
+ email: String              // Sistemas externos pueden leer/escribir
+ obtenerNombreCompleto(): String    // Operación pública
```

**Uso:** Interfaces API, comunicación externa, contratos públicos


#### **Características privadas (`-`):**

```
Cliente
- id: UUID                   // Identificador interno solamente
- hashContrasena: String     // Protección de datos sensibles
- validarContrasena(): Boolean  // Validación interna
```

**Uso:** Detalles de implementación interna, datos sensibles, métodos auxiliares



#### **Características protegidas (`#`):**

```
Persona
# fechaNacimiento: Date      // Accesible a subclases
# calcularEdad(): Integer    // Comportamiento heredado
```

**Uso:** Jerarquías de herencia, patrones de método plantilla, comportamiento compartido



### 7.3 Visibilidad de Paquete e Implementación

#### **Visibilidad de paquete (`~`):**

```
ProcesadorPedido
~ registroAuditoria: List[String]   // Registro interno del paquete
~ validarPedido(): Boolean          // Validación interna del paquete
```

**Uso:** Colaboración interna del paquete, límites de framework

##### **Visibilidad específica de implementación**

- **Clases friend** (C++) - Privilegios de acceso a clase específica
- **Internal** (C#) - Visibilidad a nivel de ensamblado
- **Default** (Java) - Acceso privado al paquete


---
### 7.4 Principios de Encapsulación

#### **Beneficios de encapsulación**

- **Ocultación de datos** - Detalles internos protegidos del acceso externo
- **Estabilidad de interfaz** - Las interfaces públicas permanecen consistentes
- **Flexibilidad de implementación** - Los cambios internos no afectan a los clientes
- **Seguridad** - Datos y operaciones sensibles protegidos

#### **Buenas  Prácticas**

- **Minimizar interfaz pública** - Exponer solo lo necesario
- **Usar privado por defecto** - Hacer características públicas solo cuando sea necesario
- **Proteger invariantes** - Usar características privadas para mantener consistencia del objeto
- **Diseñar pensando en el continuo cambio** - Mantener detalles de implementación privados para flexibilidad

---


## ***8. Operaciones y Características Comportamentales***
---

### 8.1 Definiciones de Métodos

Las operaciones definen las capacidades comportamentales de los elementos. Especifican qué acciones puede realizar un elemento.

##### **Sintaxis de operación**

```
[visibilidad] nombre ([lista-parámetros]) [: tipo-retorno] [modificadores-propiedad]
```

#### **Ejemplos**

```
Cliente
+ obtenerNombre(): String
+ establecerEmail(email: String): void
+ calcularDescuento(montopedido: Money): Money
+ validarCuenta(): Boolean {query}
- encriptarContrasena(contrasena: String): String
```

---

### 8.2 Firmas de Operaciones

#### **Especificaciones de parámetros**

```
ServicioPedido
+ crearPedido(
    cliente: Cliente,
    elementos: ElementoPedido [1..*],
    direccionEnvio: Direccion [0..1] = null,
    prioridad: Prioridad = normal
  ): Pedido
```

#### **Direcciones de parámetros**

- **in** - Parámetro de entrada (por defecto)
- **out** - Parámetro de salida (valor de retorno)
- **inout** - Tanto entrada como salida
- **return** - Valor de retorno del método

---
### 8.3 Especificaciones de Parámetros

#### **Propiedades de parámetros**

```
ServicioPago
+ procesarPago(
    in monto: Money,
    in metodo: MetodoPago,
    out idTransaccion: String,
    inout recibo: Recibo [0..1]
  ): ResultadoPago
```

#### **Restricciones de parámetros**

- **Multiplicidad** - Número de valores de parámetro
- **Valores por defecto** - Usados cuando el parámetro no se proporciona
- **Restricciones de tipo** - Reglas de validación adicionales
- **Navegabilidad/Dirección** - Cómo se usa el parámetro en la operación


---
### 8.4 Tipos de Retorno y Excepciones

#### **Especificaciones de tipo de retorno**

```
ServicioUsuario
+ encontrarUsuario(id: UUID): Usuario [0..1]      // Retorno opcional
+ obtenerTodosUsuarios(): Usuario [*]             // Retorno de colección
+ validarUsuario(usuario: Usuario): Boolean       // Retorno simple
+ /obtenerConteoUsuarios(): Integer {query}       // Consulta derivada
```

#### **Especificaciones de Excepciones**

```
ServicioArchivo
+ leerArchivo(ruta: String): String 
    {exceptions: ArchivoNoEncontradoException, ExcepcionSeguridad}
+ escribirArchivo(ruta: String, contenido: String): void
    {exceptions: IOException, ExcepcionSeguridad}
```

---


## ***9. Conceptos Avanzados de Características***
---
### 9.1 Características Estáticas vs de Instancia

#### **Características de instancia** - Pertenecen a instancias individuales de objeto:

```
CuentaBancaria
+ saldo: Money                    // Cada cuenta tiene su propio saldo
+ depositar(monto: Money): void   // Operación en cuenta específica
```

#### **Características estáticas** - Pertenecen a la clase misma, compartidas entre todas las instancias:

```
CuentaBancaria
+ tasaInteres: Real {static}         // Misma tasa para todas las cuentas
+ calcularInteres(): Money {static}  // Operación a nivel de clase
```

**Representación visual:** Las características estáticas están **subrayadas** en diagramas UML

---
### 9.2 Características Abstractas y Virtuales

### **Características abstractas** - Declaradas pero no implementadas en la clase actual:

```
Forma {abstract}
+ /area(): Real {abstract}           // Debe ser implementado por subclases
+ /perimetro(): Real {abstract}      // Operación abstracta
```

#### **Características virtuales** - Pueden ser sobrescritas por subclases:

```
Vehiculo
+ encenderMotor(): void {virtual}    // Implementación por defecto proporcionada
+ apagarMotor(): void {virtual}      // Puede ser personalizado por subclases
```

---

### 9.3 Propiedades Derivadas

**Las propiedades derivadas** se calculan desde otras propiedades:

```
Persona
+ primerNombre: String
+ apellido: String
+ /nombreCompleto: String {derived}     // Calculado desde primerNombre + apellido

Pedido
+ elementos: ElementoPedido [1..*]
+ /montoTotal: Money {derived}          // Suma de todos los precios de elementos
+ /conteoElementos: Integer {derived}   // Número de elementos
```

#### **Reglas de derivación**

- **Cálculo** - Cómo se calcula el valor
- **Dependencias** - Qué propiedades afectan el valor derivado
- **Caché** - Si los valores calculados se almacenan o calculan bajo demanda
- **Disparadores de actualización** - Cuándo los valores derivados necesitan recálculo


---

### 9.4 Redefinición de Características y Herencia

#### **Herencia de características**

```
Animal
+ nombre: String
+ hacerSonido(): String {abstract}

Perro extends Animal
+ raza: String                        // Propiedad adicional
+ hacerSonido(): String               // Operación redefinida
```

#### **Tipos de redefinición**

- **Override** - Reemplazar completamente la implementación padre
- **Extend** - Añadir comportamiento a la implementación padre
- **Restrict** - Estrechar el contrato (ej., tipo de retorno más específico)
- **Specialize** - Proporcionar implementación concreta de característica abstracta

---


## ***10. Mejores Prácticas y Directrices***
---
### 10.1 Estándares de Convenciones de Nomenclatura

#### **Nomenclatura de atributos**

- **Usar nombres claros y descriptivos** - `emailCliente` no `ec`
- **Seguir convenciones del lenguaje** - `camelCase` en Java, `snake_case` en Python
- **Usar prefijos/sufijos significativos** - `estaActivo`, `tienePermiso`, `conteoElementos`
- **Evitar jerga técnica** - Preferir terminología del dominio de negocio
- **Ser consistente a través del modelo** - Los mismos conceptos usan los mismos nombres

#### **Nomenclatura de operaciones**

- **Usar frases verbales** - `calcularTotal()`, `validarEntrada()`
- **Operaciones de consulta** - Empezar con `obtener`, `encontrar`, `es`, `tiene`
- **Operaciones de comando** - Empezar con verbos de acción `crear`, `actualizar`, `eliminar`
- **Retornos booleanos** - Usar prefijos `es`, `tiene`, `puede`

---
### 10.2 Estrategias para Documentación

#### **Niveles de documentación de características**

1. **Documentación de nombres** - Nombres claros y auto-documentados
2. **Documentación de tipos** - Especificaciones precisas de tipos
3. **Documentación de restricciones** - Reglas de multiplicidad y validación
4. **Documentación de comentarios** - Aclaración adicional cuando sea necesario
5. **Documentación externa** - Especificaciones detalladas en documentos separados

#### **Plantillas de documentación**

```
Cliente
+ email: String [1] {unique}      // Email de contacto principal
  // Debe ser formato de email válido, usado para notificaciones
+ pedidos: Pedido [*] {ordered}   // Historial de compras
  // Ordenado por fecha de creación, incluye todos los estados de pedido
```


---
### 10.3 Directrices para Colaboración en Equipo

#### **Estableciendo estándares**

- **Crear guías de nomenclatura** - Documentar convenciones del equipo
- **Usar revisión de código** - Hacer cumplir consistencia a través de revisión por pares
- **Proporcionar ejemplos** - Mostrar buenas y malas prácticas de nomenclatura
- **Refactorización regular** - Actualizar nombres conforme mejora la comprensión
- **Soporte de herramientas** - Usar herramientas UML que fuercen consistencia

#### **Prácticas de comunicación**

- **Glosarios de características** - Definiciones de terminología compartida
- **Revisiones regulares de modelo** - Validación en equipo de diseños de características
- **Entrenamiento cruzado** - Asegurar que miembros del equipo entiendan convenciones
- **Actualizaciones de documentación** - Mantener estándares actuales con la práctica


---

### 10.4 Prácticas de Aseguramiento de Calidad

#### **Verificaciones de calidad de características**

- **Consistencia de nomenclatura** - Los mismos conceptos usan los mismos nombres
- **Precisión de tipos** - Tipos de datos correctos para uso previsto
- **Completitud de restricciones** - Todas las reglas de negocio capturadas
- **Apropiada visibilidad** - Niveles apropiados de encapsulación
- **Adecuación de documentación** - Suficiente aclaración proporcionada

#### **Métricas de calidad**

- **Cobertura de características** - Porcentaje de características con documentación apropiada
- **Cumplimiento de nomenclatura** - Adherencia a convenciones establecidas
- **Seguridad de tipos** - Especificaciones correctas de tipos y restricciones
- **Estabilidad de interfaz** - Cambios a características públicas a lo largo del tiempo

---


## ***11. Errores Comunes y Anti-Patrones***
---
### 11.1 Problemas de Nomenclatura Inconsistente

#### **Inconsistencias comunes**

```
// NOPE!!!!: Múltiples estilos de nomenclatura en el mismo modelo

Usuario
+ nombreUsuario: String      // camelCase
+ email_usuario: String      // snake_case  
+ TelefonoUsuario: String    // PascalCase
+ dir: String               // abreviación
```

```
// PERFECT!!!: Nomenclatura consistente en todo


Usuario
+ nombre: String
+ email: String
+ numeroTelefono: String
+ direccion: String
```

#### **Problemas detectados**

- **Confusión del desarrollador** - No está claro qué estilo seguir
- **Dificultad de mantenimiento** - Más difícil encontrar y actualizar características
- **Problemas de generación de código** - Salida inconsistente de herramientas UML
- **Fricción del equipo** - Argumentos sobre nomenclatura "correcta"


---

### 11.2 Problemas de Sobre-Especificación

#### **Modelos sobre-detallados**

```
// NOPE!!!: Demasiado detalle de implementación en UML


ConexionBaseDatos
- cadenaConexion: String
- tamanoMaxPool: Integer = 10
- tamanoMinPool: Integer = 2
- tiempoEsperaConexion: Integer = 30000
- tiempoEsperaComando: Integer = 30000
- conteoReintentos: Integer = 3
- retrasoReintento: Integer = 1000
- habilitarSsl: Boolean = true
- protocoloSsl: String = "TLS 1.2"
```

#### **Problemas**

- **Complejidad del modelo** - Detalle abrumador oscurece conceptos importantes
- **Carga de mantenimiento** - Cada cambio de implementación requiere actualizaciones del modelo
- **Acoplamiento de implementación** - UML se vuelve demasiado atado a tecnología específica
- **Flexibilidad reducida** - Sobre-especificación restringe opciones de implementación


---

### 11.3 Mal Uso de Visibilidad

#### **Errores comunes de visibilidad**

```
// NOPE!!!!: Todo público


Cliente
+ id: UUID                          // Debería ser privado
+ hashContrasena: String            // Debería ser privado
+ notasInternas: String             // Debería ser privado
+ calcularPuntuacionRiesgo(): Integer  // Debería ser privado
```

```
// NOP!!!: Todo privado


Cliente
- nombre: String                    // Debería ser público
- email: String                     // Debería ser público
- obtenerInfoContacto(): String     // Debería ser público
```

#### **Consecuencias**

- **Vulnerabilidades de seguridad** - Datos sensibles expuestos
- **Violaciones de encapsulación** - Detalles internos filtrados
- **Inestabilidad de interfaz** - Cambios internos rompen clientes
- **Problemas de usabilidad** - Características requeridas no accesibles


---


### 11.4 Descuido de Documentación

#### **Características mal documentadas**

```
// NOPE!!!!: Propósito y restricciones poco claros

Pedido
+ datos: String                     // ¿Qué tipo de datos?
+ procesar(): Boolean               // ¿Qué hace esto?
+ x: Integer                       // Nombre sin significado
+ cosas: Object [*]                // Tipo y propósito vagos
```

#### **Problemas**

- **Confusión de implementación** - Desarrolladores adivinan el propósito de características
- **Dificultades de integración** - Otros sistemas no saben cómo usar características
- **Desafíos de pruebas** - No está claro qué comportamiento probar
- **Problemas de mantenimiento** - Desarrolladores futuros no pueden entender la intención

---


## ***12. Herramientas y Soporte de Implementación***
---
### 12.1 Herramientas de Modelado UML

#### **Herramientas de modelado empresarial**

- **Enterprise Architect** - Especificación y validación comprehensiva de características
- **MagicDraw/Cameo** - Modelado avanzado de restricciones de propiedades
- **Visual Paradigm** - Definición y documentación rica en características de propiedades
- **IBM Rational Software Architect** - Integración con entornos de desarrollo

#### **Herramientas de modelado ligeras**

- UMLetino - UML basado en web/VSCode, opensource.
- **Lucidchart** - UML basado en web con soporte básico de características
- **Draw.io/Diagrams.net** - Modelado UML en línea gratuito
- **PlantUML** - Generación UML basada en texto
- **Gliffy** - Diagramación simple con plantillas UML

---

### 12.2 Características de Generación de Código

#### **Capacidades de ingeniería  directa de software**

```
// Definición de Clase UML

Cliente
+ nombre: String
+ email: String
+ calcularDescuento(): Money




// Código Java Auto-Generado

public class Cliente {
    private String nombre;
    private String email;

    public String getNombre() { return nombre; }
    public void setNombre(String nombre) { this.nombre = nombre; }

    public String getEmail() { return email; }
    public void setEmail(String email) { this.email = email; }

    public Money calcularDescuento() {
        // Implementación por añadir
        return null;
    }
}
```

#### **Beneficios de generación de código**

- **Consistencia** - El código generado sigue especificaciones UML exactamente
- **Velocidad** - Generación rápida de esqueleto desde modelos
- **Precisión** - Reduce errores de codificación manual
- **Sincronización** - Mantiene código y modelos alineados


---
### 12.3 Capacidades de Ingeniería Inversa

#### **Extracción de código-a-UML**

- **Descubrimiento automático de características** - Extraer propiedades y operaciones de código existente
- **Inferencia de relaciones** - Identificar dependencias y asociaciones
- **Generación de documentación** - Crear modelos UML desde comentarios de código
- **Modelado de sistemas heredados** - Entender sistemas existentes a través de ingeniería inversa

#### **Lenguajes soportados**

- **Lenguajes orientados a objetos** - Java, C#, C++, Python
- **Lenguajes funcionales** - Soporte limitado para Scala, F#
- **Esquemas de base de datos** - Extraer modelos de entidad desde estructuras de base de datos
- **Servicios web** - Generar modelos desde definiciones de API

---

### 12.4 Generación de Documentación

#### **Tipos de documentación generada**

- **Documentación HTML** - Especificaciones de características navegables en web
- **Reportes PDF** - Documentación de modelo imprimible
- **Documentos Word** - Documentos de especificación editables
- **Integración wiki** - Generación automática de páginas wiki desde modelos


#### **Contenido de documentación**

- **Catálogos de características** - Listas completas de todas las propiedades y operaciones
- **Tablas de referencias cruzadas** - Donde se usan características a través del modelo

---