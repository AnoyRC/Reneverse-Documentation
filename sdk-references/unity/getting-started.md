# Getting Started

### Importing the package

Before getting started, you'll need to [download and install the Unity Hub and Unity Editor](https://learn.unity.com/tutorial/install-the-unity-hub-and-editor).

Import the Reneverse Unity SDK, by downloading the `.unitypackage` file from [.](./ "mention") Section.

Add the package to your Unity project by clicking `Assets` > `Import Package` > `Custom Package` like so:

![](<../../.gitbook/assets/image (11).png>)

Select the `.unitypackage` file you just downloaded from documentation.

Leave the default files selected, and click `Import`:

![](<../../.gitbook/assets/image (14).png>)

In your `Project` window now, you'll be able to see all of the resources that were imported:

![](<../../.gitbook/assets/image (19).png>)

### Game & SDK Integration

To open the Reneverse Settings inside Unity, navigate to the **Window** menu in the Unity Editor and click on **Reneverse Settings**.

<img src="../../.gitbook/assets/image (13).png" alt="" data-size="original">

**Reneverse Settings Fields**&#x20;

The following fields are available in the Renverse Settings:

* `APIKey` - Your ReneVerse API Key.
* `PrivateKey` - Your ReneVerse Private Key.
* `GameID` - Your ReneVerse Game ID.

![](<../../.gitbook/assets/image (5).png>)

Fill up the fields that you have generated from [integrating-with-sdk.md](../../getting-started/integrating-with-sdk.md "mention") and VOILA!! your game is now connected to Reneverse.

Now you’re ready to use the SDK. Use any of the prefabs, scenes, or scripts that come within the `Demo` folder, or create your own script and instantiate the SDK to get started.

```csharp
using UnityEngine;

//Import the required namespace
using Rene.Sdk;
using ReneVerse;

public class ReneverseManager : MonoBehaviour
{
    //Create an API instance to use throughout this class
    private API ReneAPI;
    
    void Start()
    {
        //When the game starts, set up the Reneverse API
        ReneAPI = ReneAPIManager.API();
    }
}
```
