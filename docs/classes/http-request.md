# `HttpRequest`

`HttpRequest` is an abstract class used to make requests via the `http` library. It allows users to make use of Roblox's native <a href="https://developer.roblox.com/en-us/api-reference/class/HttpService" target="_blank">HttpService</a> functions within LocalScripts (Umbra scripts), which is normally impossible.

## Values

|Value|Type|Syntax|Description|
|---|---|---|---|
|`Body`|string| |The HTTP request body.|
|`Cookies`|table|`{[string]: string}`|A dictionary of cookies to be used with this request.|
|`Headers`|table|`{[string]: string}`|A dictionary of headers to be used with this request.|
|`Method`|string|`"GET"|"POST"|"PATCH"|"PUT"`|The HTTP method that will be used by this request.|
|`Url`|string| |The URL which this request will be made out to.|