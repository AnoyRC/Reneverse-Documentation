# UserAPI

After you have initialized the `UserAPI` from [.](./ "mention") or if you are using it directly, it exposes functions required to fetch Profile and Search for other users connected to the game.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
var myProfile = await ReneAPI.User().Profile();
```

### Contents

* [profile.md](profile.md "mention")
* [search.md](search.md "mention")

### References

* [isauthorized.md](../api/isauthorized.md "mention")
* [connect.md](../gameapi/connect.md "mention")

