# Slides 0 - Scripting 101

## MonoBehaviour

If you want to write Code in Unity, there's more than one way, but the most important one is creating `MonoBehaviours`.
- In Unity
- Right-Click in your Projects Window
- Select `Create` > `C# Script`
- Enter a name, e.g. `MyFirstScript`

The following file will be created.

```csharp
using UnityEngine;

public class MyFirstScript : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        
    }
}

```

## Adding it to a GameObject

Unless your MonoBehaviour is attached to a GameObject, it only exists as a template, so to say. To make it part of your Game, you need to attach it to a GameObject.
- Either Drag and Drop the Script from your Project Window onto a GameObject
- Or Select the GameObject and click `Add Component` and then enter the Name of your Script

## Console.WriteLine

Using `Console.WriteLine` won't have any effect in Unity Projects.

## Debug.Log

The easiest way of generating Output in Unity is by using `Debug.Log`. It works the same as `Console.WriteLine` in C#. Add the following to the `Start` Method of your Script:

```csharp
Debug.Log("Put your message here.");
```

## Seeing it in Action

Start the Play Mode in Unity to see your Script in Action.