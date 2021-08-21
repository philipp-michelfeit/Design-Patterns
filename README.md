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
    return SHA2.hash();
  }
  
  private HashCode hash(){
    return "Assd7576474657eddjddedrsswertzui665";
  }
  
}
```
#### Observer
```
function b()
```
