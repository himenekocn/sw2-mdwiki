# 📦 GameDataService

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `IGameDataService`

## ⚙️ 方法

### HasSignature

```csharp
bool HasSignature(string signatureName)
```

**参数:**

- `signatureName` (`string`)

**返回值:** `bool`

### GetSignature

```csharp
nint GetSignature(string signatureName)
```

**参数:**

- `signatureName` (`string`)

**返回值:** `nint`

### TryGetSignature

```csharp
bool TryGetSignature(string signatureName, out nint signature)
```

**参数:**

- `signatureName` (`string`)
- `signature` (`out nint`)

**返回值:** `bool`

### HasOffset

```csharp
bool HasOffset(string offsetName)
```

**参数:**

- `offsetName` (`string`)

**返回值:** `bool`

### GetOffset

```csharp
int GetOffset(string offsetName)
```

**参数:**

- `offsetName` (`string`)

**返回值:** `int`

### TryGetOffset

```csharp
bool TryGetOffset(string offsetName, out nint offset)
```

**参数:**

- `offsetName` (`string`)
- `offset` (`out nint`)

**返回值:** `bool`

### HasPatch

```csharp
bool HasPatch(string patchName)
```

**参数:**

- `patchName` (`string`)

**返回值:** `bool`

### ApplyPatch

```csharp
void ApplyPatch(string patchName)
```

**参数:**

- `patchName` (`string`)

