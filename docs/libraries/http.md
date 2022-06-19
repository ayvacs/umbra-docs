# `http` Library

The `http` library provides methods to easily make HTTP requests in your scripts. It allows users to make use of Roblox's native <a href="https://developer.roblox.com/en-us/api-reference/class/HttpService" target="_blank">HttpService</a> functions within LocalScripts (Umbra scripts), which is normally impossible.

The source code of this library is available [on GitHub](https://github.com/ayvacs/umbra/blob/main/src/http).

## Limitations

These limitations are baked into Roblox's engine with no way to bypass them, unless the request is made with an `X-FE` key - we are currently working on adding `X-FE` support.

* There are port restrictions. You cannot use port **1194** or any port **below 1024**, except **80** and **443**. If you try to use a blocked port, you will receive either a **403 Forbidden** or **ERR_ACCESS_DENIED** error.
* For each Roblox game server, there is a limit of **500 HTTP requests per minute**. Exceeding this may cause request-sending functions to stall entirely for about **30 seconds**. While requests made using the `http` library are not subject to this limit, they will count towards the limit for other scripts in-game, so please pay attention to that.
* Requests cannot be made to any Roblox website, such as **www.roblox.com**. You can bypass this using what is commonly known as a **"Roblox Proxy"**. These functions do not use one.
* Although the **http://** and **file://** protocols are supported, you should use **https://** wherever possible. These are the only supported protocols.
* Attempting to perform a `GET` request targeted at one of the following file types will result in an error:
    * images, i.e. `png`, `jpg`, `jpeg`
    * executables, i.e. `exe`, `app`
    * archive files, i.e. `zip`, `rar`, `7z`
* Attempting to perform a `PUT` or `PUSH` request without proper credentials will result in either a **403 Forbidden** or **ERR_ACCESS_DENIED** error.
* Be aware of the general capacity and rate-limiting policies of the web servers to which requests are being sent.

## Functions

### `ajax`

```
HttpResponse http.ajax( data: HttpRequest )
```

Performs an HTTP request with the specified parameters.

### `get`

```
string http.get( url: string )
```

Performs a `GET` request to the specifed `url`.

### `post`

```
nil http.post( url: string, content: string )
```

Performs a `PUSH` request to the specified `url` with the specified `content`.