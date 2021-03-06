# Design Patterns

This repository is for learning basic design patterns. It is based on:

- [Refactoring Guru web site](https://refactoring.guru/).
- [Head First Design Patterns book](https://www.oreilly.com/library/view/head-first-design/0596007124/).

## Software Design Principles

- Encapsulate what varies.
- Program to an interface, not an implementation. Depend
on abstractions, not on concrete classes.
- Favor composition over inheritance.

## SOLID Principles

- Single Responsibility Principle. A class should have just one reason to change.
- Open/Closed Principle. Classes should be open for extension but closed for modification.
- Liskov Substitution Principle. When extending a class, remember that you should be able to pass objects of the subclass in place of objects of the parent class without breaking the client code.
- Interface Segregation Principle. Clients shouldn’t be forced to depend on methods they do not use.
- Dependency Inversion Principl. High-level classes shouldn’t depend on low-level classes. Both should depend on abstractions. Abstractions shouldn’t depend on details. Details should depend on abstractions.

## Creational Design Patterns

### Factory Method Pattern

Factory Method is a creational design pattern that provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created.

![Factory Method](uml/factory_method/factory_method.png)

### Abstract Factory Pattern

Abstract Factory is a creational design pattern that lets you produce families of related objects without specifying their concrete classes

![Abstract Factory](uml/abstarct_factory/abstract_factory.png)

### Singleton Pattern

Singleton is a creational design pattern that lets you ensure that a class has only one instance, while providing a global access point to this instance.

![Singleton](uml/singleton/singleton.png)

### Builder

Builder is a creational design pattern that lets you construct complex objects step by step. The pattern allows you to produce different types and representations of an object using the same construction code.

![Builder](uml/builder/builder.png)

### Prototype Pattern

Prototype is a creational design pattern that lets you copy existing objects without making your code dependent on their classes.

![Prototype](uml/prototype/prototype.png)

## Structural Design Patterns

### Bridge

Bridge is a structural design pattern that lets you split a large class or a set of closely related classes into two separate hierarchies—abstraction and implementation—which can be developed independently of each other.

![Bridge](uml/bridge/bridge.png)

### Decorator Pattern

Decorator is a structural design pattern that lets you attach new behaviors to objects by placing these objects inside special wrapper objects that contain the behaviors.

![Decorator](uml/decorator/decorator.png)

### Adapter Pattern

Adapter is a structural design pattern that allows objects with incompatible interfaces to collaborate.

![Adapter](uml/adapter/adapter.png)

### Facade Pattern

Facade is a structural design pattern that provides a simplified interface to a library, a framework, or any other complex set of classes.

![Facade](uml/facade/facade.png)

### Composite Pattern

Composite is a structural design pattern that lets you compose objects into tree structures and then work with these structures as if they were individual objects.

![Composite](uml/composite/composite.png)

### Proxy Pattern

Proxy is a structural design pattern that lets you provide a substitute or placeholder for another object. A proxy controls access to the original object, allowing you to perform something either before or after the request gets through to the original object.

![Proxy](uml/proxy/proxy.png)

### Flyweight

Flyweight is a structural design pattern that lets you fit more objects into the available amount of RAM by sharing common parts of state between multiple objects instead of keeping all of the data in each object.

![Flyweight](uml/flyweight/flyweight.png)

## Behavioral Design Patterns

### Strategy Pattern

Strategy is a behavioral design pattern that lets you define a family of algorithms, put each of them into a separate class, and make their objects interchangeable.

![Strategy](uml/strategy/strategy.png)

### Observer Pattern

Observer is a behavioral design pattern that lets you define a subscription mechanism to notify multiple objects about any events that happen to the object they’re observing.

![Observer](uml/observer/observer.png)

### Command Pattern

Command is a behavioral design pattern that turns a request into a stand-alone object that contains all information about the request. This transformation lets you parameterize methods with different requests, delay or queue a request’s execution, and support undoable operations.

![Command](uml/command/command.png)

### Template Method Pattern

Template Method is a behavioral design pattern that defines the skeleton of an algorithm in the superclass but lets subclasses override specific steps of the algorithm without changing its structure.

![Template Metod](uml/template_method/template_method.png)

### Iterator Pattern

Iterator is a behavioral design pattern that lets you traverse elements of a collection without exposing its underlying representation (list, stack, tree, etc.).

![Iterator](uml/iterator/iterator.png)

### State Pattern

State is a behavioral design pattern that lets an object alter its behavior when its internal state changes. It appears as if the object changed its class.

![State](uml/state/state.png)

### Chain of Responsibility

Chain of Responsibility is a behavioral design pattern that lets you pass requests along a chain of handlers. Upon receiving a request, each handler decides either to process the request or to pass it to the next handler in the chain.

![Chain of Responsibility](uml/chain_of_responsibility/chain_of_responsibility.png)

### Interpreter Pattern

The interpreter pattern is a design pattern that specifies how to evaluate sentences in a language. The basic idea is to have a class for each symbol (terminal or nonterminal) in a specialized computer language. The syntax tree of a sentence in the language is an instance of the composite pattern and is used to evaluate (interpret) the sentence for a client.

![Interpreter](uml/interpreter/interpret.png)

### Mediator Pattern

Mediator is a behavioral design pattern that lets you reduce chaotic dependencies between objects. The pattern restricts direct communications between the objects and forces them to collaborate only via a mediator object.

![Mediator](uml/mediator/mediator.png)

### Memento Pattern

Memento is a behavioral design pattern that lets you save and restore the previous state of an object without revealing the details of its implementation.

![Memnto](uml/memento/memento.png)

### Visitor Pattern

Visitor is a behavioral design pattern that lets you separate algorithms from the objects on which they operate.

![Visitor](uml/visitor/visitor.png)

## MVCS Pattern

- The model is responsible for managing the data of the application. It receives user input from the controller.
- The view means presentation of the model in a particular format.
- The controller responds to the user input and performs interactions on the data model objects. The controller receives the input, optionally validates it and then passes the input to the model.

### Model

The central component of the pattern. It is the application's dynamic data structure, independent of the user interface. It directly manages the data, logic and rules of the application.

### View

Any representation of information such as a chart, diagram or table. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.

### Controller

Accepts input and converts it to commands for the model or view.
In addition to dividing the application into these components, the model–view–controller design defines the interactions between them.

### Service

Between the controller and the model sometimes goes a layer which is called a service. It fetches data from the model and lets the controller use the fetched data. This layer allows to separate data storage (model), data fetching (service) and data manipulation (controller). Since this layer is not part of the original MVC concept, it is optional in most cases but can be useful for code management and reusability purposes in some cases.
