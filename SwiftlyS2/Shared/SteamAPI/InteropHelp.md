# 📦 InteropHelp

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### TestIfPlatformSupported (静态)

```csharp
void TestIfPlatformSupported()
```

### TestIfAvailableClient (静态)

```csharp
void TestIfAvailableClient()
```

### TestIfAvailableGameServer (静态)

```csharp
void TestIfAvailableGameServer()
```

### PtrToStringUTF8 (静态)

```csharp
string PtrToStringUTF8(IntPtr nativeUtf8)
```

**参数:**

- `nativeUtf8` (`IntPtr`)

**返回值:** `string`

### ByteArrayToStringUTF8 (静态)

```csharp
string ByteArrayToStringUTF8(byte[] buffer)
```

**参数:**

- `buffer` (`byte[]`)

**返回值:** `string`

### StringToByteArrayUTF8 (静态)

```csharp
void StringToByteArrayUTF8(string str, byte[] outArrayBuffer, int outArrayBufferSize)
```

**参数:**

- `str` (`string`)
- `outArrayBuffer` (`byte[]`)
- `outArrayBufferSize` (`int`)

