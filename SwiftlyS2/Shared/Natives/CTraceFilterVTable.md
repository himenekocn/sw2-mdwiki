# 📦 CTraceFilterVTable

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `pCTraceFilterVTable` | `nint` | static | - |
| `pCTraceFilterShouldHitFunctionCall` | `nint` | static | - |

## ⚙️ 方法

### Destructor (静态)

```csharp
void Destructor(CTraceFilter* filter, byte unk01)
```

**参数:**

- `filter` (`CTraceFilter*`)
- `unk01` (`byte`)

### ShouldHitEntity (静态)

```csharp
byte ShouldHitEntity()
```

**返回值:** `byte`

### ShouldHitEntity (静态)

```csharp
byte ShouldHitEntity(CTraceFilter* filter, nint entity)
```

**参数:**

- `filter` (`CTraceFilter*`)
- `entity` (`nint`)

**返回值:** `byte`

