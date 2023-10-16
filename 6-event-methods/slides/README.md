# Slides 6 - Unity Event Methods

Unity's Event Methods are Methods that, if your class defines them, are automatically invoked at the right time by the Unity Engine. It's using Black Magic (Reflection) to do so.

## Initialization

- `void Awake()`
- `void Start()`
- `void OnDestroy()`

## Update

- `void Update()`
- `void LateUpdate()`
- `void FixedUpdate()`

## Toggling

- `void OnEnable()`
- `void OnDisable()`

## Collision

- `void OnCollisionEnter(Collision other)`
- `void OnCollisionStay(Collision other)`
- `void OnCollisionExit(Collision other)`
- `void OnTriggerEnter(Collider other)`
- `void OnTriggerStay(Collider other)`
- `void OnTriggerExit(Collider other)`

## Other
- `void OnApplicationQuit()`
- `void OnApplicationPause(bool isPause)`
- `void OnGUI()`
- `void OnValidate()`
- `void OnDrawGizmos()`
- `void Reset()`