# Slides 3 - Components

Components change, what a GameObject behaves like. A GameObject can have one or more Components. It always has a `Transform` Component.

## Adding

### Adding through the Editor
You can Add any type of component the same way as you already add your `MonoBehaviour`

### Adding through Code
You can add a new component to a `GameObject` through Code as well:

```csharp
BoxCollider boxCollider = this.gameObject.AddComponent<BoxCollider>();
Rigidbody rigidBody = this.gameObject.AddComponent<Rigidbody>();
```

## Getting through Code

```csharp
Rigidbody rigidBody = enemy.GetComponent<Rigidbody>();
```

## Removing

### Removing through the Editor
You can right-click on a component in the Inspector to `Remove Component`

### Removing through Code
You can Remove Components the same way as GameObjects:
```csharp
Destroy(rigidBody);
```

## Enabling and Disabling

You don't have to enable or disable whole GameObjects, you can also enable and disable single components.

### Dis-/Enabling through the Editor
You can use the checkbox next to the Component Name in the Inspector.

### Dis-/Enabling through Code
```csharp
rigidBody.enabled = false;
rigidBody.enabled = true;
```

## Use Cases
For many Game Mechanics, e.g.:
- add Burning Component to an enemy hit by fire ball spell
- remove Collider from a door destroyed by a bomb
- add Shield Component to player after picking up a power-up
- Disable Renderer Component to make player invisible after picking up a power-up

## Intentionally Left Out
- Caching Component References
- Finding Components in Scene
