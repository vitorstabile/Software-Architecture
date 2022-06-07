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
    - [Chapter 2 - Part 6: Architectural Drivers](#chapter2part6)
    - [Chapter 2 - Part 7: Functional Requirements](#chapter2part7)
    - [Chapter 2 - Part 8: Business Constraints](#chapter2part8)
    - [Chapter 2 - Part 9: Technical Constraints](#chapter2part9)
    - [Chapter 2 - Part 10: Quality Attributes](#chapter2part10)
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

Thinking like an architect is all about seeing trade-offs in every solution, technical or otherwise, and analyzing those trade-offs to determine what is the best solution. To quote Mark (one of your authors):

- **Architecture is the stuff you can’t Google.**

Everything in architecture is a trade-off, which is why the famous answer to every architecture question in the universe is “it depends.” While many people get increasingly annoyed at this answer, it is unfortunately true. You cannot Google the answer to whether REST or messaging would be better, or whether microservices is the right architecture style, because it does depend. It depends on the deployment environment, business drivers, company culture, budgets, timeframes, developer skill set, and dozens of other factors. Everyone’s environment, situation, and problem is different, hence why architecture is so hard. To quote Neal (another one of your authors):

- **There are no right or wrong answers in architecture—only trade-offs.**

For example, consider an item auction system where someone places a bid for an item up for auction.

<br>

<div align="center"><img src="img/trade1-w626-h242.png" width=626 height=242><br><sub>Fig 8 - Auction system example of a trade-off—queues or topics? - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

The Bid Producer service generates a bid from the bidder and then sends that bid amount to the Bid Capture, Bid Tracking, and Bid Analytics services. This could be done by using queues in a point-to-point messaging fashion or by using a topic in a publish-and-subscribe messaging fashion. Which one should the architect use? You can’t Google the answer. Architectural thinking requires the architect to analyze the trade-offs associated with each option and select the best one given the specific situation.

The two messaging options for the item auction system illustrating the use of a topic in a publish-and-subscribe messaging model,and illustrating the use of queues in a point-to-point messaging model.

<br>

<div align="center"><img src="img/trade2-w630-h242.png" width=630 height=242><br><sub>Fig 9 - Use of a topic for communication between services - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

<br>

<div align="center"><img src="img/trade3-w630-h396.png" width=630 height=396><br><sub>Fig 10 - Use of queues for communication between services - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

The clear advantage (and seemingly obvious solution) to this problem in Figure 9 is that of architectural extensibility. The Bid Producer service only requires a single connection to a topic, unlike the queue solution in Figure 10 where the Bid Pro ducer needs to connect to three different queues. If a new service called Bid History were to be added to this system due to the requirement to provide each bidder with a history of all the bids they made in each auction, no changes at all would be needed to the existing system. When the new Bid History service is created, it could simply subscribe to the topic already containing the bid information. In the queue option shown in Figure 10, however, a new queue would be required for the Bid History service, and the Bid Producer would need to be modified to add an additional connection to the new queue. The point here is that using queues requires significant change to the system when adding new bidding functionality, whereas with the topic approach no changes are needed at all in the existing infrastructure. Also, notice that the Bid Producer is more decoupled in the topic option—the Bid Producer doesn’t know how the bidding information will be used or by which services. In the queue option the Bid Producer knows exactly how the bidding information is used (and by whom), and hence is more coupled to the system.

Thinking architecturally is looking at the benefits of a given solution, but also analyzing the negatives, or trade-offs, associated with a solution. Continuing with the auction system example, a software architect would analyze the negatives of the topic solution. In analyzing the differences, notice first in Figure 9 that with a topic, anyone can access bidding data, which introduces a possible issue with data access and data security. In the queue model illustrated in Figure 10, the data sent to the queue can only be accessed by the specific consumer receiving that message. If a rogue service did listen in on a queue, those bids would not be received by the corresponding service, and a notification would immediately be sent about the loss of data (and hence a possible security breach). In other words, it is very easy to wiretap into a topic, but not a queue.

In addition to the security issue, the topic solution in Figure 9 only supports homogeneous contracts. All services receiving the bidding data must accept the same contract and set of bidding data. In the queue option in Figure 10, each consumer can have its own contract specific to the data it needs. For example, suppose the new Bid History service requires the current asking price along with the bid, but no other service needs that information. In this case, the contract would need to be modified, impacting all other services using that data. In the queue model, this would be a separate channel, hence a separate contract not impacting any other service.

Another disadvantage of the topic model illustrated in Figure 9 is that it does not support monitoring of the number of messages in the topic and hence auto-scaling capabilities. However, with the queue option in Figure 10, each queue can be monitored individually, and programmatic load balancing applied to each bidding consumer so that each can be automatically scaled independency from one another. Note that this trade-off is technology specific in that the Advanced Message Queuing Protocol (AMQP) can support programmatic load balancing and monitoring because of the separation between an exchange (what the producer sends to) and a queue (what the consumer listens to).

Given this trade-off analysis, now which is the better option? And the answer? It depends!

| Topic advantages             | Topic disadvantages                       |
|:-----------------------------|:------------------------------------------|
| Architectural extensibility  | Data access and data security concerns    |
| Service decoupling           | No heterogeneous contracts                |
|                              | Monitoring and programmatic scalability   |

The point here is that everything in software architecture has a trade-off: an advantage and disadvantage. Thinking like an architect is analyzing these trade-offs, then asking “which is more important: extensibility or security?” The decision between different solutions will always depend on the business drivers, environment, and a host of other factors.

#### <a name="chapter2part5"></a>Chapter 2 - Part 5: The Four Levels of Abstraction

<br>

<div align="center"><img src="img/abstraction-w569-h440.png" width=569 height=440><br><sub>Fig 11 - The Four Levels of Abstraction - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

#### <a name="chapter2part6"></a>Chapter 2 - Part 6: Architectural Drivers

Architectural drivers (or Architecturally Significant Requirements - ASRs) are requirements that shape the architecture and include:

<br>

<div align="center"><img src="img/asrs-w540-h486.png" width=540 height=486><br><sub>Fig 12 - Architecturally Significant Requirements - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

Architectural drivers consist of coarse-grained or high-level functional requirements, technical constraints, business constraints, and quality attribute requirements. Each of these exerts forces on the architect and influences the early design decisions that the architect makes. However, the impact of each on the design can be radically different, and they are often in tension with one another. **High-level functionality** is an obvious architectural driver and refers to those general requirements for what the system must do. **Technical and business constraints** are fixed premade decisions that are in place before design begins. **Quality attribute requirements** are properties that the system must possess, such as availability, security, high performance, and so forth. Although it may seem counterintuitive, functional requirements have the least influence on design.

<br>

<div align="center"><img src="img/drivers-w756-h750.png" width=756 height=750><br><sub>Fig 13 - The architectural drivers and their influence on system design. - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

**Were to find these requirements?**

They are not always found in the "requirements document"!

- Many projects do not create or maintain detailed, high-quality documents
- More attention is paid to functional requirements
- Most requirements do not affect the architecture
- Can not wait for requirements to be ready

**When captured, quality attributes are often poorly captured**

- "The system must be modular"
- "The system must have good usability"
- "The system must meet the performance requirements"

**Much of what is important to the architect is not even in the rest**

- ASRs often derive from business objectives
- Qualities of the development team

<br>

<div align="center"><img src="img/asrs-w540-h486.png" width=540 height=486><br><sub>Fig 14 - Looking for ASRs. - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>

**Collect ASRs from stakeholders**

Stakeholders do not know what quality attributes they want in the system

- Insisting on quantitative AQs can result in arbitrary values

Some of these requirements may be difficult to meet

Often, the architect has a more reasonable idea

**Interviewing stakeholders is the best way to determine what they know and what they need**

**The outcome of the stakeholder interviews should include**:

- A list of architectural drivers
- A list of quality attributes scenarios that stakeholders as a whole prioritized

**The information can be used to:**

- Refine the system and software requirements
- Understand and clarify architectural drivers
- Provide the rationale for design decisions
- Guide the development of prototypes and simulations
- Influence the order in which the architecture is developed

#### <a name="chapter2part7"></a>Chapter 2 - Part 7: Functional Requirements

- Functional requirements explain what the system should do

- At the architectural level, what matters is the high-level functionality and not the details

- As the architecture is refined, more information about the requirements is gathered

High-level functional requirements describe in general terms what a system must do. The term high-level is used here to mean general descriptions of functionality, not the details of what is needed. Consider an air traffic control system. For architectural design, it is important that the system tracks air traffic, records flight plans, and prevents collisions, but the kinds of widgets, the colors of the entities on the displays, and other details are not important for architectural design. Although these are important requirements, they typically have little impact on systemic design choices, and they will be developed in detail as the project progresses.

At the architectural level, what matters is the high-level functionality and not the details.

**Communicating Functional Requirements**

- Descriptions
- Use cases

#### <a name="chapter2part8"></a>Chapter 2 - Part 8: Business Constraints

**Constraints**

A constraint is a design decision with 0 (zero) degrees of freedom. That is, it is a pre-existing decision.

**Business Constraints**

- Constraints with architectural impact
- Target market and "time-to-market"
- Cost and benefit expectations
- Delivery process (incremental delivery)
- Expected lifetime of the system
- Availability of resources and experience
- Product lines

**Communication of Business constraints**

- Source
   - Person or artifact that provides the objective
- Subject
   - The stakeholder promoting the objective, individual or organizatione
- Object
   - Entity to which the objective applies
- Environment
   - The context for meeting the goal
   - Social, legal, competitive, client, technological
- Objective
- Description
- Measure
   - A testable metric to validate whether the goal has been achieved
- Pedigree and value
   - The degree of confidence that the person who defined the goal has in it
   - The volatility and value of the objective

#### <a name="chapter2part9"></a>Chapter 2 - Part 9: Technical Constraints

**Constraints**

A constraint is a design decision with 0 (zero) degrees of freedom. That is, it is a pre-existing decision.

**Technical Constraints**

- Pre-existing design decisions that shape the architecture
- Use or integration with legacy systems
- Technologies, programming languages, protocols, standards, among others.
- They may have different origins, but all have an impact on architecture

**Communication of technical constraints**

- Rationale
- Rationale
- Viable alternatives
- Origin (stakeholders)

#### <a name="chapter2part10"></a>Chapter 2 - Part 10: Quality Attributes

Quality attributes are characteristics that the system must have in addition to functionality and are also called "Non-Functional Requirements"

- This term is confusing because it is impossible to describe a quality attribute and some constraints without including functionality

Quality attributes are the most difficult architectural drivers to identify, define, and test.

Quality attributes and architectural constraints condition architecture much more than functional requirements

The architecture is fundamental to ensure the fulfillment of quality attributes

Promoting a quality attribute in the architecture can negatively influence the fulfillment of another quality attribute.

Architecture is essential for balancing tradeoffs between quality attributes.

- Availability vs. Performance
- Performance vs. Security
- Portability vs extensibility

Most of the time, quality attributes are in "tension" with each other and It is important to prioritize quality attributes. Some qualities of the system have no impact on the architecture, like Usability (Choosing buttons, form elements and etc...)

**Communication of Quality Attributes**

- Quality attributes are difficult to identify and describe
- Just using the name is not enough
- Vocabulary varies
- Descriptions are vague and non-quantifiable
- Literature definitions are too simple and unhelpful
- They are often the source of little useful discussions

Ex: "The system must be modifiable"

- Useless ... The system is not always modifiable and does not support any and all changes
- Each system is modifiable in response to some but not all changes
- What prevents the modification of a system is cost and time

An efficient way to describe quality attributes is the **Scenarios** that we can Quantify quality attributes, Prioritize scenarios, Make architectural decisions that balance quality attributes and The quantification allows to measure compliance, completeness and success

**Scenarios of quality attributes**

An efficient way to describe quality attributes
Quantify quality attributes through scenarios
Prioritize scenarios
Make architectural decisions that balance quality attributes
The quantification allows to measure compliance, completeness and success

**Stimulus source**
   - This is an entity (a human being a computer system, or any other actuator) that generated the stimulus.
   
**Stimulus**
   - Stimulation is a condition that requires an answer when one arrives at a system.
   
**Environment**
   - Stimulation occurs under certain conditions. The system may be in an overload condition or in normal operation, or some other relevant condition. For many systems, the "normal" operation may refer to one of a number of modes.
   
**Artifact**
   - Some artifact is stimulated. This can be a collection of systems, the whole system, or some part or parts of it.
   
**Response**
   - The response is the specific activity as the result of the arrival of the stimulus.
   
**Measure the response**
   - When the response occurs, it must be measured in some way so that the requirement can be tested.

<br>

<div align="center"><img src="img/qualityscenarios-w1017-h693.png" width=1017 height=693><br><sub>Fig 15 - Quality Scenario Example - (<a href='https://www.uc.pt/en/fctuc/dei'>Work by University of Coimbra - DEI - https://www.uc.pt/en/fctuc/dei </a>) </sub></div>

<br>


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
