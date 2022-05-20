# `tab` Library

An extended form of the native `table` library

## Added functions

`tab` contains all of `table`'s functions, plus the following:

### `concat`

```
table tab.concat(t1: table, t2: table)
```

Concatenates **copies of** arrays `t1` and `t2`, and returns the concatenated array.

It is important to note that this function will concatenate copies of the provided arrays, not the arrays themselves. This means that you may easily concatenate read-only arrays.

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

#### Example

```
local t1 = {
    ", World!",
    " everyone!"
    " there!"
}

local t2 = tab.prefixAll(t1, "Hello")

print(t1[1])
-- ", World!"
print(t2[1])
-- " everyone!"

print(t1[2])
-- "Hello, world!"
print(t2[2])
-- "Hello everyone!"
```

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