# 📦 MurmurHash2

**命名空间:** `SwiftlyS2.Shared.Misc`

**类型:** `class`

## ⚙️ 方法

### Hash (静态)

```csharp
uint Hash(byte[] data, uint seed = 0x31415926)
```

计算字节数组的 MurmurHash2 (32位) 哈希值，可指定可选的种子。

**参数:**

- `data` (`byte[]`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

**用法示例:**
```csharp
uint hash = MurmurHash2.Hash(new byte[] { 1, 2, 3 }, 0x12345678);
```

### HashString (静态)

```csharp
uint HashString(string text, uint seed = 0x31415926)
```

字符串的便捷方法 (UTF8)。

**参数:**

- `text` (`string`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

**用法示例:**
```csharp
uint hash = MurmurHash2.HashString("hello", 0x12345678);
```

### HashStringLowercase (静态)

```csharp
uint HashStringLowercase(string text, uint seed = 0x31415926)
```

将字符串转换为小写，然后对其进行哈希处理。

**参数:**

- `text` (`string`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

**用法示例:**
```csharp
uint hash = MurmurHash2.HashStringLowercase("Hello World", 0x12345678);
```

