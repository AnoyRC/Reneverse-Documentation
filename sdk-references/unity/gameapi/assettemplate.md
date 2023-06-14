# AssetTemplate()

Fetches the asset template corresponding to the template ID provided.

The function call is asynchronous, the method should be called inside an async function.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
var assetTemplate = await ReneAPI.Game().AssetTemplate("Asset-Template-ID");
```

### Configuration



**Asset Template ID**

Template ID of the Template that needs to be fetched

must be a `string`.



### Returns

`Object<AssetTemplatesResponse.AssetTemplatesData.AssetTemplate>`&#x20;

**Structure**

```csharp
{
    public class Attribute
    {
        public DisplayTypes DisplayType { get; set; }

        public string MaxValue { get; set; }

        public string TraitType { get; set; }

        public List<string> Values { get; set; }
    }

    public class AssetTemplateData
    {
        public string Description { get; set; }

        public double? Price { get; set; }

        public int? Supply { get; set; }
    }

    public class S3File
    {
        public string Extension { get; set; }

        public string FileId { get; set; }

        public bool IsIpfs { get; set; }

        public string Name { get; set; }

        public string UploadUrl { get; set; }

        public string Url { get; set; }
    }

    public class AssetTemplateFiles
    {
        public List<S3File> Images { get; set; }

        public List<S3File> Animations { get; set; }
    }

    public class AssetTemplateMetadataTemplate
    {
        public string BackgroundColor { get; set; }

        public string Description { get; set; }

        public string Name { get; set; }
    }

    public string AssetTemplateId { get; set; }

    public string Name { get; set; }

    public List<Attribute> Attributes { get; set; }

    public AssetTemplateData Data { get; set; }

    public AssetTemplateFiles Files { get; set; }

    public List<S3File> GameEngineFiles { get; set; }

    public bool IsIpfs { get; set; }

    public AssetTemplateMetadataTemplate MetadataTemplates { get; set; }
}
```

### References

* [connect.md](connect.md "mention")
* [isauthorized.md](../api/isauthorized.md "mention")
* [creating-an-asset-template.md](../../../getting-started/creating-an-asset-template.md "mention")
