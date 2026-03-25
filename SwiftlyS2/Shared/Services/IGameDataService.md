<a id="igamedataservice"></a>

# 🔌 IGameDataService

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## ⚙️ 方法

### HasSignature

```csharp
bool HasSignature(string signatureName)
```

检查签名是否存在。

**参数:**

- `signatureName` (`string`) - 在 `signatures.jsonc` 文件中定义的签名名称。

**返回值:** `bool` - 签名是否存在。

**用法示例:**
```csharp
bool exists = gameDataService.HasSignature("player_join");
```

### GetSignature

```csharp
nint GetSignature(string signatureName)
```

通过名称获取签名。

**参数:**

- `signatureName` (`string`) - 在 `signatures.jsonc` 文件中定义的签名名称。

**返回值:** `nint` - 签名。

**用法示例:**
```csharp
nint sig = gameDataService.GetSignature("PlayerMove");
```

### TryGetSignature

```csharp
bool TryGetSignature(string signatureName, out nint signature)
```

尝试通过名称获取签名。

**参数:**

- `signatureName` (`string`) - 在 `signatures.jsonc` 文件中定义的签名名称。
- `signature` (`out nint`) - 签名。

**返回值:** `bool` - 签名是否存在。

**用法示例:**
```csharp
if (gameDataService.TryGetSignature("MySignature", out nint sig)) { }
```

### HasOffset

```csharp
bool HasOffset(string offsetName)
```

检查偏移量是否存在。

**参数:**

- `offsetName` (`string`) - 偏移量名称在 `offsets.jsonc` 文件中定义。

**返回值:** `bool` - 偏移量是否存在。

**用法示例:**
```csharp
bool exists = gameDataService.HasOffset("player_health");
```

### GetOffset

```csharp
int GetOffset(string offsetName)
```

通过名称获取偏移量。

**参数:**

- `offsetName` (`string`) - 偏移量名称在 `offsets.jsonc` 文件中定义。

**返回值:** `int` - 偏移量。

**用法示例:**
```csharp
int offset = gameDataService.GetOffset("player_health");
```

### TryGetOffset

```csharp
bool TryGetOffset(string offsetName, out nint offset)
```

尝试通过名称获取偏移量。

**参数:**

- `offsetName` (`string`) - 偏移量名称在 `offsets.jsonc` 文件中定义。
- `offset` (`out nint`) - 偏移量。

**返回值:** `bool` - 偏移量是否存在。

**用法示例:**
```csharp
if (gameDataService.TryGetOffset("m_iHealth", out nint offset)) { /* 使用 offset */ }
```

### HasPatch

```csharp
bool HasPatch(string patchName)
```

检查是否存在补丁。

**参数:**

- `patchName` (`string`) - 在 `patchs.jsonc` 文件中定义的补丁名称。

**返回值:** `bool` - 补丁是否存在。

**用法示例:**
```csharp
bool exists = gameDataService.HasPatch("update_v2");
```

### ApplyPatch

```csharp
void ApplyPatch(string patchName)
```

按名称应用补丁。

**参数:**

- `patchName` (`string`) - 在 `patchs.jsonc` 文件中定义的补丁名称。

**用法示例:**
```csharp
gameDataService.ApplyPatch("fix_crash_v1");
```

