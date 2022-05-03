# Project 45

## Initializing

### Requiring parent module

```
-- Assuming that the `ModuleScript` is named `45` and is located in `ReplicatedStorage`:
local P45 = require(game:GetService("ReplicatedStorage")["45"])
```

### Creating a new AI instance


`local AI = P45.new():assign(`*`PlayerInstance`*`)`

### Destroying an AI instance

```
P45:exit(AI)
AI.l = false
AI:Destroy(true,AI.l)
```

## Actions

### Data endpoints

All data endpoints:

```
AI.data = P45:plrCognitiveDesires()
AI.data = P45:plrCookie()
AI.data = P45:plrFace()
AI.data = P45:plrHeartbeat()
AI.data = P45:plrScare()
```

### Graphing output

```
local graph = AI.graph(true)

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

```
AI.personalization():_Enable(self)
```