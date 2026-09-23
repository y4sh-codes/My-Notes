
---

tags: [engineering, software-engineering, project-management, btech, cse, ai]

created: 2026-09-23

aliases: [SEPM, CS504 Notes]

---

  

## Table of Contents

- [[#Module 1: Introduction and Software Process Models]]

  - [[#1.1 Software and Software Engineering Foundations]]

  - [[#1.2 Software Process and Work Products]]

  - [[#1.3 Process Standards]]

  - [[#1.4 Prescriptive & Agile Process Models]]

  - [[#1.5 Financial and Economic Feasibility Analysis]]

  - [[#1.6 Technical Feasibility]]

- [[#Module 2: Requirement Engineering and Software Project Management Essentials]]

  - [[#2.1 Software Requirements Fundamentals]]

  - [[#2.2 Requirement Engineering Cycle]]

  - [[#2.3 Software Requirements Specification (SRS)]]

  - [[#2.4 Verification and Validation (V&V)]]

  - [[#2.5 Role of Management in Software Development]]

  - [[#2.6 Project Estimation Techniques]]

  - [[#2.7 Staffing and Resource Allocation]]

  - [[#2.8 Scheduling and Progress Tracking]]

  - [[#2.9 Earned Value Analysis (EVA)]]

  - [[#2.10 Risk Management]]

  - [[#2.11 Software Configuration Management (SCM)]]

  - [[#2.12 Software Process and Project Metrics]]

- [[#Module 3: Software Design and Coding]]

  - [[#3.1 Software Modeling]]

  - [[#3.2 Fundamental Design Concepts]]

  - [[#3.3 Modularity: Coupling and Cohesion]]

  - [[#3.4 Architectural Design]]

  - [[#3.5 Top-Down vs. Bottom-Up Design Approaches]]

  - [[#3.6 Object-Oriented Analysis and Design (OOAD)]]

  - [[#3.7 Function-Oriented Design vs. Object-Oriented Design]]

  - [[#3.8 Software Design Document (SDD)]]

  - [[#3.9 Coding Standards, Styles, and Documentation]]

- [[#Module 4: Software Project Management Planning & Execution]]

  - [[#4.1 Planning Process and WBS]]

  - [[#4.2 Advanced Estimation Techniques]]

  - [[#4.3 Project Scheduling Techniques]]

  - [[#4.4 Critical Path Method (CPM) and PERT]]

  - [[#4.5 Slack, Float, and Schedule Optimization]]

  - [[#4.6 Detailed Staffing and Team Structures]]

  - [[#4.7 Deep-Dive Software Configuration Management]]

- [[#Module 5: Testing and Software Quality]]

  - [[#5.1 Testing Principles and Strategies]]

  - [[#5.2 Black-Box Testing Techniques]]

  - [[#5.3 White-Box Testing Techniques]]

  - [[#5.4 Levels of Testing]]

  - [[#5.5 Test Planning and Test Case Specification]]

  - [[#5.6 Software Debugging]]

  - [[#5.7 Software Maintenance]]

  - [[#5.8 Software Quality Models & Standards]]

  - [[#5.9 Process Maturity Models: SEI CMM and CMMI]]

  - [[#5.10 Software Reliability and Availability]]

  

---

  

# Module 1: Introduction and Software Process Models

  

## 1.1 Software and Software Engineering Foundations

  

### What is Software?

Software is not merely executable program code. In software engineering, **Software** is formally defined as a collection of:

1. **Instructions / Code:** Computer programs that, when executed, provide desired features, function, and performance.

2. **Data Structures:** Information arrangements that enable the programs to adequately manipulate and process data.

3. **Documentation:** Descriptive documents (manuals, requirements, design models, comments) describing the operation, maintenance, and architecture of the programs.

  

$$\text{Software} = \text{Programs} + \text{Data Structures} + \text{Documentation}$$

  

#### Characteristics of Software vs. Hardware

| Parameter           | Software                                                                                     | Hardware                                                                              |
| ------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **Manufacturing**   | Engineered or developed; not manufactured in classical sense.                                | Manufactured via physical industrial processes.                                       |
| **Wear & Tear**     | Does not wear out. Degrades due to environment changes and patches ("software rot").         | Wears out due to physical friction, heat, and environmental stresses (Bathtub curve). |
| **Failure Curve**   | Curve shows initial high failure rate, stabilizes, then rises due to maintenance intrusions. | Follows standard bathtub curve with physical wear-out phase.                          |
| **Component Reuse** | Custom-built components remain common, though component-based engineering is growing.        | Built predominantly from standardized off-the-shelf components.                       |
  

### Definition of Software Engineering

> **IEEE Definition (IEEE 610.12):** Software Engineering is the application of a systematic, disciplined, quantifiable approach to the development, operation, and maintenance of software; that is, the application of engineering to software.

  

Fritz Bauer defined it as: *"The establishment and use of sound engineering principles in order to obtain economically software that is reliable and works efficiently on real machines."*

  

### Common Software Myths

- **Management Myths:**

  - *Myth:* "We have standards books full of procedures, so our people know everything needed." *Reality:* Books are often outdated, unread, or inadequate for modern agile workflows.

  - *Myth:* "If we fall behind schedule, we can simply add more programmers (Brooks' Law)." *Reality:* "Adding human resources to a late software project makes it later" due to communication overhead and onboarding time.

- **Customer Myths:**

  - *Myth:* "A general statement of objectives is enough to begin writing programs." *Reality:* Ambiguous requirements lead directly to project rework and cost explosions.

  - *Myth:* "Software is flexible; requirements can easily change at any stage without high impact." *Reality:* The cost of change grows exponentially throughout the lifecycle.

- **Practitioner Myths:**

  - *Myth:* "Once the program runs and is delivered, our job is done." *Reality:* 60% to 80% of all software effort occurs *after* initial release during operations and maintenance.

  - *Myth:* "Until the code is running, there is no way of assessing its quality." *Reality:* Formal technical reviews, inspections, and static analysis assess quality earlier.

  

---

  

## 1.2 Software Process and Work Products

  

- **Software Process:** A structured set of activities, actions, tasks, milestones, and work products required to engineer high-quality software.

- **Generic Process Framework Activities:**

  1. **Communication:** Collaboration between stakeholders to gather requirements.

  2. **Planning:** Defining the technical path, risks, resources, work schedule.

  3. **Modeling:** Creating representations (analysis models and architecture/design models).

  4. **Construction:** Code generation and testing (unit, integration).

  5. **Deployment:** Delivery of product for evaluation and feedback.

- **Umbrella Activities:** Persist across the entire framework:

  - Software project tracking and control

  - Risk management

  - Software quality assurance (SQA)

  - Formal technical reviews (FTR)

  - Software configuration management (SCM)

  - Measurement and metrics collection

  - Reusability management

- **Work Products:** Any tangible output produced by a process task (e.g., SRS document, Architectural design diagram, source code files, test suites, user manuals).

  

---

  

## 1.3 Process Standards

  

- **ISO/IEC 12207:** Systems and software engineering – Software life cycle processes. Defines primary processes (acquisition, supply, development, operation, maintenance), supporting processes (documentation, SCM, QA, verification, validation, review, audit), and organizational processes (management, infrastructure, improvement, training).

- **IEEE Standards:** Provide standardized guidelines for software requirements specifications (IEEE 830 / ISO/IEC/IEEE 29148), software design descriptions (IEEE 1016), and test documentation (IEEE 829).

  

---

  

## 1.4 Prescriptive & Agile Process Models

  

### 1. Waterfall Model (Classical & Iterative)

- **Concept:** Linear-sequential life cycle model. Each phase must be completed before the next begins.

- **Phases:** Feasibility Study $\rightarrow$ Requirements Analysis & Specification $\rightarrow$ Design $\rightarrow$ Coding & Unit Testing $\rightarrow$ Integration & System Testing $\rightarrow$ Maintenance.

- **Advantages:** Simple and easy to understand; rigid discipline with well-defined deliverables at each phase.

- **Disadvantages:** Inflexible to change; working software appears late in the lifecycle; high risk for complex, uncertain projects.

- **Iterative Waterfall:** Incorporates feedback paths between adjacent phases to fix defects discovered later.

  

### 2. Prototyping Model

- **Concept:** Developer builds a quick "mock-up" (throwaway or evolutionary) focusing on user interfaces and broad capabilities to clarify ambiguous requirements.

- **Phases:** Quick Plan $\rightarrow$ Modeling (Quick Design) $\rightarrow$ Construction of Prototype $\rightarrow$ Deployment & Customer Evaluation $\rightarrow$ Prototype Refinement.

- **Best Use:** Human-Computer Interface (HCI) intensive systems where end-user requirements are unstable or poorly understood.

  

### 3. Iterative Enhancement Model

- **Concept:** The software is developed in small, manageable increments. In each iteration, a subset of requirements is designed, implemented, tested, and incrementally added to the core framework.

- **Advantage:** Delivers an operational product core early; feedback shapes subsequent increments.

  

### 4. Spiral Model (Boehm)

- **Concept:** Evolutionary model coupling the iterative nature of prototyping with the controlled aspects of the waterfall model. Its defining characteristic is **explicit risk analysis** at every iteration.

- **Four Quadrants:**

  1. **Objective Setting:** Identify objectives, alternatives, and operational constraints.

  2. **Risk Assessment and Reduction:** Evaluate alternatives, identify risks, and mitigate them (often using prototypes or simulations).

  3. **Development and Validation:** Develop next-level product using traditional engineering approaches.

  4. **Review and Planning:** Review results with customer and plan the next cycle/spiral.

- **Best Use:** Large-scale, mission-critical systems where financial or operational risk is substantial.

  

### 5. RAD (Rapid Application Development) Model

- **Concept:** An incremental process model emphasizing an extremely short development cycle (typically 60–90 days) using component-based construction and high-level 4GL tools.

- **Phases:** Business Modeling $\rightarrow$ Data Modeling $\rightarrow$ Process Modeling $\rightarrow$ Application Generation $\rightarrow$ Testing and Turnover.

- **Drawbacks:** Requires heavily committed, high-performance teams; modularizable system architecture required.

  

### 6. Agile Model

- **Philosophy:** Emphasizes individuals and interactions over processes and tools, working software over comprehensive documentation, customer collaboration over contract negotiation, and responding to change over following a plan (*Agile Manifesto*).

- **Core Frameworks:**

  - **Scrum:** Iterative framework characterized by Sprints (2–4 weeks), daily standup meetings, Product Backlog, Sprint Backlog, and roles (Product Owner, Scrum Master, Cross-functional Team).

  - **Extreme Programming (XP):** Focuses on engineering excellence with practices like Pair Programming, Test-Driven Development (TDD), Continuous Integration, refactoring, and small releases.

  

### 7. V-Model (Verification and Validation Model)

- **Concept:** A sequential model showing the direct relationship between each development phase and its corresponding testing phase.

- **Mapping:**

  - Requirements Analysis $\longleftrightarrow$ Acceptance Testing

  - System Design $\longleftrightarrow$ System Testing

  - Architecture/High-Level Design $\longleftrightarrow$ Integration Testing

  - Detailed/Low-Level Design $\longleftrightarrow$ Unit Testing

  - Coding sits at the bottom vertex of the "V".

  

---

  

## 1.5 Financial and Economic Feasibility Analysis

  

Financial feasibility determines whether the development organization can afford the investment and whether the returns justify the project expenditures.

  

### 1. Time Value of Money (TVM)

Money available at the present time is worth more than the identical sum in the future due to its potential earning capacity.

$$FV = PV \times (1 + r)^n$$

Where:

- $FV$ = Future Value

- $PV$ = Present Value

- $r$ = Interest / Discount rate per period

- $n$ = Number of compounding periods

  

### 2. Discounting Formula

To calculate the Present Value ($PV$) of an expected future cash flow ($C_t$):

$$PV = \frac{C_t}{(1 + r)^t}$$

  

### 3. Payback Period

The time required to recoup the funds expended in an investment.

$$\text{Payback Period} = \frac{\text{Initial Capital Outlay}}{\text{Annual Net Cash Inflow}} \quad \text{(for uniform cash flows)}$$

For non-uniform cash flows, cumulative cash flows are tracked until they equal initial capital investment.

  

### 4. Net Present Value (NPV)

The sum of the present values of incoming cash flows minus initial investment outlay ($C_0$).

$$NPV = \sum_{t=1}^{n} \frac{C_t}{(1 + r)^t} - C_0$$

- **Decision Rule:** If $NPV > 0$, the project is economically viable. If comparing mutually exclusive projects, select the one with the higher positive $NPV$.

  

### 5. Return on Investment (ROI)

A percentage measuring the efficiency of an investment:

$$ROI = \left( \frac{\text{Total Net Benefits} - \text{Total Costs}}{\text{Total Costs}} \right) \times 100\%$$

  

### 6. Internal Rate of Return (IRR)

The discount rate $r^*$ at which the Net Present Value ($NPV$) of all cash flows from a project equals zero:

$$\sum_{t=1}^{n} \frac{C_t}{(1 + IRR)^t} - C_0 = 0$$

- **Decision Rule:** Accept project if $IRR > \text{Cost of Capital (Hurdle Rate)}$.

  

---

  

## 1.6 Technical Feasibility

Evaluates whether the technical resources, tools, competencies, and system constraints permit development within the specified environment:

- **Technological Availability:** Is the necessary hardware, networking, and platform architecture commercially viable and accessible?

- **Team Competency:** Does the engineering team possess the skills, algorithmic background, and language proficiency required?

- **Resource Constraints:** Are memory limits, network bandwidth, response time targets, and scalability parameters achievable?

  

---

  

# Module 2: Requirement Engineering and Software Project Management Essentials

  

## 2.1 Software Requirements Fundamentals

A requirement is a capability or condition to which a system must conform, either derived directly from user needs or imposed by contract, standards, or specifications.

  

### Types of Requirements

- **Functional Requirements (FRs):** Statements of services the system should provide, how the system must react to particular inputs, and how the system behaves in specific situations (e.g., "The system shall calculate the tax rate based on the billing zip code").

- **Non-Functional Requirements (NFRs):** Constraints on the functions or services offered by the system.

  - *Performance Constraints:* Response time, throughput, memory footprints.

  - *Reliability & Availability:* Mean Time Between Failures (MTBF), 99.999% uptime.

  - *Security:* Encryption standards (AES-256), authentication (OAuth2).

  - *Usability:* Adherence to WCAG accessibility guidelines.

- **Domain Requirements:** Requirements derived from the application domain that reflect domain characteristics (e.g., banking regulations, medical FDA compliance).

  

---

  

## 2.2 Requirement Engineering Cycle

The systematic process of establishing services required and system constraints.

  

1. **Inception:** Establish basic business understanding, define project scope, identify initial stakeholders.

2. **Elicitation:** Gathering requirements from stakeholders via:

   - Interviews (structured/unstructured)

   - Questionnaires / Surveys

   - Workshops & Brainstorming sessions

   - Observation / Job shadowing

   - Fast Prototyping

3. **Elaboration:** Developing technical models (use cases, activity diagrams, domain classes) to refine requirements.

4. **Negotiation:** Resolving conflicting requirements among stakeholders; prioritizing based on risk and cost.

5. **Specification:** Documenting the final requirements into a formal, binding document (SRS).

6. **Validation:** Reviewing the document for correctness, completeness, consistency, and feasibility.

7. **Requirement Management:** Tracking changes, traceability, and version dependencies across the product lifecycle.

  

---

  

## 2.3 Software Requirements Specification (SRS)

The official statement of what system developers must implement.

  

### Characteristics of an Excellent SRS (IEEE 830 / ISO/IEC/IEEE 29148)

- **Correct:** Reflects actual system requirements.

- **Unambiguous:** Every requirement has exactly one interpretation.

- **Complete:** Covers all significant operational scenarios, error states, and inputs.

- **Consistent:** No internal contradictions between requirements.

- **Ranked for Importance/Stability:** Categorized by priority (e.g., MoSCoW: Must, Should, Could, Won't).

- **Verifiable (Testable):** Quantifiable metrics; capable of being tested by a machine or human.

- **Modifiable:** Structure allows modifications without loss of integrity.

- **Traceable:** Traceable backward to business goals and forward to design elements and test cases.

  

---

  

## 2.4 Verification and Validation (V&V)

- **Verification ("Are we building the product right?"):**

  - Confirms software correctly implements specific functions.

  - *Methods:* Code reviews, static code analysis, inspections, walkthroughs.

- **Validation ("Are we building the right product?"):**

  - Confirms system meets intended customer use and requirements.

  - *Methods:* Acceptance testing, user testing, alpha/beta execution.

  

---

  

## 2.5 Role of Management in Software Development

The software project manager provides oversight to ensure deliverables arrive within budget, on schedule, and meeting specified quality constraints. The 4 P's of management:

1. **People:** Staffing, organizing, managing organizational dynamics.

2. **Product:** Defining scope, business objectives, and technical constraints.

3. **Process:** Selecting appropriate lifecycle model, work breakdown.

4. **Project:** Planning, tracking, controlling deviations, managing risks.

  

---

  

## 2.6 Project Estimation Techniques

Estimation provides approximate values for effort (person-months), project duration (calendar months), and total cost.

  

### 1. Empirical Estimation Models

- **COCOMO (Constructive Cost Model - Barry Boehm):**

  - **Basic COCOMO:**

    $$\text{Effort} = a \times (\text{KLOC})^b \quad \text{[Person-Months]}$$

    $$\text{Development Time} = c \times (\text{Effort})^d \quad \text{[Months]}$$

  - *Modes of Development:*

    - **Organic:** Small teams, well-understood environments: $a = 2.4, b = 1.05, c = 2.5, d = 0.38$.

    - **Semidetached:** Intermediate team size and complexity: $a = 3.0, b = 1.12, c = 2.5, d = 0.35$.

    - **Embedded:** Severe operational constraints, complex interactions: $a = 3.6, b = 1.20, c = 2.5, d = 0.32$.

  - **Intermediate COCOMO:** Adjusts baseline effort with 15 Cost Drivers (Effort Multipliers, $EAF$).

    $$\text{Effort} = a \times (\text{KLOC})^b \times \prod_{i=1}^{15} EM_i$$

  - **COCOMO II:** Incorporates modern software techniques: Application Composition, Early Design, and Post-Architecture models.

  

### 2. Analytical & Heuristic Techniques

- **Expert Judgment (Delphi Method):** Structural consensus-building process among independent estimators.

- **Heuristic Sizing:** Analogous estimation based on completed historical projects.

  

---

  

## 2.7 Staffing and Resource Allocation

- **Staffing Estimation:** Calculated by total Effort divided by Schedule Duration:

  $$\text{Average Staffing} = \frac{\text{Effort (Person-Months)}}{\text{Duration (Months)}}$$

- **Brooks' Law:** Assigning more developers to an already delayed software project increases delivery delay due to $N(N - 1) / 2$ communication paths.

  

---

  

## 2.8 Scheduling and Progress Tracking

Software scheduling divides total estimated project effort across planned phases by allocating tasks to designated individuals over specific intervals.

- **Milestones:** Discrete progress checkpoints denoting completion of critical work products (e.g., SRS Approved).

- **Deliverables:** Tangible assets submitted directly to clients/stakeholders.

- **Gantt Charts:** Horizontal bar graph mapping out project tasks, chronological dependencies, and schedules.

  

---

  

## 2.9 Earned Value Analysis (EVA)

EVA is an industry-standard quantitative project tracking technique measuring real-time performance against baseline plans.

  

### Core Metrics

- **Planned Value ($PV$):** Budgeted Cost of Work Scheduled ($BCWS$) up to a given time $t$.

- **Earned Value ($EV$):** Budgeted Cost of Work Performed ($BCWP$) up to time $t$.

- **Actual Cost ($AC$):** Actual Cost of Work Performed ($ACWP$) incurred up to time $t$.

  

### Variance Indicators

$$\text{Cost Variance (CV)} = EV - AC$$

$$\text{Schedule Variance (SV)} = EV - PV$$

- $\text{CV} < 0 \implies \text{Over Budget}$

- $\text{SV} < 0 \implies \text{Behind Schedule}$

  

### Performance Indexes

$$\text{Cost Performance Index (CPI)} = \frac{EV}{AC}$$

$$\text{Schedule Performance Index (SPI)} = \frac{EV}{PV}$$

- $\text{CPI}, \text{SPI} > 1 \implies \text{Favorable Performance}$

- $\text{CPI}, \text{SPI} < 1 \implies \text{Unfavorable Performance}$

  

---

  

## 2.10 Risk Management

A proactive strategy to minimize vulnerabilities, hazards, and unexpected events.

  

### Steps in Risk Management

1. **Risk Identification:** Uncovering potential risks (Project, Technical, Business, Known, Predictable, Unpredictable).

2. **Risk Projection (Estimation):** Establishing the probability of occurrence ($P$) and impact/severity ($I$).

   $$\text{Risk Exposure (RE)} = P \times I$$

3. **Risk Mitigation, Monitoring, and Management (RMMM Plan):**

   - *Mitigation:* Proactive steps to prevent risk occurrence.

   - *Monitoring:* Tracking risk metrics across the project.

   - *Management:* Contingency plans if risks materialize.

  

---

  

## 2.11 Software Configuration Management (SCM)

SCM tracks, controls, and audits modifications made to software artifacts throughout the product lifecycle.

  

### Core Components

- **Configuration Items (SCIs):** Atomic assets placed under configuration control (code files, models, documents).

- **Baselines:** Formally reviewed and agreed-upon specifications or products that serve as the basis for further development.

- **Change Control Board (CCB):** Authority reviewing, approving, or rejecting proposed Engineering Change Orders (ECO).

- **Version Control:** Branching, merging, and tracking revision histories (e.g., Git).

- **Configuration Auditing:**

  - *Functional Configuration Audit (FCA):* Validates item achieves functional requirements.

  - *Physical Configuration Audit (PCA):* Confirms documentation aligns with code.

  

---

  

## 2.12 Software Process and Project Metrics

  

```

                    ┌─────────────────────────┐

                    │ Software Metrics        │

                    └───────────┬─────────────┘

          ┌─────────────────────┴─────────────────────┐

          ▼                                           ▼

┌─────────────────────────┐                 ┌─────────────────────────┐

│ Process Metrics         │                 │ Project Metrics         │

│ (Defect removal         │                 │ (Effort variance,       │

│  efficiency, cycle time)│                 │  milestone slip, costs) │

└─────────────────────────┘                 └─────────────────────────┘

```

  

- **Process Metrics:** Long-term organizational indicators used to improve institutional capability (Defect Removal Efficiency: $DRE = \frac{E}{E + D}$, cycle times).

- **Project Metrics:** Short-term operational indicators used by managers to monitor current project trajectory (cost, effort, bug velocity).

- **Product Metrics:** Quality indicators evaluating software artifacts directly (Cyclomatic complexity, coupling, size in KLOC/FP).

  

---

  

# Module 3: Software Design and Coding

  

## 3.1 Software Modeling

Software design models transform requirements specifications into blueprints for implementation.

  

### 1. Process Modeling

Focuses on the flow of data through functions and operational transformations.

- **Data Flow Diagram (DFD):** Graphical depiction of data flow through a system.

  - *Elements:* External Entities (Rectangles), Processes (Circles/Bubbles), Data Stores (Parallel lines), Data Flows (Directed arrows).

  - *Hierarchy:* Level 0 (Context Diagram, system as a single process bubble) $\rightarrow$ Level 1 (Expansion of major subsystems) $\rightarrow$ Level 2 (Detailed process breakdowns).

- **Decision Tables & Decision Trees:** Model complex logical conditions and actions.

  - *Decision Table:* Matrix mapping input condition combinations to corresponding system actions.

  - *Decision Tree:* Branching graph displaying conditions as nodes and actions as leaves.

  

### 2. Data Modeling

- **Entity-Relationship (E-R) Diagram:** Models relational structure of data.

  - *Entities:* Objects of interest.

  - *Attributes:* Properties of entities.

  - *Relationships:* Associations between entities ($1:1$, $1:N$, $M:N$).

  

### 3. Behavioral Modeling

- **State Transition Diagrams (STD) / UML Statecharts:** Model dynamic, reactive systems by detailing explicit states, input events, guard conditions, and resulting state transitions.

  

---

  

## 3.2 Fundamental Design Concepts

- **Abstraction:** Hiding low-level implementation details and exposing only necessary interfaces (Procedural and Data abstraction).

- **Architecture:** The structural framework of the software system, showing components, properties, and relationships.

- **Patterns:** Reusable solutions to commonly occurring design problems (e.g., Gang of Four patterns: Creational, Structural, Behavioral).

- **Information Hiding (Parnas):** Modules should encapsulate internal implementations so they are inaccessible to external modules, interacting only through stable interfaces.

- **Refactoring:** Reorganizing internal code structure without altering its external behavior to improve maintainability and lower complexity.

  

---

  

## 3.3 Modularity: Coupling and Cohesion

  

Modularity divides software into named, addressable components. The core design principle is **High Cohesion and Low Coupling**.

  

### Cohesion (Intra-module Strength)

Measures how strongly related the internal elements of a single module are.

*(Ranked from Worst to Best)*

1. **Coincidental Cohesion (Worst):** Elements grouped together arbitrarily with no meaningful relationship.

2. **Logical Cohesion:** Elements perform logically similar functions (e.g., a single module handling all system input), chosen via external parameter.

3. **Temporal Cohesion:** Elements are executed within the same timeframe (e.g., startup/initialization routines).

4. **Procedural Cohesion:** Elements execute in a specific sequential order to accomplish a broader task.

5. **Communicational Cohesion:** Elements operate on the same input data or produce the same output data.

6. **Sequential Cohesion:** The output of one step serves directly as input to the next step.

7. **Functional Cohesion (Best):** Every element contributes directly to executing a single, well-defined task (e.g., `computeSquareRoot()`).

  

### Coupling (Inter-module Interdependence)

Measures the degree of dependence between distinct software modules.

*(Ranked from Worst to Best)*

1. **Content Coupling (Worst):** One module accesses or modifies the internal code, data, or memory space of another.

2. **Common Coupling:** Multiple modules share read/write access to global data variables.

3. **Control Coupling:** One module explicitly directs the execution flow of another by passing control flags/switches.

4. **Stamp Coupling:** Modules share composite data structures (e.g., passing an entire `Employee` record when only `employeeId` is needed).

5. **Data Coupling (Best):** Modules communicate strictly by passing discrete, primitive data values as parameters (e.g., passing a single integer).

  

---

  

## 3.4 Architectural Design

Structural decomposition of system components.

  

### Common Architectural Styles

- **Layered Architecture:** Organizes components into hierarchical tiers (Presentation, Business Logic, Data Access, Database). Components only communicate with adjacent layers.

- **Client-Server Architecture:** Decouples clients (requesting entities) from centralized servers (service and resource providers).

- **Model-View-Controller (MVC):** Decouples internal data representation (Model), user display rendering (View), and input/event coordination (Controller).

- **Pipe-and-Filter:** Data stream flows sequentially through intermediate processing elements (Filters) connected via intermediate streams (Pipes), common in compilers and Unix shells.

- **Event-Driven Architecture:** Asynchronous components produce and consume events via message queues or event brokers.

  

---

  

## 3.5 Top-Down vs. Bottom-Up Design Approaches

- **Top-Down Design:** Decomposes the high-level system concept into subsystems, modules, and routines. Focuses on overall architecture first, but delays detailed validation until later.

- **Bottom-Up Design:** Constructs basic, reusable low-level modules and utilities first, combining them to build higher-level subsystems. Effective for component-based engineering, but risks architecture misalignment if global goals are overlooked.

  

---

  

## 3.6 Object-Oriented Analysis and Design (OOAD)

OOAD structures a system as a collaborative collection of autonomous objects encapsulating state and behavior.

  

### Unified Modeling Language (UML) Diagrams

- **Structural Diagrams:**

  - *Class Diagrams:* Classes, attributes, methods, and relationships (Inheritance, Association, Aggregation, Composition, Dependency).

  - *Component & Deployment Diagrams:* Physical components, hardware nodes, runtime execution topologies.

- **Behavioral Diagrams:**

  - *Use Case Diagrams:* Functional interactions between external Actors and system Use Cases.

  - *Sequence Diagrams:* Time-ordered message exchanges between objects.

  - *Activity Diagrams:* Workflow and operational steps (similar to flowcharts with parallel forks/joins).

  - *State Machine Diagrams:* Reactive state lifecycles and trigger events.

  

---

  

## 3.7 Function-Oriented Design vs. Object-Oriented Design

  

| Feature              | Function-Oriented Design (SA/SD)                                  | Object-Oriented Design (OOD)                              |
| -------------------- | ----------------------------------------------------------------- | --------------------------------------------------------- |
| **Primary Focus**    | Functions and operational workflows.                              | Real-world objects and entities.                          |
| **Data & Function**  | Data and functions are decoupled.                                 | Data and operations are encapsulated together.            |
| **Core Abstraction** | Functional Decomposition, DFDs, Structure Charts.                 | Classes, Objects, Inheritance, Polymorphism.              |
| **Maintainability**  | Lower; changes in data format often ripple across many functions. | Higher; changes are encapsulated within class boundaries. |
| **Dominant Era**     | 1970s–1980s (Structured programming).                             | Modern industry standard.                                 |

  

---

  

## 3.8 Software Design Document (SDD)

The SDD translates requirements into an architectural and algorithmic blueprint for developers.

- **Standard (IEEE 1016):**

  - Section 1: Introduction, Scope, Purpose.

  - Section 2: Architectural Overview & System Decomposition.

  - Section 3: Data Design (Database schemas, file formats, data structures).

  - Section 4: Interface Design (Internal APIs, external services, GUI layouts).

  - Section 5: Detailed Component Design (Algorithms, pseudo-code, class definitions).

  

---

  

## 3.9 Coding Standards, Styles, and Documentation

- **Coding Standards:** Uniform conventions across a team (e.g., variable naming, CamelCase, indentation rules, error handling conventions).

- **Code Refactoring:** Improving internal code structure without changing external behavior.

- **Self-Documenting Code:** Writing expressive identifiers and clear module structures to reduce excessive commenting.

- **Formal Documentation:** Clean inline documentation using tools like Javadoc, Doxygen, or Sphinx for automated API documentation.

  

---

  

# Module 4: Software Project Management Planning & Execution

  

## 4.1 Planning Process and WBS

Project planning provides a roadmap for resource allocation, scheduling, and risk mitigation.

  

### Work Breakdown Structure (WBS)

A hierarchical decomposition of total project scope into distinct, manageable deliverables and work packages.

```

                      Level 1: Software System

                                  │

         ┌────────────────────────┴────────────────────────┐

Level 2: Frontend                                  Backend Engine

         │                                                 │

Level 3: ├── Authentication UI                    ├── Database ORM

         └── Dashboard Views                      └── API Endpoints

```

- **Work Package:** The lowest level deliverable unit in a WBS, small enough to be independently assigned, tracked, and estimated.

  

---

  

## 4.2 Advanced Estimation Techniques

  

### 1. Function Point (FP) Analysis (Albrecht)

Measures software size based on functional complexity delivered to the user, independent of programming language.

1. Compute **Unadjusted Function Points (UFP)** by classifying and weighting 5 components:

   - External Inputs ($EI$)

   - External Outputs ($EO$)

   - External Inquiries ($EQ$)

   - Internal Logical Files ($ILF$)

   - External Interface Files ($EIF$)

  

| Component Type                     | Low Complexity | Average Complexity | High Complexity |
| ---------------------------------- | :------------: | :----------------: | :-------------: |
| **External Inputs (EI)**           |       3        |         4          |        6        |
| **External Outputs (EO)**          |       4        |         5          |        7        |
| **External Inquiries (EQ)**        |       3        |         3          |        6        |
| **Internal Logical Files (ILF)**   |       7        |         10         |       15        |
| **External Interface Files (EIF)** |       5        |         7          |       10        |

  

$$UFP = \sum (\text{Count} \times \text{Weight})$$

  

2. Calculate Value Adjustment Factor ($VAF$) based on 14 General System Characteristics ($GSC$):

   $$VAF = 0.65 + 0.01 \times \sum_{i=1}^{14} F_i$$

   *(Where each $F_i$ ranges from 0 [no influence] to 5 [essential]).*

3. Compute Final **Function Points**:

   $$FP = UFP \times VAF$$

  

### 2. Use Case Point (UCP) Estimation (Karner)

Estimates object-oriented projects from Use Case models:

- **Unadjusted Actor Weight (UAW):** Classified as Simple (API), Average (Protocol), or Complex (GUI user).

- **Unadjusted Use Case Weight (UUCW):** Calculated from number of transactions per use case.

- **Unadjusted Use Case Points (UUCP):**

  $$UUCP = UAW + UUCW$$

- Adjusted by Technical Complexity Factors ($TCF$) and Environmental Complexity Factors ($ECF$):

  $$UCP = UUCP \times TCF \times ECF$$

  

---

  

## 4.3 Project Scheduling Techniques

- **Line of Balance (LOB):** Visual management technique used for repetitive work cycles across software production pipelines.

- **Gantt Charts:** Maps chronological schedules, dependencies, and actual vs. expected task completions.

  

---

  

## 4.4 Critical Path Method (CPM) and PERT

  

### Critical Path Method (CPM)

CPM uses deterministic (fixed) task durations to find the longest sequence of dependent tasks, which dictates the total project duration.

- Any delay along the **Critical Path** delays the entire project.

  

### Program Evaluation and Review Technique (PERT)

Uses probabilistic time estimates based on three durations per activity:

- Optimistic time ($a$ or $t_o$)

- Most likely time ($m$ or $t_m$)

- Pessimistic time ($b$ or $t_p$)

  

$$\text{Expected Duration } (t_e) = \frac{a + 4m + b}{6}$$

$$\text{Variance } (\sigma^2) = \left( \frac{b - a}{6} \right)^2$$

$$\text{Standard Deviation } (\sigma) = \frac{b - a}{6}$$

  

---

  

## 4.5 Slack, Float, and Schedule Optimization

  

### Calculating Network Parameters

For each activity:

- **Earliest Start ($ES$):** $\max(\text{Earliest Finish of predecessors})$

- **Earliest Finish ($EF$):** $ES + \text{Duration}$

- **Latest Finish ($LF$):** $\min(\text{Latest Start of successors})$

- **Latest Start ($LS$):** $LF - \text{Duration}$

  

### Floats and Slack

- **Total Float:** Time an activity can be delayed without delaying the project completion date:

  $$\text{Total Float} = LS - ES = LF - EF$$

- **Free Float:** Time an activity can be delayed without delaying the Early Start of any successor:

  $$\text{Free Float} = \min(ES_{\text{successors}}) - EF$$

- **Critical Path Condition:** An activity is on the critical path if and only if:

  $$\text{Total Float} = 0$$

  

---

  

## 4.6 Detailed Staffing and Team Structures

- **Chief Programmer Team (Democratic Centralized):** Structured around a lead architect who writes core components and delegates tasks to specialists (backup programmers, librarians, testers). High communication efficiency; high single-point-of-failure risk.

- **Democratic Decentralized Team (Egoless):** Decisions made by group consensus without rigid hierarchy. High innovation and cohesion, but slower decision-making on large teams.

- **Controlled Decentralized Team:** Hierarchical structure with a project manager coordinating sub-team leaders. Common in large enterprise systems.

  

---

  

## 4.7 Deep-Dive Software Configuration Management

- **Audit Trails:** Complete, non-repudiable logs of all codebase and artifact modifications.

- **Change Control Workflow:**

  $$\text{Change Request} \rightarrow \text{Impact Analysis} \rightarrow \text{CCB Review} \rightarrow \text{Approved/Rejected} \rightarrow \text{Checked Out} \rightarrow \text{Verified} \rightarrow \text{Merged}$$

  

---

  

# Module 5: Testing and Software Quality

  

## 5.1 Testing Principles and Strategies

  

### Fundamental Testing Principles

1. **Testing shows the presence of defects, not their absence (Dijkstra):** Testing can prove software contains bugs, but cannot prove it is completely error-free.

2. **Exhaustive testing is impossible:** Complete permutation testing of all paths and inputs is computationally infeasible; risk-based testing is used instead.

3. **Early Testing:** Testing activities must begin as early as possible in the software lifecycle to reduce defect remediation costs.

4. **Defect Clustering:** A small number of modules typically contain the majority of defects (Pareto Principle: 80/20 rule).

5. **Pesticide Paradox:** Running the same tests repeatedly reduces their ability to find new bugs; test suites must be continuously updated.

6. **Testing is context-dependent:** Safety-critical medical software is tested differently from a mobile game.

7. **Absence-of-errors fallacy:** Fixing defects does not guarantee business success if the system is unusable or does not meet customer needs.

  

---

  

## 5.2 Black-Box Testing Techniques

Tests functionality without internal knowledge of code, algorithms, or data structures.

  

### 1. Equivalence Partitioning (EP)

Divides the input domain into valid and invalid equivalence classes such that test data from any single class is representative of all data in that class.

- *Example:* If an input accepts values $10 \le X \le 50$:

  - Class 1 (Invalid): $X < 10$ (Test value: $5$)

  - Class 2 (Valid): $10 \le X \le 50$ (Test value: $25$)

  - Class 3 (Invalid): $X > 50$ (Test value: $65$)

  

### 2. Boundary Value Analysis (BVA)

Extends Equivalence Partitioning by testing values at the boundaries of equivalence classes, where defects cluster most frequently.

- For an interval $[A, B]$, test points typically include:

  $$A - 1, \quad A, \quad A + 1, \quad \text{Nominal}, \quad B - 1, \quad B, \quad B + 1$$

  

### 3. Cause-Effect Graphing

A formal technique translating complex requirement logic into boolean graphs, which are then used to derive decision tables and test cases.

  

---

  

## 5.3 White-Box Testing Techniques

Tests internal code structure, execution paths, and logic conditions.

  

### 1. Basis Path Testing & Control Flow Graphs (CFG)

Models code execution flow as a directed graph $G = (V, E)$, where $V$ is the set of nodes (statements/blocks) and $E$ is the set of edges (control transfers).

  

#### Cyclomatic Complexity ($V(G)$)

A metric quantifying the logical complexity of code and defining the number of independent execution paths required for thorough testing:

1. **Formula 1 (Edges & Nodes):**

   $$V(G) = E - N + 2P$$

   *(Where $E = \text{number of edges}$, $N = \text{number of nodes}$, $P = \text{number of connected components}$, typically $1$).*

2. **Formula 2 (Predicate Nodes):**

   $$V(G) = P + 1$$

   *(Where $P = \text{number of predicate/decision nodes with outgoing conditional branches}$).*

3. **Formula 3 (Enclosed Regions):**

   $$V(G) = R$$

   *(Where $R = \text{number of bounded planar regions} + 1 \text{ unbounded outer region}$).*

  

### 2. Structural Coverage Metrics

- **Statement Coverage:** Percentage of executable statements executed by the test suite.

  $$\text{Statement Coverage} = \left( \frac{\text{Executed Statements}}{\text{Total Statements}} \right) \times 100\%$$

- **Branch/Decision Coverage:** Validates that every boolean branch (true/false) in decision points has been evaluated.

- **Condition Coverage:** Validates that each individual boolean variable within compound predicates has evaluated to both true and false.

- **Multiple Condition / MC/DC Coverage:** Modified Condition/Decision Coverage requires demonstrating that each condition can independently affect the decision outcome.

  

---

  

## 5.4 Levels of Testing

  

```

      [Acceptance Testing]  <--- Validates Business Needs

             │

      [System Testing]      <--- Validates Integrated End-to-End System

             │

   [Integration Testing]    <--- Validates Module Interfaces

             │

       [Unit Testing]       <--- Validates Individual Functions/Classes

```

  

1. **Unit Testing:** Tests individual functions, procedures, or classes in isolation. Uses test drivers (caller simulators) and stubs (called routine simulators).

2. **Integration Testing:** Identifies interface and communication faults between integrated modules.

   - *Big-Bang Integration:* Combines all components at once and tests the whole. High risk, difficult to isolate bugs.

   - *Top-Down Integration:* Begins with top-level control modules using stubs for low-level components.

   - *Bottom-Up Integration:* Begins with lowest-level modules using drivers, moving upward.

   - *Sandwich/Hybrid:* Combines top-down and bottom-up approaches.

3. **System Testing:** Evaluates the integrated system against global requirements.

   - *Security Testing:* Validates authorization, vulnerability safeguards, and encryption.

   - *Stress Testing:* Tests system behavior under extreme loads exceeding capacity.

   - *Performance Testing:* Validates response times, throughput, and resource limits.

4. **Regression Testing:** Re-executing existing test suites after code changes to ensure modifications have not broken working functionality.

5. **Acceptance Testing:** Validates that the system meets user operational needs:

   - *Alpha Testing:* Conducted at the developer's site by representative end-users in a controlled environment.

   - *Beta Testing:* Conducted at end-user sites in real-world environments without developer oversight.

  

---

  

## 5.5 Test Planning and Test Case Specification

- **Test Plan (IEEE 829):** Defines test scope, approach, resources, schedule, pass/fail criteria, and risks.

- **Test Case Structure:**

  $$\text{Test Case ID} \mid \text{Description} \mid \text{Pre-conditions} \mid \text{Inputs} \mid \text{Expected Output} \mid \text{Actual Output} \mid \text{Pass/Fail Status}$$

  

---

  

## 5.6 Software Debugging

Debugging is the process of locating, analyzing, and fixing defects identified by testing.

- **Approaches:**

  - *Brute Force:* Memory dumps, tracing log statements everywhere.

  - *Backtracking:* Tracing code execution backward from the failure point to locate defect origin.

  - *Cause Elimination:* Forming hypotheses, running targeted tests, and isolating faulty logic.

  

---

  

## 5.7 Software Maintenance

Modifications made to a software product after delivery to correct defects, improve performance, or adapt to a changing environment.

  

### Types of Maintenance

- **Corrective Maintenance (Reactive):** Fixing faults and bugs discovered in production (typically 20% of maintenance effort).

- **Adaptive Maintenance:** Modifying software to function within altered operational environments (new OS, cloud infrastructure, updated hardware; ~20%).

- **Perfective Maintenance:** Enhancing performance, user experience, and adding new features requested by users (~50% of maintenance effort).

- **Preventive Maintenance (Proactive):** Re-engineering, refactoring, and updating documentation to prevent future bugs (~10%).

  

---

  

## 5.8 Software Quality Models & Standards

  

### 1. McCall's Quality Model

Divides software quality into three perspectives with 11 quality factors:

- **Product Operation:** Correctness, Reliability, Efficiency, Integrity, Usability.

- **Product Revision:** Maintainability, Flexibility, Testability.

- **Product Transition:** Portability, Reusability, Interoperability.

  

### 2. ISO/IEC 9126 Quality Model

Defines software quality through six primary characteristics:

1. **Functionality:** Suitability, Accuracy, Interoperability, Compliance, Security.

2. **Reliability:** Maturity, Fault Tolerance, Recoverability.

3. **Usability:** Understandability, Learnability, Operability, Attractiveness.

4. **Efficiency:** Time Behavior, Resource Utilization.

5. **Maintainability:** Analyzability, Changeability, Stability, Testability.

6. **Portability:** Adaptability, Installability, Co-existence, Replaceability.

*(Note: Superseded by the ISO/IEC 25010 SQuaRE model).*

  

---

  

## 5.9 Process Maturity Models: SEI CMM and CMMI

  

### SEI Capability Maturity Model (CMM)

Defines an evolutionary path from ad-hoc workflows to disciplined, mature software development across 5 maturity levels:

  

```

[Level 5: Optimizing]  <--- Continuous Process Improvement

         │

[Level 4: Managed]     <--- Quantitative Measurement & Quality Metrics

         │

[Level 3: Defined]     <--- Institutionalized Organizational Standards

         │

[Level 2: Repeatable]  <--- Basic Project Tracking & SCM in Place

         │

[Level 1: Initial]     <--- Ad-hoc, Unpredictable, Hero-Driven

```

  

- **Level 1 (Initial):** Ad-hoc, chaotic processes. Success depends on individual heroics; schedules and budgets are unpredictable.

- **Level 2 (Repeatable):** Basic project management techniques established. Policies track cost, schedule, and functionality. Past successes can be repeated on similar projects.

- **Level 3 (Defined):** Processes are formally documented, standardized, and integrated across the entire organization.

- **Level 4 (Managed):** Software process and product quality are quantitatively evaluated through metrics.

- **Level 5 (Optimizing):** Continuous process improvement driven by quantitative feedback and pilot adoption of innovative ideas/technologies.

  

### Capability Maturity Model Integration (CMMI)

An evolution of CMM integrating software, systems, and product development. Provides two representations:

- **Staged Representation:** Organizations progress through discrete maturity levels (1 through 5, as in classical CMM).

- **Continuous Representation:** Evaluates capability levels (0 to 3) for individual Process Areas independently, allowing targeted process improvements.

  

---

  

## 5.10 Software Reliability and Availability

  

### 1. Software Reliability

The probability of failure-free software operation for a specified period of time in a specified environment.

  

#### Core Metrics

- **Mean Time Between Failures (MTBF):** Average operational time between successive system failures.

- **Mean Time To Failure (MTTF):** Expected operational time until a failure occurs.

- **Mean Time To Repair (MTTR):** Average time required to diagnose, repair, and restore the system to service.

$$\text{MTBF} = \text{MTTF} + \text{MTTR}$$

  

### 2. Software Availability

The probability that a system is operational and accessible at a given point in time:

$$\text{Availability } (A) = \frac{\text{MTTF}}{\text{MTTF} + \text{MTTR}} \times 100\% = \frac{\text{MTTF}}{\text{MTBF}} \times 100\%$$

  

- **High Availability Metric ("Five Nines"):**

  $$A = 99.999\% \implies \text{Total unplanned downtime} \le 5.26 \text{ minutes/year}$$