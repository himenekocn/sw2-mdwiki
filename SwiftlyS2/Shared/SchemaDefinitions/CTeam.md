# 🔌 CTeam

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CTeam\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerControllers` | `ref CUtlVector\<CHandle\<CBasePlayerController\>\>` | get | - |
| `Players` | `ref CUtlVector\<CHandle\<CBasePlayerPawn\>\>` | get | - |
| `Score` | `ref int` | get | - |
| `Teamname` | `string` | get, set | - |

## ⚙️ 方法

### PlayerControllersUpdated

```csharp
void PlayerControllersUpdated()
```

### PlayersUpdated

```csharp
void PlayersUpdated()
```

### ScoreUpdated

```csharp
void ScoreUpdated()
```

### TeamnameUpdated

```csharp
void TeamnameUpdated()
```

