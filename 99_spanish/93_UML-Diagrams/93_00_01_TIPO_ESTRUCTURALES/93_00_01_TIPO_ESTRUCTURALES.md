| Guía       | Título                                              |
| ---------- | --------------------------------------------------- |
| **06-161** | **Visión General de Diagramas Estructurales en UML** |
| 06-162     | Visión General de Diagramas Comportamentales en UML |

---
# 06-161:  Diagramas Estructurales


1. Introducción a los Diagramas Estructurales  

2. Diagramas de Clases  
   2.1. Propósito y Aplicaciones  
   2.2. Componentes Principales  
   2.3. Sintaxis y Notación  
   2.4. Integración con Base de Datos  

3. Diagramas de Despliegue  
   3.1. Modelado de Arquitectura  
   3.2. Seis Elementos Principales  
   3.3. Integración CI/CD  
   3.4. Estructura de Nodos y Componentes  

4. Diagramas de Paquetes  
   4.1. Organización de Bibliotecas  
   4.2. Gestión de Dependencias  
   4.3. Arquitectura Modular  

5. Mejores Prácticas y Consejos de Implementación

---

## ***1.    Introducción a los Diagramas Estructurales***
---
Los diagramas UML estructurales representan los **aspectos estáticos de un sistema**, enfocándose en **las cosas que deben estar presentes en el sistema que se está modelando**. 

A diferencia de los diagramas comportamentales que muestran qué sucede cuando el sistema se ejecuta, los diagramas estructurales muestran **qué existe en el sistema**.

Los tres diagramas estructurales principales cubiertos en esta visión general son **Diagramas de Clases**, **Diagramas de Despliegue**, y **Diagramas de Paquetes**.


|                                 | Propósito                                    |
| ------------------------------- | -------------------------------------------- |
| **Diagrama de Clases**          | Clases, atributos, métodos, relaciones      |
| **Diagrama de Objetos**         | Instancias específicas en tiempo de ejecución |
| **Diagrama de Componentes**     | Componentes de software y dependencias      |
| **Diagrama de Estructura Compuesta** | Estructura interna de clases/componentes |
| **Diagrama de Paquetes**        | Paquetes y sus dependencias                 |
| **Diagrama de Despliegue**      | Despliegue de hardware/software             |
| **Diagrama de Perfil**          | Estereotipos y extensiones específicos del dominio |


Estos diagramas sirven como **la base para la documentación de arquitectura del sistema** y son esenciales para comunicar decisiones de diseño a equipos de desarrollo, partes interesadas y personal de mantenimiento.   

Cada tipo de diagrama aborda diferentes aspectos de la estructura del sistema, desde el diseño orientado a objetos hasta la arquitectura de despliegue físico.

---


## ***2.    Diagramas de Clases***
---
### Propósito y Aplicaciones

Los diagramas de clases son **los más populares** y comúnmente utilizados diagramas UML en el desarrollo de software.   

Sirven como la piedra angular del análisis y diseño orientado a objetos, proporcionando **una representación visual de clases, sus atributos, métodos y relaciones** dentro de un sistema.


Los diagramas de clases son particularmente **valiosos para**:

- **Diseño de Esquemas de Base de Datos**: Traducir modelos de objetos directamente a estructuras de base de datos relacionales

- **Generación de Código**: Proporcionar planos para generación automática de código

- **Comunicación de Equipo**: Ofrecer una comprensión compartida de la estructura del sistema

- **Documentación**: Servir como documentación viva que evoluciona con el sistema

----
### Componentes Principales

Cada clase en un diagrama de clases UML consiste en tres secciones esenciales:

1. **Nombre de Clase**: El compartimento superior que contiene el identificador de la clase
2. **Atributos**: La sección media listando propiedades y sus tipos de datos
3. **Operaciones/Métodos**: La sección inferior mostrando métodos y funciones

#### Sintaxis de Atributos

```
[+/-/#/~ visibilidad] [nombre] : [tipo] [multiplicidad] = valorPorDefecto
```

#### Sintaxis de Operaciones

```
[+/-/#/~ visibilidad] [nombre(parámetros)] : [tipoRetorno]
```


### Sintaxis y Notación

#### **Modificadores de Visibilidad:**

- `+` **Público**: Accesible desde fuera de la clase
- `-` **Privado**: Accesible solo dentro de la clase
- `#` **Protegido**: Accesible dentro de la clase y sus subclases
- `~` **Paquete**: Accesible dentro del mismo paquete

#### **Ejemplo de Estructura de Clase**

```
Tema
-----------------
+ titulo : String
+ slug : String
+ fechaCreacion : DateTime
+ fechaActualizacion : DateTime
-----------------
+ topDiez() : List<Tema>
- calcularRanking() : Integer
```


---
### Integración con Base de Datos

Los diagramas de clases se traducen perfectamente a esquemas de base de datos. Los administradores de base de datos pueden usar diagramas de clases para:

- Crear estructuras de tablas con nombres de campos y tipos de datos apropiados
- Establecer relaciones de claves primarias y foráneas
- Definir restricciones e índices
- Planificar estrategias de normalización de base de datos

---


## ***3.    Diagramas de Despliegue***
---
### Modelado de Arquitectura

Los diagramas de despliegue **modelan el despliegue físico de componentes de software en nodos de hardware**:

* ##### Proporcionando una vista de alto nivel de la arquitectura del sistema

* ##### Mostrando cómo diferentes partes de una aplicación se distribuyen a través de varios recursos computacionales.



### Seis Elementos Principales

1. **Nodos**: Máquinas físicas o virtuales donde se despliegan los componentes
2. **Componentes**: Módulos de software o aplicaciones
3. **Artefactos**: Piezas físicas de información usadas o producidas
4. **Rutas de Comunicación**: Conexiones entre nodos
5. **Especificaciones de Despliegue**: Detalles de configuración
6. **Especificaciones de Instancia**: Instancias específicas de nodos o componentes


---
### Integración CI/CD

Los diagramas de despliegue modernos a menudo incorporan conceptos de **Integración Continua/Despliegue Continuo (CI/CD)**:

![IMG](./06-161_IMG6.png)

#### **Flujo CI/CD Típico**

1. **Servidor CI**: Entorno automatizado de construcción y pruebas
2. **Entorno de Staging**: Plataforma de pruebas pre-producción
3. **Entorno Pre-producción**: Pruebas de aseguramiento de calidad
4. **Entorno de Producción**: Despliegue del sistema en vivo


### Estructura de Nodos y Componentes

##### **Tipos de Nodos**

- **Nodos de Dispositivo**: Hardware físico (servidores, estaciones de trabajo)
- **Nodos de Entorno de Ejecución**: Plataformas de software (JVM, runtime .NET)

##### **Despliegue de Componentes:** 

Los componentes dentro de los nodos pueden incluir:

- Servidores de aplicación
- Motores de base de datos
- Servidores web
- Procesos de construcción
- Sistemas de control de versiones

---

## ***4.    Diagramas de Paquetes***
---

### Organización de Bibliotecas

Los diagramas de paquetes **organizan clases e interfaces relacionadas en unidades cohesivas**. Son particularmente útiles para:

- **Diseño de Bibliotecas de Código**: Estructurar componentes reutilizables
- **Modularización del Sistema**: Dividir sistemas complejos en partes manejables
- **Gestión de Espacios de Nombres**: Organizar jerarquías de código


### Gestión de Dependencias

Los diagramas de paquetes sobresalen en mostrar dependencias entre diferentes módulos:

- **Dependencias de Importación**: Un paquete usa clases de otro
- **Dependencias de Acceso**: Un paquete accede a elementos públicos de otro
- **Dependencias de Uso**: Un paquete requiere otro para su operación


##### **Notación de Dependencias**

- Las flechas punteadas indican relaciones de dependencia
- Las puntas de flecha abiertas apuntan hacia el paquete del cual se depende


### Arquitectura Modular

Beneficios de la organización basada en paquetes:

- **Complejidad Reducida**: Dividir sistemas grandes en unidades más pequeñas y manejables
- **Mantenibilidad Mejorada**: Separación clara de responsabilidades
- **Reutilización Mejorada**: Los paquetes pueden reutilizarse entre proyectos
- **Mejores Pruebas**: Los paquetes individuales pueden probarse de forma aislada

---


## ***5.    Buenas Prácticas - Consejos de Implementación***
---

### Buenas Prácticas para Diagramas de Clases

- Mantener nombres de clases concisos pero descriptivos
- Usar convenciones de nomenclatura consistentes
- Incluir solo atributos y operaciones relevantes
- Mostrar relaciones claramente con multiplicidad apropiada
- Evitar diagramas demasiado complicados; usar múltiples diagramas si es necesario

### Directrices para Diagramas de Despliegue

- Empezar con arquitectura de alto nivel antes de añadir detalles
- Etiquetar claramente todos los nodos con su propósito
- Mostrar protocolos de comunicación entre nodos
- Incluir mecanismos de redundancia y recuperación ante fallos
- Documentar configuraciones de despliegue

### Recomendaciones para Diagramas de Paquetes

- Crear agrupaciones lógicas basadas en funcionalidad
- Minimizar dependencias entre paquetes
- Usar principios de arquitectura por capas
- Documentar interfaces de paquetes claramente
- Revisión regular y refactorización de estructura de paquetes


### Consejos Generales para Diagramas Estructurales

- **Selección de Herramientas**: Elegir herramientas UML que soporten el flujo de trabajo del equipo
- **Control de Versiones**: Mantener diagramas bajo control de versiones junto con el código
- **Documentación**: Mantener documentación adicional para diagramas complejos
- **Actualizaciones Regulares**: Mantener diagramas sincronizados con cambios de código
- **Entrenamiento del Equipo**: Asegurar que los miembros del equipo entiendan los estándares de notación UML

---
