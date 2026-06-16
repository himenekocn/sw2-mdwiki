<a id="schemainfo"></a>

# 📦 SchemaInfo

**命名空间:** `SwiftlyS2.Shared.Schemas`

**类型:** `class`

## ⚙️ 方法

### GetSize<T> (静态)

```csharp
int GetSize<T>()
```

**返回值:** `int`

**用法示例:**
```csharp
int size = SchemaInfo.GetSize<CBasePlayer>();
```

### Get<T> (静态)

```csharp
int Get<T>()
```

**返回值:** `int`

**用法示例:**
```csharp
int id = SchemaInfo.Get<Player>();
```

### IsSchemaClass<T> (静态)

```csharp
bool IsSchemaClass<T>()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isSchema = SchemaInfo.IsSchemaClass<CBasePlayer>();
```

