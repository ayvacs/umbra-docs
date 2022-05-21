# Getting started

To write a script, you'll first need an **Umbra developer key.** If you don't have one, you can get it by following these steps:

1. Log into the Umbra developer portal
2. Go to **Home** > **Credentials** > **Create key**
3. Give your new key a name (something like `MyScriptName`)
4. Unlock your key with 2FA
5. Follow the installation steps after you unlock your key
6. In your script, add this line: 

``` linenums="1"
Umbra = require( SCRIPTLOCATION ):Login( KEY )
```

!!! info "Variables"

    Replace `SCRIPTLOCATION` with the location of the script, and `KEY` with your key.

!!! info "Manifest"

    If you've already set your script's `manifest` variable, you can initialize it with this simple function:

    ``` linenums="1"
    Umbra = require(manifest.SCRIPTLOCATION):Login(manifest.KEY)
    ```

!!! bug "Debug Mode"

    If you want to use debug functions, please use this line instead:

    ``` linenums="1"
    Umbra = require(SCRIPT):DRM(KEY, [[ Yes I Know What I Am Doing ]])()
    ```

    Simply use `:DRM()` instead of `:Login()`, and pass `[[ Yes I Know What I Am Doing ]]` as an additional second argument to confirm that, well, you know what you are doing. Additionally, add an empty set of brackets after the `require` function.

You'll have to repeat these steps for each individual script that you create.

Keep in mind that only one script at a time can be initialized with a certain key.

**Congrats!** you just called the Umbra library in your script. Epic gamer move!!!