# `tab` Library

An extended form of the native `table` library.

The source code of this library is available [on GitHub](https://github.com/ayvacs/umbra/blob/main/src/tab).

## Added functions

`tab` contains all of `table`'s functions, plus the following:

### `concat`

??? warning "Copies Argument(s)"

    The following function will execute on **a copy of** the provided table(s), **NOT THE ACTUAL TABLE(S) THEMSEL(VES)**.

    This is important to note because when assigning a table to two (or more) different variables, all of the copied tables will update with the other(s). 

    For example, the function `tab.prefixAll(t, pre)` function will prepend `pre` to all values of **a copy of** `t`, meaning that in order for the actual `t` variable to change, you must call `t = tab.prefixAll(t, pre)`, and that simply `tab.prefixAll(t, pre)` would not work.

    Furthermore, calling the following code would print `false`:

    ``` linenums="1"
    local t1 = {1, 2, 3}
    tab.prefixAll(t1, 1)

    print( t1 == {11, 12, 13} )
    ```

```
table tab.concat(t1: table, t2: table)
```

Concatenates **copies of** arrays `t1` and `t2` together in the same manner of strings, numbers, or any other concatenable value. Returns the concatenated array.

### `contains`

```
bool tab.contains(t: table, c: any)
```

Determines whether or not table `t` contains the value `c`.

### `copy`

```
table tab.copy(t: table)
```

Returns a [deep copy](https://developer.roblox.com/en-us/articles/Cloning-tables) of `t`.

### `keys`

```
table tab.keys(t: table)
```

Returns an array of table `t`'s own enumerable property **keys**, iterated in the same order as that provided by a `for...in` loop.

!!! example

    ``` linenums="1"
    local myInventory = { sword = 1, shield = 1 apple = 16, rupee = 1504 }
    local inventoryItems = tab.keys(myInventory)

    print(inventoryItems)
    -- expected result: { sword, shield, apple, rupee }
    ```

### `prefixAll`

??? warning "Copies Argument(s)"

    The following function will execute on **a copy of** the provided table(s), **NOT THE ACTUAL TABLE(S) THEMSEL(VES)**.

    This is important to note because when assigning a table to two (or more) different variables, all of the copied tables will update with the other(s). 

    For example, the function `tab.prefixAll(t, pre)` function will prepend `pre` to all values of **a copy of** `t`, meaning that in order for the actual `t` variable to change, you must call `t = tab.prefixAll(t, pre)`, and that simply `tab.prefixAll(t, pre)` would not work.

    Furthermore, calling the following code would print `false`:

    ``` linenums="1"
    local t1 = {1, 2, 3}
    tab.prefixAll(t1, 1)

    print( t1 == {11, 12, 13} )
    ```

```
table tab.prefixAll(t: table, pre: string)
```

Prepends `pre` to all values of **a copy of** `t`.

!!! example

    ```linenums="1"
    local t1 = {
        ", World!",
        " everyone!"
        " there!"
    }

    local t2 = tab.prefixAll(t1, "Hello")

    print(t1[1])
    -- ", World!"
    print(t2[1])
    -- "Hello, World!"

    print(t1[2])
    -- " everyone!"
    print(t2[2])
    -- "Hello everyone!"
    ```

### `random`

```
any tab.random(t: table)
```

Returns a random value from table `t`.

!!! example

    In the following example, the first two lines would produce the same result as the fourth.

    ``` linenums="1"
    local t = {1, 4, 8, 9}
    local r1 = table.random(t, #t)

    local r2 = tab.random({ 1, 4, 8, 9 })
    ```

### `suffixAll`

??? warning "Copies Argument(s)"

    The following function will execute on **a copy of** the provided table(s), **NOT THE ACTUAL TABLE(S) THEMSEL(VES)**.

    This is important to note because when assigning a table to two (or more) different variables, all of the copied tables will update with the other(s). 

    For example, the function `tab.prefixAll(t, pre)` function will prepend `pre` to all values of **a copy of** `t`, meaning that in order for the actual `t` variable to change, you must call `t = tab.prefixAll(t, pre)`, and that simply `tab.prefixAll(t, pre)` would not work.

    Furthermore, calling the following code would print `false`:

    ``` linenums="1"
    local t1 = {1, 2, 3}
    tab.prefixAll(t1, 1)

    print( t1 == {11, 12, 13} )
    ```

```
table tab.suffixAll(t: table, suf: string)
```

Appepends `suf` to all values of **a copy of** `t`.

### `sum`

```
number tab.sum(t: table)
```

Returns the sum of all of `t`'s **number** values.

If `t` contains any non-number values, this function simply skips them.

### `tostring`

```
string tab.tostring(t: table)
```

Returns a string version of `t`. This function should not be used within tables, rather for exporting table data into string form. 

### `values`

```
table tab.values(t: table)
```

Returns an array of table `t`'s own enumerable property **values**, iterated in the same order as that provided by a `for...in` loop.

!!! example

    ``` linenums="1"
    local myDataStore = {
        ["Telamon"] = {
            XP = 250
        },
        ["ROBLOX"] = {
            XP = 15204
        },
        ["frogweezer"] = {
            XP = 31281
            ...
        }
    }
    local allValues = tab.values(myDataStore)
    local allStats = tab.values(allValues)
    local allXP = tab.sum(allStats)

    print("Players have collected a total of " .. allXP .. " XP in this game!")
    ```