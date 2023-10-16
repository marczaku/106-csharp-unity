# Exercises 2 - GameObjects

## Blue Adders

- Create and Open a Scene named `P2BlueVsRed`
- Create a MonoBehaviour `P2BlueAdder`
  - Every Frame, Create a new GameObject with the Name `Blue`
  - Add the Script to a new GameObject `BlueAdder`
- Test it!
  - You should see more and more `Blue` GameObjects.

## Blue Removers
- Create a MonoBehaviour `P2BlueRemover`
  - Every Frame, Find a GameObject with the Name `Blue` and Destroy it
  - Make sure that you don't see Errors in the Console
  - Add the Script to a new GameObject `BlueRemover`
- Test it!
  - You shouldn't see many `Blue` GameObjects Spawning anymore this time
  - Play around with Disabling and Enabling either the `Adder` or the `Remover` Scripts

## Blue Converters
- Create a MonoBehaviour `P2BlueConverter`
  - Every Frame, Find a GameObject with the Name `Blue` and Change its name to `Red`
  - Make sure that you don't see Errors in the Console
  - Add the Script to a new GameObject `BlueConverter`