
#### 3.2 Activity

| Guide  | Tittle                                                         |
| ------ | -------------------------------------------------------------- |
| **06-168** | **Elements of a UML Activity Diagram**                             |
| 06-169 | How to Design an Activity Diagram for an Online Grading System |

----
# 06-168:  Activity Diagrams



1. Introduction to Activity Diagrams

2. Core Elements

3. Detailed Element Analysis
   
   - Initial State (Start Point)
   - Activity/Action State
   - Action Flow
   - Decision Points and Branching
   - Guards
   - Final State (End Point)
   - Swim Lanes

4. Practical Application Context

5. Design Considerations and Best Practices

---


## ***1.     Introduction to Activity Diagrams***
---
UML Activity Diagrams are **behavioural diagrams which illustrate the flow of activities within a system or process**.   

They provide a **visual representation of workflows**, business processes, and algorithmic logic, making them essential tools for system analysis and design.


Activity diagrams are particularly useful for:

- Modeling business processes
- Describing use case scenarios
- Representing algorithmic workflows
- Documenting system behaviour across different actors

---

## ***2.     Core Elements***
---
Activity diagrams consist of **SEVEN** fundamental elements that work together to represent process flow:

1. **Initial State** 
   The starting point of any activity flow

2. **Activity/Action State**  
   Individual actions/processes within the workflow.

3. **Action Flow** 
   Connections between different states showing process direction

4. **Decision Points**
   Branch points where the flow can take different paths

5. **Guards**
   Conditions that determine which path to follow at decision points

6. **Final State** 
   The termination point of the activity flow

7. **Swim Lanes**
   Organisational boundaries that group activities by responsibility

---


## ***3.     Detailed Element Analysis***
---

### **1.    Initial State (Start Point)**

The **Initial State** is represented by **a thick black filled circle and marks the beginning of any activity diagram**.

This element **indicates where a user or system begins the process flow**.

![](./06-168_IMG1.png)

#### **Characteristics**

- Every activity diagram must have exactly one initial state
- Represents the trigger or starting condition for the entire process
- No incoming flows, only outgoing action flows

#### **Example Context** 

In a grading system, the initial state represents when a teacher decides to assign a test or quiz.

---

### 2.    **Activity/Action State**

**Activities** or **Action States** are the core building blocks of activity diagrams, represented by rectangular boxes (may have rounded edges depending on the UML tool used).

![](./06-168_IMG2.png)

#### **Characteristics**

- **Each box** represents **a single action, process, or state** within the workflow
- Activities should be "atomic" -> **representing one clear action or transformation**
- Most of the diagram content consists of these activity states
- Activities **represent points where data changes or alterations occur**

#### **Design Principle**

 When traversing through the diagram as a user, each activity represents a stage where something meaningful happens to the data or system state.

#### **Examples in Grading System**

- *"Generate individual question set"*
- *"Confirm question parameters"*
- "*Ask question to student"*

---

### 3.    **Action Flow**

**Action Flows** are **represented by arrows** with filled arrowheads that connect different activities, showing the direction of process flow.

![](./06-168_IMG3.png)

#### **Characteristics**

- **Indicates the sequence and direction** of activities
- Show **how data or control moves from one state to another**
- Create the **logical pathway** through the process
- Essential for understanding process dependencies

#### **Conceptual Understanding**

 Action flows <u>represent the "movement"</u> of something (data, control, or process state) from one activity to another, creating the workflow's logical structure.

---

### 4.    **Decision Points and Branching**

**Decision Points** are **represented by diamond shapes** ("square rotated 45 degrees") and indicate locations where **decisions** have to be made, where **the process flow must choose** between different paths based on specific conditions.

![](./06-168_IMG4.png)

#### **Characteristics**

- Diamond shape represents a **branch point or decision node**
- Exactly **one incoming flow and multiple outgoing flows**
- **Each outgoing flow** represents a **different possible path**
- Decisions are based on conditions or criteria evaluated at that point

#### **Example Context** 

In the grading system, a decision point might ask "Was this the last question?" leading to different actions based on the answer.

---

### 5.    **Guards**

**Guards** are **conditions** or **criteria** associated with action flows **leaving decision points**, typically represented as text labels like "yes," "no," or more complex conditional expressions.

![](./06-168_IMG5.png)

#### **Characteristic**

- Define the **conditions under which a particular flow path is taken**
- Can be simple boolean conditions or complex logical expressions
- Essential for understanding when different paths are executed
- Critical for process logic and flow control

#### **Design Consideration** 

> **The more guards and branches in a system, the higher the complexity. **

Multiple branches from a single decision point may indicate a need for design review, as changes become more difficult to propagate throughout the system.

---

### 6.    **Final State (End Point)**

The **Final State** represents the **termination of the activity flow**, shown as a circle with a smaller filled circle inside (bull's-eye pattern).

![](./06-168_IMG6.png)

#### **Characteristics**

- Indicates the completion of the entire process
- According to UML specification, e**very activity diagram should have a final state**
- **Only incoming** flows, no outgoing flows
- Represents the successful completion of the workflow

#### **Example Context** 

In the grading system, the final state occurs when results are stored in the system database.

---

### 0.    **Swim Lanes**

**Swim Lanes** are vertical or horizontal divisions that organise activities based on responsibility, role, or organisational boundaries.

![](./06-168_IMG7.png)

#### **Characteristics**

- Provide organisational structure to complex diagrams
- Clearly delineate responsibilities among different actors
- Help identify who performs which activities
- Essential for multi-actor processes

#### **Benefits**

- **Clarity of Responsibility**: Immediate visual identification of who does what
- **System Organization**: Clear separation of system, user, and external actor responsibilities
- **Process Understanding**: Easier comprehension of role interactions and handoffs

#### **Example Structure in Grading System:**

- **Teacher Lane**: Activities related to test creation and result review
- **System Lane**: Automated processes like question generation and result storage
- **Student Lane**: Activities performed by students during the assessment

***


## ***4.     Practical Application Context***
---
The grading system example demonstrates how these elements work together in a real-world scenario:

1. **Process Initiation**: Teacher decides to create a quiz (Initial State)
2. **System Actions**: Generate questions, configure parameters (Activities)
3. **Flow Control**: Questions presented in sequence (Action Flows)
4. **Decision Logic**: Determine if more questions remain (Decision Points with Guards)
5. **Process Completion**: Store results in database (Final State)
6. **Responsibility Distribution**: Clear separation between teacher, system, and student actions (Swim Lanes)

---


## ***5.     Design Considerations and Best Practices***
---
### Complexity Management

- **Minimize Branching**: Excessive decision points increase system complexity
- **Atomic Activities**: Each activity should represent one clear, indivisible action
- **Clear Flow Direction**: Ensure action flows create logical, easy-to-follow pathways

### Organizational Clarity

- **Effective Swim Lanes**: Use swim lanes to clearly separate responsibilities
- **Consistent Naming**: Use clear, descriptive names for activities and guards
- **Logical Grouping**: Group related activities within appropriate swim lanes

### Maintainability

- **Impact Analysis**: Consider how changes propagate through multiple branches
- **Documentation**: Ensure guards and decision conditions are clearly documented
- **Validation**: Verify that all paths lead to appropriate final states

---
