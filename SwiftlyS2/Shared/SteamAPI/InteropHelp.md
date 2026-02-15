# 📦 InteropHelp

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### TestIfPlatformSupported (静态)

```csharp
void TestIfPlatformSupported()
```

**用法示例:**
```csharp
InteropHelp.TestIfPlatformSupported();
```

### TestIfAvailableClient (静态)

```csharp
void TestIfAvailableClient()
```

**用法示例:**
```csharp
InteropHelp.TestIfAvailableClient();
```

### TestIfAvailableGameServer (静态)

```csharp
void TestIfAvailableGameServer()
```

**用法示例:**
```csharp
InteropHelp.TestIfAvailableGameServer();
```

### PtrToStringUTF8 (静态)

```csharp
string PtrToStringUTF8(IntPtr nativeUtf8)
```

**参数:**

- `nativeUtf8` (`IntPtr`)

**返回值:** `string`

**用法示例:**
```csharp
string str = InteropHelp.PtrToStringUTF8(someIntPtr);
```

### ByteArrayToStringUTF8 (静态)

```csharp
string ByteArrayToStringUTF8(byte[] buffer)
```

**参数:**

- `buffer` (`byte[]`)

**返回值:** `string`

**用法示例:**
```csharp
string result = InteropHelp.ByteArrayToStringUTF8(new byte[] { 72, 101, 108, 108, 111 });
```

### StringToByteArrayUTF8 (静态)

```csharp
void StringToByteArrayUTF8(string str, byte[] outArrayBuffer, int outArrayBufferSize)
```

**参数:**

- `str` (`string`)
- `outArrayBuffer` (`byte[]`)
- `outArrayBufferSize` (`int`)

**用法示例:**
```csharp
byte[] buffer = new byte[1024];
InteropHelp.StringToByteArrayUTF8("Hello", buffer, buffer.Length);
```

### IntPtr (静态)

```csharp
operator IntPtr(SteamParamStringArray that)
```

**参数:**

- `that` (`SteamParamStringArray`)

**返回值:** `operator`

**用法示例:**
```csharp
IntPtr ptr = InteropHelp.IntPtr(steamParamStringArrayInstance);
```

