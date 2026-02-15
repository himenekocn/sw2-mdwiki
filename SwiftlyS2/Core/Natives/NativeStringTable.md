# 📦 NativeStringTable

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### ContainerFindTable (静态)

```csharp
nint ContainerFindTable(string tableName)
```

**参数:**

- `tableName` (`string`)

**返回值:** `nint`

### ContainerGetTableById (静态)

```csharp
nint ContainerGetTableById(int tableId)
```

**参数:**

- `tableId` (`int`)

**返回值:** `nint`

### GetTableId (静态)

```csharp
int GetTableId(nint table)
```

**参数:**

- `table` (`nint`)

**返回值:** `int`

### GetTableName (静态)

```csharp
string GetTableName(nint table)
```

**参数:**

- `table` (`nint`)

**返回值:** `string`

### GetNumStrings (静态)

```csharp
int GetNumStrings(nint table)
```

**参数:**

- `table` (`nint`)

**返回值:** `int`

### FindStringIndex (静态)

```csharp
int FindStringIndex(nint table, string str)
```

**参数:**

- `table` (`nint`)
- `str` (`string`)

**返回值:** `int`

### IsStringIndexValid (静态)

```csharp
bool IsStringIndexValid(nint table, int index)
```

**参数:**

- `table` (`nint`)
- `index` (`int`)

**返回值:** `bool`

### GetString (静态)

```csharp
string GetString(nint table, int index)
```

**参数:**

- `table` (`nint`)
- `index` (`int`)

**返回值:** `string`

### GetStringUserData (静态)

```csharp
nint GetStringUserData(nint table, int index)
```

**参数:**

- `table` (`nint`)
- `index` (`int`)

**返回值:** `nint`

### SetStringUserData (静态)

```csharp
bool SetStringUserData(nint table, int index, nint userData, int userDataSize, bool forceOverride)
```

**参数:**

- `table` (`nint`)
- `index` (`int`)
- `userData` (`nint`)
- `userDataSize` (`int`)
- `forceOverride` (`bool`)

**返回值:** `bool`

### AddString (静态)

```csharp
int AddString(nint table, string str)
```

**参数:**

- `table` (`nint`)
- `str` (`string`)

**返回值:** `int`

### Serialize (静态)

```csharp
byte[] Serialize(nint table, int index, string keyName, bool newKey, nint userData, int userDataSize)
```

**参数:**

- `table` (`nint`)
- `index` (`int`)
- `keyName` (`string`)
- `newKey` (`bool`)
- `userData` (`nint`)
- `userDataSize` (`int`)

**返回值:** `byte[]`

