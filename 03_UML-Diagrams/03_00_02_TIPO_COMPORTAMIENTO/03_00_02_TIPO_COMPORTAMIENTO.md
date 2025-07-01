

| Guide  | Tittle                                  |
| ------ | --------------------------------------- |
| 06-161 | Overview of Structural Diagrams in UML  |
| **06-162** | **Overview of Behavioural Diagrams in UML** |

---
# 06-162:  Behavioural Diagrams



1. Introduction to Behavioural Diagrams

2. Activity Diagrams
   2.1. Purpose and Non-Technical Accessibility  
   2.2. Core Elements  
   2.3. Coffee Ordering Service Example  
   2.4. User Experience Modeling  

3. Use Case Diagrams
   3.1. Authorization System Illustration  
   3.2. Core Components  
   3.3. Marketing Engine Example  
   3.4. Actor-Based Access Control  

4. State Machine Diagrams
   4.1. Data Life-cycle Visualisation  
   4.2. Essential Elements  
   4.3. Lead Funnel Example  
   4.4. Comparison with Activity Diagrams  

5. Sequence Diagrams
   5.1. Message-Based System Design  
   5.2. Implementation-Focused Elements  
   5.3. Phone Parser Example  
   5.4. Input-Output System Thinking  

6. Best Practices and Implementation Guidelines

7. Tools and Diagram Selection Criteria

---



## ***1.    Introduction to Behavioural Diagrams***
---
Behavioural diagrams represent the dynamic aspects of UML modeling, illustrating **how systems should behave, act, and interact with internal components and external actors.** 

Unlike structural diagrams that show what exists in the system, behavioural diagrams **focus on what happens** when the system runs, giving clarity for understanding the system behaviour, user interactions, and the dynamic relationships between system components.


|                                  | Purpose                              |
| -------------------------------- | ------------------------------------ |
| **Use Case Diagram**             | Actors and system interactions       |
| **Activity Diagram**             | Workflows and business processes     |
| **State Machine Diagram**        | Object states and transitions        |
| **Sequence Diagram**             | Time-ordered interactions            |
| **Communication Diagram**        | Object interactions with links       |
| **Timing Diagram**               | Interactions with timing constraints |
| **Interaction Overview Diagram** | Control flow between interactions    |


The **FOU**R primary behaviourañ diagrams covered are:

- **Activity Diagrams**: Workflow and process modeling
- **Use Case Diagrams**: User interaction and system functionality
- **State Machine Diagrams**: Object state transitions and life-cycle
- **Sequence Diagrams**: Message passing and system interactions


---

## ***2.    Activity Diagrams***
---
### Purpose and Non-Technical Accessibility

Activity diagrams are exceptionally powerful for visualising system workflows and user processes.   

Their greatest strength lies in their **accessibility to non-technical stakeholders**. 
Executives and business and  users, who may have no understanding of UML notation, can easily comprehend activity diagrams, making them invaluable for stakeholder communication.

#### **Benefits**

- **Improving the Communication**: Bridge between technical and non-technical teams
- **Process Documentation**: Clear visualisation of business workflows
- **System Planning**: Foundation for building systems from scratch
- **User Journey Mapping**: Complete user life-cycle visualisation

### Core Elements

Activity diagrams comprise six essential components:

1. **Initial State**: Starting point of the process (solid black circle)
2. **Activity/Action State**: Individual steps or processes (rounded rectangles)
3. **Action Flow**: Directional arrows showing process flow
4. **Decisions/Branching**: Diamond shapes representing choice points
5. **Guards**: Conditions that must be met for transitions
6. **Final State**: End point of the process (solid black circle with outer ring)

---
### Coffee Ordering Service Example

The coffee ordering service demonstrates how activity diagrams capture complex user interactions:

#### **Process Flow**

1. User initiates order online
2. Decision point based on user selection
3. Multiple pathways depending on choices:

   - Product search and selection
   - Product viewing and details
   - Cart addition and management
   - Checkout and payment processing

This single diagram encapsulates the entire user experience, providing developers with a clear roadmap for application implementation.

### User Experience Modeling

Activity diagrams excel at high-level process modeling because they focus on activities rather than technical implementation details. They answer critical questions:

- What happens when users search for products?
- How do users navigate product selection?
- What decision points exist in the user journey?
- How do different user choices affect the workflow?

---


## ***3.    Use Case Diagram***s
---
### Authorisation System Illustration

Use case diagrams **provide high-level visualisation of system functionality and user access rights.**  

They're particularly valuable for designing authorization systems, clearly showing what different user types can access and accomplish within the system.

#### **Primary Applications**

- **Authorisation Design**: Defining user roles and permissions
- **System Scope Definition**: Boundary setting for system functionality
- **Stakeholder Communication**: Clear presentation of system capabilities
- **Feature Planning**: Comprehensive view of system features


### Core Components

Use case diagrams consist of **FOUR** fundamental elements:

1. **Use Cases**: System functionality represented as ovals
2. **Actors**: Users or external systems (stick figures)
3. **Subsystems**: Grouped functionality within system boundaries
4. **Relationships**: Connections showing interactions and dependencies

---
### Marketing Engine Example

The marketing engine use case diagram illustrates dual-actor scenarios:

**Actor Roles:**

- **Marketing Specialist**: Administrative access and content creation
- **Customer**: End-user interaction and consumption

**Relationship Types:**

- **Association**: Direct actor-to-use case connections
- **Include**: Required functionality dependencies
- **Extend**: Optional functionality extensions

Different actors access the same use cases through different pathways, demonstrating how authorization systems control user behaviour and access rights.

### Actor-Based Access Control

Use case diagrams effectively model complex authorization scenarios:

- **Employee vs. Admin**: Different access levels to timesheet systems
- **Customer vs. Specialist**: Varying capabilities within the same system
- **Role-Based Permissions**: Clear visualisation of who can do what

---


## ***4.    State Machine Diagrams***
---
### Data Life-cycle Visualisation

State machine diagrams represent one of computer science's fundamental concepts, **visualising how data and objects transition through different states during system life-cycle.**  

They focus on the various stages of system components and the conditions that trigger state changes.

#### **Core Purpose**

- **State Transition Modeling**: How objects change over time
- **Condition-Based Logic**: Rules governing state changes
- **System Behaviour**: Dynamic aspects of system components
- **Life-cycle Management**: Complete object life-cycle visualisation


### Essential Elements

State machine diagrams incorporate five key components:

1. **Entry Point**: Initial state (solid black circle)
2. **Choices**: Decision points determining transitions
3. **Constraints**: Conditions governing state changes
4. **States**: Stable conditions or situations (rectangles)
5. **Transitions**: State-to-state movements (arrows)

---
### Lead Funnel Example

The lead funnel state machine demonstrates customer progression:

#### **State Progression**

- **Visitor**: Initial user state
- **Converted**: Post-form submission state
- **Lead**: Qualified prospect state
- **Customer**: Final conversion state

Each transition requires specific conditions, illustrating how business rules govern customer progression through the sales funnel.

---
### Comparison with Activity Diagrams

State machine diagrams share similarities with activity diagrams but focus on different aspects:

#### **What State Machine Focus on**

- Object states and transitions
- Condition-based changes
- Data life-cycle management


#### **What Activity Diagram Focus on**

- Process workflows
- User activities
- Sequential actions


>**The choice between diagrams depends on whether you're modeling object states or process workflows.**

---

## ***5.    Sequence Diagrams***
---

### Message-Based System Design

Sequence diagrams ***represent sophisticated system interactions through message passing***.     

Senior developers favour these diagrams because they model applications as systems of communicating components, both internal and external.   

They provide implementation-level detail that directly translates to code structure.

#### **Strategic Value**

- **Implementation Guidance**: Direct translation to code
- **System Architecture**: Message-based system design
- **Integration Planning**: External system communication
- **Debugging Aid**: Understanding system message flow



### Implementation-Focused Elements

Sequence diagrams comprise **FOUR critical components**:

1. **Class Roles/Participants**: System components involved in interactions
2. **Activation/Execution Occurrence**: Active processing periods (wide rectangles)
3. **Messages** (And Responses): Communications between components (arrows)
4. **Lifelines**: Vertical lines representing component existence over time


---
### Phone Parser Example

The phone parser sequence diagram illustrates complex system interactions:

#### **Message Flow**

1. **Input**: Data to parse enters the system
2. **Self-Message**: Parse engine processes internally ("delete all symbols except numbers")
3. **External Message**: Validation request to digit length validator
4. **Response Message**: Validation result (dotted arrow)
5. **Output**: Parsed phone number result

This diagram provides complete input-output understanding, showing both the goal and the implementation pathway.

----
### Input-Output System Thinking

Sequence diagrams promote systematic thinking about:

- **Method Inputs**: What data enters each component
- **Expected Outputs**: What results each component produces
- **Message Contracts**: Clear interface definitions
- **System Dependencies**: Component interaction requirements


>**Understanding systems through message passing creates clear implementation roadmaps and simplifies complex system architecture into manageable communication patterns.**

---


## ***6.    Best Practices and Implementation Guidelines***
---
### Activity Diagram Guidelines

- Start with user entry points and identify all possible endpoints
- Use clear, descriptive labels for activities and decision points
- Keep diagrams focused on single processes or user journeys
- Include all significant decision points and alternative paths
- Validate workflows with business stakeholders

### Use Case Diagram Recommendations

- Clearly define system boundaries before identifying use cases
- Focus on user goals rather than system features
- Use consistent actor representations across diagrams
- Document relationships between related use cases
- Regularly review access rights and permissions with stakeholders

### State Machine Diagram Best Practices

- Identify all possible states before modeling transitions
- Define clear conditions for each state transition
- Include error states and exception handling
- Document state entry and exit actions
- Validate state logic with domain experts

### Sequence Diagram Guidelines

- Focus on significant message exchanges, avoid trivial interactions
- Use consistent naming conventions for participants
- Show both successful and error message flows
- Include return messages for complex interactions
- Align diagrams with actual implementation architecture



### General Behavioural Diagram Tips

- **Diagram Selection**: Choose diagrams based on specific modeling needs
- **Stakeholder Alignment**: Match diagram complexity to audience technical level
- **Iterative Refinement**: Continuously update diagrams as understanding evolves
- **Implementation Traceability**: Ensure diagrams can guide actual development
- **Cross-Diagram Consistency**: Maintain consistency across different diagram types

---


## ***7.    Diagram Selection Criteria***
---
### Diagram Selection Framework

Each behavioural diagram serves specific scenarios:

### **Use Activity Diagrams When**

- Modeling business processes
- Communicating with non-technical stakeholders
- Planning user experience workflows
- Documenting system processes


#### **Use Use Case Diagrams When**

- Defining system scope and boundaries
- Designing authorization systems
- Planning system features
- Communicating with business analysts


#### **Use State Machine Diagrams When**

- Modeling object life-cycles
- Designing state-dependent behaviour
- Planning condition-based logic
- Understanding data transitions


#### **Use Sequence Diagrams When**

- Designing system interactions
- Planning API integrations
- Understanding message flows
- Creating implementation blueprints

---
