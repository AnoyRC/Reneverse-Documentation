# Mint Assets

## Code

```csharp
public async Task Mint(string templateID)
{
    try
    {
        var response = await ReneverseManager.ReneAPI.Game().AssetMint(templateID);
        Debug.Log(response);

        Debug.Log("Asset Minting in progress");
    }
    catch (Exception e)
    {
        Debug.Log(e);
    }
}
```

## References

* [assetmint.md](../../sdk-references/unity/gameapi/assetmint.md "mention")
