# AssetTransfer()

Initiates a transfer request from the connected user to the user corresponding to the user ID of the asset corresponding to the asset ID. It may take 1-2 minutes to fulfill the request.

The function call is asynchronous, the method should be called inside an async function.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
var response = await ReneAPI.Game().AssetTransfer("Asset-ID", "User-ID");
```

### Configuration



**Asset ID**

Asset ID of the minted asset that needs to be transferred

must be a `string`.



**User ID**

User ID of the user to whom the asset needs to be transferred

must be a `string`.



### Returns

`Object<TransferAssetResponse.AssetTransfer>`

**Structure**

```csharp
{
    public string NftId { get; set; }

    public string RecieverUserId { get; set; }
}
```

### References

* [connect.md](connect.md "mention")
* [isauthorized.md](../api/isauthorized.md "mention")
