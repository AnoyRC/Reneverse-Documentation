# Transfer Asset

## Code

```csharp
public async Task TransferAsset()
{
    try
    {
        if (ReneverseAssetManager.SelectedAsset.NFTId == null || ReneverseUserManager.SelectedUser.UserId == null) return;

        var response = await ReneverseManager.ReneAPI.Game().AssetTransfer(ReneverseAssetManager.SelectedAsset.NFTId, ReneverseUserManager.SelectedUser.UserId);
        Debug.Log(response);

        Debug.Log("Transfer in Progress");
    }
    catch (Exception e)
    {
        Debug.Log(e);
    }
}
```

## References

* [assettransfer.md](../../sdk-references/unity/gameapi/assettransfer.md "mention")
