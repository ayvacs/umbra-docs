# `net` Library

Umbra's development team has found a workaround for net ownership, allowing script users to utilise an elevated version of it to remove (kick) players from games. These functions are contained within the `net` library.

## Functions

### `mtransf`

```
nil net:mtransf(objs: table)
```

Attempts to transfer ownership of the provided array of instances to the client.

`obj` may be one array of `Instance` types.

### `transf`

```
nil net:transf(obj: Instance)
```

Attempts to transfer ownership of the provided single instance to the client.

`obj` may be one argument of `Instance` type.

## Constants

### `key`

```
string net.key
```

Returns a network key.