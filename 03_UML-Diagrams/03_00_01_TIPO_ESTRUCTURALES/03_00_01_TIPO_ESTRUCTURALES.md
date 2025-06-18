
| Guide      | Tittle                                     |
| ---------- | ------------------------------------------ |
| **06-161** | **Overview of Structural Diagrams in UML** |
| 06-162     | Overview of Behavioural Diagrams in UML    |

---
# 06-161:  Structural Diagrams


1. Introduction to Structural Diagrams  

2. Class Diagrams  
   2.1. Purpose and Applications  
   2.2. Core Components  
   2.3. Syntax and Notation  
   2.4. Database Integration  

3. Deployment Diagrams  
   3.1. Architecture Modeling  
   3.2. Six Core Elements  
   3.3. CI/CD Integration  
   3.4. Node and Component Structure  

4. Package Diagrams  
   4.1. Library Organization  
   4.2. Dependency Management  
   4.3. Modular Architecture  

5. Best Practices and Implementation Tips

---

## ***1.    Introduction to Structural Diagrams***
---
Structural UML diagrams represent the **static aspects of a system**, focusing on **the things that must be present in the system being modeled**. 

Unlike behavioural diagrams that show what happens when the system runs, structural diagrams show **what exists in the system**.

 The three primary structural diagrams covered in this overview are **Class Diagrams**, **Deployment Diagrams**, and **Package Diagrams**.


|                                 | Purpose                                     |
| ------------------------------- | ------------------------------------------- |
| **Class Diagram**               | Classes, attributes, methods, relationships |
| **Object Diagram**              | Specific instances at runtime               |
| **Component Diagram**           | Software components and dependencies        |
| **Composite Structure Diagram** | Internal structure of classes/components    |
| **Package Diagram**             | Packages and their dependencies             |
| **Deployment Diagram**          | Hardware/software deployment                |
| **Profile Diagram**             | Domain-specific stereotypes and extensions  |


These diagrams serve as **the foundation for system architecture documentation** and are essential for communicating design decisions to development teams, stakeholders, and maintenance personnel.   

Each diagram type addresses different aspects of system structure, from object-oriented design to physical deployment architecture.

---


## ***2.    Class Diagrams***
---
### Purpose and Applications

Class diagrams are **the most popular** and commonly used UML diagrams in software development.   

They serve as the cornerstone of object-oriented analysis and design, providing **a visual representation of classes, their attributes, methods, and relationships** within a system.


Class diagrams are particularly **valuable for**:

- **Database Schema Design**: Translating object models directly into relational database structures

- **Code Generation**: Providing blueprints for automatic code generation

- **Team Communication**: Offering a shared understanding of system structure

- **Documentation**: Serving as living documentation that evolves with the system

----
### Core Components

Every class in a UML class diagram consists of three essential sections:

1. **Class Name**: The top compartment containing the class identifier
2. **Attributes**: The middle section listing properties and their data types
3. **Operations/Methods**: The bottom section showing methods and functions

#### Attribute Syntax

```
[+/-/#/~ visibility] [name] : [type] [multiplicity] = defaultValue
```

#### Operation Syntax

```
[+/-/#/~ visibility] [name(parameters)] : [returnType]
```


### Syntax and Notation

#### **Visibility Modifiers:**

- `+` **Public**: Accessible from outside the class
- `-` **Private**: Accessible only within the class
- `#` **Protected**: Accessible within the class and its subclasses
- `~` **Package**: Accessible within the same package

#### **Example Class Structure**

```
Topic
-----------------
+ title : String
+ slug : String
+ createdAt : DateTime
+ updatedAt : DateTime
-----------------
+ topTen() : List<Topic>
- calculateRanking() : Integer
```


---
### Database Integration

Class diagrams seamlessly translate to database schemas. Database administrators can use class diagrams to:

- Create table structures with appropriate field names and data types
- Establish primary and foreign key relationships
- Define constraints and indexes
- Plan database normalization strategies

---


## ***3.    Deployment Diagrams***
---
### Architecture Modeling

Deployment diagrams **model the physical deployment of software components on hardware nodes**:

* ##### Providing a high-level view of system architecture

* ##### Showing how different parts of an application are distributed across various computing resources.



### Six Core Elements

1. **Nodes**: Physical or virtual machines where components are deployed
2. **Components**: Software modules or applications
3. **Artifacts**: Physical pieces of information used or produced
4. **Communication Paths**: Connections between nodes
5. **Deployment Specifications**: Configuration details
6. **Instance Specifications**: Specific instances of nodes or components


---
### CI/CD Integration

Modern deployment diagrams often incorporate **Continuous Integration/Continuous Deployment (CI/CD)** concepts:

![IMG](./06-161_IMG6.png)

#### **Typical CI/CD Flow**

1. **CI Server**: Automated build and testing environment
2. **Staging Environment**: Pre-production testing platform
3. **Pre-production Environment**: Quality assurance testing
4. **Production Environment**: Live system deployment


### Node and Component Structure

##### **Node Types**

- **Device Nodes**: Physical hardware (servers, workstations)
- **Execution Environment Nodes**: Software platforms (JVM, .NET runtime)

##### **Component Deployment:** 

Components within nodes can include:

- Application servers
- Database engines
- Web servers
- Build processes
- Version control systems

---

## ***4.    Package Diagrams***
---

### Library Organisation

Package diagrams **organise related classes and interfaces into cohesive units**. They're particularly useful for:

- **Code Library Design**: Structuring reusable components
- **System Modularization**: Breaking complex systems into manageable parts
- **Namespace Management**: Organizing code hierarchies


### Dependency Management

Package diagrams excel at showing dependencies between different modules:

- **Import Dependencies**: One package uses classes from another
- **Access Dependencies**: One package accesses public elements of another
- **Usage Dependencies**: One package requires another for its operation


##### **Dependency Notation**

- Dotted arrows indicate dependency relationships
- Open arrowheads point toward the depended-upon package


### Modular Architecture

Benefits of package-based organization:

- **Reduced Complexity**: Breaking large systems into smaller, manageable units
- **Improved Maintainability**: Clear separation of concerns
- **Enhanced Reusability**: Packages can be reused across projects
- **Better Testing**: Individual packages can be tested in isolation

---


## ***5.    Best Practices -  Implementation Tips***
---

### Class Diagram Best Practices

- Keep class names concise but descriptive
- Use consistent naming conventions
- Include only relevant attributes and operations
- Show relationships clearly with appropriate multiplicity
- Avoid overcomplicated diagrams; use multiple diagrams if necessary

### Deployment Diagram Guidelines

- Start with high-level architecture before adding details
- Clearly label all nodes with their purpose
- Show communication protocols between nodes
- Include redundancy and failover mechanisms
- Document deployment configurations

### Package Diagram Recommendations

- Create logical groupings based on functionality
- Minimize inter-package dependencies
- Use layered architecture principles
- Document package interfaces clearly
- Regular review and refactoring of package structure

### General Structural Diagram Tips

- **Tool Selection**: Choose UML tools that support your team's workflow
- **Version Control**: Keep diagrams under version control alongside code
- **Documentation**: Maintain accompanying documentation for complex diagrams
- **Regular Updates**: Keep diagrams synchronized with code changes
- **Team Training**: Ensure team members understand UML notation standards

---
