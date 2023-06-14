# Connect()

Connects the user corresponding to the email address provided and sends an authorization request to the user.

The function call is asynchronous, the method should be called inside an async function.

### Usage

```csharp
bool connected = await ReneAPI.Game().Connect("email-address");
```

### Configuration



**Email Address**

Email address of the user to be connected to the game.

must be a `string`.



### Optional Params



**onGraphQlHttpRequestException**

Custom GraphQL request, by default, is null.

must be of type `Action<GraphQLHttpRequestException>`.



**waitToConnectForSeconds**

maximum time provided to the user to accept the authorization request,  by default, is 60

must be an `int`.



### Returns

`bool`&#x20;

Returns true, if the authorization request sent to the user or else false.

