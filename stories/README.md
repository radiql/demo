# RADiQL Stories: User Stories and Use Cases

RADiQL defines a Story as *either* a User Story or a Use Case. These are 
considered broadly equivalent in a completed system. The fundamental difference 
between them is the process by which User Stories and Use Cases are produced. 

User Stories are often brief one-line descriptions of system behavour that can 
be decomposed into a group of more focussed sub-stories that are "discovered" 
as the softwware is evolved iteratively.

Story implementations typically contain a user interface or some sort, business 
logic and a means of persisting or retrieving data from a persistent data store 
such as a database or a message queue. While the user interface and persistence
mechanisms may be optional, in RADiQL the business logic is fundamental to a 
Story.

## Architectural Significance and Context

Robert C Martin's Clean Architecture promotes User Stores and Use Cases as 
fundamental building blocks of software solutions. RADiQL is an implementation 
of Clean Architecture based upon Flow Based Programming (J Paul Morrision). 

In RADiQL, Story implementations are organised in a folder 
structure that provides a framework for independent development of software 
components that collaborate to deliver working software for each Story. Story
implementations are modular, can be developed in isolation and are independently 
testable. Furthermore, the RADiQL approach facilitates polyglot development, 
leveraging team skills and maximising development productivity while vastly 
improving solution understanding and maintability.

## RADiQL and the Benefits of Clean Architecture

The RADiQL approach provides a radical - pun intended - change in the way 
software is developed. In conventional software development, While product 
requirements are expressed in terms of User Stories or Use Cases, software 
development is typically framework-centric or service-centric of both. For 
example, a User Story may be implemented by invoking calls on services 
(either in-process service objects or remote microservices). There is
therefore an impedence mismatch between requirements and implementation. 

In conventional software development, the technical framework or the 
organisation of microservices is all important to application structure. 
Microservices may provide their own datastore for data entities under their 
control. A Use Case may be spread across several microservices (and in practice 
usually is).

In RADiQL, which is designed from the ground up to deliver the practical 
benefits of Clean Architecture, the structure of the software directly reflects 
the organiation of the Stories. There is a one to one relationship between the 
Story and its implementation. 

Stories are modules that can be assembled into larger Stories or decomposed into
lower level stories.

### Significance of Story-centric Software Architecture

RADiQL defines Story-centric Software Architecture as a software development 
architecture that directly derives its structure from the Stories. Stories 
can be broken down into sub-stories and / or combined with each other to tell
a high-level story about the behaviour of a large-scale solution or complex 
application. In other words, Stories are *composable* and *reusable*.

# Communication Between Stories

Stories communicate with each other via the data that's passed from one
story to another. Each story has inputs and outputs. 

In traditional business analysis, a Business Analyst will carefull define the
data that is consumed and produced by each Use Case. In highly agile User Story 
development, the data is discovered and described by code, with code becoming
the primary tool used to document the system. The requirements may be captured
more formally in a tool such as JIRA.

The important thing to appreciate here is that Stories fundamentally defined 
by two characteristics: 

1. the data that enters them and the data that leaves them
2. the behaviour that they exhibit

In RADiQL, we boil Stories down to these fundamental characteristics, without
any dependency on a particular framework. User Interfaces and data peristence
mechanisms such as databases, event streams or queues are treated as mere
plugins to the application.

User Story / Use Case implementations can be developed in parallel by different 
teams, thereby enchancing develeper productivity by minimising dependencies on 
other teams and software.

## Layering of Use Cases

In RADiQL, User Story Implementations are split into 3 fundamental layers:

1. UI
2. Business Logic
3. Gateways

Martin states that in Clean Architecture, the most important of these to the 
application developer (and organisation) is the Business Logic. This Business 
Logic realises the fundamental value of the system.


