# 🏗️ DurationControl_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `k_iCallback` | `int` | const | - |
| `m_appid` | `AppId_t` | - | - |
| `m_bApplicable` | `bool` | - | - |
| `m_csecsLast5h` | `int` | - | - |
| `m_csecsToday` | `int` | - | - |
| `m_csecsRemaining` | `int` | - | - |

## ⚙️ 方法

### call

```csharp
of call(always k_EResultOK for asynchronous timer-based notifications)
```

**参数:**

- `notifications` (`always k_EResultOK for asynchronous timer-based`)

**返回值:** `of`

**用法示例:**
```csharp
durationControl.call();
```

### progress

```csharp
recommended progress(either everything is fine, or please exit game)
```

**参数:**

- `fine` (`either everything is`)
- `game` (`or please exit`)

**返回值:** `recommended`

**用法示例:**
```csharp
var result = durationControl.progress();
```

### any

```csharp
if any(always k_EDurationControlNotification_None for API calls)
```

**参数:**

- `calls` (`always k_EDurationControlNotification_None for API`)

**返回值:** `if`

**用法示例:**
```csharp
if (durationControl.Any(DurationControlNotification.k_EDurationControlNotification_None)) { }
```

