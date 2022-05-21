# `ai` Library

*wip*

Project 45

## Initializing

### Requiring parent module

``` linenums="1"
ai = require(Umbra:GetService("Project45", true))
```

### Creating a new AI instance

AI instances may be created with the `new()` constructor.

``` linenums="1"
local AI_Instance = ai.new()
```

AI instances must be assigned with the to either player `Instance`s or usernames. AI instances may not be reassigned.

!!! example "Examples (both work)"

    ``` linenums="1"
    AI_Instance:Assign(player: Instance)
    AI_Instance:Assign(username: string)
    ```

## Destroying an AI instance

AI instances may be destroyed with the `Exit()` method. In order for the destruction to succeed, please supply `self.l` as the only argument.

``` linenums="1"
AI_Instance:Destroy( AI_Instance.l )
```

## Exiting

The `ai` library may be exited with the `exit()` method. In order to exit, all existing AI instances must be destroyed.

``` linenums="1"
ai:exit()
```

## Actions

### Begin tracking

AI instances may begin tracking via the `Set()` method.

``` linenums="1"
AI_Instance:Set(endpoint: Enum)

-- example:
AI_Instance:Set( ai:plrFace() )
```

### Data endpoints

All data endpoints:

```
ai:plrCognitiveDesires()
ai:plrCookie()
ai:plrFace()
ai:plrHeartbeat()
ai:plrScare()
```

### Graphing output

``` linenums="1"
local graph = AI_Instance.graph()

-- calling :Run() will begin the graph's functions and
-- automatically turn it on.
graph:Run()

-- hide:
graph:Hide()

-- show:
graph:Show()

-- exit:
graph:Rm()
```

### Personalization

``` linenums="1"
AI_Instance.personalization():_Enable(self)
```