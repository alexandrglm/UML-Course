

| Guide  | Tittle                                        |
| ------ | --------------------------------------------- |
| 07-187 | The Importance of Systems Analysis and Design |
| 07-188 | Overview of Software Systems                  |

| Guide      | Tittle                                          |
| ---------- | ----------------------------------------------- |
| 06-150     | UML Overview                                    |
| 06-151 | Stages of Development where UML is Utilized |

| Guide      | Tittle                          |
| ---------- | ------------------------------- |
| **06-160** | **Diagrams & Categories Intro** |

---
# 06-150:   UML Diagrams - Categories overview



# ***1. Complete UML Diagram Types***
---

UML (Unified Modeling Language) diagrams are divided into **two main categories**:

* #### 1.  Structural 
* #### 2.  Behavioural.

This clear distinction helps developers quickly identify which type of diagram to use based on what they're modeling.


---
## Structural Diagrams (7 types)

| Diagram Type                    | Purpose                                     |
| ------------------------------- | ------------------------------------------- |
| **Class Diagram**               | Classes, attributes, methods, relationships |
| **Object Diagram**              | Specific instances at runtime               |
| **Component Diagram**           | Software components and dependencies        |
| **Composite Structure Diagram** | Internal structure of classes/components    |
| **Package Diagram**             | Packages and their dependencies             |
| **Deployment Diagram**          | Hardware/software deployment                |
| **Profile Diagram**             | Domain-specific stereotypes and extensions  |


## Behavioural Diagrams (7 types)

| Diagram Type                     | Purpose                              |
| -------------------------------- | ------------------------------------ |
| **Use Case Diagram**             | Actors and system interactions       |
| **Activity Diagram**             | Workflows and business processes     |
| **State Machine Diagram**        | Object states and transitions        |
| **Sequence Diagram**             | Time-ordered interactions            |
| **Communication Diagram**        | Object interactions with links       |
| **Timing Diagram**               | Interactions with timing constraints |
| **Interaction Overview Diagram** | Control flow between interactions    |

---

```mermaid
graph TD
    UML[UML Diagrams] --> ST[Structural<br/>(7 types)]
    UML --> BH[Behavioural<br/>(7 types)]
    
    ST --> CL[Class]
    ST --> OB[Object]
    ST --> CO[Component]
    ST --> CS[Composite Structure]
    ST --> PK[Package]
    ST --> DP[Deployment]
    ST --> PR[Profile]
    
    BH --> UC[Use Case]
    BH --> AC[Activity]
    BH --> SM[State Machine]
    BH --> SQ[Sequence]
    BH --> CM[Communication]
    BH --> TM[Timing]
    BH --> IO[Interaction Overview]
```


---
## ***2. Decision Framework***

When choosing a UML diagram type, ask yourself:

- **Am I modeling the system's architecture?** → Use Structural Diagrams

- **Am I modeling the system's behaviour?** → Use Behavioral Diagrams

---
## ***Structural Diagrams***

### Definition

Structural diagrams model **how a system is architected** - they focus on the static aspects of the system.

### Characteristics

- Show the **structure** and **organisation** of system components
- Define relationships between different parts
- Focus on **what exists** in the system

### Primary Example: Class Diagram

- Most popular structural diagram
- Defines:
    - Class names
    - Attributes (properties/fields)
    - Method names
    - Relationships between classes

### Use Cases

- System architecture planning
- Code structure visualization
- Component relationships
- Database schema modeling



---
## ***Behavioural Diagrams***

### Definition

Behavioral diagrams model **how a system behaves** - they focus on the dynamic aspects and interactions.

### Characteristics

- Show **interactions** and **processes**
- Model **communication** between components
- Focus on **what happens** in the system

### Key Questions They Answer

- ***What messages does one system send to another?***
- ***What permissions does User A have vs User B?***
- ***How do different parts of the system interact?***
- ***What is the flow of operations?***

### Use Cases

- Process flow modeling
- User interaction scenarios
- System communication patterns
- Permission and access control modeling

---
## ***Practical Application***

### For Object-Oriented Programming

- **Structural**: Model your classes, inheritance hierarchies, composition relationships
- **Behavioral**: Model method calls, object interactions, state changes

### Development Workflow

1. **Planning Phase**: Use structural diagrams to design system architecture
2. **Implementation Phase**: Use behavioral diagrams to model interactions and workflows
3. **Documentation Phase**: Combine both types for comprehensive system documentation

---

### And, now?

##### Later, in 03_Diagrams, a comprehensive explanation of diagrams, their types, classifications, etc., will be provided. 

For now, after a brief overview of the existing diagram types and their classification, we will proceed to first define all the common elements among each type of diagram.