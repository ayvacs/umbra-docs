# `Identity`

`table Umbra:Identity( user: Player )`

`Identity` is an abstract class which provides reliable information about a given user object's identity. Because exploiters can change a `Player` object's `Name`, `UserId`, and any other property, it's difficult to reliably identify a given user - this class provides a solution to that.

If an exploit is found to bypass this, the `Identity` class will be updated immediately without requiring any change from the script developer or the end user.

## Values

|Value|Description|
|---|---|
|`Identity.DisplayName`|Reliably returns the given user's true `DisplayName`|
|`Identity.Subscription`|Returns the `Subscription` Enum for the given user|
|`Identity.SubType`|Returns the `SubType` Enum for the given user|
|`Identity.UserId`|Reliably returns the given user's true `UserId`|
|`Identity.Username`|Reliably returns the given user's true Username (`Name`)|

## Get a user's `Identity`

```
print( Umbra:Identity(user) )
```