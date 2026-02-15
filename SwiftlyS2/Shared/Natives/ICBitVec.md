# 🔌 ICBitVec

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

## ⚙️ 方法

### IsFixedSize

```csharp
bool IsFixedSize()
```

**返回值:** `bool`

**用法示例:**
```csharp
ICBitVec instance = GetSomeInstance();  
bool fixedSize = instance.IsFixedSize();
```

### NumDWords

```csharp
uint NumDWords()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint count = ICBitVec.NumDWords();
```

### GetNumBits

```csharp
uint GetNumBits()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint bitCount = convar.GetNumBits();
```

### ClearAll

```csharp
void ClearAll()
```

**用法示例:**
```csharp
icBitVec.ClearAll();
```

### SetAll

```csharp
void SetAll()
```

**用法示例:**
```csharp
convar.SetAll();
```

### Set

```csharp
void Set(uint index)
```

**参数:**

- `index` (`uint`)

**用法示例:**
```csharp
convar.Set(123);
```

### Set

```csharp
void Set(int index)
```

**参数:**

- `index` (`int`)

**用法示例:**
```csharp
bitVec.Set(5);
```

### Clear

```csharp
void Clear(uint index)
```

**参数:**

- `index` (`uint`)

**用法示例:**
```csharp
bitVec.Clear(5u);
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
bool result = bitVec.IsSet(5);
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
bool result = convar.IsSet(3);
```

### Count

```csharp
int Count()
```

**返回值:** `int`

**用法示例:**
```csharp
int count = convar.BitVec.Count();
```

### IsAllClear

```csharp
bool IsAllClear()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool result = convar.IsAllClear();
```

