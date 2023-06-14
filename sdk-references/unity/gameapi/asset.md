# Asset()

Fetches the asset details corresponding to the asset ID provided.

The function call is asynchronous, the method should be called inside an async function.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
var asset = await ReneAPI.Game().Asset("Asset-ID");
```

### Configuration



**Asset ID**

Asset ID of the minted asset that needs to be fetched

must be a `string`.



### Returns

`Object<AssetsResponse.AssetsData.Asset>`&#x20;

**Structure**

```csharp
{
    public class AssetMetadata
    {
        public class AssetAttribute
        {
            public DisplayTypes DisplayType { get; set; }
    
            public string TraitType { get; set; }
    
            public string Value { get; set; }
    
            public string MaxValue { get; set; }
        }
    
        public string Name { get; set; }
    
        public string Description { get; set; }
    
        public string Image { get; set; }
    
        public string AnimationUrl { get; set; }
    
        public List<AssetAttribute> Attributes { get; set; }
    }
    
    public string AssetTemplateId { get; set; }
    
    public string CId { get; set; }
    
    public string GameId { get; set; }
    
    public string NftId { get; set; }
    
    public string WalletAddress { get; set; }
    
    public AssetMetadata Metadata { get; set; }
}
```

### References

* [connect.md](connect.md "mention")
* [isauthorized.md](../api/isauthorized.md "mention")
* [minting-assets.md](../../../getting-started/minting-assets.md "mention")
