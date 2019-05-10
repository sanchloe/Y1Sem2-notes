# Week 2 and 3
# From Requirements to Analysis
## Tips
- Requirement analysis
- Functional and non-functional
- What is software engineering
- What are software requirements
- Generic vs customized products
- Four stage process

## What is Software Engineering
- The application of a systematic, disciplined, quantifiable approach to the development, operation, and maintenance of software:
    1. Define software requirements
    2. Perform software design
    3. Software construction
    4. Software testing
    5. Software maintenance tasks
    6. Software project management

## Software Development
Requirement Analysis > Design > Development > Testing > Maintenance

## Requirement Analysis
Software engineering task bridging the gap between system requirements engineering and software design
1. Identify customers needs
2. Evaluate system for feasibility
3. Perform economic and technical analysis
4. Allocate functions to system elements
5. Establish schedule and constraints
6. Create system definitions

## Software Requirement Analysis Phase
1. Problem recognition
2. Evaluation and synthesis (focus is on **WHAT** not HOW)
3. Modeling
4. Specification
5. Review

## Requirements
- Features of system or system function used to fulfill system purpose
- Focus on customer's **needs and problems** not on solutions
  - Requirements definition document (for customer)
  - Requirements specification document (for programmer, technical staff)

## Software Requirements
- Defines the functionality and constraints of the system
  - Answers the question **"what" , not "how"**
- Two kinds of requirements
    1. Functional requirements
        - Describes **what** a software system should do
    2. Non-functional requirements
        - Place constraints on **how** the system will do so

## Software Products (Generic VS Customized)

| Generic Products  | Customized Products |
|:------------------|:--------------------|
|Stand-alone systems that are marketed and sold to any customer who wishes to buy them |Software that is commissioned by a specific customer to meet their own needs|
|**Specification of what the software should do** is owned by the software developer and **decisions on software change** are made by the developer |**Specification of what the software should do** is owned by the customer and **decisions on software change** are made by the customers |
|Examples: Graphics programs, project management tools, CAD software, software for specific markets such as appointment systems for dentists | Examples: Embedded control systems, air traffic control software, traffic monitoring systems |

## Domain Requirements
- Describe the system characteristics and features that reflect the domain
- May be new functional requirements, constraints on existing requirements or define specific computations
- If doman requirements are not satisfied, the system may be unworkable

## Four Stage Process
1. **Feasibility Study**
   - Find out if the current user needs to be satisfied given the available technology and budget
2. **Requirements Analysis**
   - Find out what stakeholders require from the system
3. **Requirements Definition**
   - Define the requirements in a form understandable to the **customer**
4. **Requirements Specification**
   - Define the requirements in detail in a form understandable to the **developers**

## Problems with natural language
1. Lack of clarity
2. Requirements Confusion
   - Functional and non-functional requirements are mixed-up
3. Requirements mixed
   - Several different requirements may be expressed together
---
# Week 4
# Interaction Diagrams
## Tips
- Class diagram, activity diagram

## Unified Modeling Language (UML)
- UML specifies a number of interaction diagrams to model dynamic aspects of the system
  - Messages moving among objects/classes
  - Flow of control among objects
  - Sequences of events

## Sequence Diagrams
- Shows **interaction** between objects over a specific **period time**
- Show the lifetime of an object
- Describe the flow of the messages, events and actions between objects over a period of time
- Used during **analysis and design** to document and understand the logical flow of the system
- Describes the dynamic behavoir between objects of the system

## Key Parts
1. Participants: object or entity that acts in the diagram
2. Message
3. Axes: 
   - horizontal: which object is acting
   - vertical: time (down > forward in time)

## Activity Diagram
- Describe how activities are coordinated
- Support parallel behaviour
- Analyse use case, understand workflow across many use cases

## Summary
- UML are useful for **staying organised** and for **communication** with team members or clients
---
# Week 5
# Software Design
- UML
- Advantages of UML
- Why people started using UML
- Types of UML
- Name system on top tight of use case diagram
- Include and extend, generalization (arrow points towards parents)

## UML (Unified Modelling Language)
- A family of graphical notations that help in describing, desgining and organising object oriented software systems
- A industry-standard graphical language for specifying, visualizing, constructing, and documenting the artifacts of software systems

## Advantages of UML
1. Captures business processes
2. Enhance communication and ensures the right communication
3. Capability to capture the logical software architecture independent of the implementation language
4. Manages the complexity
5. Enables reuse of the design

## Why use UML?
1. Use graphical notation: clearer than natural language(imprecise) and code(too detailed)
2. Gives an **overall view of a system**
3. Not dependent on any one language or technology
4. Moves us from fragmentation to standardization

## Types of UML diagrams
## 1. Use Case diagrams
- Describes the **functional behavior** of the system as seen by the user
- A set of scenarios tied together by a common user goal
- Scenario is a sequence of steps describing an interaction between a user and a system 

A full use-case model comprise of:
1. **Overview of visible use scenarios** in the system
2. **Actors** that interact with the system
3. **Linkages** between use cases
   
- A document describing the use case in details :
 1. Actor
    - A role that a user plays with respect to the system: user, external system(another system)
    - Has a unique name and an optional description

## Why use use cases?
1. For **functional requirements analysis and specification**
2. A use case is a description of **how a user will use the system-to-be to accomplish business goals**
3. Use cases work well as an analytical tool
4. Easy to understand, both for the business and from the technological point of view
    - Used to **gather requirements of a system**
    - Used to get an **outside view of a system**
    - Identify **external and internal factors** influencing the system

## Relationships betweeen use cases
1. Generalization: uses cases that are **specialized versions of other use cases**
    - Child use case inherits the behaviour and meaning of the parent use case
    - Child may add to or ovveride the behavior of its parent

![usecase](./images/SE.4.png)

2. Include: use cases that are **included** as parts of other use cases. enable to factor **comon behaviour**
   - Explicitly incorporates the behaviour of another use case
   - Included use case occurs as a part of some larger base that **includes it**
   - `<<include>>` relationship represents common functionality needed in more than one use case
   - Arrow points from base use case towards right hand side

![include](./images/SE.5.png)

3. Extend: use cases that `<<extend>>` the behaviour of oher core use cases. Enable to factor variants
    - Implicitly incorporates the behaviour of another use case at certain points called **extension points**
    - The extension of the use case to include optional functionality
    - Arrow points from extended area towards left hand side
    - How to determine if a use case is being extended:
        1. Is this use case optional?
        2. Is the base use case complete without this use case?
        3. Is the execution of this use case conditional?
        4. Does this use case change the behaviour of the base use case?

![include](./images/SE.6.png)

## 2. Class diagrams
- Describe the static structure of the system: Objects, attributes and associations
- **Structure and behavior** in the use cases
- Graphical way to illustrate relationships between classes in an Object Oriented System
- Used for **requirement capture**, end user interaction

## Object Oriented(Class) Relationships
1. Dependency relationship
   - Indicates a semantic relationship between two or more elements
2. Generalization
    - Connects a subclass to its supercalss
    - Denotes an inheritance of attributes and behavior

![generalization](./images/SE.7.png)

3. Association
    - Represent relationship between instances of classes

![association](./images/SE.8.png)

   - **Aggregation**: Specifies a whole-part relationship between an aggregate and a constituent part
      - Denotes by a hollow-diamond adornment on the association
      - Container and containee relationship
   - **Composition** : Indicates a strong ownership and coincident lifetime of parts by the whole
      - Denoted by a filled-diamond adornment on the association
---
# Week 6 and 7
# Prototyping
## Tips
- Definition of prototyping
- Importance of prototype 
- Types of prototyping
- Problems with prototyping
- Advantages and disadvantages

## Definition
The process of quickly putting together a working model(a prototype) in order to **test various aspects** of a **design, illustrate ideas** or features and gather **early user feedback** 

## Need for prototyping
- Enables us to **explore the problem space** with the stake holders
- As a requirements artifact to **initially envision** the system
- As a design artifact that enables us to **explore the solution space** of your system
- A vehicle for you to **communicate the possible UI** design(s) of your system
- A potential foundation from which to **continue developing the system**

## Importance of prototyping
1. Allow us to reduce the cost and time-to-market of a system
2. For companies building critical systems, prototyping would help them **perform formal verification**. Provide high level of reliability in the system design and implementation

## Advantages and Disadvantages of Prototyping
![prototype](./images/SE.2.png)

## Types of Prototyping
## 1. Throw Away Prototype
- Developed from the **initial requirements** but is not used for the final project
- Written specifications of the requirements
- Some believe that this type is a **waste of time** because it won't be used in the final project
- Concentrates experimenting with the customer requirements that are poorly understood

|Advantages|Disadvantages|
|:---------|:------------|
|Significantly reduce project risk|The prototype actually does nothing, just presentational|
|Has a short project timeline|Only for a limited purpose|

## 2. Evolutionary Prototype
- Most fundamental form of prototyping
- Build a robust prototype and constantly improve it
- Objective to deliver a working system to the end user
- Prototype eventually become the product

|Advantages|Disadvantages|
|:---------|:------------|
|Always looking for new ways to improve the system|Avoid documenting the requirements of the system|
|Increases the chance of **having the client satisfied** with the working system|Management is required|
|Model can be used even when requirements are not defined|Long term maintenance can be expensive|
|Quickly delivery of the system|Uncertain design idea's|
| |Information can be lost through so many improvement changes|

## 3. Low-Fidelity Prototyping
- **Limited function, limited interaction** prototyping effort
- Constructed to **depict concepts, design alternatives and screen layouts**. Intended to **demonstrate general look** and feel of the interface
- Created to educated, communicate and inform, but not to train, test or serve as a basis for which to code
- **Used early in the design cycle** to show general conceptual approaches

## 4. Medium fidelity prototype
- Limited functionality but clickable areas which presents the interactions and navigation possibilities of an application
- Usually built upon storyboards or user scenarios
- Correct content dscription is emphasized. a basic visual design is created for every actions tep
- Suited for the validation of the interaction concept
- Understandability of interaction elements can be validated

Advantages:
- The impression of an already functioning application makes it easy for all stakeholders to derive processes from the range of features
- This way the solution can be developed in the sense of the prototype.

## 5. High-Fidelity Prototyping
- The core functionality of the products user interface
- Fully interactive systems 
- Trade-off speed for accuracy
- Consume resources and have high cost

![comparison](./images/SE.3.png)

## 6. User Interface Prototyping
- Development of highly ineractive software system with gui
- Depnds highly on the quality of the GUI
- Generate ideas on how the GUI can be designed and helps to evaluate the quality of solution at an early stage

## Risks in Prototyping
1. Client may believe system is real. unrealistic expectations of the progess
2. Implementers make poor choice
3. Prototype is not identical to the real system
---
# Week 8 and 9
# Agile Software Developent

## Tips
- Details about waterfall and spiral model
- Advantages and disadvantages of traditional approach
- Why people moved from traditional to agile (7 reasons)
- Ignore scrum 

## Traditional Approach
- Requirements > Design > Implementation > Testing > Deployment and Maintenance
- In sequential order, no way back

## Advantages and Disadvantages
![Image](./images/SE.9.png)

## Waterfall Model
- Requirements are well known
- Product definition is stable
- Technology is understood
- New version of existing product
- Inflexible structure of product

### Problems:
- A lot of waiting time for developers
- Tons of documentaition
- Costly unnoticed mistakes and buggy code
- Hard to incorporate new or changing customer requirements
- Unclear requirements 
- Requirements change 
- Lack of involvement of the customers 
- Accuracy of estimation 
- Uneven loading of the resources 
- Last minute correction is very difficult
- Not much time for testing
- No time to fix test defects 
- Lot of documentation
- Schedule and cost overruns
- Customers not happy 

## 7 reasons to move to Agile
1. Ambiguous Requirements
2. Requirements Changes are Inevitable
3. Big, Upfront Planning is not Practical
4. Reviewing the working software is better than reviewing the documents.
5. Iterative and incremental development is better than sequential waterfall development
6. Delivery through small steps is better than a single huge delivery at the end of delivery life cycle. 
7. Frequent reflection by the project team is very important.

---
# Week 10 and 11
# Software testing and version Control 
## Tips
- Why testing is used
- What is unit testing, integration testing, and system testing
- Differences between black and white box

## Why testing is used
- Ensure quality of the product
- Saves money  (bugs in earlier stages)
- Customer satisfaction 

## Software Testing 
- Formal documentation
- Test cases: Pass/Fail
  - outputs are bug reports and validation
- Test Suite Document
  - specify a sequence of actions 
  - put test cases into an executable order
- Automated Testing

## Unit Test
- A piece of code which tests behaviour of a function or class

## Integration Testing
- The functional specification of the element being integrated
- Integration testing is done to test the modules/components when integrated to verify that they work as expected
- Integrate/combine the unit tested module one by one and test the behavior as a combined unit

## System testing
- A level of software testing where a complete and integrated software is tested. 
- The purpose of this test is to evaluate the system’s compliance with the specified requirements.
- The process of testing an integrated system to verify that it meets specified requirements

## Acceptance testing
- Formal testing with respect to user needs, requirements, and business processes conducted to determine whether or not a system satisfies the acceptance criteria and to enable the user, customers or other authorized entity to determine whether or not to accept the system

## White Box Testing
- Tests the design structure and interactions of functional code
- Require knowledge of the internals of the system

## Black Box Testing
- treats the product as a finished system, no knowledge of the internal workings
- users perspective

## Differences
![Image](./images/SE.1.png)
---
