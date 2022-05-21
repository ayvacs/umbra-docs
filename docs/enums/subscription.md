# `Subscription`

`Subscription` defines the general license type which a user has. You should use it to check whether a user has Premium or not. For specific plan info, use the `SubType` enum.

### Values

|Value|Description|
|---|---|
|`None`|The user does not have Premium|
|`Premium`|The user is a Premium user|

### Get a user's `Subscription`

### within a script

```
print( Umbra:Identity(plr: Instance).Subscription )
```

!!! example

    ``` title="Script" linenums="1"
    local id = Umbra:Identity(game:GetService("Players").LocalPlayer)
    print(id.Subscription)
    ```

    ``` title="Potential Output" linenums="1"
    Enum.Subscription.Premium
    ```

### with the web API

!!! warning "Beta Feature"

    This feature is currently only available to certain users.

```
https://ave.is-a.dev/umbra/api/v4/{username}/subscription
```

!!! example

    ``` title="Request URL"
    https://ave.is-a.dev/umbra/api/v4/frogweezer/subscription
    ```

    ``` title="Response"
    Premium
    ```