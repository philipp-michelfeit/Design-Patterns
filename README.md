# Design-Patterns

## OO Basics

- [x] Abstraction
- [x] Encapsulation
- [x] Polymorphism
- [x] Inheritance

## OO Principles

- [x] Encapsulate what varies
- [x] Favor composition over inheritance
- [x] Program to an interface, not an implementation
- [x] Strive for loosely coupled designs between objects that interact
- [x] Classes should be open for extension, but closed for modification ( Open Closed )
- [x] Depend upon abstractions. Do not depend upon concrete classes. ( Dependency Inversion )

## OO Patterns

#### Strategy
##### Defines a family of algorithms, encapsulates each one, and makes them interchangeable. 
##### Strategy lets the algorithm vary independently from Clients that use it.

```
interface HashAlgorithm {
  public Hash hash();
}
```

```
class SHA2 implements HashAlgorithm {
  @Override
  public Hash hash(){
    return HashAlgorithms.get(this.class.getName()).hash();
  }
  
}
```
#### Observer
##### Defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically.   

```
interface Subject {
  public void registerObserver( Observer o );
  public void removeObserver( Observer o );
  public void notifyObservers();
}
```
```
interface Observer {
  public void update();
}
```

#### Decorator
##### Attaches additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.

```
public class Decorator implements Component {

  private Component wrappedObj;
  
  public void operation();
  
}
```

#### Factory

##### Factory Method
###### Defines an interface for creating an object, but lets subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses.

```
  abstract Product factoryMethod(String type);

```

##### Abstract Factory
###### Provides an Interface for creating families of related or dependent objects without specifying their concrete classes.

```
interface AbstractFactory {
  public Product createProductA();
  public Product createProductB();
}
```

##### Singleton
###### Ensures a class has only one instance, and provides a global point of access to it.

```
public class Singleton {
  private static Singleton uniqueInstance = new Singleton();

  private Singleton(){}
  
  public static Singleton getInstance(){
    return uniqueInstance;
  }
}
```
