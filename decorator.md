# Decorator Pattern
Extension at runtime than compile time .  (Open for extension and Closed for modification. )

## Main essence 
- Inheritance. 
- Composition
- Delegation

If you inherit behavior through subclassing , you are setting the behavior statically at compile time. In addition , all subclasses must inherit the same behavior. If you set this in runtime through composition , you can dynamically set behavior . 

## Important points to know about decorators. 
- Decorators have the same supertype for the objects they decorate .
- You can use one or more decorators to wrap an object.
- Given that decorators have the same super type for the object it decorates , we can pass around the decorated object instead of original wrapped object.
- Objects can be decorated at run time with as many decorators we like.
 
## When to Use Alternatives 🛠️

Consider alternatives, like subclassing, if:
- Only one or two responsibilities need to be added: Simple subclassing is often clearer and less complex.
- The order of adding responsibilities  matter: Subclassing handles fixed additions more cleanly.
- The added responsibility is a core feature of the object, not a optional, runtime modification. 
- if A-> B not same as B -> A , for the methods we use , decorator might not be the best design pattern.
