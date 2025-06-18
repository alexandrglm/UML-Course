#### 3.4 Deployment

| Guide  | Tittle                                                    |
| ------ | --------------------------------------------------------- |
| **07-175** | **Overview of the Elements of a UML Deployment Diagram**      |
| 07-176 | Deep Dive: Build a Song Request Deployment Engine Diagram |

---

# 07-175: UML Deployment Diagram Elements


1. **Introduction to Deployment Diagrams**

2. **Core Elements Overview**
   1. Nodes
   2. Components
   3. Artifacts
   4. Links
   5. Dependencies
   6. Associations

3. **Design Principles and Best Practices**

---

## ***1.     Introduction to Deployment Diagrams***

Deployment diagrams are ***structural UML diagrams that model the physical architecture of a system.***

They are primarily used for ***system architecture decisions*** and show how software components are distributed across hardware infrastructure.

### 🎯 **Primary Purpose**

- ***Visualise system architecture*** and infrastructure requirements
- ***Define deployment strategies*** and configuration needs
- Show relationships between ***hardware and software*** components
- ***Guide infrastructure setup*** and deployment processes

### 📋 **When to Use**

- ***Planning system architecture*** at project start
- ***Documenting existing system*** infrastructure
- ***Communicating deployment requirements*** to operations teams
- ***Designing scalable*** and distributed systems

---


## ***2.     Core Elements Overview***
---
Deployment diagrams consist of ***SIX*** fundamental elements that work together to represent system architecture:

![large](./07-175_IMG0.png)

- **Nodes**: ***Physical or logical*** hardware/software units
- **Components**: ***Software applications*** or services running on nodes
- **Artifacts**: ***Deployable software elements*** with specific configurations
- **Links**: ***Basic connections*** between nodes
- **Dependencies**: ***Directional relationships*** showing dependencies
- **Associations**: ***Complex relationships*** in distributed systems

---

## ***2.1     Nodes***

### 📝 **Definition**

> Nodes represent ***the fundamental building blocks*** of deployment diagrams - they are ***the actual real-world components where software runs***.

### 🎨 **Visual Representation**

![large](./07-175_IMG1.png)

***Three-dimensional boxes*** or cubes representing physical or logical deployment targets

### 🏗️ **Types of Nodes**

- **Physical Servers**: ***Web servers, database servers, application servers***
- **Virtual Machines**: ***Cloud instances, containers***
- **Databases**: ***Database management systems***
- **APIs**: ***Service endpoints***
- **Network Devices**: ***Load balancers, routers, firewalls***

### 🔑 **Key Principle**

> ***Everything in a deployment diagram is essentially a node***. All other elements either add detail to nodes or show relationships between them.

### 💡 **Examples**

- ***Web Server*** hosting a React/Angular frontend
- ***Database Server*** running MongoDB, PostgreSQL
- ***API Gateway*** managing service requests
- ***Load Balancer*** distributing traffic

---

## ***2.2     Components***

### 📝 **Definition**

> ***Software applications, services, or logical units that run within nodes*** and handle business logic and communication.

![large](07-175_IMG3.png)

### 🎨 **Visual Representation**

![large](./07-175_IMG2.png)

***Rounded rectangles*** contained within nodes, often with component stereotypes

### 🔧 **Component Types**

- **Web Applications**: ***Front-end applications*** (Angular, React, Vue)
- **Web Services**: ***Back-end services*** and APIs
- **Database Systems**: ***Database management software***
- **Middlewares**: ***Message queues, caching systems***
- **Business Logic Services**: ***Domain-specific applications***

### 🎭 **Alternative Syntax**

Different UML tools may represent components with ***varying visual styles***:

- **Standard Style**: ***Rounded rectangles*** with component labels
- **Enterprise Architect Style**: ***Rectangular boxes*** with component stereotypes
- **Simplified Style**: ***Text labels*** within nodes

### 💭 **Design Philosophy**

> ***The specific visual representation is less important than clearly communicating the software components*** and their organisation.

Choose the style that ***best serves your stakeholders*** and documentation needs.

---

## ***2.3     Artifacts***

### 📝 **Definition**

***Specific "deployable" software elements*** that provide detailed configuration and deployment information.

### 🎨 **Visual Representation**

Text surrounded by ***angle brackets*** (e.g., `<<device>>`, `<<angular web service>>`)

![large](./07-175_IMG4.png)

### 🎯 **Purpose**

Artifacts tell architects and operations teams exactly ***what needs to be installed, configured, and deployed*** on each node.

### 📊 **Artifact Information Types**

- **Software Stack Requirements**: ***Framework and runtime specifications***
- **Operating System Details**: ***OS type and version requirements***
- **Configuration Parameters**: ***Environment-specific settings***
- **Interface Specifications**: ***Communication protocols and ports***

### 💡 **Examples**

- `<<device:webServer Interface {OS=Linux}>>`
- `<<angular web service>>`
- `<<Rails API {version=7.0, database=PostgreSQL}>>`

### 🔍 **Practical Value Example**

>#### 1️⃣ When an artifact specifies ***"angular web service"***....
>#### 2️⃣ .... operations teams know to install ***Node.js, NPM, and Angular dependencies***.


>#### 1️⃣ If it specifies ***"Rails web service,"***....
>#### 2️⃣ .... they know to prepare ***Ruby, Rails, and associated dependencies***.


### 📋 **Formal Naming Convention**

UML standard format includes ***device type, interface specification, and configuration parameters*** in a structured format for precise deployment instructions.

---

## ***2.4     Links***

### 📝 **Definition**

***Basic connections*** between nodes showing that communication occurs between system components.

### 🎨 **Visual Representation**

***Simple lines*** connecting nodes without directional information

![large](07-175_IMG5.png)

### 🎯 **Purpose**

- ***Show which nodes can communicate*** with each other
- Indicate ***network connectivity requirements***
- Visualise ***basic system topology***

### 🔗 **Connection Examples**

- ***Angular front-end*** linked to Authentication system
- ***Front-end*** linked to Rails API
- ***API*** linked to Authentication system

### 💭 **Use Case**

> ***Links provide a high-level view*** of system connectivity without specifying the nature or direction of dependencies.

---

## ***2.5     Dependencies***

### 📝 **Definition**

***Directional relationships*** that specify which nodes depend on others for functionality.

### 🎨 **Visual Representation**

***Dotted lines with arrows*** pointing toward the nodes being depended upon

![large](07-175_IMG6.png)

### 🎯 **Purpose**

- ***Show explicit dependency relationships***
- Indicate ***deployment order requirements***
- ***Clarify*** service dependencies for troubleshooting
- ***Guide system startup*** and shutdown sequences

### 📈 **Dependency Analysis Benefits**

- **Quick Assessment**: At a glance, understand ***which components rely on others***
- **Deployment Planning**: Dependencies indicate ***which services must be started first***
- **Impact Analysis**: Understand ***which components are affected*** if a dependency fails

### 💡 **Example Pattern**

- ***Angular frontend*** depends on Authentication system (arrow points to Auth)
- ***Angular frontend*** depends on Rails API (arrow points to API)
- ***Rails API*** depends on Authentication system (arrow points to Auth)

---

## ***2.6     Associations***

### 📝 **Definition**

***Complex relationships*** in distributed systems that show how multiple nodes work together in sophisticated architectures.

### 🎨 **Visual Representation**

***Lines connecting multiple nodes***, often in hub-and-spoke or network patterns

![large](07-175_IMG7.png)

### 🛠️ **Use Cases**

- **Load Balancer Architectures**: Show how load balancers ***distribute requests*** to multiple application servers
- **Microservice Communication**: Model ***complex service-to-service*** communication patterns
- **Database Clustering**: Represent ***database replication*** and clustering relationships
- **CDN Networks**: Show ***content distribution*** and caching relationships

### 🏗️ **Example Architecture**

A ***load balancer*** receiving requests from the Internet and mapping them to various application servers, which then communicate with ***database clusters***.

### 📋 **Deployment Strategy Insights**

Association patterns provide a ***"recipe" for infrastructure setup***, showing:

- ***Number of application servers*** needed
- ***Database clustering requirements***
- ***Load balancer configuration*** needs
- ***Network topology requirements***

---


## ***3.     Design Principles and Best Practices***
---
### 🎯 **Clarity Over Perfection**

- Focus on ***clear communication*** rather than perfect UML notation
- Choose ***visual styles*** that make sense to your stakeholders
- Prioritize ***understanding*** over strict symbol adherence

### 🏗️ **Architecture-First Approach**

- Use deployment diagrams ***early in project planning***
- Let ***infrastructure requirements*** drive technology choices
- Consider ***scalability and maintenance*** from the start

### 👥 **Stakeholder Communication**

- Ensure diagrams serve both ***technical and business audiences***
- Include ***enough detail*** for implementation without overwhelming
- Use ***consistent notation*** across project documentation

### 📋 **Deployment Recipe Mentality**

- Design diagrams that serve as ***deployment guides***
- Include ***configuration details*** in artifacts
- Show dependencies clearly for ***proper deployment sequencing***

### 🛠️ **Tool Flexibility**

- Accept that different UML tools may have ***varying visual representations***
- Focus on ***content accuracy*** rather than visual consistency across tools
- Document any ***tool-specific notation choices*** for team clarity
