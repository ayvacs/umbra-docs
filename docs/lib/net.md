# `net` Library

Umbra's development team has found a workaround for net ownership, allowing script users to utilise an elevated version of it to remove (kick) players from games. These functions are contained within the `net` library.

## Functions

### `transfer`

`nil net:transfer(obj: Instance)`

`nil net:transfer(objs: table)`

Attempts to transfer ownership of the provided instance(s) to the client.

Takes one argument: either an `Instance` or an array of `Instance`s.

## Constants

### `key`

`string net.key`

Returns a network key.