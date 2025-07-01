|Guía|Título|
|---|---|
|06-152|Introducción a los Componentes UML y Elementos Comunes|
|06-153|Componentes UML Comunes: Marcos (Frames)|
|06-154|Componentes UML Comunes: Clasificadores (Classifiers)|
|06-155|Componentes UML Comunes: Estereotipos (Stereotypes)|
|**06-156**|**Componentes UML Comunes: Comentarios y Notas**|
|06-157|Componentes UML Comunes: Dependencias (Dependencies)|
|06-158|Componentes UML Comunes: Características y Propiedades|
|06-159|Cuestionario: Introducción a UML|

---

# 06-156: UML   COMENTARIOS - NOTAS

### 1. Qué son los Comentarios y las Notas

- **1.1** Definición y Propósito
- **1.2** Variaciones de Terminología
- **1.3** Papel en la Documentación UML

### 2. Características y Propiedades

- **2.1** Representación Visual
- **2.2** Métodos de Conexión
- **2.3** Flexibilidad de Contenido

### 3. Comentarios vs Estereotipos

- **3.1** Niveles de Formalidad
- **3.2** Distinciones de Casos de Uso
- **3.3** Diferencias Semánticas

### 4. Escenarios de Aplicación

- **4.1** Comunicación entre Desarrolladores
- **4.2** Aclaración para Partes Interesadas (Stakeholders)
- **4.3** Documentación Técnica

### 5. Elementos Visuales y Notación

- **5.1** Notación Estándar
- **5.2** Líneas de Conexión
- **5.3** Directrices de Posicionamiento

### 6. Ejemplos Prácticos

- **6.1** Aplicaciones en Diagramas de Clases
- **6.2** Aclaración de Atributos
- **6.3** Documentación de Métodos

### 7. Directrices de Implementación

- **7.1** Cuándo Usar Comentarios
- **7.2** Mejores Prácticas de Contenido
- **7.3** Estrategias de Colocación

### 8. Mejores Prácticas y Consejos

- **8.1** Escribir Comentarios Efectivos
- **8.2** Evitar la Sobredocumentación
- **8.3** Consideraciones de Mantenimiento

---

## _**1. Qué son los Comentarios y las Notas**_
---

![large](06-156_IMG1.png)

### 1.1 Definición y Propósito

Los Comentarios UML (también denominados **Notas**) son **elementos de documentación suplementaria que proporcionan marcado descriptivo dentro de los diagramas UML**.

Sirven como _**puente entre la notación formal UML y la explicación en lenguaje natural,**_ permitiendo una comunicación más clara de la intención de diseño y los detalles de implementación.

Los comentarios son anotaciones **no estandarizadas**, no regladas por UML, por lo que pueden contener prácticamente cualquier texto descriptivo, convirtiéndolos en herramientas altamente flexibles para mejorar la legibilidad y comprensión de los diagramas.

---

### 1.2 Variaciones de Terminología

La terminología utilizada para estos elementos puede variar dependiendo del contexto y las herramientas:

- **Comentarios** - Más comúnmente utilizado en contextos de desarrollo de software
- **Notas** - A menudo preferido en documentación académica y formal
- **Anotaciones** - A veces utilizado en herramientas UML especializadas
- **Observaciones** - Ocasionalmente encontrado en documentación heredada (legacy)

Tanto "Comentarios" como "Notas" se refieren al mismo concepto-construcción UML y  se acepta que se usen de manera intercambiable.

---

### 1.3 Papel en la Documentación UML

Los comentarios cumplen múltiples funciones críticas en el modelado UML:

- **Aclaración** de elementos complejos o ambiguos
- **Provisión de contexto** para partes interesadas no técnicas
- **Guía de implementación** para equipos de desarrollo
- **Documentación de reglas de negocio** dentro de diagramas técnicos
- **Registro de suposiciones** para referencia futura

---


## _**2. Características y Propiedades**_
---

### 2.1 Representación Visual

Los Comentarios UML están representados por **cajas rectangulares** con características visuales específicas:

![large](06-156_IMG2.png)

- **Forma**: Rectángulo con una esquina "doblada" (efecto de esquina plegada)
- **Fondo**: Típicamente amarillo o de color claro
- **Borde**: Línea sólida delgada
- **Esquina**: Pequeño pliegue triangular en la esquina superior derecha

### 2.2 Métodos de Conexión

Los comentarios se conectan a los elementos UML a través de:

- **Líneas punteadas** (líneas discontinuas) - El método de conexión estándar
- **Flechas de dependencia** - Utilizadas en algunos casos especializados
- **Posicionamiento directo** - Cuando el contexto hace clara la asociación

### 2.3 Flexibilidad de Contenido

A diferencia de otros elementos UML, los comentarios tienen restricciones mínimas en el contenido:

- **Texto de forma libre** - Sin requisitos de formato específico
- **Múltiples idiomas** - Pueden ser escritos en cualquier lenguaje natural
- **Contenido mixto** - Pueden incluir terminología técnica y de negocio
- **Longitud variable** - Desde anotaciones breves hasta explicaciones detalladas

---


## _**3. Comentarios vs Estereotipos**_
---

### 3.1 Nivel de Formalidad

|Aspecto|Comentarios|Estereotipos|
|---|---|---|
|**Formalidad**|Informal, descriptivo|Formal, estandarizado|
|**Propósito**|Explicación y aclaración|Clasificación y extensión|
|**Contenido**|Texto de forma libre|Palabras clave predefinidas|
|**Uso**|Ayuda de comunicación|Mejora semántica|

---

### 3.2 Comentarios VS Estereotipos

### **Los comentarios son ideales para:**

- Explicar reglas de negocio
- Proporcionar pistas de implementación
- Aclarar relaciones complejas
- Añadir contexto para partes interesadas

### **Los estereotipos son ideales para:**

- Extender el metamodelo UML
- Clasificación formal (ej., «Controller», «Model», «View»)
- Anotaciones específicas de herramientas
- Identificación de patrones arquitectónicos

---

### 3.3 Diferencias Semánticas

- Los **comentarios** no afectan el significado semántico del modelo
- Los **estereotipos** extienden y modifican la interpretación semántica de los elementos
- Los **comentarios** son puramente documentales
- Los **estereotipos** pueden influir en la generación de código y el comportamiento de las herramientas

---


## _4. Escenarios de Aplicación_
---

### 4.1 Comunicación entre Desarrolladores

Los comentarios sobresalen en escenarios donde los desarrolladores necesitan contexto adicional:

- **Explicaciones de algoritmos** para métodos complejos
- **Consideraciones de rendimiento** para operaciones críticas
- **Notas de integración** para interacciones con sistemas externos
- **Advertencias de mantenimiento** para áreas de código sensibles

---

### 4.2 Mejora del contexto

Al presentar diagramas UML a audiencias no técnicas:

- **Explicaciones de procesos de negocio** en diagramas de actividad
- **Aclaraciones de interacción del usuario** en diagramas de casos de uso
- **Descripciones de flujo de datos** en diagramas de secuencia
- **Explicaciones de límites del sistema** en diagramas de despliegue

---

### 4.3 Documentación Técnica

Los comentarios sirven como documentación integrada para:

- **Decisiones de diseño** y su justificación
- **Explicaciones de restricciones** y sus implicaciones
- **Documentación de suposiciones** para referencia futura
- **Enlaces de trazabilidad de requisitos**

---


## _**5. Elementos Visuales y Notación**_
---

### 5.1 Notación Estándar

La especificación UML define elementos visuales específicos para los comentarios:

```
┌─────────────────◣
│ Texto del       │
│ comentario...   │  
└─────────────────┘
```

![large](./06-156_IMG03.png)

**La esquina plegada (◣) es una característica distintiva que identifica inmediatamente el elemento como un comentario.**

---

### 5.2 Líneas de Conexión

Las líneas de conexión entre comentarios y elementos del modelo siguen estas convenciones:

- **Estilo**: Línea discontinua o punteada
- **Dirección**: No se requiere punta de flecha específica
- **Múltiples conexiones**: Un comentario puede conectarse a múltiples elementos
- **Posicionamiento**: Las líneas no deben obscurecer otros elementos del diagrama

---

### 5.3 Directrices de Posicionamiento

La colocación efectiva de comentarios sigue estos principios:

- **Proximidad**: Colocar comentarios cerca de los elementos que describen
- **Claridad**: Evitar superposición con otros elementos del diagrama
- **Legibilidad**: Asegurar que las líneas de conexión sean claras e inequívocas
- **Equilibrio**: Mantener armonía visual dentro del diagrama

---


## _**6. Ejemplos Prácticos**_
---
### 6.1 Aplicaciones en Diagramas de Clases
---

### 6.2 Aclaración de Atributos

Cada comentario en el ejemplo anterior cumple un propósito específico:

1. **Comentario del atributo Title**: Indica regla de negocio (campo requerido)
2. **Comentario del atributo Slug**: Proporciona guía de implementación (auto-generación)
3. **Comentario del atributo TopTen**: Explica funcionalidad del alcance de consulta

---

### 6.3 Documentación de Métodos

**Los comentarios también pueden documentar métodos** y su comportamiento:

```
┌─────────────────┐
│ + authenticate()│ <──┐
└─────────────────┘    │
                       │
┌─────────────────────────◣
│ Implementa OAuth 2.0    │
│ con tokens JWT          │
└─────────────────────────┘
```

---

## _**7. Directrices de Implementación**_

---

### 7.1 Cuándo Usar Comentarios

Los comentarios deben usarse cuando:

- La **notación UML estándar** es insuficiente para la claridad
- Las **reglas de negocio** necesitan documentación explícita
- Los **detalles de implementación** requieren especificación
- Las **partes interesadas no técnicas** necesitan explicación
- Las **relaciones complejas** requieren aclaración

---

### 7.2 Mejores Prácticas de Contenido

El contenido efectivo de comentarios debe ser:

- **Conciso** pero informativo
- **Claro** e inequívoco
- **Relevante** al elemento asociado
- **Actual** y actualizado
- **Consistente** en estilo y terminología

---

### 7.3 Estrategias de Colocación

La colocación estratégica de comentarios involucra:

- **Agrupación lógica** de comentarios relacionados
- **Equilibrio visual** dentro del diagrama
- **Claridad de conexión** para evitar confusión
- **Eficiencia de espacio** para mantener legibilidad
- **Accesibilidad de actualización** para mantenimiento

---

## _**8. Mejores Prácticas y Consejos**_
---

### _8.1 Escribir Comentarios Efectivos_

## 🗿**Cómo Hacerlo**

- Usar lenguaje claro y simple
- Enfocarse en el "por qué" en lugar del "qué"
- Incluir contexto de negocio cuando sea relevante
- Mantener comentarios concisos pero completos
- Usar terminología consistente en todo el documento

## 🙅** Cómo NO Hacerlo**

- Duplicar información ya clara desde el diagrama
- Usar jerga excesivamente técnica sin sentido
- Crear comentarios que rápidamente queden obsoletos
- Saturar diagramas con anotaciones excesivas

---

### 8.2 _Evitar la Sobredocumentación_

Las señales de sobredocumentación incluyen:

- **Información redundante** ya evidente desde el nombrado
- **Detalle excesivo** que obscurece el diagrama principal
- **Explicaciones triviales** de elementos obvios
- **Comentarios obsoletos** que ya no reflejan la realidad

---

### 8.3 _Consideraciones de Mantenimiento_

#### **Proceso de Revisión Habitual**

- Programar revisiones periódicas de comentarios durante actualizaciones de diseño
- Remover comentarios obsoletos prontamente
- Actualizar comentarios cuando cambien los requisitos
- Validar precisión de comentarios con partes interesadas

#### **Control de Versiones**

- Rastrear cambios de comentarios junto con la evolución del diagrama
- Documentar justificación para modificaciones de comentarios
- Mantener historial de comentarios para trazabilidad

#### **Coordinación de Equipo**

- Establecer estándares de escritura de comentarios
- Definir procesos de revisión para adiciones de comentarios
- Asegurar calidad consistente de comentarios entre miembros del equipo

---

### 8.4 _Consideraciones Específicas de Herramientas_

Diferentes herramientas UML pueden tener variaciones en:

- Opciones de **formato de comentarios**
- Estilos de **líneas de conexión**
- **Capacidades de exportación** para comentarios
- **Funcionalidad de búsqueda** dentro de comentarios

---

### 8.5 _Accesibilidad e Internacionalización_

Considerar estos factores para mayor accesibilidad:

- **Consistencia de idioma** dentro de contextos de proyecto
- **Sensibilidad cultural** en explicaciones
- **Precisión de traducción técnica**
- **Compatibilidad con lectores de pantalla** en formatos digitales