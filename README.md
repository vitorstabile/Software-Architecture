# Content

1. [Chapter 1: Software-Architecture](#chapter1)
    - [Chapter 1 - Part 1: What is Software Architecture](#chapter1part1)
    - [Chapter 1 - Part 2: Structure](#chapter1part2)
    - [Chapter 1 - Part 3: Architecture Characteristics](#chapter1part3)
    - [Chapter 1 - Part 4: Architecture Decisions](#chapter1part4)
    - [Chapter 1 - Part 5: Design Principles](#chapter1part5)
    - [Chapter 1 - Part 6: Who is the Software Architect?](#chapter1part6)
    - [Chapter 1 - Part 7: Why is Software-Architecture relevant?](#chapter1part7)
    - [Chapter 1 - Part 8: Laws of Software Architecture](#chapter1part8)
2. [Chapter 2: Architecturally Significant Requirements](#chapter2)
    - [Chapter 2 - Part 1: Architectural Thinking](#chapter2part1)
    - [Chapter 2 - Part 2: Architecture versus Design](#chapter2part2)
    - [Chapter 2 - Part 3: Technical Breadth](#chapter2part3)
    - [Chapter 2 - Part 4: Analyzing Trade-Offs](#chapter2part4)
    - [Chapter 2 - Part 5: The Four Levels of Abstraction](#chapter2part5)
The Four Levels of Abstraction
3. [Chapter 3: Quality Attributes](#chapter3)
    - [Chapter 3 - Part 1: xxxxxx](#chapter3part1)
    - [Chapter 3 - Part 2: yyyyyy](#chapter3part2)
4. [Chapter 4: Software-Architecture Design](#chapter4)
    - [Chapter 4 - Part 1: xxxxxx](#chapter4part1)
    - [Chapter 4 - Part 2: yyyyyy](#chapter4part2)
5. [Chapter 5: Architectural Styles](#chapter5)
    - [Chapter 5 - Part 1: xxxxxx](#chapter5part1)
    - [Chapter 5 - Part 2: yyyyyy](#chapter5part2)
6. [Chapter 6: Communication of Software Architecture](#chapter6)
    - [Chapter 6 - Part 1: xxxxxx](#chapter6part1)
    - [Chapter 6 - Part 2: yyyyyy](#chapter6part2)
7. [Chapter 7: Software Architectures and Quality](#chapter7)
    - [Chapter 7 - Part 1: xxxxxx](#chapter7part1)
    - [Chapter 7 - Part 2: yyyyyy](#chapter7part2)
8. [Chapter 8: Design Patterns](#chapter8)
    - [Chapter 8 - Part 1: xxxxxx](#chapter8part1)
    - [Chapter 8 - Part 2: yyyyyy](#chapter8part2)
9. [Chapter 9: Economics for Software Architects](#chapter9)
    - [Chapter 9 - Part 1: xxxxxx](#chapter9part1)
    - [Chapter 9 - Part 2: yyyyyy](#chapter9part2)
10. [Chapter 10: Architecture Modelling and Tools](#chapter10)
    - [Chapter 10 - Part 1: xxxxxx](#chapter10part1)
    - [Chapter 10 - Part 2: yyyyyy](#chapter10part2)
11. [Chapter 11: Effective Teams and the Software Architect](#chapter11)
    - [Chapter 11 - Part 1: xxxxxx](#chapter11part1)
    - [Chapter 11 - Part 2: yyyyyy](#chapter11part2)
12. [Bibliography's](#biblio)

## <a name="chapter1"></a>Chapter 1: Software-Architecture

#### <a name="chapter1part1"></a>Chapter 1 - Part 1: What is Software Architecture?

**Architecture is nota a phase of projects**

In this definition, software architecture consists of the structure of the system (denoted as the heavy black lines supporting the architecture), combined with architecture characteristics (“-ilities”) the system must support, architecture decisions, and finally design principles.

Architecture consists of the **structure** combined with **architecture characteristics (“-ilities”)**, **architecture decisions**, and **design principles**

#### <a name="chapter1part2"></a>Chapter 1 - Part 2: Structure

The structure of the system refers to the type of architecture style (or styles) the system is implemented in (such as microservices, layered, or microkernel). Describing an architecture solely by the structure does not wholly elucidate an architecture. For example, suppose an architect is asked to describe an architecture, and that architect responds “it’s a microservices architecture.” Here, the architect is only talking about the structure of the system, but not the architecture of the system. Knowledge of the architecture characteristics, architecture decisions, and design principles is also needed to fully understand the architecture of the system.

<br>

<div align="center"><img src="img/systemstructure-w1397-h973.png" width=600 height=400><br><sub>Fig 1 - Structure refers to the type of architecture styles used in the system - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter1part3"></a>Chapter 1 - Part 3: Architecture Characteristics

The architecture characteristics define the success criteria of a system, which is generally orthogonal to the functionality of the system. Notice that all of the characteristics listed do not require knowledge of the functionality of the system, yet they are required in order for the system to function properly. Architecture characteristics are so important that we’ve devoted several chapters in this book to understanding and defining them.

<br>

<div align="center"><img src="img/architecturecharacteristic-w1397-h973.png" width=600 height=400><br><sub>Fig 2 - Architecture characteristics refers to the “-ilities” that the system must support - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter1part4"></a>Chapter 1 - Part 4: Architecture Decisions

Architecture decisions define the rules for how a system should be constructed. For example, an architect might make an architecture decision that only the business and services layers within a layered architecture can access the database restricting the presentation layer from making direct database calls. Architecture decisions form the constraints of the system and direct the development teams on what is and what isn’t allowed.

If a particular architecture decision cannot be implemented in one part of the system due to some condition or other constraint, that decision (or rule) can be broken through something called a variance. Most organizations have variance models that are used by an architecture review board (ARB) or chief architect. Those models formalize the process for seeking a variance to a particular standard or architecture decision. An exception to a particular architecture decision is analyzed by the ARB (or chief architect if no ARB exists) and is either approved or denied based on justifications and trade-offs.

<br>

<div align="center"><img src="img/architecturedecision-w1397-h973.png" width=600 height=400><br><sub>Fig 3 - Architecture decisions are rules for constructing systems - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter1part5"></a>Chapter 1 - Part 5: Design Principles

The last factor in the definition of architecture is design principles. A design principle differs from an architecture decision in that a design principle is a guideline rather than a hard-and-fast rule. For example, the design principle illustrated above states that the development teams should leverage asynchronous messaging between services within a microservices architecture to increase performance. An architecture decision (rule) could never cover every condition and option for communication between services, so a design principle can be used to provide guidance for the preferred method (in this case, asynchronous messaging) to allow the developer to choose a more appropriate communication protocol (such as REST or gRPC) given a specific circumstance.

<br>

<div align="center"><img src="img/designprinciples-w1397-h973.png" width=600 height=400><br><sub>Fig 4 - Design principles are guidelines for constructing systems - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter1part6"></a>Chapter 1 - Part 6: Who is the Software Architect?

There are eight core expectations placed on a software architect, irrespective of any given role, title, or job description:

- Make architecture decisions
- Continually analyze the architecture
- Keep current with latest trends
- Ensure compliance with decisions
- Diverse exposure and experience
- Have business domain knowledge
- Possess interpersonal skills
- Understand and navigate politics

<br>

<div align="center"><img src="img/softwarearchitecturerole-w800-h600.png" width=800 height=600><br><sub>Fig 5 - Software Architecture Role - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter1part7"></a>Chapter 1 - Part 7: Why is Software-Architecture relevant?

- Inhibit or enable a system’s driving quality attributes.
- Reason about and manage change as the system evolves.
- Early prediction of a system’s qualities.
- Enhances communication among stakeholders.
- Carrier of the earliest, and hence most-fundamental, hardest-to-change design decisions.
- Defines a set of constraints on subsequent implementation.
- Dictates the structure of an organization, or vice versa.
- Provide the basis for incremental development.
- Key artifact that allows the architect and the project manager to reason about cost and schedule.
- Can be created as a transferable, reusable model that forms the heart of a product line.
- Focuses attention on the assembly of components, rather than simply on their creation.
- By restricting design alternatives, architecture channels the creativity of developers, reducing design and system complexity.
- Foundation for training of a new team member.

#### <a name="chapter1part8"></a>Chapter 1 - Part 8: Laws of Software Architecture

While the scope of software architecture is almost impossibly broad, unifying elements do exist. The authors have first and foremost learned the First Law of Software Architecture by constantly stumbling across it:

**Everything in software architecture is a trade-off.** —First Law of Software Architecture

Nothing exists on a nice, clean spectrum for software architects. Every decision must take into account many opposing factors.

**If an architect thinks they have discovered something that isn’t a trade-off, more likely they just haven’t identified the trade-off yet.** —Corollary 1

We define software architecture in terms beyond structural scaffolding, incorporating principles, characteristics, and so on. Architecture is broader than just the combination of structural elements, reflected in our Second Law of Software Architecture:

**Why is more important than how.** —Second Law of Software Architecture

The authors discovered the importance of this perspective when we tried keeping the results of exercises done by students during workshop as they crafted architecture solutions. Because the exercises were timed, the only artifacts we kept were the diagrams representing the topology. In other words, we captured how they solved the problem but not why the team made particular choices. An architect can look at an existing system they have no knowledge of and ascertain how the structure of the architecture works, but will struggle explaining why certain choices were made versus others.

## <a name="chapter2"></a>Chapter 2: Architecturally Significant Requirements

#### <a name="chapter2part1"></a>Chapter 2 - Part 1: Architectural Thinking

An architect sees things differently from a developer’s point of view, much in the same way a meteorologist might see clouds differently from an artist’s point of view.

This is called architectural thinking. Unfortunately, too many architects believe that architectural thinking is simply just “thinking about the architecture.”

Architectural thinking is much more than that. It is seeing things with an architectural eye, or an architectural point of view. There are four main aspects of thinking like an architect:

- **First, it’s understanding the difference between architecture and design and knowing how to collaborate with development teams to make architecture work.** 

- **Second, it’s about having a wide breadth of technical knowledge while still maintaining a certain level of technical depth, allowing the architect to see solutions and possibilities that others do not see.** 

- **Third, it’s about understanding, analyzing, and reconciling trade-offs between various solutions and technologies.** 

- **Finally, it’s about understanding the importance of business drivers and how they translate to architectural concerns.**

#### <a name="chapter2part2"></a>Chapter 2 - Part 2: Architecture versus Design

As shown in the diagram, an architect is responsible for things like analyzing business requirements to extract and define the architectural characteristics (“-ilities”), selecting which architecture patterns and styles would fit the problem domain, and creating components (the building blocks of the system). The artifacts created from these activities are then handed off to the development team, which is responsible for creating class diagrams for each component, creating user interface screens, and developing and testing source code.

To make architecture work, both the physical and virtual barriers that exist between architects and developers must be broken down, thus forming a strong bidirectional relationship between architects and development teams. The architect and developer must be on the same virtual team to make this work. Not only does this model facilitate strong bidirectional communication between architecture and development, but it also allows the architect to provide mentoring and coaching to developers on the team.

Unlike the old-school waterfall approaches to static and rigid software architecture, the architecture of today’s systems changes and evolves every iteration or phase of a project. A tight collaboration between the architect and the development team is essential for the success of any software project. So where does architecture end and design begin? It doesn’t. They are both part of the circle of life within a software project and must always be kept in synchronization with each other in order to succeed.

<br>

<div align="center"><img src="img/archvsdesign-w1404-h646.png" width=800 height=500><br><sub>Fig 6 - Architecture Versus Design - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter2part3"></a>Chapter 2 - Part 3: Technical Breadth

The scope of technological detail differs between developers and architects. Unlike a developer, who must have a significant amount of technical depth to perform their job, a software architect must have a significant amount of technical breadth to think like an architect and see things with an architecture point of view. This is illustrated by the knowledge pyramid shown above, which encapsulates all the technical knowledge in the world. It turns out that the kind of information a technologist should value differs with career stages. any individual can partition all their knowledge into three sections: stuff you know, stuff you know you don’t know, and stuff you don’t know you don’t know.

**Stuff you know**: includes the technologies, frameworks, languages, and tools a technologist uses on a daily basis to perform their job, such as knowing Java as a Java programmer. 

**Stuff you know you don’t know**: includes those things a technologist knows a little about or has heard of but has little or no expertise in. A good example of this level of knowledge is the Clojure programming language. Most technologists have heard of Clojure and know it’s a programming language based on Lisp, but they can’t code in the language. 

**Stuff you don’t know you don’t know**: is the largest part of the knowledge triangle and includes the entire host of technologies, tools, frameworks, and languages that would be the perfect solution to a problem a technologist is trying to solve, but the technologist doesn’t even know those things exist.

However, the nature of knowledge changes as developers transition into the architect role. A large part of the value of an architect is a broad understanding of technology and how to use it to solve particular problems. For example, as an architect, it is more beneficial to know that five solutions exist for a particular problem than to have singular expertise in only one. The most important parts of the pyramid for architects are the top and middle sections; how far the middle section penetrates into the bottom section represents an architect’s technical breadth

Architects should focus on technical breadth so that they have a larger quiver from which to draw arrows. Developers transitioning to the architect role may have to change the way they view knowledge acquisition. Balancing their portfolio of knowledge regarding depth versus breadth is something every developer should consider throughout their career.

<br>

<div align="center"><img src="img/techbreadth-w1278-h1079.png" width=800 height=700><br><sub>Fig 7 - Technical Breadth - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter2part4"></a>Chapter 2 - Part 4: Analyzing Trade-Offs

#### <a name="chapter2part4"></a>Chapter 2 - Part 5: The Four Levels of Abstraction

The four levels of abstraction

## <a name="chapter3"></a>Chapter 3: Quality Attributes

#### <a name="chapter3part1"></a>Chapter 3 - Part 1: xxxxxx

#### <a name="chapter3part2"></a>Chapter 3 - Part 2: yyyyyy

## <a name="chapter4"></a>Chapter 4: Software-Architecture Design

#### <a name="chapter4part1"></a>Chapter 4 - Part 1: xxxxxx

#### <a name="chapter4part2"></a>Chapter 4 - Part 2: yyyyyy

## <a name="chapter5"></a>Chapter 5: Architectural Styles

#### <a name="chapter5part1"></a>Chapter 5 - Part 1: xxxxxx

#### <a name="chapter5part2"></a>Chapter 5 - Part 2: yyyyyy

## <a name="chapter6"></a>Chapter 6: Communication of Software Architecture

#### <a name="chapter6part1"></a>Chapter 6 - Part 1: xxxxxx

#### <a name="chapter6part2"></a>Chapter 6 - Part 2: yyyyyy

## <a name="chapter7"></a>Chapter 7: Software Architectures and Quality

#### <a name="chapter7part1"></a>Chapter 7 - Part 1: xxxxxx

#### <a name="chapter7part2"></a>Chapter 7 - Part 2: yyyyyy

## <a name="chapter8"></a>Chapter 8: Design Patterns

#### <a name="chapter8part1"></a>Chapter 8 - Part 1: xxxxxx

#### <a name="chapter8part2"></a>Chapter 8 - Part 2: yyyyyy

## <a name="chapter9"></a>Chapter 9: Economics for Software Architects

#### <a name="chapter9part1"></a>Chapter 9 - Part 1: xxxxxx

#### <a name="chapter9part2"></a>Chapter 9 - Part 2: yyyyyy

## <a name="chapter10"></a>Chapter 10: Architecture Modelling and Tools

#### <a name="chapter10part1"></a>Chapter 10 - Part 1: xxxxxx

#### <a name="chapter10part2"></a>Chapter 10 - Part 2: yyyyyy

## <a name="chapter11"></a>Chapter 11: Effective Teams and the Software Architect

#### <a name="chapter11part1"></a>Chapter 11 - Part 1: xxxxxx

#### <a name="chapter11part2"></a>Chapter 11 - Part 2: yyyyyy

# Bibliography's <a name="biblio"></a>

Some of references that I use.

1. [Systems Engineering Body of Knowledge][sebok-url]
2. [Software Engineering - Computer Notes][swcomputernotes-url]
3. [Software Engineering - Geeks for Geeks][swgeeks-url]
4. [Software Engineering - Java T Point][swjavatpoint-url]
