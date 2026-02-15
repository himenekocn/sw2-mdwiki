# 🔌 CEnvWindShared

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CEnvWindShared\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StartTime` | `GameTime_t` | get | - |
| `WindSeed` | `ref uint` | get | - |
| `MinWind` | `ref ushort` | get | - |
| `MaxWind` | `ref ushort` | get | - |
| `WindRadius` | `ref int` | get | - |
| `MinGust` | `ref ushort` | get | - |
| `MaxGust` | `ref ushort` | get | - |
| `MinGustDelay` | `ref float` | get | - |
| `MaxGustDelay` | `ref float` | get | - |
| `GustDuration` | `ref float` | get | - |
| `GustDirChange` | `ref ushort` | get | - |
| `InitialWindDir` | `ref ushort` | get | - |
| `InitialWindSpeed` | `ref float` | get | - |
| `Location` | `ref Vector` | get | - |
| `OnGustStart` | `ref CEntityIOOutput` | get | - |
| `OnGustEnd` | `ref CEntityIOOutput` | get | - |
| `EntOwner` | `ref CHandle\<CBaseEntity\>` | get | - |

## ⚙️ 方法

### StartTimeUpdated

```csharp
void StartTimeUpdated()
```

### WindSeedUpdated

```csharp
void WindSeedUpdated()
```

### MinWindUpdated

```csharp
void MinWindUpdated()
```

### MaxWindUpdated

```csharp
void MaxWindUpdated()
```

### WindRadiusUpdated

```csharp
void WindRadiusUpdated()
```

### MinGustUpdated

```csharp
void MinGustUpdated()
```

### MaxGustUpdated

```csharp
void MaxGustUpdated()
```

### MinGustDelayUpdated

```csharp
void MinGustDelayUpdated()
```

### MaxGustDelayUpdated

```csharp
void MaxGustDelayUpdated()
```

### GustDurationUpdated

```csharp
void GustDurationUpdated()
```

### GustDirChangeUpdated

```csharp
void GustDirChangeUpdated()
```

### InitialWindDirUpdated

```csharp
void InitialWindDirUpdated()
```

### InitialWindSpeedUpdated

```csharp
void InitialWindSpeedUpdated()
```

### LocationUpdated

```csharp
void LocationUpdated()
```

