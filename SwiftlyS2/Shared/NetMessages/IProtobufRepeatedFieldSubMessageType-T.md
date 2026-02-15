# 🔌 IProtobufRepeatedFieldSubMessageType<T>

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

**继承:** `IRepeatedField`

**实现接口:** `IEnumerable\<T\> where T : ITypedProtobuf\<T\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `int` | get | - |

## ⚙️ 方法

### Get

```csharp
T Get(int index)
```

**参数:**

- `index` (`int`)

**返回值:** `T`

**用法示例:**
```csharp
T value = convar.Get(0);
```

### Add

```csharp
T Add()
```

**返回值:** `T`

**用法示例:**
```csharp
T item = convar.Add();
```

### Clear

```csharp
void Clear()
```

**用法示例:**
```csharp
convar.Clear();
```

