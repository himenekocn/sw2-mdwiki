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
Ray_t ray;  
ray.Init(new Vector(1f, 2f, 3f));
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
Ray_t ray;  
ray.Init(new Vector(0, 0, 0), 1.0f);
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
Ray_t ray;  
ray.Init(Vector.Zero, Vector.One);
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
Ray_t ray;  
ray.Init(new Vector(0f, 0f, 0f), new Vector(1f, 1f, 1f), 5.0f);
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
Ray_t.Init(Vector.Zero, Vector.One, null, 0);
```

