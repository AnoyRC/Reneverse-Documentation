# Search()

Get the list of Users connected to the game corresponding to the search term provided as a parameter using `Search()` method provided with [.](./ "mention").

### Usage

```csharp
var usersData = await ReneAPI.User().Search("search-term");
```

### Configuration



**Search Term**

The term which needs to be search.

must be a `string`.



### Returns

`Object<UsersResponse.UsersData>`&#x20;

**Structure**

```csharp
{
    public List<UserResponse.UserData> Items { get; set; }

    public int? Limit { get; set; }

    public string NextToken { get; set; }
}
```

Get the reference `Object<UserResponse.UserData>` from [profile.md](profile.md "mention").

### References

* [profile.md](profile.md "mention")

