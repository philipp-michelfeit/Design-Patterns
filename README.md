# Design-Patterns

## OO Basics

#### [x] Abstraction
#### [x] Encapsulation
#### [x] Polymorphism
#### [x] Inheritance

## OO Principles

#### Encapsulate what varies
#### Favor composition over inheritance
#### Program to an interface, not an implementation

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
    return AlgorithmFactory.get(this.class.getName()).hash();
  }
  
}
```
#### Observer
```
interface Observer {
  public void observe();
}
```
