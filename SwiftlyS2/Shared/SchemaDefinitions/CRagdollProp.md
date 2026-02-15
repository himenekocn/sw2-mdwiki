# 🔌 CRagdollProp

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseAnimGraph`

**实现接口:** `ISchemaClass\<CRagdollProp\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ragdoll` | `ragdoll_t` | get | - |
| `StartDisabled` | `ref bool` | get | - |
| `RagEnabled` | `ref CUtlVector\<bool\>` | get | - |
| `RagPos` | `ref CUtlVector\<Vector\>` | get | - |
| `RagAngles` | `ref CUtlVector\<QAngle\>` | get | - |
| `LastUpdateTickCount` | `ref uint` | get | - |
| `AllAsleep` | `ref bool` | get | - |
| `FirstCollisionAfterLaunch` | `ref bool` | get | - |
| `DamageEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Killer` | `ref CHandle\<CBaseEntity\>` | get | - |
| `PhysicsAttacker` | `ref CHandle\<CBasePlayerPawn\>` | get | - |
| `LastPhysicsInfluenceTime` | `GameTime_t` | get | - |
| `FadeOutStartTime` | `GameTime_t` | get | - |
| `FadeTime` | `ref float` | get | - |
| `LastOrigin` | `ref Vector` | get | - |
| `AwakeTime` | `GameTime_t` | get | - |
| `LastOriginChangeTime` | `GameTime_t` | get | - |
| `StrOriginClassName` | `string` | get, set | - |
| `StrSourceClassName` | `string` | get, set | - |
| `HasBeenPhysgunned` | `ref bool` | get | - |
| `AllowStretch` | `ref bool` | get | - |
| `BlendWeight` | `ref float` | get | - |
| `DefaultFadeScale` | `ref float` | get | - |
| `RagdollMins` | `ref CUtlVector\<Vector\>` | get | - |
| `RagdollMaxs` | `ref CUtlVector\<Vector\>` | get | - |
| `ShouldDeleteActivationRecord` | `ref bool` | get | - |

## ⚙️ 方法

### RagEnabledUpdated

```csharp
void RagEnabledUpdated()
```

### RagPosUpdated

```csharp
void RagPosUpdated()
```

### RagAnglesUpdated

```csharp
void RagAnglesUpdated()
```

### BlendWeightUpdated

```csharp
void BlendWeightUpdated()
```

