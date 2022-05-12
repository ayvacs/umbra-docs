# Engine Literals

## Functions

The following functions are baked into Umbra's execution engine, but may be overwritten.

### `hop`

`bool hop()`

Attempts to serverhop. Returns `true` if the serverhop succeeded, and `false` if it didn't.

### `inf`

`table inf()`

Returns a dictionary of information about the script, including its metadata.

### `int`

`number int(n: any)`

Converts `n` to a number. Equivalent to `tonumber()`.

### `key`

`string key()`

Returns the script's `fenv` key (`_gay_furry_porn`) to indicate that it is launched and working as expected. Should be used instead of a string whenever possible.

### `ls`

`table ls()`

Returns a table of loadstrings.

|Key|Value|Desc|
|---|---|---|
|_|`https://ave.is-a.dev/umbra/release`|umbra|

### `str`

`string str(s: any)`

Converts `s` to a string. Equivalent to `tostring()`.

### `typ`

`string typ(n: any)`

Returns the type of `n`. Equivalent to `typeof()`.

### `quit`

`nil quit(force: bool)`

Quits Umbra. Will error and do nothing if the quit button is locked and `force` is `false`. If `force` is `true`, it will force the script to quit, which may sometimes cause errors