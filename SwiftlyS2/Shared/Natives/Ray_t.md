# 🏗️ Ray_t

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## ⚙️ 方法

### Init

```csharp
void Init(Vector StartOffset)
```

**参数:**

- `StartOffset` (`Vector`)

**用法示例:**
```csharp
Ray_t ray; ray.Init(Vector.Zero);
```

### Init

```csharp
void Init(Vector Center, float Radius)
```

**参数:**

- `Center` (`Vector`)
- `Radius` (`float`)

**用法示例:**
```csharp
Ray_t ray; ray.Init(Vector.Zero, 10.0f);
```

### Init

```csharp
void Init(Vector Mins, Vector Maxs)
```

**参数:**

- `Mins` (`Vector`)
- `Maxs` (`Vector`)

**用法示例:**
```csharp
Ray_t ray; ray.Init(Vector.Zero, Vector.One);
```

### Init

```csharp
void Init(Vector CenterA, Vector CenterB, float Radius)
```

**参数:**

- `CenterA` (`Vector`)
- `CenterB` (`Vector`)
- `Radius` (`float`)

**用法示例:**
```csharp
Ray_t ray; ray.Init(Vector.Zero, Vector.UnitX, 1.0f);
```

### Init

```csharp
void Init(Vector Mins, Vector Maxs, Vector* Vertices, int NumVertices)
```

**参数:**

- `Mins` (`Vector`)
- `Maxs` (`Vector`)
- `Vertices` (`Vector*`)
- `NumVertices` (`int`)

**用法示例:**
```csharp
Ray_t ray; ray.Init(Vector.Zero, Vector.One, null, 0);
```

