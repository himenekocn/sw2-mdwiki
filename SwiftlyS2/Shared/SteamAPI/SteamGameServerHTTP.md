# 📦 SteamGameServerHTTP

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateHTTPRequest (静态)

```csharp
HTTPRequestHandle CreateHTTPRequest(EHTTPMethod eHTTPRequestMethod, string pchAbsoluteURL)
```

<para> Initializes a new HTTP request, returning a handle to use in further operations on it. Requires</para> <para> the method (GET or POST) and the absolute URL for the request. Both http and https are supported,</para> <para> so this string must start with http:// or https:// and should look like http://store.steampowered.com/app/250/</para> <para> or such.</para>

**参数:**

- `eHTTPRequestMethod` (`EHTTPMethod`)
- `pchAbsoluteURL` (`string`)

**返回值:** `HTTPRequestHandle`

### SetHTTPRequestContextValue (静态)

```csharp
bool SetHTTPRequestContextValue(HTTPRequestHandle hRequest, ulong ulContextValue)
```

<para> Set a context value for the request, which will be returned in the HTTPRequestCompleted_t callback after</para> <para> sending the request. This is just so the caller can easily keep track of which callbacks go with which request data.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `ulContextValue` (`ulong`)

**返回值:** `bool`

### SetHTTPRequestNetworkActivityTimeout (静态)

```csharp
bool SetHTTPRequestNetworkActivityTimeout(HTTPRequestHandle hRequest, uint unTimeoutSeconds)
```

<para> Set a timeout in seconds for the HTTP request, must be called prior to sending the request. Default</para> <para> timeout is 60 seconds if you don't call this. Returns false if the handle is invalid, or the request</para> <para> has already been sent.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unTimeoutSeconds` (`uint`)

**返回值:** `bool`

### SetHTTPRequestHeaderValue (静态)

```csharp
bool SetHTTPRequestHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, string pchHeaderValue)
```

<para> Set a request header value for the request, must be called prior to sending the request. Will</para> <para> return false if the handle is invalid or the request is already sent.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pchHeaderValue` (`string`)

**返回值:** `bool`

### SetHTTPRequestGetOrPostParameter (静态)

```csharp
bool SetHTTPRequestGetOrPostParameter(HTTPRequestHandle hRequest, string pchParamName, string pchParamValue)
```

<para> Set a GET or POST parameter value on the request, which is set will depend on the EHTTPMethod specified</para> <para> when creating the request. Must be called prior to sending the request. Will return false if the</para> <para> handle is invalid or the request is already sent.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchParamName` (`string`)
- `pchParamValue` (`string`)

**返回值:** `bool`

### SendHTTPRequest (静态)

```csharp
bool SendHTTPRequest(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

<para> Sends the HTTP request, will return false on a bad handle, otherwise use SteamCallHandle to wait on</para> <para> asynchronous response via callback.</para> <para> Note: If the user is in offline mode in Steam, then this will add a only-if-cached cache-control</para> <para> header and only do a local cache lookup rather than sending any actual remote request.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

### SendHTTPRequestAndStreamResponse (静态)

```csharp
bool SendHTTPRequestAndStreamResponse(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

<para> Sends the HTTP request, will return false on a bad handle, otherwise use SteamCallHandle to wait on</para> <para> asynchronous response via callback for completion, and listen for HTTPRequestHeadersReceived_t and</para> <para> HTTPRequestDataReceived_t callbacks while streaming.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

### DeferHTTPRequest (静态)

```csharp
bool DeferHTTPRequest(HTTPRequestHandle hRequest)
```

<para> Defers a request you have sent, the actual HTTP client code may have many requests queued, and this will move</para> <para> the specified request to the tail of the queue. Returns false on invalid handle, or if the request is not yet sent.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

### PrioritizeHTTPRequest (静态)

```csharp
bool PrioritizeHTTPRequest(HTTPRequestHandle hRequest)
```

<para> Prioritizes a request you have sent, the actual HTTP client code may have many requests queued, and this will move</para> <para> the specified request to the head of the queue. Returns false on invalid handle, or if the request is not yet sent.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

### GetHTTPResponseHeaderSize (静态)

```csharp
bool GetHTTPResponseHeaderSize(HTTPRequestHandle hRequest, string pchHeaderName, out uint unResponseHeaderSize)
```

<para> Checks if a response header is present in a HTTP response given a handle from HTTPRequestCompleted_t, also</para> <para> returns the size of the header value if present so the caller and allocate a correctly sized buffer for</para> <para> GetHTTPResponseHeaderValue.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `unResponseHeaderSize` (`out uint`)

**返回值:** `bool`

### GetHTTPResponseHeaderValue (静态)

```csharp
bool GetHTTPResponseHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, byte[] pHeaderValueBuffer, uint unBufferSize)
```

<para> Gets header values from a HTTP response given a handle from HTTPRequestCompleted_t, will return false if the</para> <para> header is not present or if your buffer is too small to contain it's value. You should first call</para> <para> BGetHTTPResponseHeaderSize to check for the presence of the header and to find out the size buffer needed.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pHeaderValueBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

### GetHTTPResponseBodySize (静态)

```csharp
bool GetHTTPResponseBodySize(HTTPRequestHandle hRequest, out uint unBodySize)
```

<para> Gets the size of the body data from a HTTP response given a handle from HTTPRequestCompleted_t, will return false if the</para> <para> handle is invalid.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unBodySize` (`out uint`)

**返回值:** `bool`

### GetHTTPResponseBodyData (静态)

```csharp
bool GetHTTPResponseBodyData(HTTPRequestHandle hRequest, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para> Gets the body data from a HTTP response given a handle from HTTPRequestCompleted_t, will return false if the</para> <para> handle is invalid or is to a streaming response, or if the provided buffer is not the correct size. Use BGetHTTPResponseBodySize first to find out</para> <para> the correct buffer size to use.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

### GetHTTPStreamingResponseBodyData (静态)

```csharp
bool GetHTTPStreamingResponseBodyData(HTTPRequestHandle hRequest, uint cOffset, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para> Gets the body data from a streaming HTTP response given a handle from HTTPRequestDataReceived_t. Will return false if the</para> <para> handle is invalid or is to a non-streaming response (meaning it wasn't sent with SendHTTPRequestAndStreamResponse), or if the buffer size and offset</para> <para> do not match the size and offset sent in HTTPRequestDataReceived_t.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `cOffset` (`uint`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

### ReleaseHTTPRequest (静态)

```csharp
bool ReleaseHTTPRequest(HTTPRequestHandle hRequest)
```

<para> Releases an HTTP response handle, should always be called to free resources after receiving a HTTPRequestCompleted_t</para> <para> callback and finishing using the response.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

### GetHTTPDownloadProgressPct (静态)

```csharp
bool GetHTTPDownloadProgressPct(HTTPRequestHandle hRequest, out float pflPercentOut)
```

<para> Gets progress on downloading the body for the request. This will be zero unless a response header has already been</para> <para> received which included a content-length field. For responses that contain no content-length it will report</para> <para> zero for the duration of the request as the size is unknown until the connection closes.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pflPercentOut` (`out float`)

**返回值:** `bool`

### SetHTTPRequestRawPostBody (静态)

```csharp
bool SetHTTPRequestRawPostBody(HTTPRequestHandle hRequest, string pchContentType, byte[] pubBody, uint unBodyLen)
```

<para> Sets the body for an HTTP Post request. Will fail and return false on a GET request, and will fail if POST params</para> <para> have already been set for the request. Setting this raw body makes it the only contents for the post, the pchContentType</para> <para> parameter will set the content-type header for the request so the server may know how to interpret the body.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchContentType` (`string`)
- `pubBody` (`byte[]`)
- `unBodyLen` (`uint`)

**返回值:** `bool`

### CreateCookieContainer (静态)

```csharp
HTTPCookieContainerHandle CreateCookieContainer(bool bAllowResponsesToModify)
```

<para> Creates a cookie container handle which you must later free with ReleaseCookieContainer(). If bAllowResponsesToModify=true</para> <para> than any response to your requests using this cookie container may add new cookies which may be transmitted with</para> <para> future requests. If bAllowResponsesToModify=false than only cookies you explicitly set will be sent. This API is just for</para> <para> during process lifetime, after steam restarts no cookies are persisted and you have no way to access the cookie container across</para> <para> repeat executions of your process.</para>

**参数:**

- `bAllowResponsesToModify` (`bool`)

**返回值:** `HTTPCookieContainerHandle`

### ReleaseCookieContainer (静态)

```csharp
bool ReleaseCookieContainer(HTTPCookieContainerHandle hCookieContainer)
```

<para> Release a cookie container you are finished using, freeing it's memory</para>

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

### SetCookie (静态)

```csharp
bool SetCookie(HTTPCookieContainerHandle hCookieContainer, string pchHost, string pchUrl, string pchCookie)
```

<para> Adds a cookie to the specified cookie container that will be used with future requests.</para>

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)
- `pchHost` (`string`)
- `pchUrl` (`string`)
- `pchCookie` (`string`)

**返回值:** `bool`

### SetHTTPRequestCookieContainer (静态)

```csharp
bool SetHTTPRequestCookieContainer(HTTPRequestHandle hRequest, HTTPCookieContainerHandle hCookieContainer)
```

<para> Set the cookie container to use for a HTTP request</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `hCookieContainer` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

### SetHTTPRequestUserAgentInfo (静态)

```csharp
bool SetHTTPRequestUserAgentInfo(HTTPRequestHandle hRequest, string pchUserAgentInfo)
```

<para> Set the extra user agent info for a request, this doesn't clobber the normal user agent, it just adds the extra info on the end</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchUserAgentInfo` (`string`)

**返回值:** `bool`

### SetHTTPRequestRequiresVerifiedCertificate (静态)

```csharp
bool SetHTTPRequestRequiresVerifiedCertificate(HTTPRequestHandle hRequest, bool bRequireVerifiedCertificate)
```

<para> Disable or re-enable verification of SSL/TLS certificates.</para> <para> By default, certificates are checked for all HTTPS requests.</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `bRequireVerifiedCertificate` (`bool`)

**返回值:** `bool`

### SetHTTPRequestAbsoluteTimeoutMS (静态)

```csharp
bool SetHTTPRequestAbsoluteTimeoutMS(HTTPRequestHandle hRequest, uint unMilliseconds)
```

<para> Set an absolute timeout on the HTTP request, this is just a total time timeout different than the network activity timeout</para> <para> which can bump everytime we get more data</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unMilliseconds` (`uint`)

**返回值:** `bool`

### GetHTTPRequestWasTimedOut (静态)

```csharp
bool GetHTTPRequestWasTimedOut(HTTPRequestHandle hRequest, out bool pbWasTimedOut)
```

<para> Check if the reason the request failed was because we timed it out (rather than some harder failure)</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pbWasTimedOut` (`out bool`)

**返回值:** `bool`

