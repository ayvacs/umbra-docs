# Getting started

First, you'll need an **Umbra developer key.** If you don't have one, you can get it by following these steps:

1. Log into the Umbra developer portal
2. Go to **Home** > **Credentials** > **Create key**
3. Give your new key a name (something like `MyScriptName`)
4. Unlock your key with 2FA
5. Follow the installation steps after you unlock your key
6. In your script, add this line: `Umbra = require(`*`Location`*`):Login(`*`Token`*`)`
    * You can only use Umbra's functions *after* this line, so it should be near the top.
    * You can name the variable anything you'd like, if you're feeling special.
    * If you want to use debug functions, please use this line instead:<br/>`Umbra = require(`*`Location`*`):DRM(`*`Token`*`, [[ Yes I Know What I Am Doing ]])`

You'll have to repeat these steps for each individual script that you create.

Only one script at a time can be initialized with a certain key and token.