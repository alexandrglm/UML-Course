


#### 3.3  Use Case

| Guide      | Tittle                                                            |
| ---------- | ----------------------------------------------------------------- |
| 07-172     | Overview of UML Use Case Diagram Elements                         |
| **07-173** | **Example: Build a Marketing Automation System Use Case Diagram** |

---
# 07-173:  Use Case Diagram with an example



1. System Overview

2. Actor Analysis
    - Marketing Specialist
    - Customer/Lead

3. Use Case Breakdown
    - External System Functions
    - Web Dashboard Subsystem

4. Relationship Patterns

5. Development Implementation Insights

6. System Architecture Implications

7. UML Value Demonstration

---

## ***1.      System Overview***
---
The Marketing Automation System use case diagram demonstrates a complete implementation of all use case diagram elements working together to model a real-world business application.   

It's based/derivated from what we walked through the Activity Diagram section, at least as actors' part. ![small](./07-173_IMG2.png)

This system manages the entire customer journey from lead generation to conversion, providing different access levels for marketing specialists and customers.

**Core System Purpose**

- Track customer journeys from lead to sale
- Automate marketing processes and notifications
- Provide reporting and contact management capabilities
- Enable dynamic form creation and customer interaction

![large](07-173_IMG1.png)

---


## ***2.      Actor Analysis***
---
## A)   Marketing Specialist

#### **Role Definition**
Administrative user with comprehensive system access, functioning as the primary system operator.

#### **Available Use Cases**

- **Manage Journeys and Shapes**: Create and modify customer journey workflows
- **Get Notifications Regarding Journeys**: Receive alerts about customer journey events
- **Get Reports**: Access analytics and performance data
- **Manage Contacts**: Handle customer and lead information
- **Generate Forms**: Create dynamic forms for customer interaction
- **Get Messages**: Access communication logs and customer messages
- **Visit Resources**: View system resources and documentation

### **Access Pattern** 

The marketing specialist has the broadest system access, including both external functions and full web dashboard capabilities.

---

## B)   Customer/Lead

####  **Role Definition**

External users interacting with the marketing system, representing potential or existing customers.

#### **Available Use Cases**

- **Trigger Journey Events**: Initiate marketing workflows (e.g., signing up via website forms)
- **Get Messages**: Receive communications from the marketing system
- **Visit Resources**: Access provided materials and content
- **Fill Out Forms**: Complete dynamic forms created by marketing specialists


#### **Access Pattern**

Customers have limited, interaction-focused access designed to capture engagement and move them through marketing funnels.

---


## ***3.      Use Case Breakdown***
---
### a)     External System Functions

Functions that operate outside the web dashboard subsystem:
##### **1)     Manage Journeys and Shapes**

- **Purpose**: Configure customer journey workflows and decision trees
- **Implementation Implication**: Requires workflow engine and visual journey builder
- **Actor Access**: Marketing Specialist only

##### **2)     Get Notifications Regarding Journeys**

- **Purpose**: Alert marketing specialists about customer journey events
- **Implementation Implication**: Email notification system required
- **Actor Access**: Marketing Specialist only
- **Special Relationship**: Connected to "Trigger Journey Events" via "notify" relationship

##### **3)      Trigger Journey Events**

- **Purpose**: Customer actions that initiate or advance marketing workflows
- **Implementation Implication**: Event tracking and workflow trigger system
- **Actor Access**: Customer/Lead only
- **Connection**: Links to notification system for marketing specialists

---
### b)     Web Dashboard Subsystem

The web dashboard contains five integrated use cases representing the core administrative interface:

##### **4)     Get Reports**

- **Purpose**: Analytics and performance monitoring
- **Implementation Requirement**: Reporting interface with data visualization

##### **5)     Manage Contacts**

- **Purpose**: Customer and lead information management
- **Implementation Requirement**: Contact database and management interface

##### **6)      Generate Forms**

- **Purpose**: Dynamic form creation for customer engagement
- **Implementation Requirement**: Form builder components and rendering system

##### **7)       Get Messages**

- **Purpose**: Communication log access and management
- **Implementation Requirement**: Message storage and retrieval system

##### **8)      Visit Resources**

- **Purpose**: Access to system documentation and materials
- **Implementation Requirement**: Resource library and access control

---


## ***4.      Relationship Patterns***
---
### **Direct Actor-Use Case Relationships**


#### - **Marketing Specialist Connections**
![small](./07-173_IMG04.png)
- Direct access to all external functions
- Full access to web dashboard subsystem
- Comprehensive system privileges


#### **- Customer/Lead Connections**
![small](./07-173_IMG05.png)
- Limited to customer-facing interactions
- No administrative access
- Focused on engagement and data collection

---

### **Inter-Use Case Relationships**

#### **- "Notify" Relationship**
![small](./07-173_IMG06.png)
- **Source**: Trigger Journey Events
- **Target**: Get Notifications Regarding Journeys
- **Purpose**: Automatic notification flow when customers take actions
- **Implementation**: Event-driven notification system

---


## ***5.      Development Implementation Insights***
---
### **System Architecture Requirements**
---
##### **Email Notification System** 

The placement of "Get Notifications Regarding Journeys" outside the web dashboard indicates a separate email notification service that alerts marketing specialists of customer actions.

---
##### **Form System Components** 

The "Generate Forms" use case implies a dual-component system:

- **Admin Component**: Form builder interface for marketing specialists
- **Customer Component**: Form rendering and submission system for customers
- **Data Flow**: Form submissions feed into reporting system

---
##### **Web Dashboard Structure** 

Five distinct functional areas requiring:

- Reporting interface with analytics
- Contact management system
- Message handling capabilities
- Resource library
- Form generation tools

---
### **Authorisation Engine Requirements**

##### **Role-Based Access Control**

- **Marketing Specialist**: Full system access including administrative functions
- **Customer/Lead**: Limited to interaction and engagement functions
- **Clear Boundaries**: Web dashboard requires authentication and role verification


---


## ***6.      System Architecture Implications***
---

### Component Distribution

#### **External Services**

- Journey management engine
- Notification service
- Event tracking system


#### **Web Dashboard Module**

- Integrated administrative interface
- Reporting subsystem
- Contact management
- Form builder
- Resource management

---
### Data Flow Patterns

#### **Customer Journey Flow**

1. Customer triggers journey event (signup, form submission)
2. System processes event and updates journey state
3. Marketing specialist receives notification
4. Reports updated with new engagement data

#### **Form Interaction Flow**

1. Marketing specialist generates form in web dashboard
2. Customer accesses and fills out form
3. Form data feeds into contact management and reporting systems

---


## 7.      UML Value
---
## 1. Efficiency of Visual Modeling

### **Information Density**

This compact diagram conveys system architecture information that would require extensive written documentation to communicate effectively.

### **Clear Authorisation Framework**

The visual representation immediately shows:

- Who can access what functionality
- Which components belong to which system modules
- How different user types interact with the system

---
## 2. Development Planning Benefits

### **Component Identification**

Developers can immediately identify required system components:

- Web dashboard interface
- Email notification service
- Form generation and rendering systems
- Journey management engine
- Reporting infrastructure


### **Feature Scope Understanding**

Eight use cases reveal significant functionality requirements including:

- Dynamic form creation
- Customer journey tracking
- Automated notifications
- Comprehensive reporting
- Contact management


---
## 3. UML Power Demonstration

#### **Simple Tools, Complex Systems**

Using only four UML elements (actors, use cases, subsystems, relationships), the diagram models an entire marketing automation platform.



#### **Longevity and Effectiveness** 

The enduring relevance of UML is demonstrated by how these simple visual tools can capture complex system requirements clearly and efficiently.


#### **Communication Bridge** 

The diagram serves multiple audiences:

- **Developers**: Clear implementation requirements
- **Business Stakeholders**: Understanding of system capabilities
- **System Architects**: High-level system organization
