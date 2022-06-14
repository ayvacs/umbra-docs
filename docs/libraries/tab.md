# `tab` Library

An extended form of the native `table` library

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

Concatenates **copies of** arrays `t1` and `t2`, and returns the concatenated array.

### `contains`

```
bool tab.contains(t: table, c: any)
```

Returns whether or not table `t` contains the value `c`.

### `copy`

```
table tab.copy(t: table)
```

Returns a [deep copy](https://developer.roblox.com/en-us/articles/Cloning-tables) of `t`.

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

Prepends `pre` to all values of **a copy of ** `t`.

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

Returns a random value from `t`.

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

Appepends `suf` to all values of **a copy of ** `t`.

### `tostring`

```
string tab.tostring(t: table)
```

Returns a string version of `t`. Useful for printing logs to files