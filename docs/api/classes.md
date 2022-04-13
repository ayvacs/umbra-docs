# Classes

## `Identity`

`Identity` is an abstract class which provides reliable information about a given user object's identity. Because exploiters can change a `Player` object's `Name`, `UserId`, and any other property, it's difficult to reliably identify a given user - this class provides a solution to that.

If an exploit is found to bypass this, the `Identity` class will be updated immediately without requiring any change from the script developer or the end user.

### Values

|Value|Description|
|---|---|
|`Identity.Subscription`|Returns the `Subscription` Enum for the given user|
|`Identity.SubType`|Returns the `SubType` Enum for the given user|
|`Identity.UserId`|Reliably returns the given user's true `UserId`|
|`Identity.Username`|Reliably returns the given user's true Username (`Name`)|

### Get a user's `Identity`

```
print( Umbra.Identity(user) )
```

## `Release`

`Release` is an abstract class which provides information about the current Umbra version. This information can be checked against Umbra's web API (`https://ave.is-a.dev/umbra/api/launchpad`).

### Values

|Value|Description|
|---|---|
|`Release.Commit`|Returns the current version's Git commit ID|
|`Release.CommitHash`|Returns the current version's Git commit hash|
|`Release.Name`|One of `Umbra`, `Umbra Canary`, `Umbra Nightly`|
|`Release.Url`|Returns `https://ave.is-a.dev/umbra` to specify the Umbra website URL|
|`Release.Version`|Returns the current version's ID code|
|`Release.type1`|Equivalent to `Release.Name .. " v" .. Release.Version .. " | " .. Release.Url`|
|`Release.type2`|Equivalent to `Release.Name .. " v" .. Release.Version .. " [" .. Release.Commit .. "] | " .. Release.Url`|

### Get `Release`

`Release` is grabbed using a variable instead of with a function.

```
print( Umbra.Release )
```

## `Subscription`

`Subscription` defines the general type of subscription which a user has. You should use it to check whether a user has Premium or not. For specific plan info, use `SubType`.

### Values

|Value|Description|
|---|---|
|`Subscription.None`|The user has no subscription|
|`Subscription.Premium`|The user has a Premium plan|

### Get a user's `Subscription`

```
print( Umbra.identity(user).Subscription )
```

## `SubType`

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
print( Umbra.identity(user).SubType )
```

## [Deprecated] `Codesign`

> :bootstrap-exclamation-circle:
**Deprecated**<br>
This class is no longer supported and should not be used for new work.

`Codesign` provides information about the engine.

### Values

|ValueName|ValueClass|Description|
|---|---|---|
|`PLR Scriptinjector`|`ArcHandles`||
|`plr bkpk`|`ArcHandles`||
|`plr gui`|`ArcHandles`||
|`en_CA`|`Flag`||
|`en_US`|`Flag`||
|`en_GB`|`Flag`||
|`RepCODESIGN5A`|`Flag`||
|`fe`|`LocalScript`||
|`fe-ena`|`LocalScript`||
|`Repeventhandler`|`LocalScript`||
|`Repeventvictim`|`LocalScript`||
|`ver`|`StringValue`|x|
|`id_6`|`StringValue`|Eqivalent to `Umbra.id`|