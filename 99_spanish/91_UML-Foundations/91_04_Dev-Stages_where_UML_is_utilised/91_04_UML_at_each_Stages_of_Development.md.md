|Guía|Título|
|---|---|
|07-187|La Importancia del Análisis y Diseño de Sistemas|
|07-188|Visión General de los Sistemas de Software|

|Guía|Título|
|---|---|
|06-150|Visión General de UML|
|**06-151**|**Etapas de Desarrollo donde se Utiliza UML**|

---

# **06-151: Etapas de Desarrollo donde UML es utilizado

1. Integrando UML con el Ciclo de Vida del Desarrollo
    
2. Mapeo de Tipos de Diagramas a Fases de Desarrollo
    
    - **Fase 1: Pre-Desarrollo**
        
        - Diagramas de Actividad
        - Diagramas de Despliegue

    - **Fase 2: Desarrollo Activo**
        
        - Diagramas de Clases
        - Diagramas de Casos de Uso

    - **Fase 3: Post-Desarrollo y Mantenimiento**
        
        - Diagramas de Secuencia
        - Diagramas de Paquetes

3. Aplicación Estratégica de UML
    

---

## 1. **Ciclo de Vida del Desarrollo e Integración de UML**

Los diagramas UML pueden emplearse estratégicamente a lo largo de todo el ciclo de vida del desarrollo de software.

Cada fase se beneficia de tipos específicos de diagramas que abordan desafíos y requerimientos particulares.

---

## **2. Visión General de las Fases de Desarrollo**

```
* **Fase 1: Pre-Desarrollo**
    * Diagramas de Actividad
    * Diagramas de Despliegue

* **Fase 2: Desarrollo Activo**
    * Diagramas de Clases
    * Diagramas de Casos de Uso

* **Fase 3: Post-Desarrollo y Mantenimiento**
    * Diagramas de Secuencia
    * Diagramas de Paquetes
```

---

## _**Fase 1: Planificación Pre-Desarrollo**_

Antes de escribir una sola línea de código, UML ayuda a establecer una hoja de ruta clara y arquitectura para tu aplicación.



### Diagramas Utilizados en la Fase de Pre-Desarrollo
---

## A) Diagramas de Actividad

![](./06-151_IMG1.png)

### **Cuándo Usar**

Cuando necesites entender el **flujo de la aplicación** e **interacciones del usuario**.

### **Propósito**

- Mapear el flujo secuencial de actividades.
- Definir puntos de decisión y rutas alternativas.
- Descomponer procesos complejos en pasos manejables.
- Visualizar el viaje del usuario a través de la aplicación.

### **Escenario de Ejemplo**

> Planificar un sistema de registro de usuario, desde registro inicial y verificación de email hasta activación de cuenta.

### **Beneficios**

- Clarifica funcionalidad antes de implementación.
- Identifica potenciales cuellos de botella o puntos de decisión complejos.
- Proporciona una referencia clara para desarrolladores y stakeholders.

---

## B) Diagramas de Despliegue

![](./06-151_IMG2.png)

### **Cuándo Usar**

Cuando **diseñes arquitectura del sistema** e **infraestructura**.

### **Propósito**

- Definir la arquitectura del sistema de alto nivel.
- Especificar el stack tecnológico y relaciones de componentes.
- Planificar configuraciones de servidor y estrategias de despliegue.
- Visualizar cómo diferentes componentes del sistema se comunicarán.

### **Escenario de Ejemplo**

> Planificar una aplicación web con un front-end de JavaScript/React/Angular, un back-end de API REST, y un servidor de base de datos, incluyendo configuraciones específicas.

### **Beneficios**

- Previene errores arquitectónicos temprano en el desarrollo.
- Ayuda a estimar costos y requerimientos de infraestructura.
- Facilita comunicación con DevOps y administradores de sistemas.
- Sirve como blueprint para procedimientos de despliegue.

---


## _**Fase 2: Desarrollo Activo**_

Durante el desarrollo, UML ayuda a mantener organización y asegurar mejores prácticas mientras se construye el sistema.


### Diagramas Utilizados en la Fase de Desarrollo Activo
---

## C) Diagramas de Clases

![Class Diagram Example](./06-151_IMG3.png)

### **Cuándo Usar**

Cuando **diseñes esquemas de base de datos** y **relaciones de objetos**.

### **Propósito**

- Modelar relaciones de tablas de base de datos.
- Asegurar normalización apropiada de base de datos.
- Definir propiedades y métodos de objetos.
- Visualizar relaciones de herencia y composición.

### **Escenario de Ejemplo**

> Diseñar una base de datos de comercio electrónico con entidades `Usuario`, `Producto`, `Orden`, y `Pago` y sus relaciones.

### **Beneficios**

- Promueve diseño organizado de base de datos.
- Ayuda a identificar redundancia y oportunidades de optimización.
- Sirve como documentación para la estructura de base de datos.
- Facilita generación de código y mapeo ORM.

---

## D) Diagramas de Casos de Uso

![Use Case Diagram Example](./06-151_IMG4.png)

### **Cuándo Usar**

Cuando construyas **sistemas de autorización** y defines **roles de usuario**.

### **Propósito**

- Definir roles de usuario y permisos.
- Organizar funcionalidades del sistema por tipo de usuario.
- Documentar niveles de acceso a características.
- Planificar requerimientos de autorización y autenticación.

### **Escenario de Ejemplo**

> Definir diferentes niveles de acceso para roles de Admin, Manager, y Cliente en una aplicación de negocios.

### **Beneficios**

- Proporciona una hoja de ruta clara de autorización.
- Facilita comunicación con stakeholders no técnicos.
- Ayuda a prevenir descuidos de seguridad.
- Sirve como lista de verificación de requerimientos.


---

## _**Fase 3: Post-Desarrollo / Mantenimiento**_

Después de que el sistema está construido, UML continúa proporcionando valor **para mantenimiento, optimización, incorporación de nuevas funciones, cuando nuevos miembros entran a formar parte del equipo.**

### Diagramas Utilizados en la Fase de Post-Desarrollo / Mantenimiento

---

## E) Diagramas de Secuencia

![Sequence Diagrams Example](./06-151_IMG5.png)

### **Cuándo Usar**

Cuando agregues **características avanzadas** o **refactorices código existente**.

### **Propósito**

- Visualizar flujo interno de mensajes del sistema.
- Analizar interacciones de métodos y dependencias.
- Identificar oportunidades de optimización.
- Debuggear comportamientos complejos del sistema.

### **Escenario de Ejemplo**

> Entender el flujo de mensajes en un sistema de procesamiento de pagos para agregar nuevos métodos de pago o solucionar fallas de transacciones.

### **Beneficios**

- Revela ineficiencias del sistema.
- Ayuda a mantener calidad del código durante modificaciones.
- Facilita debugging de interacciones complejas.
- Documenta comportamiento del sistema para referencia futura.

---

## F) Diagramas de Paquetes

![Package Diagrams Example](./06-151_IMG6.png)

### **Cuándo Usar**

Cuando **organices arquitectura de código** o **planifiques modularmente**.

### **Propósito**

- Visualizar organización de código y dependencias.
- Identificar oportunidades para reducir acoplamiento.
- Planificar extracción de bibliotecas de código.
- Documentar estructura del sistema para nuevos miembros del equipo.

### **Escenario de Ejemplo**

> Analizar una aplicación monolítica para identificar componentes que podrían extraerse en micro-servicios o bibliotecas separadas.

### **Beneficios**

- Mejora mantenibilidad del código.
- Facilita incorporación del equipo.
- Identifica oportunidades de refactorización.
- Documenta decisiones de arquitectura.

---


## **3. Pautas de Aplicación Estratégica**
---

### Cuándo Elegir Cuál Diagrama 

Mientras que cualquier diagrama UML puede técnicamente usarse en cualquier etapa de desarrollo, **la selección estratégica basada en tus necesidades actuales y fase maximizará la efectividad.**

### Recomendaciones de Diagramas por Fase de Desarrollo

| Fase de Desarrollo  | Desafío Principal                | Diagramas Recomendados       | Opciones Secundarias |
| ------------------- | -------------------------------- | ---------------------------- | -------------------- |
| _Pre-Desarrollo_    | Entender Requerimientos          | **Actividad, Casos de Uso**  | Secuencia, Clases    |
| _Pre-Desarrollo_    | Planificación de Arquitectura    | **Despliegue, Paquetes**     | Componentes          |
| _Desarrollo Activo_ | Modelado de Datos                | **Clases, Entidad-Relación** | Paquetes             |
| _Desarrollo Activo_ | Planificación de Características | **Casos de Uso, Actividad**  | Secuencia            |
| _Post-Desarrollo_   | Optimización de Rendimiento      | **Secuencia, Actividad**     | Paquetes             |
| _Post-Desarrollo_   | Organización de Código           | **Paquetes, Componentes**    | Clases               |

---

## **Buenas Prácticas**

> 🎨 Piensa en tus **diagramas como un lienzo dinámico** para tu proyecto.

1. ### **Comienza Simple, Crece Inteligentemente**
    
    Siempre comienza con **diagramas de alto nivel** para establecer el panorama general. No te atasques en detalles intrincados muy temprano; puedes agregar esas capas conforme tu entendimiento se solidifique.
    
2. ### **Abraza la Iteración, Mantente Ágil**
    
    Recuerda, los diagramas son **documentos vivos**. Actualízalos regularmente conforme tu sistema evoluciona y los requerimientos cambian. Piénsalo como refinar un boceto hasta que sea una obra maestra.
    
3. ### **Colabora, Comunica, Conquista**
    
    Usa los diagramas como tu **herramienta central de comunicación**. Son fantásticos para generar discusiones, alinear tu equipo, y fomentar un entendimiento compartido entre todos los stakeholders.
    
4. ### **Documenta Decisiones, Preserva Sabiduría**
    
    ¡No solo dibujes! Incluye el **razonamiento detrás de tus eleccionesde arquitectura  diseño** directamente dentro o junto a tus diagramas. Este contexto es invaluable para referencia futura y nuevos miembros del equipo.
    
5. ### **Mantente Actualizado, Permanece Relevante**
    
    Esto es crucial: **asegúrate de que tus diagramas estén siempre sincronizados con tu código**. Los diagramas desactualizados pueden llevar a confusión y mala dirección, haciéndolos más dañinos que útiles.
    

---

## Estrategia de Implementación Práctica

---

### Listas de Verificación para Comenzar

#### **Antes de Cualquier Proyecto**

- [ ] Crear un **Diagrama de Actividad** para entender flujos centrales del usuario.
- [ ] Diseñar un **Diagrama de Despliegue** para planificación inicial de arquitectura.
- [ ] **Revisar y validar** estos diagramas iniciales con todos los stakeholders clave.

#### **Durante el Desarrollo**

- [ ] Construir **Diagramas de Clases** para modelado detallado de datos.
- [ ] Crear **Diagramas de Casos de Uso** para organizar características y funcionalidades.
- [ ] **Actualizar diagramas** prontamente conforme los requerimientos evolucionan o emergen nuevos sistemas/herramientas/etc.

#### **Después del Desarrollo Inicial / Para Mantenimiento**

- [ ] Documentar interacciones complejas con **Diagramas de Secuencia**.
- [ ] Organizar tu arquitectura de código usando **Diagramas de Paquetes**.
- [ ] Planificar futuras mejoras seleccionando los **tipos de diagrama apropiados** para la tarea.

---

## **Errores Comunes**

#### ⚠️  Ten cuidado con estos errores comunes que pueden tirar por la borda tus esfuerzos de análisis, diseño e implementación

1. ### **La Falacia de "Más es Más" (Sobre-Documentación)**
    
    No caigas en la trampa de crear diagramas solo por completitud. Enfócate en diagramas que **agreguen valor real**, clarifiquen problemas específicos, o ayuden al entendimiento. ¡Calidad sobre cantidad, siempre!
    
2. ### **El Síndrome del "Boceto Viejo" (Diagramas Desactualizados)**
    
    Este es un error crítico: diagramas que no reflejan el estado actual de tu código llevan a **confusión y desconfianza**. Haz una prioridad mantener tus diagramas **sincronizados** con cada cambio de código. ¡Un mapa desactualizado es peor que no tener mapa!
    
3. ### **El Error de "Talla Única" (Selección Incorrecta de Herramienta)**
    
    Resiste la urgencia de usar el mismo diagrama para cada problema. Diferentes tipos de diagramas sirven **propósitos diferentes**. Elige el que **mejor aborde tus necesidades actuales** y comunique claramente la información requerida.
    
4. ### **La Trampa del "Lobo Solitario" (Aislamiento)**
    
    Nunca crees diagramas en el vacío. **¡La colaboración es clave!**
    Involucra a un equipo, a buenos contactos, líderes, personas intelectualmente de tu respeto, a lo largo de todo proceso de diagramación.   
    Su input asegura precisión, fomenta entendimiento compartido, y construye propiedad colectiva.
