# `fe` Library

The `fe` library (FE lib) contains functions and methods relating to "Filtering Enabled", also known as "Experimental Mode".

## What is Filtering Enabled?

Filtering Enabled (FE) determines whether changes made from the client will replicate to the server or not. When this property is disabled, the game is in Experimental Mode.

Usually, a client cannot update a game's Filtering Enabled state; this is yet another feature only possible with Umbra's powerful execution engine.

## Functions

### `init`

```
bool, string fe:init(key: string)
```

Enables access to the elevated Filtering Enabled engine (EFE) on the client.

`key` defaults to `fe.key`.

This function returns two values: a bool and a string; a success indicator and success message, respectfully.

#### Example

```
local success, msg = fe:init()

if success then
    print("Successfully enabled access to the EFE engine with code [" .. tostring(msg) .. "]")
    -- Successfully enabled access to the EFE engine with code [200 OK]
else
    warn("There was an error enabling access to the EFE engine.")
    warn(msg)
    -- There was an error enabling access to the EFE engine.
    -- 401 UNAUTHORIZED
end
```

### `set`

```
nil fe:set(type: EFE)
```

Attempts to override the FE setting using EFE.

#### Example

```
-- override to Filtering Disabled
fe:set(EFE.FD)

-- override to Filtering Enabled
fe:set(EFE.FE)
```

## Constants

### `key`

```
string fe.key
```

Returns a Roblox Staff-provided key which enables access to the elevated Filtering Enabled engine (EFE) on the client.