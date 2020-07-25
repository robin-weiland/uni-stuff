Robin Weiland


EIST Summary
==================

[TOC]

<div style="page-break-after: always; break-after: page;"></div>

# 01 Introduction

---

```mermaid
graph RL
    N1(Problem Solving)
    N2(Dealing with Complexity)
    N3(Dealing with Change)

    N1---N2
    N3---N1
    N3---|Software Engineering|N2

linkStyle default color:#f00
```

## Abstraction

>   *The 7 ± 2 phenomena*
>   Our short term memory cannot store more than 7 ± 2 pieces at the same time
>   $\rightarrow$ chunking: Group collection of objects to reduce complexity


- thought process $\longrightarrow$ **activity**
- result $\longrightarrow$ **entity**

> Abstraction as a model of a *priorly*, *currently* or *not yet existing system*.

## Typical Models

|                      |                |                                          |
| :------------------- | :------------- | ---------------------------------------- |
| **Object** Model     | **entities**   | **structure** of the system?             |
| **Functional** Model | **use cases**  | **functions** of the system?             |
| **Dynamic** Model    | **activities** | system's **reaction to external events** |

> System model: object model + functional model + dynamic model

## Difficulties in software development

- Problem's **ambiguity**                     <img src="res\impossible-trident.png" alt="impossible trident" style="zoom:60%;" /> [impossible trident](https://en.wikipedia.org/wiki/Impossible_trident)
- **Requirements** are usually **unclear** and **change** when they become clearer
- The **problem domain** (also **application domain**) is **complex**, and so is the **solution domain**
- The **development process** is **difficult to manage**
- Software is a **discrete** system
    -   Continuous systems have no hidden surprises
    -   Discrete systems can have hidden surprises! ([Parnas](https://en.wikipedia.org/wiki/David_Parnas))

## Software Engineering as a problem solving activity

```mermaid
graph LR
	N1(Analysis<br \><br \>Understand the nature<br \>of the problem and break<br \>the problem into pieces)
	N2(Synthesis<br \><br \>Put the pieces together<br \>into a larger structure<br \>)
	
	N1==>N2
```

## Techniques, methodologies and tools

|                          Techniques                          |                        methodologies                         |                            tools                             |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Formal procedures** for producing results using some **well defined notation** | **Collection of techniques** applied across software development and unified by a philosophical approach | **Instruments or automated systems** to accomplish a technique |
|                 recipe, quick sort algorithm                 | cookbook, object oriented analysis and design, functional decomposition |            compiler, editor, debugger, IDE, CASE             |

## [Team]

I don't know whether that's important for the exam, but it feels like some bs they could ask in a bad mood.

### Stages of team development

<img src="res\stages-of-team-development.png" alt="stages of team development" style="zoom:60%;" />

### Team productivity and performance

<img src="res\team-productivity-and-performance.png" alt="team productivity and performance" style="zoom:60%;" />

### Difference between group and team

-   ==Group== a number of people that have some relationship to one another
    -   Participants are loosely connected
    -   Do not focus on specific outcomes or a common purpose
    -   Every individual works on his own
-   ==Team== any group of people involved in the same activity with a common goal, especially referring to sports and work
    -   Participants are strongly connected
    -   Focus on a specific outcome, requires coordination of tasks and activities
    -   Members need to work together

## Phenomenon vs. Concept

Phenomenon
​		An **object** in the **world of a domain** as it is **perceived**
​		*This EIST lecture at 9:25		 my black watch*

Concept
		**Common properties** of phenomena
		*All lectures on software engineering		All black watches*

|         | A concept is a 3-tuple                                       |
| :------ | :----------------------------------------------------------- |
| Name    | The name distinguishes the concept from other concepts       |
| Purpose | Properties that determine if a phenomenon is a member of a concept |
| Members | Set of phenomena which are part of the concept               |

> [**Abstraction:**](## Abstraction) classification of phenomena into concepts 
>
> **Modelling:** development of abstractions to answer specific questions about a set of phenomena while ignoring irrelevant details

## Systems, models and views

### Systems

- Organized set of communicating parts
    - Natural system: a system whose ultimate purpose is not known
    - Engineered system: designed and built by engineers for a specific purpose

- The parts of the system can be considered as systems again
    - In this case we call them subsystems

|    natural systems     |  engineered systems  |           subsystems           |
| :--------------------: | :------------------: | :----------------------------: |
| universe, earth, ocean | airplane, watch, GPS | jet engine, battery, satellite |

### Model and View

-   Model: Abstraction of a system
-   View: Selected aspects of a model
-   Notation: Set of Graphical or textual rules for depicting models and views
    -   Informal ("napkin design")
    -   Formal (UML)

|  System  |               Model               |                             View                             |
| :------: | :-------------------------------: | :----------------------------------------------------------: |
| Airplane | Flight simulator<br />Scale model | Blueprint of the airplane<br />electric wiring diagram<br />an airplane breaking the sound barrier |

### Napkin Notation 

<img src="res\napkin-notation.png" alt="napkin notation" style="zoom:60%;" />

### UML Notation

<img src="res\uml-notation.png" alt="uml notation" style="zoom:60%;" />

## Overview of UML diagrams

<img src="res\uml-overview.png" alt="uml overview" style="zoom:50%;" />

## OOP principles (some with maybe not so obvious terminology)

### Type & instance

|  name   |     purpose     |            members            |
| :-----: | :-------------: | :---------------------------: |
|   int   | integral number | $\N_{\text{in memory range}}$ |
| boolean |     logical     |         {true, false}         |

These relationships are similar

-   Type $\longleftrightarrow$ variable
-   Concept $\longleftrightarrow$ Phenomenon
-   Class $\longleftrightarrow$ Object

### Encapsulation

>   Encapsulation means creating classes for such objects to define
>   -   Structure / state by using attributes
>   -   Functionality / behavior by providing methods
>   
>   <img src="res\java-encapsulation.png" alt="java encapsulation" style="zoom:40%;" align="left" />

<div style="page-break-after: always; break-after: page;"></div> 

# 02 Model based Software Engineering

---

## Software Lifecycle

-   Set of activities and their relationships to each other to support the development if a software system
-   Examples of activities: requirements elicitation, analysis, system design, implementation, testing, configuration management, delivery
-   **Software lifecycle model** An abstraction representing the development of software for the purpose of understanding, monitoring or controlling the development of software

|                       |                                                         |
| :-------------------- | :------------------------------------------------------ |
| Requirements analysis | What is the problem?                                    |
| System design         | What is the solution?                                   |
| Object design         | What are the best mechanisms to implement the solution? |
| Implementation        | How is the solution constructed?                        |
| Testing               | How is the problem solved?                              |
| Delivery              | Can the customer use the solution?                      |
| Maintenance           | Are enhancements needed?                                |

A **lifecycle** is based (loosely) on the metaphor of the life of a person

```mermaid
graph LR
	L1(Conceptption)
	L2(Childhood)
	L3(Adulthood)
	L4(Retirement)
	
	D1(Pre-Development)
	D2[Development]
	D3(Post-Development)
	
	L1-->L2-->L3-->L4
	D1-.->D2-.->D3
	
	L1==>D1
	L2==>D2
	L3==>D3 --> D2 & D1
	
	D3==>D2
	D3==>D1
```

## Tailoring

>   There is no “one size fits all” software lifecycle model that works for all possible software engineering projects

| Tailoring | adjusting a lifecycle model to fit a project    |
| :-------- | :---------------------------------------------- |
| naming    | adjusting the naming of activities              |
| cutting   | removing activities not needed in the project   |
| ordering  | defining the order the activities take place in |

## Controlling software development with a process

|            organizational maturity (Humphrey '89)            |                    agility (Schwaber '01)                    |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| Repeatable process<br />Capability Maturity Model Integration (CMMI) | Large parts of the _sd_ is empirical in nature<br />they cannot be modelled with a defined process |



## Defined vs Empirical process

|                     Defined process                     |              Empirical process              |
| :-----------------------------------------------------: | :-----------------------------------------: |
| Planed<br />Follows strict rules<br />Avoids deviations | Not entirely planned<br />inspect and adapt |

<div style="page-break-after: always; break-after: page;"></div>

# 03 Requirements Analysis

---



<div style="page-break-after: always; break-after: page;"></div>

# 04 System Design I

---

<div style="page-break-after: always; break-after: page;"></div>

# 05 System Design II

---

<div style="page-break-after: always; break-after: page;"></div>

# 06 Object Design I

---

<div style="page-break-after: always; break-after: page;"></div>

# 07 Object Design II

---

<div style="page-break-after: always; break-after: page;"></div>

# 08 Testing

---

<div style="page-break-after: always; break-after: page;"></div>

# 10 Software Configuration Management

---

<div style="page-break-after: always; break-after: page;"></div>

# 11.1 Software Quality Management

---

<div style="page-break-after: always; break-after: page;"></div>

# 11.2 Guest Lecture: Dr. Elmar Jürgens

---

<div style="page-break-after: always; break-after: page;"></div>

# 12 Project Management

---

<div style="page-break-after: always; break-after: page;"></div>