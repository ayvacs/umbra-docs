# Engine Literals

## Functions

The following functions are baked into Umbra's execution engine, but may be overwritten.

### `hop`

```
bool hop()
```

Attempts to serverhop. Returns `true` if the serverhop succeeded, and `false` if it didn't.

### `int`

```
number int(n: any)
```

Converts `n` to a number. Equivalent to `tonumber()`.

### `key`

```
string key()
```

Returns the script's `fenv` key (`_gay_furry_porn`) to indicate that it is launched and working as expected. Should be used instead of a string whenever possible.

```
table ls()
```

Returns a table of loadstrings.

|Key|Value|Desc|
|---|---|---|
|_|`https://ave.is-a.dev/umbra/release`|umbra|

### `str`

```
string str(s: any)
```

Converts `s` to a string. Equivalent to `tostring()`.

### `typ`

```
string typ(n: any)
```

Returns the type of `n`. Equivalent to `typeof()`.

### `quit`

```
nil quit(force: bool, cool: bool)
```

Attempts to exit the script. Will error and do nothing if the quit button is locked and `force` is `false`. If `force` is `true`, it will force the script to quit, which may sometimes cause errors.

If `cool` is `false`, it will exit the scipt and shut down its modules immediately. Otherwise, it'll shut down with... style.

### [Deprecated] `ls`

???+ fail "Deprecated"

    This function is no longer supported and should not be used for new work.