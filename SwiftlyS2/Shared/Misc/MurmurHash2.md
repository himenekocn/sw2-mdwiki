<a id="murmurhash2"></a>

# 📦 MurmurHash2

**命名空间:** `SwiftlyS2.Shared.Misc`

**类型:** `class`

## ⚙️ 方法

### Hash (静态)

```csharp
uint Hash(byte[] data, uint seed = 0x31415926)
```

计算字节数组的 MurmurHash2（32 位）哈希值，可选指定种子值。

**参数:**

- `data` (`byte[]`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

**用法示例:**
```csharp
byte[] data = System.Text.Encoding.UTF8.GetBytes("example");
uint hash = MurmurHash2.Hash(data, 0x9747b28c);
```

### HashString (静态)

```csharp
uint HashString(string text, uint seed = 0x31415926)
```

字符串的便捷方法（UTF8）。

**参数:**

- `text` (`string`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

**用法示例:**
```csharp
uint hash = MurmurHash2.HashString("HelloWorld", 0);
```

### HashStringLowercase (静态)

```csharp
uint HashStringLowercase(string text, uint seed = 0x31415926)
```

将字符串转换为小写，然后进行哈希处理。

**参数:**

- `text` (`string`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

**用法示例:**
```csharp
uint hash = MurmurHash2.HashStringLowercase("HelloWorld", 0);
```

