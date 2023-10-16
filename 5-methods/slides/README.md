# Slides 3 - Methods

Methods allow you to define behaviour on your MonoBehaviours. They are functions that each class instance has.

## Definition
You define the method similar to a function, but within the Scope `{` `}` of a `MonoBehaiour` and using the `public`-Keyword (otherwise, you won't be able to access it in the next step):
```csharp
public class Player {
    public void SayHello() {
        Console.WriteLine("Hello");
    }
}
```

## Invocation
To invoke a value to a `class` Method you need:
- an object (Component instance) reference
- to access the Member using the `.` (member-of) operator
```csharp
Player first = new GameObject().AddComponent<Player>();
first.SayHello();
```

## Member Access
What makes Methods so special and why can you only invoke them on class instances? Because you can access component instance members like Fields and Methods from within the methods. That's really useful!

```csharp
public class Cookies : MonoBehaviour {
    public int amount;
    
    public void OnClick() {
        amount++;
    }
}
```

## Context Menu
Something that I sometimes find convenient for Testing and Debugging: If you add a `[ContextMenu("MethodName")]`-Attribute over your Method, you can invoke it by right-clicking on your Component and clicking on the Method Name:

```csharp
[ContextMenu("Spawn")]
public void Spawn(){
    // ...
}
```

## Intentionally Left Out
- Private Methods
- Static Methods