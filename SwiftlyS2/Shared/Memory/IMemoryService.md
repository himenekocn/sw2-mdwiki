# 🔌 IMemoryService

**命名空间:** `SwiftlyS2.Shared.Memory`

**类型:** `interface`

## ⚙️ 方法

### GetUnmanagedFunctionByAddress<TDelegate>

```csharp
IUnmanagedFunction<TDelegate> GetUnmanagedFunctionByAddress<TDelegate>(nint address)
```

通过地址获取非托管函数。

**参数:**

- `address` (`nint`) - 非托管函数的地址。

**返回值:** `IUnmanagedFunction\<TDelegate\>` - 非托管函数。

**用法示例:**
```csharp
var func = manager.GetUnmanagedFunctionByAddress<SomeDelegate>(0x12345678);
```

### GetUnmanagedFunctionByVTable<TDelegate>

```csharp
IUnmanagedFunction<TDelegate> GetUnmanagedFunctionByVTable<TDelegate>(nint pVTable, int index)
```

通过其 vtable 地址和索引获取非托管函数。

**参数:**

- `pVTable` (`nint`) - vtable 的地址。
- `index` (`int`) - vtable中该函数的索引。

**返回值:** `IUnmanagedFunction\<TDelegate\>` - 非托管函数。

**用法示例:**
```csharp
var func = manager.GetUnmanagedFunctionByVTable<SomeDelegate>(vtablePtr, 0);
```

### GetUnmanagedMemoryByAddress

```csharp
IUnmanagedMemory GetUnmanagedMemoryByAddress(nint address)
```

根据指定地址获取非托管内存块。

**参数:**

- `address` (`nint`) - 用于创建非托管内存包装器的地址。

**返回值:** `IUnmanagedMemory`

**用法示例:**
```csharp
IUnmanagedMemory mem = memoryService.GetUnmanagedMemoryByAddress(0x12345678);
```

### GetInterfaceByName

```csharp
nint? GetInterfaceByName(string name)
```

根据名称获取阀门或快速原生接口的地址。

**参数:**

- `name` (`string`) - 接口的名称。

**返回值:** `nint?` - 接口的地址。如果未找到，则返回 null。

**用法示例:**
```csharp
nint? addr = memoryService.GetInterfaceByName(" Valve ");
```

### GetAddressBySignature

```csharp
nint? GetAddressBySignature(string library, string signature)
```

获取IDA风格签名的地址。

**参数:**

- `library` (`string`) - 该签名所属的库。
- `signature` (`string`) - 函数的签名。

**返回值:** `nint?` - 函数的地址。如果未找到，则返回 null。

**用法示例:**
```csharp
nint? addr = memoryService.GetAddressBySignature("game.dll", "48 89 5C 24 ?? 48 89 74 24 ?? 57 41 56 41 57");
```

### GetVTableAddress

```csharp
nint? GetVTableAddress(string library, string vtableName)
```

根据名称获取虚函数表的地址。

**参数:**

- `library` (`string`) - 该虚函数表所属的库。
- `vtableName` (`string`) - vtable 的名称。

**返回值:** `nint?` - vtable的地址。如果未找到，则返回null。

**用法示例:**
```csharp
nint? addr = memoryService.GetVTableAddress("mylib", "MyVTableName");
```

### ResolveXrefAddress

```csharp
nint ResolveXrefAddress(nint xrefAddress)
```

解析交叉引用签名（xref signature）的地址。

**参数:**

- `xrefAddress` (`nint`) - xref 的地址。

**返回值:** `nint` - 已解析的地址。

**用法示例:**
```csharp
memoryService.ResolveXrefAddress(0x12345678);
```

### GetObjectPtrVtableName

```csharp
string? GetObjectPtrVtableName(nint address)
```

获取对象指针的虚表名称。

**参数:**

- `address` (`nint`) - 对象指针的地址。

**返回值:** `string?` - vtable 名称。如果未找到，则返回 null。

**用法示例:**
```csharp
string? vtableName = memoryService.GetObjectPtrVtableName(someAddress);
```

### ObjectPtrHasVtable

```csharp
bool ObjectPtrHasVtable(nint address)
```

检查对象指针是否具有虚函数表。

**参数:**

- `address` (`nint`) - 对象指针的地址。

**返回值:** `bool` - 如果对象指针具有虚函数表，则为 true；否则为 false。

**用法示例:**
```csharp
bool hasVtable = memoryService.ObjectPtrHasVtable(someAddress);
```

### ObjectPtrHasBaseClass

```csharp
bool ObjectPtrHasBaseClass(nint address, string baseClassName)
```

检查对象指针是否具有基类。

**参数:**

- `address` (`nint`) - 对象指针的地址。
- `baseClassName` (`string`) - 基类的名称。

**返回值:** `bool` - 如果对象指针具有基类，则为 true；否则为 false。

**用法示例:**
```csharp
bool hasBase = memoryService.ObjectPtrHasBaseClass(player.Address, "Character");
```

### ToSchemaClass<T>

```csharp
T ToSchemaClass<T>(nint address)
```

将原始地址转换为架构类。

**参数:**

- `address` (`nint`) - 架构类的地址。

**返回值:** `T` - 架构类。

**用法示例:**
```csharp
var player = manager.ToSchemaClass<Player>(0x12345678);
```

### Alloc

```csharp
nint Alloc(ulong size)
```

分配一块内存。

**参数:**

- `size` (`ulong`) - 要分配的内存块大小。

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

- `pointer` (`nint`) - 要释放的内存块的地址。

**用法示例:**
```csharp
IMemoryService.Free(pointer);
```

### Resize

```csharp
nint Resize(nint pointer, ulong newSize)
```

调整一块内存的大小。

**参数:**

- `pointer` (`nint`) - 要调整大小的内存块的地址。
- `newSize` (`ulong`) - 内存块的新大小。

**返回值:** `nint` - 调整大小后的内存块的地址。

**用法示例:**
```csharp
nint resized = IMemoryService.Resize(existingPointer, 1024UL);
```

