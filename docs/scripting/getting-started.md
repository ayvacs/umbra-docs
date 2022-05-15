# Getting started

To write a script, you'll first need an **Umbra developer key.** If you don't have one, you can get it by following these steps:

1. Log into the Umbra developer portal
2. Go to **Home** > **Credentials** > **Create key**
3. Give your new key a name (something like `MyScriptName`)
4. Unlock your key with 2FA
5. Follow the installation steps after you unlock your key
6. In your script, add this line: 

```
Umbra = require( SCRIPTLOCATION ):Login( KEY )
```

> Replace `SCRIPTLOCATION` with the location of the script, and `KEY` with your key.<br/>
If you set your script up correctly you can easily login like this:<br/>
```
Umbra = require(
    manifest.SCRIPTLOCATION
):Login(
    manifest.KEY
)
```
If you want to use debug functions, please use this line instead:<br/>
```
Umbra = require( SCRIPT ):DRM( KEY , [[ Yes I Know What I Am Doing ]])
```

You'll have to repeat these steps for each individual script that you create.

Keep in mind that only one script at a time can be initialized with a certain key.

**Congrats!** you just called the Umbra library in your script. Epic gamer move!!!