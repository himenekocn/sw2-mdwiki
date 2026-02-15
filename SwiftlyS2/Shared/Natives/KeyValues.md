# 🏗️ KeyValues

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `KeyNameCaseSensitive` | `int` | get, set | - |
| `DataType` | `KeyValuesDataType` | get, set | - |
| `HasEscapeSequences` | `bool` | get, set | - |
| `AllocatedExternalMemory` | `bool` | get, set | - |
| `KeySymbolCaseSensitiveMatchesCaseInsensitive` | `bool` | get, set | - |
| `StoredSubKey` | `bool` | get, set | - |

## ⚙️ 方法

### FindKey

```csharp
KeyValues* FindKey(HKeySymbol keyName, bool create = false)
```

**参数:**

- `keyName` (`HKeySymbol`)
- `create` (`bool`) = `false`

**返回值:** `KeyValues*`

### FindKey

```csharp
KeyValues* FindKey(string keyName, bool create = false)
```

**参数:**

- `keyName` (`string`)
- `create` (`bool`) = `false`

**返回值:** `KeyValues*`

### GetInt

```csharp
int GetInt(string keyName, int defaultValue = 0)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`int`) = `0`

**返回值:** `int`

### GetUint64

```csharp
ulong GetUint64(string keyName, ulong defaultValue = 0)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`ulong`) = `0`

**返回值:** `ulong`

### GetFloat

```csharp
float GetFloat(string keyName, float defaultValue = 0f)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`float`) = `0f`

**返回值:** `float`

### GetString

```csharp
string GetString(string keyName, string defaultValue = "")
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`string`) = `""`

**返回值:** `string`

### GetPtr

```csharp
nint GetPtr(string keyName, nint defaultValue = 0)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`nint`) = `0`

**返回值:** `nint`

### GetColor

```csharp
Color GetColor(string keyName, Color defaultValue)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`Color`)

**返回值:** `Color`

### GetBool

```csharp
bool GetBool(string keyName, bool defaultValue = false)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`bool`) = `false`

**返回值:** `bool`

### IsEmpty

```csharp
bool IsEmpty()
```

**返回值:** `bool`

### GetName

```csharp
string GetName()
```

**返回值:** `string`

### SetName

```csharp
void SetName(string name)
```

**参数:**

- `name` (`string`)

### SetString

```csharp
void SetString(string keyName, string value)
```

**参数:**

- `keyName` (`string`)
- `value` (`string`)

### SetInt

```csharp
void SetInt(string keyName, int value)
```

**参数:**

- `keyName` (`string`)
- `value` (`int`)

### SetFloat

```csharp
void SetFloat(string keyName, float value)
```

**参数:**

- `keyName` (`string`)
- `value` (`float`)

### SetBool

```csharp
void SetBool(string keyName, bool value)
```

**参数:**

- `keyName` (`string`)
- `value` (`bool`)

### SetPtr

```csharp
void SetPtr(string keyName, nint value)
```

**参数:**

- `keyName` (`string`)
- `value` (`nint`)

### SetColor

```csharp
void SetColor(string keyName, Color value)
```

**参数:**

- `keyName` (`string`)
- `value` (`Color`)

### GetFirstSubKey

```csharp
KeyValues* GetFirstSubKey()
```

**返回值:** `KeyValues*`

### GetNextKey

```csharp
KeyValues* GetNextKey()
```

**返回值:** `KeyValues*`

### FindLastSubKey

```csharp
KeyValues* FindLastSubKey()
```

**返回值:** `KeyValues*`

### GetFirstTrueSubKey

```csharp
KeyValues* GetFirstTrueSubKey()
```

**返回值:** `KeyValues*`

### GetNextTrueSubKey

```csharp
KeyValues* GetNextTrueSubKey()
```

**返回值:** `KeyValues*`

### GetFirstValue

```csharp
KeyValues* GetFirstValue()
```

**返回值:** `KeyValues*`

### GetNextValue

```csharp
KeyValues* GetNextValue()
```

**返回值:** `KeyValues*`

### GetDataType

```csharp
KeyValuesDataType GetDataType()
```

**返回值:** `KeyValuesDataType`

### GetDataType

```csharp
KeyValuesDataType GetDataType(string keyName)
```

**参数:**

- `keyName` (`string`)

**返回值:** `KeyValuesDataType`

