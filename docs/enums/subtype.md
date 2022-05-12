# `SubType`

`SubType` defines the specific type of license which a user has. For example, you can use it to determine which specific Premium plan a user has. For general plan info, use the `Subscription` enum.

### Values

|Value|Description|
|---|---|
|`FreeTier`|Free plan|
|`granted`|The user has been granted Premium, usually due to their administrator status.|
|`Premium15`|Legacy premium|
|`Premium17`|Modern premium|

### Get a user's `SubType`

### within a script

```
print( Umbra:Identity(plr: Instance).SubType )
```

### with the web API

> :bootstrap-exclamation-circle:
**Beta Feature**<br>
This feature is currently only available to certain users.

```
https://ave.is-a.dev/umbra/api/v4/username/subtype
```

#### Example request

``` title="Request URL"
https://ave.is-a.dev/umbra/api/v4/frogweezer/subtype
```

``` title="Response"
Premium15
```