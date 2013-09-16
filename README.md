# Examen
Examen is a testing suite for Java. It it designed to interface
very easily with an existing code-base. Currently, its functionality
is limited; however, the `Examen.run` function allows for tests
to be assessed on a given test class. For example:

```java
public class Test extends Examen {
  public Boolean testArithmetic() {    
    // verify that arithmetic works
    return (1+1) == 2;
  } 
  public static void main(String[] args) {
    Examen.run(Test.class, "testArithmetic", "Verify that arithmetic works as expected.");
  }
}
```

Notice that any test class will inherit from `Examen`. Additionally,
note that its class will be passed as argument to the `run` function.
