# 🔌 CNetworkedSequenceOperation

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CNetworkedSequenceOperation\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Sequence` | `HSequence` | get | - |
| `PrevCycle` | `ref float` | get | - |
| `Cycle` | `ref float` | get | - |
| `Weight` | `ref CNetworkedQuantizedFloat` | get | - |
| `SequenceChangeNetworked` | `ref bool` | get | - |
| `Discontinuity` | `ref bool` | get | - |
| `PrevCycleFromDiscontinuity` | `ref float` | get | - |
| `PrevCycleForAnimEventDetection` | `ref float` | get | - |

## ⚙️ 方法

### SequenceUpdated

```csharp
void SequenceUpdated()
```

### PrevCycleUpdated

```csharp
void PrevCycleUpdated()
```

### CycleUpdated

```csharp
void CycleUpdated()
```

### WeightUpdated

```csharp
void WeightUpdated()
```

