# 📦 Schema

**命名空间:** `SwiftlyS2.Core.Schemas`

**类型:** `class`

## ⚙️ 方法

### GetOffset (静态)

```csharp
nint GetOffset(ulong hash)
```

**参数:**

- `hash` (`ulong`)

**返回值:** `nint`

### Update (静态)

```csharp
void Update(nint handle, ulong hash)
```

**参数:**

- `handle` (`nint`)
- `hash` (`ulong`)

### SetString (静态)

```csharp
void SetString(nint handle, nint offset, string value)
```

**参数:**

- `handle` (`nint`)
- `offset` (`nint`)
- `value` (`string`)

### SetFixedString (静态)

```csharp
void SetFixedString(nint handle, nint offset, string value, int maxSize)
```

**参数:**

- `handle` (`nint`)
- `offset` (`nint`)
- `value` (`string`)
- `maxSize` (`int`)

### GetString (静态)

```csharp
string GetString(nint handle)
```

**参数:**

- `handle` (`nint`)

**返回值:** `string`

### GetCUtlString (静态)

```csharp
string GetCUtlString(nint handle)
```

**参数:**

- `handle` (`nint`)

**返回值:** `string`

### SetCUtlString (静态)

```csharp
void SetCUtlString(nint handle, nint offset, string value)
```

**参数:**

- `handle` (`nint`)
- `offset` (`nint`)
- `value` (`string`)

