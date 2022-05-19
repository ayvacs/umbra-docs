# `tab` Library

An extended form of the native `table` library

## Added functions

### `concat`

```
table tab.concat(t1: table, t2: table)
```

Concatenates `t1` and `t2`, and returns the new array.

### `copy`

```
table tab.copy(t: table)
```

Returns a [deep copy](https://developer.roblox.com/en-us/articles/Cloning-tables) of `t`.

### `prefixAll`

```
table tab.prefixAll(t: table, pre: string)
```

Prepends `pre` to all values of `t`.

### `random`

```
any tab.random(t: table)
```

Returns a random value from `t`.

With this function, declaring a variable is unnecessary.

### `suffixAll`

```
table tab.suffixAll(t: table, suf: string)
```

Appepends `suf` to all values of `t`.

#### Example

In the following example, the first two lines would produce the same result as the fourth.

```
local t = {1, 4, 8, 9}
local r1 = table.random(t, #t)

local r2 = tab.random({ 1, 4, 8, 9 })
```