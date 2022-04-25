# `http` Library

The `http` library provides methods to easily make HTTP requests in your scripts. It allows users to make use of Roblox's native <a href="https://developer.roblox.com/en-us/api-reference/class/HttpService" target="_blank">HttpService</a> functions within LocalScripts (Umbra scripts), which is normally impossible.

## Limitations

These limitations are baked into Roblox's client and server with no way to bypass them.

* There are port restrictions. You cannot use port **1194** or any port **below 1024**, except **80** and **443**. If you try to use a blocked port, you will receive either a **403 Forbidden** or **ERR_ACCESS_DENIED** error.
* For each Roblox game server, there is a limit of **500 HTTP requests per minute**. Exceeding this may cause request-sending functions to stall entirely for about **30 seconds**. Requests made with this library are also subject to this limit.
* Requests cannot be made to any Roblox website, such as **www.roblox.com**. You can bypass this using what is commonly known as a **"Roblox Proxy"**. These functions do not use one.
* Although the **http://** and **file://** protocols are supported, you should use **https://** wherever possible. These are the only supported protocols.
* Attempting to perform a `GET` request targeted at one of the following file types will result in an error:
    * images, i.e. png, jpg, jpeg
    * executables, i.e. exe, app
* Attempting to perform a `PUT` or `PUSH` request without proper credentials will result in either a **403 Forbidden** or **ERR_ACCESS_DENIED** error.
* Be aware of the general capacity and rate-limiting policies of the web servers to which requests are being sent.

### `:ajax( data: HttpRequest )`

Performs an HTTP request with the specified parameters.

Requires an [`HttpRequest`](/classes/http-request) object.

Returns an [`HttpResponse`](/classes/http-response) object.

### `:get( url: string )`

Performs a `GET` request to the specifed `url`.

### `:post( url: string, content: string )`

Performs a `PUSH` request to the specified `url` with the specified `content`.