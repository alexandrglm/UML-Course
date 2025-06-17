
| Guide      | Tittle                                          |
| ---------- | ----------------------------------------------- |
| 06-150     | UML Overview                                    |
| **06-151** | **Stages of Development where UML is Utilized** |

| Guide  | Tittle                                        |
| ------ | --------------------------------------------- |
| 07-187 | The Importance of Systems Analysis and Design |
| 07-188 | Overview of Software Systems                  |

---

# **06-151:    Dev. Stages where UML is utilised**
  

1.  Integrating UML with the Development Life-cycle

2.  Mapping Diagram Types to Development Phases

    * **Phase 1:      Pre-Development**
        * Activity Diagrams
        * Deployment Diagrams

    * **Phase 2:      Active Development**
        * Class Diagrams
        * Use Case Diagrams

    * **Phase 3:      Post-Development and Maintenance**
        * Sequence Diagrams
        * Package Diagrams

3.  Strategic Application of UML

---
## 1.    **Development Life-Cycle and UML Integration**

UML diagrams can be strategically employed throughout the entire software development lifecycle.  

Each phase benefits from specific diagram types that address particular challenges and requirements.

---
## **2.     Development Phases Overview**

    * **Phase 1:      Pre-Development**
        * Activity Diagrams
        * Deployment Diagrams

    * **Phase 2:      Active Development**
        * Class Diagrams
        * Use Case Diagrams

    * **Phase 3:      Post-Development and Maintenance**
        * Sequence Diagrams
        * Package Diagrams
---

## ***Phase 1:     Pre-Development Planning***
 

Before writing a single line of code, UML helps establish a clear roadmap and architecture for your application.
### Diagrams Used in Pre-Development Phase
---
## A)    Activity Diagrams

![](./06-151_IMG1.png)

### **When to Use**
When you need to understand the **application flow** and **user interactions**.

### **Purpose**
* Map out the sequential flow of activities.
* Define decision points and alternative paths.
* Break down complex processes into manageable steps.
* Visualize the user journey through the application.

### **Example Scenario**
>Planning a user registration system, from initial signup and email verification to account activation.

### **Benefits**
* Clarifies functionality before implementation.
* Identifies potential bottlenecks or complex decision points.
* Provides a clear reference for developers and stakeholders.

---
## B)    Deployment Diagrams

  

![](./06-151_IMG2.png)

### **When to Use**
When **designing system architecture** and **infrastructure**.

### **Purpose**
* Define the high-level system architecture.
* Specify the technology stack and component relationships.
* Plan server configurations and deployment strategies.
* Visualise how different system components will communicate.

### **Example Scenario**
>Planning a web application with a JavaScript/React/Angular front-end, a REST API back-end, and a database server, including specific configurations.

### **Benefits**
* Prevents architectural missteps early in development.
* Helps estimate infrastructure costs and requirements.
* Facilitates communication with DevOps and system administrators.
* Serves as a blueprint for deployment procedures.

---


## ***Phase 2: Active Development***

During development, UML helps maintain organization and ensures best practices while building the system.

---
### Diagrams Used in Active Development Phase
---
## C)    Class Diagrams

  

![Class Diagram Example](./06-151_IMG3.png)

### **When to Use**
When **designing database schemas** and **object relationships**.

### **Purpose**
* Model database table relationships.
* Ensure proper database normalization.
* Define object properties and methods.
* Visualize inheritance and composition relationships.

### **Example Scenario**
>Designing an e-commerce database with `User`, `Product`, `Order`, and `Payment` entities and their relationships.

### **Benefits**

* Promotes organized database design.
* Helps identify redundancy and optimization opportunities.
* Serves as documentation for the database structure.
* Facilitates code generation and ORM mapping.
 ---
## D)    Use Case Diagrams
  

![Use Case Diagram Example](./06-151_IMG4.png)

### **When to Use**
When building **authorisation systems** and defining **user roles**.

### **Purpose**
* Define user roles and permissions.
* Organize system functionalities by user type.
* Document feature access levels.
* Plan authorization and authentication requirements.

### **Example Scenario**
>Defining different access levels for Admin, Manager, and Customer roles in a business application.

### **Benefits**

* Provides a clear authorization roadmap.
* Facilitates communication with non-technical stakeholders.
* Helps prevent security oversights.
* Serves as a requirements checklist.

---
---

## ***Phase 3: Post-Development / Maintenance***

After the system is built, UML continues to provide value **for maintenance, optimisation, and team on-boarding.**

### Diagrams Used in Post-Development / Mainteinance Phase
---
##  E)    Sequence Diagrams

![Sequence Diagrams Example](./06-151_IMG5.png)

### **When to Use**
When adding **advanced features** or **refactoring existing code**.

### **Purpose**
* Visualize internal system message flow.
* Analyse method interactions and dependencies.
* Identify optimization opportunities.
* Debug complex system behaviors.

### **Example Scenario**
>Understanding the message flow in a payment processing system to add new payment methods or troubleshoot transaction failures.

### **Benefits**

* Reveals system inefficiencies.
* Helps maintain code quality during modifications.
* Facilitates debugging of complex interactions.
* Documents system behaviour for future reference.
  
--- 
## F)    Package Diagrams
  
![Package Diagrams Example](./06-151_IMG6.png)

### **When to Use**

When **organising code architecture** or **planning modularisation**.

### **Purpose**
* Visualise code organisation and dependencies.
* Identify opportunities to reduce coupling.
* Plan code library extraction.
* Document system structure for new team members.

### **Example Scenario**
>Analysing a monolithic application to identify components that could be extracted into micro-services or separate libraries.

### **Benefits**

* Improves code maintainability.
* Facilitates team on-boarding.
* Identifies refactoring opportunities.
* Documents architectural decisions.

  
  

---

  

## **3.     Strategic Application Guidelines**
---
### When to choose the Right Diagram

While any UML diagram can technically be used at any development stage, **strategic selection based on your current needs and phase will maximize effectiveness.**

### Diagram Recommendations by Development Phase

| Development Phase    | Primary Challenge          | Recommended Diagrams           | Secondary Options |
| -------------------- | -------------------------- | ------------------------------ | ----------------- |
| *Pre-Development*    | Understanding Requirements | **Activity, Use Case**         | Sequence, Class   |
| *Pre-Development*    | Architecture Planning      | **Deployment, Package**        | Component         |
| *Active Development* | Data Modeling              | **Class, Entity-Relationship** | Package           |
| *Active Development* | Feature Planning           | **Use Case, Activity**         | Sequence          |
| *Post-Development*   | Performance Optimisation   | **Sequence, Activity**         | Package           |
| *Post-Development*   | Code Organisation          | **Package, Component**         | Class             |

---
## **Best Practices**

>🎨  Think of your **diagrams as a dynamic canvas** for your project.

1. ### **Start Simple, Grow Smart**
    
    Always begin with **high-level diagrams** to establish the big picture. Don't get bogged down in intricate details too early; you can add those layers as your understanding solidifies.
    
2. ### **Embrace Iteration, Stay Agile**
    
    Remember, diagrams are **living documents**. Update them regularly as your system evolves and requirements shift. Think of it as refining a sketch until it's a masterpiece.
    
3. ### **Collaborate, Communicate, Conquer**
    
    Use diagrams as your central **communication tool**. They're fantastic for sparking discussions, aligning your team, and fostering a shared understanding among all stakeholders.
    
4. ### **Document Decisions, Preserve Wisdom**
    
    Don't just draw! Include the **reasoning behind your architectural and design choices** directly within or alongside your diagrams. This context is invaluable for future reference and new team members.
    
5. ### **Keep Current, Stay Relevant**
    
    This is crucial: **ensure your diagrams are always synchronized with your code**. Outdated diagrams can lead to confusion and misdirection, making them more harmful than helpful.
    
---
## Practical Implementation Strategy
---

### Getting Started Checklist

#### **Before Any Project**

* [ ] Create an **Activity Diagram** to understand core user flows.
* [ ] Design a **Deployment Diagram** for initial architecture planning.
* [ ] **Review and validate** these initial diagrams with all key stakeholders.

#### **During Development**

* [ ] Build **Class Diagrams** for detailed data modeling.
* [ ] Create **Use Case Diagrams** to organize features and functionalities.
* [ ] **Update diagrams** promptly as requirements evolve or new insights emerge.

#### **After Initial Development / For Maintenance**

* [ ] Document complex interactions with **Sequence Diagrams**.
* [ ] Organize your code architecture using **Package Diagrams**.
* [ ] Plan future enhancements by selecting the **appropriate diagram types** for the task.

---

## **Common Pitfalls**

#### ⚠️ **Warning Signs:** Be aware of these common mistakes that can derail your diagramming efforts.

1. ### **The "More is More" Fallacy (Over-Documentation)**
    
    Don't fall into the trap of creating diagrams just for the sake of completeness. Focus on diagrams that **add real value**, clarify specific problems, or aid understanding. Quality over quantity, always!
    
2. ### **The "Stale Sketch" Syndrome (Outdated Diagrams)**
    
    This is a critical pitfall: diagrams that don't reflect the current state of your code lead to **confusion and mistrust**. Make it a priority to keep your diagrams **synchronized** with every code change. An outdated map is worse than no map at all!
    
3. ### **The "One-Size-Fits-All" Blunder (Wrong Tool Selection)**
    
    Resist the urge to use the same diagram for every problem. Different diagram types serve **different purposes**. Choose the one that **best addresses your current needs** and clearly communicates the information required.
    
4. ### **The "Lone Wolf" Trap (Isolation)**
    
    Never create diagrams in a vacuum. **Collaboration is key!** Involve your team throughout the diagramming process. Their input ensures accuracy, fosters shared understanding, and builds collective ownership.