# AssetMint()

Initiates a mint request of the asset template corresponding to the asset template ID to the connected user. It may take 4-5 minutes to mint the asset.

The function call is asynchronous, the method should be called inside an async function.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
bool response = await ReneAPI.Game().AssetMint("Asset-Template-ID");
```

### Configuration



**Asset Template ID**

Asset Template ID of the asset template to be minted.

must be a `string`.



### Overloads



**Asset Metadata**

Mint the asset with custom metadata

must be of type `Object<AssetMetadata>`.

**`Structure`**

```csharp
{
    public class AssetAttribute
    {
        public string displayType { get; set; }

        public string traitType { get; set; }

        public string value { get; set; }
    }

    public string name { get; set; }

    public string description { get; set; }

    public string imageFilename { get; set; }

    public string animationFilename { get; set; }

    public List<AssetAttribute> attributes { get; set; }
}
```



**Asset Metadata, is Testnet**

method overload accepting the above-mentioned parameter plus

parameter to decide if the asset is to be minted in Testnet or not

must be a `bool`.



### Returns

`bool`

Returns true, if the mint request is being sent successfully, else false.

### References

* [connect.md](connect.md "mention")
* [isauthorized.md](../api/isauthorized.md "mention")
