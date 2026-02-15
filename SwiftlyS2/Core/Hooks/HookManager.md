# 📦 HookManager

**命名空间:** `SwiftlyS2.Core.Hooks`

**类型:** `class`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `HookHandle` | `nint` | get, set | - |
| `OriginalFuncPtr` | `nint` | get, set | - |
| `BuiltDelegate` | `Delegate?` | get, set | - |
| `BuiltPointer` | `nint` | get, set | - |
| `HookHandle` | `nint` | get, set | - |
| `Hooked` | `bool` | get, set | - |
| `HookHandle` | `nint` | get, set | - |
| `OriginalFunctionAddress` | `nint` | get, set | - |
| `Nodes` | `List\<HookNode\>` | get, set | - |
| `Hooked` | `bool` | get, set | - |
| `HookHandle` | `nint` | get, set | - |
| `Nodes` | `List\<MidHookNode\>` | get, set | - |
| `InternalCallback` | `MidHookInternalDelegate?` | get, set | - |

## ⚙️ 方法

### IsMidHooked

```csharp
bool IsMidHooked(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `bool`

### IsHooked

```csharp
bool IsHooked(nint functionAddress)
```

**参数:**

- `functionAddress` (`nint`)

**返回值:** `bool`

### GetOriginal

```csharp
nint GetOriginal(nint functionAddress)
```

**参数:**

- `functionAddress` (`nint`)

**返回值:** `nint`

### AddMidHook

```csharp
Guid AddMidHook(nint address, MidHookDelegate callback)
```

**参数:**

- `address` (`nint`)
- `callback` (`MidHookDelegate`)

**返回值:** `Guid`

### AddHook

```csharp
Guid AddHook(nint functionAddress, Func<Func<nint>, Delegate> callbackBuilder)
```

**参数:**

- `functionAddress` (`nint`)
- `callbackBuilder` (`Func\<Func\<nint\>, Delegate\>`)

**返回值:** `Guid`

### RemoveMidHook

```csharp
void RemoveMidHook(List<Guid> nodeIds)
```

**参数:**

- `nodeIds` (`List\<Guid\>`)

### Remove

```csharp
void Remove(List<Guid> nodeIds)
```

**参数:**

- `nodeIds` (`List\<Guid\>`)

