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
- [x] Classes should be open for extension, but closed for modification 

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
    return Algorithms.get(this.class.getName()).hash();
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
##### ...
