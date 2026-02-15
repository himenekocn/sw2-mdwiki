# 📦 MemoryService

**命名空间:** `SwiftlyS2.Core.Memory`

**类型:** `class`

**继承:** `IMemoryService`

**实现接口:** `IDisposable`

## ⚙️ 方法

### GetUnmanagedMemoryByAddress

```csharp
IUnmanagedMemory GetUnmanagedMemoryByAddress(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `IUnmanagedMemory`

### GetInterfaceByName

```csharp
nint? GetInterfaceByName(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `nint?`

### GetAddressBySignature

```csharp
nint? GetAddressBySignature(string library, string signature)
```

**参数:**

- `library` (`string`)
- `signature` (`string`)

**返回值:** `nint?`

### GetVTableAddress

```csharp
nint? GetVTableAddress(string library, string vtableName)
```

**参数:**

- `library` (`string`)
- `vtableName` (`string`)

**返回值:** `nint?`

### ResolveXrefAddress

```csharp
nint ResolveXrefAddress(nint xrefAddress)
```

**参数:**

- `xrefAddress` (`nint`)

**返回值:** `nint`

### GetObjectPtrVtableName

```csharp
string? GetObjectPtrVtableName(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `string?`

### ObjectPtrHasVtable

```csharp
bool ObjectPtrHasVtable(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `bool`

### ObjectPtrHasBaseClass

```csharp
bool ObjectPtrHasBaseClass(nint address, string baseClassName)
```

**参数:**

- `address` (`nint`)
- `baseClassName` (`string`)

**返回值:** `bool`

### Alloc

```csharp
nint Alloc(ulong size)
```

**参数:**

- `size` (`ulong`)

**返回值:** `nint`

### Free

```csharp
void Free(nint pointer)
```

**参数:**

- `pointer` (`nint`)

### Resize

```csharp
nint Resize(nint pointer, ulong newSize)
```

**参数:**

- `pointer` (`nint`)
- `newSize` (`ulong`)

**返回值:** `nint`

### Dispose

```csharp
void Dispose()
```

