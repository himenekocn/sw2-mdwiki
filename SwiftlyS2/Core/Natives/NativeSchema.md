# 📦 NativeSchema

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### SetStateChanged (静态)

```csharp
void SetStateChanged(nint entity, ulong hash)
```

**参数:**

- `entity` (`nint`)
- `hash` (`ulong`)

### FindChainOffset (静态)

```csharp
uint FindChainOffset(string className)
```

**参数:**

- `className` (`string`)

**返回值:** `uint`

### GetOffset (静态)

```csharp
int GetOffset(ulong hash)
```

**参数:**

- `hash` (`ulong`)

**返回值:** `int`

### IsStruct (静态)

```csharp
bool IsStruct(string className)
```

**参数:**

- `className` (`string`)

**返回值:** `bool`

### IsClassLoaded (静态)

```csharp
bool IsClassLoaded(string className)
```

**参数:**

- `className` (`string`)

**返回值:** `bool`

### GetPropPtr (静态)

```csharp
nint GetPropPtr(nint entity, ulong hash)
```

**参数:**

- `entity` (`nint`)
- `hash` (`ulong`)

**返回值:** `nint`

### WritePropPtr (静态)

```csharp
void WritePropPtr(nint entity, ulong hash, nint value, uint size)
```

**参数:**

- `entity` (`nint`)
- `hash` (`ulong`)
- `value` (`nint`)
- `size` (`uint`)

### GetVData (静态)

```csharp
nint GetVData(nint entity)
```

**参数:**

- `entity` (`nint`)

**返回值:** `nint`

### GetDatamapFunction (静态)

```csharp
nint GetDatamapFunction(uint hash)
```

**参数:**

- `hash` (`uint`)

**返回值:** `nint`

