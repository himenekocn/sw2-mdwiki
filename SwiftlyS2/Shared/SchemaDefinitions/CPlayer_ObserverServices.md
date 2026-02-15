# 🔌 CPlayer_ObserverServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerPawnComponent`

**实现接口:** `ISchemaClass\<CPlayer_ObserverServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ObserverMode` | `ref byte` | get | - |
| `ObserverTarget` | `ref CHandle\<CBaseEntity\>` | get | - |
| `ObserverLastMode` | `ref ObserverMode_t` | get | - |
| `ForcedObserverMode` | `ref bool` | get | - |

## ⚙️ 方法

### ObserverModeUpdated

```csharp
void ObserverModeUpdated()
```

### ObserverTargetUpdated

```csharp
void ObserverTargetUpdated()
```

