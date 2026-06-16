<a id="physsurfacepropertiestrace"></a>

# 📦 PhysSurfacePropertiesTrace

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `class`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 表面的名称。 |
| `NameHash` | `uint` | get, set | 表面名称的哈希值，用于加速查找。 |
| `BaseNameHash` | `uint` | get, set | 此表面派生于基础表面名称的哈希值。 |
| `ListIndex` | `int` | get, set | 该材质在材质列表中的索引。 |
| `BaseListIndex` | `int` | get, set | 材质列表中基础表面的索引。 |
| `Hidden` | `bool` | get, set | 指示此表面是隐藏还是内部。 |
| `Description` | `string` | get, set | 该表面及其属性的描述。 |
| `Physics` | `PhysSurfacePropertiesPhysicsTrace?` | get, set | 该表面的物理属性。 |
| `AudioSounds` | `PhysSurfacePropertiesSoundNamesTrace?` | get, set | 与此表面上的交互相关联的声音名称。 |
| `AudioParams` | `PhysSurfacePropertiesAudioTrace?` | get, set | 该表面的音频处理参数。 |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

