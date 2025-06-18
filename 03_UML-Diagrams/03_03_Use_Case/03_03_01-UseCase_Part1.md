
#### 3.3  Use Case

| Guide  | Tittle                                                          |
| ------ | --------------------------------------------------------------- |
| **07-172** | **Overview of UML Use Case Diagram Elements**                       |
| 07-173 | Deep Dive: Build a Marketing Automation System Use Case Diagram |

---
# 07-172:    Use Case Diagrams (1)


1. What UML UseCase Diagrams are
2. Core Elements Overview
3. Use Cases
4. Actors
5. Subsystems (System Boundaries)
6. Relationships
7. Key Design Principles

---

## ***1.      What UML Class Diagrams are***

Use Case Diagrams are **behavioural UML diagrams designed to model system functionality from a user's (actors') perspective**. 

Their primary purpose is to establish **authorisation rules** and **illustrate what features different types of users or clients can access within a system**.

#### **Primary Objectives**

- Define **access permissions and authorisation** boundaries
- Visualise system functionality available to different user types
- Provide developers with clear requirements for building authorisation engines
- Document feature accessibility across different user roles

---


## ***2.      Core Elements***
---
Use Case Diagrams consist of **FOUR fundamental elements** which work together to represent system access and functionality:

1.  **Use Cases**: Specific actions or functionalities available in the system

2. **Actors**: Users, systems, or clients that interact with the system

3. **Subsystems**: Organisational boundaries that group related use cases

4. **Relationships**: Connections between actors and use cases


---


## 3. Use Cases
---
#### **Visual Representation**

![medium](./07-171_IMG1.png)
Ovals or elliptical shapes containing action descriptions

#### **Characteristics**

- Represent specific actions or functionalities within the system
- Should be **action-oriented** using verb-noun format
- Focus on what users can do, not how the system implements it
- Abstract away implementation details and data attributes

#### **Examples of Use Cases**

>- "Get Reports"
>- "Get Messages"
>- "Manage Contacts"
>- "Visit Resources"


#### **Design Principle**

Use cases should clearly communicate available features to developers, enabling them to understand authorisation requirements without getting bogged down in technical implementation details.


#### 🙅 **What Use Cases DON'T Include**

- Data attributes or database schema details
- Specific methods or function implementations
- Technical implementation specifics
- Internal system processes invisible to users

---


## ***4.     Actors***
---
#### **Visual Representation** 
Stick figures or actor symbols positioned outside the system boundary

![medium](./07-171_IMG2.png)

#### **Definition** 

Any entity that interacts with the system from the outside, including both human users and non-human systems.
##### Human Actors

- **Admin**: System administrators with elevated privileges
- **Customer**: End users or clients using the system
- **Manager**: Users with specific role-based permissions
##### Non-Human Actors

- **API Clients**: External applications that consume system APIs
- **Mobile Applications**: iOS/Android apps accessing backend services
- **Third-Party Systems**: External websites or services that integrate with the system
- **Automated Services**: Scheduled processes or monitoring systems


#### **Important Consideration** 

In API-driven architectures, you may never have direct human users. Instead, various software clients (mobile apps, web applications, other APIs) act as the primary actors accessing system functionality.


#### **Example Scenario** 

> An API that provides blog posts or user data to mobile applications, where the mobile app itself is the actor, not the individual users of that mobile app.

---


## ***5.      Subsystems (System Boundaries)***
---
#### **Visual Representation** 
Large rectangular boxes that contain related use cases and other elements
![medium](./07-171_IMG3.png)

#### **Purpose**
Organize and group related functionality within logical system boundaries


#### **Characteristics**

- Help organize complex systems into manageable sections
- Clearly delineate what functionality belongs to which part of the system
- Provide visual separation between different system components or modules


#### **Example Structure**

```
Web Dashboard (Subsystem)
|
├── Get Reports
├── Get Messages  
├── Manage Contacts
├── Visit Resources
└── Forms

External to Web Dashboard:
|
├── Manage Journeys and Shapes
├── Trigger Journey Events
└── Get Notifications Regarding Journeys
```


#### 🗿 **Organisational Benefits**

- **Clear Scope Definition**: Shows exactly which features belong to each system component
- **Development Planning**: Helps teams understand which features to implement in which modules
- **System Architecture Visualisation**: Provides high-level view of system organisation

---


## ***6.     Relationships***
---
#### **Visual Representation**

Lines connecting actors to use cases, typically with arrows indicating direction of interaction

![medium](./07-171_IMG4.png)

## **Types of Relationship Lines:

- ##### **Solid Lines**: 
  Direct associations between actors and use cases

- ##### **Dotted Lines with Open Arrows** 
  Show relationships and connections between different use cases


#### **Purpose**

##### Establish clear connections between who can access what functionality in the system



#### **Relationship Functions**

- Connect actors directly to the use cases they can access
- Show which system elements each actor type can interact with
- Visualise permission and access patterns
- Document authorisation rules in visual format


#### **Authorisation Mapping**

Relationships serve as the visual representation of an authorisation matrix, showing developers exactly which actors should have access to which system features.

---


## ***7.      Design Principles***
---
### Action-Oriented Focus

Use cases should emphasise **what** users can do rather than **how** the system accomplishes those tasks. This keeps diagrams focused on functionality rather than implementation.

### Authorisation-Centric Design

The primary goal is to create a clear authorisation framework that developers can use to implement proper access controls and permission systems.

### Abstraction Level

Use case diagrams operate at a high level of abstraction, focusing on user-visible functionality while hiding internal system complexity.

### Actor Diversity Recognition

Modern systems often have diverse actor types, including automated systems, APIs, and various client applications, not just human users.

### Organisational Clarity

Subsystems help manage complexity in large systems by providing logical groupings of related functionality, making the overall system easier to understand and implement.
