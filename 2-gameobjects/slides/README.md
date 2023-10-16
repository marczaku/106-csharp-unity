# Slides 2 - GameObjects

Scenes contain GameObjects, therefore, we'll continue learning about these.

## Creation

### Creation through the Editor
You can Right-Click in the Scene and create `New Empty` GameObject and then configure a Name.

### Creation through Code
In Code, you can create GameObjects like this:

```csharp
GameObject monster = new GameObject("Monster");
```

## Finding through Code

### Find Attached GameObject
If you want to get the GameObject, that the MonoBehaviour is attached to, you can use its `gameObject` Property:
```csharp
GameObject myGameObject = this.gameObject;
```

### Finding Other GameObjects

If you want to work with other GameObjects, e.g. to Change their Name, you need to Find Them in the Scene through their name first:
```csharp
GameObject player = GameObject.Find("Player");
```

## Null Checking
When trying to Find a GameObject, it can be, that no GameObject exists with that name. You should therefore check, whether it was found:

```csharp
if(player != null) {
    Debug.Log("Found the Player!");
}
```

## Destruction

### Garbage Collector?
Since GameObjects become part of your Scene, they are not automatically Garbage Collected. You need to manually Destroy them, if you want them to disappear again.
- Or Load a new Scene
- Or Stop Play Mode

### Destruction through the Editor
You can right-click on a GameObject and select `Delete`

### Destruction through Code
It is just as easy to Destroy a GameObject through Code
```csharp
Destroy(monster);
```

## Enabling and Disabling

### Dis-/Enabling through the Editor
You can select a GameObject and enable/disable it in the Inspector through the Checkbox.

### Dis-/Enabling through Code
To disable a GameObject, you can use this Code:
```csharp
monster.SetActive(false);
```

```csharp
monster.SetActive(true);
```

## Renaming

### Renaming through the Editor
You can select a GameObject and change its name through the Inspector's Name TextField.

### Renaming through Code
To disable a GameObject, you can use this Code:
```csharp
monster.SetActive(false);
```

```csharp
monster.SetActive(true);
```

## Duplicate

### Duplicating through the Editor
You can select a GameObject and duplicate it through the (right-click) Context Menu or by using Ctrl+D

### Duplicating through Code
This is one of the most powerful functions in Unity! Say you have a Bullet GameObject prepared already, so you can duplicate it like this:

```csharp
Instantiate(bullet);
```

## What happens?
Whenever you create a new GameObject:
- the GameObject is created
- you can see it in the Hierarchy View in the Editor
- a Transform component is added
- if you used `Instantiate`:
  - all Components that the original had are added to the new GameObjects
  - all Component Values that the original had are copied to the new Components
  - if the GameObject had any children, they are also instantiated!
- it is assigned to the currently loaded Scene
  - which means that it is Destroyed when loading another Scene

## Use Cases
To Spawn new Objects to your Game:
- spawning new items
- spawning new monsters
- spawning bullets
To Destroy Objects in your Game:
- a player after disconnecting
- an enemy after defeating
- a power-up after picking it up

## Intentionally Left Out
- Tags
- FindWithTag
- DestroyImmediate