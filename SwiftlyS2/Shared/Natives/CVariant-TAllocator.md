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
var variant = new CVariant();
variant.byte(1);
```

### IsVoid

```csharp
bool IsVoid()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isVoid = variant.IsVoid();
```

### SetBool

```csharp
void SetBool(bool value)
```

**参数:**

- `value` (`bool`)

**用法示例:**
```csharp
CVariant variant;
variant.SetBool(true);
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
CVariant variant;
variant.SetShort(10);
```

### SetUShort

```csharp
void SetUShort(ushort value)
```

**参数:**

- `value` (`ushort`)

**用法示例:**
```csharp
CVariant variant;
variant.SetUShort(123);
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
variant.SetUInt(100);
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
variant.SetLong(100L);
```

### SetULong

```csharp
void SetULong(ulong value)
```

**参数:**

- `value` (`ulong`)

**用法示例:**
```csharp
CVariant variant;
variant.SetULong(1234567890UL);
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
CVariant variant;
variant.SetDouble(3.14);
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
variant.SetHScript(script);
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
CVariant variant;
variant.SetString("Hello");
```

### SetVector2D

```csharp
void SetVector2D(Vector2D value)
```

**参数:**

- `value` (`Vector2D`)

**用法示例:**
```csharp
cVariant.SetVector2D(Vector2D.Zero);
```

### SetVector

```csharp
void SetVector(Vector value)
```

**参数:**

- `value` (`Vector`)

**用法示例:**
```csharp
variant.SetVector(Vector.Zero);
```

### SetVector4D

```csharp
void SetVector4D(Vector4D value)
```

**参数:**

- `value` (`Vector4D`)

**用法示例:**
```csharp
cvariant.SetVector4D(Vector4D.Zero);
```

### SetQAngle

```csharp
void SetQAngle(QAngle value)
```

**参数:**

- `value` (`QAngle`)

**用法示例:**
```csharp
CVariant variant;
variant.SetQAngle(new QAngle(0, 90, 0));
```

### SetQuaternion

```csharp
void SetQuaternion(Quaternion value)
```

**参数:**

- `value` (`Quaternion`)

**用法示例:**
```csharp
variant.SetQuaternion(Quaternion.Identity);
```

### SetColor

```csharp
void SetColor(Color value)
```

**参数:**

- `value` (`Color`)

**用法示例:**
```csharp
variant.SetColor(Color.Red);
```

### Set<T>

```csharp
void Set<T>(T value)
```

**参数:**

- `value` (`T`)

**用法示例:**
```csharp
CVariant variant = default;
variant.Set(42);
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
char c;
bool success = variant.TryGetChar(out c);
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
bool success = variant.TryGetInt16(out short value);
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
bool success = variant.TryGetInt32(out int value);
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
bool success = variant.TryGetUInt32(out uint value);
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
CVariant variant = default;
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
bool success = cVariant.TryGetUInt64(out ulong value);
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
bool success = variant.TryGetDouble(out double value);
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
bool success = cVariant.TryGetResourceHandle(out var handle);
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
if (variant.TryGetHScript(out var script)) { script.Call(); }
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
bool success = cVariant.TryGetCHandle<IntPtr>(out IntPtr handle);
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
if (variant.TryGetVector2D(out var vec)) Console.WriteLine(vec);
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
bool success = variant.TryGetVector(out Vector3 result);
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
bool success = variant.TryGetVector4D(out var vector);
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
bool success = variant.TryGetQAngle(out var angle);
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
if (variant.TryGetQuaternion(out var quat)) { }
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
bool success = variant.TryGetColor(out Color color);
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
if (cVariant.TryGetString(out string value)) { /* use value */ }
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

