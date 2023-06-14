# User()

Initializes `UserAPI` or returns `UserAPI` if initialized already, for the game which contains functions required to fetch Profile and Search for other users connected to the game.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
UserAPI userAPI = ReneAPI.User();
```

or

use the functions provided by `User()` directly.

```csharp
var myProfile = await ReneAPI.User().Profile();
```

### Returns

`Object<UserAPI>`&#x20;

Returns instance of the `UserAPI` class containing several useful functions

### References

* [userapi](../userapi/ "mention")
* [isauthorized.md](isauthorized.md "mention")
* [connect.md](../gameapi/connect.md "mention")
