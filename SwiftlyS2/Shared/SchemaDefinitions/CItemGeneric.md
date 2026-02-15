# 🔌 CItemGeneric

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CItem`

**实现接口:** `ISchemaClass\<CItemGeneric\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HasTriggerRadius` | `ref bool` | get | - |
| `HasPickupRadius` | `ref bool` | get | - |
| `PickupRadiusSqr` | `ref float` | get | - |
| `TriggerRadiusSqr` | `ref float` | get | - |
| `LastPickupCheck` | `GameTime_t` | get | - |
| `PlayerCounterListenerAdded` | `ref bool` | get | - |
| `PlayerInTriggerRadius` | `ref bool` | get | - |
| `SpawnParticleEffect` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `AmbientSoundEffect` | `string` | get, set | - |
| `AutoStartAmbientSound` | `ref bool` | get | - |
| `SpawnScriptFunction` | `string` | get, set | - |
| `PickupParticleEffect` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `PickupSoundEffect` | `string` | get, set | - |
| `PickupScriptFunction` | `string` | get, set | - |
| `TimeoutParticleEffect` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `TimeoutSoundEffect` | `string` | get, set | - |
| `TimeoutScriptFunction` | `string` | get, set | - |
| `PickupFilterName` | `string` | get, set | - |
| `PickupFilter` | `ref CHandle\<CBaseFilter\>` | get | - |
| `OnPickup` | `ref CEntityIOOutput` | get | - |
| `OnTimeout` | `ref CEntityIOOutput` | get | - |
| `OnTriggerStartTouch` | `ref CEntityIOOutput` | get | - |
| `OnTriggerTouch` | `ref CEntityIOOutput` | get | - |
| `OnTriggerEndTouch` | `ref CEntityIOOutput` | get | - |
| `AllowPickupScriptFunction` | `string` | get, set | - |
| `PickupRadius` | `ref float` | get | - |
| `TriggerRadius` | `ref float` | get | - |
| `TriggerSoundEffect` | `string` | get, set | - |
| `GlowWhenInTrigger` | `ref bool` | get | - |
| `GlowColor` | `ref Color` | get | - |
| `Useable` | `ref bool` | get | - |
| `TriggerHelper` | `ref CHandle\<CItemGenericTriggerHelper\>` | get | - |

