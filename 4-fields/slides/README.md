# Slides 2 - Fields

Fields allow you to define the data that your MonoBehavior instances will contain. It basically works like a variable that belongs to each Component instance.

## Definition
You define the field similar to a variable, but within the Scope `{` `}` of a `MonoBehaviour` and using the `public`-Keyword (otherwise, you won't be able to access it in the next step):
```csharp
public class Player : MonoBehaviour {
    public int Health;
    public string Name;
}
```

In above example, every `Player` will have:
- an Integer `Health` variable (Field)
- a Text `Name` variable (Field)

## Assignment

### Assignment through the Editor
You can assign new Values to the Field in the Editor by selecting the GameObject and changing the values in the Inspector. These changes will be saved in the Scene.

#### Play Mode
If you change the values while the Play Mode is active, the changes will be lost upon stopping Play Mode.

### Assignment through Code
To assign a value to a `MonoBehaviour` Field you need:
- an object (Component instance) reference
- to access the Member using the `.` (member-of) operator
```csharp
Player player = new GameObject("First").AddComponent<Player>();
player.Health--;
```

Each `class` instance will have its own individual values:
```csharp
Player first = new GameObject("First").AddComponent<Player>();
Player second = new GameObject("First").AddComponent<Player>();
first.Name="Red";
second.Name="Blue";
```

## Access
To access a value of a `class` Field you need:
- an object (class instance) reference
- to access the Member using the `.` (member-of) operator
```csharp
Console.WriteLine(first.Health);
```

## Initialization?
Class Members are initialized to their default values automatically, there is no need to initialize them manually like with variables:

```csharp
public class Player : MonoBehaviour {
    public int Health; // 0
    public bool WantsToQuit; // false (0)
    public float LevelBonus; // 0f (0)
    public char Initial; // '\0' (0)
    public string Name; // null (0)
}
```

It's valid to access these members without explicitly initializing them:
```csharp
Player first = new GameObject("First").AddComponent<PLayer>();
Console.WriteLine(first.Health);
```

But that's not possible with regular variables:
```csharp
int health;
Console.WriteLine(health); // ERROR
```

## Null Reference Exception
You can't access the members of "nothing":
```csharp
Player first = null;
Console.WriteLine(first.Health); // NullReferenceException
```

## Null Check
You can check, whether a value is null before accessing a Member:
```csharp
if(first != null) {
    Console.WriteLine(first.Health);
}
```

## Use Cases
- Add variable information to Components, e.g.:
  - Add Health, Gold, Name information to Player
- Add configurable information to Components, e.g.:
    - Add Power, Value, Durability to Weapon
    - Add Speed to PlayerController
- Changing variables on other Components, e.g.:
  - the velocity on a RigidBody
  - the position of a Transform
  - the Color of a Sprite

## Intentionally Left Out
- Properties
- SerializeField & other Attributes
- Private Fields