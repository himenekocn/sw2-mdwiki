<a id="steamgameserverhttp"></a>

# 📦 SteamGameServerHTTP

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateHTTPRequest (静态)

```csharp
HTTPRequestHandle CreateHTTPRequest(EHTTPMethod eHTTPRequestMethod, string pchAbsoluteURL)
```

<para> 初始化一个新的HTTP请求，返回一个句柄用于后续操作。需要</para> <para> 指定请求方法（GET或POST）以及绝对URL。支持http和https协议，</para> <para> 因此该字符串必须以http://或https://开头，格式如http://store.steampowered.com/app/250/</para> <para> 或类似形式。</para>

**参数:**

- `eHTTPRequestMethod` (`EHTTPMethod`)
- `pchAbsoluteURL` (`string`)

**返回值:** `HTTPRequestHandle`

**用法示例:**
```csharp
var requestHandle = SteamGameServerHTTP.CreateHTTPRequest(EHTTPMethod.k_EHTTPMethodGET, "https://api.steampowered.com/ISteamWebAPIUtil/GetServerInfo/v0001/");
```

### SetHTTPRequestContextValue (静态)

```csharp
bool SetHTTPRequestContextValue(HTTPRequestHandle hRequest, ulong ulContextValue)
```

<para> 为请求设置一个上下文值，该值将在发送请求后的 HTTPRequestCompleted_t 回调中返回。</para> <para> 这仅用于让调用方能够轻松追踪哪些回调对应哪些请求数据。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `ulContextValue` (`ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestContextValue(hRequest, 12345UL);
```

### SetHTTPRequestNetworkActivityTimeout (静态)

```csharp
bool SetHTTPRequestNetworkActivityTimeout(HTTPRequestHandle hRequest, uint unTimeoutSeconds)
```

<para> 为HTTP请求设置超时时间（秒），必须在发送请求前调用。默认</para> <para> 超时时间为60秒（若不调用此方法）。若句柄无效或请求</para> <para> 已发送，则返回false。</para>

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

<para> 为请求设置请求头值，必须在发送请求前调用。若句柄无效或请求已发送，</para> <para> 将返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pchHeaderValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestHeaderValue(requestHandle, "Authorization", "Bearer token123");
```

### SetHTTPRequestGetOrPostParameter (静态)

```csharp
bool SetHTTPRequestGetOrPostParameter(HTTPRequestHandle hRequest, string pchParamName, string pchParamValue)
```

<para> 在请求上设置一个GET或POST参数值，具体设置哪个取决于创建请求时指定的EHTTPMethod。</para>
<para> 必须在发送请求前调用。如果句柄无效或请求已发送，将返回false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchParamName` (`string`)
- `pchParamValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.SetHTTPRequestGetOrPostParameter(hRequest, "key", "value");
```

### SendHTTPRequest (静态)

```csharp
bool SendHTTPRequest(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

<para> 发送HTTP请求，若处理句柄无效则返回false，否则使用SteamCallHandle等待</para>
<para> 通过回调获取异步响应。</para>
<para> 注意：若用户Steam处于离线模式，则此操作将添加仅缓存缓存控制</para>
<para> 标头，仅执行本地缓存查找而不发送任何实际远程请求。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamAPICall_t callHandle;
bool success = SteamGameServerHTTP.SendHTTPRequest(hRequest, out callHandle);
```

### SendHTTPRequestAndStreamResponse (静态)

```csharp
bool SendHTTPRequestAndStreamResponse(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

<para> 发送HTTP请求，若句柄无效则返回false，否则使用SteamCallHandle等待</para> <para> 通过回调获取异步响应以完成操作，并在流式传输期间监听</para> <para> HTTPRequestHeadersReceived_t和HTTPRequestDataReceived_t回调。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamAPICall_t callHandle; bool success = SteamGameServerHTTP.SendHTTPRequestAndStreamResponse(hRequest, out callHandle);
```

### DeferHTTPRequest (静态)

```csharp
bool DeferHTTPRequest(HTTPRequestHandle hRequest)
```

<para> 延迟您已发送的请求，实际的 HTTP 客户端代码可能有许多请求在队列中等待，此操作会将</para> <para> 指定的请求移至队列尾部。若句柄无效或请求尚未发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerHTTP.DeferHTTPRequest(requestHandle);
```

### PrioritizeHTTPRequest (静态)

```csharp
bool PrioritizeHTTPRequest(HTTPRequestHandle hRequest)
```

<para> 优先处理您已发送的请求，实际HTTP客户端代码中可能有许多请求在队列中等待，此操作将</para> <para> 将指定请求移至队列头部。若句柄无效或请求尚未发送，则返回false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerHTTP.PrioritizeHTTPRequest(existingRequestHandle);
```

### GetHTTPResponseHeaderSize (静态)

```csharp
bool GetHTTPResponseHeaderSize(HTTPRequestHandle hRequest, string pchHeaderName, out uint unResponseHeaderSize)
```

<para> 检查给定HTTPRequestCompleted_t句柄的HTTP响应中是否存在某个响应头，</para> <para> 如果存在则同时返回该头值的大小，以便调用方为GetHTTPResponseHeaderValue分配正确大小的缓冲区。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `unResponseHeaderSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool exists = SteamGameServerHTTP.GetHTTPResponseHeaderSize(requestHandle, "Content-Type", out uint size);
```

### GetHTTPResponseHeaderValue (静态)

```csharp
bool GetHTTPResponseHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, byte[] pHeaderValueBuffer, uint unBufferSize)
```

<para> 从HTTPRequestCompleted_t的句柄获取HTTP响应的标头值，若标头不存在或缓冲区过小无法容纳其值则返回false。应首先调用</para> <para> BGetHTTPResponseHeaderSize以检查标头是否存在并确定所需缓冲区大小。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pHeaderValueBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = SteamGameServerHTTP.BGetHTTPResponseHeaderSize(hRequest, "Content-Type");
byte[] buffer = new byte[size]; bool success = SteamGameServerHTTP.GetHTTPResponseHeaderValue(hRequest, "Content-Type", buffer, size);
```

### GetHTTPResponseBodySize (静态)

```csharp
bool GetHTTPResponseBodySize(HTTPRequestHandle hRequest, out uint unBodySize)
```

<para> 从HTTPRequestCompleted_t提供的句柄所对应的HTTP响应中获取主体数据的大小，如果句柄无效则返回false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unBodySize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bodySize;
bool success = SteamGameServerHTTP.GetHTTPResponseBodySize(hRequest, out bodySize);
```

### GetHTTPResponseBodyData (静态)

```csharp
bool GetHTTPResponseBodyData(HTTPRequestHandle hRequest, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para> 从HTTPRequestCompleted_t提供的句柄对应的HTTP响应中获取主体数据，如果句柄无效、指向流式响应或提供的缓冲区大小不正确，则返回false。请先使用BGetHTTPResponseBodySize确定正确的缓冲区大小。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = SteamGameServerHTTP.GetHTTPResponseBodySize(hRequest);
byte[] buffer = new byte[size]; bool success = SteamGameServerHTTP.GetHTTPResponseBodyData(hRequest, buffer, size);
```

### GetHTTPStreamingResponseBodyData (静态)

```csharp
bool GetHTTPStreamingResponseBodyData(HTTPRequestHandle hRequest, uint cOffset, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para> 从给定的 HTTPRequestDataReceived_t 句柄的流式 HTTP 响应中获取主体数据。如果句柄无效、指向非流式响应（即未使用 SendHTTPRequestAndStreamResponse 发送），或者缓冲区大小和偏移量与 HTTPRequestDataReceived_t 中发送的大小和偏移量不匹配，将返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `cOffset` (`uint`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.GetHTTPStreamingResponseBodyData(hRequest, 0, buffer, (uint)buffer.Length);
```

### ReleaseHTTPRequest (静态)

```csharp
bool ReleaseHTTPRequest(HTTPRequestHandle hRequest)
```

<para> 释放HTTP响应句柄，在收到HTTPRequestCompleted_t</para> <para> 回调并完成响应使用后，应始终调用此函数以释放资源。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.ReleaseHTTPRequest(hRequest);
```

### GetHTTPDownloadProgressPct (静态)

```csharp
bool GetHTTPDownloadProgressPct(HTTPRequestHandle hRequest, out float pflPercentOut)
```

<para> 获取请求正文的下载进度。除非已收到包含内容长度字段的响应头，否则此值将为零。</para> <para> 对于不包含内容长度的响应，在请求持续期间该值将报告为零，因为在连接关闭前大小未知。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pflPercentOut` (`out float`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.GetHTTPDownloadProgressPct(hRequest, out float percent);
```

### SetHTTPRequestRawPostBody (静态)

```csharp
bool SetHTTPRequestRawPostBody(HTTPRequestHandle hRequest, string pchContentType, byte[] pubBody, uint unBodyLen)
```

<para> 设置HTTP POST请求的正文。对于GET请求将失败并返回false，如果该请求已设置POST参数也会失败。</para>
<para> 设置此原始正文将使其成为POST的唯一内容，pchContentType参数将设置请求的Content-Type标头，以便服务器了解如何解释正文。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchContentType` (`string`)
- `pubBody` (`byte[]`)
- `unBodyLen` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
var body = System.Text.Encoding.UTF8.GetBytes("{\"key\":\"value\"}");
SteamGameServerHTTP.SetHTTPRequestRawPostBody(hRequest, "application/json", body, (uint)body.Length);
```

### CreateCookieContainer (静态)

```csharp
HTTPCookieContainerHandle CreateCookieContainer(bool bAllowResponsesToModify)
```

<para> 创建一个Cookie容器句柄，之后必须通过ReleaseCookieContainer()释放。若bAllowResponsesToModify=true</para> <para> 则使用此Cookie容器的任何请求的响应都可能添加新Cookie，这些Cookie可能随</para> <para> 后续请求一起发送。若bAllowResponsesToModify=false，则仅会发送你显式设置的Cookie。此API仅适用于</para> <para> 进程生命周期内，Steam重启后不会持久化任何Cookie，你也无法在</para> <para> 进程重复执行期间访问该Cookie容器。</para>

**参数:**

- `bAllowResponsesToModify` (`bool`)

**返回值:** `HTTPCookieContainerHandle`

**用法示例:**
```csharp
var cookieHandle = SteamGameServerHTTP.CreateCookieContainer(true);
```

### ReleaseCookieContainer (静态)

```csharp
bool ReleaseCookieContainer(HTTPCookieContainerHandle hCookieContainer)
```

<para> 释放使用完毕的Cookie容器，释放其内存</para>

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.ReleaseCookieContainer(cookieHandle);
```

### SetCookie (静态)

```csharp
bool SetCookie(HTTPCookieContainerHandle hCookieContainer, string pchHost, string pchUrl, string pchCookie)
```

<para> 向指定的Cookie容器中添加一个Cookie，该Cookie将在后续请求中使用。</para>

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)
- `pchHost` (`string`)
- `pchUrl` (`string`)
- `pchCookie` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetCookie(HTTPCookieContainerHandle.Invalid, "example.com", "/api", "session=abc123");
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
bool result = SteamGameServerHTTP.SetHTTPRequestCookieContainer(hRequest, hCookieContainer);
```

### SetHTTPRequestUserAgentInfo (静态)

```csharp
bool SetHTTPRequestUserAgentInfo(HTTPRequestHandle hRequest, string pchUserAgentInfo)
```

<para> 设置请求的额外用户代理信息，这不会覆盖正常的用户代理，仅在末尾添加额外信息</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchUserAgentInfo` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestUserAgentInfo(requestHandle, "MyCustomBot/1.0");
```

### SetHTTPRequestRequiresVerifiedCertificate (静态)

```csharp
bool SetHTTPRequestRequiresVerifiedCertificate(HTTPRequestHandle hRequest, bool bRequireVerifiedCertificate)
```

<para>禁用或重新启用 SSL/TLS 证书验证。</para>
<para>默认情况下，所有 HTTPS 请求都会检查证书。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `bRequireVerifiedCertificate` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestRequiresVerifiedCertificate(requestHandle, false);
```

### SetHTTPRequestAbsoluteTimeoutMS (静态)

```csharp
bool SetHTTPRequestAbsoluteTimeoutMS(HTTPRequestHandle hRequest, uint unMilliseconds)
```

<para> 对HTTP请求设置绝对超时，这与网络活动超时不同，后者会在每次获取更多数据时重置</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unMilliseconds` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerHTTP.SetHTTPRequestAbsoluteTimeoutMS(hRequest, 5000);
```

### GetHTTPRequestWasTimedOut (静态)

```csharp
bool GetHTTPRequestWasTimedOut(HTTPRequestHandle hRequest, out bool pbWasTimedOut)
```

<para> 检查请求失败的原因是否是我们请求超时（而非更严重的故障）</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pbWasTimedOut` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool wasTimedOut;
SteamGameServerHTTP.GetHTTPRequestWasTimedOut(requestHandle, out wasTimedOut);
```

