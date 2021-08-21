# Design-Patterns

## OO Basics

#### Abstraction
#### Encapsulation
#### Polymorphism
#### Inheritance

## OO Principles

#### Encapsulate what varies
#### Favor composition over inheritance
#### Program to interfaces, not implementations

## OO Patterns

#### Strategy
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
