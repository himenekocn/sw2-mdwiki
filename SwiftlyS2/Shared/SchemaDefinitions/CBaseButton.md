# 🔌 CBaseButton

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseToggle`

**实现接口:** `ISchemaClass\<CBaseButton\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MoveEntitySpace` | `ref QAngle` | get | - |
| `StayPushed` | `ref bool` | get | - |
| `Rotating` | `ref bool` | get | - |
| `Ls` | `locksound_t` | get | - |
| `UseSound` | `string` | get, set | - |
| `LockedSound` | `string` | get, set | - |
| `UnlockedSound` | `string` | get, set | - |
| `OverrideAnticipationName` | `string` | get, set | - |
| `Locked` | `ref bool` | get | - |
| `Disabled` | `ref bool` | get | - |
| `UseLockedTime` | `GameTime_t` | get | - |
| `SolidBsp` | `ref bool` | get | - |
| `OnDamaged` | `ref CEntityIOOutput` | get | - |
| `OnPressed` | `ref CEntityIOOutput` | get | - |
| `OnUseLocked` | `ref CEntityIOOutput` | get | - |
| `OnIn` | `ref CEntityIOOutput` | get | - |
| `OnOut` | `ref CEntityIOOutput` | get | - |
| `State` | `ref int` | get | - |
| `Constraint` | `ref CHandle\<CEntityInstance\>` | get | - |
| `ConstraintParent` | `ref CHandle\<CEntityInstance\>` | get | - |
| `ForceNpcExclude` | `ref bool` | get | - |
| `GlowEntity` | `string` | get, set | - |
| `GlowEntity1` | `ref CHandle\<CBaseModelEntity\>` | get | - |
| `Usable` | `ref bool` | get | - |
| `DisplayText` | `string` | get, set | - |

## ⚙️ 方法

### GlowEntity1Updated

```csharp
void GlowEntity1Updated()
```

### UsableUpdated

```csharp
void UsableUpdated()
```

### DisplayTextUpdated

```csharp
void DisplayTextUpdated()
```

