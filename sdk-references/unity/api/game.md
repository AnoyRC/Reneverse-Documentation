# Game()

Initializes `GameAPI` or returns `GameAPI` if initialized already, for the game which contains several functions and variables required to connect, mint, etc.

### Usage

```csharp
GameAPI gameAPI = ReneAPI.Game();
```

or

use the functions provided by `Game()` directly.

```csharp
bool connected = await ReneAPI.Game().Connect(email.text);
```

### Returns

`Object<GameAPI>`&#x20;

Returns instance of the `GameAPI` class containing several useful functions

### References

* [gameapi.md](../gameapi.md "mention")
