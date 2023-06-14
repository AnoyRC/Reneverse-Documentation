# AssetTemplates()

Fetches the list of asset templates configured in the Reneverse Portal.

The function call is asynchronous, the method should be called inside an async function.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
var assets = await ReneAPI.Game().AssetTemplates();
```

### Overloads



**limit**

limits the number of asset templates to be fetched

must be an `int`.



**nextToken**

token ID of the next asset template

must be a `string`.



**nextToken, limit**

method overload accepting both the above-mentioned params



**limit, nextToken, assetTemplateId**

method overload accepting the above-mentioned params plus

Asset Template ID of the template to be fetched

must be a `string`.



### Returns

`Object<AssetsResponse.AssetsData>`&#x20;

**Structure**

<pre class="language-csharp"><code class="lang-csharp">{
    public List&#x3C;AssetTemplate> Items { get; set; }

    public string Limit { get; set; }

<strong>    public string NextToken { get; set; }
</strong>}
</code></pre>

Get the reference `Object<AssetTemplate>` from [assettemplate.md](assettemplate.md "mention").

### References

* [assettemplate.md](assettemplate.md "mention")
* [isauthorized.md](../api/isauthorized.md "mention")
* [connect.md](connect.md "mention")
