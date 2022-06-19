# `net` Library

Umbra's development team has found a workaround for net ownership, allowing script users to utilise an elevated version of it to transfer ownership of any object. These functions are contained within the `net` library.

## Functions

### `mtransf`

```
nil net:mtransf(objs: table, newown: string, key: string)
nil objs:mtransf(newown: string)
```

Attempts to transfer ownership of the provided array of instances to `newown`.

`objs` may be one array of `Instance` types.

`newown` may be one argument of `string` type.

`key` may be one argument of `string` type. It is not required and, if not set, will default to `net.key`.

`newown` should be, in string form, the `UserId` (or `SystemName`) to which you wish to transfer each value in `objs`. For example, if you wished to transfer the Workspace's children to the LocalPlayer, you could run the following code:

```
local objects = workspace:GetChildren()
local newOwnerId = game:GetService("Players").LocalPlayer.UserId

net:mtransf(objects, tostring(newOwnerId))
```

### `transf`

```
nil net:transf(obj: Instance, newown: string, key: string)
nil obj:transf(newown: string)
```

Attempts to transfer ownership of the provided single instance to `newown`.

`obj` may be one argument of `Instance` type.

`newown` may be one argument of `string` type.

`key` may be one argument of `string` type. It is not required and, if not set, will default to `net.key`.

`newown` should be, in string form, the `UserId` (or `SystemName`) to which you wish to transfer `obj`. For example, if you wished to transfer the Workspace to the LocalPlayer, you could run the following code:

```
local object = workspace
local newOwnerId = game:GetService("Players").LocalPlayer.UserId

net:transf(object, tostring(newOwnerId))
```

### `whois`

```
string net:whois(obj: Instance)
string obj:whois()
```

Returns the `UserId` or `SystemName` of `obj`'s network owner **in string form**.

## Constants

### `key`

```
string net.key
```

Returns the default network key.