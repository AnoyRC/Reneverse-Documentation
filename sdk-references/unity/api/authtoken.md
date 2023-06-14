# AuthToken

Returns the Authorization Token of the current session after the user has connected to the game using `Game().Connect()` and authorized with `isAuthorized()`.

### Usage

```csharp
string authToken = ReneAPI.AuthToken;
```

### Returns

`string` containing the Authorization Token of the current session.

### References

* [isauthorized.md](isauthorized.md "mention")
* [connect.md](../gameapi/connect.md "mention")
