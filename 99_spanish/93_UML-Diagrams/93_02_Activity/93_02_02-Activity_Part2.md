#### 3.2 Actividad

| Guía       | Título                                                                      |
| ---------- | --------------------------------------------------------------------------- |
| 06-168     | Elementos de un Diagrama de Actividad UML                                   |
| **06-169** | **Ejemplo: Diagrama de Actividad para un Sistema de Calificación en Línea** |

---

# 06-169: Diagramas de Actividad - Ejemplo de Sistema de Calificación en Línea


1. **Análisis de Arquitectura del Sistema**
   - Visión General del Diagrama y Nomenclatura
   - Organización de Carriles (Swim Lanes) (Swim Lanes)
   - Distribución de Roles y Responsabilidades

1. **Recorrido del Flujo de Proceso**
   - Fase Inicial del Proceso
   - Fase de Procesamiento del Sistema
   - Fase de Interacción del Estudiante
   - Lógica de Decisión y Bucles
   - Fase Final de Aprobación y Almacenamiento

3. **Análisis de Flujo de Actividad**
   - Analogía del Baloncesto para Flujos de Acción
   - Patrones de Flujo de Datos
   - Mecanismos de Transferencia de Control

4. **Patrones de Implementación y Lógica**
   - Implementación de Bucles
   - Condiciones de Guarda
   - Resolución de Ramas

5. **Mejores Prácticas para Diagramas Complejos**



---


## ***1.     Análisis de Arquitectura del Sistema***
---

> **🎯 Enfoque de la Guía:** 
> 
> Esta guía continúa demostrando la ***implementación práctica*** de diagramas de actividad UML, pero a través de un ***ejemplo integral de sistema de calificación en línea***. 
>
> A diferencia del análisis teórico de elementos, esta implementación muestra cómo ***todos los componentes del diagrama de actividad trabajan juntos*** para modelar un proceso de negocio completo de principio a fin.
>
> El enfoque está en entender cómo ***leer, analizar y seguir diagramas de actividad complejos*** en aplicaciones del mundo real, enfatizando el ***flujo lógico de datos y control*** a través de diferentes actores del sistema.


![large](./06-169_IMG1.png)

---
### 🏷️ **Visión General del Diagrama y Nomenclatura Utilizada**

El diagrama de actividad, titulado ***"Quiz"***, establece inmediatamente el ***alcance y propósito*** del proceso modelado.

Esta convención de nomenclatura es crucial para la ***identificación del diagrama*** y ayuda a las partes interesadas a entender el ***flujo de trabajo específico*** que se está representando.


#### 📝 **Principios de Nomenclatura**

- Los títulos de diagramas deben ***indicar claramente*** el alcance del proceso
- Los nombres deben ser ***lo suficientemente específicos*** para distinguirse de procesos relacionados
- La ***identificación clara*** ayuda en la documentación y mantenimiento

---

###  **Organización de Carriles (Swim Lanes)**

El diagrama emplea una ***estructura de Carriles (Swim Lanes) de tres carriles*** que puede orientarse horizontal o verticalmente dependiendo de las restricciones de espacio y preferencias de diseño.

La elección de orientación es ***puramente estética y funcional*** - los arreglos horizontal y vertical son ***equivalentes en significado***.

#### 🏗️ **Estructura de Carriles (Swim Lanes)**

- **Carril del Mentor**: Representa ***responsabilidades del instructor humano***
- **Carril del Sistema**: Representa ***procesos automatizados del sistema***
- **Carril del Estudiante**: Representa ***interacciones del estudiante*** y respuestas

#### 🎨 **Flexibilidad de Diseño**

La orientación de los Carriles (Swim Lanes) (horizontal vs. vertical) depende de:

- ***Espacio disponible en la página*** y restricciones de diseño
- ***Número de actividades*** por carril
- ***Legibilidad del diagrama*** y visualización del flujo
- ***Preferencias de formato*** específicas de herramientas

---

### 👥 **Distribución de Roles y Responsabilidades**

Entender la ***distribución de roles*** es fundamental para el diseño e implementación del sistema. Cada carril de natación define ***límites claros*** de responsabilidad y capacidad.

#### 👨‍🏫 **Responsabilidades del Mentor**

- **Iniciación del Proceso**: ***Asignar Quiz o prueba*** a estudiantes
- **Aprobación Final**: ***Revisar y aprobar*** resultados finales
- **Participación Intermedia Mínima**: Los Mentores tienen ***participación activa limitada*** durante la ejecución del examen

#### 🖥️ **Responsabilidades del Sistema**

- **Generación de Contenido**: ***Generar conjuntos individuales de preguntas***
- **Entrega de Preguntas**: ***Presentar preguntas*** a los estudiantes
- **Procesamiento de Resultados**: ***Calcular y procesar*** resultados
- **Persistencia de Datos**: ***Almacenar resultados finales*** en la base de datos del sistema
- **Orquestación del Proceso**: ***Gestionar el flujo de trabajo general*** y transiciones

#### 👨‍🎓 **Responsabilidades del Estudiante**

- **Confirmación del Proceso**: ***Confirmar participación*** y preparación
- **Respuesta a Preguntas**: ***Responder preguntas presentadas***
- **Control Limitado**: Los estudiantes siguen un ***flujo de trabajo guiado por el sistema*** con acciones autónomas mínimas


> **🏗️ Perspectiva de Arquitectura** 
> 
> Este patrón de distribución revela una ***arquitectura centrada en el sistema*** donde el sistema automatizado maneja la mayor parte del procesamiento complejo, mientras que los actores humanos (Mentor y estudiante) realizan ***tareas específicas y bien definidas***.

---



## ***2.     Recorrido del Flujo de Proceso***
---
### 🚀 **Fase Inicial del Proceso**

El flujo de trabajo comienza en el carril del Mentor con la actividad ***"Asignar Quiz/Prueba"***. Esto representa el ***evento disparador*** que inicia todo el proceso de evaluación.

#### 📋 **Características del Proceso**

- **Punto de Entrada Único**: ***Una condición de inicio clara***
- **Iniciación Específica del Rol**: ***Solo los Mentores*** pueden iniciar el proceso
- **Traspaso al Sistema**: ***Transferencia inmediata*** de control al sistema

---

### ⚙️ **Fase de Procesamiento del Sistema**

Siguiendo la iniciación del Mentor, el control se transfiere al carril del Sistema para ***"Generar Conjunto Individual de Preguntas"***.

Esto representa la ***fase de preparación*** del sistema donde el contenido de evaluación se personaliza o selecciona.

#### 🔧 **Comportamientos del Sistema**

- **Preparación de Contenido**: El sistema prepara ***conjuntos de preguntas personalizadas***
- **Asignación de Recursos**: El sistema asigna ***recursos necesarios*** para la evaluación
- **Preparación de Estado**: El sistema se prepara para ***interacción con el estudiante***

---

### 👨‍🎓 **Fase de Interacción del Estudiante**

El proceso se mueve al carril del Estudiante para la actividad ***"Confirmar"***.   

Esto representa ***autenticación del estudiante***, verificación de preparación, o consentimiento explícito para comenzar la evaluación.

#### ✅ **Lógica de Confirmación del Estudiante**

- **Verificación de Acceso**: El estudiante ***inicia sesión en el sistema***
- **Reconocimiento de Preparación**: El estudiante confirma que está ***listo para comenzar***
- **Compromiso del Proceso**: El estudiante se compromete a ***iniciar la evaluación***

Después de la confirmación, el control regresa al sistema para ***"Hacer Pregunta"***, seguido por transferencia al estudiante para la actividad ***"Responder"***.

---

### 🔄 **Lógica de Decisión y Bucles**

El punto de decisión crítico ocurre después de que el estudiante responde, representado por la rama con la condición de guarda ***"¿Era la última?"***

#### 🌟 **Lógica de Rama**

- **Ruta "No"**: Si ***no es la última pregunta***, el flujo regresa a "Hacer Pregunta" creando un bucle de procesamiento
- **Ruta "Sí"**: Si era ***la última pregunta***, el flujo procede al procesamiento de resultados

#### 🔁 **Implementación de Bucle**

Esto crea un ***patrón iterativo*** donde el sistema continúa haciendo preguntas hasta que todas las preguntas del conjunto se completen. La estructura del bucle demuestra:

- **Iteración Condicional**: El bucle continúa basado en la ***disponibilidad de preguntas***
- **Gestión de Estado**: El sistema ***rastrea el progreso*** a través del conjunto de preguntas
- **Control de Flujo Dinámico**: La ruta del flujo se determina ***en tiempo de ejecución*** basada en el estado actual

---

### ✅ **Fase Final de Aprobación y Almacenamiento**

Cuando se completa la última pregunta, el flujo de trabajo procede a través de:

1. **"Asumir Resultados"** (Sistema): ***Calcular y preparar*** los resultados finales de evaluación
2. **"Aprobar"** (Mentor): El Mentor ***revisa y aprueba*** los resultados calculados
3. **"Almacenar Resultado"** (Sistema): ***Almacenamiento final*** y finalización del proceso

---

## ***3.     Análisis de Flujo de Actividad***
---
### 🏀 **Analogía del Baloncesto para Flujos de Acción**

Los flujos de acción en diagramas de actividad se pueden conceptualizar usando una ***analogía del baloncesto*** donde cada actividad representa un jugador y los flujos de acción representan ***pasar la pelota*** entre jugadores.

![](./06-169_IMG03.png)

#### 🎯 **Características del Flujo**

- **Transferencia de Control**: Cada flujo de acción representa ***pasar el control*** de un actor a otro
- **Procesamiento Secuencial**: Como los pases de baloncesto, los flujos típicamente se mueven en ***secuencia lógica***
- **Traspasos Claros**: Cada transferencia tiene un ***emisor y receptor claros***
- **Continuidad del Proceso**: La "pelota" (control del proceso) ***nunca desaparece***, siempre está en poder de algún actor

#### 📋 **Aplicación Práctica**

- El Mentor ***"pasa"*** al Sistema asignando el examen
- El Sistema ***"pasa"*** al Estudiante solicitando confirmación
- El Estudiante ***"pasa"*** de vuelta al Sistema confirmando preparación
- El Sistema ***"pasa"*** al Estudiante haciendo preguntas
- El Estudiante ***"pasa"*** de vuelta al Sistema proporcionando respuestas

---

### 📊 **Patrones de Flujo de Datos**

El diagrama demuestra varios ***patrones clave de flujo de datos***:

#### 📈 **Patrón de Flujo Lineal**

```
Mentor → Sistema → Estudiante (configuración inicial)
```

#### 🏓 **Patrón Ping-Pong**

```
Sistema ↔ Estudiante (ciclos pregunta-respuesta)
```

#### 🔄 **Patrón de Flujo Convergente**

```
Múltiples rutas convergiendo en puntos de decisión
```

#### 🌟 **Patrón de Flujo Divergente**

```
Puntos de decisión creando múltiples rutas posibles
```

![](./06-169_IMG04.png)

---

### 🔄 **Mecanismos de Transferencia de Control**

Cada flujo de acción representa no solo ***movimiento de datos*** sino ***transferencia de control***:

- **Transferencia Síncrona**: El control ***espera la finalización de la actividad*** antes de proceder
- **Consistencia de Estado**: Cada actor mantiene ***estado apropiado*** durante su período de control
- **Manejo de Errores**: ***Suposición implícita*** de que las actividades se completan exitosamente

---

## ***4.     Patrones de Implementación y Lógica***
---
### 🔁 **Implementación de Bucle**

El bucle pregunta-respuesta demuestra un ***patrón fundamental*** en diagramas de actividad:

#### 🔧 **Componentes de la Estructura del Bucle:**

- **Punto de Entrada del Bucle**: Actividad ***"Hacer Pregunta"***
- **Cuerpo del Bucle**: ***Presentación de pregunta*** y recolección de respuesta
- **Condición del Bucle**: Punto de decisión ***"¿Era la última?"***
- **Salida del Bucle**: Progresión a ***"Asumir Resultados"***

#### ⚡ **Características del Bucle**

- **Iteración Finita**: El bucle tiene una ***condición de terminación definida***
- **Progresión de Estado**: Cada iteración ***avanza el estado general***
- **Interfaz Consistente**: ***Mismas actividades repetidas*** con datos diferentes

---

###  **Condiciones de Guarda**

Las guardas ***"Sí" y "No"*** proporcionan lógica explícita de control de flujo:

####  **Implementación de Guarda:**

- **Lógica Booleana**: Toma de decisiones ***simple sí/no***
- **Evaluación en Tiempo de Ejecución**: Las guardas se evalúan cuando el flujo ***llega al punto de decisión***
- **Comportamiento Determinístico**: Cada condición de guarda produce ***dirección de flujo predecible***

---

### 🌟 **Resolución de Ramas**

El rombo de decisión crea ***dos rutas de ejecución distintas***:

#### 🔄 **Ruta A (No - Continuar Bucle):**

- Redirige a ***"Hacer Pregunta"***
- Mantiene ***estado actual del proceso***
- Continúa ***comportamiento iterativo***

#### ✅ **Ruta B (Sí - Completar Proceso):**

- Procede al ***procesamiento de resultados***
- Inicia ***secuencia de finalización***
- Se prepara para ***terminación del proceso***

---


## ***5.     Mejores Prácticas para Diagramas Complejos***
---
### 📖 **Estrategia de Lectura**

Al analizar ***diagramas de actividad complejos***:

1. **Comenzar con Identificación**: Leer el título del diagrama y entender el ***alcance del proceso***
2. **Identificar Carriles (Swim Lanes)**: Entender los ***actores y sus responsabilidades generales***
3. **Localizar Puntos de Inicio y Final**: Encontrar ***estados iniciales y finales***
4. **Seguir la Ruta Principal**: Rastrear el ***flujo de trabajo primario*** de inicio a fin
5. **Analizar Puntos de Decisión**: Entender la ***lógica de ramificación*** y rutas alternativas
6. **Identificar Bucles**: Buscar ***patrones iterativos*** y sus condiciones de terminación

---

### ✅ **Validación de Diseño**

Para crear ***diagramas de actividad robustos***:

#### 🔍 **Verificaciones de Completitud**

- Cada carril de natación debe tener ***actividades significativas***
- Todos los puntos de decisión deben tener ***guardas claramente definidas***
- Todas las rutas deben llevar a ***puntos finales apropiados***
- Las condiciones de terminación de bucles deben ser ***explícitas***

#### 🎯 **Validación de Consistencia**

- Los flujos de acción deben seguir ***secuencia lógica***
- Los límites de Carriles (Swim Lanes) deben ser ***respetados***
- Las responsabilidades de roles deben alinearse con la ***estructura organizacional***
- El flujo de datos debe ser consistente con la ***arquitectura del sistema***

---

### 📝 **Estándares de Documentación**

#### 🏷️ **Convenciones de Nomenclatura**

- Las actividades deben usar ***formato verbo-sustantivo***
- Las guardas deben ser ***condiciones claras y comprobables***
- Los Carriles (Swim Lanes) deben representar ***entidades organizacionales distintas***
- Los títulos de diagramas deben ***indicar claramente el alcance del proceso***
