<a id="istringtable"></a>

# 🔌 IStringTable

**命名空间:** `SwiftlyS2.Shared.StringTable`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TableName` | `string` | get | 获取字符串表的名称。 |
| `TableId` | `int` | get | 获取字符串表的 ID。 |
| `NumStrings` | `int` | get | 获取字符串表中的字符串数量。 |

## ⚙️ 方法

### FindStringIndex

```csharp
int? FindStringIndex(string str)
```

在字符串表中查找指定字符串的索引。

**参数:**

- `str` (`string`) - 要查找索引的字符串。

**返回值:** `int?` - 字符串的索引，如果未找到该字符串则为 null。

**用法示例:**
```csharp
int? index = stringTable.FindStringIndex("example_string");
```

### IsStringIndexValid

```csharp
bool IsStringIndexValid(int index)
```

检查指定的索引是否有效。

**参数:**

- `index` (`int`) - 用于检查的索引。

**返回值:** `bool` - 若索引有效则为 true，否则为 false。

**用法示例:**
```csharp
bool isValid = stringTable.IsStringIndexValid(5);
```

### GetString

```csharp
string? GetString(int index)
```

获取指定索引处的字符串。

**参数:**

- `index` (`int`) - 获取字符串的索引。

**返回值:** `string?` - 指定索引处的字符串，若索引无效则为 null。

**用法示例:**
```csharp
string? value = stringTable.GetString(0);
```

### TryGetStringUserData

```csharp
bool TryGetStringUserData(int index, out StringTableOutUserData result)
```

尝试获取指定索引的用户数据。

**参数:**

- `index` (`int`) - 用于获取用户数据的索引。
- `result` (`out StringTableOutUserData`) - 用户数据，如果索引无效则为空。

**返回值:** `bool` - 若用户数据成功获取则为 true，否则为 false。

**用法示例:**
```csharp
if (stringTable.TryGetStringUserData(0, out var result)) { }
```

### GetStringUserData

```csharp
StringTableOutUserData GetStringUserData(int index)
```

获取指定索引的用户数据。

**参数:**

- `index` (`int`) - 用于获取用户数据的索引。

**返回值:** `StringTableOutUserData` - 用户数据，如果索引无效则为空。

**用法示例:**
```csharp
var userData = stringTable.GetStringUserData(0);
```

### TryGetStringUserData

```csharp
bool TryGetStringUserData(string str, out StringTableOutUserData result)
```

尝试获取指定字符串对应的用户数据。

**参数:**

- `str` (`string`) - 获取用户数据所需的字符串。
- `result` (`out StringTableOutUserData`) - 用户数据，若字符串未找到则为无效。

**返回值:** `bool` - 若用户数据成功获取则为 true，否则为 false。

**用法示例:**
```csharp
bool success = stringTable.TryGetStringUserData("key", out StringTableOutUserData result);
```

### GetStringUserData

```csharp
StringTableOutUserData GetStringUserData(string str)
```

获取指定字符串的用户数据。

**参数:**

- `str` (`string`) - 获取用户数据所需的字符串。

**返回值:** `StringTableOutUserData` - 用户数据，若字符串未找到则为无效。

**用法示例:**
```csharp
var userData = stringTable.GetStringUserData("myString");
```

### SetStringUserData

```csharp
bool SetStringUserData(int index, StringTableUserData userData, bool forceOverride = true)
```

为指定索引设置用户数据。

**参数:**

- `index` (`int`) - 用于设置用户数据的索引。
- `userData` (`StringTableUserData`) - 要设置的UserData。
- `forceOverride` (`bool`) = `true` - 如果用户数据已存在，是否覆盖该数据。

**返回值:** `bool` - 若用户数据设置成功则为 true，否则为 false。

**用法示例:**
```csharp
stringTable.SetStringUserData(0, StringTableUserData.None, true);
```

### SetStringUserData

```csharp
bool SetStringUserData(string str, StringTableUserData userData, bool forceOverride = true)
```

为指定的字符串设置用户数据。

**参数:**

- `str` (`string`) - 要为用户数据设置的字符串。
- `userData` (`StringTableUserData`) - 要设置的UserData。
- `forceOverride` (`bool`) = `true` - 如果用户数据已存在，是否覆盖该数据。

**返回值:** `bool` - 若用户数据设置成功则为 true，否则为 false。

**用法示例:**
```csharp
bool result = stringTable.SetStringUserData("example_key", existingUserData, true);
```

### SetOrAddStringUserData

```csharp
bool SetOrAddStringUserData(string str, StringTableUserData userData, bool forceOverride = true)
```

为指定的字符串设置用户数据，如果该字符串不存在，则添加该字符串并设置其值。

**参数:**

- `str` (`string`) - 要为用户数据设置的字符串。
- `userData` (`StringTableUserData`) - 要设置的UserData。
- `forceOverride` (`bool`) = `true` - 如果用户数据已存在，是否覆盖该数据。

**返回值:** `bool` - 如果用户数据成功设置或添加则为 true，否则为 false。

**用法示例:**
```csharp
stringTable.SetOrAddStringUserData("example_key", new StringTableUserData(), true);
```

### GetOrAddString

```csharp
int GetOrAddString(string str)
```

获取指定字符串在字符串表中的索引，如果不存在则将其添加。

**参数:**

- `str` (`string`) - 要获取或添加的字符串。

**返回值:** `int` - 该字符串的索引，或者如果字符串未找到并被添加时的新索引。

**用法示例:**
```csharp
int index = stringTable.GetOrAddString("example_string");
```

### ReplicateUserData

```csharp
void ReplicateUserData(int stringIndex, StringTableUserData userData, in CRecipientFilter filter)
```

将指定字符串的用户数据复制给指定的接收者。

**参数:**

- `stringIndex` (`int`) - 要为其复制用户数据的字符串索引。
- `userData` (`StringTableUserData`) - 待复制的用户数据。
- `filter` (`in CRecipientFilter`) - 用于复制用户数据的目标接收方。

**用法示例:**
```csharp
stringTable.ReplicateUserData(0, userData, filter);
```

### ReplicateUserData

```csharp
void ReplicateUserData(string str, StringTableUserData userData, in CRecipientFilter filter)
```

将指定字符串的用户数据复制给指定的接收者。请注意，该字符串必须在调用前若干帧（ticks）之前已添加到字符串表中。如果字符串未提前添加，则复制操作将失败；若该字符串仅在此调用前 1-2 帧内被添加，服务器将会覆盖已复制的值。

**参数:**

- `str` (`string`) - 用于复制用户数据的字符串。
- `userData` (`StringTableUserData`) - 待复制的用户数据。
- `filter` (`in CRecipientFilter`) - 用于复制用户数据的目标接收方。

**用法示例:**
```csharp
stringTable.ReplicateUserData("my_string", userData, new CRecipientFilter());
```

