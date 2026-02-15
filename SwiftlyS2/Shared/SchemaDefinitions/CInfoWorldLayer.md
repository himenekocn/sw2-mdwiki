# 🔌 CInfoWorldLayer

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CInfoWorldLayer\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OutputOnEntitiesSpawned` | `ref CEntityIOOutput` | get | - |
| `WorldName` | `string` | get, set | - |
| `LayerName` | `string` | get, set | - |
| `WorldLayerVisible` | `ref bool` | get | - |
| `EntitiesSpawned` | `ref bool` | get | - |
| `CreateAsChildSpawnGroup` | `ref bool` | get | - |
| `LayerSpawnGroup` | `ref uint` | get | - |

## ⚙️ 方法

### WorldNameUpdated

```csharp
void WorldNameUpdated()
```

### LayerNameUpdated

```csharp
void LayerNameUpdated()
```

### WorldLayerVisibleUpdated

```csharp
void WorldLayerVisibleUpdated()
```

### EntitiesSpawnedUpdated

```csharp
void EntitiesSpawnedUpdated()
```

