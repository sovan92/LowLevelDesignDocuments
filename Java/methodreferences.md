# Method references 
We can understand that method references are lambdas that are converted to method references at runtime. 
There are 4 types. 
## Types of Method reference
1. Static
2. Method references on a particular object.
3. Instance methods on the parameters determined at runtime.
4. Constructor.

### Static types

```java
  interface Converter{
      long roundabout(double num);
  }

  Converter methodRef = Math::round 
  Converter lambda = x -> Math.round(x)
  
```
Look how static method references shall work. On the runtime, the `methodRef` shall take 1 parameter.  Math.round takes one parameter so it works. Math.round is overloaded for both float and double, so Java infers in the runtime that the parameter can be a double. Java looks for method that fits the description , if it finds more than 1 one match or no match it can report an error. 

### Calling Instance method on particular object 

```java
  interface StringStart{

      boolean beginCheck(String s);

  }

  var str = "Zoo";
  StringStart lambda = str::startsWith;
  // Same as
  StringStart lambda = s -> str.startsWith(s)
  
  
```
Notice `str` is an object on which the method reference is getting called.  

### Calling instance method on a parameter without knowing it in advance

```java

  interface StringParameterChecker{
      boolean check(String text);
  }

  StringParameterChecker methodRef = String::isEmpty;
  StringParameterChecker lmbda = x -> x.isEmpty();

  # How to use the methodref
  methodRef.check("") // true
```

### We can combine the Instance method on particular object and instance method on a parameter without knowing it . 

```java

  interface StringTwoParameterChecker{
      boolean check(String text, String prefix);
  }

  StringTwoParameterChecker methodRef = String::startsWith;
  StringTwoParameterChecker methodRef = (s,p)->s.startsWith(p);

  methodRef.check("Zoo", "A");

```
### Calling constuctors

```java

  interface EmptyStringGenerator {
      String create();
  }
  EmptyStringCreator methodRef = String::new;
  EmptyStringCreator lambda = () -> new String();

  var myString = methodRef.create()
  
  // These things can be tricky as well

  interface CopyGenerator {

      String copy(String value);
  }

  CopyGenerator copyGen = String::new;
  CopyGenerator lambda = x->new String(x);

  // Now why does this work: It works as the contructor is of multiple types , one is a default constuctor other is a parameterized constructor.  

```


