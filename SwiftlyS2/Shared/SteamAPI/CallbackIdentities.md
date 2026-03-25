<a id="callbackidentities"></a>

# 📦 CallbackIdentities

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetCallbackIdentity (静态)

```csharp
int GetCallbackIdentity(Type callbackStruct)
```

**参数:**

- `callbackStruct` (`Type`)

**返回值:** `int`

**用法示例:**
```csharp
int identity = CallbackIdentities.GetCallbackIdentity(typeof(MyCallbackStruct));
```

