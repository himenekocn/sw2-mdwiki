# 🔌 CBaseTrigger

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseToggle`

**实现接口:** `ISchemaClass\<CBaseTrigger\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OnStartTouch` | `ref CEntityIOOutput` | get | - |
| `OnStartTouchAll` | `ref CEntityIOOutput` | get | - |
| `OnEndTouch` | `ref CEntityIOOutput` | get | - |
| `OnEndTouchAll` | `ref CEntityIOOutput` | get | - |
| `OnTouching` | `ref CEntityIOOutput` | get | - |
| `OnTouchingEachEntity` | `ref CEntityIOOutput` | get | - |
| `OnNotTouching` | `ref CEntityIOOutput` | get | - |
| `TouchingEntities` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |
| `FilterName` | `string` | get, set | - |
| `Filter` | `ref CHandle\<CBaseFilter\>` | get | - |
| `Disabled` | `ref bool` | get | - |
| `UseAsyncQueries` | `ref bool` | get | - |

## ⚙️ 方法

### DisabledUpdated

```csharp
void DisabledUpdated()
```

