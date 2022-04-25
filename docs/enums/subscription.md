# `Subscription`

`Subscription` defines the general license type which a user has. You should use it to check whether a user has Premium or not. For specific plan info, use the `SubType` enum.

### Values

|Value|Description|
|---|---|
|`Subscription.None`|The user does not have Premium|
|`Subscription.Premium`|The user is a Premium user|

### Get a user's `Subscription`

### within a script

`print( Umbra:Identity(`*`playerObject`*`).Subscription )`

### with the web API

> :bootstrap-exclamation-circle:
**Beta Feature**<br>
This feature is currently only available to users in a closed beta. We plan to make it available for everyone as soon as possible!

`https://ave.is-a.dev/umbra/api/Subscription/`*`username`*

Alternatively, you can use the `http` library in a script:

> :bootstrap-exclamation-circle:
**Required Libraries**<br>
This feature requires the `http` library.

`print( http.get("https://ave.is-a.dev/umbra/api/Subscription/`*`username`*`") )`