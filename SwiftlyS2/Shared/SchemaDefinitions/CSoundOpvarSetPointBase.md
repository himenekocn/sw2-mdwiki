# 🔌 CSoundOpvarSetPointBase

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CSoundOpvarSetPointBase\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Disabled` | `ref bool` | get | - |
| `Source` | `ref CHandle\<CEntityInstance\>` | get | - |
| `SourceEntityName` | `string` | get, set | - |
| `LastPosition` | `ref Vector` | get | - |
| `RefreshTime` | `ref float` | get | - |
| `StackName` | `string` | get, set | - |
| `OperatorName` | `string` | get, set | - |
| `OpvarName` | `string` | get, set | - |
| `OpvarIndex` | `ref int` | get | - |
| `UseAutoCompare` | `ref bool` | get | - |
| `FastRefresh` | `ref bool` | get | - |

## ⚙️ 方法

### StackNameUpdated

```csharp
void StackNameUpdated()
```

### OperatorNameUpdated

```csharp
void OperatorNameUpdated()
```

### OpvarNameUpdated

```csharp
void OpvarNameUpdated()
```

### OpvarIndexUpdated

```csharp
void OpvarIndexUpdated()
```

### UseAutoCompareUpdated

```csharp
void UseAutoCompareUpdated()
```

### FastRefreshUpdated

```csharp
void FastRefreshUpdated()
```

