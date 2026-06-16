<a id="isteammatchmakingrulesresponse"></a>

# 📦 ISteamMatchmakingRulesResponse

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_VTRulesResponded` | `InternalRulesResponded` | - | - |
| `m_VTRulesFailedToRespond` | `InternalRulesFailedToRespond` | - | - |
| `m_VTRulesRefreshComplete` | `InternalRulesRefreshComplete` | - | - |

## ⚙️ 方法

### RulesResponded

```csharp
void RulesResponded(string pchRule, string pchValue)
```

**参数:**

- `pchRule` (`string`)
- `pchValue` (`string`)

**用法示例:**
```csharp
matchmakingRulesResponse.RulesResponded("rule_name", "rule_value");
```

### RulesFailedToRespond

```csharp
void RulesFailedToRespond()
```

**用法示例:**
```csharp
matchmakingRulesResponse.RulesFailedToRespond();
```

### RulesRefreshComplete

```csharp
void RulesRefreshComplete()
```

**用法示例:**
```csharp
matchmakingRulesResponse.RulesRefreshComplete();
```

### InternalRulesResponded

```csharp
void InternalRulesResponded(IntPtr pchRule, IntPtr pchValue)
```

**参数:**

- `pchRule` (`IntPtr`)
- `pchValue` (`IntPtr`)

**用法示例:**
```csharp
matchmakingRulesResponse.InternalRulesResponded(rulePtr, valuePtr);
```

### InternalRulesFailedToRespond

```csharp
void InternalRulesFailedToRespond()
```

**用法示例:**
```csharp
matchmakingRulesResponse.InternalRulesFailedToRespond();
```

### InternalRulesRefreshComplete

```csharp
void InternalRulesRefreshComplete()
```

**用法示例:**
```csharp
matchmakingRulesResponse.InternalRulesRefreshComplete();
```

