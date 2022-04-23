# `SubType`

`SubType` defines the specific type of subscription which a user has. For example, you can use it to determine which specific Premium plan a user has. For general plan info, use `Subscription`.

### Values

|Value|Description|
|---|---|
|`SubType.FreeTier`|Free plan|
|`SubType.Premium15`|Legacy premium|
|`SubType.Premium17`|Modern premium|
|`SubType.granted`|The user has been granted Premium, usually due to their administrator status.|

### Get a user's `SubType`

```
print( Umbra:Identity(user).SubType )
```