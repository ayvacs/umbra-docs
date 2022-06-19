# `HttpResponse`

`HttpResponse` is an abstract class which provides information about requests made using the `http` library, including the reponse body and headers. It allows users to make use of Roblox's native <a href="https://developer.roblox.com/en-us/api-reference/class/HttpService" target="_blank">HttpService</a> functions within LocalScripts (Umbra scripts), which is normally impossible.

## Values

|Value|Type|Description|
|---|---|--|
|`Body`|string|The raw body content recieved.|
|`Headers`|table|A dictionary of headers recieved.|
|`StatusCode`|number|The status/error code recieved.|
|`StatusMessage`|string|The status/error message recieved.|
|`Success`|bool|A boolean that indicates whether or not the `HttpRequest` was successful.|