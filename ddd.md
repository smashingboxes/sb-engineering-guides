# Domain-Driven Design

## Ubiquitous Language
#### Problem
A client requests a feature or reports a problem to a PM. The PM creates a Jira issue and assigns it to an engineer. The engineer reads the issue and there is a lot of room for interpretation to what there is to be done.

#### Technique
Everyone involved in the project should speak a common language that prevents ambiguity while talking about domain logic. This ubiquitous language is the intersection of technical and business terms that is relevant for both sides.

"Use the model as the backbone of a language. Commit the team to using that language relentlessly in all communication within the team and in the code. Use the same language in diagrams, writing, and, especially speech.

Iron out difficulties by experimenting with alternative expressions, which reflect alternative models. Then refactor the code, renaming classes, methods and modules to conform to the new model. Resolve confusion over terms in conversation, in just the way we converge on agreed meaning of ordinary words." [1]


## Model-Driven Design
#### Problem
Once you start to design software based on your model of the domain you usually find reasons to depart from the original model.

#### Technique
"Design a portion of the software system to reflect the domain model in a very literal way, so that mapping is obvious." [2] As soon as you start to depart from it: "Revisit the model and modify it to be implemented more naturally in software". [2]

"Concentrate all the code related to the domain model in one layer and isolate it from the user interface, application, and infrastructure code. The domain objects, free of the responsibility of displaying themselves, storing themselves, managing application tasks, and so forth, can be focused on expressing the domain model." [2]


## Domain Events
#### Problem
"An entity is responsible for tracking its state and the rules regulating its lifecycle. But if you need to know the actual causes of the state changes, this is typically not explicit, and it may be difficult to explain how the system got the way it is." [2]

#### Technique
"Model information about activity in the domain as a series of discrete events. Represent each event as a domain object. These are distinct from system events that reflect activity within the software itself [...]

A domain event is a full-fledged part of the domain model, a representation of something that happened in the domain. Ignore irrelevant domain activity while making explicit the events that the domain experts want to track or be notified of, or which are associated with state change in the other model objects. [...]

Domain events are ordinarily immutable, as they are a record of something in the past. In addition to a description of the event, a domain event typically contains a timestamp for the time the event occurred and the identity of entities involved in the event. Also, a domain event often has a separate timestamp indicating when the event was entered into the system and the identity of the person who entered it. When useful, an identity for the domain event can be based on some set of these properties. So, for example, if two instances of the same event arrive at a node they can be recognized as the same." [2]


## Sources
[1] Domain-Driven Design, Eric Evans, 2003

[2] [Domain-Driven Design Reference, Eric Evans, 2015](http://domainlanguage.com/wp-content/uploads/2016/05/DDD_Reference_2015-03.pdf)
