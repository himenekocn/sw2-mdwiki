# 📦 MurmurHash2

**命名空间:** `SwiftlyS2.Shared.Misc`

**类型:** `class`

## ⚙️ 方法

### Hash (静态)

```csharp
uint Hash(byte[] data, uint seed = 0x31415926)
```

Compute MurmurHash2 (32-bit) of a byte array with an optional seed.

**参数:**

- `data` (`byte[]`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

### HashString (静态)

```csharp
uint HashString(string text, uint seed = 0x31415926)
```

Convenience method for strings (UTF8).

**参数:**

- `text` (`string`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

### HashStringLowercase (静态)

```csharp
uint HashStringLowercase(string text, uint seed = 0x31415926)
```

Convert a string to lowercase and then hash it.

**参数:**

- `text` (`string`)
- `seed` (`uint`) = `0x31415926`

**返回值:** `uint`

