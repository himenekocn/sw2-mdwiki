# 🏗️ KeyValues

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `KeyNameCaseSensitive` | `int` | - | - |
| `DataType` | `KeyValuesDataType` | - | - |
| `HasEscapeSequences` | `bool` | - | - |
| `AllocatedExternalMemory` | `bool` | - | - |
| `KeySymbolCaseSensitiveMatchesCaseInsensitive` | `bool` | - | - |
| `StoredSubKey` | `bool` | - | - |

## ⚙️ 方法

### FindKey

```csharp
KeyValues* FindKey(HKeySymbol keyName, bool create = false)
```

**参数:**

- `keyName` (`HKeySymbol`)
- `create` (`bool`) = `false`

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* result = existingKeyValues.FindKey(HKeySymbol.PlayerName, false);
```

### FindKey

```csharp
KeyValues* FindKey(string keyName, bool create = false)
```

**参数:**

- `keyName` (`string`)
- `create` (`bool`) = `false`

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* result = existingKeyValues.FindKey("exampleKey", true);
```

### GetInt

```csharp
int GetInt(string keyName, int defaultValue = 0)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`int`) = `0`

**返回值:** `int`

**用法示例:**
```csharp
int value = keyValues.GetInt("max_players", 10);
```

### GetUint64

```csharp
ulong GetUint64(string keyName, ulong defaultValue = 0)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`ulong`) = `0`

**返回值:** `ulong`

**用法示例:**
```csharp
ulong value = keyValues.GetUint64("player_id", 0UL);
```

### GetFloat

```csharp
float GetFloat(string keyName, float defaultValue = 0f)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`float`) = `0f`

**返回值:** `float`

**用法示例:**
```csharp
float value = keyValues.GetFloat("gravity", 9.8f);
```

### GetString

```csharp
string GetString(string keyName, string defaultValue = "")
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`string`) = `""`

**返回值:** `string`

**用法示例:**
```csharp
string value = keyValues.GetString("player_name", "Unknown");
```

### GetPtr

```csharp
nint GetPtr(string keyName, nint defaultValue = 0)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`nint`) = `0`

**返回值:** `nint`

**用法示例:**
```csharp
nint result = keyValues.GetPtr("config_ptr", IntPtr.Zero);
```

### GetColor

```csharp
Color GetColor(string keyName, Color defaultValue)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`Color`)

**返回值:** `Color`

**用法示例:**
```csharp
Color color = keyValues.GetColor("background", Color.Red);
```

### GetBool

```csharp
bool GetBool(string keyName, bool defaultValue = false)
```

**参数:**

- `keyName` (`string`)
- `defaultValue` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
bool isActive = keyValues.GetBool("enabled", false);
```

### IsEmpty

```csharp
bool IsEmpty()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isEmpty = keyValues.IsEmpty();
```

### GetName

```csharp
string GetName()
```

**返回值:** `string`

**用法示例:**
```csharp
string name = keyValues.GetName();
```

### SetName

```csharp
void SetName(string name)
```

**参数:**

- `name` (`string`)

**用法示例:**
```csharp
keyValues.SetName("example_name");
```

### SetString

```csharp
void SetString(string keyName, string value)
```

**参数:**

- `keyName` (`string`)
- `value` (`string`)

**用法示例:**
```csharp
keyValues.SetString("player_name", "Swiftly");
```

### SetInt

```csharp
void SetInt(string keyName, int value)
```

**参数:**

- `keyName` (`string`)
- `value` (`int`)

**用法示例:**
```csharp
keyValues.SetInt("rounds", 5);
```

### SetFloat

```csharp
void SetFloat(string keyName, float value)
```

**参数:**

- `keyName` (`string`)
- `value` (`float`)

**用法示例:**
```csharp
keyValues.SetFloat("health", 100.5f);
```

### SetBool

```csharp
void SetBool(string keyName, bool value)
```

**参数:**

- `keyName` (`string`)
- `value` (`bool`)

**用法示例:**
```csharp
keyValues.SetBool("is_active", true);
```

### SetPtr

```csharp
void SetPtr(string keyName, nint value)
```

**参数:**

- `keyName` (`string`)
- `value` (`nint`)

**用法示例:**
```csharp
keyValues.SetPtr("pointer_key", 0x12345678);
```

### SetColor

```csharp
void SetColor(string keyName, Color value)
```

**参数:**

- `keyName` (`string`)
- `value` (`Color`)

**用法示例:**
```csharp
keyValues.SetColor("light_color", Color.Red);
```

### GetFirstSubKey

```csharp
KeyValues* GetFirstSubKey()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* firstSubKey = existingKeyValues.GetFirstSubKey();
```

### GetNextKey

```csharp
KeyValues* GetNextKey()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* next = keyValues.GetNextKey();
```

### FindLastSubKey

```csharp
KeyValues* FindLastSubKey()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* lastSubKey = existingKeyValues.FindLastSubKey();
```

### GetFirstTrueSubKey

```csharp
KeyValues* GetFirstTrueSubKey()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* subKey = existingKeyValues.GetFirstTrueSubKey();
```

### GetNextTrueSubKey

```csharp
KeyValues* GetNextTrueSubKey()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* nextSubKey = existingKeyValues.GetNextTrueSubKey();
```

### GetFirstValue

```csharp
KeyValues* GetFirstValue()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* firstValue = existingKeyValues.GetFirstValue();
```

### GetNextValue

```csharp
KeyValues* GetNextValue()
```

**返回值:** `KeyValues*`

**用法示例:**
```csharp
KeyValues* next = keyValues.GetNextValue();
```

### GetDataType

```csharp
KeyValuesDataType GetDataType()
```

**返回值:** `KeyValuesDataType`

**用法示例:**
```csharp
KeyValuesDataType type = keyValues.GetDataType();
```

### GetDataType

```csharp
KeyValuesDataType GetDataType(string keyName)
```

**参数:**

- `keyName` (`string`)

**返回值:** `KeyValuesDataType`

**用法示例:**
```csharp
KeyValuesDataType type = keyValues.GetDataType("player_name");
```

