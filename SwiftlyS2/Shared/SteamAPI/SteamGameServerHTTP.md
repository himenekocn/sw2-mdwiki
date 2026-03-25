# 📦 SteamGameServerHTTP

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateHTTPRequest (静态)

```csharp
HTTPRequestHandle CreateHTTPRequest(EHTTPMethod eHTTPRequestMethod, string pchAbsoluteURL)
```

<para>初始化一个新的 HTTP 请求，返回一个句柄以用于后续的对该请求的操作。需要指定请求方法（GET 或 POST）以及请求的绝对 URL。支持 http 和 https 协议，因此该字符串必须以 http://或 https://开头，格式应类似于 http://store.steampowered.com/app/250/等。</para>

**参数:**

- `eHTTPRequestMethod` (`EHTTPMethod`)
- `pchAbsoluteURL` (`string`)

**返回值:** `HTTPRequestHandle`

**用法示例:**
```csharp
HTTPRequestHandle request = SteamGameServerHTTP.CreateHTTPRequest(EHTTPMethod.GET, "https://store.steampowered.com/app/250/");
```

### SetHTTPRequestContextValue (静态)

```csharp
bool SetHTTPRequestContextValue(HTTPRequestHandle hRequest, ulong ulContextValue)
```

<para>为请求设置上下文值，该值将在发送请求后随 HTTPRequestCompleted_t 回调返回。</para><para>此功能仅用于使调用方能轻松追踪回调与对应请求数据的关联关系。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `ulContextValue` (`ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestContextValue(requestHandle, 12345UL);
```

### SetHTTPRequestNetworkActivityTimeout (静态)

```csharp
bool SetHTTPRequestNetworkActivityTimeout(HTTPRequestHandle hRequest, uint unTimeoutSeconds)
```

<para>设置 HTTP 请求的超时时间（单位：秒），必须在发送请求之前调用。若未调用此方法，默认超时时间为 60 秒。如果句柄无效或请求已发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unTimeoutSeconds` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestNetworkActivityTimeout(hRequest, 10u);
```

### SetHTTPRequestHeaderValue (静态)

```csharp
bool SetHTTPRequestHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, string pchHeaderValue)
```

<para>为请求设置请求头值，必须在发送请求之前调用。如果句柄无效或请求已发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pchHeaderValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestHeaderValue(requestHandle, "Content-Type", "application/json");
```

### SetHTTPRequestGetOrPostParameter (静态)

```csharp
bool SetHTTPRequestGetOrPostParameter(HTTPRequestHandle hRequest, string pchParamName, string pchParamValue)
```

<para>设置请求的 GET 或 POST 参数值，具体取决于创建请求时指定的 EHTTPMethod。必须在发送请求之前调用此方法。如果句柄无效或请求已发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchParamName` (`string`)
- `pchParamValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestGetOrPostParameter(requestHandle, "appid", "480");
```

### SendHTTPRequest (静态)

```csharp
bool SendHTTPRequest(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

<para>发送 HTTP 请求；若句柄无效则返回 false，否则请使用 SteamCallHandle 通过回调等待异步响应。</para><para>注意：如果用户处于 Steam 离线模式，则此操作将添加仅缓存的 Cache-Control 头，并仅执行本地缓存查找，而不会发送任何实际的网络请求。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamAPICall_t callHandle;
bool ok = SteamGameServerHTTP.SendHTTPRequest(hRequest, out callHandle);
```

### SendHTTPRequestAndStreamResponse (静态)

```csharp
bool SendHTTPRequestAndStreamResponse(HTTPRequestHandle hRequest, out SteamAPICall_t pCallHandle)
```

发送 HTTP 请求；句柄无效时返回 false，否则请使用 SteamCallHandle 等待。通过回调异步响应完成状态，并在流式传输期间监听 HTTPRequestHeadersReceived_t 和 HTTPRequestDataReceived_t 回调。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pCallHandle` (`out SteamAPICall_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamAPICall_t callHandle; bool ok = SteamGameServerHTTP.SendHTTPRequestAndStreamResponse(reqHandle, out callHandle);
```

### DeferHTTPRequest (静态)

```csharp
bool DeferHTTPRequest(HTTPRequestHandle hRequest)
```

<para>延迟您已发送的请求。实际的 HTTP 客户端代码中可能存在多个排队请求，此操作会将指定请求移至队列末尾。若句柄无效或请求尚未发送，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool deferred = SteamGameServerHTTP.DeferHTTPRequest(hRequest);
```

### PrioritizeHTTPRequest (静态)

```csharp
bool PrioritizeHTTPRequest(HTTPRequestHandle hRequest)
```

优先处理您已发送的请求。实际的 HTTP 客户端代码中可能已有多个请求排队，此操作会将指定的请求移至队列头部。若句柄无效或请求尚未发送，则返回 false。

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool prioritized = SteamGameServerHTTP.PrioritizeHTTPRequest(requestHandle);
```

### GetHTTPResponseHeaderSize (静态)

```csharp
bool GetHTTPResponseHeaderSize(HTTPRequestHandle hRequest, string pchHeaderName, out uint unResponseHeaderSize)
```

<para>检查给定自 HTTPRequestCompleted_t 的句柄的 HTTP 响应中是否存在指定的响应头；若存在，同时返回该头值的大小，以便调用方分配正确大小的缓冲区以调用 GetHTTPResponseHeaderValue。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `unResponseHeaderSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint headerSize; bool hasHeader = SteamGameServerHTTP.GetHTTPResponseHeaderSize(requestHandle, "Content-Type", out headerSize);
```

### GetHTTPResponseHeaderValue (静态)

```csharp
bool GetHTTPResponseHeaderValue(HTTPRequestHandle hRequest, string pchHeaderName, byte[] pHeaderValueBuffer, uint unBufferSize)
```

<para>从 HTTP 响应中获取指定头部的值。该函数接受一个来自 HTTPRequestCompleted_t 的句柄，若请求的头部不存在或提供的缓冲区不足以容纳其值，则返回 false。您应首先调用 BGetHTTPResponseHeaderSize 以检查该头部是否存在并确定所需缓冲区的大小。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchHeaderName` (`string`)
- `pHeaderValueBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint headerSize = 0; SteamGameServerHTTP.BGetHTTPResponseHeaderSize(hRequest, "Content-Type", ref headerSize);
SteamGameServerHTTP.GetHTTPResponseHeaderValue(hRequest, "Content-Type", headerValueBuffer, headerSize);
```

### GetHTTPResponseBodySize (静态)

```csharp
bool GetHTTPResponseBodySize(HTTPRequestHandle hRequest, out uint unBodySize)
```

从 HTTP 响应中获取主体数据的大小，该函数接受由 HTTPRequestCompleted_t 结构体提供的句柄；若句柄无效则返回 false。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unBodySize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bodySize;
bool ok = SteamGameServerHTTP.GetHTTPResponseBodySize(requestHandle, out bodySize);
```

### GetHTTPResponseBodyData (静态)

```csharp
bool GetHTTPResponseBodyData(HTTPRequestHandle hRequest, byte[] pBodyDataBuffer, uint unBufferSize)
```

从 HTTP 响应中获取 Body 数据，需提供来自 HTTPRequestCompleted_t 的句柄；若句柄无效、指向流式响应，或提供的缓冲区大小不正确，则返回 false。请先调用 BGetHTTPResponseBodySize 以确定应使用的正确缓冲区大小。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bodySize; SteamGameServerHTTP.BGetHTTPResponseBodySize(requestHandle, out bodySize);
bool ok = SteamGameServerHTTP.GetHTTPResponseBodyData(requestHandle, bodyBuffer, bodySize);
```

### GetHTTPStreamingResponseBodyData (静态)

```csharp
bool GetHTTPStreamingResponseBodyData(HTTPRequestHandle hRequest, uint cOffset, byte[] pBodyDataBuffer, uint unBufferSize)
```

<para> 从给定 HTTPRequestDataReceived_t 句柄的流式 HTTP 响应中获取正文数据。若该句柄无效、指向非流式响应（即未通过 SendHTTPRequestAndStreamResponse 发送），或缓冲区大小和偏移量与 HTTPRequestDataReceived_t 中声明的大小及偏移量不匹配，则返回 false。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `cOffset` (`uint`)
- `pBodyDataBuffer` (`byte[]`)
- `unBufferSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.GetHTTPStreamingResponseBodyData(hRequest, 0u, bodyDataBuffer, (uint)bodyDataBuffer.Length);
```

### ReleaseHTTPRequest (静态)

```csharp
bool ReleaseHTTPRequest(HTTPRequestHandle hRequest)
```

释放 HTTP 响应句柄；在接收到 HTTPRequestCompleted_t 回调并结束使用该响应后，应始终调用此方法以释放资源。

**参数:**

- `hRequest` (`HTTPRequestHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool released = SteamGameServerHTTP.ReleaseHTTPRequest(hRequest);
if (released) Console.WriteLine("HTTP request handle released.");
```

### GetHTTPDownloadProgressPct (静态)

```csharp
bool GetHTTPDownloadProgressPct(HTTPRequestHandle hRequest, out float pflPercentOut)
```

获取请求主体的下载进度。除非已接收到包含 Content-Length 字段的响应头，否则此值将为零。对于不包含 Content-Length 字段的响应，在连接关闭前由于大小未知，该值将始终报告为零。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pflPercentOut` (`out float`)

**返回值:** `bool`

**用法示例:**
```csharp
float percent;
bool ok = SteamGameServerHTTP.GetHTTPDownloadProgressPct(hRequest, out percent);
```

### SetHTTPRequestRawPostBody (静态)

```csharp
bool SetHTTPRequestRawPostBody(HTTPRequestHandle hRequest, string pchContentType, byte[] pubBody, uint unBodyLen)
```

设置 HTTP POST 请求的主体。在 GET 请求上执行此操作将失败并返回 false；若请求已设置过 POST 参数，此操作也将失败。设置此原始主体将使该主体成为 POST 的唯一内容；pchContentType 参数将设置请求的 Content-Type 头，以便服务器能够正确解析主体。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchContentType` (`string`)
- `pubBody` (`byte[]`)
- `unBodyLen` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerHTTP.SetHTTPRequestRawPostBody(hRequest, "application/json", body, (uint)body.Length);
```

### CreateCookieContainer (静态)

```csharp
HTTPCookieContainerHandle CreateCookieContainer(bool bAllowResponsesToModify)
```

<para>创建一个 Cookie 容器句柄，后续需使用 ReleaseCookieContainer() 释放。若 bAllowResponsesToModify 为 true</para> <para>，则任何通过此 Cookie 容器发出的请求所接收到的响应均可添加新 Cookie，这些新 Cookie 将在后续请求中自动携带发送。若 bAllowResponsesToModify 为 false，则仅会发送您显式设置的 Cookie。本 API 仅适用于进程运行期间；Steam 重启后不会持久化保存任何 Cookie，且无法在进程的多次重复执行间访问同一 Cookie 容器。</para>

**参数:**

- `bAllowResponsesToModify` (`bool`)

**返回值:** `HTTPCookieContainerHandle`

**用法示例:**
```csharp
var cookieContainer = SteamGameServerHTTP.CreateCookieContainer(true);
SteamGameServerHTTP.ReleaseCookieContainer(cookieContainer);
```

### ReleaseCookieContainer (静态)

```csharp
bool ReleaseCookieContainer(HTTPCookieContainerHandle hCookieContainer)
```

释放已使用完毕的 Cookie 容器，以释放其内存

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

将 Cookie 添加到指定的 Cookie 容器，该容器将在后续请求中使用。

**参数:**

- `hCookieContainer` (`HTTPCookieContainerHandle`)
- `pchHost` (`string`)
- `pchUrl` (`string`)
- `pchCookie` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetCookie(cookieContainer, "example.com", "/login", "sessionid=abc123");
```

### SetHTTPRequestCookieContainer (静态)

```csharp
bool SetHTTPRequestCookieContainer(HTTPRequestHandle hRequest, HTTPCookieContainerHandle hCookieContainer)
```

设置用于 HTTP 请求的 Cookie 容器。

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `hCookieContainer` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestCookieContainer(requestHandle, cookieContainerHandle);
```

### SetHTTPRequestUserAgentInfo (静态)

```csharp
bool SetHTTPRequestUserAgentInfo(HTTPRequestHandle hRequest, string pchUserAgentInfo)
```

<para>设置请求的额外用户代理信息，此操作不会覆盖常规的用户代理，仅在其末尾追加额外信息。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pchUserAgentInfo` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestUserAgentInfo(requestHandle, "MyGameServer/1.0");
```

### SetHTTPRequestRequiresVerifiedCertificate (静态)

```csharp
bool SetHTTPRequestRequiresVerifiedCertificate(HTTPRequestHandle hRequest, bool bRequireVerifiedCertificate)
```

<para>禁用或重新启用对 SSL/TLS 证书的验证。</para> <para>默认情况下，所有 HTTPS 请求均会检查证书。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `bRequireVerifiedCertificate` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestRequiresVerifiedCertificate(requestHandle, true);
```

### SetHTTPRequestAbsoluteTimeoutMS (静态)

```csharp
bool SetHTTPRequestAbsoluteTimeoutMS(HTTPRequestHandle hRequest, uint unMilliseconds)
```

<para>为 HTTP 请求设置绝对超时时间；此为总耗时超时，不同于网络活动超时</para> <para>该网络活动超时值可能在每次获取更多数据时被更新。</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `unMilliseconds` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerHTTP.SetHTTPRequestAbsoluteTimeoutMS(hRequest, 5000);
```

### GetHTTPRequestWasTimedOut (静态)

```csharp
bool GetHTTPRequestWasTimedOut(HTTPRequestHandle hRequest, out bool pbWasTimedOut)
```

<para>检查请求失败的原因是否为超时（而非其他更严重的故障）</para>

**参数:**

- `hRequest` (`HTTPRequestHandle`)
- `pbWasTimedOut` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool wasTimedOut;
bool ok = SteamGameServerHTTP.GetHTTPRequestWasTimedOut(requestHandle, out wasTimedOut);
```

