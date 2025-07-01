|Guía|Título|
|---|---|
|06-152|Introducción a los Componentes UML y Elementos Comunes|
|06-153|Componentes UML Comunes: Marcos (Frames)|
|06-154|Componentes UML Comunes: Clasificadores (Classifiers)|
|06-155|Componentes UML Comunes: Estereotipos (Stereotypes)|
|06-156|Componentes UML Comunes: Comentarios y Notas|
|**06-157**|**Componentes UML Comunes: Dependencias (Dependencies)**|
|06-158|Componentes UML Comunes: Características y Propiedades|
|06-159|Cuestionario: Introducción a UML|

---

# 06-157: UML      DEPENDENCIAS

---

### 1. Qué Son las Dependencias

- **1.1** Definición y Conceptos Fundamentales
- **1.2** El Papel del Acoplamiento en el Diseño de Software
- **1.3** Las Dependencias como Indicadores de Arquitectura del Sistema

### 2. Entendiendo el Acoplamiento

- **2.1** Fundamentos del Acoplamiento
- **2.2** Tipos de Acoplamiento
- **2.3** Evaluación de la Fuerza del Acoplamiento
- **2.4** Impacto en la Mantenibilidad del Sistema

### 3. Representación Visual y Notación

- **3.1** Notación UML Estándar
- **3.2** Dirección de la Flecha y Significado
- **3.3** Estilos de Línea y Variaciones
- **3.4** Dependencias con Estereotipos

### 4. Tipos de Dependencias UML

- **4.1** Dependencias de Uso
- **4.2** Dependencias de Abstracción
- **4.3** Dependencias de Permiso
- **4.4** Dependencias de Realización
- **4.5** Dependencias de Sustitución

### 5. Aplicaciones de Dependencias en Diagramas

- **5.1** Diagramas de Clases
- **5.2** Diagramas de Componentes
- **5.3** Diagramas de Paquetes
- **5.4** Diagramas de Despliegue
- **5.5** Diagramas de Casos de Uso

### 6. Ejemplos Prácticos y Estudios de Caso

- **6.1** Dependencias de Integración de API
- **6.2** Dependencias de Bibliotecas y Frameworks
- **6.3** Dependencias de Conexión a Base de Datos
- **6.4** Dependencias de Capa de Servicio

### 7. Análisis y Gestión de Dependencias

- **7.1** Identificación de Dependencias Críticas
- **7.2** Evaluación del Impacto de Dependencias
- **7.3** Reducción del Acoplamiento Innecesario
- **7.4** Estrategias de Refactorización

### 8. Mejores Prácticas y Patrones de Diseño

- **8.1** Principio de Inversión de Dependencias
- **8.2** Estrategias de Acoplamiento Débil
- **8.3** Dependencias Basadas en Interfaces
- **8.4** Patrones de Inyección de Dependencias

### 9. Anti-Patrones y Errores Comunes

- **9.1** Dependencias Circulares
- **9.2** Problemas de Sobre-Acoplamiento
- **9.3** Dependencias Ocultas
- **9.4** Problemas de Dependencias Transitivas

### 10. Herramientas y Técnicas para la Gestión de Dependencias

- **10.1** Herramientas de Análisis Estático
- **10.2** Visualización de Dependencias
- **10.3** Métodos de Análisis de Impacto
- **10.4** Seguimiento Automatizado de Dependencias

---


## _**1. Qué Son las Dependencias**_
---

### 1.1 Definición y Conceptos Fundamentales

Una **dependencia** UML es una relación que indica que un elemento (por ejemplo, "el cliente") depende de otro elemento ("el proveedor") para su funcionamiento adecuado.

Las dependencias **representan la forma más fundamental de relación en UML**, denotando que los cambios en el proveedor pueden afectar al cliente.

La esencia de las dependencias radica en:

* #### Acoplamiento
- ##### El grado en que un componente necesita otro componente para funcionar correctamente. 


Entender las dependencias es crucial para:

- **Definir y Comprender la arquitectura del sistema**
- **Análisis de impacto** durante cambios
- **Evaluación de riesgos** para modificaciones
- **Planificación de mantenimiento** y asignación de recursos

![large](./06-157_IMG1.png)

---

### 1.2 El Papel del Acoplamiento en el Diseño de Software

El acoplamiento describe la **interdependencia entre módulos o componentes de software**. En las dependencias UML:

- #### **Alto acoplamiento** = Dependencia fuerte, difícil de modificar independientemente
    
- #### **Bajo acoplamiento** = Dependencia débil, más fácil de mantener y modificar
    
- #### **Sin acoplamiento** = Componentes independientes, máxima flexibilidad
    

El objetivo en el diseño de software es típicamente lograr **bajo acoplamiento** **mientras se mantienen las relaciones funcionales necesarias**.

---

### 1.3 Las Dependencias como Indicadores de Arquitectura del Sistema

Las dependencias sirven como indicadores arquitectónicos que revelan:

- **Rutas críticas del sistema** que no pueden romperse
- **Puntos únicos de fallo** que podrían colapsar el sistema
- **Complejidad de integración** entre componentes
- **Dependencias de pruebas** y secuencias de prueba requeridas
- **Requisitos de orden de despliegue** para componentes del sistema

---


## _**2. Entendiendo el Acoplamiento**_
---

### 2.1 Fundamentos del Acoplamiento

El acoplamiento en sistemas de software se manifiesta a través de varios mecanismos:

- **Acoplamiento de datos** - Los componentes comparten estructuras de datos
- **Acoplamiento de control** - Un componente controla la ejecución de otro
- **Acoplamiento común** - Los componentes comparten datos globales
- **Acoplamiento de contenido** - Un componente modifica los datos internos de otro
- **Acoplamiento de mensaje** - Los componentes se comunican a través de interfaces bien definidas

---

### 2.2 Tipos de Acoplamiento

|Tipo de Acoplamiento|Fuerza|Descripción|Representación UML|
|---|---|---|---|
|**Datos**|Baja|Solo paso de parámetros|Dependencia simple|
|**Sello**|Baja-Media|Compartir estructura de datos|Dependencia con estereotipo|
|**Control**|Media|Dependencia de flujo de control|Dependencia con estereotipo de control|
|**Común**|Alta|Compartir datos globales|Múltiples dependencias a elemento común|
|**Contenido**|Muy Alta|Acceso a estructura interna|Relación de dependencia fuerte|

---

### 2.3 Evaluación de la Fuerza del Acoplamiento

Factores que determinan la fuerza del acoplamiento:

- **Número de puntos de conexión** entre componentes
- **Tipo de datos compartidos** (primitivos vs. complejos)
- **Frecuencia de interacción** entre componentes
- **Grado de conocimiento** que un componente tiene sobre otro
- **Estabilidad de la interfaz** entre componentes

---

### 2.4 Impacto en la Mantenibilidad del Sistema

El **acoplamiento fuerte impacta negativamente** en:

- **Modificabilidad** - Los cambios se propagan a través de componentes dependientes
- **Capacidad de prueba** - Difícil probar componentes de forma aislada
- **Reutilización** - Los componentes fuertemente acoplados no pueden reutilizarse fácilmente
- **Comprensibilidad** - Las interdependencias complejas oscurecen el comportamiento del sistema

---


## _**3. Representación Visual y Notación**_
---

### 3.1 Notación UML Estándar

Las dependencias se representan por:

```
Cliente -----> Proveedor
(línea discontinua con punta de flecha abierta)
```

![large](./06-157_IMG2.png)

#### **Elementos visuales**

- **Estilo de línea**: Línea discontinua o punteada
- **Punta de flecha**: Triángulo abierto apuntando al proveedor
- **Dirección**: Del cliente (dependiente) al proveedor (objetivo de dependencia)
- **Etiquetas opcionales**: Nombre de dependencia o estereotipo

---

### 3.2 Dirección de la Flecha y Significado

La dirección de la flecha es crucial para entender la relación de dependencia:

```
A -----> B
```

#### **Interpretación**: "A depende de B"

- A es el **cliente** (el elemento dependiente)
- B es el **proveedor** (el elemento del cual se depende)
- Los cambios en B pueden afectar a A
- A no puede funcionar apropiadamente sin B

---

### 3.3 Estilos de Línea y Variaciones

Diferentes estilos de línea pueden indicar características de dependencia:

- **Línea discontinua estándar** - Dependencia general
- **Línea punteada con estereotipo** - Tipo específico de dependencia
- **Líneas coloreadas** - Indicación de prioridad o categoría (específico de herramienta)
- **Variaciones gruesas/delgadas** - Indicación de fuerza (específico de herramienta)

---

### 3.4 Dependencias con Estereotipos

Estereotipos comunes de dependencias incluyen:

- **«use»** - El cliente usa servicios del proveedor
- **«call»** - El cliente llama operaciones en el proveedor
- **«create»** - El cliente crea instancias del proveedor
- **«import»** - El cliente importa el espacio de nombres del proveedor
- **«access»** - El cliente accede a características públicas del proveedor
- **«instantiate»** - El cliente crea instancias de la clase proveedor

---

## _**4. Tipos de Dependencias UML**_
---

### 4.1 Dependencias de Uso

**Las dependencias de uso** indican que **un elemento requiere otro** para su implementación u operación.

```
Controlador -----> Servicio
«use»
```

#### **Características**

- Tipo de dependencia más común
- Indica dependencia operacional
- A menudo representa llamadas a métodos o uso de servicios

---

### 4.2 Dependencias de Abstracción

**Las dependencias de abstracción** **relacionan elementos en diferentes niveles de abstracción.**

#### **Subtipos**

- **«derive»** - Elemento derivado calculado desde la fuente
- **«trace»** - Correspondencia informal entre elementos
- **«refine»** - Elemento refinado añade detalle a la fuente

---

### 4.3 Dependencias de Permisos

**Las dependencias de permiso** **otorgan derechos de acceso a elementos.**

#### **Subtipos**

- **«access»** - Acceso a características públicas
- **«import»** - Importación de espacio de nombres
- **«friend»** - Privilegios de acceso especiales (concepto de C++)

---

### 4.4 Dependencias de Realización

**Las dependencias de realización** indican relaciones de implementación.

```
ClaseConcreta -----> Interfaz
«realize»
```

**Uso:** Clases implementando interfaces o componentes realizando especificaciones

---

### 4.5 Dependencias de Sustitución

**Las dependencias de sustitución** indican que **un elemento puede ser sustituido** por otro.

```
SubClase -----> SuperClase
«substitute»
```

**Uso:** Relaciones polimórficas e implementaciones de patrones de diseño

---


## _**5. Aplicaciones de Dependencias en Diagramas**_
---

### 5.1 Diagramas de Clases

En diagramas de clases, las dependencias representan:

- **Tipos de parámetros de métodos** usados por una clase
- **Tipos de variables locales** dentro de métodos
- **Tipos de excepciones** lanzadas por métodos
- **Uso de clases utilitarias** para operaciones

#### **Ejemplo**

```
┌─────────────────┐     «use»      ┌─────────────────┐
│ ProcesadorPedido│ ────────────>  │ ServicioPago    │
├─────────────────┤                ├─────────────────┤
│ + procesarPedido│                │ + cobrar()      │
|                 |                │ + reembolsar()  │
└─────────────────┘                └─────────────────┘
```

---

### 5.2 Diagramas de Componentes

Las dependencias de componentes muestran:

- **Consumo de servicios** entre componentes
- **Requisitos de uso de interfaces**
- **Dependencias de bibliotecas** para funcionalidad
- **Requisitos de frameworks** para operación

---

### 5.3 Diagramas de Paquetes

Las dependencias de paquetes indican:

- **Relaciones de importación** entre paquetes
- **Permisos de acceso** a través de límites de paquetes
- **Dependencias de compilación** en procesos de construcción
- **Requisitos de secuencia de despliegue**

---

### 5.4 Diagramas de Despliegue

Las dependencias de despliegue representan:

- **Requisitos de hardware** para componentes de software
- **Necesidades de conectividad de red** entre nodos
- **Dependencias de servicios** a través de unidades de despliegue
- **Requisitos de infraestructura** para aplicaciones

---

### 5.5 Diagramas de Casos de Uso

Las dependencias de casos de uso muestran:

- **Relaciones «include»** para sub-casos de uso obligatorios
- **Relaciones «extend»** para extensiones opcionales
- **Dependencias de actores** en capacidades del sistema
- **Requisitos de cruce de límites del sistema**

---


## _**6. Ejemplos Prácticos Casos de Uso**_
---

### 6.1 Dependencias de Integración de API

#### Sistema de Solicitud de Música con Integración de Spotify

_Este patrón de dependencia demuestra los desafíos de la integración de API externa y la importancia de diseñar sistemas resistentes y débilmente acoplados que puedan manejar fallos de servicios externos con elegancia._

```
                    ┌─────────────────────┐
                    │   App Cliente       │
                    │   (Reproductor)     │
                    └─────────────────────┘
                             │
                             │ «envía»
                             ▼
┌─────────────────────┐               ┌─────────────────────┐
│   SolicitudCancion  │ ─────────────>│   SpotifyAPI        │
├─────────────────────┤    «use»      ├─────────────────────┤
│ - titulo: String    │               │ + autenticar()      │
│ - artista: String   │               │ + buscar(consulta)  │
│ - duracion: Integer │               │ + obtenerPista(id)  │
│ - idSolicitud: UUID │               │ + obtenerAlbum(id)  │
├─────────────────────┤               │ + añadirACola(id)   │
│ + enviar()          │               │ + obtenerPlaylists()│
│ + validar()         │               │ + crearPlaylist()   │
│ + aConsultaSpotify()│               └─────────────────────┘
│ + reintentar()      │                         │
└─────────────────────┘                         │ «depende de»
            │                                   ▼
            │ «respaldo»               ┌─────────────────────┐
            ▼                          │   Servicio Spotify  │
┌─────────────────────┐                ├─────────────────────┤
│  APIAlternativa     │                │ - Web API           │
├─────────────────────┤                │ - Autenticación     │
│ + buscarYouTube()   │                │ - Límite de Tasa    │
│ + buscarAppleMusic()│                │ - Manejo de Errores │
│ + buscarLocal()     │                └─────────────────────┘
└─────────────────────┘
```

### Análisis de Dependencias

**SolicitudCancion no puede funcionar sin SpotifyAPI** - esto crea riesgos críticos de dependencia:

|Factor de Riesgo|Nivel de Impacto|Estrategia de Mitigación|
|---|---|---|
|**Caída de API**|Alto|Implementar servicios de respaldo|
|**Límite de Tasa**|Medio|Añadir cola de solicitudes y limitación|
|**Cambios de Esquema**|Alto|Usar patrón adaptador y versionado|
|**Autenticación**|Crítico|Implementar renovación de token y auth backup|

### Evaluación de Acoplamiento

#### **Indicadores de Acoplamiento Fuerte:**

- Llamadas directas a métodos de API en lógica de negocio
- Formatos de datos específicos de Spotify en clases principales
- Sin capa de abstracción entre solicitud y servicio externo
- Fallo inmediato cuando la API no está disponible

#### **Estrategias de Desacoplamiento Recomendadas**

1. **Abstracción de Interfaz**

```
Interfaz ServicioMusica
├── ServicioSpotify (primario)
├── ServicioAppleMusic (respaldo)
└── ServicioYouTube (respaldo)
```

2. **Patrón Adaptador**

```
SolicitudCancion → AdaptadorMusica → [SpotifyAPI | APIAlternativa]
```

3. **Patrón Circuit Breaker**

```
SolicitudCancion → CircuitBreaker → SpotifyAPI
```

### Diseño de Arquitectura Mejorada

#### **Problemas con el Diseño Actual:**

- **Punto Único de Fallo**: Sin mecanismos de respaldo
- **Dependencia de Proveedor**: Implementación específica de Spotify
- **Propagación de Errores**: Los fallos de API rompen todo el flujo de solicitud
- **Complejidad de Pruebas**: No se puede hacer pruebas unitarias sin API externa

#### **Beneficios del Diseño Mejorado:**

- **Resistencia**: Múltiples proveedores de servicios de música
- **Flexibilidad**: Fácil añadir nuevos servicios de música
- **Capacidad de Prueba**: Interfaces simuladas para pruebas unitarias
- **Mantenibilidad**: Cambios aislados a adaptadores específicos

### Recomendaciones de Implementación

#### **Acciones Inmediatas**

1. Extraer interfaz `IServicioMusica`
2. Implementar lógica de reintento con retroceso exponencial
3. Añadir manejo de errores y registro comprehensivo
4. Crear servicio simulado para pruebas

#### **Mejoras a Largo Plazo**

1. Implementar múltiples proveedores de servicios de música
2. Añadir monitoreo de salud de servicios
3. Implementar caché de solicitudes para contenido accedido frecuentemente
4. Crear mecanismo de descubrimiento de servicios


---

### 6.2 Dependencias de Bibliotecas y Frameworks

_Este patrón ilustra cómo las aplicaciones modernas dependen de frameworks y bibliotecas, mostrando tanto los beneficios del desarrollo rápido como las consideraciones arquitectónicas para manejar dependencias externas._

```
                    ┌─────────────────────┐
                    │   Componentes de    │
                    │   Aplicación        │
                    └─────────────────────┘
                             │
                             │ «depende de»
                             ▼
┌────────────────────────┐               ┌─────────────────────┐
│   WebController        │ ─────────────>│  Framework Spring   │
├────────────────────────┤   «import»    ├─────────────────────┤
│ @RestController        │               │ @RestController     │
│ @RequestMapping        │               │ @RequestMapping     │
│                        │               │ @GetMapping         │
│ + obtenerUsuarioPorId()│               │ @PostMapping        │
│ + crearUsuario()       │               │ ResponseEntity<T>   │
│ + actualizarUsuario()  │               │ RequestBody         │
│ + eliminarUsuario()    │               │ PathVariable        │
└────────────────────────┘               └─────────────────────┘
            │                                    │
            │ «uses»                             │ «proporciona»
            ▼                                    ▼
┌─────────────────────┐               ┌───────────────────────┐
│   ServicioUsuario   │ ─────────────>│  Spring Core          │
├─────────────────────┤   «inject»    ├───────────────────────┤
│ @Service            │               │ @Component            │
│ @Autowired          │               │ @Service              │
│                     │               │ @Repository           │
│ + encontrarUsuario()│               │ ApplicationContext    │
│ + guardarUsuario()  │               │ BeanFactory           │
└─────────────────────┘               │ Inyección Dependencias│
            │                         └───────────────────────┘
            │ «uses»                            │
            ▼                                   │ «construido sobre»
┌─────────────────────┐                       ▼
│   Biblioteca Externa│               ┌─────────────────────┐
├─────────────────────┤               │   Plataforma Java   │
│ Jackson JSON        │               ├─────────────────────┤
│ Hibernate ORM       │               │ JVM Runtime         │
│ Apache Commons      │               │ Bibliotecas Estándar│
│ SLF4J Logging       │               │ API Reflection      │
└─────────────────────┘               └─────────────────────┘
```

### Capas de Dependencias de Framework

#### **Dependencias de Capa de Aplicación:**

- **WebController** → **Spring MVC** (Anotaciones y utilidades de tier web)
- **ServicioUsuario** → **Spring Core** (Inyección de dependencias y gestión de ciclo de vida)
- **Bibliotecas Externas** → **Funcionalidades específicas** (JSON, ORM, logging)

### Análisis de Dependencias

|Componente|Framework/Biblioteca|Tipo de Dependencia|Nivel de Acoplamiento|
|---|---|---|---|
|**Controller**|Spring MVC|Basado en anotaciones|Medio|
|**Service**|Spring Core|Basado en inyección|Bajo|
|**Capa de Datos**|Hibernate|Basado en interfaz|Medio|
|**Utilidades**|Apache Commons|Llamadas a métodos|Alto|

### Beneficios vs Compromisos del Framework

#### **Beneficios**

- **Desarrollo Rápido**: Componentes y patrones pre-construidos
- **Convención sobre Configuración**: Código repetitivo reducido
- **Integración de Ecosistema**: Bibliotecas y herramientas compatibles
- **Soporte de Comunidad**: Documentación y mejores prácticas

#### **Compromisos**

- **Dependencia de Framework**: Complejidad de migración aumenta
- **Curva de Aprendizaje**: Conocimiento específico del framework requerido
- **Dependencias de Versiones**: Restricciones de compatibilidad
- **Sobrecarga de Rendimiento**: Capas adicionales de abstracción

#### Estrategias de Gestión de Dependencias

1. **Abstracción de Interfaz**: Minimizar acoplamiento directo de framework
2. **Patrón Facade**: Envolver funcionalidad específica del framework
3. **Externalización de Configuración**: Reducir dependencias codificadas
4. **Arquitectura Modular**: Aislar dependencias de framework por capa

---

### 6.3 Dependencias de Conexión a Base de Datos

_Este patrón demuestra cómo el patrón repository gestiona dependencias de base de datos mientras mantiene acoplamiento débil a través de abstracción de interfaz._

```
                    ┌─────────────────────┐
                    │   Capa de           │
                    │   Aplicación        │
                    └─────────────────────┘
                             │
                             │ «depende de»
                             ▼
┌──────────────────────┐               ┌─────────────────────┐
│   RepositorioUsuario │ ─────────────>│  ControladorBD      │
├──────────────────────┤    «use»      ├─────────────────────┤
│ + encontrarPorId(id) │               │ + conectar()        │
│ + encontrarPorEmail()│               │ + ejecutarConsulta()│
│ + guardar(usuario)   │               │ + ejecutarActualiz()│
│ + actualizar(usuario)│               │ + iniciarTransaccion│
│ + eliminar(id)       │               │ + confirmar()       │
│ + encontrarTodos()   │               │ + deshacer()        │
└──────────────────────┘               │ + desconectar()     │
            │                          └─────────────────────┘
            │ «implements»                        │
            ▼                                     │ «abstrae»
┌──────────────────────┐                          ▼
│   IRepositorioUsuario│               ┌──────────────────────┐
├──────────────────────┤               │  Pool de Conexiones  │
│ + encontrarPorId(id) │               ├──────────────────────┤
│ + guardar(usuario)   │               │ + obtenerConexion()  │
│ + eliminar(id)       │               │ + liberarConexion()  │
└──────────────────────┘               │ + obtenerConteoActivo│
                                       └──────────────────────┘
```

### Análisis de Dependencias

#### **Implementación del Patrón Repository:**

- **RepositorioUsuario** depende de **ControladorBD** para persistencia de datos
- **Abstracción de interfaz** reduce acoplamiento directo a implementaciones específicas de base de datos
- **Pool de conexiones** gestiona eficiencia de recursos de base de datos

### Tipos de Dependencias

|Relación|Tipo|Descripción|
|---|---|---|
|**Repository → Controlador**|Dependencia de Uso|Operaciones de base de datos en tiempo de ejecución|
|**Repository → Interfaz**|Realización|Implementación de contrato|
|**Controlador → Pool**|Abstracción|Capa de gestión de recursos|

### Características de Acoplamiento

**Acoplamiento Fuerte**: Los métodos del repository invocan directamente operaciones del controlador  
**Acoplamiento Débil**: La abstracción de interfaz permite sustitución de controlador  
**Dependencia de Recursos**: El pool de conexiones gestiona recursos compartidos de base de datos

### Beneficios de Este Patrón

- **Capacidad de Prueba**: La interfaz permite implementaciones simuladas
- **Flexibilidad**: Cambio fácil de controlador de base de datos
- **Rendimiento**: El pool de conexiones reduce sobrecarga
- **Mantenibilidad**: Separación clara de responsabilidades

---

### 6.4 Dependencias de Capa de Servicio

_Esta arquitectura de capa de servicio demuestra un patrón típico de dependencias de microservicios donde un orquestador central coordina servicios especializados._

```
                    ┌─────────────────────┐
                    │   ServicioPedido    │
                    ├─────────────────────┤
                    │ + crearPedido()     │
                    │ + validarPedido()   │
                    └─────────────────────┘
                             │
                             │ «orquesta»
                             │
            ┌────────────────┼────────────────┐
            │                │                │
            │ «use»          │ «call»         │ «use»
            ▼                ▼                ▼
┌──────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│ ServicioInventar │ │ ServicioPago    │ │ ServicioNotific │
├──────────────────┤ ├─────────────────┤ ├─────────────────┤
│ + verificarStock │ │ + procesarPago  │ │ + enviarEmail() │
│ + reservarItems()│ │ + validarTarjeta│ │ + enviarSMS()   │
│ + actualizarStock│ │ + reembolsarPago│ │ + registrarActiv│
└──────────────────┘ └─────────────────┘ └─────────────────┘
```

### Relaciones Clave de Dependencias

**ServicioPedido** actúa como el **orquestador** que coordina múltiples servicios:

- **ServicioInventario**: Gestiona validación y reserva de stock
- **ServicioPago**: Maneja procesamiento y validación de pagos
- **ServicioNotificacion**: Gestiona comunicaciones con clientes

### Análisis de Flujo de Dependencias

1. **Flujo Primario**: ServicioPedido → ServicioPago (ruta crítica)
2. **Flujo de Soporte**: ServicioPedido → ServicioInventario (validación)
3. **Flujo de Notificación**: ServicioPedido → ServicioNotificacion (comunicación)

### Evaluación de Acoplamiento

|Servicio|Nivel de Acoplamiento|Justificación|
|---|---|---|
|**Pago**|Alto|Operación crítica de negocio|
|**Inventario**|Medio|Validación de stock requerida|
|**Notificación**|Bajo|Operación no bloqueante|

---


## _**7. Análisis y Gestión de Dependencias**_

---

### 7.1 Identificación de Dependencias Críticas

#### **Indicadores de dependencias críticas**

- **Puntos únicos de fallo** - Componentes sin alternativas
- **Uso de alta frecuencia** - Componentes llamados repetidamente
- **Dependencias entre límites** - Dependencias que cruzan capas arquitectónicas
- **Dependencias de servicios externos** - Integraciones de servicios de terceros

#### **Técnicas de análisis**

- **Mapeo de dependencias** - Representación visual de todas las dependencias
- **Análisis de impacto** - Evaluación de efectos en cascada de cambios
- **Puntuación de criticidad** - Clasificación de dependencias por importancia
- **Análisis de modos de fallo** - Identificación de escenarios potenciales de fallo

---

### 7.2 Evaluación del Impacto de Dependencias

#### **Criterios de evaluación**

- **Frecuencia de cambio** de componentes proveedores
- **Estabilidad** de interfaces proveedoras
- **Número de clientes** afectados por cambios del proveedor
- **Costo de modificación** cuando las dependencias se rompen
- **Opciones alternativas** disponibles para reemplazo

#### **Niveles de impacto**

- **Alto impacto** - Dependencias críticas para la misión sin alternativas
- **Impacto medio** - Dependencias importantes con soluciones alternativas difíciles
- **Bajo impacto** - Dependencias de conveniencia con alternativas fáciles

---

### 7.3 Reducción del Acoplamiento Innecesario

#### **Estrategias para reducción de acoplamiento**

1. **Abstracción de interfaz** - Depender de interfaces, no de implementaciones
2. **Inyección de dependencias** - Externalizar la creación de dependencias
3. **Arquitectura dirigida por eventos** - Reemplazar llamadas directas con eventos
4. **Abstracción de servicios** - Usar capas de servicio para ocultar detalles de implementación
5. **Externalización de configuración** - Mover dependencias a configuración

### 7.4 Estrategias de Refactorización

#### **Patrones comunes de refactorización**

- **Extraer Interfaz** - Crear abstracciones para dependencias concretas
- **Introducir Capa de Servicio** - Añadir indirección entre componentes
- **Reemplazar Herencia con Delegación** - Reducir acoplamiento a través de composición
- **Mover Método** - Reubicar funcionalidad para reducir dependencias
- **Extraer Componente** - Separar responsabilidades para minimizar acoplamiento

---


## _**8. Buenas Prácticas  -  Patrones de Diseño**_
---

### 8.1 Principio de Inversión de Dependencias

#### **Declaración del principio:** "Depende de abstracciones, no de concreciones"

#### **Implementación**

```
┌─────────────────┐     «use»      ┌──────────────────┐
│ ModuloAltoNivel │ ────────────>  │ <<interface>>    │
│                 │                │ ServicioAbstracto│
└─────────────────┘                └──────────────────┘
                                           ▲
                                           │ «implement»
                                           │
                                   ┌─────────────────┐
                                   │ ServicioConcreto│
                                   └─────────────────┘
```

---

### 8.2 Estrategias de Acoplamiento Débil

#### **Enfoques de diseño**

1. **Patrón Publicar-Suscribir** - Desacoplar productores de consumidores
2. **Patrón Mediador** - Centralizar interacciones de componentes
3. **Patrón Observador** - Minimizar dependencias directas entre objetos
4. **Patrón Factory** - Desacoplar creación de objetos del uso
5. **Patrón Strategy** - Hacer algoritmos intercambiables

---

### 8.3 Dependencias Basadas en Interfaces

#### **Beneficios**

- **Flexibilidad** - Fácil intercambio de implementaciones
- **Capacidad de prueba** - Simple crear dobles de prueba
- **Mantenibilidad** - Cambios aislados a implementaciones
- **Extensibilidad** - Nuevas implementaciones sin cambios en clientes

#### **Patrón de implementación**

```
┌───────────────┐             ┌──────────────────┐      ┌─────────────────┐
│     Cliente   │ ───────────>│ <<interface>>    │      │ Implementación  │
│               │    «use»    │ ServicioAbstracto│      │ Concreta        │
└───────────────┘             └──────────────────┘      └─────────────────┘
                                      ▲                        │
                                      │       «realize»        │
                                      └────────────────────────┘
```

---

### 8.4 Patrones de Inyección de Dependencias

#### **Tipos comunes de inyección**

- **Inyección por constructor** - Dependencias proporcionadas durante creación de objeto
- **Inyección por propiedad** - Dependencias establecidas a través de propiedades públicas
- **Inyección por interfaz** - Dependencias proporcionadas a través de interfaces específicas
- **Localizador de servicios** - Dependencias recuperadas desde registro central

---

## _**9. Anti-Patrones y Errores Comunes**_
---

### 9.1 Dependencias Circulares

**Problema:** Dos o más componentes dependen entre sí directa o indirectamente

```
┌─────┐      ┌─────┐      ┌─────┐
│  A  │ ────>│  B  │ ────>│  C  │
│     │      │     │      │     │
└─────┘      └─────┘      └─────┘
   ▲                        │
   │                        │
   └────────────────────────┘
```

#### **Soluciones**

- **Extracción de interfaz** - Romper ciclos con abstracciones
- **Introducción de mediador** - Componente central de coordinación
- **Reestructuración de dependencias** - Reorganizar responsabilidades

---

### 9.2 Problemas de Sobre-Acoplamiento

#### **Síntomas**

- **Cirugía de escopeta** - Cambios pequeños requieren muchas modificaciones
- **Sistemas frágiles** - Cambios menores causan fallos inesperados
- **Dificultades de prueba** - No se pueden probar componentes de forma aislada
- **Complejidad de despliegue** - Debe desplegar múltiples componentes juntos

#### **Prevención**

- **Análisis regular de acoplamiento** - Monitorear crecimiento de dependencias
- **Revisiones arquitectónicas** - Evaluar acoplamiento en decisiones de diseño
- **Disciplina de refactorización** - Mejorar continuamente niveles de acoplamiento

---

### 9.3 Dependencias Ocultas

#### **Fuentes comunes**

- **Variables globales** - Dependencias implícitas a través de estado compartido
- **Singletons** - Dependencias ocultas a través de acceso global
- **Métodos estáticos** - Uso directo sin declaración explícita
- **Magia de framework** - Dependencias creadas por frameworks

#### **Estrategias de detección**

- **Herramientas de análisis estático** - Descubrimiento automatizado de dependencias
- **Revisiones de código** - Inspección manual para dependencias ocultas
- **Aislamiento de pruebas** - Identificar dependencias a través de fallos de prueba

---

### 9.4 Problemas de Dependencias Transitivas

#### **Problemas**

- **Conflictos de versiones** - Diferentes versiones de la misma dependencia
- **Despliegues hinchados** - Dependencias innecesarias incluidas
- **Vulnerabilidades de seguridad** - Dependencias desconocidas con problemas
- **Complicaciones de licencias** - Requisitos de licencia conflictivos

#### **Enfoques de gestión**

- **Herramientas de análisis de dependencias** - Mapear dependencias transitivas
- **Gestión de versiones** - Controlar versiones de dependencias explícitamente
- **Auditorías regulares** - Revisar y limpiar dependencias
- **Principio de dependencia mínima** - Solo incluir dependencias necesarias

---

## _**10. Herramientas y Técnicas para la Gestión de Dependencias**_

---

### 10.1 _Herramientas de Análisis Estático_

#### **Herramientas de análisis de código**

- **SonarQube** - Análisis de dependencias y métricas de acoplamiento
- **NDepend** - Análisis y visualización de dependencias .NET
- **JDepend** - Análisis de dependencias de paquetes Java
- **Dependency Cruiser** - Análisis de dependencias JavaScript/TypeScript

#### **Herramientas UML con análisis de dependencias**

- **Enterprise Architect** - Modelado comprehensivo de dependencias
- **Visual Paradigm** - Análisis de impacto de dependencias
- **MagicDraw** - Características avanzadas de gestión de dependencias

---

### 10.2 _Visualización de Dependencias_

#### **Técnicas de visualización**

- **Grafos de dependencias** - Representaciones de nodos y aristas
- **Matrices de dependencias** - Relaciones de dependencia tabulares
- **Diagramas por capas** - Dependencias de capas arquitectónicas
- **Estructuras de árbol** - Vistas jerárquicas de dependencias

#### **Herramientas de visualización**

- **Graphviz** - Motor de visualización de grafos
- **D3.js** - Visualizaciones interactivas de dependencias
- **Gephi** - Análisis y visualización de redes
- **yEd** - Edición profesional y análisis de grafos

---

### 10.3 _Métodos de Análisis de Impacto_

#### **Enfoques de análisis**

- **Impacto hacia adelante** - ¿Qué afecta este componente?
- **Impacto hacia atrás** - ¿Qué afecta a este componente?
- **Impacto de cambio** - ¿Qué cambia cuando esto se modifica?
- **Impacto de fallo** - ¿Qué falla si este componente falla?

#### **Herramientas de análisis de impacto**

- **Lattix** - Análisis de arquitectura y dependencias
- **Structure101** - Matrices de estructura de dependencias
- **CAST** - Inteligencia de aplicación y análisis de impacto

---

### 10.4 _Seguimiento Automatizado de Dependencias_

#### **Capacidades de seguimiento**

- **Análisis en tiempo de construcción** - Dependencias identificadas durante compilación
- **Monitoreo en tiempo de ejecución** - Descubrimiento dinámico de dependencias
- **Seguimiento de versiones** - Cambios de versión de dependencias a lo largo del tiempo
- **Analíticas de uso** - Frecuencia y patrones de uso de dependencias

#### **Herramientas de implementación**

- **Maven/Gradle** - Gestión de dependencias en tiempo de construcción
- **NPM/Yarn** - Seguimiento de dependencias JavaScript
- **NuGet** - Gestión de dependencias de paquetes .NET
- **Pip/Poetry** - Gestión de dependencias Python

---