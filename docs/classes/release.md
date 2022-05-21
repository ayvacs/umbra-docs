# `Release`

`Release` is an abstract class which provides information about the current Umbra version. This information can be checked against Umbra's web API (`https://ave.is-a.dev/umbra/api/launchpad`).

### Values

|Value|Description|
|---|---|
|`Commit`|Returns the current version's Git commit ID|
|`CommitHash`|Returns the current version's Git commit hash|
|`Name`|One of `Umbra`, `Umbra Canary`, `Umbra Nightly`|
|`Url`|Returns `https://ave.is-a.dev/umbra` to specify the Umbra website URL|
|`Version`|Returns the current version's ID code|
|`type1`|Equivalent to `Release.Name .. " v" .. Release.Version`|
|`type2`|Equivalent to `Release.Name .. " v" .. Release.Version .. " [" .. Release.Commit .. "] | " .. Release.Url`|

### Get `Release`

`Release` is stored within a variable.

``` linenums="1"
print( Umbra.Release )
```