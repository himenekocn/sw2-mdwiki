# 📦 NativeBenchmark

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### VoidToVoid (静态)

```csharp
void VoidToVoid()
```

### GetBool (静态)

```csharp
bool GetBool()
```

**返回值:** `bool`

### GetInt32 (静态)

```csharp
int GetInt32()
```

**返回值:** `int`

### GetUInt32 (静态)

```csharp
uint GetUInt32()
```

**返回值:** `uint`

### GetInt64 (静态)

```csharp
long GetInt64()
```

**返回值:** `long`

### GetUInt64 (静态)

```csharp
ulong GetUInt64()
```

**返回值:** `ulong`

### GetFloat (静态)

```csharp
float GetFloat()
```

**返回值:** `float`

### GetDouble (静态)

```csharp
double GetDouble()
```

**返回值:** `double`

### GetPtr (静态)

```csharp
nint GetPtr()
```

**返回值:** `nint`

### BoolToBool (静态)

```csharp
bool BoolToBool(bool value)
```

**参数:**

- `value` (`bool`)

**返回值:** `bool`

### Int32ToInt32 (静态)

```csharp
int Int32ToInt32(int value)
```

**参数:**

- `value` (`int`)

**返回值:** `int`

### UInt32ToUInt32 (静态)

```csharp
uint UInt32ToUInt32(uint value)
```

**参数:**

- `value` (`uint`)

**返回值:** `uint`

### Int64ToInt64 (静态)

```csharp
long Int64ToInt64(long value)
```

**参数:**

- `value` (`long`)

**返回值:** `long`

### UInt64ToUInt64 (静态)

```csharp
ulong UInt64ToUInt64(ulong value)
```

**参数:**

- `value` (`ulong`)

**返回值:** `ulong`

### FloatToFloat (静态)

```csharp
float FloatToFloat(float value)
```

**参数:**

- `value` (`float`)

**返回值:** `float`

### DoubleToDouble (静态)

```csharp
double DoubleToDouble(double value)
```

**参数:**

- `value` (`double`)

**返回值:** `double`

### PtrToPtr (静态)

```csharp
nint PtrToPtr(nint value)
```

**参数:**

- `value` (`nint`)

**返回值:** `nint`

### StringToString (静态)

```csharp
string StringToString(string value)
```

**参数:**

- `value` (`string`)

**返回值:** `string`

### StringToPtr (静态)

```csharp
nint StringToPtr(string value)
```

**参数:**

- `value` (`string`)

**返回值:** `nint`

### MultiPrimitives (静态)

```csharp
int MultiPrimitives(nint p1, int i1, float f1, bool b1, ulong u1)
```

**参数:**

- `p1` (`nint`)
- `i1` (`int`)
- `f1` (`float`)
- `b1` (`bool`)
- `u1` (`ulong`)

**返回值:** `int`

### MultiWithOneString (静态)

```csharp
int MultiWithOneString(nint p1, string s1, nint p2, int i1, float f1)
```

**参数:**

- `p1` (`nint`)
- `s1` (`string`)
- `p2` (`nint`)
- `i1` (`int`)
- `f1` (`float`)

**返回值:** `int`

### MultiWithTwoStrings (静态)

```csharp
void MultiWithTwoStrings(nint p1, string s1, nint p2, string s2, int i1)
```

**参数:**

- `p1` (`nint`)
- `s1` (`string`)
- `p2` (`nint`)
- `s2` (`string`)
- `i1` (`int`)

### VectorToVector (静态)

```csharp
void VectorToVector(nint result, Vector value)
```

**参数:**

- `result` (`nint`)
- `value` (`Vector`)

### QAngleToQAngle (静态)

```csharp
void QAngleToQAngle(nint result, QAngle value)
```

**参数:**

- `result` (`nint`)
- `value` (`QAngle`)

### ComplexWithString (静态)

```csharp
void ComplexWithString(nint entity, Vector pos, string name, QAngle angle)
```

**参数:**

- `entity` (`nint`)
- `pos` (`Vector`)
- `name` (`string`)
- `angle` (`QAngle`)

