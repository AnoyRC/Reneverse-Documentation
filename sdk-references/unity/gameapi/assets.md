# Assets()

Fetches the list of assets owned by connected user.

The function call is asynchronous, the method should be called inside an async function.

A user must be connected to the game using `Game().Connect()` and authorized with `IsAuthorized()`.

### Usage

```csharp
var assets = await ReneAPI.Game().Assets();
```

### Overloads



**limit**

limits the number of assets to be fetched

must be an `int`.



**nextToken**

token ID of the next asset

must be a `string`.



**nextToken, limit**

method overload accepting both the above-mentioned params



**limit, nextToken, nftId**

method overload accepting the above-mentioned params plus

nftID of the minted asset

must be a `string`.



### Returns

`Object<AssetsResponse.AssetsData>`&#x20;

**Structure**

<pre class="language-csharp"><code class="lang-csharp">{
    public List&#x3C;Asset> Items { get; set; }

    public string Limit { get; set; }

<strong>    public string NextToken { get; set; }
</strong>}
</code></pre>

Get the reference `Object<Asset>` from [asset.md](asset.md "mention").

### References

* [asset.md](asset.md "mention")
* [isauthorized.md](../api/isauthorized.md "mention")
* [connect.md](connect.md "mention")
