# 🔌 CBeam

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CBeam\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FrameRate` | `ref float` | get | - |
| `HDRColorScale` | `ref float` | get | - |
| `FireTime` | `GameTime_t` | get | - |
| `Damage` | `ref float` | get | - |
| `NumBeamEnts` | `ref byte` | get | - |
| `BaseMaterial` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |
| `HaloIndex` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |
| `BeamType` | `ref BeamType_t` | get | - |
| `BeamFlags` | `ref uint` | get | - |
| `AttachEntity` | `ISchemaFixedArray\<CHandle\<CBaseEntity\>\>` | get | - |
| `AttachIndex` | `ISchemaClassFixedArray\<AttachmentHandle_t\>` | get | - |
| `Width` | `ref float` | get | - |
| `EndWidth` | `ref float` | get | - |
| `FadeLength` | `ref float` | get | - |
| `HaloScale` | `ref float` | get | - |
| `Amplitude` | `ref float` | get | - |
| `StartFrame` | `ref float` | get | - |
| `Speed` | `ref float` | get | - |
| `Frame` | `ref float` | get | - |
| `ClipStyle` | `ref BeamClipStyle_t` | get | - |
| `TurnedOff` | `ref bool` | get | - |
| `EndPos` | `ref Vector` | get | - |
| `EndEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `DissolveType` | `ref int` | get | - |

## ⚙️ 方法

### FrameRateUpdated

```csharp
void FrameRateUpdated()
```

### HDRColorScaleUpdated

```csharp
void HDRColorScaleUpdated()
```

### NumBeamEntsUpdated

```csharp
void NumBeamEntsUpdated()
```

### BaseMaterialUpdated

```csharp
void BaseMaterialUpdated()
```

### HaloIndexUpdated

```csharp
void HaloIndexUpdated()
```

### BeamTypeUpdated

```csharp
void BeamTypeUpdated()
```

### BeamFlagsUpdated

```csharp
void BeamFlagsUpdated()
```

### AttachEntityUpdated

```csharp
void AttachEntityUpdated()
```

### AttachIndexUpdated

```csharp
void AttachIndexUpdated()
```

### WidthUpdated

```csharp
void WidthUpdated()
```

### EndWidthUpdated

```csharp
void EndWidthUpdated()
```

### FadeLengthUpdated

```csharp
void FadeLengthUpdated()
```

### HaloScaleUpdated

```csharp
void HaloScaleUpdated()
```

### AmplitudeUpdated

```csharp
void AmplitudeUpdated()
```

### StartFrameUpdated

```csharp
void StartFrameUpdated()
```

### SpeedUpdated

```csharp
void SpeedUpdated()
```

### FrameUpdated

```csharp
void FrameUpdated()
```

### ClipStyleUpdated

```csharp
void ClipStyleUpdated()
```

### TurnedOffUpdated

```csharp
void TurnedOffUpdated()
```

### EndPosUpdated

```csharp
void EndPosUpdated()
```

