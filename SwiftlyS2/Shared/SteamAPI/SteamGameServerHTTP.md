# 📦 SteamGameServerHTTP

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateHTTPRequest (静态)

```csharp
HTTPRequestHandle CreateHTTPRequest(EHTTPMethod eHTTPRequestMethod, string pchAbsoluteURL)
```

<para>初始化一个新的 HTTP 请求，并返回一个句柄以用于后续操作。需要指定请求的方法（GET 或 POST）以及请求的绝对 URL。HTTP 和 HTTPS 均受支持，因此该字符串必须以 http:// 或 https:// 开头，并应类似于 http://store.steampowered.com/app/250/ 或类似格式。</para>

**参数:**

- `eHTTPRequestMethod` (`EHTTPMethod`)
- `pchAbsoluteURL` (`string`)

**返回值:** `HTTPRequestHandle`

**用法示例:**
```csharp
SteamGameServerHTTP.CreateHTTPRequest(EHTTPMethod.k_EHTTPMethodGET, "https://store.steampowered.com/app/250/");
```

### SetHTTPRequestContextValue (静态)

```csharp
bool SetHTTPRequestContextValue(HTTPRequestHandle hRequest, ulong ulContextValue)
```

为请求设置一个上下文值，该值将在发送请求后的 HTTPRequestCompleted_t 回调中返回。这样做的目的是让调用方可以轻松地追踪哪个回调对应于哪份请求数据。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `ulContextValue` (`ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
ulong contextId = 12345;
SteamGameServerHTTP.SetHTTPRequestContextValue(myRequestHandle, contextId);
```

### SetHTTPRequestNetworkActivityTimeout (静态)

```csharp
bool SetHTTPRequestNetworkActivityTimeout(HTTPRequestHandle hRequest, uint unTimeoutSeconds)
```

<para> 为 HTTP 请求设置以秒为单位的超时时间，必须在发送请求之前调用。如果不调用此方法，默认超时时间为 60 秒。如果句柄无效或请求已发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unTimeoutSeconds` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestNetworkActivityTimeout(requestHandle, 30);
```

### SetHTTPRequestHeaderValue (静态)

```csharp
bool SetHTTPRequestHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, string pchHeaderValue)
```

<para>为请求设置请求头值，必须在发送请求之前调用。如果句柄无效或请求已发送，将返回 false。</para> <para></para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pchHeaderValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.SetHTTPRequestHeaderValue(requestHandle, "Authorization", "Bearer token123");
```

### SetHTTPRequestGetOrPostParameter (静态)

```csharp
bool SetHTTPRequestGetOrPostParameter(HTTPRequestHandle hRequest, string pchParamName, string pchParamValue)
```

<para>在请求上设置GET或POST参数值，具体设置哪种参数取决于创建请求时指定的EHTTPMethod。</para> <para>必须在发送请求之前调用此方法。如果句柄无效或请求已发送，将返回false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchParamName` (`string`)
- `pchParamValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
HTTPRequestHandle request = SteamGameServerHTTP.CreateHTTPRequest(EHTTPMethod.k_EHTTPMethodGET, "/api/test");
SteamGameServerHTTP.SetHTTPRequestGetOrPostParameter(request, "username", "player1");
```

### SendHTTPRequest (静态)

```csharp
bool SendHTTPRequest(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

<para>发送 HTTP 请求，若句柄无效则返回 false，否则需使用 SteamCallHandle 等待异步回调响应。</para> <para>注意：若用户处于 Steam 离线模式，则会添加 only-if-cached 缓存控制头，仅执行本地缓存查找而非发送实际远程请求。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SendHTTPRequest(myRequestHandle, out var callHandle);
```

### SendHTTPRequestAndStreamResponse (静态)

```csharp
bool SendHTTPRequestAndStreamResponse(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

发送 HTTP 请求，若句柄无效则返回 false，否则请使用 SteamCallHandle 等待异步响应。响应将通过回调完成，并在流式传输过程中监听 HTTPRequestHeadersReceived_t 和 HTTPRequestDataReceived_t 回调。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SendHTTPRequestAndStreamResponse(requestHandle, out callHandle);
```

### DeferHTTPRequest (静态)

```csharp
bool DeferHTTPRequest(HTTPRequestHandle hRequest)
```

<para> 延迟你已发送的请求，实际的 HTTP 客户端代码可能有许多请求在队列中，这将把指定的请求移至队列末尾。如果句柄无效或请求尚未发送，则返回 false。</para> <para> </para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.DeferHTTPRequest(requestHandle);
```

### PrioritizeHTTPRequest (静态)

```csharp
bool PrioritizeHTTPRequest(HTTPRequestHandle hRequest)
```

<para> 优先处理您已发送的请求。实际的 HTTP 客户端代码可能有许多请求在队列中等待，此操作会将指定的请求移至队列头部。如果句柄无效或请求尚未发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
HTTPRequestHandle hRequest = default; // 假设已通过其他方式获取有效句柄
SteamGameServerHTTP.PrioritizeHTTPRequest(hRequest);
```

### GetHTTPResponseHeaderSize (静态)

```csharp
bool GetHTTPResponseHeaderSize(HTTPRequestHandle hRequest, string pchHeaderName, out uint unResponseHeaderSize)
```

<para> 检查在给定 HTTPRequestCompleted_t 句柄的 HTTP 响应中是否存在响应头，同时</para> <para> 返回头值的大小（如果存在），以便调用方可以为 GetHTTPResponseHeaderValue 分配正确大小的缓冲区。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `unResponseHeaderSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint headerSize;
bool success = SteamGameServerHTTP.GetHTTPResponseHeaderSize(requestHandle, "Content-Type", out headerSize);
```

### GetHTTPResponseHeaderValue (静态)

```csharp
bool GetHTTPResponseHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, byte[] pHeaderValueBuffer, uint unBufferSize)
```

<para>根据 HTTPRequestCompleted_t 提供的句柄，从 HTTP 响应中获取头字段值。如果头字段不存在，或者您的缓冲区太小，无法容纳其值，则返回 false。您应首先调用 BGetHTTPResponseHeaderSize 来检查头字段是否存在，并确定所需缓冲区的大小。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pHeaderValueBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bufferSize = SteamGameServerHTTP.BGetHTTPResponseHeaderSize(requestHandle, "Content-Type");
byte[] buffer = new byte[bufferSize];
bool success = SteamGameServerHTTP.GetHTTPResponseHeaderValue(requestHandle, "Content-Type", buffer, (uint)buffer.Length);
```

### GetHTTPResponseBodySize (静态)

```csharp
bool GetHTTPResponseBodySize(HTTPRequestHandle hRequest, out uint unBodySize)
```

<para> 获取由 HTTPRequestCompleted_t 提供的 HTTP 响应中的正文数据大小，如果句柄无效，则返回 false。</para> <para> </para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unBodySize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bodySize;
bool success = SteamGameServerHTTP.GetHTTPResponseBodySize(requestHandle, out bodySize);
Console.WriteLine($"Response body size: {bodySize}");
```

### GetHTTPResponseBodyData (静态)

```csharp
bool GetHTTPResponseBodyData(HTTPRequestHandle hRequest, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para>根据 HTTPRequestCompleted_t 提供的句柄获取 HTTP 响应的主体数据，如果句柄无效、指向的是流式响应，或提供的缓冲区大小不正确，则返回 false。请先使用 BGetHTTPResponseBodySize 来获取正确的缓冲区大小。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bufferSize = 1024;
byte[] buffer = new byte[bufferSize];
bool success = SteamGameServerHTTP.GetHTTPResponseBodyData(requestHandle, buffer, bufferSize);
```

### GetHTTPStreamingResponseBodyData (静态)

```csharp
bool GetHTTPStreamingResponseBodyData(HTTPRequestHandle hRequest, uint cOffset, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para>根据来自 HTTPRequestDataReceived_t 的句柄，从流式 HTTP 响应中获取正文数据。如果句柄无效、或指向非流式响应（即未通过 SendHTTPRequestAndStreamResponse 发送）、或缓冲区大小和偏移量与 HTTPRequestDataReceived_t 中发送的大小和偏移量不匹配，则将返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `cOffset` (`uint`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.GetHTTPStreamingResponseBodyData(requestHandle, 0, buffer, bufferSize);
```

### ReleaseHTTPRequest (静态)

```csharp
bool ReleaseHTTPRequest(HTTPRequestHandle hRequest)
```

<para> 释放一个 HTTP 响应句柄，应在收到 HTTPRequestCompleted_t 回调并完成对响应的使用后调用，以释放资源。</para> <para></para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.ReleaseHTTPRequest(requestHandle);
```

### GetHTTPDownloadProgressPct (静态)

```csharp
bool GetHTTPDownloadProgressPct(HTTPRequestHandle hRequest, out float pflPercentOut)
```

<para> 获取请求正文的下载进度。除非已收到包含 content-length 字段的响应头，否则此值将为零。对于不包含 content-length 的响应，在连接关闭之前，其大小未知，因此将在请求期间始终报告为零。</para> <para> </para> <para> </para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pflPercentOut` (`out float`)

**返回值:** `bool`

**用法示例:**
```csharp
HTTPRequestHandle requestHandle = default;
float progress;
bool success = SteamGameServerHTTP.GetHTTPDownloadProgressPct(requestHandle, out progress);
```

### SetHTTPRequestRawPostBody (静态)

```csharp
bool SetHTTPRequestRawPostBody(HTTPRequestHandle hRequest, string pchContentType, byte[] pubBody, uint unBodyLen)
```

<para>为 HTTP Post 请求设置正文。在 GET 请求上会失败并返回 false，如果请求已设置 POST 参数也会失败。设置此原始正文将使其成为 post 的唯一内容，pchContentType 参数将设置请求的 content-type 标头，以便服务器知道如何解释正文。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchContentType` (`string`)
- `pubBody` (`byte[]`)
- `unBodyLen` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] body = Encoding.UTF8.GetBytes("{\"action\":\"start\"}");
SteamGameServerHTTP.SetHTTPRequestRawPostBody(requestHandle, "application/json", body, (uint)body.Length);
```

### CreateCookieContainer (静态)

```csharp
HTTPCookieContainerHandle CreateCookieContainer(bool bAllowResponsesToModify)
```

<para>创建一个 cookie 容器句柄，您必须稍后使用 ReleaseCookieContainer() 释放它。如果 bAllowResponsesToModify 为 true</para> <para>则使用此 cookie 容器发出的任何请求的响应都可以添加新 cookie，这些 cookie 可能会随</para> <para>后续请求一起发送。如果 bAllowResponsesToModify 为 false，则只有您显式设置的 cookie 才会被发送。此 API 仅用于</para> <para>进程生命周期内，在 Steam 重启后，cookie 不会被持久化，并且您无法在进程的重复执行过程中访问该 cookie 容器。</para>

**参数:**

- `bAllowResponsesToModify` (`bool`)

**返回值:** `HTTPCookieContainerHandle`

**用法示例:**
```csharp
SteamGameServerHTTP.HTTPCookieContainerHandle container = SteamGameServerHTTP.CreateCookieContainer(true);
SteamGameServerHTTP.ReleaseCookieContainer(container);
```

### ReleaseCookieContainer (静态)

```csharp
bool ReleaseCookieContainer(HTTPCookieContainerHandle hCookieContainer)
```

<para> 释放您已使用完毕的 Cookie 容器，以释放其内存</para>

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.ReleaseCookieContainer(hCookieContainer);
```

### SetCookie (静态)

```csharp
bool SetCookie(HTTPCookieContainerHandle hCookieContainer, string pchHost, string pchUrl, string pchCookie)
```

<para> 向指定的 cookie 容器中添加一个 cookie，该 cookie 将用于后续的请求。</para>

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)
- `pchHost` (`string`)
- `pchUrl` (`string`)
- `pchCookie` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetCookie(HTTPCookieContainerHandle.Invalid, "example.com", "/api", "sessionid=abc123");
```

### SetHTTPRequestCookieContainer (静态)

```csharp
bool SetHTTPRequestCookieContainer(HTTPRequestHandle hRequest, HTTPCookieContainerHandle hCookieContainer)
```

<para> 设置用于 HTTP 请求的 Cookie 容器</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `hCookieContainer` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.SetHTTPRequestCookieContainer(requestHandle, cookieContainerHandle);
```

### SetHTTPRequestUserAgentInfo (静态)

```csharp
bool SetHTTPRequestUserAgentInfo(HTTPRequestHandle hRequest, string pchUserAgentInfo)
```

<para> 为请求设置额外的用户代理信息，此操作不会覆盖常规的用户代理，只是在末尾添加额外信息</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchUserAgentInfo` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.SetHTTPRequestUserAgentInfo(requestHandle, "Custom-Agent/1.0");
```

### SetHTTPRequestRequiresVerifiedCertificate (静态)

```csharp
bool SetHTTPRequestRequiresVerifiedCertificate(HTTPRequestHandle hRequest, bool bRequireVerifiedCertificate)
```

<para> 禁用或重新启用对 SSL/TLS 证书的验证。</para> <para> 默认情况下，所有 HTTPS 请求都会检查证书。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `bRequireVerifiedCertificate` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestRequiresVerifiedCertificate(HTTPRequestHandle.Invalid, false);
```

### SetHTTPRequestAbsoluteTimeoutMS (静态)

```csharp
bool SetHTTPRequestAbsoluteTimeoutMS(HTTPRequestHandle hRequest, uint unMilliseconds)
```

为 HTTP 请求设置绝对超时，这是一种总时间超时，与每次获取更多数据时都会重置的网络活动超时不同。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unMilliseconds` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.SetHTTPRequestAbsoluteTimeoutMS(requestHandle, 30000);
```

### GetHTTPRequestWasTimedOut (静态)

```csharp
bool GetHTTPRequestWasTimedOut(HTTPRequestHandle hRequest, out bool pbWasTimedOut)
```

<para> 检查请求失败的原因是否是因为我们超时（而不是某些更严重的故障）</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pbWasTimedOut` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool wasTimedOut;
SteamGameServerHTTP.GetHTTPRequestWasTimedOut(requestHandle, out wasTimedOut);
Console.WriteLine($"Request timed out: {wasTimedOut}");
```

