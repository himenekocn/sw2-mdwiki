# 🔌 CPlayerPing

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CPlayerPing\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Player` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `PingedEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Type` | `ref int` | get | - |
| `Urgent` | `ref bool` | get | - |
| `PlaceName` | `string` | get, set | - |

## ⚙️ 方法

### PlayerUpdated

```csharp
void PlayerUpdated()
```

### PingedEntityUpdated

```csharp
void PingedEntityUpdated()
```

### TypeUpdated

```csharp
void TypeUpdated()
```

### UrgentUpdated

```csharp
void UrgentUpdated()
```

### PlaceNameUpdated

```csharp
void PlaceNameUpdated()
```

