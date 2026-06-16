<a id="cbitvec4096"></a>

# 🏗️ CBitVec4096

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `ICBitVec`

## ⚙️ 方法

### ClearAll

```csharp
void ClearAll()
```

**用法示例:**
```csharp
bitVec.ClearAll();
```

### SetAll

```csharp
void SetAll()
```

**用法示例:**
```csharp
bitVec.SetAll();
```

### Set

```csharp
void Set(uint index)
```

**参数:**

- `index` (`uint`)

**用法示例:**
```csharp
CBitVec4096 bitVec;
bitVec.Set(10);
```

### Set

```csharp
void Set(int index)
```

**参数:**

- `index` (`int`)

**用法示例:**
```csharp
CBitVec4096 bitVec;
bitVec.Set(10);
```

### Clear

```csharp
void Clear(uint index)
```

**参数:**

- `index` (`uint`)

**用法示例:**
```csharp
bitVec.Clear(0);
```

### Clear

```csharp
void Clear(int index)
```

**参数:**

- `index` (`int`)

**用法示例:**
```csharp
bitVec.Clear(0);
```

### IsSet

```csharp
bool IsSet(uint index)
```

**参数:**

- `index` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isSet = someBitVec.IsSet(10);
```

### IsSet

```csharp
bool IsSet(int index)
```

**参数:**

- `index` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isSet = bitVec.IsSet(10);
```

### Count

```csharp
int Count()
```

**返回值:** `int`

**用法示例:**
```csharp
int count = bitVec.Count();
```

### IsAllClear

```csharp
bool IsAllClear()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isClear = bitVec.IsAllClear();
```

