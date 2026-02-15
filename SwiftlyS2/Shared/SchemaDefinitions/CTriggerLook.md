# 🔌 CTriggerLook

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CTriggerOnce`

**实现接口:** `ISchemaClass\<CTriggerLook\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LookTarget` | `ref CHandle\<CBaseEntity\>` | get | - |
| `FieldOfView` | `ref float` | get | - |
| `LookTime` | `ref float` | get | - |
| `LookTimeTotal` | `ref float` | get | - |
| `LookTimeLast` | `GameTime_t` | get | - |
| `TimeoutDuration` | `ref float` | get | - |
| `TimeoutFired` | `ref bool` | get | - |
| `IsLooking` | `ref bool` | get | - |
| `B2DFOV` | `ref bool` | get | - |
| `UseVelocity` | `ref bool` | get | - |
| `TestOcclusion` | `ref bool` | get | - |
| `TestAllVisibleOcclusion` | `ref bool` | get | - |
| `OnTimeout` | `ref CEntityIOOutput` | get | - |
| `OnStartLook` | `ref CEntityIOOutput` | get | - |
| `OnEndLook` | `ref CEntityIOOutput` | get | - |

## ⚙️ 方法

### TestOcclusionUpdated

```csharp
void TestOcclusionUpdated()
```

### TestAllVisibleOcclusionUpdated

```csharp
void TestAllVisibleOcclusionUpdated()
```

