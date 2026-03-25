<a id="imemoryservice"></a>

# 🔌 IMemoryService

**命名空间:** `SwiftlyS2.Shared.Memory`

**类型:** `interface`

## ⚙️ 方法

### GetUnmanagedFunctionByAddress<TDelegate>

```csharp
IUnmanagedFunction<TDelegate> GetUnmanagedFunctionByAddress<TDelegate>(nint address)
```

根据其地址获取一个非托管函数。

**参数:**

- `address` (`nint`) - 非托管函数的地址。

**返回值:** `IUnmanagedFunction\<TDelegate\>` - 非托管函数。

**用法示例:**
```csharp
var func = memoryService.GetUnmanagedFunctionByAddress<MyDelegate>(0x12345678);
```

### GetUnmanagedFunctionByVTable<TDelegate>

```csharp
IUnmanagedFunction<TDelegate> GetUnmanagedFunctionByVTable<TDelegate>(nint pVTable, int index)
```

通过其虚表地址和索引获取一个非托管函数。

**参数:**

- `pVTable` (`nint`) - 虚函数表（vtable）的地址。
- `index` (`int`) - 该函数在虚表中的索引。

**返回值:** `IUnmanagedFunction\<TDelegate\>` - 非托管函数。

**用法示例:**
```csharp
var func = memoryService.GetUnmanagedFunctionByVTable<MyDelegate>(pVTable, 0);
```

### GetUnmanagedMemoryByAddress

```csharp
IUnmanagedMemory GetUnmanagedMemoryByAddress(nint address)
```

根据其地址获取未托管内存块。

**参数:**

- `address` (`nint`) - 用于创建非托管内存包装器的地址。

**返回值:** `IUnmanagedMemory`

**用法示例:**
```csharp
var memory = memoryService.GetUnmanagedMemoryByAddress(address);
```

### GetInterfaceByName

```csharp
nint? GetInterfaceByName(string name)
```

根据其名称获取 Valve 或 Swiftly 原生接口的地址。

**参数:**

- `name` (`string`) - 接口的名称。

**返回值:** `nint?` - 接口的地址。若未找到则返回 null。

**用法示例:**
```csharp
nint? address = memoryService.GetInterfaceByName("IServer");
```

### GetAddressBySignature

```csharp
nint? GetAddressBySignature(string library, string signature)
```

获取 IDA 风格签名的地址。

**参数:**

- `library` (`string`) - 该签名所属的库。
- `signature` (`string`) - 该函数的签名。

**返回值:** `nint?` - 函数的地址。若未找到则返回 null。

**用法示例:**
```csharp
nint? address = memoryService.GetAddressBySignature("server.dll", "48 89 5C 24 ?");
```

### GetVTableAddress

```csharp
nint? GetVTableAddress(string library, string vtableName)
```

通过名称获取虚函数表（vtable）的地址。

**参数:**

- `library` (`string`) - 所属的虚函数表（vtable）库。
- `vtableName` (`string`) - 虚表（vtable）的名称。

**返回值:** `nint?` - 虚函数表（vtable）的地址。若未找到，则返回 null。

**用法示例:**
```csharp
var addr = memoryService.GetVTableAddress("server", "CBaseEntity");
```

### ResolveXrefAddress

```csharp
nint ResolveXrefAddress(nint xrefAddress)
```

解析跨引用签名的地址。

**参数:**

- `xrefAddress` (`nint`) - 交叉引用的地址。

**返回值:** `nint` - 解析后的地址。

**用法示例:**
```csharp
nint resolvedAddress = memoryService.ResolveXrefAddress(xrefAddress);
```

### GetObjectPtrVtableName

```csharp
string? GetObjectPtrVtableName(nint address)
```

获取对象指针的虚表名称。

**参数:**

- `address` (`nint`) - 对象指针的地址。

**返回值:** `string?` - 虚函数表名称。若未找到则返回 null。

**用法示例:**
```csharp
string? vtableName = memoryService.GetObjectPtrVtableName(address);
```

### ObjectPtrHasVtable

```csharp
bool ObjectPtrHasVtable(nint address)
```

检查对象指针是否拥有虚函数表（vtable）。

**参数:**

- `address` (`nint`) - 对象指针的地址。

**返回值:** `bool` - 如果对象指针具有虚函数表（vtable），则为 true，否则为 false。

**用法示例:**
```csharp
bool hasVtable = memoryService.ObjectPtrHasVtable(address);
```

### ObjectPtrHasBaseClass

```csharp
bool ObjectPtrHasBaseClass(nint address, string baseClassName)
```

检查对象指针是否拥有基类。

**参数:**

- `address` (`nint`) - 对象指针的地址。
- `baseClassName` (`string`) - 基类的名称。

**返回值:** `bool` - 当对象指针具有基类时为 true，否则为 false。

**用法示例:**
```csharp
bool hasBase = memoryService.ObjectPtrHasBaseClass(player.Address, "CBasePlayer");
```

### ToSchemaClass<T>

```csharp
T ToSchemaClass<T>(nint address)
```

将原始地址转换为架构类。

**参数:**

- `address` (`nint`) - Schema 类的地址。

**返回值:** `T` - 模式类。

**用法示例:**
```csharp
var schemaClass = memoryService.ToSchemaClass<MySchema>(address);
```

### Alloc

```csharp
nint Alloc(ulong size)
```

分配一块内存。

**参数:**

- `size` (`ulong`) - 要分配的内存块的大小。

**返回值:** `nint` - 已分配内存块的地址。

**用法示例:**
```csharp
nint ptr = memoryService.Alloc(1024);
```

### Free

```csharp
void Free(nint pointer)
```

释放一块内存。

**参数:**

- `pointer` (`nint`) - 要释放的内存块地址。

**用法示例:**
```csharp
memoryService.Free(pointer);
```

### Resize

```csharp
nint Resize(nint pointer, ulong newSize)
```

调整内存块的大小。

**参数:**

- `pointer` (`nint`) - 要调整大小的内存块地址。
- `newSize` (`ulong`) - 内存块的新大小。

**返回值:** `nint` - 调整大小后的内存块的地址。

**用法示例:**
```csharp
nint newPointer = memoryService.Resize(existingPointer, 1024);
```

