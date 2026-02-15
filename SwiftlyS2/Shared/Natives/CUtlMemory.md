# 🏗️ CUtlMemory

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Base` | `nint` | - | - |

## ⚙️ 方法

### Init

```csharp
void Init(int growSize, int initSize)
```

**参数:**

- `growSize` (`int`)
- `initSize` (`int`)

### Purge

```csharp
void Purge()
```

### Purge

```csharp
void Purge(int numElements)
```

**参数:**

- `numElements` (`int`)

### ConvertToGrowableMemory

```csharp
void ConvertToGrowableMemory(int growSize)
```

**参数:**

- `growSize` (`int`)

### SetExternalBuffer

```csharp
void SetExternalBuffer(nint memory, int numelements, bool readOnly)
```

**参数:**

- `memory` (`nint`)
- `numelements` (`int`)
- `readOnly` (`bool`)

### AssumeMemory

```csharp
void AssumeMemory(nint memory, int numelements)
```

**参数:**

- `memory` (`nint`)
- `numelements` (`int`)

### DetachMemory

```csharp
nint DetachMemory()
```

**返回值:** `nint`

### Grow

```csharp
void Grow(int num)
```

**参数:**

- `num` (`int`)

### EnsureCapacity

```csharp
void EnsureCapacity(int num)
```

**参数:**

- `num` (`int`)

### SetGrowSize

```csharp
void SetGrowSize(int size)
```

**参数:**

- `size` (`int`)

