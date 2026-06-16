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

- `signatureName` (`string`) - `signatures.jsonc` 文件中定义的签名名称。

**返回值:** `bool` - 签名是否存在。

**用法示例:**
```csharp
bool exists = gameDataService.HasSignature("player_join");
```

### GetSignature

```csharp
nint GetSignature(string signatureName)
```

根据名称获取签名。

**参数:**

- `signatureName` (`string`) - `signatures.jsonc` 文件中定义的签名名称。

**返回值:** `nint` - 签名。

**用法示例:**
```csharp
nint sig = gameDataService.GetSignature("player_jump");
```

### TryGetSignature

```csharp
bool TryGetSignature(string signatureName, out nint signature)
```

尝试通过名称获取签名。

**参数:**

- `signatureName` (`string`) - `signatures.jsonc` 文件中定义的签名名称。
- `signature` (`out nint`) - 签名。

**返回值:** `bool` - 签名是否存在。

**用法示例:**
```csharp
bool success = gameDataService.TryGetSignature("example_sig", out nint signature);
```

### HasOffset

```csharp
bool HasOffset(string offsetName)
```

检查偏移量是否存在。

**参数:**

- `offsetName` (`string`) - 在 `offsets.jsonc` 文件中定义的偏移量名称。

**返回值:** `bool` - 偏移量是否存在。

**用法示例:**
```csharp
bool exists = gameDataService.HasOffset("player_health");
```

### GetOffset

```csharp
int GetOffset(string offsetName)
```

根据名称获取偏移量。

**参数:**

- `offsetName` (`string`) - 在 `offsets.jsonc` 文件中定义的偏移量名称。

**返回值:** `int` - 偏移。

**用法示例:**
```csharp
int offset = gameDataService.GetOffset("player_health");
```

### TryGetOffset

```csharp
bool TryGetOffset(string offsetName, out nint offset)
```

根据名称尝试获取偏移量。

**参数:**

- `offsetName` (`string`) - 在 `offsets.jsonc` 文件中定义的偏移量名称。
- `offset` (`out nint`) - 偏移。

**返回值:** `bool` - 偏移量是否存在。

**用法示例:**
```csharp
bool found = gameDataService.TryGetOffset("m_iHealth", out nint offset);
```

### HasPatch

```csharp
bool HasPatch(string patchName)
```

检查补丁是否存在。

**参数:**

- `patchName` (`string`) - 在 `patches.jsonc` 文件中定义的补丁名称。

**返回值:** `bool` - 补丁是否存在。

**用法示例:**
```csharp
bool exists = gameDataService.HasPatch("v1.0");
```

### ApplyPatch

```csharp
void ApplyPatch(string patchName)
```

应用指定名称的补丁。

**参数:**

- `patchName` (`string`) - 在 `patches.jsonc` 文件中定义的补丁名称。

**用法示例:**
```csharp
gameDataService.ApplyPatch("v1.0.1");
```

### RevertPatch

```csharp
void RevertPatch(string patchName)
```

根据名称还原一个补丁。

**参数:**

- `patchName` (`string`) - 在 `patches.jsonc` 文件中定义的补丁名称。

**用法示例:**
```csharp
gameDataService.RevertPatch("patch_v1.2");
```

