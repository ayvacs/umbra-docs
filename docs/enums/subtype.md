# `SubType`

`SubType` defines the specific type of license which a user has. For example, you can use it to determine which specific Premium plan a user has. For general plan info, use the `Subscription` enum.

### Values

|Value|Description|
|---|---|
|`SubType.FreeTier`|Free plan|
|`SubType.Premium15`|Legacy premium|
|`SubType.Premium17`|Modern premium|
|`SubType.granted`|The user has been granted Premium, usually due to their administrator status.|

### Get a user's `SubType`

### within a script

`print( Umbra:Identity(`*`playerObject`*`).SubType )`

### with the web API

> :bootstrap-exclamation-circle:
**Beta Feature**<br>
This feature is currently only available to users in a closed beta. We plan to make it available for everyone as soon as possible!

`https://ave.is-a.dev/umbra/api/SubType/`*`username`*

Alternatively, you can use the `http` library in a script:

> :bootstrap-exclamation-circle:
**Required Libraries**<br>
This feature requires the `http` library.

`print( http.get("https://ave.is-a.dev/umbra/api/SubType/`*`username`*`") )`