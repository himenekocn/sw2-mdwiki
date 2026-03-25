<a id="httprequestcompleted_t"></a>

# 🏗️ HTTPRequestCompleted_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `k_iCallback` | `int` | const | - |
| `m_hRequest` | `HTTPRequestHandle` | - | - |
| `m_ulContextValue` | `ulong` | - | - |
| `m_bRequestSuccessful` | `bool` | - | - |
| `m_eStatusCode` | `EHTTPStatusCode` | - | - |

## ⚙️ 方法

### GetHTTPResponseBodySize

```csharp
as GetHTTPResponseBodySize()
```

**返回值:** `as`

**用法示例:**
```csharp
var bodySize = requestCompleted.GetHTTPResponseBodySize();
```

