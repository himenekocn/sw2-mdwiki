# 📦 NativeMemoryHelpers

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### FetchInterfaceByName (静态)

```csharp
nint FetchInterfaceByName(string ifaceName)
```

supports both internal interface system, but also valve interface system

**参数:**

- `ifaceName` (`string`)

**返回值:** `nint`

### GetVirtualTableAddress (静态)

```csharp
nint GetVirtualTableAddress(string library, string vtableName)
```

**参数:**

- `library` (`string`)
- `vtableName` (`string`)

**返回值:** `nint`

### GetVirtualTableAddressNested2 (静态)

```csharp
nint GetVirtualTableAddressNested2(string library, string class1, string class2)
```

**参数:**

- `library` (`string`)
- `class1` (`string`)
- `class2` (`string`)

**返回值:** `nint`

### GetAddressBySignature (静态)

```csharp
nint GetAddressBySignature(string library, string sig, int len, bool rawBytes)
```

**参数:**

- `library` (`string`)
- `sig` (`string`)
- `len` (`int`)
- `rawBytes` (`bool`)

**返回值:** `nint`

### GetObjectPtrVtableName (静态)

```csharp
string GetObjectPtrVtableName(nint objptr)
```

**参数:**

- `objptr` (`nint`)

**返回值:** `string`

### ObjectPtrHasVtable (静态)

```csharp
bool ObjectPtrHasVtable(nint objptr)
```

**参数:**

- `objptr` (`nint`)

**返回值:** `bool`

### ObjectPtrHasBaseClass (静态)

```csharp
bool ObjectPtrHasBaseClass(nint objptr, string baseClassName)
```

**参数:**

- `objptr` (`nint`)
- `baseClassName` (`string`)

**返回值:** `bool`

