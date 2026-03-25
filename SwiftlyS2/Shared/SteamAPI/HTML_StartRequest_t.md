<a id="html_startrequest_t"></a>

# 🏗️ HTML_StartRequest_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `k_iCallback` | `int` | const | - |
| `unBrowserHandle` | `HHTMLBrowser` | - | - |
| `pchURL` | `string` | - | - |
| `pchPostData` | `string` | - | - |
| `bIsRedirect` | `bool` | - | - |

## ⚙️ 方法

### type

```csharp
target type(i.e _blank,  _self,  _parent,  _top)
```

**参数:**

- `_blank` (`i.e`)
- `_self` (``)
- `_parent` (``)
- `_top` (``)

**返回值:** `target`

**用法示例:**
```csharp
htmlStartRequest.target("_blank");
```

