Robin Weiland


EIST Important Stuff
==================

[TOC]

<div style="page-break-after: always; break-after: page;"></div>

# UML/Models

# System Design

<img src="res\important stuff\system-design.png" alt="system design" style="zoom:60%;" align="left"/>



Main influence of requirements analysis artifacts to system design

| Requirements analysis      | System Design                                                |
| -------------------------- | ------------------------------------------------------------ |
| Nonfunctional Requirements | 1. Design Goals                                              |
| Functional model           | 2. Subsystem decomposition<br />8. Boundary Conditions       |
| Object model               | 4. Hardware/software mapping<br />5. Persistent data management |
| Dynamic model              | 3. Concurrency<br />6. Global resource handling<br />7. Software control |

# Clues for design Patterns

| Pattern                | Text                                                         |
| :--------------------- | ------------------------------------------------------------ |
| Composite Pattern      | _complex structure_<br />_must have variable depth and width_ |
| Strategy Pattern       | _must provide a policy independent from the mechanism_<br />_must allow to change algorithms at runtime_ |
| Proxy Pattern          | _must be location transparent_                               |
| Observer Pattern (MVC) | _states must synchronized_<br />_many systems must be notified_ |
| Adapter Pattern        | _must interface with an existing object_                     |
| Bridge Pattern         | _must interface to several systems, some of them to be developed in the future_<br />_an early prototype must be demonstrated_<br />_must provide backward compatibility_ |
| Façade Pattern         | _must interface to existing set if objects_<br />_must interface to existing API_<br />_must interface to existing service_ |



---



<div style="page-break-after: always; break-after: page;"></div>