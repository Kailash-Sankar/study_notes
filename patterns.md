
### Programming patterns

- Types
  - creational patterns
    - providing object creation mechanisms
  - structural patterns
  - behaviroual patterns
  
- Factory
  - a central function which creates multiple types of objects
  
- Singleton
  - limit the number of instances of an object to one
  - example: Database driver
  
- Strategy
  - encapsualte a set of strategies or function together
  
- Iterator
  - loop over a collection of objects in a certain(custom) order
  
- Observer
  - define one to many relationships (subject to observers)
  - observers watch a subject and wait for an event (event listeners)
  
- Proxy
  - use one object as a placeholder for another
  - control access to an object, instead of using it directly
  
- Mediator
  - define a mediator that encapsulates and controls how some set of objects interact with each other
  
- Visitor
  - add or provide new methods or operations to a an existing object without modfying its source
  - new functionality is kept in a visitor object
  - like extending things

- Command
  - Commands are an object-oriented replacement for callbacks
  - wrap logic as a callable object with actions
  - decoupling

- Facade
  - Hide inner components with a outer layer (like a building)
  - example: Compiler
  
- Bridge(or Adapter)
  - different context based on the bridge (like camera and lens)
  
  
  
General notes:
  - break programs into logically independent components, have dependencies where necessary
  - inspect and understand component interactions, keep one way data flow and classes simple
  - simple number of class types and conventions, keep business logic out of view
  - single responsibility principle
  - ownership graph, which object owns which other objects - parent to child flow
  - singletons (globals) and communication patterns. pub/sub approaches in case of two way dataflows
  - Delegate 
  - Chain of responsibility
  - lazy initialization/lazy loading
  - Adapters
  - Factories
  
  
