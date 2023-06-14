# Get User Assets

## Code

```csharp
private async Task GetUserAssetsAsync()
{
    AssetsResponse.AssetsData userAssets = await ReneAPI.Game().Assets();
    //By this way you could check in the Unity console your NFT assets
    userAssets?.Items.ForEach(asset => Debug.Log
        ($" - Asset Id '{asset.NftId}' Name '{asset.Metadata.Name}"));

    userAssets?.Items.ForEach(asset =>
    {
        string assetName = asset.Metadata.Name;
        string assetImageUrl = asset.Metadata.Image;
        string assetStyle = "";
        asset.Metadata?.Attributes?.ForEach(attribute =>
        {
        //Keep in mind that this TraitType should be preset in your Reneverse Account
            if (attribute.TraitType == "Style")
            {
                assetStyle = attribute.Value;
            }
        });
        //An example of how you could keep retrieved information
        Asset assetObj = new Asset(assetName, assetImageUrl, assetStyle);
        //one of many ways to add it to the game logic
        //_assetManager can be of list datatype 
        _assetManager.userAssets.Add(assetObj);
    });
}
```

## References

* [assets.md](../../sdk-references/unity/gameapi/assets.md "mention")
