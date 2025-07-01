
| Guide      | Tittle                                             |
| ---------- | -------------------------------------------------- |
| 06-152     | Introduction to UML Components and Common Elements |
| 06-153     | Common UML Components: Frames                      |
| 06-154     | Common UML Components: Classifiers                 |
| 06-155     | Common UML Components. Stereotypes                 |
| **06-156** | **Common UML Components: Comments and Notes**      |
| 06-157     | Common UML Components: Dependencies                |
| 06-158     | Common UML Components: Features and Properties     |
| 06-159     | Quiz:   Introduction to UML                        |

---

# 06-156: UML      COMMENTS - NOTES

### 1. What Comments and Notes are

- **1.1** Definition and Purpose
- **1.2** Terminology Variations
- **1.3** Role in UML Documentation

### 2. Characteristics and Properties

- **2.1** Visual Representation
- **2.2** Connection Methods
- **2.3** Content Flexibility

### 3. Comments vs Stereotypes

- **3.1** Formality Levels
- **3.2** Use Case Distinctions
- **3.3** Semantic Differences

### 4. Application Scenarios

- **4.1** Developer Communication
- **4.2** Stakeholder Clarification
- **4.3** Technical Documentation

### 5. Visual Elements and Notation

- **5.1** Standard Notation
- **5.2** Connection Lines
- **5.3** Positioning Guidelines

### 6. Practical Examples

- **6.1** Class Diagram Applications
- **6.2** Attribute Clarification
- **6.3** Method Documentation

### 7. Implementation Guidelines

- **7.1** When to Use Comments
- **7.2** Content Best Practices
- **7.3** Placement Strategies

### 8. Best Practices and Tips

- **8.1** Writing Effective Comments
- **8.2** Avoiding Over-Documentation
- **8.3** Maintenance Considerations

---


## ***1.     What Comments and Notes are***
---
![large](06-156_IMG1.png)
### 1.1     Definition and Purpose

UML Comments (also referred to as **Notes**) are **supplementary documentation elements that provide descriptive markup within UML diagrams**.

They serve as ***a bridge between formal UML notation and natural language* explanation,** enabling clearer communication of design intent and implementation details.

Comments are **non-formalized** annotations that can contain virtually any descriptive text, making them highly flexible tools for enhancing diagram readability and comprehension.

---
### 1.2     Terminology Variations

The terminology used for these elements can vary depending on the context and tools:

- **Comments** - More commonly used in software development contexts
- **Notes** - Often preferred in academic and formal documentation
- **Annotations** - Sometimes used in specialized UML tools
- **Remarks** - Occasionally found in legacy documentation

Both "Comments" and "Notes" refer to the same UML construction-concept and are also accepted to be used interchangeably.

---
### 1.3     Role in UML Documentation

Comments serve multiple critical functions in UML modeling:

- **Clarification** of complex or ambiguous elements
- **Context provision** for non-technical stakeholders
- **Implementation guidance** for development teams
- **Business rule documentation** within technical diagrams
- **Assumption recording** for future reference

---

## ***2.     Characteristics and Properties***
---
### 2.1     Visual Representation

UML Comments are represented by **rectangular boxes** with specific visual characteristics:

![large](06-156_IMG2.png)

- **Shape**: Rectangle with a "dog-eared" corner (folded corner effect)
- **Background**: Typically yellow or light-colored
- **Border**: Solid thin line
- **Corner**: Small triangular fold in the upper-right corner

### 2.2     Connection Methods

Comments connect to UML elements through:

- **Dotted lines** (dashed lines) - The standard connection method
- **Dependency arrows** - Used in some specialized cases
- **Direct positioning** - When the context makes the association clear

### 2.3     Content Flexibility

Unlike other UML elements, comments have minimal restrictions on content:

- **Free-form text** - No specific format requirements
- **Multiple languages** - Can be written in any natural language
- **Mixed content** - Can include technical and business terminology
- **Variable length** - From brief annotations to detailed explanations

---

## ***3.     Comments vs Stereotypes***
---
### 3.1     Formality Levels

| Aspect        | Comments                      | Stereotypes                  |
| ------------- | ----------------------------- | ---------------------------- |
| **Formality** | Informal, descriptive         | Formal, standardized         |
| **Purpose**   | Explanation and clarification | Classification and extension |
| **Content**   | Free-form text                | Predefined keywords          |
| **Usage**     | Communication aid             | Semantic enhancement         |

---
### 3.2    Comments VS Stereotypes

### **Comments are ideal for:**

- Explaining business rules
- Providing implementation hints
- Clarifying complex relationships
- Adding context for stakeholders

### **Stereotypes are ideal for:**

- Extending UML metamodel
- Formal classification (e.g., «Controller», «Model», «View»)
- Tool-specific annotations
- Architectural pattern identification

---
### 3.3     Semantic Differences

- **Comments** do not affect the semantic meaning of the model
- **Stereotypes** extend and modify the semantic interpretation of elements
- **Comments** are purely documentational
- **Stereotypes** can influence code generation and tool behavior
---


## *4.     Application Scenarios*
---
### 4.1     Developer Communication

Comments excel in scenarios where developers need additional context:

- **Algorithm explanations** for complex methods
- **Performance considerations** for critical operations
- **Integration notes** for external system interactions
- **Maintenance warnings** for sensitive code areas

---
### 4.2     Stakeholder Clarification

When presenting UML diagrams to non-technical audiences:

- **Business process explanations** in activity diagrams
- **User interaction clarifications** in use case diagrams
- **Data flow descriptions** in sequence diagrams
- **System boundary explanations** in deployment diagrams

---
### 4.3     Technical Documentation

Comments serve as embedded documentation for:

- **Design decisions** and their rationale
- **Constraint explanations** and their implications
- **Assumption documentation** for future reference
- **Requirements traceability** links

---


## ***5.     Visual Elements and Notation***
---
### 5.1     Standard Notation

The UML specification defines specific visual elements for comments:

```
┌─────────────────◣
│ Comment text    │
│ goes here...    │
└─────────────────┘
```

![large](./06-156_IMG03.png)

**The folded corner (◣) is a distinctive feature that immediately identifies the element as a comment.**

---
### 5.2 Connection Lines

Connection lines between comments and model elements follow these conventions:

- **Style**: Dashed or dotted line
- **Direction**: No specific arrowhead required
- **Multiple connections**: One comment can connect to multiple elements
- **Positioning**: Lines should not obscure other diagram elements

---
### 5.3 Positioning Guidelines

Effective comment placement follows these principles:

- **Proximity**: Place comments near the elements they describe
- **Clarity**: Avoid overlapping with other diagram elements
- **Readability**: Ensure connection lines are clear and unambiguous
- **Balance**: Maintain visual harmony within the diagram

---


## ***6.     Practical Examples***
---
### 6.1     Class Diagram Applications

---
### 6.2     Attribute Clarification

Each comment in the example above serves a specific purpose:

1. **Title attribute comment**: Indicates business rule (required field)
2. **Slug attribute comment**: Provides implementation guidance (auto-generation)
3. **TopTen attribute comment**: Explains query scope functionality

---
### 6.3     Method Documentation

**Comments can also document methods** and their behavior:

```
┌─────────────────┐
│ + authenticate()│ ←──┐
└─────────────────┘    │
                       │
┌─────────────────────────◣
│ Implements OAuth 2.0    │
│ with JWT tokens         │
└─────────────────────────┘
```

---


## ***7.     Implementation Guidelines***
---
### 7.1     When to Use Comments

Comments should be used when:

- **Standard UML notation** is insufficient for clarity
- **Business rules** need explicit documentation
- **Implementation details** require specification
- **Non-technical stakeholders** need explanation
- **Complex relationships** require clarification

---
### 7.2     Content Best Practices

Effective comment content should be:

- **Concise** yet informative
- **Clear** and unambiguous
- **Relevant** to the associated element
- **Current** and up-to-date
- **Consistent** in style and terminology

---
### 7.3     Placement Strategies

Strategic comment placement involves:

- **Logical grouping** of related comments
- **Visual balance** within the diagram
- **Connection clarity** to avoid confusion
- **Space efficiency** to maintain readability
- **Update accessibility** for maintenance

---


## ***8.     Best Practices and Tips***
---
### *8.1     Writing Effective Comments*

## 🗿**Do**

- Use clear, simple language
- Focus on "why" rather than "what"
- Include business context when relevant
- Keep comments concise but complete
- Use consistent terminology throughout

## 🙅** Don't**

- Duplicate information already clear from the diagram
- Use overly technical jargon without explanation
- Create comments that will quickly become outdated
- Clutter diagrams with excessive annotations

---
### 8.2     *Avoiding Over-Documentation*

Signs of over-documentation include:

- **Redundant information** already evident from naming
- **Excessive detail** that obscures the main diagram
- **Trivial explanations** of obvious elements
- **Outdated comments** that no longer reflect reality

---
### 8.3     *Maintenance Considerations*

#### **Regular Review Process**

- Schedule periodic comment reviews during design updates
- Remove obsolete comments promptly
- Update comments when requirements change
- Validate comment accuracy with stakeholders

#### **Version Control**

- Track comment changes alongside diagram evolution
- Document rationale for comment modifications
- Maintain comment history for traceability


#### **Team Coordination**

- Establish comment writing standards
- Define review processes for comment additions
- Ensure consistent comment quality across team members

---
### 8.4     *Tool-Specific Considerations*

Different UML tools may have variations in:

- **Comment formatting** options
- **Connection line** styles
- **Export capabilities** for comments
- **Search functionality** within comments

---
### 8.5 *Accessibility and Internationalisation*

Consider these factors for broader accessibility:

- **Language consistency** within project contexts
- **Cultural sensitivity** in explanations
- **Technical translation** accuracy
- **Screen reader compatibility** in digital formats
