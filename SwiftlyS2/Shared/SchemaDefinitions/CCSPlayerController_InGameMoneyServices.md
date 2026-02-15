# 🔌 CCSPlayerController_InGameMoneyServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerControllerComponent`

**实现接口:** `ISchemaClass\<CCSPlayerController_InGameMoneyServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ReceivesMoneyNextRound` | `ref bool` | get | - |
| `MoneyEarnedForNextRound` | `ref int` | get | - |
| `Account` | `ref int` | get | - |
| `StartAccount` | `ref int` | get | - |
| `TotalCashSpent` | `ref int` | get | - |
| `CashSpentThisRound` | `ref int` | get | - |

## ⚙️ 方法

### AccountUpdated

```csharp
void AccountUpdated()
```

### StartAccountUpdated

```csharp
void StartAccountUpdated()
```

### TotalCashSpentUpdated

```csharp
void TotalCashSpentUpdated()
```

### CashSpentThisRoundUpdated

```csharp
void CashSpentThisRoundUpdated()
```

