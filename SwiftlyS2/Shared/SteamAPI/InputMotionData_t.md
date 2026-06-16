<a id="inputmotiondata_t"></a>

# 🏗️ InputMotionData_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `rotQuatX` | `float` | - | - |
| `rotQuatY` | `float` | - | - |
| `rotQuatZ` | `float` | - | - |
| `rotQuatW` | `float` | - | - |
| `posAccelX` | `float` | - | - |
| `posAccelZ` | `float` | - | - |
| `rotVelX` | `float` | - | - |
| `rotVelY` | `float` | - | - |
| `rotVelZ` | `float` | - | - |

## ⚙️ 方法

### port

```csharp
charging port(forward side of controller)
```

**参数:**

- `controller` (`forward side of`)

**返回值:** `charging`

**用法示例:**
```csharp
var isCharging = inputMotionData.port;
```

