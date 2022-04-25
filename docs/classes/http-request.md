# `HttpRequest`

*wip*

`HttpRequest` is an abstract class used to make requests via the `http` library. It allows users to make use of Roblox's native <a href="https://developer.roblox.com/en-us/api-reference/class/HttpService" target="_blank">HttpService</a> functions within LocalScripts (Umbra scripts), which is normally impossible.

## Values

|Value|Description|
|---|---|
|`Url`|The url to make the request.|
|`RetryC`|The amount of times to re-send the request in case it fails. Defaults to `0` (will not re-try). Limit: `math.huge`|