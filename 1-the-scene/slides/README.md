# Slides 1 - The Scene

Scenes contain GameObjects. You can't make a Game in Unity without having a Scene. So let's start here.

## Opening through the Editor

You can open a Scene through the Project Window by Double-Clicking on it.

## Opening through Code

You can also open a Scene through Code using:

```csharp
UnityEngine.SceneManagement.SceneManager.LoadScene("SecondScene");
```

But you also need to add the Scene that you want to open to your Build Settings.

## What happens?
Whenever you load another Scene through Code:
- the current Scene is unloaded
  - this will destroy all current GameObjects
- the new Scene is loaded
  - this will instantiate all GameObjects of the Scene

## Use Cases
- switch from one menu to another
- switch from one level to another

## Intentionally Left Out
- Unloading Single Scenes
- Checking for Loaded Scenes
- Loading Scenes Additively