# 📦 StringAlloc

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### CStringAction

```csharp
void CStringAction(byte* cstr)
```

**参数:**

- `cstr` (`byte*`)

**用法示例:**
```csharp
unsafe { byte* cstr = stackalloc byte[] { (byte)'H', (byte)'i', 0 }; StringAlloc.CStringAction(cstr); }
```

### CreateCString (静态)

```csharp
void CreateCString(string str, int treshold, Action<nint> action)
```

**参数:**

- `str` (`string`)
- `treshold` (`int`)
- `action` (`Action\<nint\>`)

**用法示例:**
```csharp
StringAlloc.CreateCString("hello", 16, ptr => Console.WriteLine(ptr));
```

### CreateCString (静态)

```csharp
void CreateCString(string str, Action<nint> action)
```

**参数:**

- `str` (`string`)
- `action` (`Action\<nint\>`)

**用法示例:**
```csharp
StringAlloc.CreateCString("hello", ptr => Console.WriteLine(ptr));
```

### CreateCString<T> (静态)

```csharp
T CreateCString<T>(string str, int treshold, Func<nint, T> action)
```

**参数:**

- `str` (`string`)
- `treshold` (`int`)
- `action` (`Func\<nint, T\>`)

**返回值:** `T`

**用法示例:**
```csharp
nint ptr = StringAlloc.CreateCString<nint>("hello", 32, p => p);
```

### CreateCString<T> (静态)

```csharp
T CreateCString<T>(string str, Func<nint, T> action)
```

**参数:**

- `str` (`string`)
- `action` (`Func\<nint, T\>`)

**返回值:** `T`

**用法示例:**
```csharp
var result = StringAlloc.CreateCString<int>("hello", ptr => ptr != 0 ? 1 : 0);
```

### CreateCSharpString (静态)

```csharp
string CreateCSharpString(int length, int treshold, Action<nint> action)
```

**参数:**

- `length` (`int`)
- `treshold` (`int`)
- `action` (`Action\<nint\>`)

**返回值:** `string`

**用法示例:**
```csharp
var s = StringAlloc.CreateCSharpString(16, 8, p => System.Console.WriteLine(p));
```

### CreateCSharpString (静态)

```csharp
string CreateCSharpString(int length, Action<nint> action)
```

**参数:**

- `length` (`int`)
- `action` (`Action\<nint\>`)

**返回值:** `string`

**用法示例:**
```csharp
var s = StringAlloc.CreateCSharpString(16, ptr => { });
```

