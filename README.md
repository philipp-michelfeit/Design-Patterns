# Design-Patterns

## Design Principles

#### Abstraction
#### Programming to an Interface

## Design Patterns

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
