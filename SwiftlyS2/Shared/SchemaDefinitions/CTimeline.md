# 🔌 CTimeline

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `IntervalTimer`

**实现接口:** `ISchemaClass\<CTimeline\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Values` | `ISchemaFixedArray\<float\>` | get | - |
| `ValueCounts` | `ISchemaFixedArray\<int\>` | get | - |
| `BucketCount` | `ref int` | get | - |
| `Interval` | `ref float` | get | - |
| `FinalValue` | `ref float` | get | - |
| `CompressionType` | `ref TimelineCompression_t` | get | - |
| `Stopped` | `ref bool` | get | - |

## ⚙️ 方法

### ValuesUpdated

```csharp
void ValuesUpdated()
```

### ValueCountsUpdated

```csharp
void ValueCountsUpdated()
```

### BucketCountUpdated

```csharp
void BucketCountUpdated()
```

### IntervalUpdated

```csharp
void IntervalUpdated()
```

### FinalValueUpdated

```csharp
void FinalValueUpdated()
```

### CompressionTypeUpdated

```csharp
void CompressionTypeUpdated()
```

### StoppedUpdated

```csharp
void StoppedUpdated()
```

