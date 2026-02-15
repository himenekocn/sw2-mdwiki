# 🔌 CGameRules

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CGameRules\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `QuestName` | `string` | get, set | - |
| `QuestPhase` | `ref int` | get | - |
| `TotalPausedTicks` | `ref int` | get | - |
| `PauseStartTick` | `ref int` | get | - |
| `GamePaused` | `ref bool` | get | - |

## ⚙️ 方法

### TotalPausedTicksUpdated

```csharp
void TotalPausedTicksUpdated()
```

### PauseStartTickUpdated

```csharp
void PauseStartTickUpdated()
```

### GamePausedUpdated

```csharp
void GamePausedUpdated()
```

