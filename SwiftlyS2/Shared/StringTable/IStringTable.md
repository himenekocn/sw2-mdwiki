<a id="istringtable"></a>

# 🔌 IStringTable

**命名空间:** `SwiftlyS2.Shared.StringTable`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TableName` | `string` | get | 获取字符串表的名称。 |
| `TableId` | `int` | get | 获取字符串表的ID。 |
| `NumStrings` | `int` | get | 获取字符串表中字符串的数量。 |

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
int? index = stringTable.FindStringIndex("example");
```

### IsStringIndexValid

```csharp
bool IsStringIndexValid(int index)
```

检查指定的索引是否有效。

**参数:**

- `index` (`int`) - 要检查的索引。

**返回值:** `bool` - 如果索引有效则为真，否则为假。

**用法示例:**
```csharp
bool isValid = stringTable.IsStringIndexValid(0);
```

### GetString

```csharp
string? GetString(int index)
```

获取指定索引处的字符串。

**参数:**

- `index` (`int`) - 用于获取字符串的索引。

**返回值:** `string?` - 指定索引处的字符串，如果索引无效则为 null。

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
- `result` (`out StringTableOutUserData`) - 用户数据，如果索引无效则为无效数据。

**返回值:** `bool` - 如果用户数据成功检索，则为真；否则为假。

**用法示例:**
```csharp
bool success = stringTable.TryGetStringUserData(0, out var result);
```

### GetStringUserData

```csharp
StringTableOutUserData GetStringUserData(int index)
```

获取指定索引的用户数据。

**参数:**

- `index` (`int`) - 用于获取用户数据的索引。

**返回值:** `StringTableOutUserData` - 用户数据，如果索引无效则为无效数据。

**用法示例:**
```csharp
var userData = stringTable.GetStringUserData(0);
```

### TryGetStringUserData

```csharp
bool TryGetStringUserData(string str, out StringTableOutUserData result)
```

尝试获取指定字符串的用户数据。

**参数:**

- `str` (`string`) - 要获取用户数据的字符串。
- `result` (`out StringTableOutUserData`) - 用户数据，如果未找到该字符串则为无效。

**返回值:** `bool` - 如果用户数据成功检索，则为真；否则为假。

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

- `str` (`string`) - 要获取用户数据的字符串。

**返回值:** `StringTableOutUserData` - 用户数据，如果未找到该字符串则为无效。

**用法示例:**
```csharp
var userData = stringTable.GetStringUserData("example_key");
```

### SetStringUserData

```csharp
bool SetStringUserData(int index, StringTableUserData userData, bool forceOverride = true)
```

为指定的索引设置用户数据。

**参数:**

- `index` (`int`) - 用于设置用户数据的索引。
- `userData` (`StringTableUserData`) - 要设置的用户数据。
- `forceOverride` (`bool`) = `true` - 是否覆盖已存在的用户数据。

**返回值:** `bool` - 如果用户数据设置成功则为真，否则为假。

**用法示例:**
```csharp
stringTable.SetStringUserData(0, userData, true);
```

### SetStringUserData

```csharp
bool SetStringUserData(string str, StringTableUserData userData, bool forceOverride = true)
```

为指定字符串设置用户数据。

**参数:**

- `str` (`string`) - 用于设置用户数据的字符串。
- `userData` (`StringTableUserData`) - 要设置的用户数据。
- `forceOverride` (`bool`) = `true` - 是否覆盖已存在的用户数据。

**返回值:** `bool` - 如果用户数据设置成功则为真，否则为假。

**用法示例:**
```csharp
bool success = stringTable.SetStringUserData("myKey", userData, true);
```

### SetOrAddStringUserData

```csharp
bool SetOrAddStringUserData(string str, StringTableUserData userData, bool forceOverride = true)
```

为指定的字符串设置用户数据，如果该字符串不存在则添加并设置。

**参数:**

- `str` (`string`) - 用于设置用户数据的字符串。
- `userData` (`StringTableUserData`) - 要设置的用户数据。
- `forceOverride` (`bool`) = `true` - 是否覆盖已存在的用户数据。

**返回值:** `bool` - 如果用户数据成功设置或添加则为 true，否则为 false。

**用法示例:**
```csharp
stringTable.SetOrAddStringUserData("player_name", userData, true);
```

### GetOrAddString

```csharp
int GetOrAddString(string str)
```

获取字符串表中指定字符串的索引，若不存在则添加该字符串。

**参数:**

- `str` (`string`) - 要获取或添加的字符串。

**返回值:** `int` - 字符串的索引，若未找到该字符串并添加后则为新索引。

**用法示例:**
```csharp
int index = stringTable.GetOrAddString("Hello World");
```

### ReplicateUserData

```csharp
void ReplicateUserData(int stringIndex, StringTableUserData userData, in CRecipientFilter filter)
```

将指定字符串的用户数据复制到指定接收方。

**参数:**

- `stringIndex` (`int`) - 要复制的用户数据字符串的索引。
- `userData` (`StringTableUserData`) - 要复制的用户数据。
- `filter` (`in CRecipientFilter`) - 要将用户数据复制到的接收者。

**用法示例:**
```csharp
stringTable.ReplicateUserData(0, userData, filter);
```

### ReplicateUserData

```csharp
void ReplicateUserData(string str, StringTableUserData userData, in CRecipientFilter filter)
```

将指定字符串的用户数据复制给指定接收者。注意:该字符串必须在若干游戏刻之前就已添加到字符串表中。若字符串尚未添加,则复制操作将失败。若该字符串仅在此调用前1-2个游戏刻才被添加,服务器将覆盖已复制值。

**参数:**

- `str` (`string`) - 用于复制用户数据的字符串。
- `userData` (`StringTableUserData`) - 要复制的用户数据。
- `filter` (`in CRecipientFilter`) - 要将用户数据复制到的接收者。

**用法示例:**
```csharp
stringTable.ReplicateUserData("my_key", userData, filter);
```

