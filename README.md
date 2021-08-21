# Design-Patterns

## OO Basics

#### Abstraction
#### Encapsulation
#### Polymorphism
#### Inheritance

## OO Principles

#### Encapsulate what varies
#### Favor composition over inheritance
#### Program to an interface, not an implementation

## OO Patterns

#### Strategy
##### Defines a family of algorithms, encapsulates each one, and makes them interchangeable. Strategy lets the algorithm vary independently from Clients that use it.

```
interface HashAlgorithm {
  public HashCode hashCode();
}
```

```
class SHA2 implements HashAlgorithm {
  @Override
  public HashCode hashCode(){
    return AlgorithmFactory.get("SHA2").hash();
  }
  
}
```
#### Observer
```
interface Observer {
  public void observe();
}
```
