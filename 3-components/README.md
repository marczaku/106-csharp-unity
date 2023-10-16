# Exercises 3 - Components

## Adding Gods

- Create and Open a Scene named `P3Gods`
- Create a MonoBehaviour `P3God`
- Create a MonoBehaviour `P3GodManager`
    - Every Frame, Check, whether The Key `A` was just pressed using `Input.GetKeyDown(KeyCode.A)`.
    - If it was just pressed, then add a new `P3God` Component to the same GameObject as `P3GodManager`
    - Add the Script to a new GameObject `GodManager`
- Test it!
    - You should see more and more `P3God` Components on the GameObject every time you press the `A` Button.

## Removing Gods
- Modify your MonoBehaviour `P3GodManager`
  - Every Frame, Check, whether The Key `R` was just pressed.
  - If it was just pressed, then remove a `P3God` Component from the same GameObject as `P3GodManager`
- Test it!
  - You should see less and less `P3God` Components on the GameObject every time you press the `A` Button.
- Exception!
  - What happens when you try removing Gods when there's none left anymore?
  - How can you fix it? (Hint: Null Check)

## There can only be one
- Modify your Code of adding Gods on your MonoBehaviour `P3GodManager`
  - Instead of adding more and more gods, make sure that not more than one God is added to the same GameObject ever.
  - How can you solve this problem? You don't need any new function, actually. Only the functions that you've already used in this exercise.