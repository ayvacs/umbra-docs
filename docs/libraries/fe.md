# `fe` Library

The `fe` library (FE lib) contains functions and methods relating to "Filtering Enabled", also known as "Experimental Mode".

## What is Filtering Enabled?

Filtering Enabled (FE) determines whether changes made from the client will replicate to the server or not. When this property is disabled, the game is in Experimental Mode.

Usually, a client cannot update a game's Filtering Enabled state; this is yet another feature only possible with Umbra's powerful execution engine.

## Functions

### `init`

```
bool fe:init(key: string)
```

Enables access to the elevated Filtering Enabled engine (EFE) on the client. Returns a boolean, depending on whether the initialization succeeded.

If `key` is not provided, the EFE will attempt to use `fe.key` instead. Therefore, you can simply call `fe:init()` to enable access.

### `set`

```
nil fe:set(type: bool)
```

Attempts to override the FE setting using EFE.

`type` must be a boolean: `true` if you wish to enable FE, and `false` if you wish to disable it.

## Constants

### `key`

```
string fe.key
```

Returns a Roblox Staff-provided key which enables access to the elevated Filtering Enabled engine (EFE) on the client.