# `Subscription`

`Subscription` defines the general type of subscription which a user has. You should use it to check whether a user has Premium or not. For specific plan info, use `SubType`.

### Values

|Value|Description|
|---|---|
|`Subscription.None`|The user has no subscription|
|`Subscription.Premium`|The user has a Premium plan|

### Get a user's `Subscription`

```
print( Umbra:Identity(user).Subscription )
```