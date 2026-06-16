<a id="imemoryservice"></a>

# 🔌 IMemoryService

**命名空间:** `SwiftlyS2.Shared.Memory`

**类型:** `interface`

## ⚙️ 方法

### GetUnmanagedFunctionByAddress<TDelegate>

```csharp
IUnmanagedFunction<TDelegate> GetUnmanagedFunctionByAddress<TDelegate>(nint address)
```

根据地址获取非托管函数。

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

通过虚函数表地址和索引获取非托管函数。

**参数:**

- `pVTable` (`nint`) - 虚函数表的地址。
- `index` (`int`) - vtable 中函数的索引。

**返回值:** `IUnmanagedFunction\<TDelegate\>` - 非托管函数。

**用法示例:**
```csharp
var func = memoryService.GetUnmanagedFunctionByVTable<Action>(vTablePtr, 0);
```

### GetUnmanagedMemoryByAddress

```csharp
IUnmanagedMemory GetUnmanagedMemoryByAddress(nint address)
```

根据地址获取一个非托管内存块。

**参数:**

- `address` (`nint`) - 用于创建非托管内存封装的地址。

**返回值:** `IUnmanagedMemory`

**用法示例:**
```csharp
var memory = memoryService.GetUnmanagedMemoryByAddress(0x12345678);
```

### GetInterfaceByName

```csharp
nint? GetInterfaceByName(string name)
```

根据名称获取Valve或Swiftly原生接口的地址。

**参数:**

- `name` (`string`) - 接口的名称。

**返回值:** `nint?` - 接口的地址。如果未找到则返回null。

**用法示例:**
```csharp
nint? address = memoryService.GetInterfaceByName("VEngineClient014");
```

### GetAddressBySignature

```csharp
nint? GetAddressBySignature(string library, string signature)
```

获取IDA风格签名的地址。

**参数:**

- `library` (`string`) - 该签名所属的库。
- `signature` (`string`) - 函数的签名。

**返回值:** `nint?` - 函数的地址。若未找到则返回 null。

**用法示例:**
```csharp
var address = memoryService.GetAddressBySignature("server.dll", "48 89 5C 24 ?");
```

### GetVTableAddress

```csharp
nint? GetVTableAddress(string library, string vtableName)
```

通过名称获取虚函数表地址。

**参数:**

- `library` (`string`) - 该虚函数表所属的库。
- `vtableName` (`string`) - vtable 的名称。

**返回值:** `nint?` - 虚函数表的地址。如果未找到则返回 null。

**用法示例:**
```csharp
var vtableAddr = memoryService.GetVTableAddress("server.dll", "CBaseEntity");
```

### ResolveXrefAddress

```csharp
nint ResolveXrefAddress(nint xrefAddress)
```

解析交叉引用签名的地址。

**参数:**

- `xrefAddress` (`nint`) - 交叉引用的地址。

**返回值:** `nint` - 已解析的地址。

**用法示例:**
```csharp
nint resolvedAddress = memoryService.ResolveXrefAddress(0x12345678);
```

### GetObjectPtrVtableName

```csharp
string? GetObjectPtrVtableName(nint address)
```

获取对象指针的虚函数表名称。

**参数:**

- `address` (`nint`) - 对象指针的地址。

**返回值:** `string?` - vtable 名称。如果未找到则返回 null。

**用法示例:**
```csharp
string? vtableName = memoryService.GetObjectPtrVtableName(0x12345678);
```

### ObjectPtrHasVtable

```csharp
bool ObjectPtrHasVtable(nint address)
```

检查对象指针是否具有虚函数表。

**参数:**

- `address` (`nint`) - 对象指针的地址。

**返回值:** `bool` - 如果对象指针具有虚函数表（vtable）则为真，否则为假。

**用法示例:**
```csharp
bool hasVtable = memoryService.ObjectPtrHasVtable(0x12345678);
```

### ObjectPtrHasBaseClass

```csharp
bool ObjectPtrHasBaseClass(nint address, string baseClassName)
```

检查对象指针是否具有基类。

**参数:**

- `address` (`nint`) - 对象指针的地址。
- `baseClassName` (`string`) - 基类的名称。

**返回值:** `bool` - 如果对象指针拥有基类则为真，否则为假。

**用法示例:**
```csharp
bool hasBase = memoryService.ObjectPtrHasBaseClass(0x12345678, "CBaseEntity");
```

### ToSchemaClass<T>

```csharp
T ToSchemaClass<T>(nint address)
```

将原始地址转换为架构类。

**参数:**

- `address` (`nint`) - 架构类（schema class）的地址。

**返回值:** `T` - 模式类。

**用法示例:**
```csharp
var schema = memoryService.ToSchemaClass<Player>(0x12345678);
```

### ToServerSideClient

```csharp
IServerSideClient ToServerSideClient(nint address)
```

将原始地址转换为服务端客户端

**参数:**

- `address` (`nint`) - 服务端客户端地址。

**返回值:** `IServerSideClient` - 服务端客户端。

**用法示例:**
```csharp
var client = memoryService.ToServerSideClient(address);
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

**返回值:** `nint` - 调整后的内存块地址。

**用法示例:**
```csharp
nint newPtr = memoryService.Resize(oldPointer, 1024);
```

