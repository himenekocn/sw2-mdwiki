# 🏗️ CUtlMemory<T>

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Base` | `nint` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ElementSize` | `int` | - | - |
| `this[int index]` | `ref T` | - | - |
| `ExternallyAllocated` | `bool` | - | - |
| `IsReadOnly` | `bool` | - | - |
| `Base` | `nint` | - | - |
| `Count` | `int` | - | - |

## ⚙️ 方法

### Init

```csharp
void Init(int growSize, int initSize)
```

**参数:**

- `growSize` (`int`)
- `initSize` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;
memory.Init(10, 20);
```

### Purge

```csharp
void Purge()
```

**用法示例:**
```csharp
CUtlMemory memory = default;
memory.Purge();
```

### Purge

```csharp
void Purge(int numElements)
```

**参数:**

- `numElements` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;  
memory.Purge(10);
```

### ConvertToGrowableMemory

```csharp
void ConvertToGrowableMemory(int growSize)
```

**参数:**

- `growSize` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;  
memory.ConvertToGrowableMemory(10);
```

### SetExternalBuffer

```csharp
void SetExternalBuffer(nint memory, int numelements, bool readOnly)
```

**参数:**

- `memory` (`nint`)
- `numelements` (`int`)
- `readOnly` (`bool`)

**用法示例:**
```csharp
IntPtr buffer = Marshal.AllocHGlobal(100 * sizeof(int));
memory.SetExternalBuffer(buffer, 100, false);
```

### AssumeMemory

```csharp
void AssumeMemory(nint memory, int numelements)
```

**参数:**

- `memory` (`nint`)
- `numelements` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;
memory.AssumeMemory(IntPtr.Zero, 0);
```

### DetachMemory

```csharp
nint DetachMemory()
```

**返回值:** `nint`

**用法示例:**
```csharp
CUtlMemory memory = default;
nint ptr = memory.DetachMemory();
```

### Grow

```csharp
void Grow(int num)
```

**参数:**

- `num` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;
memory.Grow(10);
```

### EnsureCapacity

```csharp
void EnsureCapacity(int num)
```

**参数:**

- `num` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;  
memory.EnsureCapacity(10);
```

### SetGrowSize

```csharp
void SetGrowSize(int size)
```

**参数:**

- `size` (`int`)

**用法示例:**
```csharp
CUtlMemory memory;
memory.SetGrowSize(10);
```

