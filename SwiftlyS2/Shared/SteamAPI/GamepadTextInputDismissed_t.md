# 🏗️ GamepadTextInputDismissed_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `k_iCallback` | `int` | const | - |
| `m_unSubmittedText` | `uint` | - | - |
| `m_unAppID` | `AppId_t` | - | - |

## ⚙️ 方法

### text

```csharp
accepted text(Call ISteamUtils::GetEnteredGamepadTextInput()
```

**参数:**

- `ISteamUtils::GetEnteredGamepadTextInput(` (`Call`)

**返回值:** `accepted`

**用法示例:**
```csharp
GamepadTextInputDismissed_t.accepted(GameUtils.GetEnteredGamepadTextInput());
```

