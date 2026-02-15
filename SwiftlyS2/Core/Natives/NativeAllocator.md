# 📦 NativeAllocator

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### Alloc (静态)

```csharp
nint Alloc(ulong size)
```

**参数:**

- `size` (`ulong`)

**返回值:** `nint`

### TrackedAlloc (静态)

```csharp
nint TrackedAlloc(ulong size, string identifier, string details)
```

**参数:**

- `size` (`ulong`)
- `identifier` (`string`)
- `details` (`string`)

**返回值:** `nint`

### Free (静态)

```csharp
void Free(nint pointer)
```

**参数:**

- `pointer` (`nint`)

### Resize (静态)

```csharp
nint Resize(nint pointer, ulong new_size)
```

**参数:**

- `pointer` (`nint`)
- `new_size` (`ulong`)

**返回值:** `nint`

### GetSize (静态)

```csharp
ulong GetSize(nint pointer)
```

works only for pointers allocated through Memory.Allocator

**参数:**

- `pointer` (`nint`)

**返回值:** `ulong`

### GetTotalAllocated (静态)

```csharp
ulong GetTotalAllocated()
```

**返回值:** `ulong`

### GetAllocatedByTrackedIdentifier (静态)

```csharp
ulong GetAllocatedByTrackedIdentifier(string identifier)
```

**参数:**

- `identifier` (`string`)

**返回值:** `ulong`

### IsPointerValid (静态)

```csharp
bool IsPointerValid(nint pointer)
```

**参数:**

- `pointer` (`nint`)

**返回值:** `bool`

### Copy (静态)

```csharp
void Copy(nint dst, nint src, ulong size)
```

**参数:**

- `dst` (`nint`)
- `src` (`nint`)
- `size` (`ulong`)

### Move (静态)

```csharp
void Move(nint dst, nint src, ulong size)
```

**参数:**

- `dst` (`nint`)
- `src` (`nint`)
- `size` (`ulong`)

