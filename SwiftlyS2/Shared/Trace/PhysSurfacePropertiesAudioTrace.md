<a id="physsurfacepropertiesaudiotrace"></a>

# 🏗️ PhysSurfacePropertiesAudioTrace

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `struct`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reflectivity` | `float` | get, set | 表面的音频反射率，影响声音在其上的反射效果。 |
| `HardnessFactor` | `float` | get, set | 用于音频处理的表面硬度系数。 |
| `RoughnessFactor` | `float` | get, set | 用于音频处理的表面粗糙度系数。 |
| `RoughThreshold` | `float` | get, set | 音频处理中粗糙度的阈值。 |
| `HardThreshold` | `float` | get, set | 音频处理中的硬度阈值。 |
| `HardVelocityThreshold` | `float` | get, set | 音频处理中硬表面撞击的速度阈值。 |
| `StaticImpactVolume` | `float` | get, set | 此表面的静态撞击体积。 |
| `OcclusionFactor` | `float` | get, set | 音频的遮挡因子，影响声音穿过或绕过表面时的传播方式。 |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

