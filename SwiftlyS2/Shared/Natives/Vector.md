# 🏗️ Vector

3-Dimensional vector for source 2. No more cssharp chaos.

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | - |
| `Y` | `float` | - | - |
| `Z` | `float` | - | - |

## ⚙️ 方法

### Normalize

```csharp
void Normalize()
```

### Deserialize (静态)

```csharp
Vector Deserialize(string input, IFormatProvider? formatProvider = null)
```

Deserializes the vector from a string. Example input: "100 200 300"

**参数:**

- `input` (`string`) - Serialized vector in string.
- `formatProvider` (`IFormatProvider?`) = `null` - Format provider to use for the string. Null for default provider.

**返回值:** `Vector` - Deserialized vector.

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

Tries to deserialize the vector from a string. Example input: "100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - True if the deserialization was successful, false otherwise.

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

Tries to deserialize the vector from a string. Example input: "100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - True if the deserialization was successful, false otherwise.

### Normalize2D

```csharp
void Normalize2D()
```

