# 🏗️ CVariant<TAllocator>

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
CVariant.byte();
```

### IsVoid

```csharp
bool IsVoid()
```

**返回值:** `bool`

**用法示例:**
```csharp
CVariant variant;
bool result = variant.IsVoid();
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
CVariant variant;  
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
CVariant variant;  
variant.SetUShort(42);
```

### SetInt

```csharp
void SetInt(int value)
```

**参数:**

- `value` (`int`)

**用法示例:**
```csharp
CVariant variant;  
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
CVariant variant;  
variant.SetUInt(42u);
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
var.SetULong(123456ul);
```

### SetFloat

```csharp
void SetFloat(float value)
```

**参数:**

- `value` (`float`)

**用法示例:**
```csharp
CVariant variant;
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
convar.SetResourceHandle(ResourceHandle.Invalid);
```

### SetUtlStringToken

```csharp
void SetUtlStringToken(CUtlStringToken value)
```

**参数:**

- `value` (`CUtlStringToken`)

**用法示例:**
```csharp
CVariant variant;  
variant.SetUtlStringToken(CUtlStringToken.Invalid);
```

### SetHScript

```csharp
void SetHScript(HSCRIPT value)
```

**参数:**

- `value` (`HSCRIPT`)

**用法示例:**
```csharp
convar.SetHScript(HSCRIPT.NULL);
```

### SetHandle

```csharp
void SetHandle(ICHandle value)
```

**参数:**

- `value` (`ICHandle`)

**用法示例:**
```csharp
CVariant variant;  
variant.SetHandle(ICHandle.Null);
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
variant.SetString("Hello World");
```

### SetVector2D

```csharp
void SetVector2D(Vector2D value)
```

**参数:**

- `value` (`Vector2D`)

**用法示例:**
```csharp
convar.SetVector2D(new Vector2D(1.0f, 2.0f));
```

### SetVector

```csharp
void SetVector(Vector value)
```

**参数:**

- `value` (`Vector`)

**用法示例:**
```csharp
CVariant variant;  
variant.SetVector(new Vector(1f, 2f, 3f));
```

### SetVector4D

```csharp
void SetVector4D(Vector4D value)
```

**参数:**

- `value` (`Vector4D`)

**用法示例:**
```csharp
CVariant var;  
var.SetVector4D(new Vector4D(1f, 2f, 3f, 4f));
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
variant.SetQAngle(new QAngle(0f, 90f, 0f));
```

### SetQuaternion

```csharp
void SetQuaternion(Quaternion value)
```

**参数:**

- `value` (`Quaternion`)

**用法示例:**
```csharp
CVariant variant;  
variant.SetQuaternion(Quaternion.identity);
```

### SetColor

```csharp
void SetColor(Color value)
```

**参数:**

- `value` (`Color`)

**用法示例:**
```csharp
CVariant variant;  
variant.SetColor(Color.Red);
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
bool result = convar.TryGetBool(out bool value);
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
bool success = convar.TryGetChar(out c);
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
short value;
bool success = convar.TryGetInt16(out value);
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
ushort value;
bool success = CVariant.TryGetUInt16(out value);
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
int value;
bool success = CVariant.TryGetInt32(out value);
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
uint value;
bool success = CVariant.TryGetUInt32(out value);
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
long value;
bool success = CVariant.TryGetInt64(out value);
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
ulong value;
bool success = CVariant.TryGetUInt64(out value);
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
float value;
bool success = CVariant.TryGetFloat(out value);
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
double value;
bool success = CVariant.TryGetDouble(out value);
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
CVariant variant = default;
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
CVariant variant = default;
bool success = variant.TryGetUtlStringToken(out var token);
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
CVariant variant = default;
bool success = variant.TryGetHScript(out HScript script);
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
Vector2D v;  
bool success = convar.TryGetVector2D(out v);
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
Vector3 position;
bool success = convar.TryGetVector(out position);
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
Vector4D v;  
bool success = convar.TryGetVector4D(out v);
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
CVariant variant = default;
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
CVariant variant = default;
bool success = variant.TryGetQuaternion(out Quaternion q);
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
CVariant variant = default;
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
string result;
bool success = CVariant.TryGetString("key", out result);
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
CVariant variant = default;
variant.Free();
```

### Dispose

```csharp
void Dispose()
```

