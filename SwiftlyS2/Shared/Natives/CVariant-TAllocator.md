<a id="cvariant-tallocator"></a>

# 🏗️ CVariant&lt;TAllocator&gt;

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IDisposable
    where TAllocator : IVariantAllocator`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Flags` | `CVFlags` | - | - |

## ⚙️ 方法

### byte

```csharp
1 byte(uint8 enum)
```

**参数:**

- `enum` (`uint8`)

**返回值:** `1`

**用法示例:**
```csharp
CVariant variant = CVariant.byte((byte)Team.T);
```

### IsVoid

```csharp
bool IsVoid()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isVoid = cVariant.IsVoid();
```

### SetBool

```csharp
void SetBool(bool value)
```

**参数:**

- `value` (`bool`)

**用法示例:**
```csharp
CVariant variant; variant.SetBool(true);
```

### SetChar

```csharp
void SetChar(char value)
```

**参数:**

- `value` (`char`)

**用法示例:**
```csharp
variant.SetChar('A');
```

### SetShort

```csharp
void SetShort(short value)
```

**参数:**

- `value` (`short`)

**用法示例:**
```csharp
variant.SetShort(123);
```

### SetUShort

```csharp
void SetUShort(ushort value)
```

**参数:**

- `value` (`ushort`)

**用法示例:**
```csharp
CVariant variant; variant.SetUShort(123);
```

### SetInt

```csharp
void SetInt(int value)
```

**参数:**

- `value` (`int`)

**用法示例:**
```csharp
variant.SetInt(42);
```

### SetUInt

```csharp
void SetUInt(uint value)
```

**参数:**

- `value` (`uint`)

**用法示例:**
```csharp
variant.SetUInt(42);
```

### SetLong

```csharp
void SetLong(long value)
```

**参数:**

- `value` (`long`)

**用法示例:**
```csharp
CVariant variant;
variant.SetLong(12345L);
```

### SetULong

```csharp
void SetULong(ulong value)
```

**参数:**

- `value` (`ulong`)

**用法示例:**
```csharp
CVariant var;
var.SetULong(1234567890);
```

### SetFloat

```csharp
void SetFloat(float value)
```

**参数:**

- `value` (`float`)

**用法示例:**
```csharp
variant.SetFloat(3.14f);
```

### SetDouble

```csharp
void SetDouble(double value)
```

**参数:**

- `value` (`double`)

**用法示例:**
```csharp
CVariant variant; variant.SetDouble(3.14);
```

### SetResourceHandle

```csharp
void SetResourceHandle(ResourceHandle value)
```

**参数:**

- `value` (`ResourceHandle`)

**用法示例:**
```csharp
variant.SetResourceHandle(handle);
```

### SetUtlStringToken

```csharp
void SetUtlStringToken(CUtlStringToken value)
```

**参数:**

- `value` (`CUtlStringToken`)

**用法示例:**
```csharp
variant.SetUtlStringToken(token);
```

### SetHScript

```csharp
void SetHScript(HSCRIPT value)
```

**参数:**

- `value` (`HSCRIPT`)

**用法示例:**
```csharp
variant.SetHScript(existingScript);
```

### SetHandle

```csharp
void SetHandle(ICHandle value)
```

**参数:**

- `value` (`ICHandle`)

**用法示例:**
```csharp
variant.SetHandle(handle);
```

### SetString

```csharp
void SetString(string value)
```

**参数:**

- `value` (`string`)

**用法示例:**
```csharp
variant.SetString("HelloWorld");
```

### SetVector2D

```csharp
void SetVector2D(Vector2D value)
```

**参数:**

- `value` (`Vector2D`)

**用法示例:**
```csharp
CVariant variant; variant.SetVector2D(new Vector2D(1.0f, 2.0f));
```

### SetVector

```csharp
void SetVector(Vector value)
```

**参数:**

- `value` (`Vector`)

**用法示例:**
```csharp
CVariant variant; variant.SetVector(Vector.Zero);
```

### SetVector4D

```csharp
void SetVector4D(Vector4D value)
```

**参数:**

- `value` (`Vector4D`)

**用法示例:**
```csharp
CVariant variant; variant.SetVector4D(new Vector4D(1.0f, 2.0f, 3.0f, 4.0f));
```

### SetQAngle

```csharp
void SetQAngle(QAngle value)
```

**参数:**

- `value` (`QAngle`)

**用法示例:**
```csharp
variant.SetQAngle(QAngle.Zero);
```

### SetQuaternion

```csharp
void SetQuaternion(Quaternion value)
```

**参数:**

- `value` (`Quaternion`)

**用法示例:**
```csharp
variant.SetQuaternion(Quaternion.Euler(0, 90, 0));
```

### SetColor

```csharp
void SetColor(Color value)
```

**参数:**

- `value` (`Color`)

**用法示例:**
```csharp
cvar.SetColor(Color.Red);
```

### Set<T>

```csharp
void Set<T>(T value)
```

**参数:**

- `value` (`T`)

**用法示例:**
```csharp
CVariant variant; variant.Set(42);
```

### TryGetBool

```csharp
bool TryGetBool([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetBool(out bool value);
```

### TryGetChar

```csharp
bool TryGetChar([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
char value; bool success = variant.TryGetChar(out value);
```

### TryGetInt16

```csharp
bool TryGetInt16([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (convar.TryGetInt16(out short value)) { }
```

### TryGetUInt16

```csharp
bool TryGetUInt16([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetUInt16(out ushort value);
```

### TryGetInt32

```csharp
bool TryGetInt32([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetInt32(out int value)) { Console.WriteLine(value); }
```

### TryGetUInt32

```csharp
bool TryGetUInt32([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetUInt32(out uint value)) { Console.WriteLine(value); }
```

### TryGetInt64

```csharp
bool TryGetInt64([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetInt64(out long value);
```

### TryGetUInt64

```csharp
bool TryGetUInt64([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetUInt64(out ulong value)) { Console.WriteLine(value); }
```

### TryGetFloat

```csharp
bool TryGetFloat([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetFloat(out float value)) Console.WriteLine(value);
```

### TryGetDouble

```csharp
bool TryGetDouble([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetDouble(out double value)) Console.WriteLine(value);
```

### TryGetResourceHandle

```csharp
bool TryGetResourceHandle([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetResourceHandle(out var handle);
```

### TryGetUtlStringToken

```csharp
bool TryGetUtlStringToken([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetUtlStringToken(out string token);
```

### TryGetHScript

```csharp
bool TryGetHScript([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetHScript(out var hScript);
```

### TryGetCHandle<T>

```csharp
bool TryGetCHandle<T>([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetCHandle<CBasePlayer>(out var handle)) { var player = handle; }
```

### TryGetVector2D

```csharp
bool TryGetVector2D([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetVector2D(out var vector)) { Console.WriteLine(vector); }
```

### TryGetVector

```csharp
bool TryGetVector([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetVector(out var vector)) { }
```

### TryGetVector4D

```csharp
bool TryGetVector4D([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetVector4D(out var vector)) { Console.WriteLine(vector); }
```

### TryGetQAngle

```csharp
bool TryGetQAngle([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetQAngle(out QAngle angle);
```

### TryGetQuaternion

```csharp
bool TryGetQuaternion([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = variant.TryGetQuaternion(out var quaternion);
```

### TryGetColor

```csharp
bool TryGetColor([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (cVariant.TryGetColor(out var color)) { Console.WriteLine(color); }
```

### TryGetString

```csharp
bool TryGetString([MaybeNullWhen(false )
```

**参数:**

- `` (`[MaybeNullWhen(false`)

**返回值:** `bool`

**用法示例:**
```csharp
if (variant.TryGetString(out string? value)) Console.WriteLine(value);
```

### ToString

```csharp
string? ToString()
```

**返回值:** `string?`

### Free

```csharp
void Free()
```

**用法示例:**
```csharp
variant.Free();
```

### Dispose

```csharp
void Dispose()
```

