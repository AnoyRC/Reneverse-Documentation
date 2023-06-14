# Connect to Reneverse

## Code

```csharp
using UnityEngine;

//Import the required namespace
using Rene.Sdk;
using ReneVerse;

public class ReneverseManager : MonoBehaviour
{
    //Create an API instance to use throughout this class
    private API ReneAPI;
    //Text Mesh Pro - Input Field for Email
    public GameObject Email;
    
    void Start()
    {
        //When the game starts, set up the Reneverse API
        ReneAPI = ReneAPIManager.API();
    }
    
    //Connect User function
    async Task ConnectUser()
    {
        
        string EmailHandler = Email.GetComponent<TMP_InputField>().text;

        if (!EmailHandler.IsEmail())
        {
            Debug.Log("Please provide a valid Email");
            return;
        }

        bool connected = await ReneAPI.Game().Connect(EmailHandler);
        Debug.Log(connected);

        if (!connected)
        {
            Debug.Log("Error Connecting");
            SignInButton.SetActive(true);
            return;
        }

        StartCoroutine(ConnectReneService());
    }
}
```

## References

* [connect.md](../../sdk-references/unity/gameapi/connect.md "mention")
