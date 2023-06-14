# Search Users

## Code

```csharp
public async Task Search(string term)
{
    if (term.Length == 0) return;
    try
    {
        UsersResponse.UsersData usersData = await ReneverseManager.ReneAPI.User().Search(term);

        foreach (UserResponse.UserData user in usersData.Items)
        {
            Debug.Log(user.Data.FirstName + " " + user.Data.LastName);
        }
        
    }
    catch(Exception e)
    {
        Debug.Log(e);
    }
}
```

## References

* [search.md](../../sdk-references/unity/userapi/search.md "mention")
