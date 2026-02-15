# 🔌 CModelState

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CModelState\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Model` | `ref CStrongHandle\<InfoForResourceTypeCModel\>` | get | - |
| `ModelName` | `string` | get, set | - |
| `ClientClothCreationSuppressed` | `ref bool` | get | - |
| `MeshGroupMask` | `ref ulong` | get | - |
| `BodyGroupChoices` | `ref CUtlVector\<int\>` | get | - |
| `IdealMotionType` | `ref byte` | get | - |
| `ForceLOD` | `ref byte` | get | - |
| `ClothUpdateFlags` | `ref byte` | get | - |

## ⚙️ 方法

### ModelUpdated

```csharp
void ModelUpdated()
```

### ClientClothCreationSuppressedUpdated

```csharp
void ClientClothCreationSuppressedUpdated()
```

### MeshGroupMaskUpdated

```csharp
void MeshGroupMaskUpdated()
```

### BodyGroupChoicesUpdated

```csharp
void BodyGroupChoicesUpdated()
```

### IdealMotionTypeUpdated

```csharp
void IdealMotionTypeUpdated()
```

