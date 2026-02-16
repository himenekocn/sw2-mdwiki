# 📚 Datamaps

**命名空间:** `SwiftlyS2.Core.Datamaps`

共 2 个定义

## 📋 目录

- 📦 [DatamapFunctionHookManager](#datamapfunctionhookmanager)
- 🔗 [StubDelegate](#stubdelegate)

## 📦 DatamapFunctionHookManager

**命名空间:** `SwiftlyS2.Core.Datamaps`

**类型:** `class`

### ⚙️ 方法

#### AddHook (静态)

```csharp
void AddHook(nint address, nint hook)
```

**参数:**

- `address` (`nint`)
- `hook` (`nint`)

**用法示例:**
```csharp
DatamapFunctionHookManager.AddHook(0x12345678, 0x87654321);
```

#### RemoveHook (静态)

```csharp
void RemoveHook(nint address)
```

**参数:**

- `address` (`nint`)

**用法示例:**
```csharp
DatamapFunctionHookManager.RemoveHook(0x12345678);
```

#### TryGetHook (静态)

```csharp
bool TryGetHook(nint address, out nint hook)
```

**参数:**

- `address` (`nint`)
- `hook` (`out nint`)

**返回值:** `bool`

**用法示例:**
```csharp
nint hook;
bool success = DatamapFunctionHookManager.TryGetHook(0x12345678, out hook);
```



---

## 🔗 StubDelegate

**命名空间:** `SwiftlyS2.Core.Datamaps`

**类型:** `delegate`

**委托:**
```csharp
delegate void StubDelegate(nint a1);
```

**参数:**

- `a1` (`nint`)



---

