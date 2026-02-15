# 📦 NativeHooks

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### AllocateHook (静态)

```csharp
nint AllocateHook()
```

**返回值:** `nint`

### AllocateVHook (静态)

```csharp
nint AllocateVHook()
```

**返回值:** `nint`

### AllocateMHook (静态)

```csharp
nint AllocateMHook()
```

**返回值:** `nint`

### DeallocateHook (静态)

```csharp
void DeallocateHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### DeallocateVHook (静态)

```csharp
void DeallocateVHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### DeallocateMHook (静态)

```csharp
void DeallocateMHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### SetHook (静态)

```csharp
void SetHook(nint hook, nint func, nint callback)
```

the callback should receive the exact arguments as the function has, and to return the same amount of arguments

**参数:**

- `hook` (`nint`)
- `func` (`nint`)
- `callback` (`nint`)

### SetVHook (静态)

```csharp
void SetVHook(nint hook, nint entityOrVTable, int index, nint callback, bool isVtable)
```

the callback should receive the exact arguments as the function has, and to return the same amount of arguments, plus the first argument needs to be the pointer to the original function

**参数:**

- `hook` (`nint`)
- `entityOrVTable` (`nint`)
- `index` (`int`)
- `callback` (`nint`)
- `isVtable` (`bool`)

### SetMHook (静态)

```csharp
void SetMHook(nint hook, nint addr, nint callback)
```

the callback should receive `ref Context64`

**参数:**

- `hook` (`nint`)
- `addr` (`nint`)
- `callback` (`nint`)

### EnableHook (静态)

```csharp
void EnableHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### EnableVHook (静态)

```csharp
void EnableVHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### EnableMHook (静态)

```csharp
void EnableMHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### DisableHook (静态)

```csharp
void DisableHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### DisableVHook (静态)

```csharp
void DisableVHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### DisableMHook (静态)

```csharp
void DisableMHook(nint hook)
```

**参数:**

- `hook` (`nint`)

### IsHookEnabled (静态)

```csharp
bool IsHookEnabled(nint hook)
```

**参数:**

- `hook` (`nint`)

**返回值:** `bool`

### IsVHookEnabled (静态)

```csharp
bool IsVHookEnabled(nint hook)
```

**参数:**

- `hook` (`nint`)

**返回值:** `bool`

### IsMHookEnabled (静态)

```csharp
bool IsMHookEnabled(nint hook)
```

**参数:**

- `hook` (`nint`)

**返回值:** `bool`

### GetHookOriginal (静态)

```csharp
nint GetHookOriginal(nint hook)
```

**参数:**

- `hook` (`nint`)

**返回值:** `nint`

### GetVHookOriginal (静态)

```csharp
nint GetVHookOriginal(nint hook)
```

**参数:**

- `hook` (`nint`)

**返回值:** `nint`

