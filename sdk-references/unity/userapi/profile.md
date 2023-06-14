# Profile()

Returns the profile of the user connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`. The function call is asynchronous, the method should be called inside an async function.

### Usage

```csharp
var myProfile = await ReneAPI.User().Profile();
```

### Returns

`Object<UserResponse.UserData>`&#x20;

**Structure**

```csharp
{
    public class UserDetailsData
    {
        public string FirstName { get; set; }

        public string LastName { get; set; }
    }

    public class UserStats
    {
        public string Assets { get; set; }

        public string Games { get; set; }

        public string Value { get; set; }
    }

    public class UserVerified
    {
        public bool IsEmail { get; set; }
    }

    public enum UserRoles
    {
        GAMER,
        GAMER_DEV
    }

    public class S3File
    {
        public string Extension { get; set; }

        public string FileId { get; set; }

        public string Name { get; set; }

        public string Url { get; set; }

        public string UploadUrl { get; set; }

        public bool IsIpfs { get; set; }
    }

    public class UserExternalAccounts
    {
        public string DiscordId { get; set; }

        public string SteamId { get; set; }

        public string TwitterId { get; set; }
    }

    public enum Scope
    {
        jwt_get_token,
        jwt_refresh_token,
        org_all,
        user_all,
        user_verify_email
    }

    public string UserId { get; set; }

    public string Email { get; set; }

    public string OrgId { get; set; }

    public bool IsActive { get; set; }

    public string WalletAddress { get; set; }

    public UserDetailsData Data { get; set; }

    public UserStats Stats { get; set; }

    public UserVerified Verified { get; set; }

    public List<Scope> Scopes { get; set; }

    public UserRoles Role { get; set; }

    public S3File Image { get; set; }

    public UserExternalAccounts ExternalAccounts { get; set; }
}
```

