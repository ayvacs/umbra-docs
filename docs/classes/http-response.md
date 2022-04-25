# `HttpResponse`

`HttpResponse` is an abstract class which provides information about requests made using the `http` library, including the reponse body and headers. It allows users to make use of Roblox's native <a href="https://developer.roblox.com/en-us/api-reference/class/HttpService" target="_blank">HttpService</a> functions within LocalScripts (Umbra scripts), which is normally impossible.

## Values

|Value|Description|
|---|---|
|`HttpResponse.Body`|The raw body content recieved in the response|
|`HttpResponse.Headers`|A dictionary of headers recieved in the response|
|`HttpResponse.StatusCode`|The status/error code recieved in the response|
|`HttpResponse.StatusMessage`|The status/error message recieved in the response|
|`HttpResponse.Succeeded`|A boolean that indicates whether or not the `HttpRequest` was successful|