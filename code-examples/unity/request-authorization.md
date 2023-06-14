# Request Authorization

## Code

```csharp
private IEnumerator ConnectReneService()
{
    var counter = TimeToWait;
    var userConnected = false;
    //Interval how often the code checks that user accepted to log in
    var secondsToDecrement = 1;
    while (counter >= 0 && !userConnected)
    {
        Timer.text = counter.ToString();
        if (ReneAPI.IsAuthorized())
        {

            //Here can be added any extra logic once the user logged in

            yield return GetUserAssetsAsync();


            userConnected = true;
        }

        yield return new WaitForSeconds(secondsToDecrement);
        counter -= secondsToDecrement;
    }
}
```

## References

* [isauthorized.md](../../sdk-references/unity/api/isauthorized.md "mention")
