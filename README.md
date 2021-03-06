# Mock University System
Mock university system developed as part of the Software Project Analysis subject from PUC Minas' graduate program.

## Languages

This project uses Java 8 with Spring for the backend and React for the frontend.

## Architectural decisions

In the sections bellow, the architectural decisions on how to develop such a system are discussed.

### Architecture

Domain Driven Design was chosen as the architecture for this project mainly because university-wide systems tend to envelop large groups of domains, with intrincated and complex business rules. Also, systems of this type tend to need a certain level of scalability - since subject enrollment periods and other moments in which there are usage peaks will certainly demand a considerably bigger amount of computational effort from the system than that in which it would normally run given common circumstances.

Domain Driven Design is a good choice for both situations presented, since it presents the possibility of encapsulating complex business rules, while still maintaining a level of modularity that would make the system electable for usage within a microservice architectural style.

### Architectural style

Microservices where selected as the architectural style primarily because of the need of scalability from certain parts of the system in usage peaks - such as enrollment, mid-term and finals periods. Situations like this require more computing power from certain services of the system - e.g. the enrollment and grade recording systems, in the examples given - while not scaling other parts of the system.

### Architectural pattern

MVVM was chosen as the architectural pattern to separate development of graphical user interfaces and server-side business logic (encapsulated as domains in the DDD architecture).

## Scaffolding

The initial scaffolding was done via the Springboot Initializr, which generates the general skeleton needed for the application.
