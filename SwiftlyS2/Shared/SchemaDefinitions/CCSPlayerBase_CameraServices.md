# 🔌 CCSPlayerBase_CameraServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayer_CameraServices`

**实现接口:** `ISchemaClass\<CCSPlayerBase_CameraServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FOV` | `ref uint` | get | - |
| `FOVStart` | `ref uint` | get | - |
| `FOVTime` | `GameTime_t` | get | - |
| `FOVRate` | `ref float` | get | - |
| `ZoomOwner` | `ref CHandle\<CBaseEntity\>` | get | - |
| `TriggerFogList` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |
| `LastFogTrigger` | `ref CHandle\<CBaseEntity\>` | get | - |

## ⚙️ 方法

### FOVUpdated

```csharp
void FOVUpdated()
```

### FOVStartUpdated

```csharp
void FOVStartUpdated()
```

### FOVTimeUpdated

```csharp
void FOVTimeUpdated()
```

### FOVRateUpdated

```csharp
void FOVRateUpdated()
```

### ZoomOwnerUpdated

```csharp
void ZoomOwnerUpdated()
```

